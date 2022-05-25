## Temporally importing samples in Estuary / Importando samples temporalmente en Estuary

1. On your repository, go to the section you have uploaded your sound files / Es tu repositorio, ve a la sección donde has subido tus archivos de sonido.  
2. Create a new file / Crea una nuevo archivo.  
  
In this example, I have a folder named "Sound" with three sub-folders with different samples.  
En este ejemplo tengo un folder llamado "Sound" con tres sub-folders con differentes sonidos.  
  
<img src="imgs/26.png" width="600">  
  
2. Name your file and add the extension ".json" / Escribe el nombre y agrega la extensión ".json".  
  
<img src="imgs/27.png" width="600">  
   
3. You will make a list of your sound samples `[]` / Escribirás una lista con tus samples de sonido `[]`.  
  
The sintax is the following: `[ { "url":"locationInGitHub","type":"audio","bank":"name-of-the-bank","n":samplesNumber} ]`.  
La sintaxis es la siguiente: `[ { "url":"locaciónEnGitHub","type":"audio","bank":"nombre-del-banco","n":númeroDeSample} ]`.  
  
<img src="imgs/28.png" width="600">  
   
4. Write the correct information in those fields / Escribe la información correcta en esos campos.  
  
<img src="imgs/29.png" width="600"><img src="imgs/30.png" width="600">  
   
In this example, I have three folders/banks (150, 151, 152) with three sound samples in each folder. The location is `"nameOfFolder/file.extension"`, in `name-of-the-bank` I am keeping the name of the folder (but this can be different), lastly, `samplesNumber` should start from 0,1,2...  
En este ejemplo tengo tres carpetas/bancos (150, 151, 152) con tres archivos cada una. La locación es `"nombreDelFolder/archivo.extensión"`, en `nombre-del-banco` estoy conservando el nombre el folder (pero éste puede ser diferente), por último, `númeroDeSample` debe comenzar desde 0,1,2...  
  
<img src="imgs/31.png" width="600">  
   
5. Add more files if needed separated by commas / Añade más archivos, si es necesario, separados por comas.  
6. Press commit at the end of the page / Envía tu commit al final de la páguina.  
  
<img src="imgs/32.png" width="600"><img src="imgs/33.png" width="600">  
   
You can see the file now. In this example, I finished adding the information of the other files I have.  
Puedes ver tu archivo publicado ahora. En este ejemplo, terminé de añadir los archivos restantes que tengo.  
  
<img src="imgs/34.png" width="600">  
   
   
   
   
   
   
   
