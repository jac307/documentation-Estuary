
[Tutorials](README.md) | [Home](../../README.md)

-------------------------------------------------------------------------------

<style>
  .tts-button {
    position: fixed;
    top: 20px;
    right: 20px;
    padding: 10px 15px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }

  .tts-button:hover {
    background-color: #45a049;
  }
</style>

<button class="tts-button" onclick="speakText()">🔊 Read Aloud</button>

<script>
  function speakText() {
    let text = document.body.innerText;
    let speech = new SpeechSynthesisUtterance(text);
    speech.lang = "en-US"; // Set language
    speech.rate = 1; // Adjust speed (1 = normal)
    window.speechSynthesis.speak(speech);
  }
</script>

# Codework: Executable Code-Poetry  

**John Cayley**’s categories include **functional codeworks**, which merge executable commands with creative writing. These works are both **human-readable** and **computer-executable**.  

**Cayley, J. (2006).** *Time code language: New media poetics and programmed signification.*  
In **New Media Poetics: Contexts, Technotexts, and Theories**, pp. 307-334.  

---  

## 🔹 **Executable Code-Poetry in MEMORIAS**  

The **code-poetry** of *[Jessica A. Rodriguez](https://vimeo.com/jessicaarianne)*, particularly her project *[MEMORIAS](https://jac307.github.io/MEMORIAS/)*, exemplifies **executable code-poetry**, blending **Live Coding** and **Electronic Literature**.  

<iframe src="https://player.vimeo.com/video/565310015" width="90%" height="90%" frameborder="0" allowfullscreen></iframe>

**MEMORIAS** is a web-based project featuring **six executable codeworks**, integrating natural languages (**Spanish, English, Spanglish**) with **computing languages** to generate audiovisual textures.  

---

# 🌟 **Codework Activity: Writing Executable Code-Poetry in Estuary**  

**Level:** Intermediate  

## 🎯 **Objective**  
Explore the intersection of **computer language syntax and poetry** by crafting an **executable code-poem** using **JSoLangs** in <a href="https://estuary.mcmaster.ca/" target="_blank">Estuary</a>.  


## 💻 **Technologies**  

**Estuary** is a *live coding platform for collaboration and experimentation with sound, music, and visuals in a web browser.*  

**JSoLangs** are *small JavaScript programs* [built with the peggyjs/peggy library] *that transpile live-coded text into one or more of Estuary’s underlying languages* (Ogborn, et al., 2021).  

📖 **Reference:** Ogborn, D., Littler, C., & Sicchio, K. (2021).  
*<a href="https://works.hcommons.org/records/fpq3s-6b149" target="_blank">JSoLangs: Ephemeral esolangs in a collaborative live coding environment</a>.* CSDH/SCHN @ Congress - 2021 University of Alberta.  


---  

## 🔹 **Step 1: Choose Your Live Coding Tool**  

JSoLangs allow you to create **new poetic languages** on top of Estuary’s existing live coding environments. First, choose one of the following tools:  

- 🎨 **Hydra** → For **video synthesis** (generative visuals).  
- 🎞 **CineCer0** → For **text-based animation & video manipulation**.  
- 🎵 **TydalCycles (MiniTidal)** → For **musical event patterning**.  

💡 **Tip:** Choose the tool that best fits your artistic or conceptual goals!  

---  

## 🔹 **Step 2: Learn the Basics of Your Chosen Tool**  

📌 Follow these tutorials to **learn how your tool works**:  

### **Hydra**  
- <a href="Languages/Hydra-Intro.md" target="_blank">Hydra: Intro</a>  
- <a href="Languages/Hydra-Transformers.md" target="_blank">Hydra: Transformers</a>  
- <a href="Languages/Hydra-ModOpe.md" target="_blank">Hydra: Modulators & Operators</a>  
- <a href="Languages/Hydra-AdvanceReferences.md" target="_blank">Hydra: Advanced References</a>  
- <a href="Languages/Hydra-Cheatsheet.md" target="_blank">Hydra: Cheatsheet</a>  

### **CineCer0**  
- <a href="Languages/CineCer0-Intro.md" target="_blank">CineCer0: Intro</a>  
- <a href="Languages/CineCer0-Transformations.md" target="_blank">CineCer0: Transforming Text, Image, or Video</a>  
- <a href="Languages/CineCer0-DynValues.md" target="_blank">CineCer0: Dynamic Values</a>  
- <a href="Languages/CineCer0-AdvanceReferences.md" target="_blank">CineCer0: Advanced References</a>  
- <a href="Languages/CineCer0-Cheatsheet.md" target="_blank">CineCer0: Cheatsheet</a>  

### **TydalCycles (MiniTidal)**  
- <a href="Languages/MiniTidal-Intro.md" target="_blank">MiniTidal: Intro</a>  
- <a href="Languages/MiniTidal-TranformPatterns.md" target="_blank">MiniTidal: Transform Patterns</a>  
- <a href="Languages/MiniTidal-AdvanceReferences.md" target="_blank">MiniTidal: Advanced References</a>  
- <a href="Languages/MiniTidal-Cheatsheet.md" target="_blank">MiniTidal: Cheatsheet</a>  


📌 **Explore:**  
✅ Identify **basic commands & syntax** that control visuals, text, or sound.  
✅ Modify example code to see how it changes the output.  

---  

## 🔹 **Step 3: Create Your Executable Code-Poem**  

📖 **Follow this tutorial to learn how to create a JSoLang:**  
➡️ <a href="Estuary-WorkingWithJsoLangs.md" target="_blank">Estuary: Working with JSoLangs</a> 

Now, write a **short code-poem** that is both **readable as text** and **executable in Estuary**.  

✅ **Use at least three syntax elements** from your chosen tool.  
✅ **Experiment with poetic structure**—play with rhythm, repetition, or glitch aesthetics.  
✅ **Test & refine**—observe how syntax manipulation shapes meaning.  

💾 **Save your work** in a separate file for future use in Estuary.  

---  

### **🚀 Final Thoughts**  
By engaging with **executable code-poetry**, you are blending **programming logic with poetic language**, transforming syntax into **an expressive medium**.  

How does this experience change your perception of **code, language, and creative writing?**  

---
