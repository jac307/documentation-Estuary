  
[Tutorials](../Tutorials/README.md) | [Home](../README.md)    
  
-------------------------------------------------------------------------------  
  
## JSoLangs: Simple Text Replacement / Reemplazo de Texto Simple
  
JSoLangs is an application in <a href="https://estuary.mcmaster.ca/" target="_blank">Estuary</a> to parse available live coding language to create new ones.  
Los JSoLangs es una aplicación en <a href="https://estuary.mcmaster.ca/" target="_blank">Estuary</a> que permite parsear lenguajes de live coding disponibles para crear nuevos.  
  
For this tutorial, I have created this [folder](../JSoLang/README.md) to host a simple text replacement template as well as some examples.  
Para este tutorial, he agregado esta [carpeta](../JSoLang/README.md) que contiene un template simple de reemplazo de texto, así como algunos ejemplos.  
  
JSoLangs can be written directly on Estuary but it is always better to write and save your JSoLang locally or in any other platform. For my project, I am using GitHub.  
Los JSoLangs pueden escribirse directamente en Estuary pero siempre es mejor guardarlos localmente o en alguna otra plataforma. Para mi proyecto estoy usando GitHub.  
  
+ Create a `name.peg` file / Crea un archivo `name.peg`.  
  
<img src="imgs/77.png" width="600">  
<img src="imgs/78.png" width="600">  

+ Write and save your JSoLang / Escribe y guarda tu JSoLang.  
For this project, I have this [template](../JSoLang/template-jsolang.peg) / Para este proyecto tengo este template [template](../JSoLang/template-jsolang.peg) 

  + `name-of-jsolang` = Name your JsoLang / Nombra tu JsoLang.  
  + `language-parsing` = Write the name of one of the lc languages in Estuary / Escribe el nombre de alguno de los lenguajes de lc que hay en Estuary.   
  + `a-function or a-conjunction-of-functions` = Write the function(s) you want to translate / Escribe la(s) funcion(es) que quieras traducir.  
  + `word` = Write the word you want to use to replace the above / Escribe la palabra que quieres para reemplazar lo anterior.  
  + `"word"i` = Write the word again inside quotation marks / Escribe de nuevo la palabra pero entre comillas.  
       + `i` = case sensitive / sensible al cambio de may/min.
       + erase the i so it is not case sensitive / borra el i para que no sea sensible al cambio de may/min.  
  + `words-to-add-divided-by-slash` = Write all the words you used divided by "/" / Escribe todas las palabras que usaste divididas por "/".  

<img src="imgs/79.png">  
  
+ Go to: / Ve a: <a href="https://estuary.mcmaster.ca/" target="_blank">Estuary</a>
+ Copy/Paste your JSoLang in one editor-box. Evaluate and check for sintax errors / Copia/Pega tu JSoLang en un editor de texto. Evalúa y checa por errores de sintaxis.  
+ In a different editor-box write: `##name-of-jsolang` / En un editor de texto diferente, escribe: `##name-of-jsolang`.    
+ You can now use this second box to write with your new sintax / Ahora puedes usar este segundo editor para escribir con tu nueva sintaxis.    
  
<img src="imgs/80.png">    
  
  
_________________________________________________________________________________________
  
### Example 1: Text Replacement with MiniTidal / Ejemplo 1: Reemplazo de Text con MiniTidal

[This](../JSoLang/drSeuss.peg) is the JSoLang I wrote with the name `drSeuss`, where you can run the following sintax:    
  `I donT like "green" eggs 0.9 and ham 1.0`.   
which translate in MiniTidal as:  
  `slow 3.2 $ s "alphabet:4 alphabet:6 alphabet:6 alphabet:18 # gain 0.9 # up 1.0"`  
  
[Este](../JSoLang/drSeuss.peg) que escribí con el nombre de `drSeuss`, donde puedes correr la siguiente sintaxis:    
  `I donT like "green" eggs 0.9 and ham 1.0`.   
que se traduce en MiniTidal como:  
  `slow 3.2 $ s "alphabet:4 alphabet:6 alphabet:6 alphabet:18 # gain 0.9 # up 1.0"`  
  
I have seven translations: / Tengo siete traducciones:    
  
+ `like = "like"i { return "s" }` =
  
+ `eggs = "eggs"i { return " # gain" }` and `ham = "ham"i { return "# up" }` =
  
+ `green = "green"i { return "alphabet:4 alphabet:6 alphabet:6 alphabet:18" }` =
  
+ `I = "I"i { return "slow 3.2 $" }` =
  
+ `and = "and"i { return "" }` and `donT = "donT"i { return "" }` =
  
<img src="imgs/83.png" width="600">  
  
_________________________________________________________________________________________
  
### Example 2: Text Replacement with CineCer0 / Ejemplo 2: Reemplazo de Text con CineCer0
  
<img src="imgs/81.png" width="600"><img src="imgs/82.png" width="600">  
  
_________________________________________________________________________________________
  
### Example 3: Text Replacement with Hydra / Ejemplo 3: Reemplazo de Text con Hydra
  
<img src="imgs/84.png" width="600"><img src="imgs/85.png" width="600">  
  
