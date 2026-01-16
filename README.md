# The Free Self-Directed AI Security Mastery Path

## Zero-Cost Route to Elite AI Security Expertise

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Last Updated](https://img.shields.io/badge/Last%20Updated-January%202026-blue.svg)]()

> **Platform:** Optimized for Kubuntu/Ubuntu 24.04 LTS with Python virtual environments

---

## Why This Exists

The AI security training market charges $5,000-$15,000 for courses teaching skills you can learn for free. This repository is a complete, structured learning path built from publicly available resources, open-source tools, and hands-on labs.

**This path is designed for:**
- Security professionals expanding into AI/ML security
- Penetration testers wanting to add LLM red teaming skills
- Blue teamers building AI defense capabilities
- Anyone with security fundamentals ready to specialize

**What you'll learn:**
- Prompt injection, jailbreaking, and LLM exploitation
- Adversarial machine learning attacks and defenses
- RAG poisoning and agent security
- Deepfake detection and synthetic media forensics
- AI security governance and compliance frameworks

**Time commitment:** 2-3 hours daily for 36 weeks (or accelerate based on your background)

---

## Table of Contents

- [Environment Setup](#environment-setup)
- [Phase 1: Foundation (Weeks 1-4)](#phase-1-foundation-weeks-1-4)
- [Phase 2: Offensive LLM Security (Weeks 5-12)](#phase-2-offensive-llm-security-weeks-5-12)
- [Phase 3: Classical Adversarial ML (Weeks 13-16)](#phase-3-classical-adversarial-ml-weeks-13-16)
- [Phase 4: Building Your Security Lab (Weeks 17-20)](#phase-4-building-your-security-lab-weeks-17-20)
- [Phase 5: Deepfakes and Synthetic Media (Weeks 21-22)](#phase-5-deepfakes-and-synthetic-media-weeks-21-22)
- [Phase 6: Purple Team Integration (Weeks 23-26)](#phase-6-purple-team-integration-weeks-23-26)
- [Phase 7: Real-World Practice (Weeks 27-30)](#phase-7-real-world-practice-weeks-27-30)
- [Phase 8: Advanced Specialization (Weeks 31-36)](#phase-8-advanced-specialization-weeks-31-36)
- [Essential Resources](#essential-resources)
- [Progress Tracking](#progress-tracking)
- [Contributing](#contributing)

---

## Environment Setup

### 🚀 Quick Start (Kubuntu/Ubuntu 24.04)

Ubuntu 24.04+ enforces PEP 668 to protect system Python. We use virtual environments (the professional approach).

#### Option 1: Automated Setup (Recommended)
```bash
# Clone this repository
git clone https://github.com/WaypointCA/ai-security-lab.git
cd ai-security-lab

# Run the complete setup script
bash scripts/setup_ai_security_lab.sh
```

#### Option 2: Quick Manual Setup
```bash
# Install Python venv support
sudo apt install python3-full python3-venv python3-pip

# Create and activate virtual environment
cd ~/ai-security-lab
python3 -m venv venv
source venv/bin/activate

# Install packages
pip install --upgrade pip
pip install -r requirements.txt
```

#### Option 3: Minimal 2-Minute Start
```bash
bash scripts/quick_start.sh
```

### 📁 Repository Structure
```
ai-security-lab/
├── README.md                      # This file
├── LICENSE                        # MIT License
├── CONTRIBUTING.md                # Contribution guidelines
├── requirements.txt               # Full Python dependencies
├── requirements-minimal.txt       # Minimal dependencies to start
├── scripts/
│   ├── setup_ai_security_lab.sh  # Complete setup automation
│   ├── quick_start.sh            # 2-minute quick start
│   ├── activate.sh               # Daily environment activation
│   └── test_setup.py             # Verify installation
├── phases/
│   ├── phase1-foundation/
│   ├── phase2-llm-security/
│   ├── phase3-adversarial-ml/
│   ├── phase4-lab-setup/
│   ├── phase5-deepfakes/
│   ├── phase6-purple-team/
│   ├── phase7-real-world/
│   └── phase8-advanced/
├── tools/                         # Cloned security tools
├── labs/                          # Lab exercises by week
├── projects/                      # Your security projects
└── venv/                          # Python virtual environment (auto-created)
```

### 🔧 Daily Workflow

#### Start Your Day
```bash
# Using the alias (if you set it up)
ai-lab

# Or manually
cd ~/ai-security-lab
source venv/bin/activate
```

#### Verify Environment
```bash
python scripts/test_setup.py
```

#### Update Tools
```bash
pip install --upgrade -r requirements.txt
```

### 💡 Pro Setup Tips

#### Add Convenient Alias
```bash
echo "alias ai-lab='cd ~/ai-security-lab && source venv/bin/activate'" >> ~/.bashrc
source ~/.bashrc
# Now just type: ai-lab
```

#### VS Code Integration
1. Open folder in VS Code: `code ~/ai-security-lab`
2. `Ctrl+Shift+P` → "Python: Select Interpreter"
3. Choose `./venv/bin/python`
4. VS Code auto-activates venv in terminals

#### Jupyter Setup
```bash
# After activating venv
pip install jupyter ipykernel
python -m ipykernel install --user --name=ai-security
# Now select "ai-security" kernel in Jupyter
```

---

## Phase 1: Foundation (Weeks 1-4)

### Learn Just Enough ML to Break It

### Week 1-2: ML Fundamentals for Attackers

**Free Learning Resources:**
- [ ] **Fast.ai Course (Part 1)**: [https://course.fast.ai](https://course.fast.ai) - Just lessons 1-3 for basics
- [ ] **Andrew Ng's ML Course**: [Coursera ML Course](https://www.coursera.org/learn/machine-learning) (audit free) - Only weeks 1-3 needed
- [ ] **3Blue1Brown Neural Network Series**: [YouTube Playlist](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi)
- [ ] **Google's Machine Learning Crash Course**: [https://developers.google.com/machine-learning/crash-course](https://developers.google.com/machine-learning/crash-course)

**Hands-On Labs (Free):**
- [ ] **Google Colab**: [https://colab.research.google.com](https://colab.research.google.com) (free GPU/TPU access)
- [ ] **Kaggle Notebooks**: [https://www.kaggle.com/code](https://www.kaggle.com/code) (free compute)
- [ ] **Local Jupyter**: Run `jupyter lab` in your activated venv

**Required Reading:**
- [ ] [Adversarial Examples: Attacks and Defenses for Deep Learning](https://arxiv.org/abs/1712.07107)
- [ ] [The Limitations of Deep Learning in Adversarial Settings](https://arxiv.org/abs/1511.07528)
- [ ] [NIST AI 100-2e2025 - Adversarial Machine Learning](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-2e2025.pdf)

**Week 1 Lab Exercises:**
```bash
# In your activated environment
cd ~/ai-security-lab/labs/week01
jupyter lab week01_ml_basics.ipynb
```
- [ ] Train a basic image classifier on CIFAR-10
- [ ] Generate your first adversarial example using FGSM
- [ ] Document the attack in a blog post

### Week 3-4: AI Security Frameworks

**Study Materials (All Free):**
- [ ] **MITRE ATLAS**: [https://atlas.mitre.org](https://atlas.mitre.org) - Complete framework study
- [ ] **OWASP Top 10 for LLM Applications**: [https://owasp.org/www-project-top-10-for-large-language-model-applications/](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [ ] **NIST AI RMF**: [https://www.nist.gov/itl/ai-risk-management-framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [ ] **AI Incident Database**: [https://incidentdatabase.ai](https://incidentdatabase.ai) - Study real breaches

**YouTube Channels to Follow:**
- [ ] [Two Minute Papers](https://www.youtube.com/c/TwoMinutePapers)
- [ ] [Yannic Kilcher](https://www.youtube.com/c/YannicKilcher)
- [ ] [DEF CON Conference](https://www.youtube.com/user/DEFCONConference)
- [ ] [Black Hat](https://www.youtube.com/c/BlackHatOfficialYT)

**Practical Exercises:**
- [ ] Map 5 recent AI breaches to MITRE ATLAS tactics
- [ ] Create your own threat model for a hypothetical AI system
- [ ] Join the OWASP Slack (#project-top10-for-llm channel)

---

## Phase 2: Offensive LLM Security (Weeks 5-12)

### Master Prompt Injection and Jailbreaking

### Week 5-6: Prompt Injection Mastery

**Free Resources:**
- [ ] **Simon Willison's Blog Series**: [https://simonwillison.net/series/prompt-injection/](https://simonwillison.net/series/prompt-injection/)
- [ ] **Prompt Injection Handbook**: [https://github.com/utkusen/prompt-injection-handbook](https://github.com/utkusen/prompt-injection-handbook)
- [ ] **LangChain Security Documentation**: [https://python.langchain.com/docs/security](https://python.langchain.com/docs/security)
- [ ] **PortSwigger Web Security Academy**: [https://portswigger.net/web-security/llm-attacks](https://portswigger.net/web-security/llm-attacks)
- [ ] **Lakera Blog on Prompt Injection**: [https://www.lakera.ai/blog/guide-to-prompt-injection](https://www.lakera.ai/blog/guide-to-prompt-injection)

**Install and Master These Tools:**
```bash
# In your activated venv
pip install garak promptfoo
git clone https://github.com/Azure/PyRIT.git tools/PyRIT
cd tools/PyRIT && pip install -e .
```

**Tools Documentation:**
- [ ] **Garak** (NVIDIA): [https://github.com/NVIDIA/garak](https://github.com/NVIDIA/garak)
- [ ] **Promptfoo**: [https://github.com/promptfoo/promptfoo](https://github.com/promptfoo/promptfoo)
- [ ] **PyRIT** (Microsoft): [https://github.com/Azure/PyRIT](https://github.com/Azure/PyRIT)

**Practice Targets (All Free):**
- [ ] **Gandalf CTF**: [https://gandalf.lakera.ai](https://gandalf.lakera.ai) (levels 1-8)
- [ ] **HackAPrompt**: [https://www.aicrowd.com/challenges/hackaprompt-2023](https://www.aicrowd.com/challenges/hackaprompt-2023)
- [ ] **AI Village CTF Challenges**: [https://github.com/aivillage](https://github.com/aivillage)
- [ ] **Local Ollama models**: [https://ollama.ai](https://ollama.ai)

**Week 5-6 Lab Setup:**
```bash
# Install Ollama for local testing
curl -fsSL https://ollama.com/install.sh | sh
ollama pull llama2
ollama pull mistral

# Test with garak
garak --model_type ollama --model_name llama2
```

### Week 7-8: Advanced Jailbreaking

**Research Papers (Free on arXiv):**
- [ ] [Universal and Transferable Adversarial Attacks on Aligned Language Models](https://arxiv.org/abs/2307.15043)
- [ ] [Jailbroken: How Does LLM Safety Training Fail?](https://arxiv.org/abs/2307.02483)
- [ ] [Tree of Attacks: Jailbreaking Black-Box LLMs Automatically](https://arxiv.org/abs/2312.02119)
- [ ] [Red Teaming the Mind of the Machine](https://arxiv.org/html/2505.04806v1)

**Free Labs:**
```bash
cd ~/ai-security-lab/labs/week07
python jailbreak_automation.py
```
1. [ ] Set up Ollama with multiple models
2. [ ] Test jailbreaks across models for transferability
3. [ ] Build automated jailbreak generator using PyRIT
4. [ ] Document 10 working jailbreaks with success rates

### Week 9-10: Model Extraction and Privacy Attacks

**Learning Resources:**
- [ ] [Extracting Training Data from Large Language Models](https://arxiv.org/abs/2012.07805)
- [ ] [Model Extraction of BERT-based APIs](https://arxiv.org/abs/1910.05887)
- [ ] **Nicholas Carlini's Blog**: [https://nicholas.carlini.com](https://nicholas.carlini.com)
- [ ] [I Know What You Trained Last Summer - Model Extraction Survey](https://dl.acm.org/doi/10.1145/3595292)

**Free API Practice:**
- [ ] OpenAI API free tier: [https://platform.openai.com/signup](https://platform.openai.com/signup)
- [ ] Anthropic Claude API: [https://www.anthropic.com/api](https://www.anthropic.com/api)
- [ ] Google AI Studio: [https://aistudio.google.com](https://aistudio.google.com)

### Week 11-12: RAG and Agent Security

**Build Your Lab:**
```bash
# In activated venv
cd ~/ai-security-lab

# Pull models for RAG testing
ollama pull llama2
ollama pull mistral
ollama pull mixtral

# Install AnythingLLM
docker pull mintplexlabs/anythingllm
docker run -d -p 3001:3001 --name anythingllm mintplexlabs/anythingllm
```

**Free Learning Path:**
- [ ] **LangChain Security Docs**: [https://python.langchain.com/docs/security](https://python.langchain.com/docs/security)
- [ ] **LlamaIndex Security**: [https://docs.llamaindex.ai/en/stable/module_guides/security/](https://docs.llamaindex.ai/en/stable/module_guides/security/)
- [ ] **OWASP LLM AI Security Cheat Sheet**: [https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/LLM_AI_Security_Cheat_Sheet.md](https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/LLM_AI_Security_Cheat_Sheet.md)

**Projects to Build:**
- [ ] Poison a RAG system's knowledge base
- [ ] Exploit agent tool-calling with malicious prompts
- [ ] Chain attacks across multiple agents
- [ ] Write detailed attack methodology

---

## Phase 3: Classical Adversarial ML (Weeks 13-16)

### Beyond LLMs - Computer Vision and Traditional ML

### Week 13-14: Adversarial Examples

**Install Frameworks in venv:**
```bash
pip install adversarial-robustness-toolbox foolbox cleverhans textattack
```

**Free Frameworks:**
- [ ] **ART (IBM)**: [https://github.com/Trusted-AI/adversarial-robustness-toolbox](https://github.com/Trusted-AI/adversarial-robustness-toolbox)
- [ ] **Foolbox**: [https://github.com/bethgelab/foolbox](https://github.com/bethgelab/foolbox)
- [ ] **CleverHans**: [https://github.com/cleverhans-lab/cleverhans](https://github.com/cleverhans-lab/cleverhans)
- [ ] **TextAttack**: [https://github.com/QData/TextAttack](https://github.com/QData/TextAttack)

**Learning Resources:**
- [ ] [Adversarial ML Tutorial (Ian Goodfellow)](https://www.youtube.com/watch?v=CIfsB_EYsVI)
- [ ] [Explaining and Harnessing Adversarial Examples](https://arxiv.org/abs/1412.6572)
- [ ] **Awesome ML for Cybersecurity**: [https://github.com/jivoi/awesome-ml-for-cybersecurity](https://github.com/jivoi/awesome-ml-for-cybersecurity)

**Build These Attacks:**
```python
# Week 13 lab template
from art.attacks.evasion import FastGradientMethod
from art.estimators.classification import PyTorchClassifier
# Your code here
```
- [ ] FGSM, PGD, C&W against ImageNet models
- [ ] Physical adversarial patches (printable)
- [ ] Black-box attacks with limited queries
- [ ] Transfer attacks between models

### Week 15-16: Data Poisoning

**Critical Research (Free):**
- [ ] [Poisoning Language Models During Instruction Tuning](https://arxiv.org/abs/2305.00944)
- [ ] [Backdoor Attacks on Deep Learning Models](https://arxiv.org/abs/2007.08745)
- [ ] [Sleeper Agents (Anthropic)](https://arxiv.org/abs/2401.05566)
- [ ] [Model Namespace Reuse Attack](https://unit42.paloaltonetworks.com/model-namespace-reuse/)

**Hands-On Experiments:**
- [ ] Poison MNIST classifier with 1% bad data
- [ ] Implement backdoor trigger in neural network
- [ ] Clean-label poisoning attack
- [ ] Test defenses and bypass them

---

## Phase 4: Building Your Security Lab (Weeks 17-20)

### Professional Testing Environment at Zero Cost

### Week 17-18: Local AI Security Lab

**Complete Lab Stack Setup:**
```bash
# After environment activation
cd ~/ai-security-lab

# Install full requirements
pip install -r requirements-full.txt
```

**Vulnerable Apps to Deploy:**
```bash
cd ~/ai-security-lab/tools
git clone https://github.com/dhammon/ai-goat.git
git clone https://github.com/DamnVulnerableLLM/DamnVulnerableLLM.git
git clone https://github.com/orcasecurity-research/AIGoat.git
git clone https://github.com/AImaginationLab/vulnerable-llms.git
```

**Vulnerable App Links:**
- [ ] **AI-Goat**: [https://github.com/dhammon/ai-goat](https://github.com/dhammon/ai-goat)
- [ ] **Damn Vulnerable LLM**: [https://github.com/DamnVulnerableLLM/DamnVulnerableLLM](https://github.com/DamnVulnerableLLM/DamnVulnerableLLM)
- [ ] **AIGoat (Orca)**: [https://github.com/orcasecurity-research/AIGoat](https://github.com/orcasecurity-research/AIGoat)
- [ ] **Vulnerable LLMs**: [https://github.com/AImaginationLab/vulnerable-llms](https://github.com/AImaginationLab/vulnerable-llms)

### Week 19-20: Automation and Tooling

**Build Your Own Tools:**
```python
# Template structure
cd ~/ai-security-lab/projects
mkdir prompt-injection-scanner
cd prompt-injection-scanner
touch scanner.py requirements.txt README.md
```

- [ ] Prompt injection scanner (Python + Garak)
- [ ] Automated jailbreak tester
- [ ] Model extraction framework
- [ ] RAG poisoning toolkit

**Free Infrastructure:**
- [ ] **GitHub Actions**: [https://github.com/features/actions](https://github.com/features/actions) (2000 minutes/month free)
- [ ] **Cloudflare Workers**: [https://workers.cloudflare.com](https://workers.cloudflare.com) (100k requests/day free)
- [ ] **Fly.io**: [https://fly.io](https://fly.io) (free tier for hosting)
- [ ] **ngrok**: [https://ngrok.com](https://ngrok.com) (exposing local services)
- [ ] **GitHub Codespaces**: [https://github.com/features/codespaces](https://github.com/features/codespaces) (120 hrs/month)

---

## Phase 5: Deepfakes and Synthetic Media (Weeks 21-22)

### Understanding the $25M Threat Vector

### Week 21: Generation Techniques

**Free Tools:**
- [ ] **Stable Diffusion WebUI**: [https://github.com/AUTOMATIC1111/stable-diffusion-webui](https://github.com/AUTOMATIC1111/stable-diffusion-webui)
- [ ] **RVC for Voice**: [https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI)
- [ ] **DeepFaceLab**: [https://github.com/iperov/DeepFaceLab](https://github.com/iperov/DeepFaceLab)
- [ ] **Wav2Lip**: [https://github.com/Rudrabha/Wav2Lip](https://github.com/Rudrabha/Wav2Lip)

**Detection Tools (Free):**
- [ ] **Deepware Scanner**: [https://scanner.deepware.ai](https://scanner.deepware.ai)
- [ ] **Sensity AI**: [https://sensity.ai/deepfakes-detection/](https://sensity.ai/deepfakes-detection/)
- [ ] **Intel FakeCatcher**: [https://www.intel.com/content/www/us/en/research/responsible-ai-fakecatcher.html](https://www.intel.com/content/www/us/en/research/responsible-ai-fakecatcher.html)

### Week 22: Defense and Detection

**Build These Projects:**
- [ ] Deepfake detection model using ResNet
- [ ] Audio deepfake classifier
- [ ] Metadata forensics toolkit
- [ ] Corporate defense playbook

---

## Phase 6: Purple Team Integration (Weeks 23-26)

### Bridging Offense and Defense

### Week 23-24: Blue Team Defenses

**Free Defensive Tools:**
- [ ] **NeMo Guardrails** (NVIDIA): [https://github.com/NVIDIA/NeMo-Guardrails](https://github.com/NVIDIA/NeMo-Guardrails)
- [ ] **Lakera Guard**: [https://www.lakera.ai/lakera-guard](https://www.lakera.ai/lakera-guard) (API with free tier)
- [ ] **LangKit**: [https://github.com/whylabs/langkit](https://github.com/whylabs/langkit)
- [ ] **Evidently AI**: [https://github.com/evidentlyai/evidently](https://github.com/evidentlyai/evidently)

**SIEM Integration (Free):**
- [ ] **Elastic Stack**: [https://www.elastic.co/elastic-stack](https://www.elastic.co/elastic-stack)
- [ ] **Grafana + Loki**: [https://grafana.com/oss/loki/](https://grafana.com/oss/loki/)
- [ ] **OpenSearch**: [https://opensearch.org](https://opensearch.org)

### Week 25-26: Compliance and Governance

**Free Compliance Resources:**
- [ ] [ISO/IEC 23053:2022](https://www.iso.org/standard/74438.html) (Framework for AI trustworthiness)
- [ ] [EU AI Act Full Text](https://artificialintelligenceact.eu/the-act/)
- [ ] [NIST AI RMF Playbook](https://airc.nist.gov/AI_RMF_Knowledge_Base/Playbook)
- [ ] [ISACA AI Governance](https://www.isaca.org/resources/artificial-intelligence) (free with registration)

**Build Compliance Artifacts:**
- [ ] AI Risk Register template
- [ ] Assessment questionnaires
- [ ] Governance framework document
- [ ] Vendor assessment checklist

---

## Phase 7: Real-World Practice (Weeks 27-30)

### Building Your Portfolio

### Week 27-28: Bug Bounties and CTFs

**Free Practice Platforms:**
- [ ] **HackerOne**: [https://www.hackerone.com/ai-security](https://www.hackerone.com/ai-security)
- [ ] **Bugcrowd**: [https://www.bugcrowd.com](https://www.bugcrowd.com)
- [ ] **Intigriti**: [https://www.intigriti.com](https://www.intigriti.com)
- [ ] **CTFtime.org**: [https://ctftime.org](https://ctftime.org)
- [ ] **PentesterLab**: [https://pentesterlab.com/exercises](https://pentesterlab.com/exercises) (some free exercises)

**Strategy for Success:**
1. [ ] Start with programs explicitly mentioning AI/LLM
2. [ ] Focus on prompt injection and data leakage initially
3. [ ] Document everything for portfolio
4. [ ] Aim for 5-10 valid submissions

### Week 29-30: Open Source Contributions

**High-Value Contribution Targets:**
- [ ] **OWASP Top 10 for LLMs**: [https://github.com/OWASP/www-project-top-10-for-large-language-model-applications](https://github.com/OWASP/www-project-top-10-for-large-language-model-applications)
- [ ] **MITRE ATLAS**: [https://github.com/mitre-atlas/atlas](https://github.com/mitre-atlas/atlas)
- [ ] **Garak**: [https://github.com/NVIDIA/garak](https://github.com/NVIDIA/garak)
- [ ] **PyRIT**: [https://github.com/Azure/PyRIT](https://github.com/Azure/PyRIT)
- [ ] **AI Village**: [https://github.com/aivillage](https://github.com/aivillage)

**Portfolio Projects:**
- [ ] Security assessment of popular open-source AI project
- [ ] White paper on emerging AI threat
- [ ] Tool release on GitHub
- [ ] Blog series (10+ technical posts)

---

## Phase 8: Advanced Specialization (Weeks 31-36)

### Becoming the Expert

### Week 31-32: Nation-State TTPs

**Intelligence Sources (Free):**
- [ ] [Microsoft Security Blog](https://www.microsoft.com/en-us/security/blog/)
- [ ] [Google Threat Analysis Group](https://blog.google/threat-analysis-group/)
- [ ] [OpenAI Security](https://openai.com/index/disrupting-malicious-uses-of-ai-by-state-affiliated-threat-actors/)
- [ ] [Mandiant Intelligence](https://www.mandiant.com/resources/blog)
- [ ] [CrowdStrike Intelligence](https://www.crowdstrike.com/blog/category/threat-intelligence/)

**Analysis Framework:**
- [ ] Track 5 APT groups using AI
- [ ] Map their TTPs to MITRE ATLAS
- [ ] Build detection strategies
- [ ] Publish threat brief

### Week 33-34: Cutting-Edge Research

**Stay Current With:**
- [ ] **arXiv AI Security**: [https://arxiv.org/list/cs.CR/recent](https://arxiv.org/list/cs.CR/recent) (check daily)
- [ ] **Papers With Code - Adversarial**: [https://paperswithcode.com/task/adversarial-attack](https://paperswithcode.com/task/adversarial-attack)
- [ ] **AI Safety Papers**: [https://www.alignmentforum.org](https://www.alignmentforum.org)
- [ ] **Conference Videos**: [Media.ccc.de](https://media.ccc.de), [InfoCon.org](https://infocon.org)

**Twitter/X Accounts to Follow:**
- [ ] Nicholas Carlini (@nicholas_carlini)
- [ ] Simon Willison (@simonw)
- [ ] Kai Greshake (@KGreshake)
- [ ] Rich Harang (@rharang)
- [ ] Will Pearce (@moo_hax)

### Week 35-36: Capstone Project Options

**Option 1: Security Tool Development**
- [ ] Build comprehensive AI security scanner
- [ ] 1000+ stars on GitHub as goal
- [ ] Full documentation and examples
- [ ] Conference talk submission

**Option 2: Major Vulnerability Research**
- [ ] Find significant vulnerability in popular AI system
- [ ] Responsible disclosure
- [ ] Detailed write-up
- [ ] Conference presentation

**Option 3: Defensive Framework**
- [ ] Complete security framework for specific industry
- [ ] Open-source release
- [ ] Implementation guides
- [ ] Community adoption

---

## Essential Resources

### Documentation and Frameworks
- **OWASP AI Security**: [https://owaspai.org](https://owaspai.org)
- **MITRE ATLAS Navigator**: [https://mitre-atlas.github.io/atlas-navigator/](https://mitre-atlas.github.io/atlas-navigator/)
- **NIST AI Publications**: [https://www.nist.gov/artificial-intelligence](https://www.nist.gov/artificial-intelligence)
- **AI Incident Database**: [https://incidentdatabase.ai](https://incidentdatabase.ai)
- **Awesome AI Security Lists**: 
  - [https://github.com/ottosulin/awesome-ai-security](https://github.com/ottosulin/awesome-ai-security)
  - [https://github.com/TalEliyahu/Awesome-AI-Security](https://github.com/TalEliyahu/Awesome-AI-Security)

### Learning Platforms (Free)
- **fast.ai**: [https://www.fast.ai](https://www.fast.ai)
- **FreeCodeCamp**: [https://www.freecodecamp.org](https://www.freecodecamp.org)
- **Coursera** (Audit Mode): [https://www.coursera.org](https://www.coursera.org)
- **MIT OpenCourseWare**: [https://ocw.mit.edu](https://ocw.mit.edu)
- **Kaggle Learn**: [https://www.kaggle.com/learn](https://www.kaggle.com/learn)

### Community and Forums
- **AI Village Discord**: [https://aivillage.org/discord](https://aivillage.org/discord)
- **OWASP Slack**: [https://owasp.slack.com](https://owasp.slack.com)
- **Reddit Communities**:
  - r/netsec: [https://reddit.com/r/netsec](https://reddit.com/r/netsec)
  - r/MachineLearning: [https://reddit.com/r/MachineLearning](https://reddit.com/r/MachineLearning)
  - r/LocalLLaMA: [https://reddit.com/r/LocalLLaMA](https://reddit.com/r/LocalLLaMA)
- **Hugging Face Forums**: [https://discuss.huggingface.co](https://discuss.huggingface.co)

### Free Compute Resources
- **Google Colab**: [https://colab.research.google.com](https://colab.research.google.com)
- **Kaggle Notebooks**: [https://www.kaggle.com/code](https://www.kaggle.com/code)
- **GitHub Codespaces**: [https://github.com/features/codespaces](https://github.com/features/codespaces) (120 hrs/month)
- **Gitpod**: [https://www.gitpod.io](https://www.gitpod.io) (50 hrs/month)
- **Paperspace Gradient**: [https://gradient.run](https://gradient.run) (free tier)

---

## Progress Tracking

### 6-Month Milestones

**Technical Skills**
- [ ] Execute 10 different attack types
- [ ] Build 5 security tools
- [ ] Find 10 valid vulnerabilities
- [ ] Complete 20 CTF challenges
- [ ] Contribute to 3 major projects

**Portfolio Development**
- [ ] 20+ technical blog posts
- [ ] 1000+ GitHub commits
- [ ] 5+ detailed vulnerability write-ups
- [ ] 3+ conference talk proposals
- [ ] 10+ tool demonstrations

**Professional Growth**
- [ ] 500+ LinkedIn connections in AI security
- [ ] 3+ consulting inquiries received
- [ ] 1+ paid engagement completed
- [ ] Known expert in 3+ communities

### Weekly Time Commitment

**Daily (2-3 hours)**
- **Morning (30 min):** Read one research paper, review security news
- **Lunch (30 min):** Watch one conference talk, practice one CTF challenge
- **Evening (1-2 hours):** Hands-on lab work, tool development, blog writing

**Weekend (4-6 hours):**
- [ ] Deep dive into new attack technique
- [ ] Build/improve security tool
- [ ] Write comprehensive blog post
- [ ] Participate in CTF or bug bounty

---

## Requirements Files

### requirements.txt (Core Dependencies)
```
# Essential AI Security Tools
garak
promptfoo
adversarial-robustness-toolbox
foolbox
textattack

# Core ML Libraries
torch
transformers
tensorflow
numpy
pandas
scikit-learn

# LLM Tools
langchain
openai
anthropic

# Development
jupyter
streamlit
gradio
```

### requirements-minimal.txt (Quick Start)
```
numpy
pandas
requests
jupyter
notebook
```

See `requirements-full.txt` for complete dependencies including all frameworks and tools.

---

## Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Ways to contribute:**
- Add new resources you discover
- Update links that have changed
- Share lab solutions (ethically)
- Contribute tools back to the community
- Report issues or suggest improvements

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## About

This learning path was compiled and is maintained by [Waypoint Compliance Advisory LLC](https://waypointcompliance.com), a Service-Disabled Veteran-Owned Small Business (SDVOSB) specializing in cybersecurity consulting, CMMC compliance, and AI security assessments.

**Contact:** [info@waypointcompliance.com](mailto:info@waypointcompliance.com)

---

**The knowledge is free. The tools are free. The communities are free. Your only investment is time and determination.**

*Last Updated: January 2026*
