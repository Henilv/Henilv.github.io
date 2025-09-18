<!-- Hacker Terminal Cyberpunk README -->

<div style="background-color:black; color:#00ff00; font-family:'Courier New', monospace; padding:20px;">

<div style="white-space:pre; font-family:monospace; line-height:1em;">
⢀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀
⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿
</div>

<div id="typing-text"></div><span id="cursor" style="display:inline-block; background-color:#00ff00; width:10px; animation: blink 1s infinite;"></span>

<style>
@keyframes blink { 0%,50%,100% {opacity:1;} 25%,75%{opacity:0;} }
button.collapsible {
  background-color:#111; color:#0f0; cursor:pointer;
  padding:10px; width:100%; border:none; text-align:left;
  outline:none; font-size:16px; margin-top:5px;
}
button.collapsible:hover { background-color:#222; }
div.content { display:none; padding:0 18px; background-color:#000; margin-bottom:10px; }
</style>

<button class="collapsible">Education & Labs</button>
<div class="content">
During my Masters, I performed hands-on exploits in educational in-house VMs and open-sourced labs:  
<a href="https://seedsecuritylabs.org/Labs_20.04/" target="_blank" style="color:#39ff14;">Seed Security Labs</a>  
Lab reports & exploits: <a href="https://github.com/Henilv/Computer_Security-attacks" target="_blank" style="color:#39ff14;">Computer Security Reports</a>
</div>

<button class="collapsible">Adversarial ML & Privacy</button>
<div class="content">
Experimented with frameworks like CleverHans on datasets such as FMNIST.  
Explored privacy-preserving ML including Machine Unlearning & Differential Privacy:  
<a href="https://github.com/Henilv/MachineLearning_Privacy-Security" target="_blank" style="color:#39ff14;">ML Privacy & Security nb</a>  
Enhanced IDS/IPS signatures & explored fairness:  
<a href="https://github.com/Henilv/Algorithmic_Fairness_in-decision-making/tree/main" target="_blank" style="color:#39ff14;">Algorithmic Fairness</a>
</div>

<button class="collapsible">IoT & Edge Security</button>
<div class="content">
Formalized IoT attacks & security for edge sensors with MQTT protocols:  
<a href="https://github.com/Henilv/IoT-app_sec/tree/main" target="_blank" style="color:#39ff14;">IoT Edge Sensors IDS</a>
</div>

<button class="collapsible">Web & Cloud Security</button>
<div class="content">
Performed black-box offensive security testing on vehicle & fleet microservices, MQTT brokers, OTA servers, and cloud infra.  
Threat modeling under ISO/SAE 21434 & R155/156. Automated security tests to enforce guardrails.
</div>

<button class="collapsible">Current Research</button>
<div class="content">
Pursuing PhD-level security research on system hardening & layered security approach.  
Building Digital Forensics & Incident Rich playbooks with strategic & operational security governance.
</div>

<button class="collapsible">Professional Memberships</button>
<div class="content">
Member of ISC2, ISACA – former Detroit & Mumbai Chapters, currently Silicon Valley Chapter.
</div>

<button class="collapsible">Connect & Blogs</button>
<div class="content">
<a href="https://www.linkedin.com/in/ħenil-v-974257347/" target="_blank" style="color:#39ff14;">LinkedIn</a>  
<a href="https://medium.com/@hhv8051/owasp-web-vulnerability-sqli-its-prevention-using-ml-for-endpoint-security-4fdac0ec926d" target="_blank" style="color:#39ff14;">OWASP SQLi Paper</a>  
<a href="https://medium.com/@hhv8051/privacy-security-of-m-l-vs-privacy-security-using-ml-96e57fbb7102" target="_blank" style="color:#39ff14;">ML Privacy/Security</a>  
<a href="https://link.springer.com/chapter/10.1007/978-981-16-6285-0_24" target="_blank" style="color:#39ff14;">OWASP Vuln Patch</a>
</div>

<div style="white-space:pre; font-family:monospace; line-height:1em;">
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░
</div>

<script>
const text = `I am a Security researcher focusing on full lifecycle, identifying & mitigating vulnerabilities in cloud infra, Web APIs & microservices.

Currently working on adversarial ML, IDS profiling, IoT attacks, and web/cloud security. 
From strategic perspective, leveraging knowledgebase for secure DLC, DFIR-rich playbooks, scoring metrics & governance-aligned procedures.
`;

let i = 0;
function typeWriter() {
  if (i < text.length) {
    document.getElementById("typing-text").innerHTML += text.charAt(i);
    i++;
    setTimeout(typeWriter, 20);
  }
}

window.onload = function() {
  typeWriter();
  
  const collapsibles = document.getElementsByClassName("collapsible");
  for (let j = 0; j < collapsibles.length; j++) {
    collapsibles[j].addEventListener("click", function() {
      this.classList.toggle("active");
      const content = this.nextElementSibling;
      if (content.style.display === "block") {
        content.style.display = "none";
      } else {
        content.style.display = "block";
      }
    });
  }
};
</script>

</div>
