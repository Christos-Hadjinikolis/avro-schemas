# schemas
A project for versioning various canonical schemas we use with a variety of projects.

## How to use
1. Just go under `src/main/avro` and add your `*.avdl` file. Have a look at the `Example.avdl` 
file, to get an idea about how yours should look.
2. In the terminal run:
```kotlin
./gradlew clean check
```
3. Check under the projects `build` directory under `generated-main-avro-avpr` for the 
`java` POJO automatically generated.  
 
## Useful plugins
Install https://plugins.jetbrains.com/plugin/7971-apache-avro-support for a more convenient `avro` editor.
  