---
title: Perqless - About Me
layout: default
---

# About Me

**Timezone:** AEST
**My Current Time:** <span id="currentTime"></span>

<script>
  function updateDateTime() {
    const now = new Date();
    const dateTimeString = now.getFullYear() + '-' + 
      String(now.getMonth() + 1).padStart(2, '0') + '-' + 
      String(now.getDate()).padStart(2, '0') + ' ' + 
      String(now.getHours()).padStart(2, '0') + ':' + 
      String(now.getMinutes()).padStart(2, '0') + ':' + 
      String(now.getSeconds()).padStart(2, '0');
    document.getElementById("currentTime").innerText = dateTimeString;
  }
  updateDateTime();
  setInterval(updateDateTime, 1000);
</script>

<p id="timeDiff"></p>
<script>
  const myOffset = 10; 
  const visitorOffset = new Date().getTimezoneOffset() / -60;
  const diff = visitorOffset - myOffset;
  document.getElementById("timeDiff").innerText = 
    diff === 0 ? "We are in the same timezone!" : 
    `You are ${Math.abs(diff)} hour(s) ${diff > 0 ? "ahead" : "behind"} me.`;
</script>

---

## My Skills
I work with the following tools and languages:

* Adobe Photoshop
* Adobe Premiere Pro
* Java
* Minecraft Mods & Plugins
* Kotlin
* Python
* Assembly
* Windows
* Ubuntu
* HTML & CSS

## Contact Me
**Discord Username:** `perqless`

## Socials
* **X (Twitter):** [x.com](https://x.com/perqIess)
* **GitHub:** [github.com](https://github.com/Perqless)
