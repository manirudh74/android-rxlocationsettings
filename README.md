Android-RxLocationSettings
==========================

[![JitPack](https://jitpack.io/v/jetradarmobile/android-rxlocationsettings.svg)](https://jitpack.io/#jetradarmobile/android-rxlocationsettings)
[![API](https://img.shields.io/badge/API-14%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=14)

An easy way to check the settings before requesting location using RxJava.

![image](https://raw.githubusercontent.com/JetradarMobile/android-rxlocationsettings/master/art/rxlocationsettings.png)


Compatibility
-------------

This library is compatible from API 14 (Android 4.0).


Download
--------

Add it in your root build.gradle at the end of repositories:

```groovy
allprojects {
    repositories {
        ...
        maven { url "https://jitpack.io" }
    }
}
```

Add the dependency

```groovy
dependencies {
    compile 'com.github.jetradarmobile:android-rxlocationsettings:1.0.0'
}
```


Usage
-----

Default implementation with round snowflakes:

```java
LocationSettingsRequest locationSettingsRequest = new LocationSettingsRequest.Builder()
    .addLocationRequest(LocationRequest.create().setPriority(LocationRequest.PRIORITY_HIGH_ACCURACY))
    .build();
RxLocationSettings.with(this).checkLocationSettings(locationSettingsRequest)
    .subscribe(resolved -> ...);
```


Credits
-------

This library was inspired by [RxPermissions](https://github.com/tbruyelle/RxPermissions).


License
-------

    Copyright 2017 JetRadar

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.