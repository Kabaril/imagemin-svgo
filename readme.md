[SVGO](https://github.com/svg/svgo) imagemin plugin


## Warning

This repo is only for development purposes and not intended to be used in production enviroments.


## Usage

```js
const imagemin = require('imagemin');
const imageminSvgo = require('imagemin-svgo');

(async () => {
	await imagemin(['images/*.svg'], {
		destination: 'build/images',
		plugins: [
			imageminSvgo({
				plugins: [{
					name: 'removeViewBox',
					active: false
				}]
			})
		]
	});

	console.log('Images optimized');
})();
```


## API

### imageminSvgo([options])(buffer)

Returns a `Promise<Buffer>`.

#### options

Type: `Object`

Pass options to [SVGO](https://github.com/svg/svgo#configuration).

#### buffer

Type: `Buffer`

Buffer to optimize.


## License

MIT © [imagemin](https://github.com/imagemin)
