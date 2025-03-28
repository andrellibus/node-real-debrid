# node-real-debrid (Working Fork)

This is a fork of the [`node-real-debrid`](https://github.com/atombarel/node-real-debrid) library, which stopped working correctly after switching to `axios`.

The original working fork was created by [DavidRayner](https://github.com/DavidRayner):  
🔗 **[DavidRayner/node-real-debrid](https://github.com/DavidRayner/node-real-debrid)**

This package was published on npm solely to provide a working, installable version.

## Usage example
	npm install @andrellibus/node-real-debrid
```javascript
const RealDebridClient = require('real-debrid-api')
const RD = new RealDebridClient('Your API Token')

;(async () => {
	try {
		console.log(await RD.time.ISO())
		console.log(await RD.time.get())
		console.log(await RD.user.get())
		console.log(await RD.unrestrict.check('https://openload.co/f/faqKmuLs7ro/Scappa_-_Get_Out_%5BHD%5D_%282017%29_MD_Bluray_1080p.mp4'))
		console.log(await RD.traffic.get())
		console.log(await RD.unrestrict.link('https://openload.co/f/faqKmuLs7ro/Scappa_-_Get_Out_%5BHD%5D_%282017%29_MD_Bluray_1080p.mp4'))
		console.log(await RD.torrents.addTorrent(__dirname + '\\file.torrent'))
        	console.log(await RD.torrents.addMagnet('magnet_link'))
        	console.log(await RD.streaming.mediaInfos('id'))
	} catch (e) {
		console.log(e)
	}
})()
```
