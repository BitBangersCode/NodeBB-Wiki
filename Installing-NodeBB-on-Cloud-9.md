Installation instructions for the Cloud 9 web based IDE.

Step 1: Clone NodeBB into a new workspace from GitHub.

Step 2: Install redis (Cloud 9 has it's own package manager tool "c9pm")
`c9pm install redis`

Step 3: Run your redis server on port 16379 - port 6379 tends to be already used on Cloud 9. The "&" makes the command run in the background. You can always terminate the process later. $IP is a Cloud 9 system variable containing the global ip of your server instance.
`redis-server --port 16379 --bind $IP &`

Step 4: Find out your instance's ip address so NodeBB can bind to it correctly. This is one of Cloud 9's demands and seems to be the only way it will work. You can't use $IP in your config.json either (which means you can't enter $IP in the node app --setup).
`echo $IP`

Step 5: Install NodeBB and it's dependencies:
`npm install`

Step 6: Run the nodebb setup utility:
`node app --setup`

URL of this installation should be set to 'http://workspace_name-c9-username.c9.io', replacing workspace_name with your workspace name and username with your username. Note that as NodeBB is currently using unsecure http for loading jQuery you will find it much easier using http:// instead of https:// for your base url. Otherwise jQuery won't load and NodeBB will break.

Port number isn't so important - Cloud9 will force you to use port 80 anyway. Just set it to 80.

Use a port number to acces NodeBB? Again, this doesn't seem to make a big difference. Set this to no. Either will work.

Host IP or address of your Redis instance: localhost
Host port of your Redis instance: 16379
IP or Hostname to bind to: 123.4.567.8 (enter what your $IP value holds here found in step 4).

And you're good to go! Don't use the Run button at the top if the IDE, it has been a little buggy for me. Besides, you're better off using the command line anyway. Run:
`node app`

And then open http://workspace_name-c9-username.c9.io in your browser.