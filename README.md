Below is a sample `README.md` that you could use as a template for your Java 17 Maven Parent POM library under the `net.sasu.lib` namespace. Adjust the details (like versions, badges, and descriptions) as needed for your specific library.

---

# net.sasu.lib-parent

A Maven parent POM for libraries under the `net.sasu.lib` namespace. Purpose: entralizing common configuration and dependency management.

## Table of Contents
- [Features](#features)
- [Usage](#usage)
- [Configuration & Setup](#configuration--setup)
- [Contributing](#contributing)
- [License](#license)

---

## Features
- Centralized **Java 17** version enforcement and compilation settings.
- Common plugins and plugin management (Surefire, JUnit, etc.).
- Shared dependency management (predefined versions for well-known libraries).
- Common code quality checks and build configurations.
- Simplifies version alignment across multiple `net.sasu.lib` projects.
- Makes deployment easier by ensuring that the settings are aligned in all libraries

## Usage

To use this parent POM in your project, update your `pom.xml` file with the following snippet:

```xml
<project>
    <modelVersion>4.0.0</modelVersion>
    <parent>
        <groupId>net.sasu.lib</groupId>
        <artifactId>net-sasu-lib-parent</artifactId>
        <version>1.0.2</version>
    </parent>
    
    <artifactId>my-library</artifactId>
    <packaging>jar</packaging>
    <name>My Library</name>
    <description>A description for my library.</description>

    <!-- Your project-specific configuration here -->

</project>
```


## Configuration & Setup

### Java Version
This parent POM enforces the usage of Java 17. Make sure your system is configured with Java 17 installed:

```xml
<properties>
    <maven.compiler.source>17</maven.compiler.source>
    <maven.compiler.target>17</maven.compiler.target>
</properties>
```

### Plugins & Dependencies
We have pre-configured several popular Maven plugins:
- **Maven Surefire Plugin** for unit testing.
- **Maven Compiler Plugin** pinned to 17 for consistency.

Additionally, some commonly used dependencies (like JUnit) may already be managed by this parent, so you only need to add them as needed within `<dependencies>` without worrying about version conflicts.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use or modify it as appropriate for your own needs.
