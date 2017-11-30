# p5.js-speech
Web Audio Speech Synthesis and Speech Recognition Implementation for p5.js (http://p5js.org)

R. Luke DuBois (dubois@nyu.edu)   
[ABILITY Lab](http://abilitylab.nyu.edu) / [Brooklyn Experimental Media Center](http://bxmc.poly.edu)   
NYU

This is a simple p5 extension to provide Web Speech (Synthesis and Recognition) API functionality.  It consists of two object classes (p5.Speech and p5.SpeechRec) along with accessor functions to speak and listen for text, change parameters (synthesis voices, recognition models, etc.), and retrieve callbacks from the system.

Speech recognition requires launching from a server (e.g. a python simpleserver on a local machine).

## Simple Example (Synthesis)

Demo simple http://ability.nyu.edu/p5.js-speech/examples/02speechbox.html

```javascript
var voice = new p5.Speech(); // speech synthesis object
voice.speak('hi there'); // say something
```

## Simple Example (Recognition)

```javascript
var speechRec = new p5.SpeechRec(gotSpeech); // speech recognition object (will prompt for mic access)
speechRec.start(); // start listening

function gotSpeech(speech) {
  console.log(speech.text); // log the result
}
```
