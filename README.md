# Python Pytest Selenium Framework

![Python](https://img.shields.io/badge/python-3.11-blue)
![Pytest](https://img.shields.io/badge/pytest-8.3-green)
![CI](https://img.shields.io/github/actions/workflow/status/snnarangsumit/python-pytest-selenium-framework/python-app.yml)

## 🛠 Overview
A modern Python Selenium framework using pytest for UI automation.  
It demonstrates **Page Object Model (POM)** design, reusable utilities, and reporting.  
Designed to be scalable, CI/CD-ready, and interview-friendly.

---

## 🛠 Tech Stack
- Python 3.9 - 3.12  
- Selenium 4.24+  
- Pytest 8.3+  
- HTML/Allure Reporting  
- GitHub Actions CI/CD

---

## 🛠 Features
- Page Object Model (POM) design  
- Supports Chrome, Firefox, and remote browsers  
- Environment-based configuration (dev, stage)  
- Reusable helper utilities  
- Secure secrets handling  
- Generates test reports with logs  

---

## 🛠 Folder Structure
```
python-pytest-selenium-framework/
├── config/ # environment configs
├── drivers/ # browser driver setup
├── resources/ # test data (JSON, CSV, YAML)
├── src/
│   └── pageobjects/ # Page Object Models
├── tests/
│   └── fill_form/ # test scripts organized by feature
├── utils/ # helper functions (logger, browser utils)
├── .github/ # CI/CD workflows
├── requirements.txt
├── conftest.py
├── README.md
└── .gitignore
```

---

## 🛠 How to Run

1. Clone the repository:
```bash
git clone https://github.com/snnarangsumit/python-pytest-selenium-framework.git
cd python-pytest-selenium-framework
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run tests:
```bash
pytest tests/ --html=reports/report.html --self-contained-html
```

4. Open report:
```
reports/report.html
```

---

## 🛠 Talking Points
- Framework design & POM explanation  
- Environment/config management  
- Reporting & CI/CD integration  
- Utilities & reusability  
- Cross-browser support and scalability

