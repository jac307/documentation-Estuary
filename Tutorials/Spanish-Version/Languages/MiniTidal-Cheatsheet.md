
[Tutoriales](../README.md) | [Tutoriales en MiniTidal (TidalCycles), Hydra, y CineCer0](README.md)    

-------------------------------------------------------------------------------  

## MiniTidal: Guía Rápida

### Patrones Sonoros Básicos

+ `s "sound"` -- un sonido en cada ciclo
+ `s "sound sound"` -- dos sonidos en cada ciclo
+ `s "sound*4"` --un sonido cuatro veces en cada ciclo
+ `s "sound:2"`--reproduce el archivo 2 de ese sample
+ `s "<sound sound>"` --cada ciclo tiene un sonido diferente
+ `s "[sound sound] sound"` -- la primera mitad del ciclo reproduce dos sonidos (más rápido), la segunda mitad del ciclo reproduce un sonido (más lento)
+ `s "[sound sound]/3 sound"` --la primera mitad del ciclo reproduce dos sonidos pero esta vez el tiempo se divide percibiéndose más lento.

### Funciones-Transformaciones aplicadas "antes" del patrón sonoro

+ `slow 1 $` -- alenta el ciclo, 1++ = más lento.
+ `fast 1 $` -- acelera el ciclo, 1++ = más rápido.
+ `chop 8 $` -- corta los audios en un # de veces.
+ `striate 8 $` -- granula el sonido.
+ `degrade $` -- de manera aleatoria remueve eventos sonoros.
+ `rev $` -- da una versión en reversa del patrón sonoro.
+ `jux ([transformation]) $` -- crea un sonido stereo extraño aplicando una función-transformación.
+ `every 2 ([transformation]) $` -- aplica una función-transformación cada # de ciclos.
+ `always ([transformation]) $` -- aplica una función-transformación un % de veces. Otros posibles parametros: `almostAlways`, `often`, `sometimes`, y `rarely`.

### Funciones-Transformaciones aplicadas "después" del patrón sonoro

+ `# gain 1` -- cambia el volumen; 1 = normal vol, 1-- = menos, 1++ =más (aunque el valor sea mayor, esta función tiene un máx de 2 por seguridad).
+ `# n 0` -- cambia el número de los samples.
+ `# note 0` -- cambia la nota.
+ `# speed 0` -- cambia la velocidad; 1 = normal.
+ `# pan 0.5` -- mueve el sonido por las bocinas; 1 = derecha, 0 = izquierda
+ `# vowel "a"` --aplica un filtro; valores: `e`, `i`, `o`, `u`
+ `# shape 5` -- produce una distorsión de onda; 0 = sin distorsión.
+ `# accelerate 2` -- similar a speed.
+ `# begin 0.1` -- corta el inicio de los samples
+ `# end 0.9` -- corta el final de los samples

### Parámetros Dinámicos

+ `"1 2 3 4"` -- un patrón de parámetros, funciona completamente únicamente si se tiene el mismo número (o más) samples.
+ `(choose[1,2,3,4])` --el parámetro es seleccionado dentro de los valores de la lista
+ `(irand 5)` -- parámetro que oscila entre 0 y el valor que le das
+ `(rand + 0.5)` -- parámetro que oscila entre 0 y 1 + el valor que le das; en este ejemplo, oscila entre 0.5 y 1.5

### Multiples Statements

`stack[
statement-1,
statement-2
]`






-
