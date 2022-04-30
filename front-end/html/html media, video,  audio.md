//** HTML Media **//

Multimedia on the web is sound, music, movies, and animations.

-- What is Multimedia? --

Multimedia comes in many different formates. It can be almost anything you can hear or see, like images, music, sound, videos, records, films, animations, and more.

Web pages often contain multimedia elements of different types and formats.

-- Browser Support --

The first web browsers had support for text only, limited to a single font in a single color.

Later came browsers with suppport for colors, fonts, images, and multimedia!

-- Multimedia Formats --

Multimedia elements (like audio or video) are stored in media files.

The most common way to discover the type of a file, is to look at the file extension.

Multimedia files have formats and different extensions like: .wav, .mp3, .mp4, .mpg, .wmv, and .avi.

-- Video Formats --

There are many video formats out there.

The MP4, WebM, and Ogg formats are supported by HTML.

The MP4 format is recommended by YouTube.

-- Audio Formats --

MP3 is the best format for compressed recorded music. The term MP3 has become synonymous with digital music.

//** HTML Video **//

The HTML `<video>` element is used to show a video on a web page.

```
<video width="320" height="240" controls>  
 <source src="movie.mp4" type="video/mp4">  
 <source src="movie.ogg" type="video/ogg">  
Your browser does not support the video tag.  
</video>
```

-- How it Works --

The `<controls>` attributes add video controls, like play, pause, and volume.

It is a good idea to always include `width` and `height` attributes. If height and width are not set, the page might flicker while the video loads.

The `<source>` element allows you to specify alternative video files which the browser may choose from. The browser will use the first recognized format.

The text between the `<video>` and `</video>` tags will only be displayed in browsers that do not support the `<video>` element.

-- HTML `<video>` Autoplay --

To start a video automatically use the `autoplay` attribute:

```
<video width="320" height="240" autoplay>  
 <source src="movie.mp4" type="video/mp4">  
 <source src="movie.ogg" type="video/ogg">  
Your browser does not support the video tag.  
</video>
```

//** HTML Audio **//

The HTML `<audio>` element is used to play an audio file on a web page.

-- The HTML `<audio>` Element --

To play an audio file in HTML, use the `<audio>` element:

```
<audio controls>  
 <source src="horse.ogg" type="audio/ogg">  
 <source src="horse.mp3" type="audio/mpeg">  
Your browser does not support the audio element.  
</audio>
```

-- HTML Audio - How it Works --

The `controls` attribute adds audio controls, like play, pause, and volume.

The `<source>` element allows you to specify alternative audio files which the browser may choose from. The browser will use the first recognized format.

The text between the `<audio>` and `</audio>` tags will only be displayed in browsers that do not support the `<audio>` element.

-- HTML Audio - Methods, Properties, and Events --

The HTML DOM defines methods, properties, and events for the `<audio>` element.

This allows you to load, play, and pause audios, as well as set duration and volume.

There are also DOM events that can notify you when an audio begins to play, is paused, etc.

