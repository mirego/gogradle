# gogradle
Contains some useful gradle scripts.

Increment version script
-----------

This script increments the version when the switch -PincrementVersion=true is passed.

First, you must create a version.properties file with the initial version. Second you need to insert this into your gradle build script. The script will work even offline if you executed it online at least once.

```
plugins {
  id 'com.kageiit.url-cache' version '1.0.0'
}

apply plugin: 'com.kageiit.url-cache'
apply from: urlCache.get("https://raw.githubusercontent.com/mirego/gogradle/master/increment.gradle")

...

android {
  ...
  defaultConfig {
  ...
    versionCode = getStoredVersionCode(project)
  }
}

```
