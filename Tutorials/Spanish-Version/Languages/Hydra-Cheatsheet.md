
[Tutorials](../Tutorials/README.md) | [Tutorials in MiniTidal (TidalCycles), Hydra, & CineCer0](README.md)    

-------------------------------------------------------------------------------  

## Hydra (in Estuary): Guía Rápida

### Parameters
+ double
+ list of doubles = `[]`
-- Lists' tranformers:
  + `.fast(amount)` -- default: 1
  + `.smooth(amount)` -- default: 1

### Statements
-- Each statement is divided by a semicolon
+ `speed = double` -- default: 1 <br />
+ `setResolution(double,double)` <br />

### Imports

+ `s0`,`s1`,`s2`,`s3`

+ `initScreen(#)` // default: 0
+ `initCam(#)n` // default: 0
+ `initVideo("url")`
+ `initImage("url")`

### Sources

+ `osc(fequency, sync, rgb-offset)` // defaults: 60.0, 0.1, 0.0
+ `solid(r, g, b, a)` // defaults: 0.0, 0.0, 0.0, 1.0
+ `gradient(speed)` // default: 0.0
+ `noise(scale, offset)` // defaults: 10.0, 0.1
+ `shape(sides, radius, smoothing)` // defaults: 3.0, 0.3, 0.01
+ `voronoi(scale, speed, blending)` // defaults: 5.0, 0.3, 0.3
+ `src()` // options: (any output) `o0`, `o1`, `o2`, `o3` or (any imports) `s0`, `s1`, `s2`, `s3`


### Outputs
+ `.out(buffer)` // default: `o0` // other options: `o0`, `o1`, `o2`, `o3`
+ `render(buffer)` // default: all // other options: `o0`, `o1`, `o2`, `o3`


### Transformers
+ `.brightness(amount)` // default: 0.4
+ `.contrast(amount)` // default: 1.6
+ `.color(red, green, blue, alpha)` // vec4
+ `.colorama(amount)` // default: 0.005 -- shifts HSV values
+ `.invert(amount)` // default:1.0
+ `.luma(threshold, tolerance)` // defaults: 0.5, 0.1
+ `.hue(amount)` // default: 0.4
+ `.posterize(bins, gamma)` // defaults: 3.0, 0.6
+ `.saturate(amount)` // default: 2.0
+ `.shift(r, g, b, a)` // defaults: 0.5 for all
+ `.thresh(threshold, tolerance)` // defaults: 0.5, 0.04
+ `.kaleid(#sides)` // default: 4.0
+ `.pixelate(x, y)` // defaults: 20.0, 20.0
+ `.repeat(repeatX, repeatY, offsetX, offsetY)` // defaults: 3.0, 3.0, 0.0, 0.0
+ `.repeatX(reps, offset)`
+ `.repeatY(reps, offset)`
+ `.rotate(angle, speed)` // defaults: 10.0, 0.0
+ `.scale(size, xMult, yMult)` // defaults: 1.5, 1.0, 1.0
+ `.scroll(scrollX, scrollY, speedX, speedY)` // defaults: 0.5, 0.5, 0.0, 0.0
+ `.scrollX(scrollX, speed)`
+ `.scrollX(scrollY, speed)`


### Modulators

// t = texture = source => osc, solid, gradient, noise, shape, voronoi <br />

+ `.modulate(t, amount)` // amount’s default: 0.1
+ `.modulateHue(t, amount)` // default: 0.4
+ `.modulateKaleid(t, #Sides)` // default: 4.0
+ `.modulatePixelate(t, multiple, offset)` // defaults: 10.0, 3.0
+ `.modulateRepeat (t, repeatX, repeatY, offsetX, offsetY)` //defaults: 3.0, 3.0, 0.5, 0.5
+ `.modulateRepeatX (t, repeatX, offsetX)`
+ `.modulateRepeatY (t, repeatY, offsetY)`
+ `.modulateRotate(t, multiple, offset)` // defaults: 1.0, 0.0
+ `.modulateScale(t, multiple, offset)` // defaults: 1.0, 1.0
+ `.modulateScrollX(t, scrollX, speed)` // defaults: 0.5, 0.0
+ `.modulateScrollY(t, scrollY, speed)` // defaults: 0.5, 0.0


### Operators

+ `.add(t, amount)` // default: 0.5
+ `.mult(t, amount)` // default: 0.5
+ `.blend(t, amount)` // default: 0.5
+ `.diff(t)`
+ `.layer(t)`
+ `.mask(t, reps, offset)` // defaults: 3.0, 0.5


-
