pro-3: Installing intelliJ 
IntelliJ IDEA Community Edition (Free version): sudo snap install intellij-idea-community --classic
IntelliJ IDEA Ultimate Edition (Paid version, has a free trial):sudo snap install intellij-idea-ultimate --classic

using terminal:
 1.Install Java JDK :
sudo apt update
sudo apt install openjdk-17-jdk -y

2. sudo apt install gradle -y
3. mkdir GradleDemo
cd GradleDemo

4. gradle init :
5. Answer the prompts:

Type of project → 2: application

DSL → 1: Groovy

Language → 1: Java

Project name → GradleDemo or any name

6. Edit build.gradle -nano build.gradle

7. plugins {
    id 'java'
    id 'application'
}

group = 'org.example'
version = '1.0-SNAPSHOT'

repositories {
    mavenCentral()
}

dependencies {
    implementation 'com.google.guava:guava:32.1.2-jre'
    testImplementation 'junit:junit:4.13.2'
}

application {
    mainClass = 'Hello'
}

task helloWorld {
    doLast {
        println 'Hello, Gradle!'
    }
}

tasks.build {
    doLast {
        println "Build finished! You can deploy now."
    }
}
Save and exit (Ctrl+O, Enter, then Ctrl+X).
8.
mkdir -p src/main/java
nano src/main/java/Hello.java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello from Java with Gradle!");
    }
}
9.. Run Custom Task -./gradlew helloWorld
10. Run the Build - ./gradlew build
11. eun the java app - ./gradle run





 
