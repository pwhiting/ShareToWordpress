# ShareToWordpress
android app that shares google photos to android wordpress app.

When composing in the wordpress app on android it is advantageous to be able to add links 
to photos and albums in your google photo library. This app helps with that process. 
It requires two shortcodes in wordpress - one for albums and one to simplify the insertion
of images by URL reference. 

To use this app go to google photos and hit share on either a photo or an album. If you are 
sharing an album you will need to select ShareAlbumToWordpress for the application target.
If you are sharing a single photo select SharePhotoToWordpress. In both cases a shortcode
will be copied to your clipboard which references that photo or album and the wordpress 
app will be brought to the foreground. Go to the location you want to include the picture
or ablum and paste the shortcode.

The advantage for doing photos and albums this way is that google hosts the images, so 
they won't use storage on your server and if you pay for bandwidth out on your server 
(if you are using aws lightsail for example.) Additionally, it will avoid the work of 
having to upload the image twice. The first time happens when your phone uploads the image 
to yourgoogle account and the second time happens if you follow the normal path in the 
wordpress app - in which case your phone uploads a copy to your wordpress site.

I put this together to help out with blogging when we are on multi-day bike rides with 
limited bandwidth. We may write a blog entry with no bandwidth using the wordpress app
offline, and then when we get bandwidth finalize the post and attach pictures. This just
makes that process a bit more easy. If you have a laptop or plenty of bandwidth, you 
might be better served by just accessing wordpress from chrome.

Information on the necessary shortcodes:

See Gupta's answer: https://stackoverflow.com/questions/42479022/wordpress-simple-image-shortcode 
This app assumes a shortcode with similar syntax has been loaded for image references: 
[img link="http://yoururl"].
It grabs the link to your photo using logic similar to that described here:
https://medium.com/@ValentinHervieu/how-i-used-google-photos-to-host-my-website-pictures-gallery-d49f037c8e3.
The other shortcode comes from Pavex's embed google photos album plugin. Information on it 
can be found here:
https://www.publicalbum.org/blog/wordpress-google-photos-album-plugin.
