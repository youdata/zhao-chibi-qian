# 赵孟頫 · 行书前赤壁赋

赵孟頫《行书前赤壁赋》（台北故宫博物院藏） — a narrated deep-zoom reading, as a static page (in Chinese).

Zhao Mengfu's running-script Former Ode on the Red Cliff (National Palace Museum, Taipei): his portrait of Su Shi, the title and the 45 columns, each with its modern reading.

Live: https://youdata.github.io/zhao-chibi-qian/

The image pyramid is a tile folder (`zhao-chibi-qian/`: `header.idx` + `{z}/{x}/{y}.png`), so any static host serves it.
Its fonts are in `fonts/`, trimmed to the page's characters. The narrated video is not included.

## How it is made

From `infographic-examples/zhao-chibi-qian/build.mjs` (the page) with rx (`~/rx-cli`):

```sh
node build.mjs                                                     # → zhao-chibi-qian.json
rx export zhao-chibi-qian.json --out site --app /rx-graphic-editor/web/index.html --canvas --theme dark --lock-layers --tiles dir
rx publish site --to github:youdata/zhao-chibi-qian --yes
```
