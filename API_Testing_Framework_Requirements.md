
# 🧪 API Testing Framework Using PyTest + Requests

## 🎯 Objective
Build a maintainable, scalable framework to test REST APIs. Focus on modular design, data-driven testing, reusable components, and easy configuration for different environments (QA, Staging, Prod).

---

## 🛠️ Requirements

### 1. Framework Design
- Use `PyTest` for test structure.
- Use `Requests` library for making API calls.
- Organize tests using folders/modules (e.g., `tests`, `utils`, `data`, `config`).

### 2. Core Features
- Support for GET, POST, PUT, DELETE.
- Token-based or Basic Auth support.
- Custom assertions for status code, headers, JSON fields, etc.
- Reusable request handler functions.
- Config file for base URLs, endpoints, headers.

### 3. Test Data
- Use JSON or YAML files for payloads and input data.
- Parameterize tests using `pytest.mark.parametrize`.

### 4. Reporting
- Integrate Allure or HTMLTestRunner for detailed reports.
- Include request/response in test logs.

### 5. Advanced Features (Optional but Recommended)
- Add support for multiple environments via CLI or `.env`.
- Retry logic for flaky tests.
- JSON schema validation.
- Tagging and grouping tests (e.g., smoke, regression).
- Integration with Jenkins for CI pipeline.

---

## 📂 Sample Directory Structure

```
api_test_framework/
│
├── tests/
│   ├── test_users.py
│   ├── test_orders.py
│
├── utils/
│   ├── request_handler.py
│   ├── validators.py
│
├── config/
│   ├── config.yaml
│   ├── environments/
│       ├── qa.yaml
│       ├── staging.yaml
│
├── data/
│   ├── users.json
│   ├── orders.json
│
├── conftest.py
├── requirements.txt
├── pytest.ini
└── README.md
```

## How to Run

Run the following command in your terminal to execute all tests:

```bash

pytest
| Command                                      | Description                                                 |
| -------------------------------------------- | ----------------------------------------------------------- |
| `pytest`                                     | Runs all tests in the current directory and subdirectories. |
| `pytest tests/`                              | Runs tests located in the `tests` folder.                   |
| `pytest -v`                                  | Runs tests in **verbose** mode (shows more details).        |
| `pytest -s`                                  | Disables output capture (shows print/log output).           |
| `pytest test_example.py`                     | Runs tests from a specific file.                            |
| `pytest test_example.py::test_function_name` | Runs a single specific test.                                |
| `pytest -k "keyword"`                        | Runs tests whose names match a keyword expression.          |
| `pytest --maxfail=3 --disable-warnings -q`   | Stops after 3 failures, hides warnings, and runs quietly.   |
