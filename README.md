## Diamond Square Terrain Generation

This is a simple implementation of the [Diamond Square Algorithm](https://en.wikipedia.org/wiki/Diamond-square_algorithm) in vanilla JS ES5. This algo is used to generate semi-realistic terrain heightmaps. 

Quoting Wiki for definition:

> The diamond-square algorithm is a method for generating heightmaps for computer graphics. It is a slightly better algorithm than the three-dimensional implementation of the midpoint displacement algorithm which produces two-dimensional landscapes. It is also known as the random midpoint displacement fractal, the cloud fractal or the plasma fractal, because of the plasma effect produced when applied.

#### Usage

The module exports a single function, which accepts the size `n` of the terrain you want to generate and returns a 2D array of size `2^n x 2^n`. The value of each point in the terrain can range from 0 to 1.

```
var terrain = diamondSquareTerrain(<size in order of 2>);
```

Example:

```
var diamondSquareTerrain = require('diamond-square-terrain');
var terrain = diamondSquareTerrain(8); // Returns a 2D array of size 256x256
var terrain = diamondSquareTerrain(5); // Returns a 2D array of size 32x32
```

#### Sample output

![Array mapped to an image](https://cloud.githubusercontent.com/assets/304605/12910178/1ab089d0-cf2e-11e5-9a01-28656919522e.png "Array mapped to an image")
