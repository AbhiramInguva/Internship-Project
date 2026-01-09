# 🛡️ Password Security Toolkit (PST)

### **Internship Project: Defensive Analysis & Offensive Simulation Engine**

## 📖 Executive Summary

This project was developed to address the "Complexity Paradox"—the phenomenon where passwords meet corporate complexity requirements (length, symbols, casing) but remain vulnerable to targeted dictionary attacks. The **PST** provides a professional-grade API for auditing password strength using pattern-recognition entropy and a generation engine for simulating targeted brute-force attacks.

---

## 🛠️ System Architecture

The toolkit is built using an **Object-Oriented Programming (OOP)** approach to ensure modularity. By encapsulating logic within the `PasswordSecurityEngine` class, the core security functions are decoupled from the user interface.

### **Core Modules**

1. **The Analyst (`zxcvbn` Integration):** * Moves beyond simple "character-type" counting.
* Implements spatial heuristics (keyboard patterns) and dictionary lookups (30k+ common entries).
* Calculates **Guesses to Crack** based on a  guesses/sec offline hash-cracking scenario.


2. **The Generator (Permutation Engine):**
* **Seed Logic:** Ingests PII (Personally Identifiable Information) such as names and dates.
* **Recursive Leetspeak:** Applies multi-level character substitution.
* **Temporal Masking:** Automatically appends historical and current year variations.



---

## 📊 Technical Specifications

### **Strength Metrics**

The engine evaluates entropy () and converts it into a score of 0-4. The mathematical model assumes:


### **Wordlist Permutation Logic**

For every "Seed Word," the engine generates:

* **Casing:** `lower`, `Title`, `UPPER`
* **Substitutions:** `a -> @`, `s -> $`, `o -> 0`, etc.
* **Suffixes:** Common symbols (`!`, `?`) and Year markers.

---

## 🚀 Installation & Deployment

### **Requirements**

* Python 3.8+
* `zxcvbn` library

### **Setup**

```bash
# Clone the repository
git clone https://github.com/yourusername/password-security-toolkit.git

# Install dependencies
pip install zxcvbn

```

### **Usage (API)**

```python
from security_engine import PasswordSecurityEngine

# Initialize Engine
engine = PasswordSecurityEngine()

# Perform Audit
results = engine.analyze_strength("MyP@ssword2024")

# Generate Attack List
engine.generate_targeted_wordlist(seeds=["John", "Buddy"], years=["1995", "2026"])

```

---

## 📈 Internship Portfolio Impact

This project demonstrates proficiency in:

* **Cybersecurity Principles:** Understanding the bridge between Application Security (AppSec) and human-centric vulnerabilities.
* **Clean Code Standards:** Implementing Type Hinting, Docstrings, and PEP8 compliance.
* **Data Serialization:** Handling automated file exports for integration with security tools like **Hashcat** or **John the Ripper**.

---

## ⚖️ Ethical Disclaimer

This tool is intended for **Ethical Security Auditing** and educational purposes. Usage of the wordlist generator against systems without explicit written consent is illegal and a violation of the Computer Fraud and Abuse Act (CFAA).

---

### **How to use this on GitHub**

1. Create a new file in your repo titled `README.md`.
2. Paste the content above.
3. Upload your `main.py` (the OOP code I provided previously).

**Would you like me to create a "Technical Presentation" outline in case you have to present this to your internship manager?**
