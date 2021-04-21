# HTML forms have been quite tricky — firstly, because at least a little bit of JavaScript was required, and secondly, because no amount of CSS could ever make them behave.

However, this isn’t necessarily true in the case of the modern web, so let’s learn how to mark up forms using only HTML and CSS.

Form-ing the basic structure
A form input with a prefilled value

Start off with the <form> element.

Nothing fancy here. Just covering the basic structure.

<form>
    ...
</form>
If you’re submitting the form data naturally (that is, without JavaScript), you’ll need to include the action attribute, where the value is the URL you’ll be sending the form data to. The method should be GET or POST depending on what you’re trying to achieve (don’t send sensitive data with GET).

Additionally, there’s also the lesser-used enctype attribute which defines the encoding type of the data being sent. Also, the target attribute, although not necessarily an attribute unique to forms, can be used to show the output in a new tab.

JavaScript-based forms don’t necessarily need these attributes.

<form method="POST" action="/subscribe" enctype="application/x-www-form-urlencoded" target="_blank">
    ...
</form>
Forms are made up of inputs, which expect data values.

<form>
    <input type="text"><!-- text input -->
    <input type="text" value="Prefilled value">
</form>

Including Labels for Better Usability & Accessibility
Every input needs a label.

A label is a text descriptor that describes what an input is for. There are three ways to declare a label, but one of them is superior to the other two. Let’s dive into these now.

Adjacent labels
Adjacent labels require the most code because we need to explicitly declare which input the label describes. To most, this is counterintuitive because we can instead wrap inputs inside labels to achieve the same effect with less code.


That being said, the adjacent method may be necessary in extenuating circumstances, so here’s what that would look like:

<label for="firstName">First name</label>
<input id="firstName">
As you can see from the example above, the for attribute of the <label> must match the id attribute of the input, and what this does is explain to input devices which text descriptor belongs to which input. The input device will then relay this to users (screen readers, for example, will dictate it via speech).

ARIA labels
While semantic HTML is better, ARIA (Accessible Rich Internet Applications) labels can compensate in their absence. In this case, here’s what a label might look like in the absence of an actual HTML <label>:

<input aria-label="First name">
Unfortunately, the downside of this approach is the lack of a visual label. However, this might be fine with some markups (for example, a single-input form with a heading and placeholder):


Learn PHP for free!
Make the leap into server-side programming with a comprehensive cover of PHP & MySQL.

Normally RRP $39.99 Yours absolutely free

Name
Email
Get the book free
<h1>Subscribe</h1>
<form>
    <input aria-label="Email address" placeholder="bruce@wayneenterpris.es">
</form>
(I’ll explain what placeholders are for in a moment.)

Wrapping labels
Wrapping inputs within labels is the cleanest approach. Also, thanks to CSS’s :focus-within, we can even style labels while their child inputs receive focus, but we’ll discuss that later.

<label>
    First name<input>
</label>
---------------------------------------------------------------------------------------------------------------------------------
Basic table: Set up a table with three headings to your page, by adding the following code to your document under the “ordered list” code. This is a real-life example that lists a weekly class schedule. The <th> tags will form the columns in this table, and the <td> tags will form the rows.

 

<table style="width:100%">
 <tr>
   <th>Monday</th>
   <th>Tuesday</th>
   <th>Wednesday</th>
 </tr>
 <tr>
   <td>9AM Lecture</td>
   <td>12PM Lecture</td>
   <td>Study Break</td>
 </tr>
  <tr>
   <td>10AM Lecture</td>
   <td>Study Break</td>
   <td>2PM Lecture</td>
  </tr>
</table>
-------------------------------------------------------------------------------------------------------------------------------
Events are fired to notify code of "interesting changes" that may affect code execution. These can arise from user interactions such as using a mouse or resizing a window, changes in the state of the underlying environment (e.g. low battery or media events from the operating system), and other causes.

Each event is represented by an object that is based on the Event interface, and may have additional custom fields and/or functions to provide information about what happened. The documentation for every event has a table (near the top) that includes a link to the associated event interface, and other relevant information. A full list of the different event types is given in Event > Interfaces based on Event.

This topic provides an index to the main sorts of events you might be interested in (animation, clipboard, workers etc.) along with the main classes that implement those sorts of events. At the end is a flat list of all documented events.

Note
This page lists many of the most common events you'll come across on the web. If you are searching for an event that isn't listed here, try searching for its name, topic area, or associated specification on the rest of MDN.

Event index
Event type	Description	Documentation
Animation	
Events related to the Web Animation API.

Used to respond to changes in animation status (e.g. when an animation starts or ends).

Animation events fired on Document, Window, HTMLElement.
Asynchronous data fetching	
Events related to the fetching data.

Events fired on AbortSignal, XMLHttpRequest, FileReader.
Clipboard	
Events related to the Clipboard API.

Used to notify when content is cut, copied, or pasted.

Events fired on Document, Element, Window.
Composition	
Events related to composition; entering text "indirectly" (rather than using normal keyboard presses).

For example, text entered via a speech to text engine, or using special key combinations that modify keyboard presses to represent new characters in another language.

Events fired on Element.
CSS transition	
Events related to CSS Transitions.

Provides notification events when CSS transitions start, stop, are cancelled, etc.

Events fired on Document, HTMLElement, Window.
Database	
Events related to database operations: opening, closing, transactions, errors, etc.

Events fired on IDBDatabase, IDBOpenDBRequest, IDBRequest, IDBTransaction.
DOM mutation	
Events related to modifications to the Document Object Model (DOM) hierarchy and nodes.

Note
Mutation Events are deprecated. Mutation Observers should be used instead.

Drag'n'drop, Wheel	
Events related to using the HTML Drag and Drop API and wheel events.

Drag and Wheel events are derived from mouse events. While they are fired when using mouse wheel or drag/drop, they may also be used with other appropriate hardware.

Drag events fired on Document

Wheel events fired on Document and Element

Focus	
Events related to elements gaining and losing focus.

Events fired on Element, Window.
Form	
Events related to forms being constructed, reset and submitted.

Events fired on HTMLFormElement.
Fullscreen	
Events related to the Fullscreen API.

Used to notify when the transitioning between full screen and windowed modes, and also of errors occuring during this transition.

Events fired on Document, Element.
Gamepad	
Events related to the Gamepad API.

Events fired on Window.
Gestures	
Touch events are recommended for implementing gestures.

Events fired on Document, Element.

In addition there are a number of non-standard gesture events:

Non-standard WebKit specific events on Element: gesturestart event, gesturechange event, gestureend event.
Non-standard IE specific events on Element: MSGestureStart, MSGestureChange, MSGestureEnd, MSGestureHold, MSGestureTap.
Deprecated/non-standard Mozilla touch events Touch events (Mozilla experimental)
Mouse gesture events for Firefox Addons
History	
Events related to the History API.

Events fired on Window.
HTML element content display management	
Events related to changing the state of a display or textual element.

Events fired on HTMLDetailsElement, HTMLDialogElement, HTMLSlotElement.
Inputs	
Events related to HTML input elements e.g. <input>, <select>, or <textarea>.

Events fired on HTMLElement, HTMLInputElement.
Keyboard	
Events related to using a keyboard.

Used to notify when keys are moved up, down, or just pressed.

Events fired on Document, Element.
Loading/unloading documents	
Events related to loading and unloading documents.

Events fired on Document and Window.

Manifests	
Events related to installation of progressive web app manifests.

Events fired on Window.
Media	
Events related to media usage (including the Media Capture and Streams API, Web Audio API, Picture-in-Picture API, etc.).

Events fired on ScriptProcessorNode, HTMLMediaElement, AudioTrackList, AudioScheduledSourceNode, MediaRecorder, MediaStream, MediaStreamTrack, VideoTrackList, HTMLTrackElement, OfflineAudioContext, TextTrack, TextTrackList, Element/audio, Element/video.
Messaging	
Events related to a window receiving a message from another browsing context.

Events fired on Window.
Mouse	
Events related to using a computer mouse.

Used to notify when the mouse is clicked, doubleclicked, up and down events, right-click, movement in and out of an element, text selection, etc.

Pointer events provide a hardware-agnostic alternative to mouse events. Drag and Wheel events are derived from mouse events.

Mouse events fired on Element
Network/Connection	
Events related to gaining and losing network connection.

Events fired on Window.

Events fired on NetworkInformation (Network Information API).

Payments	
Events related to the Payment Request API.

Events fired on PaymentRequest, PaymentResponse.

Performance	
Events related to High Resolution Time API, Performance Timeline API, Navigation Timing API, User Timing API, and Resource Timing API.

Events fired on Performance.

Pointer	
Events related to the Pointer Events API.

Provides hardware-agnostic notification from pointing devices including Mouse, Touch, pen/stylus.

Events fired on Document, HTMLElement.
Print	
Events related to printing.

Events fired on Window.
Promise rejection	
Events sent to the global script context when any JavaScript promise is rejected.

Events fired on Window.
Sockets	
Events related to the WebSockets API.

Events fired on Websocket.
SVG	
Events related to SVG images.

Events fired on SVGElement, SVGAnimationElement, SVGGraphicsElement.

Text selection	
Events related to selecting text.

Events fired on Document.

Touch	
Events related to the Touch Events API.

Provides notification events from interacting with a touch sensitive screen (i.e. using a finger or stylus). Not related to the Force Touch API.

Events fired on Document, Element.
Virtual reality	
Events related to the WebXR Device API.

The WebVR API (and associated Window events) are deprecated.

Events fired on XRSystem, XRSession, XRReferenceSpace.
RTC (real time communication)	
Events related to the WebRTC API.

Events fired on RTCDataChannel, RTCDTMFSender, RTCIceTransport, RTCPeerConnection.
Server-sent events	
Events related to the server sent events API.

Events fired on EventSource.
Speech	
Events related to the Web Speech API.

Events fired on SpeechSynthesisUtterance.
Workers	
Events related to the Web Workers API, Service Worker API, Broadcast Channel API, and Channel Messaging API.

Used to respond to new messages and message sending errors. Service workers can also be notified of other events, including push notifications, users clicking on displayed notifications, that push subscription has been invalidated, deletion of items from the content index, etc.

Events fired on ServiceWorkerGlobalScope, DedicatedWorkerGlobalScope, SharedWorkerGlobalScope, WorkerGlobalScope, Worker, WorkerGlobalScope, BroadcastChannel, MessagePort.
Event listing
This section lists events that have their own reference pages on MDN. If you are interested in an event that isn't listed here, try searching for its name, topic area, or associated specification on the rest of MDN.

AbortSignal
abort event
AudioScheduledSourceNode
ended event
AudioTrackList
addtrack event
change event
removetrack event
BroadcastChannel
messageerror event
message event
DedicatedWorkerGlobalScope
messageerror event
message event
Document
animationcancel event
animationend event
animationiteration event
animationstart event
copy event
cut event
DOMContentLoaded event
dragend event
dragenter event
dragleave event
dragover event
dragstart event
drag event
drop event
fullscreenchange event
fullscreenerror event
gotpointercapture event
keydown event
keypress event
keyup event
lostpointercapture event
paste event
pointercancel event
pointerdown event
pointerenter event
pointerleave event
pointerlockchange event
pointerlockerror event
pointermove event
pointerout event
pointerover event
pointerup event
readystatechange event
scroll event
selectionchange event
selectstart event
touchcancel event
touchend event
touchmove event
touchstart event
transitioncancel event
transitionend event
transitionrun event
transitionstart event
visibilitychange event
wheel event
Element
afterscriptexecute event
auxclick event
beforescriptexecute event
blur event
click event
compositionend event
compositionstart event
compositionupdate event
contextmenu event
copy event
cut event
dblclick event
DOMActivate event
DOMMouseScroll event
error event
focusin event
focusout event
focus event
fullscreenchange event
fullscreenerror event
gesturechange event
gestureend event
gesturestart event
keydown event
keypress event
keyup event
mousedown event
mouseenter event
mouseleave event
mousemove event
mouseout event
mouseover event
mouseup event
mousewheel event
msContentZoom event
MSGestureChange event
MSGestureEnd event
MSGestureHold event
MSGestureStart event
MSGestureTap event
MSInertiaStart event
MSManipulationStateChanged event
overflow event
paste event
scroll event
select event
show event
touchcancel event
touchend event
touchmove event
touchstart event
underflow event
webkitmouseforcechanged event
webkitmouseforcedown event
webkitmouseforceup event
webkitmouseforcewillbegin event
wheel event
EventSource
error event
message event
open event
FileReader
abort event
error event
loadend event
loadstart event
load event
progress event
HTMLCanvasElement
webglcontextcreationerror event
webglcontextlost event
webglcontextrestored event
HTMLDetailsElement
toggle event
HTMLDialogElement
cancel event
close event
HTMLElement
animationcancel event
animationend event
animationiteration event
animationstart event
beforeinput event
change event
gotpointercapture event
input event
lostpointercapture event
pointercancel event
pointerdown event
pointerenter event
pointerleave event
pointermove event
pointerout event
pointerover event
pointerup event
transitioncancel event
transitionend event
transitionrun event
transitionstart event
HTMLFormElement
formdata event
reset event
submit event
HTMLInputElement
invalid event
search event
HTMLMediaElement
abort event
canplaythrough event
canplay event
durationchange event
emptied event
ended event
error event
loadeddata event
loadedmetadata event
loadstart event
pause event
playing event
play event
progress event
ratechange event
seeked event
seeking event
stalled event
suspend event
timeupdate event
volumechange event
waiting event
HTMLSlotElement
slotchange event
HTMLTrackElement
cuechange event
HTMLVideoElement
enterpictureinpicture event
leavepictureinpicture event
IDBDatabase
abort event
close event
error event
versionchange event
IDBOpenDBRequest
blocked event
upgradeneeded event
IDBRequest
error event
success event
IDBTransaction
abort event
complete event
error event
MediaDevices
devicechange event
MediaRecorder
error event
MediaStream
addtrack event
removetrack event
MediaStreamTrack
ended event
mute event
unmute event
MessagePort
messageerror event
message event
OfflineAudioContext
complete event
PaymentRequest
merchantvalidation event
paymentmethodchange event
shippingaddresschange event
shippingoptionchange event
PaymentResponse
payerdetailchange event
Performance
resourcetimingbufferfull event
PictureInPictureWindow
resize event
RTCDataChannel
bufferedamountlow event
close event
closing event
error event
message event
open event
RTCDtlsTransport
error event
RTCDTMFSender
tonechange event
RTCIceTransport
gatheringstatechange event
selectedcandidatepairchange event
statechange event
RTCPeerConnection
addstream event
connectionstatechange event
datachannel event
icecandidateerror event
icecandidate event
iceconnectionstatechange event
icegatheringstatechange event
identityresult event
idpassertionerror event
idpvalidationerror event
negotiationneeded event
peeridentity event
removestream event
signalingstatechange event
track event
ScriptProcessorNode
audioprocess event
ServiceWorkerContainer
message event
ServiceWorkerGlobalScope
activate event
contentdelete event
install event
message event
notificationclick event
pushsubscriptionchange event
push event
SharedWorkerGlobalScope
connect event
SpeechRecognition
audioend event
audiostart event
end event
error event
nomatch event
result event
soundend event
soundstart event
speechend event
speechstart event
start event
SpeechSynthesis
voiceschanged event
SpeechSynthesisUtterance
boundary event
end event
error event
mark event
pause event
resume event
start event
SVGAnimationElement
beginEvent event
endEvent event
repeatEvent event
SVGElement
abort event
error event
load event
resize event
scroll event
unload event
SVGGraphicsElement
copy event
cut event
paste event
TextTrack
cuechange event
TextTrackList
addtrack event
change event
removeTrack event
VideoTrackList
addtrack event
change event
removetrack event
VisualViewport
resize event
scroll event
WebSocket
close event
error event
message event
open event
Window
afterprint event
animationcancel event
animationend event
animationiteration event
animationstart event
appinstalled event
beforeprint event
beforeunload event
blur event
copy event
cut event
devicemotion event
deviceorientation event
DOMContentLoaded event
error event
focus event
gamepadconnected event
gamepaddisconnected event
hashchange event
languagechange event
load event
messageerror event
message event
offline event
online event
orientationchange event
pagehide event
pageshow event
paste event
popstate event
rejectionhandled event
resize event
storage event
transitioncancel event
transitionend event
transitionrun event
transitionstart event
unhandledrejection event
unload event
vrdisplayactivate event
vrdisplayblur event
vrdisplayconnect event
vrdisplaydeactivate event
vrdisplaydisconnect event
vrdisplayfocus event
vrdisplaypointerrestricted event
vrdisplaypointerunrestricted event
vrdisplaypresentchange event
Worker
messageerror event
message event
WorkerGlobalScope
languagechange event
XMLHttpRequest
abort event
error event
loadend event
loadstart event
load event
progress event
timeout event
XRReferenceSpace
reset event
XRSession
end event
inputsourceschange event
selectend event
selectstart event
select event
squeezeend event
squeezestart event
squeeze event
visibilitychange event
XRSystem
devicechange event
