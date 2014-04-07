sidebar-sdk
===========
#ScribbleLive Iframe Sidebar implementation instructions.

= ScribbleLive Iframe Sidebar =

  * Create a page which returns a page with HTML structure shown in the example HTML page (in the *Downloads* section). This page will be shown in an iframe in the right side bar of an event. This page can be preceded by any login and/or search functionality. See [HTMLDetails] page for more information. *IMPORTANT:* The page needs to be secure, ie. hosted on HTTPS, since web browsers will not allow non secure content to be loaded from our secure site.

<img src="http://s3.amazonaws.com/customerfiles.scribblelive.com/sidebarsdk/devsettings.jpg"/>

  * From the Dashboard, on the left hand menu under Admin click Global Settings. On the bottom of that page there is a section called Developer Settings. Enter a name for the iframe and an URL for it.

  * Then you can go to an event click the tab on the sidebar. From the dropdown select the iframe you just entered in the settings.

<img src="http://s3.amazonaws.com/customerfiles.scribblelive.com/sidebarsdk/sidebar_select.jpg"/>

  * Click the Advanced tab above post box. Now you can drag items from the iframe into the post box.

<img src="http://s3.amazonaws.com/customerfiles.scribblelive.com/sidebarsdk/adv_post.jpg"/>


Note: some browsers don't always refresh the iframe content on page reload. If that happens clear the browser cache.
