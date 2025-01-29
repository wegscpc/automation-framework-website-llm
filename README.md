# Automation Framework with LLM Integration

A modern test automation framework that combines Selenium WebDriver with Large Language Models (LLM) for enhanced web testing capabilities.

## Features

- **Multi-Browser Support**: Chrome (default) with WebDriverManager for automatic driver management
- **BDD Implementation**: Cucumber integration for behavior-driven development
- **LLM Integration**: Support for multiple LLM providers (OpenAI, LM Studio, Mock)
- **Flexible Configuration**: Externalized configuration through properties files
- **Robust Logging**: SLF4J with Logback implementation
- **Smart Wait Strategies**: Both implicit and explicit waits with configurable timeouts
- **Failure Handling**: Automatic screenshot capture on test failure with retry mechanism

## Tech Stack

- Java 17
- Selenium WebDriver 4.15.0
- TestNG 7.8.0
- Cucumber 7.14.0
- WebDriverManager 5.6.2
- OpenAI API Client 0.18.2
- JSoup 1.17.2 for HTML parsing

## Project Structure

```
src/
├── main/
│   └── resources/
│       ├── config.properties    # Configuration settings
│       └── logback.xml         # Logging configuration
└── test/
    ├── java/
    │   └── com/automation/
    │       ├── BaseTest.java   # Test base class
    │       └── TestExample.java # Example test implementation
    └── resources/
        └── features/
            └── llm_integration.feature # BDD feature files
```

## Best Practices Implemented

1. **Design Patterns**
   - Page Object Model for better maintainability
   - Factory Pattern for WebDriver initialization
   - Builder Pattern for test data construction

2. **Code Organization**
   - Clear separation of concerns (test logic, configuration, features)
   - Modular and reusable components
   - BDD approach for better collaboration

3. **Configuration Management**
   - Externalized configuration in properties files
   - Environment-specific settings support
   - Secure handling of sensitive data (API keys)

4. **Testing Best Practices**
   - Smart wait strategies to prevent flaky tests
   - Screenshot capture on failure
   - Retry mechanism for unstable tests
   - Comprehensive logging

5. **LLM Integration**
   - Multiple provider support (OpenAI, LM Studio)
   - Fallback mechanisms
   - Local LLM support through LM Studio
   - Configurable model selection

## Getting Started

1. Clone the repository
2. Set up environment variables:
   - `OPENAI_API_KEY` (if using OpenAI)
3. Configure `config.properties` as needed
4. Run tests using Maven:
   ```bash
   mvn clean test
   ```

## Configuration

Key configurations in `config.properties`:
- Browser settings (type, timeout)
- LLM provider selection
- Wait timeouts
- Test retry settings
- Screenshot configurations
