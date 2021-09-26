# Manga
📖 Easily find the place to read a manga

## Frontend Development
### Requirements
* Git
* Node.js
* A backend server (see note below)
* CDN with manga site logos (see note below)

### Installation
1. ``git clone https://github.com/davidcralph/mangapages``
2. ``cd mangapages`` and then ``npm i`` (or ``yarn``)
3. ``npm start``

### Note
The currently hosted backend is currently not opensource and most likely won't be for some time (it's a bit of a mess!). If you wish to make your own backend, all you really need is a ``/random`` and ``/search`` route that returns an array like this:
```js
[
  {
    "title": "Hunter x Hunter",
    "site": "viz",
    "url": "https://www.viz.com/hunter-x-hunter" // depending on the site, this may be different and you will need custom code!
  }
]
```

The currently hosted API limits results to 300 to prevent lag. For images, simply have a web server or CDN (e.g imagekit which is what I am using) and upload the site logos there.
