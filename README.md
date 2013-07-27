You can use this repository as a maven repo in your gradle build. Example of working `build.gradle`:

```groovy
buildscript {
    repositories {
        mavenCentral()
    }

    dependencies {
        classpath 'com.android.tools.build:gradle:0.5+'
    }
}

repositories {
    mavenCentral()
    mavenLocal()
    maven {
        url "http://mente.github.io/facebook-api-android-aar"
    }
}

apply plugin: 'android'
dependencies {
    compile 'com.facebook:facebook-android-sdk:3.0.2@aar'
    //your other dependencies
}

android {
	//android build setup
}
```