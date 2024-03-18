# Setup of Baisc Gradle project using CLI

```dtd
gradle init --use-defaults --type java-application
```
The above command will setup a basic gradle project.

To prepare a jar which is executable, we need to setup a manifest property in ``` build.gradle``` to identify the Main class to execute.
```dtd
jar {
    manifest {
        attributes(
                'Main-Class' : 'org.example.Main'
        )
    }
}
```
```dtd
./gradlew build
```

The above command will build the project.

```dtd
./gradlew jar
```
The above command creates a new jar file in the ``` build/libs``` folder.

```dtd
java -jar build/libs/filename.jar
```
The above command will execute the code.