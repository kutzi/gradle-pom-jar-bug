# gradle-pom-jar-bug

Steps to reproduce:
- delete your local Maven repository (.m2/repository) and Gradle caches (.gradle/caches)
- run mvn install
-- => local Maven repo contains the POM for zookeeper 3.4.6
- run gradle jar
-- => check create JAR in build/libs - it doesn't contain the zookeeper classes

- delete local maven repository and try again gradle jar
-- => check create JAR in build/libs - now it does contain the zookeeper classes
