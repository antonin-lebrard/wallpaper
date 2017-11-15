Modification of [https://github.com/sindresorhus/wallpaper](https://github.com/sindresorhus/wallpaper)
to make available scaling options for linux under GNOME environment supporting gsettings (tested on ubuntu 16.04)

Original README :

# wallpaper

> Get or set the desktop wallpaper

Works on macOS, Linux, and Windows.


## Install

```
$ npm install --save wallpaper
```


## Usage

```js
const wallpaper = require('wallpaper');

wallpaper.set('unicorn.jpg').then(() => {
	console.log('done');
});

wallpaper.get().then(imagePath => {
	console.log(imagePath);
	//=> '/Users/sindresorhus/unicorn.jpg'
});
```


## API

### .get()

Returns a promise for the path of the current desktop wallpaper.

### .set(imagePath, [options])

Returns a promise.

#### imagePath

Type: `string`

Path to the image to set as the desktop wallpaper.

#### options

Type: `Object`

##### scale

Type: `string`<br>
Values: `fill` `fit` `stretch` `center`<br>
Default: Current system setting

Scaling method. Only available on macOS. <b>Now available for Linux under GNOME</b>


## Related

- [wallpaper-cli](https://github.com/sindresorhus/wallpaper-cli) - CLI for this module
- [macos-wallpaper](https://github.com/sindresorhus/macos-wallpaper) - macOS binary used in this module
- [win-wallpaper](https://github.com/sindresorhus/win-wallpaper) - Windows binary used in this module


## License

MIT © [Sindre Sorhus](https://sindresorhus.com)
