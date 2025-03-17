
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

## Codework: Executable Code-Poetry

**John Cayley**’s categories also include **functional codeworks** that merge executable commands with creative writing—both **human-readable** and **computer-executable**.

**Cayley, J. (2006).** *Time code language: New media poetics and programmed signification.*  
In **New Media Poetics: Contexts, Technotexts, and Theories**, pp. 307-334.

--

The **code poetry** (Fig.1) of Mexican-Canadian media artist *<a href="https://vimeo.com/jessicaarianne" target="_blank">Jessica A. Rodriguez</a>*, particularly her project *<a href="https://jac307.github.io/MEMORIAS/" target="_blank">MEMORIAS</a>* exemplifies **executable code-poetry**. Her work hybridizes live coding practices with Electronic Literature.

<iframe src="https://player.vimeo.com/video/565310015" width="90%" frameborder="0" allowfullscreen></iframe>

**MEMORIAS** is a Web-based artistic project with **six executable codeworks** that combines natural (Spanish, English, and Spanglish) with computing languages to produce a/v textures.


---
