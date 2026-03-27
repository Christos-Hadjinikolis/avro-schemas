## Summary

Describe the schema change clearly and briefly.

## Why

Explain the business or technical reason for this change.

## Schema Impact

- [ ] This change is backward compatible
- [ ] This change is intentionally breaking and has been called out below
- [ ] Downstream consumers have been identified

Compatibility notes:

<!-- Describe any compatibility concerns, migration notes, or coordination needs. -->

## Validation

- [ ] I ran `./gradlew clean check`
- [ ] I reviewed the generated output under `build/generated-main-avro-avpr`
- [ ] I reviewed the generated output under `build/generated-main-avro-java`

## Downstream Coordination

List any services, teams, or consumers that need to be aware of this change.
