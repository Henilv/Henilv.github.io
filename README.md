<style>
  body {
    background-color: #000000;
    color: #00ff00;
    font-family: "Courier New", monospace;
    overflow-x: hidden;
  }

  a {
    color: #39ff14;
    text-decoration: none;
  }

  a:hover {
    color: #00ffff;
  }

  h1, h2, h3 {
    color: #00ff00;
    margin-bottom: 0.2em;
  }

  /* Typing animation */
  .typed-text {
    border-right: 2px solid #00ff00;
    white-space: pre-wrap;
    overflow-wrap: break-word;
    animation: blink 0.7s infinite;
  }

  @keyframes blink {
    0% { border-color: #00ff00; }
    50% { border-color: transparent; }
    100% { border-color: #00ff00; }
  }

  /* Collapsible sections */
  .collapsible {
    background-color: #111;
    color: #00ff00;
    cursor: pointer;
    padding: 10px;
    width: 100%;
    border: none;
    text-align: left;
    outline: none;
    font-size: 16px;
    font-family: "Courier New", monospace;
  }

  .active, .collapsible:hover {
    background-color: #222;
  }

  .content {
    padding: 0 18px;
    display: none;
    overflow: hidden;
    background-color: #000;
  }

  /* Neon emoji ASCII spacing */
  .art {
    font-family: monospace;
    white-space: pre;
    line-height: 1em;
  }
</style>

<h1>Henil V. – Offensive Security Researcher</h1>

<div class="art">
⢀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀
⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿
</div>

<div id="typing"></div>

<button class="collapsible">Education & Labs</button>
<div class="content">
During my Masters, I performed hands-on exploits in educational in-house VMs and open-sourced labs:  
[Seed Security Labs](https://seedsecuritylabs.org/Labs_20.04/)  
Lab reports & exploits: [Computer Security Reports](https://github.com/Henilv/Computer_Security-attacks)
</div>

<button class="collapsible">Adversarial ML & Privacy</button>
<div class="content">
Experimented with frameworks like CleverHans on datasets such as FMNIST.  
Explored privacy-preserving ML including Machine Unlearning & Differential Privacy:  
[ML Privacy & Security nb](https://github.com/Henilv/MachineLearning_Privacy-Security)  
Enhanced IDS/IPS signatures & explored fairness:  
[Algorithmic Fairness](https://github.com/Henilv/Algorithmic_Fairness_in-decision-making/tree/main)
</div>

<button class="collapsible">IoT & Edge Security</button>
<div class="content">
Formalized IoT attacks & security for edge sensors with MQTT protocols:  
[IoT Edge Sensors IDS](https://github.com/Henilv/IoT-app_sec/tree/main)
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
[LinkedIn](https://www.linkedin.com/in/ħenil-v-974257347/)  

[OWASP SQLi Research Paper](https://medium.com/@hhv8051/owasp-web-vulnerability-sqli-its-prevention-using-ml-for-endpoint-security-4fdac0ec926d)  
[ML Privacy/Security](https://medium.com/@hhv8051/privacy-security-of-m-l-vs-privacy-security-using-ml-96e57fbb7102)  
[OWASP Vuln Patch](https://link.springer.com/chapter/10.1007/978-981-16-6285-0_24)  
[CVE Submissions]()
</div>

<div class="art">
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░
</div>

<script>
  const text = `
I am a Security researcher focusing on full lifecycle, identifying & mitigating vulnerabilities in cloud infra, Web APIs & microservices.

Currently working on adversarial ML, IDS profiling, IoT attacks, and web/cloud security. 
From strategic perspective, leveraging knowledgebase for secure DLC, DFIR-rich playbooks, scoring metrics & governance-aligned procedures.
  `;
  
  let i = 0;
  function typeWriter() {
    if (i < text.length) {
      document.getElementById("typing").innerHTML += text.charAt(i);
      i++;
      setTimeout(typeWriter, 20); // fast typing effect
    }
  }
  
  window.onload = typeWriter;

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
</script>
