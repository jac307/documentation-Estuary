
[Tutoriales](../Tutorials/README.md) | [Tutoriales en MiniTidal (TidalCycles), Hydra, y CineCer0](README.md)    

-------------------------------------------------------------------------------  

## CineCer0: Guía rápida

### Playing Videos, Images, or Text

+ `video "videoURL"`
+ `image "imageURL"`
+ `text "This is not a text"` -- lo que va entre comillas es el texto que aparecerá.

###  Position on Videos, Images, or Text

+ `setPosX [x] $` -- de izq (-1) a der 1
+ `setPosY [y] $` -- de abajo (-1) a arriba 1
+ `setCoord [x] [y] $`

###  Videos with Audio

+ `vol 0.5 $` -- sin vol 0 a máx vol 1

###  Video/Image functions

+ `setWidth [w] $` -- 1 = ancho natural
+ `setHeight [h] $` -- 1 = altura natural
+ `setSize [wh] $` --one parámetro afectara el ancho y la altura del video proporcionalmente
+ `setRotate [d] $` --parámetro en grados
+ `setOpacity [o] $` -- de 0 - 1 (sin opacidad)
+ `setBlur [bl] $` -- 0 = sin blur (1++ = más)
+ `setBrightness [br] $` -- 0-0.9 = menos, 1++ = más
+ `setContrast [c] $` -- 0-0.9 = menos, 1++ = más
+ `setGrayscale [g] $` -- 0 = a color, 1 = en escala de grises
+ `setSaturate [s] $` -- 1 = saturación natural (1++ = más, 1-- = menos)
+ `circleMask [m] $` -- 0 sin máscara, 0-0.99 más máscara (creciendo desde el centro)
+ `circleMask' [m] [x] [y] $` -- similar a circleMask pero con un tercer parámetro para modificar el punto central
+ `sqrMask [m] $` -- 0 sin máscara, 0-0.99 más máscara (creciendo desde el centro)
+ `rectMask [t] [r] [b] [l] $` -- acepta cuatro parámetros: arriba, derecha, abajo, izquierda, de donde dismonuye.
+ `z [n] $` -- cambios en en número de capa (layer)

###  Text Function

+ `size [n] $` --cambia el tamaño del texto creciendo de 1
+ `font "fontType" $` -- cambia el tipo de fuente
+ `colour "colour" $` -- cambia el color usando un número hexacolor
+ `rgb [r] [g] [b] $` -- cambia el colour usando los parametros de rojo verde azul, normalizado de 0 a 1
+ `rgba [r] [g] [b] [a] $` -- añade el parametro de alpha a rgb
+ `hsl [h] [s] [l] $` -- cambia el colour usando los parametros de hue saturación brillo, normalizado de 0 a 1
+ `hsla [h] [s] [l] [a] $` -- añade el parametro de alpha a hsl
+ `strike $` -- tacha el texto
+ `bold $` -- cambia el texto a negritas
+ `italic $` -- cambia el texto a itálicas
+ `z [n] $` -- cambios en en número de capa (layer)

###  Parámetros Dinámicos

+ `(ramp [Dur_In_Cycles] [Initial_Value] [End_Value])` -- parámetro dinámico que en un número determinado de ciclos (1++) va de un valor inicial a otro valor final.
+ `(range [Value_1] [Value_2] $ sin [Speed])` -- parámetro animado que va de un valor a otro y viceversa con una velocidad que puede ser lenta (cercana al 0), o más rápida incrementando el tercer valor.


-
