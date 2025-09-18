<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Henil V. – Offensive Security Researcher</title>
<style>
  body {
    background-color: #000;
    color: #00ff00;
    font-family: "Courier New", monospace;
    padding: 20px;
  }
  a { color: #39ff14; text-decoration: none; }
  a:hover { color: #0ff; }
  .terminal { white-space: pre-wrap; line-height: 1.2em; }
  .cursor { display:inline-block; background-color:#00ff00; width:10px; animation: blink 1s infinite; }
  @keyframes blink { 0%,50%,100% {opacity:1;} 25%,75%{opacity:0;} }
  button.collapsible {
    background-color:#111;
    color:#0f0;
    cursor:pointer;
    padding:10px;
    width:100%;
    border:none;
    text-align:left;
    outline:none;
    font-size:16px;
    margin-top:5px;
  }
  button.collapsible:hover { background-color:#222; }
  .content { display:none; padding:0 18px; background-color:#000; margin-bottom:10px; }
  .art { font-family: monospace; white-space: pre; line-height:1em; }
</style>
</head>
<body>



<div class="art">
⢀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀
</div>

<div id="terminal" class="terminal"></div><span class="cursor"></span>

<button class="collapsible">Education & Labs</button>
<div class="content">
During my Masters, I performed hands-on exploits in educational in-house VMs and open-sourced labs:  
<a href="https://seedsecuritylabs.org/Labs_20.04/" target="_blank">Seed Security Labs</a>  
Lab reports & exploits: <a href="https://github.com/Henilv/Computer_Security-attacks" target="_blank">Computer Security Reports</a>
</div>

<button class="collapsible">Adversarial ML & Privacy</button>
<div class="content">
Experimented with frameworks like CleverHans on datasets such as FMNIST.  
Explored privacy-preserving ML including Machine Unlearning & Differential Privacy:  
<a href="https://github.com/Henilv/MachineLearning_Privacy-Security" target="_blank">ML Privacy & Security nb</a>  
Enhanced IDS/IPS signatures & explored fairness:  
<a href="https://github.com/Henilv/Algorithmic_Fairness_in-decision-making/tree/main" target="_blank">Algorithmic Fairness</a>
</div>

<button class="collapsible">IoT & Edge Security</button>
<div class="content">
Formalized IoT attacks & security for edge sensors with MQTT protocols:  
<a href="https://github.com/Henilv/IoT-app_sec/tree/main" target="_blank">IoT Edge Sensors IDS</a>
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
<a href="https://www.linkedin.com/in/ħenil-v-974257347/" target="_blank">LinkedIn</a>  
<a href="https://medium.com/@hhv8051/owasp-web-vulnerability-sqli-its-prevention-using-ml-for-endpoint-security-4fdac0ec926d" target="_blank">OWASP SQLi Paper</a>  
<a href="https://medium.com/@hhv8051/privacy-security-of-m-l-vs-privacy-security-using-ml-96e57fbb7102" target="_blank">ML Privacy/Security</a>  
<a href="https://link.springer.com/chapter/10.1007/978-981-16-6285-0_24" target="_blank">OWASP Vuln Patch</a>
</div>

<div class="art">
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░
</div>

<script>
  // Typing effect
  const text = `I am a Security researcher focusing on full lifecycle, identifying & mitigating vulnerabilities in cloud infra, Web APIs & microservices.

Currently working on adversarial ML, IDS profiling, IoT attacks, and web/cloud security. 
From strategic perspective, leveraging knowledgebase for secure DLC, DFIR-rich playbooks, scoring metrics & governance-aligned procedures.
`;

  let i = 0;
  function typeWriter() {
    if (i < text.length) {
      document.getElementById("terminal").innerHTML += text.charAt(i);
      i++;
      setTimeout(typeWriter, 20);
    }
  }
  window.onload = function() {
    typeWriter();

    // Collapsible logic AFTER DOM is ready
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

</body>
</html>

