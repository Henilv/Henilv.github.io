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

div.full-section {
  background-color:black; 
  color:#00ff00; 
  padding:20px; 
  border:2px solid #00ff00; 
  margin-top:20px; 
  white-space:pre-line; 
  line-height:1.2em;
  font-family:'Courier New', monospace;
}
a { color:#39ff14; text-decoration:none; }
a:hover { color:#00ffff; }
</style>

<!-- Full Black Box for All Sections -->
<div class="full-section">
<strong>Education & Labs:</strong>  
During my Masters, I performed hands-on exploits in educational in-house VMs and open-sourced labs:  
<a href="https://seedsecuritylabs.org/Labs_20.04/" target="_blank">Seed Security Labs</a>  
Lab reports & exploits: <a href="https://github.com/Henilv/Computer_Security-attacks" target="_blank">Computer Security Reports</a>

<strong>Adversarial ML & Privacy:</strong>  
Experimented with frameworks like CleverHans on datasets such as FMNIST.  
Explored privacy-preserving ML including Machine Unlearning & Differential Privacy:  
<a href="https://github.com/Henilv/MachineLearning_Privacy-Security" target="_blank">ML Privacy & Security nb</a>  
Enhanced IDS/IPS signatures & explored fairness:  
<a href="https://github.com/Henilv/Algorithmic_Fairness_in-decision-making/tree/main" target="_blank">Algorithmic Fairness</a>

<strong>IoT & Edge Security:</strong>  
Formalized IoT attacks & security for edge sensors with MQTT protocols:  
<a href="https://github.com/Henilv/IoT-app_sec/tree/main" target="_blank">IoT Edge Sensors IDS</a>

<strong>Web & Cloud Security:</strong>  
Performed black-box offensive security testing on vehicle & fleet microservices, MQTT brokers, OTA servers, and cloud infra.  
Threat modeling under ISO/SAE 21434 & R155/156. Automated security tests to enforce guardrails.

<strong>Current Research:</strong>  
Pursuing PhD-level security research on system hardening & layered security approach.  
Building Digital Forensics & Incident Rich playbooks with strategic & operational security governance.

<strong>Connect & Blogs:</strong>  
<a href="https://www.linkedin.com/in/ħenil-v-974257347/" target="_blank">LinkedIn</a>  
<a href="https://medium.com/@hhv8051/owasp-web-vulnerability-sqli-its-prevention-using-ml-for-endpoint-security-4fdac0ec926d" target="_blank">OWASP SQLi Paper</a>  
<a href="https://medium.com/@hhv8051/privacy-security-of-m-l-vs-privacy-security-using-ml-96e57fbb7102" target="_blank">ML Privacy/Security</a>  
<a href="https://link.springer.com/chapter/10.1007/978-981-16-6285-0_24" target="_blank">OWASP Vuln Patch</a>
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
</script>

