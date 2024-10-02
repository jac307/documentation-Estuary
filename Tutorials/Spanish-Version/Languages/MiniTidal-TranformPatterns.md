
[Tutoriales](../Tutorials/README.md) | [Tutoriales en MiniTidal (TidalCycles), Hydra, y CineCer0](README.md)    

-------------------------------------------------------------------------------  


## MiniTidal: Transformaciones y Patrones

Una vez que se tiene la estructura básica (i.e. `s "bd cp*2"`) se pueden añadir transformaciones (después de esta estructura básica) usando el símbolo `#`. Algunas de las transformaciones que puede añadir son: el filtro `vowel`, cambiar el volumen (`gain`), añadir paneo (`pan`), cambiar la nota (`note`) y cambiar el número de sample/audio (`n`).  

Otro tipo de transformaciones se puede añadir antes de la estructura básica (i.e. `s "bd cp*2"`) usando el símbolo `$`. Este es el caso para `slow` (alentar el ciclo) y `fast` (hacer más rápido el ciclo).  

En este tutorial se revisarán estas transformaciones.   

IMPORTANTE: cuidado con las comillas que usas. Éstas tienen que ser del tipo `""`, no “” (estas últimas generarán un error de sintaxis). Si haces copias y pegas las líneas de código de este tutorial code from this tutorial, revisa que tengan las comillas correctas ya que algunas veces se pueden cambiar.  

_________________________________________________________________________________________
_________________________________________________________________________________________

### El Filtro `vowel`

Reproduce lo siguiente:

+ `s "hh cp cp"`

Ahora, prueba con la siguiente línea de código:

+ `s "hh cp cp" # vowel "a"`

El patrón ahora tiene el filtro `vowel` activado. Los valores pueden ser: `a` `e` `i` `o` `u`  

Ahora, prueba con la siguientes líneas de código por separado:

+ `s "hh cp cp" # vowel "e"`
+ `s "hh cp cp" # vowel "i"`
+ `s "hh cp cp" # vowel "o"`
+ `s "hh cp cp" # vowel "u"`

Ahora, prueba jugando con el patrón sonoro:

+ `s "arpy cp arpy:2" # vowel "i"`
+ `s "sn sn:2 bd sn" # vowel "a"`
+ `s "[bd bd sn:5] [bd sn:3]" # vowel "e"`

_________________________________________________________________________________________
_________________________________________________________________________________________

### Cambiando el volumen (`gain`) + Patrones en los parámetros

Reproduce lo siguiente:

+ `s "hh cp cp"`

Prueba:

+ `s "hh cp cp" # gain 0.5`

Prueba:

+ `s "hh cp cp" # gain 1.2`

Los valores de `gain` van de `0` (sin sonido) a `2.0` (el volumen más alto que puedes obtener). Cuidado con los valores arriba de `1.5`.

Los ejemplos anteriores tienen únicamente un valor para `gain`, pero también se pueden añadir más valores.    

Prueba:

+ `s "hh cp cp" # gain "0.5 1.1 0.8"`

Puedes escuchar cómo los tres samples tienen diferentes volúmenes. Esto sucede porque ahora el parametro para `gain` en un patrón (usando diferentes valores dentro de comillas) con tres valores.  

Prueba este otro ejemplo:

+ `s "hh cp cp" # gain "0.5 1.1"`

En este ejemplo tenemos únicamente tres valores en `gain` con tres samples. El patrón de `gain` comienza al mismo tiempo que el patro de `s`, pero luego diferirá en los ciclos siguientes.  

IMPORTANTE: Para que funcionen los patrones en las transformaciones, se puede que tener el mismo número de samples (o un número mayor) en el patrón de `s`.

Prueba otras variaciones:

+ `s "arpy cp arpy:2" # gain "0.2 1 0.8”`
+ `s "sn sn:2 bd sn" # gain "0.5 1.1 0.8 0.4”`
+ `s "[bd bd sn:5] [bd sn:3]" # gain "0.5 1.1"`

_________________________________________________________________________________________
_________________________________________________________________________________________

### Paneo (`pan`)

¡Usa audífonos!  

Reproduce lo siguiente:

+ `s "hh cp cp"`

Prueba las siguientes líneas de código por separado:

+ `s "hh cp cp" # pan 0`
+ `s "hh cp cp" # pan 0.5`
+ `s "hh cp cp" # pan 1`

Los valores para `pan` van de `0` (canal izquierdo) a `1` (canal derecho).  

Puedes usar patrones para los parametros de `pan`:

+ `s "hh cp cp" # pan "0 0.5 1"`
+ `s "arpy cp arpy:2" # gain "0 1"`
+ `s "sn sn:2 bd sn" # gain "0.5 0.2 0.8 1"`
+ `s "[bd bd sn:5] [bd sn:3]" # gain "0.2 0.8"`

_________________________________________________________________________________________
_________________________________________________________________________________________

### Cambia el número de sample (`n`) + parámetros dinámicos

Reproduce lo siguiente:

+ `s "hh cp cp"`

Prueba las siguientes líneas de código por separado:

+ `s "hh cp cp" # n 1`
+ `s "hh cp cp" # n 3`

La función `n` es similar a usar `s "hh:1 cp:1 cp:1"` pero aplica el cambio de sample a todo el patrón sonoro. Los valores de `n` comienzan con `0` (por defecto reproducirán el primer archivo).  

Puedes también usar el valor dinámico `(choose[])` para generar variaciones aleatorias.  

Reproduce lo siguiente:

+ `s "hh cp cp" # n (choose[0,3,2])`

En este caso, el valor de `n` es elegido aleatoriamente considerando los parámetros dentro de los siguientes paréntesis `[]`.  

Otro valor dinámico que se puede usar es `(irand)` que usará un valor aleatorio que va de `0` al valor que le des en la función `irand`.  

Reproduce lo siguiente:

+ `s "hh cp cp" # n (irand 4)`

El valor de `n` es seleccionado aleatoriamente usando los primeros `5` archivos sonoros (¡estamos contando desde `0`!) de cada sample.  

Prueba las siguientes líneas de código:

+ `s "arpy cp arpy" # n (irand 2)`
+ `s "sn sn bd sn" # n (irand 3)`


_________________________________________________________________________________________
_________________________________________________________________________________________

### Modifica el tiempo del patrón (`slow` y `fast`)

Reproduce lo siguiente:

+ `s "hh cp cp"`

Reproduce lo siguiente:

+ `slow 2 $ s "hh cp cp”`
+ `fast 2 $ s "hh cp cp"`

The function `slow` alenta el tiempo del patrón, la función `fast` hace lo opuesto. Para ambos casos, el parametro `1` representa el tiempo por default, de ahí puede crecer y disminuir. No se pueden usar ambas funciones al mismo tiempo.   

Prueba las siguientes líneas de código:

+ `slow 1.3 $ s "arpy cp arpy:2"`
+ `fast 5 $ s "sn sn:2 bd sn"`
+ `slow 2 $ s "[bd bd sn:5] [bd sn:3]"`


_________________________________________________________________________________________
_________________________________________________________________________________________

### Transformaciones Múltiples

Mezcla todas las posibilidades!

+ `s "drum drum drum drum" # vowel "a o e e" # gain 1.2`
+ `fast 2 $ s "bd hh sn:1 hh sn:1 hh" # gain "1 0.7 0.5" # pan (choose[0,1])`
+ `slow 2 $ s "numbers:1 numbers:2 numbers:3 numbers:4" # pan "0 0.5 1" # vowel "a"`
+ `s "drum ~ drum drum" # n (choose [0,2,3]) # gain (choose[1, 1.2,0.8])`

¡Experimenta!

_________________________________________________________________________________________
_________________________________________________________________________________________

### Multiples Patrones Sonoros

+ Puedes reproducir múltiples patrones sonoros usando la siguiente estructura:

`stack [
s "drum drum drum drum" # vowel "a o e e" # gain 1.2,
fast 2 $ s "bd hh sn:1 hh sn:1 hh" # gain "1 0.7 0.5" # pan (choose[0,1])
 ]`  

Puedes añadir más patrones sonoros añadiendo una coma al final de cada patrón `,`. Todos los patrones sonoros deben estar dentro de `stack []`. El último patrón sonoro no debe de tener coma.

+ Reproduce lo siguiente:  

`stack [
s "drum drum drum drum" # vowel "a o e e" # gain 1.2,
slow 2 $ s "numbers:1 numbers:2 numbers:3 numbers:4" # pan "0 0.5 1" # vowel "a",
slow 2 $ s "numbers:1 numbers:2 numbers:3 numbers:4" # pan "0 0.5 1" # vowel "a",
s "drum ~ drum drum" # n (choose [0,2,3]) # gain (choose[1, 1.2,0.8])
]`

+ ¡Experimenta!  

Una parte importante de las prácticas de live coding es la improvisación: cambiando las funciones y parámetros en vivo, constantemente modificando cosas.
