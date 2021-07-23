# Audio, Video, Images
Multimedia on the web is sound, music, videos, movies, and animations.

What is Multimedia?
Multimedia comes in many different formats. It can be almost anything you can hear or see, like images, music, sound, videos, records, films, animations, and more.

Web pages often contain multimedia elements of different types and formats.

Browser Support
The first web browsers had support for text only, limited to a single font in a single color.

Later came browsers with support for colors, fonts, images, and multimedia!

Multimedia Formats
Multimedia elements (like audio or video) are stored in media files.

The most common way to discover the type of a file, is to look at the file extension.

Multimedia files have formats and different extensions like: .wav, .mp3, .mp4, .mpg, .wmv, and .avi.
## HTML Video
The HTML ```<video> ``` element is used to show a video on a web page.
example
```html
<p>
Video courtesy of 
<a href="https://www.bigbuckbunny.org/" target="_blank">Big Buck Bunny</a>.
</p>
```
```html
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>
```
## HTML Audio
The HTML <audio> element is used to play an audio file on a web page.

The HTML <audio> Element
To play an audio file in HTML, use the <audio> element:
example:
```html
<audio controls>
<source src="horse.ogg" type="audio/ogg">
<source src="horse.mp3" type="audio/mpeg">
Your browser does not support the audio element.
</audio>
```
  ##HTML Images
  Images can improve the design and the appearance of a web page.
HTML Images Syntax
The HTML <img> tag is used to embed an image in a web page.

Images are not technically inserted into a web page; images are linked to web pages. The <img> tag creates a holding space for the referenced image.

The <img> tag is empty, it contains attributes only, and does not have a closing tag.

The <img> tag has two required attributes:

src - Specifies the path to the image
alt - Specifies an alternate text for the image
  example
  ```html
  <img src="pic_trulli.jpg" alt="Italian Trulli">
<img src="img_girl.jpg" alt="Girl in a jacket">
<img src="img_chania.jpg" alt="Flowers in Chania">
  ```
  The src Attribute
The required src attribute specifies the path (URL) to the image.

Note: When a web page loads; it is the browser, at that moment, that gets the image from a web server and inserts it into the page. Therefore, make sure that the image actually stays in the same spot in relation to the web page, otherwise your visitors will get a broken link icon. The broken link icon and the alt text are shown if the browser cannot find the image.
