
[Tutorials](../Tutorials/README.md) | [Tutorials in MiniTidal (TidalCycles), Hydra, & CineCer0](README.md)    

-------------------------------------------------------------------------------  

## Hydra (in Estuary): Guía Rápida

### Parameters
+ número con decimal
+ lista de valores = `[]`
-- Transformadores para listas:
  + `.fast(valor)` -- default: 1
  + `.smooth(valor)` -- default: 1

### Statements
-- Las líneas de hydra se separan con un `;`
+ `speed = valor` -- default: 1
+ `setResolution(valor,valor)`

### Imports

+ `s0`,`s1`,`s2`,`s3`

+ `initScreen(#)` // default: 0
+ `initCam(#)n` // default: 0
+ `initVideo("url")`
+ `initImage("url")`

### Sources

+ `osc(frecuencia, sync, rgb-offset)` // defaults: 60.0, 0.1, 0.0
+ `solid(r, g, b, a)` // defaults: 0.0, 0.0, 0.0, 1.0
+ `gradient(velocidad)` // default: 0.0
+ `noise(scale, offset)` // defaults: 10.0, 0.1
+ `shape(lados, radio, smoothing)` // defaults: 3.0, 0.3, 0.01
+ `voronoi(escala, velocidad, blending)` // defaults: 5.0, 0.3, 0.3
+ `src()` // opciones: (outputs) `o0`, `o1`, `o2`, `o3` o (imports) `s0`, `s1`, `s2`, `s3`


### Outputs
+ `.out(buffer)` // default: `o0` // opciones: `o0`, `o1`, `o2`, `o3`
+ `render(buffer)` // default: all // opciones: `o0`, `o1`, `o2`, `o3`


### Transformers
+ `.brightness(valor)` // default: 0.4
+ `.contrast(valor)` // default: 1.6
+ `.color(red, green, blue, alpha)` // vec4
+ `.colorama(valor)` // default: 0.005 -- desplaza los valores de HSV
+ `.invert(valor)` // default:1.0
+ `.luma(threshold, tolerance)` // defaults: 0.5, 0.1
+ `.hue(valor)` // default: 0.4
+ `.posterize(bins, gamma)` // defaults: 3.0, 0.6
+ `.saturate(valor)` // default: 2.0
+ `.shift(r, g, b, a)` // defaults: 0.5 para todos
+ `.thresh(threshold, tolerancia)` // defaults: 0.5, 0.04
+ `.kaleid(#sides)` // default: 4.0
+ `.pixelate(x, y)` // defaults: 20.0, 20.0
+ `.repeat(repeatX, repeatY, offsetX, offsetY)` // defaults: 3.0, 3.0, 0.0, 0.0
+ `.repeatX(reps, offset)`
+ `.repeatY(reps, offset)`
+ `.rotate(ángulo, velocidad)` // defaults: 10.0, 0.0
+ `.scale(size, xMult, yMult)` // defaults: 1.5, 1.0, 1.0
+ `.scroll(scrollX, scrollY, speedX, speedY)` // defaults: 0.5, 0.5, 0.0, 0.0
+ `.scrollX(scrollX, velocidad)`
+ `.scrollX(scrollY, velocidad)`


### Modulators

// t = texture = source => osc, solid, gradient, noise, shape, voronoi

+ `.modulate(t, valor)` // amount’s default: 0.1
+ `.modulateHue(t, valor)` // default: 0.4
+ `.modulateKaleid(t, #Sides)` // default: 4.0
+ `.modulatePixelate(t, multiple, offset)` // defaults: 10.0, 3.0
+ `.modulateRepeat (t, repeatX, repeatY, offsetX, offsetY)` //defaults: 3.0, 3.0, 0.5, 0.5
+ `.modulateRepeatX (t, repeatX, offsetX)`
+ `.modulateRepeatY (t, repeatY, offsetY)`
+ `.modulateRotate(t, multiple, offset)` // defaults: 1.0, 0.0
+ `.modulateScale(t, multiple, offset)` // defaults: 1.0, 1.0
+ `.modulateScrollX(t, scrollX, velocidad)` // defaults: 0.5, 0.0
+ `.modulateScrollY(t, scrollY, velocidad)` // defaults: 0.5, 0.0


### Operators

+ `.add(t, valor)` // default: 0.5
+ `.mult(t, valor)` // default: 0.5
+ `.blend(t, valor)` // default: 0.5
+ `.diff(t)`
+ `.layer(t)`
+ `.mask(t, reps, offset)` // defaults: 3.0, 0.5


-
