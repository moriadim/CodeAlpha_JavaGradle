# 🛠️ Java Gradle Project – Task 3 (CodeAlpha Internship)

This project was built as part of Task 3 for the CodeAlpha internship. It demonstrates how to set up a **Java application using Gradle**, build and run the application, and integrate **Continuous Integration (CI)** using **GitHub Actions**.

---

## 🚀 Features

- ✅ Java application using Gradle
- ✅ JUnit tests
- ✅ GitHub Actions CI pipeline
- ✅ Compatible with Java 23
- ✅ Clean and simple structure

---

## 📁 Project Structure

```

CodeAlpha\_JavaGradle/
├── app/
│   └── src/
│       ├── main/java/org/example/App.java
│       └── test/java/org/example/AppTest.java
├── build.gradle
├── settings.gradle
└── .github/
└── workflows/
└── gradle.yml

````

---

## 🧑‍💻 Getting Started

### 🔧 Prerequisites

- Java 17+ (Java 23 recommended)
- Gradle (or use the included Gradle Wrapper)
- Git

### 📦 Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/moriadim/CodeAlpha_JavaGradle.git
   cd CodeAlpha_JavaGradle
````

2. Run the project:

   ```bash
   ./gradlew run
   ```

3. Build the project:

   ```bash
   ./gradlew build
   ```

4. Run tests:

   ```bash
   ./gradlew test
   ```

---

## 🔁 CI/CD with GitHub Actions

This project includes a **GitHub Actions** workflow that automatically runs on every `push` or `pull request` to the `main` branch. It builds the project and runs tests.

### 📄 Workflow File

The file is located at `.github/workflows/gradle.yml` and contains:

```yaml
name: Java CI with Gradle

on:
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v4

      - name: Set up JDK 23
        uses: actions/setup-java@v4
        with:
          java-version: '23'
          distribution: 'temurin'

      - name: Grant execute permission for Gradle wrapper
        run: chmod +x gradlew

      - name: Build with Gradle
        run: ./gradlew build

---

## 📬 Output Example

```
> Task :app:run
Hello World!
```

---

## 📚 Learning Outcome

* Learned how to initialize a Gradle project
* Understood Gradle build and test lifecycle
* Automated build/test using GitHub Actions
* Practical exposure to CI in modern DevOps workflows

---

## 🤝 Contributing

Pull requests are welcome! If you have suggestions or want to improve the app, feel free to fork and submit changes.

---


## 🙌 Acknowledgments

* [Gradle Documentation](https://docs.gradle.org/)
* [GitHub Actions](https://docs.github.com/en/actions)
* [CodeAlpha](https://codealpha.tech)

```

---

