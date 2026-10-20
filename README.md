# kathack

tribute mirror of [kathack.com](http://kathack.com/), the 2011 katamari damacy bookmarklet by alex leone, david nufer and david truong.

the original is still up but only over http, so the bookmarklet (which loads `http://kathack.com/js/kh.js`) gets blocked as mixed content on basically every site now. this copy serves the same page, kh.js, jquery 1.5.1 and the music over https.

changes vs the original (see `0.original/` for the untouched files):

- bookmarklet urls are built from wherever the page is served instead of hard-coded http urls
- `kh.js` derives its own base url (for the mp3 and the popup link) from its script tag
- controls are spelled out on the page: hold right-click and move the mouse
- google analytics snippet removed

controls were never the problem by the way: the game works in chromium, webkit, headed and headless, as long as you actually hold the mouse button.

## run locally

```
python3 -m http.server -d site 8000
```

## deploy

static disco project, `disco.json` points at `site/`.
