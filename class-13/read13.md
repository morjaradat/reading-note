# Local Storage

- Historically, web applications have had none of these luxuries. Cookies were invented early in the web’s history, and indeed they can be used for persistent local storage of small amounts of data. But they have three potentially dealbreaking downsides:

Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over
Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL)
Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful

## INTRODUCING HTML5 STORAGE

- Web Storage, which was at one time part of the HTML5 specification proper, but was split out into its own specification for uninteresting political reasons.
- Certain browser vendors also refer to it as “Local Storage” or “DOM Storage.

**check for HTML5 Storage**
`function supports_html5_storage() {`<br>
 `try {`<br>
  `return 'localStorage' in window && window['localStorage'] !== null;`<br>
 `} catch (e) {`<br>
   `return false;`<br>
 `}`<br>
`}`<br>

## USING HTML5 STORAGE

- HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored as a string. If you are storing and retrieving anything other than strings, you will need to use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype.

- methods for removing the value for a given named key, and clearing the entire storage area (that is, deleting all the keys and values at once).<br>

`interface Storage {`<br>
 `deleter void removeItem(in DOMString key);`<br>
 `void clear();`<br>
`};`<br>

## TRACKING CHANGES TO THE HTML5 STORAGE AREA

- you can keep track programmatically of when the storage area changes by trap the storage event.
- The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something.

- The storage event is supported everywhere the localStorage object is supported, which includes Internet Explorer 8. IE 8 does not support the W3C standard addEventListener (although that will finally be added in IE 9).

- STORAGEEVENT OBJECT
**PROPERTY :** 

1. key :TYPE string/ the named key that was added, removed, or modified
2. oldValue: TYPE any/ the previous value (now overwritten), or null if a new item was added
3. newValue :TYPE any/ the new value, or null if an item was removed
4. url*: TYPE string/ the page which called a method that triggered this change

## LIMITATIONS IN CURRENT BROWSERS

- the history of local storage hacks using third-party plugins, I made a point of mentioning the limitations of each technique, such as storage limits. I just realized that I haven’t mentioned anything about the limitations of the now-standardized HTML5 Storage. I’ll give you the answers first, then explain them. The answers, in order of importance, are “5 megabytes,” “QUOTA_EXCEEDED_ERR,” and “no.”

## HTML5 STORAGE IN ACTION

- the Halma game we constructed in the canvas chapter. There’s a small problem with the game: if you close the browser window mid-game, you’ll lose your progress. But with HTML5 Storage, we can save the progress locally, within the browser itself. Here is a live demonstration. Make a few moves, then close the browser tab, then re-open it. If your browser supports HTML5 Storage, the demonstration page should magically remember your exact position within the game, including the number of moves you’ve made, the position of each of the pieces on the board, and even whether a particular piece is selected.

## BEYOND NAMED KEY-VALUE PAIRS: COMPETING VISIONS

- While the past is littered with hacks and workarounds, the present condition of HTML5 Storage is surprisingly rosy. A new API has been standardized and implemented across all major browsers, platforms, and devices. As a web developer, that’s just not something you see every day, is it? But there is more to life than “5 megabytes of named key/value pairs,” and the future of persistent local storage is… how shall I put it… well, there are competing visions.
