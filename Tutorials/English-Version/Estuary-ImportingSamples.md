
[Tutorials](../Tutorials/README.md) | [Home](../../README.md)    

-------------------------------------------------------------------------------  


## Temporally importing samples in Estuary

If you have not made your repo a GitHub Page, please follow [GitHub: Setup](GitHub-setup.md){:target="_blank"} tutorial first.

+ On your repository, go to the section you have uploaded your sound files.
+ Create a new file.

In this example, I have a folder named "Sound" with three sub-folders with different samples.  

<img src="imgs/26.png" width="600">  

+ Name your file and add the extension ".json".  

<img src="imgs/27.png" width="600">  

+ You will make a list of your sound samples `[]`.  

The sintax is the following: `[ { "url":"locationInGitHub","type":"audio","bank":"name-of-the-bank","n":samplesNumber} ]`.

<img src="imgs/28.png" width="600">  

+ Write the correct information in those fields.  

<img src="imgs/29.png" width="300"><img src="imgs/30.png" width="300">  

In this example, I have three folders/banks (150, 151, 152) with three sound samples in each folder. The location is `"nameOfFolder/file.extension"`, in `name-of-the-bank` I am keeping the name of the folder (but this can be different), lastly, `samplesNumber` should start from 0,1,2...  

<img src="imgs/31.png" width="600">  

+ Add more files if needed separated by commas.  
+ Press commit at the end of the page.  

<img src="imgs/32.png" width="600"><img src="imgs/33.png" width="300">  

You can see the file now. In this example, I finished adding the information of the other files I have.

<img src="imgs/34.png" width="600">  

+ Go to the folder where you have the new .json file and edit the README.md file there.  
+ Add a link to the .json file by following this sintax: `[text](url or location-on-GitHub)`, Commit changes.   

<img src="imgs/35.png" width="600">
<img src="imgs/36.png" width="600">

+ Confirm the link works.  

<img src="imgs/37.png" width="600">   

+ If you have uploaded and created these files inside of a folder/sub-folder, go to the beginning of your repository.  
+ Edit the README file there and add a link to your previous, Sound README file.  
These steps are not necesarry if you have all your files in the main repo.  

<img src="imgs/38.png" width="600">
<img src="imgs/39.png" width="600">

+ Go to "Settings", then "Pages", click on the site's url.   

<img src="imgs/40.png" width="600">

+ Click until you get to your .json file / Dale click hasta entrar a tu archivo de .json.  
In this example, I have to go to Sound Samples, then Samples.  

<img src="imgs/41.png" width="600">
<img src="imgs/42.png" width="600">

Something like this should appear.  
+ Copy the URL / Copia la URL.  

<img src="imgs/43.png" width="600">

+ Go to one of your README files (In this case, I will modify the README on Sound).  

<img src="imgs/44.png" width="600">

+ Add the following: `!reslist "paste-url"`.  
In this case, I also added some other information about the samples.   

<img src="imgs/45.png" width="600">
<img src="imgs/46.png" width="600">

+ Go to: <a href="https://estuary.mcmaster.ca/" target="_blank">Estuary</a>
+ Go into Solo Mode or enter an ensamble.  
+ In the terminal, send your `!reslist "pasted-url"`.  

<img src="imgs/47.png" width="600">  

Now you can use your samples!

<img src="imgs/48.png" width="300"><img src="imgs/49.png" width="300">   

In Solo Mode, you will have to do this last step everytime you enter. In Collaborative/Ensamble mode, it should be saved.  
En Modo Solo, tendrás que hacer este último paso cada vez que entres. En modo Colaborativo/Ensamble, se deberían guardar.   


<img src="imgs/50.png" width="600">
