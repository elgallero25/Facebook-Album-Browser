Facebook-Album-Browser
======================

Reponsive jQuery plugin for browsing public albums of a Facebook account.
Plugin is suitable for both desktop and mobile websites.

###What can I do with it
The main purpose of this plugin is to enable to embed and customize phot albums in your website without being limited with Facebook styling. It also allows you to use it as picker as it raises events for clicked album/photo.

###How to add to a page
Add a reference to jQuery library, this plugin library and this plugin CSS stylesheet
```html
<link rel="stylesheet" type="text/css" href="../src/jquery.fb.albumbrowser.css" />
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.11.0/jquery.min.js"></script>
<script type="text/javascript" src="../src/jquery.fb.albumbrowser.js"></script>
```
Simply add a container (div or any other element) and apply the plugin to it.
```html
<div class="fb-album-container"></div>

<script type="text/javascript">
    $(document).ready(function () {
        $(".fb-album-container").FacebookAlbumBrowser({
            account: "natgeo"
        });
    });
</script>
```

###What are options for plugin
The following are options for the plugin which are used to congigure the plugin instance:
* **account** - Facebook account for which albums and photos will be fetched and displayed. This parameter is mandatory and must be provided in order for plugin to work.
* **acessToken** - Access token for accessing non public content for the facebook account.
* **showAccountInfo** - Show Facebook account name and icon abowe the browser. Default value is _true_
* **showImageCount** - Show number of protos in each album. Default value is _true_
* **skipEmptyAlbums** - Skip albums for which plugin was unable to fetch at least one photo. Default value is _true_
* **skipAlbums** - List of IDs or names or combined IDs and names of albums which will not be browsed (e.g ["Profile Pictures", "Timeline Photos"]). Default value is _[]_
* **lightbox** - Show full size image in a lightbox style when clicked. Default value is _true_
 
###Events
The following are events raised by plugin:
* **albumSelected** - Handler function for event raised when album is selecetd in the browser. Default value is _null_
* **photoSelected** - Handler function for event raised when photo is selecetd in the browser. Default value is _null_

###Demo
[Checkout demo on plunker](http://plnkr.co/edit/bpcaagDgxVClt1lsDH5a?p=preview)

![ScreenShot](http://dejanstojanovic.net/media/31597/facebook-album-browser.png)

###Notes
In order to make this plugin work with Facebook account photos you need to allow **user_photos** permission in your Facebook App that is used to authenticate and add permissions.
Please read the article on Facebook https://developers.facebook.com/docs/apps/review.

For testing purposes you can use Facebook App test users. More about using test users you can find at https://developers.facebook.com/docs/apps/test-users/.
