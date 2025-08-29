# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.7.0] - 2025-08-29

### Changed
- **BREAKING**: Upgraded Java version from 8 to 17
- **BREAKING**: Migrated groupId from `org.smartregister` to `io.github.bluecodesystems`
- Updated all dependencies to Java 17 compatible versions:
  - lombok: 1.18.12 → 1.18.34
  - jackson: 2.10.5.1 → 2.17.2  
  - junit: 4.13.1 → 4.13.2
  - mockito: 3.3.0 → 5.14.2
  - commons-lang3: 3.12.0 → 3.17.0
  - commons-text: 1.8 → 1.12.0
  - gson: 2.8.6 → 2.11.0
  - joda-time: 2.10.6 → 2.13.0
  - jacoco: 0.8.5 → 0.8.12
  - powermock: 2.0.5 → 2.0.9
  - equalsverifier: 3.1.12 → 3.17.1
  - openpojo: 0.8.6 → 0.9.1

### Added
- Added pluginManagement section for better plugin version control
- Centralized dependency versions using properties for better maintainability

### Updated
- Maven plugins to latest versions:
  - maven-compiler-plugin: 3.8.1 → 3.13.0 with Java 17 release configuration
  - maven-source-plugin: add version 3.3.1
  - maven-javadoc-plugin: add version 3.10.1 with Java 17 configuration

### Infrastructure
- Added maven-central-bundle/ to .gitignore to exclude build artifacts

### Migration Notes
**Breaking Changes:**
- This release requires Java 17 or higher
- GroupId changed from `org.smartregister` to `io.github.bluecodesystems`
- Update your dependency declarations:
  ```xml
  <dependency>
      <groupId>io.github.bluecodesystems</groupId>
      <artifactId>opensrp-plan-evaluator</artifactId>
      <version>1.7.0</version>
  </dependency>
  ```

**Gradle:**
```gradle
implementation 'io.github.bluecodesystems:opensrp-plan-evaluator:1.7.0'
```