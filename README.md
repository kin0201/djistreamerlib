# Android DJI WebRTC Video Streaming Library

**Management Summary**:

Forget about RTMP!

Make a DJI drone a **real** real-time video streamer utilizing WebRTC!

## Documentation, history and API description

[Available here](https://github.com/neilyoung/djistreamerlib/wiki)

## Code and current version

Available at JFrog Artifactory:

```bash
implementation 'com.decades.android:djistreamerlib:1.4.0'
```

[Version History](https://github.com/neilyoung/djistreamerlib/wiki/Version-history)

Because of the new hosting at JFrog Artifactory here needs to be be an additional adaptation applied in your project's build.gradle (the one in the project's root) in order to help the Gradle build system to find the new library:

```bash
buildscript {
    ...
    dependencies {
        classpath "org.jfrog.buildinfo:build-info-extractor-gradle:4.13.0"
    }
}
allprojects {
    repositories {
        ...
        maven {
            url "https://decades.jfrog.io/artifactory/djistreamerlib/"
        }
    }
    apply plugin: "com.jfrog.artifactory"
}

```

## Sample app

[Available here](https://github.com/neilyoung/android-videostreamdecodingsample-webrtc)
