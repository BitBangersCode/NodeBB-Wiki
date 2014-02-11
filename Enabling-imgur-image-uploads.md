To enable post image attachments, first create an imgur app from :

https://api.imgur.com/oauth2/addclient

You can use : "Anonymous usage without user authorization"

After that you will get a "Client ID". 

Then install the nodebb-plugin-imgur with `npm install nodebb-plugin-imgur`.

Activate the plugin from the control panel and restart NodeBB.

You should see a Imgur menu item in the control panel. Paste the Client ID to the "Imgur Client ID" in the plugin page. Save and you should be able to upload images by dragging them into the composer window.

