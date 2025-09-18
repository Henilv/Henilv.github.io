<!-- Cyberpunk Terminal Split-Screen README -->

<div style="display:flex; height:90vh; font-family:'Courier New', monospace;">

  <!-- Terminal Panel -->
  <div id="terminal-panel" style="background-color:black; color:#00ff00; width:60%; padding:20px; overflow-y:auto; position:relative;">
    <div id="boot-dialog" style="white-space:pre; line-height:1.2em;"></div>
    <div id="typing-text"></div><span id="cursor" style="display:inline-block; background-color:#00ff00; width:10px; animation: blink 1s infinite;"></span>
  </div>

  <!-- Info Panel -->
  <div style="background-color:black; color:#00ff00; width:40%; padding:20px; border-left:2px solid #00ff00; overflow-y:auto;">
    <div style="border:1px solid #00ff00; padding:10px;">
      <h3>Quick Load Info</h3>
      <p>Henil V. – Offensive Security Researcher</p>
      <ul>
        <li>Cloud & Web API Security</li>
        <li>Adversarial ML & Privacy</li>
        <li>IoT & Edge Device Security</li>
        <li>Digital Forensics & Incident Response</li>
      </ul>
      <p>Links:</p>
      <ul>
        <li><a href="https://github.com/Henilv/Computer_Security-attacks" target="_blank" style="color:#39ff14;">Lab Reports & Exploits</a></li>
        <li><a href="https://github.com/Henilv/MachineLearning_Privacy-Security" target="_blank" style="color:#39ff14;">ML Privacy & Security</a></li>
        <li><a href="https://github.com/Henilv/IoT-app_sec/tree/main" target="_blank" style="color:#39ff14;">IoT Edge Sensors IDS</a></li>
      </ul>
    </div>
  </div>

</div>

<style>
@keyframes blink { 0%,50%,100% {opacity:1;} 25%,75%{opacity:0;} }
button.collapsible {
  background-color:#111; color:#0f0; cursor:pointer;
  padding:10px; width:100%; border:none; text-align:left;
  outline:none; font-size:16px; margin-top:5px;
}
button.collapsible:hover { background-color:#222; }
button.active { background-color:#222; } /* visually show open */
div.content { display:block; padding:0 18px; background-color:#000; margin-bottom:10px; color:#00ff00; } /* green text */
</style>

<!-- Collapsible Sections (Expanded by Default) -->
<button class="collapsible active">Education & Labs</button>
<div class="content">
During my Masters, I performed hands-on exploits in educational in-house VMs and open-sourced labs:  
<a href="https://seedsecuritylabs.org/Labs_20.04/" target="_blank" style="color:#39ff14;">Seed Security Labs</a>  
Lab reports & exploits: <a href="https://github.com/Henilv/Computer_Security-attacks" target="_blank" style="color:#39ff14;">Computer Security Reports</a>
</div>

<button class="collapsible active">Adversarial ML & Privacy</button>
<div class="content">
Experimented with frameworks like CleverHans on datasets such as FMNIST.  
Explored privacy-preserving ML including Machine Unlearning & Differential Privacy:  
<a href="https://github.com/Henilv/MachineLearning_Privacy-Security" target="_blank" style="color:#39ff14;">ML Privacy & Security nb</a>  
Enhanced IDS/IPS signatures & explored fairness:  
<a href="https://github.com/Henilv/Algorithmic_Fairness_in-decision-making/tree/main" target="_blank" style="color:#39ff14;">Algorithmic Fairness</a>
</div>

<button class="collapsible active">IoT & Edge Security</button>
<div class="content">
Formalized IoT attacks & security for edge sensors with MQTT protocols:  
<a href="https://github.com/Henilv/IoT-app_sec/tree/main" target="_blank" style="color:#39ff14;">IoT Edge Sensors IDS</a>
</div>

<button class="collapsible active">Web & Cloud Security</button>
<div class="content">
Performed black-box offensive security testing on vehicle & fleet microservices, MQTT brokers, OTA servers, and cloud infra.  
Threat modeling under ISO/SAE 21434 & R155/156. Automated security tests to enforce guardrails.
</div>

<button class="collapsible active">Current Research</button>
<div class="content">
Pursuing PhD-level security research on system hardening & layered security approach.  
Building Digital Forensics & Incident Rich playbooks with strategic & operational security governance.
</div>

<button class="collapsible active">Connect & Blogs</button>
<div class="content">
<a href="https://www.linkedin.com/in/ħenil-v-974257347/" target="_blank" style="color:#39ff14;">LinkedIn</a>  
<a href="https://medium.com/@hhv8051/owasp-web-vulnerability-sqli-its-prevention-using-ml-for-endpoint-security-4fdac0ec926d" target="_blank" style="color:#39ff14;">OWASP SQLi Paper</a>  
<a href="https://medium.com/@hhv8051/privacy-security-of-m-l-vs-privacy-security-using-ml-96e57fbb7102" target="_blank" style="color:#39ff14;">ML Privacy/Security</a>  
<a href="https://link.springer.com/chapter/10.1007/978-981-16-6285-0_24" target="_blank" style="color:#39ff14;">OWASP Vuln Patch</a>
</div>

<script>
const bootText = `Booting cyber terminal...\nLoading modules: ████████ 100%\nInitializing environment...\nReady.\n\n`;
const introText = `I am a Security researcher focusing on full lifecycle, identifying & mitigating vulnerabilities in cloud infra, Web APIs & microservices.

Currently working on adversarial ML, IDS profiling, IoT attacks, and web/cloud security. 
From strategic perspective, leveraging knowledgebase for secure DLC, DFIR-rich playbooks, scoring metrics & governance-aligned procedures.
`;

function runTerminal() {
  const bootEl = document.getElementById('boot-dialog');
  const typingEl = document.getElementById('typing-text');
  bootEl.innerHTML = '';
  typingEl.innerHTML = '';
  let i=0;
  function typeBoot() {
    if(i<bootText.length){
      bootEl.innerHTML += bootText.charAt(i);
      i++;
      setTimeout(typeBoot,10);
    } else {
      typeIntro(0);
    }
  }
  function typeIntro(j){
    if(j<introText.length){
      typingEl.innerHTML += introText.charAt(j);
      j++;
      setTimeout(()=>typeIntro(j),20);
    }
  }
  typeBoot();
}

window.onload = runTerminal;

// Collapsibles toggle still works
const collapsibles = document.getElementsByClassName("collapsible");
for(let k=0;k<collapsibles.length;k++){
  collapsibles[k].addEventListener("click",function(){
    this.classList.toggle("active");
    const content=this.nextElementSibling;
    content.style.display=(content.style.display==="block")?"none":"block";
  });
}
</script>
