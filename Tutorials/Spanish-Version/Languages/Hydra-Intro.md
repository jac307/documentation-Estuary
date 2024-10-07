
[Tutoriales](../Tutorials/README.md) | [Tutoriales en MiniTidal (TidalCycles), Hydra, y CineCer0](README.md)    

-------------------------------------------------------------------------------  

## Hydra: Intro

Hydra es una plataforma de live coding para síntesis visual basado en los desarrollos visuales que los sintetizadores análogos generan. Hydra es un proyecto open-source desarrollado por [Olivia Jack](https://ojack.github.io/){:target="_blank"}.  

Hidra en Estuary es una versión reducida del stand-alone de Hydra.  

### Primeros pasos

Ve a [https://estuary.mcmaster.ca/](https://estuary.mcmaster.ca/){:target="_blank"}  
Selecciona SOLO MODE (Modo Solo).  

<img src="imgs/minitidal-01.jpg" width="600">

Encontraras un espacio de trabajo con 6 editores de código. Cada editor tiene un menu vacío en la parte superior izquierda. Estuary permite trabajar con diferentes lenguajes para live coding. Puedes elegir el lenguaje de programación que quieras operar en este menú.  

<img src="imgs/minitidal-02.jpg" width="600">

Selecciona Hydra en el menú de uno de los editores.

<img src="imgs/hydra-01.jpg" width="600">

Escribe lo siguiente y presiona el botón de play (o también puedes presionar shift+return/enter).  

+ `osc().out()` = esta línea reproducirá un oscilador en escala de grises.

IMPORTANTE: cuidado con las comillas que usas. Éstas tienen que ser del tipo `""`, no “” (estas últimas generarán un error de sintaxis). Si haces copias y pegas las líneas de código de este tutorial code from this tutorial, revisa que tengan las comillas correctas ya que algunas veces se pueden cambiar.  

Cambia `osc().out()` por otras fuentes disponibles:  

+ `voronoi().out()`
+ `noise().out()`

_________________________________________________________________________________________
_________________________________________________________________________________________

### Fuentes - Sources

Una de las estructuras más simples de hydra es la siguiente:

+ `fuente` + `.` + `salida`

Las fuentes son elementos o objetos iniciales que puedes generar en Hydra:

+ `osc()`
+ `voronoi()`
+ `shape()`
+ `noise()`
+ `solid()`

`out()` es la sintaxis para la salida.

Ejemplo:

+ `solid()` + `.` + `out()`

#### Fuente: `solid(r,g,b)`

<img src="imgs/hydra-02.jpg" width="600">

`solid().out` generará un sólido con parámetros por defecto: (0,0,0,1) = negro.

En el entorno digital, la composición de color se puede realizar a través de diferentes modelos.

Los parámetros para crear sólidos en Hydra son a partir del modelo RGB que toma los colores primarios modificando la intensidad a través de los tres canales, añadiendo un cuarto canal: RGBA = "alpha", que modifica la opacidad o transparencia.  

Ejemplos:

+ `solid(1).out()` // Sólido rojo
+ `solid(0,1).out()` // Sólido verde
+ `solid(0,0,1).out()` // Sólido azul
+ `solid(1,1,1).out()` // Sólido blanco
+ `solid(0.3,0,0.5).out()` // Sólido morado
+ `solid(0.5,0.5,0.9,0.5).out()` // Sólido con opacidad al 50%

Los parámetros pueden ser enteros (int), decimales (double), y listas []. Este último resultará en un tipo de modulación discreta (con saltos ya que no pasa por números intermedios).

+ `solid([0.4,0.5,0.0,1.0],0,0).out()` // Sólido con modulaciones en el canal rojo
+ `solid([0.4,0.5],[0.0, 0.5],[0.1, 0.2]).out()` //Sólido con modulaciones en los canales RGB

#### Fuente: `gradient(velocidad)`

<img src="imgs/hydra-03.jpg" width="600">

`gradient().out()` generarán una gradiente con parámetros por defecto: (0).

El valor (velocidad) modifica la rapidez de cambio de la posición de colores dentro del círculo cromático = varia los tonos del gradiente.

Ejemplos:

+ `gradient(1).out()` // Velocidad de cambio relativamente lenta
+ `gradient(40).out()` // Velocidad de cambio rápida
+ `gradient([1,2,0.5]).out()` // Modulación de la velocidad de cambio

#### Fuente: `osc(frecuencia, sincronización, impresionDeColor)`

<img src="imgs/hydra-04.jpg" width="600">

`osc().out()` generará un oscilador con parámetros por defecto: (60,0.1,0).

Los osciladores generan señales (en este caso de color) periódicas. La modulación de frecuencia produce variaciones en las oscilaciones visibles (un tipo de efecto de línea en gradiente): entre más alta, más oscilaciones.

+ `osc(2).out()`
+ `osc(40).out()`
+ `osc(400).out()`

El segundo parámetro (sincronización) corresponde a la velocidad de las oscilaciones.

+ `osc(40,0).out()` // Sin movimiento
+ `osc(40,0.3).out()` // Los número arriba del 0 aceleran las frecuencias visibles

Ejemplos:

+ `osc(40,0.1,0.5).out()` // Oscilador con el tercer parámetro(colorRGB)
+ `osc(40,0.1,[2.0,0.5,1.0]).out()` // Modulación del canal de color utilizando listas
+ `osc([4,100],[0.1,0.5],[2.0,0.5,1.0]).out()` // Modulación de todos los parámetros


#### Fuente: `noise(escala, velocidad)`

<img src="imgs/hydra-05.jpg" width="600">

`noise().out()` genera una textura similar al Ruido Perlin (o la estática visible generada en los televisores). Parámetros por defecto (10,0.1)

El primer parámetro (escala) modifica el tamaño de los gradientes (formas) generados. En parámetros chicos, la escala es mayor; parámetros grandes, la escala es menor.

+ `noise(2).out()`
+ `noise(100).out()`

Ejemplos:

+ `noise(2,4).out()` // Noise con un parámetro de velocidad mayor
+ `noise([5.5, 10, 20.7],2).out()` // Noise con modulación en la escala
+ `noise([5.5, 10, 20.7],[2,0,4]).out()` //Noise con modulación en ambos parámetros


#### Fuente: `voronoi(escala, velocidad, combinación)`

<img src="imgs/hydra-06.jpg" width="600">

`voronoi().out()` genera una textura a partir de la partición del espacio con contrucciones geométricas, esto se llama Polígonos de Thiessen (Voronoi diagram). Parámetros por defecto: (5,0.3,0.3).

El tercer parámetro corresponde a la forma en que las construcciones geométricas se combinan. Valores grandes generan un tipo de espacios negativos (en negro) que deforma los polígonos. Valores negativos crean un espacio positivo (en blanco) entre ellos.

+ `voronoi(5,0.3,2).out()` // Voronoi con espacios negativos entre polígonos
+ `voronoi(5,0.3,-2).out()` // Voronoi con espacios positivos entre polígonos

Ejemplos:

+ `voronoi(3).out()` // Voronoi a una escala grande
+ `voronoi(30,40).out()` // Voronoi a una escala pequeña con una velocidad rápida
+ `voronoi(1,0.3,2).out()` // Voronoi con una escala mayor entre espacios negativos
+ `voronoi(100,5,-1).out()` // Voronoi con una escala pequeña entre espacios positivos a una velocidad mediana
+ `voronoi([1,10,100],0.3).out()` // Voronoi con modulación en la escala
+ `voronoi([4,30,70,10],[0.1,3],[-1,1,-2]).out()` // Voronoi con modulación en todos los parámetros


#### Fuente: `shape(lados, radio, difuminado)`

<img src="imgs/hydra-07.jpg" width="600">

`shape().out()`se utiliza para generar un polígono, modificando los tres parámetros para generar formas más complejas. Parámetros por defecto: (3,0.3,0.01)

Ejemplos:

+ `shape(5).out()` // Pentagono
+ `shape(8,0.9).out()` // Octágono con un tamaño grande
+ `shape(4,0.5,0.1).out()` // Rectángulo con límites difuminados
+ `shape(3,[0.1,0.2,0.3,0.4]).out()` // Triángulo con modulación en el tamaño
+ `shape([3,4,5],[0.1,0.5,0.2],[0.5,0.2]).out()` // Diferentes formas que están siendo moduladas en los tres parámetros



--
