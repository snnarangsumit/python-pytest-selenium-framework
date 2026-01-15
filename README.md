# Python Pytest Selenium Framework

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![Selenium](https://img.shields.io/badge/Selenium-4.x-green?style=for-the-badge&logo=selenium)
![Pytest](https://img.shields.io/badge/Pytest-7.x-orange?style=for-the-badge&logo=pytest)


Enterprise-grade UI test automation framework built with Python, Pytest, and Selenium WebDriver.


## 🎯 Overview

This framework implements the **Page Object Model (POM)** design pattern for maintainable and scalable UI automation. Built for enterprise web applications with cross-browser support and CI/CD integration.

## ✨ Key Features

- ✅ **Page Object Model** - Clean separation of test logic and page elements
- ✅ **Cross-Browser Testing** - Chrome, Firefox, Edge support
- ✅ **Parallel Execution** - Run tests in parallel using pytest-xdist
- ✅ **Data-Driven Testing** - Support for Excel, CSV, and JSON data sources
- ✅ **Smart Waits** - Explicit and implicit wait strategies
- ✅ **Screenshot on Failure** - Automatic capture for debugging
- ✅ **Comprehensive Logging** - Detailed execution logs
- ✅ **HTML & Allure Reports** - Multiple reporting options
- ✅ **CI/CD Ready** - GitHub Actions integration

## 📋 Prerequisites

- Python 3.8+
- pip package manager
- Chrome/Firefox browser

## 🚀 Quick Start

### Installation
```bash
# Clone the repository
git clone https://github.com/snnarangsumit/python-pytest-selenium-framework.git
cd python-pytest-selenium-framework

# Create virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### Run Tests
```bash
# Run all tests
pytest tests/ -v

# Run specific test file
pytest tests/test_login.py -v

# Run tests with markers
pytest -m smoke    # Smoke tests only
pytest -m regression    # Regression tests

# Parallel execution
pytest tests/ -n 4    # Run with 4 workers

# Generate HTML report
pytest tests/ --html=reports/report.html --self-contained-html

# Generate Allure report
pytest tests/ --alluredir=reports/allure
allure serve reports/allure
```

## 📁 Project Structure
```
python-pytest-selenium-framework/
│
├── src/                    # Source code
│   ├── pages/             # Page Object classes
│   └── helpers/           # Helper functions
│
├── tests/                  # Test cases
│   └── conftest.py        # Pytest fixtures
│
├── utils/                  # Utility modules
│   ├── logger.py          # Logging utility
│   └── screenshot.py      # Screenshot utility
│
├── config/                 # Configuration files
│   └── key.properties     # App configuration
│
├── resources/              # Test resources & data
│
├── drivers/                # WebDriver binaries
│
├── .github/workflows/      # CI/CD pipelines
│
├── requirements.txt        # Python dependencies
├── pytest.ini              # Pytest configuration
├── Dockerfile              # Docker configuration
├── conftest.py             # Root-level fixtures
└── README.md               # This file
```

## ⚙️ Configuration

Edit `config/config.ini` to customize:
- Base URL
- Browser selection (chrome/firefox/edge)
- Timeout values
- Screenshot settings

## 🔧 Tech Stack

- **Python** - Programming language
- **Pytest** - Testing framework
- **Selenium WebDriver** - Browser automation
- **WebDriver Manager** - Automatic driver management
- **Allure** - Test reporting
- **GitHub Actions** - CI/CD

## 📊 Reports

- **HTML Reports** - Available in `reports/html/`
- **Allure Reports** - Interactive reports with detailed test steps
- **Screenshots** - Captured on test failures in `reports/screenshots/`
- **Logs** - Detailed execution logs in `logs/`

## 🤝 Best Practices Implemented

- Page Object Model (POM) design pattern
- DRY principle - Reusable methods
- Explicit waits over implicit waits
- Independent test cases
- Meaningful assertions
- Proper error handling
- Clean code structure

## 📝 Sample Test
```python
import pytest
from pages.login_page import LoginPage

class TestLogin:
    
    @pytest.mark.smoke
    def test_valid_login(self, driver):
        login_page = LoginPage(driver)
        login_page.navigate_to_login()
        login_page.login("username", "password")
        assert login_page.is_login_successful()
```

## 🔄 CI/CD Integration

This framework includes GitHub Actions workflow for automated test execution on:
- Push to main/develop branches
- Pull requests
- Scheduled runs (daily)

## 📧 Contact

**Sumit Narang**
- LinkedIn: [linkedin.com/in/sumit-narang15](https://www.linkedin.com/in/sumit-narang15)
- GitHub: [@snnarangsumit](https://github.com/snnarangsumit)


---

⭐ **If you find this framework helpful, please give it a star!**
