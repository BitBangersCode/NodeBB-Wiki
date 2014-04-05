NodeBB supports integration for Facebook, Twitter, and Google through third party plugins:

* `npm install nodebb-plugin-sso-facebook`
* `npm install nodebb-plugin-sso-twitter`
* `npm install nodebb-plugin-sso-google`

After installing and activating them, they require an API key in order to function:

## Facebook

Register an application via the [Facebook Developers](https://developers.facebook.com/) page. A credit card  or mobile phone number may be required in order to create a Developer account.

Create a new application, and obtain an Application Key and Application Secret:

![Facebook Application Settings](http://i.imgur.com/hfy0eVo.png)

Ensure that "Website with Facebook Login" is checked, and that the URL to your NodeBB instance is specified in the "Site URL" box. Add that site's domain to the "App Domains" field.

Paste this key and secret into the appropriate boxes in the NodeBB Administration Panel (accessible via /admin on your NodeBB install)

## Twitter

Register an application at the [Twitter Developers](https://dev.twitter.com/) page. Create a new Application, and obtain the Access Token and Secret:

![Twitter Application Settings](http://i.imgur.com/ksrHkgN.png)

**Important**: While setting up your application, be sure to specify a Callback URL. It does not have to correspond to your installation, it just cannot be blank.

Paste this token and secret into the appropriate boxes in the NodeBB Administration Panel (accessible via /admin on your NodeBB install)

## Google

Register an application at the [Google API Console](https://code.google.com/apis/console/), and obtain a Client ID and Secret.

![Google Application Settings](http://i.imgur.com/xutDs1R.png)

Paste this ID and secret into the appropriate boxes in the NodeBB Administration Panel (accessible via /admin on your NodeBB install)