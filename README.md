# 🚀 Avro Schemas

[![CI](https://github.com/Christos-Hadjinikolis/avro-schemas/actions/workflows/ci.yml/badge.svg)](https://github.com/Christos-Hadjinikolis/avro-schemas/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

📦 Canonical Avro schemas used as shared data contracts across projects.

## ✨ Why This Repo Exists

This repository is the source of truth for schema definitions written in Avro IDL.

Every change is designed to be:

- 🔍 Easy to review
- 🧪 Validated in CI
- 🔁 Safer for downstream consumers
- 🧱 Consistent across projects

The build generates:

- `build/generated-main-avro-avpr` for generated Avro JSON definitions
- `build/generated-main-avro-java` for generated Java sources

## ⚡ Quick Start

Prerequisites:

- ☕ JDK 21
- 🛠️ The checked-in Gradle wrapper

Run the validation build:

```bash
./gradlew clean check
```

## 🧭 Working With Schemas

1. Add or update `*.avdl` files under `src/main/avro`.
2. Use [`Example.avdl`](src/main/avro/Example.avdl) as the reference for structure and namespace conventions.
3. Run `./gradlew clean check`.
4. Review generated output in `build/generated-main-avro-avpr` and `build/generated-main-avro-java`.

## 📝 Example

```avdl
namespace io.github.christoshadjinikolis.schemas.avro;

schema Example;

record Example {
    string id = "";
    string name = "";
    string surname = "";
    int salary = 0;
    int taxPercentage = 0;
}
```

See the full example in [`src/main/avro/Example.avdl`](src/main/avro/Example.avdl).

## 🔐 Compatibility Expectations

- Prefer additive, backward-compatible schema changes.
- Treat breaking changes as exceptional and document them clearly in the pull request.
- Call out downstream consumers that need to coordinate with the change.

## 🗂️ Repository Layout

```text
src/main/avro/                   Avro IDL source files
build/generated-main-avro-avpr/  Generated Avro JSON definitions
build/generated-main-avro-java/  Generated Java sources
```

## 🛠️ Tooling Notes

- Use the repository Gradle wrapper rather than a globally installed Gradle version.
- The build now targets Java `21` and Gradle `8.14.3`.
- Gradle supports Java 21 starting with Gradle `8.5`, and the current `8.14.x` patch line keeps the repository on a current Java 21-capable release.
- Install the Apache Avro Support plugin for a better editor experience:
  https://plugins.jetbrains.com/plugin/7971-apache-avro-support

## 🤝 Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for setup, schema change workflow, and pull request expectations.

## 📄 License

This project is available under the [MIT License](LICENSE).
