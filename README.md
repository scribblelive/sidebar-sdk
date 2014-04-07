sidebar-sdk
===========
####ScribbleLive Iframe Sidebar implementation instructions.

  * Create a page which returns a page with HTML structure shown in the example HTML page (in the *Downloads* section). This page will be shown in an iframe in the right side bar of an event. This page can be preceded by any login and/or search functionality.  *IMPORTANT:* The page needs to be secure, ie. hosted on HTTPS, since web browsers will not allow non secure content to be loaded from our secure site.
  * Example:

Below is the HTML code for an item of the list.

data-author and data-avatar are optional and are used to specify the name and the avatar for the author. 
When the item is approved into ScribbleLive that name and avatar are used for the author details.

To set the author information when the item is dragged in use the tags in the "Meta" span.

See sample file for full code. 

```
            <li>
                <div onmousedown="return SCRIBBLE.lib.Library.Drag(event,this);" onmouseover="SCRIBBLE.lib.Library.MouseOverAction(this);" class="Helper" data-author="Sample Author" data-avatar="https://s3.amazonaws.com/avatars.scribblelive.com/2011/6/6/742700e1-c842-4cfe-a60f-10b330674146.png">
                    <iframe width="230" height="114" src="https://www.youtube.com/embed/C_hqVkix6Xo?html5=1" frameborder="0" allowfullscreen></iframe>
                    <div class="Caption">youtube video</div>
                                    <span class="Meta">
                                            <em class="ByLine">by Sample Author</em>
                                            <span class="Source"> YouTube </span>
                                            <span class="Date">Feb 16, 2013</span>
                                    </span>
                            </div>
            </li>
```

<img src="http://s3.amazonaws.com/customerfiles.scribblelive.com/sidebarsdk/devsettings.jpg"/>

  * From the Dashboard, on the left hand menu under Admin click Global Settings. On the bottom of that page there is a section called Developer Settings. Enter a name for the iframe and an URL for it.

  * Then you can go to an event click the tab on the sidebar. From the dropdown select the iframe you just entered in the settings.

<img src="http://s3.amazonaws.com/customerfiles.scribblelive.com/sidebarsdk/sidebar_select.jpg"/>

  * Click the Advanced tab above post box. Now you can drag items from the iframe into the post box.

<img src="http://s3.amazonaws.com/customerfiles.scribblelive.com/sidebarsdk/adv_post.jpg"/>


Note: some browsers don't always refresh the iframe content on page reload. If that happens clear the browser cache.
