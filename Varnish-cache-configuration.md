In order to be sure Varnish will work properly with NodeBB check your ```/etc/varnish/default.vcl``` to make sure its optimized for websockets.

```varnish
backend nodebb {
  .host = "127.0.0.1"; # your app host
  .port = "4567"; # your app port
}

sub vcl_recv {

  # Pipe websocket connections directly to Node.js
  if (req.http.Upgrade ~ "(?i)websocket") {
    set req.backend = nodebb;
    return (pipe);
  }

  # NodeBB
  if (req.http.host == "forum.yourwebsite.com") { # change this to match your host
    if (req.url ~ "^/socket.io/") {
        set req.backend = nodebb;
        return (pipe); # return pass seems not working for websockets
    }
    return (pass); # don't cache
  }

}

sub vcl_pipe {
  # Need to copy the upgrade header
  if (req.http.upgrade) {
    set bereq.http.upgrade = req.http.upgrade;
  }
}
```