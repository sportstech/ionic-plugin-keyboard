Keyboard
======

The `window.Keyboard` object provides functions to make interacting with the keyboard easier, and fires events to indicate that the keyboard will hide/show.

    cordova plugin add ionic-plugin-keyboard

Methods
-------

- window.Keyboard.hideKeyboardAccessoryBar
- window.Keyboard.close
- window.Keyboard.disableScroll
- window.Keyboard.show

Properties
--------

- window.Keyboard.isVisible

Events
--------

These events are fired on the window.

- native.keyboardshow
  * A number `keyboardHeight` is given on the event object, which is the pixel height of the keyboard.
- native.keyboardhide

Keyboard.hideKeyboardAccessoryBar
=================

Hide the keyboard accessory bar with the next, previous and done buttons.

    window.Keyboard.hideKeyboardAccessoryBar(true);
    window.Keyboard.hideKeyboardAccessoryBar(false);

Supported Platforms
-------------------

- iOS


Keyboard.close
=================

Close the keyboard if it is open.

    window.Keyboard.close();

Supported Platforms
-------------------

- iOS, Android, Blackberry 10, Windows 


Keyboard.disableScroll
=================

Disable native scrolling, useful if you are using JavaScript to scroll

    window.Keyboard.disableScroll(true);
    window.Keyboard.disableScroll(false);

Supported Platforms
-------------------

- iOS, Windows

Keyboard.show
=================

Force keyboard to be shown. This typically helps if autofocus on a text element does not pop up the keyboard automatically

    window.Keyboard.show();

Supported Platforms

- Android, Blackberry 10, Windows 

native.keyboardshow
=================

This event fires when the keyboard will be shown

    window.addEventListener('native.keyboardshow', keyboardShowHandler);

    function keyboardShowHandler(e){
        alert('Keyboard height is: ' + e.keyboardHeight);
    }

Properties
-----------

keyboardHeight: the height of the keyboard in pixels


Supported Platforms
-------------------

- iOS, Android, Blackberry 10, Windows


native.keyboardhide
=================

This event fires when the keyboard will hide

    window.addEventListener('native.keyboardhide', keyboardHideHandler);

    function keyboardHideHandler(e){
        alert('Goodnight, sweet prince');
    }

Properties
-----------

None

Supported Platforms
-------------------

- iOS, Android, Blackberry 10, Windows
