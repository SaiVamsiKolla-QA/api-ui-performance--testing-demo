# Comprehensive Web Testing Framework (Python & Postman)
<div align="center">

![CI Status](https://github.com/SaiVamsiKolla-QA/api-ui-performance-testing-demo/workflows/CI/badge.svg)
![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)
![Pytest](https://img.shields.io/badge/testing-pytest-green.svg)
![Selenium](https://img.shields.io/badge/automation-selenium-orange.svg)
![Allure](https://img.shields.io/badge/reports-allure-yellow.svg)
![License](https://img.shields.io/badge/license-Open%20Source-brightgreen.svg)
![Platform](https://img.shields.io/badge/platform-cross--platform-lightgrey.svg)

</div>

A robust automated testing framework demonstrating expertise across multiple testing layers: UI Testing, API Simulation Testing, and Performance Testing. All tests target the Sauce Labs Swag Labs demo website, showcasing a structured approach to quality assurance for modern web applications.

## 🎯 Project Overview

This project serves as a practical demonstration of building maintainable automated testing solutions that integrate both code-based (Python) and tool-based (Postman, JMeter) approaches. The framework uniquely combines different testing methodologies to provide comprehensive coverage of web application functionality.

**Target Application:** [Sauce Labs Swag Labs](https://www.saucedemo.com/)

## 🛠️ Technologies & Tools

- **Python** - Primary programming language for test automation
- **pytest** - Testing framework with rich assertion library and plugin architecture
- **requests** - HTTP library for programmatic API interaction
- **Selenium WebDriver** - Browser automation for UI functional testing
- **Page Object Model (POM)** - Design pattern for maintainable UI tests
- **Postman** - API development and testing platform
- **Apache JMeter** - Load and performance testing tool
- **Allure** - Advanced test reporting framework for beautiful, interactive reports
- **GitHub Actions** - Continuous Integration (CI) pipeline

## 📁 Project Structure

```
comprehensive-web-testing-framework/
├── ui_tests/                    # UI automation tests
│   ├── pages/                   # Page Object Model classes
│   └── tests/                   # UI test cases
├── api_tests/                   # API simulation tests
│   └── test_api_simulation.py
├── performance_tests/           # JMeter performance tests
├── postman_collections/         # Postman API test collections
├── conftest.py                  # pytest fixtures and configuration
├── requirements.txt             # Python dependencies
├── .github/workflows/           # CI/CD configuration
└── README.md
```

## 🚀 Installation & Setup

### Prerequisites

- Python 3.8 or higher
- Chrome or Firefox browser
- Git

### Installation Steps

```bash
# Clone the repository
git clone https://github.com/SaiVamsiKolla-QA/api-ui-performance-testing-demo.git
cd api-ui-performance-testing-demo

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Install browser drivers (if not using WebDriver Manager)
# ChromeDriver will be managed automatically via selenium-manager
```

## 🧪 Running Tests

### UI Tests

```bash
# Run all UI tests
pytest ui_tests/ -v

# Run specific UI test file
pytest ui_tests/tests/test_login.py -v

# Run with Allure report
pytest ui_tests/ --alluredir=allure-results
allure serve allure-results
```

### API Simulation Tests

```bash
# Run API simulation tests
pytest api_tests/ -v

# Run with Allure reporting
pytest api_tests/ --alluredir=allure-results -v
```

### All Python Tests

```bash
# Run complete test suite with Allure
pytest --alluredir=allure-results -v

# Generate and serve Allure report
allure serve allure-results

# Run with coverage
pytest --cov=. --cov-report=html
```

### Performance Tests

1. Open Apache JMeter
2. Load test plan from `performance_tests/` directory
3. Configure thread groups for desired load
4. Execute and analyze results

### Postman Collections

1. Import collections from `postman_collections/` directory into Postman
2. Run individual requests or entire collections
3. Use Postman Runner for automated execution

## 🎯 Key Features & Testing Capabilities

### UI Test Automation with Page Object Model
- ✅ **User Authentication Testing**
  - Valid user login verification
  - Invalid credentials handling
  - Locked user account scenarios
  - Secure logout functionality
- ✅ **Dynamic Element Handling**
  - Explicit waits for robust test execution
  - Cross-browser compatibility
- ✅ **Maintainable Architecture**
  - Page Object Model implementation
  - Reusable components and utilities

### API Simulation Testing
- ✅ **Dual Approach Implementation**
  - Python `requests` library for programmatic testing
  - Postman collections for GUI-based testing
- ✅ **Browser Traffic Simulation**
  - Reverse-engineered HTTP requests from browser network traffic
  - Login/logout API endpoint simulation
  - HTTP status code and response validation

### Performance Testing
- ✅ **Load Testing Capabilities**
  - Concurrent user simulation with Apache JMeter
  - Login functionality performance assessment
  - Response time and throughput analysis
- ✅ **Responsible Testing**
  - Moderate load respect for public demo environment

### Continuous Integration
- ✅ **Automated Test Execution**
  - GitHub Actions integration
  - Automated testing on code changes
  - Quick feedback loop for quality assurance

## 📊 Test Reports

The framework generates comprehensive test reports:

- **Allure Reports**: Beautiful, interactive test execution reports with detailed step-by-step execution, screenshots, and test analytics
- **Coverage Reports**: Code coverage analysis
- **JMeter Reports**: Performance testing metrics
- **CI/CD Reports**: Automated test results in GitHub Actions

## 🔧 Configuration

### Browser Configuration
```python
# conftest.py - Browser setup
@pytest.fixture
def driver():
    # Configure your preferred browser options
    options = webdriver.ChromeOptions()
    options.add_argument("--headless")  # For CI environment
    driver = webdriver.Chrome(options=options)
    yield driver
    driver.quit()
```

### Test Data Management
```python
# Centralized test data configuration
TEST_USERS = {
    "standard_user": "standard_user",
    "locked_out_user": "locked_out_user",
    "problem_user": "problem_user"
}
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-test-scenario`)
3. Commit your changes (`git commit -m 'Add comprehensive checkout flow tests'`)
4. Push to the branch (`git push origin feature/new-test-scenario`)
5. Open a Pull Request

## 📈 Future Enhancements

- [ ] Advanced performance monitoring
- [ ] Test data management with factories
- [ ] Parallel test execution optimization

## 🎓 Learning Outcomes

This project demonstrates proficiency in:

- **Test Automation Architecture** - Scalable and maintainable test framework design
- **Multi-layer Testing** - UI, API, and Performance testing integration
- **Tool Integration** - Combining code-based and tool-based testing approaches
- **CI/CD Implementation** - Automated testing pipeline setup
- **Quality Assurance Best Practices** - Comprehensive testing strategy

## 📞 Contact

For questions, suggestions, or collaboration opportunities:

- **GitHub Issues**: [Create an issue](https://github.com/SaiVamsiKolla-QA/api-ui-performance-testing-demo/issues)
- **Email**: saivamsikolla@gmail.com
- **LinkedIn**: [Sai Vamsi Kolla](https://www.linkedin.com/in/saivamsi-kolla/)

## 📄 License

This project is open source and available for educational and demonstration purposes.

## 🙏 Acknowledgments

- Sauce Labs for providing the Swag Labs demo application
- The open-source testing community for excellent tools and frameworks
- Contributors and testers who help improve this framework

---

**⚠️ Important Note**: This framework is designed for educational and demonstration purposes using the public Sauce Labs demo site. Always ensure you have proper authorization before testing any web application.
