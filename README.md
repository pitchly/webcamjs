# Webcam.js
Webcam interface, written entirely in ECMAScript 6 using HTML5's `getUserMedia` and `MediaDevices` APIs. 
No external dependencies.
Each call returns a `Promise`.
Works in Chrome and Firefox.

Example:
``` html
<video id="videoElement" muted="true" >
<script src="https://raw.githubusercontent.com/pitchly/webcamjs/master/webcam.js"></script>
<script>
  window.webcam.init().then(function() {
    var videoElement = document.getElementById("videoElement");
    videoElement.src = window.webcam.videoStream;
    videoElement.play();
  }).catch(function(error){
    console.log(error);
  });
</script>
```
