# Core-Publisher-Twitter-Homepage-Block-Hack
Adapting the embed code for Twitter's widgets to build a block for Core Publisher's modular responsive homepage.

1 - Have you created the Twitter widget you want to use? Timelines, Likes, Lists, Search or Collections should work. We'll need the embed code, so do that now: https://twitter.com/settings/widgets

2 - You'll get an embed code that will look similar to this:

    <a class="twitter-timeline" data-dnt="true" href="https://twitter.com/hashtag/corgi" data-widget-id="251702382566719490">#corgi Tweets</a>
    <script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0],p=/^http:/.test(d.location)?'http':'https';if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src=p+"://platform.twitter.com/widgets.js";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","twitter-wjs");</script>

Of interest to us is the Data Widget ID and the script. For the embed to work in Core Publisher, you will have to host a copy of the jscript on your own server. Copy everthing between the script tags (leaving the tags themselves out) and save it to a new file (ex: twitter-widget.js) and upload the file. Note the URL path and the Data Widget ID, you'll need them later.

3 – Open Core Publisher, and create a "Small Image Promo" block in the Core Publisher block factory (http://YOUR-URL.org/admin/structure/block-factory/promotional/treatment) [Note: the "Large Image Promo" block also works for this]

4 – Name the block title whichever way you like...

5 – You won't be using a promotional image, so you can skip that field.

6 – In the "Heading" field put in some descriptive text like "Follow Our Reporters On Primary Night."

7 – We'll be using the "Subheading" to make the magic happen, place this code in there:

    <a class="twitter-timeline" data-dnt="true" data-widget-id="XXXXXXXXXXX" href="#">_</a><script type="text/javascript" src="http://PATH.TO/twitter-widget.js"></script>

This is an abbreviated version of the Twitter code (you only have 200 characters to work with, so be brief) with a link to the script that will initialize the embed.

8 – In that snippet of code replace the "XXXXXXXXXXX" with your Twitter Data Widget ID you got in step 2 for the list you've built already on Twitter.com's widget page.

9 – In that snipped of code, PATH.TO is the url for your copy of the Twitter jscript that handles the embed, this is the file you created and hosed in step 2.  

10 – Leave the "Button Text" and "url" fields under "Call to Action" blank and then hit save.

11 – You can then place the completed block on your homepage layout screen (http://YOUR-URL.org/admin/structure/layout/default). I recommend Region A since the completed widget will be tall, rather than wide.

Last updated 2.2.2016 By Jim Hill, KUNC tweet your q's to @ejimbo_com
