phonegap-toast-notification-ios
===============================

Adds support for toast notification in phonegap. Uses iToast - the native plugin for toast notification in iOS. You can download it here: https://github.com/ecstasy2/toast-notifications-ios

## Installation:

1. Download iToast from https://github.com/ecstasy2/toast-notifications-ios . Drag the `iToast.h` and `iToast.m` files to you Plugins folder in Xcode.
2. Download this plugin and drag its contents to Plugins folder in Xcode.
3. Add the .js file `PhonegapITost.js` to your `www` folder on disk, and add reference(s) to the .js file using `<script>` tag in your html file

`<script type="text/javascript" src="js/plugins/PhonegapIToast.js"></script>`

4. Add new entry with key `PhonegapIToast` and value `PhonegapIToast` to `Plugins` in `Cordova.plist/Cordova.plist`

## Usage:

Default notification:

```javascript
	window.plugins.iToast.show('This is a toast notification');
```

You can also specify options:

*duration* - long/short/normal string or time in milliseconds for how long the notification will be shown (default is normal)
*gravity* - top/bottom/center string that sets the place to show your notification (default is center)
*top* - integer that sets offset from top in pixels. Can also be a negative value
*left* - integer that sets offset from left side in pixels. Can also be a negative value

```javascript
	// this will set toast notification for 5 seconds 50px from the top of screen
	window.plugins.iToast.show('This is a toast notification', {
		duration : 5000,
		gravity  : 'top',
		top      : 50
	});
```

## License

(The MIT License)

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.