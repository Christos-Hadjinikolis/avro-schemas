# Contributing

## Setup

1. Use JDK 21.
2. Use the repository Gradle wrapper rather than a globally installed Gradle version.
3. Run:

```bash
./gradlew clean check
```

This project currently uses Gradle `8.14.3` and targets Java `21`.

## Making Schema Changes

1. Add or update Avro IDL files in `src/main/avro`.
2. Follow the namespace and layout used in [`Example.avdl`](src/main/avro/Example.avdl).
3. Keep schema changes backward compatible unless the change is intentionally breaking and agreed in advance.
4. Run `./gradlew clean check` before opening a pull request.
5. Review generated sources in `build/generated-main-avro-java` and confirm the output matches the intended API.

## Pull Requests

- Keep pull requests scoped to one logical schema change where possible.
- Describe the business reason for the change and any compatibility impact.
- Include regenerated build output only if the repository starts tracking it in the future.
- Call out any downstream consumers that must coordinate with the schema update.
- Ensure CI is green before requesting review.
