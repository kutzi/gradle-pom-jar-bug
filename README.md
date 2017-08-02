# gradle-pom-jar-bug

Reproduction steps for https://github.com/gradle/gradle/issues/2631:
- delete your local Maven repository (.m2/repository) and Gradle caches (.gradle/caches)
- run mvn install
-- => local Maven repo contains only the POM for zookeeper 3.4.6
- run gradle jar
-- => check created JAR in build/libs - it doesn't contain the zookeeper classes

- delete local maven repository and try again gradle jar
-- => check created JAR in build/libs - now it does contain the zookeeper classes
