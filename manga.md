# Manga
📖 Easily find the place to read a manga

## API
### Endpoints
/ - returns hello world message (30 requests a minute ratelimit)
/random - returns 4 random manga/light novels (use query ``?type=lightnovel`` to change) (100 requests a minute ratelimit)
/search - search for manga/light novels (use query ``type=lightnovel`` to change and query ``input=insert search here`` to search) (500 requests a minute ratelimit)
/mal - redirect to the MyAnimeList page for a manga/light novel using search (query ``?slug=insert search here``) (50 requests a minute ratelimit)

## Development
### Frontend
#### Requirements
* Git
* Node.js
* CDN with manga site logos (see note below)

#### Installation
1. ``git clone https://github.com/davidcralph/mangapages``
2. ``cd mangapages`` and then ``npm i`` (or ``yarn``)
3. ``npm start``

For images, simply have a web server or CDN (e.g imagekit which is what I am using) and upload the site logos there.

### Backend
#### Requirements
* Git
* Node.js
* Vercel
* Data (see note below)

#### Installation
1. ``git clone https://github.com/davidcralph/mangapages-backend``
2. ``cd mangapages`` and then ``npm i`` (or ``yarn``)
3. ``vercel dev``

You will need ``data.json`` and ``dataLightNovel.json`` files with contents in the format below in order to use this.

```js
[
  {
    title: "Hunter x Hunter",
    site: "viz",
    url: "https://www.viz.com/hunter-x-hunter",
  },
]
```
