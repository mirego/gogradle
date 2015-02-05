# gogradle
Contains some useful gradle scripts.

Increment version script
-----------
```
plugins {
  id 'com.kageiit.url-cache' version '1.0.0'
}

apply plugin: 'com.kageiit.url-cache'
apply from: urlCache.get("https://raw.githubusercontent.com/mirego/gogradle/master/increment.gradle")
```
