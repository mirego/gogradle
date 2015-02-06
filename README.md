# gogradle
Contains some useful gradle scripts.

Increment version script
-----------

This script increments the version when the switch -PincrementVersion=true is passed.

You need to insert this into your gradle build script. The script will work even offline if you executed it online at least once.

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


## License

`gogradle` is © 2013-2015 [Mirego](http://www.mirego.com) and may be freely distributed under the [New BSD license](http://opensource.org/licenses/BSD-3-Clause).  See the [`LICENSE.md`](https://github.com/mirego/gogradle/blob/master/LICENSE.md) file.

## About Mirego

[Mirego](http://mirego.com) is a team of passionate people who believe that work is a place where you can innovate and have fun. We’re a team of [talented people](http://life.mirego.com) who imagine and build beautiful Web and mobile applications. We come together to share ideas and [change the world](http://mirego.org).

We also [love open-source software](http://open.mirego.com) and we try to give back to the community as much as we can.