# coordinates-transformer

Transform coordinates between projections (coordinate systems).

```
npm install --save coordinates-transformer
```

## Usage

```
import transform from 'coordinates-transformer'
```
```
transform([12345.36, 6730006.31], 'EPSG:25833', 'EPSG:4258')
// Returns: [ 6.129140025806947, 60.41006820280935 ]
```

## API

```
(coordinates: [number, number], fromProjection: EpsgCode, toProjection?: EpsgCode) => [number, number]
```

All coordinates are on the format `[longitude, latitude]` format (or `[easting, northing]`).

If the third parameter `toProjection` is omitted, `EPSG:4258` is used.

An EPSG code represents a projection (coordinate system). Read about EPSG on https://epsg.io/ or https://register.geonorge.no/epsg-koder (Norwegian site).

Available EPSG codes:

* `EPSG:4258` (lat/long)
* `EPSG:25831` (UTM 31)
* `EPSG:25832` (UTM 32)
* `EPSG:25833` (UTM 33)
* `EPSG:25834` (UTM 34)
* `EPSG:25835` (UTM 35)
* `EPSG:25836` (UTM 36)
