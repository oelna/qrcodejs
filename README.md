# QRCode.js
QRCode.js is javascript library for making QRCode by [davidshimjs](https://github.com/davidshimjs/qrcodejs). QRCode.js supports Cross-browser with HTML5 Canvas and table tag in DOM.
QRCode.js has no dependencies.

## Note

This is an amateurish attempt (by Arno Richter) to make the original script use the ESM format and more modern class syntax. It may work for you, it may not. Take it as is.

## Basic Usages
```html
<div id="qrcode"></div>
<script type="module">
	import { QRCode } from './qrcode.esm.js';

	new QRCode(document.querySelector('#qrcode'), 'https://richter.studio');
</script>
```

or with some options

```html
<div id="qrcode"></div>
<script type="module">
	import { QRCode } from './qrcode.esm.js';

	var qrcode = new QRCode(document.querySelector('#qrcode'), {
		text: 'https://richter.studio',
		width: 128,
		height: 128,
		colorDark : "#000",
		colorLight : "transparent",
		correctLevel : QRCode.CorrectLevel.H
	});
</script>
```

and you can use some methods

```js
qrcode.clear(); // clear the code.
qrcode.makeCode("http://naver.com"); // make another code.
```

## Browser Compatibility
Should be all modern browsers that support ESM

## License
MIT License

## Contact
Original author: twitter @davidshimjs
ESM modifications by: mastodon @oelna@mas.to
