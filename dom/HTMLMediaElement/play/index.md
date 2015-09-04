---
title: play
tags:
  0: API
  1: Object
  2: Methods
  4: Audio
  5: DOM
  6: Video
readiness: 'Almost Ready'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'clean-up of MSDN import content to use WPD sections, compatibility'
summary: 'Loads and starts playback of a media resource.'
uri: dom/HTMLMediaElement/play

---
# play

## Summary

Loads and starts playback of a media resource.

*Method of [dom/HTMLMediaElement](/dom/HTMLMediaElement)*

## Syntax

``` {.js}
 object.play();
```

## Return Value

No return value

## Examples

Play method example.

``` {.html}
<!DOCTYPE html>
<html>
  <head>
    <title>Simple Video Example</title>
     <script>
         function hidecontrol(e) {
           // Set controls to true or false based on their current state
           var video = document.getElementById('video1');
           if (video.controls == true) {
             // Controls are binary, true if there, false if not
             video.removeAttribute("controls");
             e.innerHTML = "Show controls";
           } else {
             // Controls are binary, true if there, false if not
             video.setAttribute("controls", true);
             e.innerHTML = "Hide controls";
           }
         }

         function playVideo(e) {
           var video = document.getElementById('video1');      //video element
           //  Toggle between play and pause based on the paused property
           if (video.paused) {
             var input = document.getElementById('videoFile');   //text box
             if (input.value) {
               //  Only load a video file when the text field changes
               if (input.value != video.src) {
                 video.src = input.value;
               }
               video.play();
               e.innerHTML = "Pause";
             }
           } else {
             video.pause();
             e.innerHTML = "Play";
           }

         }
     </script>
</head>
<body>
<video id="video1" controls >HTML5 video is not supported</video>
<input type="text" id="videoFile" size="60" placeholder="Enter video file URL here"/>
  <button onclick="playVideo(this);">Play</button>
  <button onclick="hidecontrol(this);">Hide controls</button>
</body>
</html>
```

## Notes

### Remarks

To change the URL that is currently playing, assign it to [**src**](/dom/HTMLMediaElement/src). This method sets [**paused**](/dom/HTMLMediaElement/paused) to false. To change the URL using the **source** element, or if the original video was specified by the **source** element, call [**load**](/dom/HTMLMediaElement/load) before calling **play**.

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.9.8

## See also

### Related pages (MSDN)

-   `media`
-   `audio`
-   `audio`
-   `video`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

