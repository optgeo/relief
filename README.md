# relief
Natural Earth II image tiles for extremely small scales

Feel free to use this. You can load the tiles using the following information. 

## sources

```hocon
sources: {
  relief: {
    type: raster
    tiles: [
      "https://optgeo.github.io/relief/zxy/{z}/{x}/{y}.png"
    ]
    tileSize: 512
    minzoom: 0
    maxzoom: 5
    attribution: "Made with Natural Earth" # this is optional
  }
}
```

## layers

```hocon
layers: [
  {
    id: relief
    type: raster
    source: relief
    minzoom: 0
    maxzoom: 18 # or anything you want
  }
]
```
