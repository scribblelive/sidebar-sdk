sidebar-sdk
===========
####ScribbleLive Iframe Sidebar implementation instructions.

  * Create a page which returns a page with HTML structure shown in the example HTML page (sample.html). This page will be shown in an iframe in the right-hand sidebar of your stream. This page can be preceded by any login and/or search functionality.  *IMPORTANT:* The page needs to be secure, ie. hosted on HTTPS, since web browsers will not allow non secure content to be loaded from our secure site.
  * Example:

Below is the HTML code for an item of the list.

data-author and data-avatar are optional and are used to specify the name and the avatar for the author. 
When the item is approved into ScribbleLive that name and avatar are used for the author details.

To set the author information when the item is dragged in use the tags in the "Meta" span.

See sample file for full code. 

```
            <li>
                <div onmousedown="return SCRIBBLE.lib.Library.Drag(event,this);" onmouseover="SCRIBBLE.lib.Library.MouseOverAction(this);" class="Helper" data-author="Sample Author" data-avatar="https://s3.amazonaws.com/avatars.scribblelive.com/2011/6/6/742700e1-c842-4cfe-a60f-10b330674146.png">
                    <div class="actions">
                        <a class="Approve" onclick="return SCRIBBLE.lib.Library.Post();" title="Publish">✓</a>
                        <a class="SendToRTE" onclick="return SCRIBBLE.lib.Library.SendToRTE();" title="Send to RTE">⇦</a>
                        <a class="SendToModerationHub" onclick="return SCRIBBLE.lib.Library.SendToModerationHub();" title="Send to Moderation Hub">↲</a>
                    </div>
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

<img src="http://s3.amazonaws.com/customerfiles.scribblelive.com/sidebarsdk/2017/Sidebar_SDK_Setup.png"/>

  * From the Dashboard, on the left hand menu under 'Settings' click 'Global Settings'. On that page, there is a section called Developer Settings. Enter a name for your SDK integration and an HTTPs URL that will be loading it.
  
 - Note that it is important that you specify an HTTPs url. Otherwise the iframe may not load.

  * Then go to your stream's Content Studio and click on "..." in the 'Search Content' sidebar. You will see a dropdown showing one or more of the SDK integrations you have specified.

<img src="http://s3.amazonaws.com/customerfiles.scribblelive.com/sidebarsdk/2017/Content_Studio_Sidebar_SDK_Selection.png"/>

  * Once an SDK integration has been selected, you should start seeing all the content your integration offers
  * Click 'Approve' near your content item to publish the content to your stream.
  * Click 'Send to Moderation' near your content item to add the content to the Moderation Hub
  * Click 'Send to RTE' near your content item to add the content to the Rich Text Editor.
  
  Note: 'Send to Moderation' and 'Send to RTE' options are only supported in Content Studio, not in the Standard interface.

<img src="http://s3.amazonaws.com/customerfiles.scribblelive.com/sidebarsdk/2017/Content_Studio_Sidebar_SDK_Approve.png"/>
<img src="http://s3.amazonaws.com/customerfiles.scribblelive.com/sidebarsdk/2017/Content_Studio_Sidebar_SDK_ModHub.png"/>
<img src="http://s3.amazonaws.com/customerfiles.scribblelive.com/sidebarsdk/2017/Content_Studio_Sidebar_SDK_RTE.png"/>

Note: some browsers don't always refresh the iframe content on page reload. If that happens clear the browser cache.
