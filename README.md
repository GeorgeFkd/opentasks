[![Build Status](https://travis-ci.org/dmfs/opentasks.svg?branch=master)](https://travis-ci.org/dmfs/opentasks)
# OpenTasks

__An Open Source Task App for Android__

This is a task app for Android.

## Migrating OpenTasks to newer android SDK and tooling

Steps that I carried out in order to make it compile on java21.

- Change the gradle version to 8.11.1 in the gradle-wrapper.properties file
- Upgrade versions for android libraries in gradle files
- Remove unsupported things from gradle files(e.g. jcenter repositories)
- Changed things in gradle files to comply with newer versions
- Remove from Android Manifests the package namespace and instead put it in each module's build.gradle
- Add an android:exported="true" for activities as it has to be declared whether they are used elsewhere or not
- Change property accesses from R.thing.value to org.dmfs.tasks.theme.R.thing.value
- Changes to code itself and not xml files were minimal(probably only one such case).
- Testing currently does not work but will be fixed

## Requirements

* Android SDK Level 8(Currently compiled for android 14, api level 34)
* [android-xml-magic 0.1.1](https://github.com/dmfs/android-xml-magic)
* [Color Picker](https://github.com/dmfs/color-picker)
* [Dashclock 2.0](https://github.com/romannurik/dashclock/)
* [Retention Magic 1.2.2](https://github.com/dmfs/retention-magic)
* [Task Provider 1.1.8.1](https://github.com/dmfs/task-provider)
* [xmlobject 0.4.2](https://github.com/dmfs/xmlobjects)

## TODO:

* add support for recurrence
* add support for extended attributes like alarms, attendees and categories
* add sortings and filters
* ...

## Download

For people that want to compile it themselves and download it,
<a href="https://f-droid.org/packages/org.dmfs.tasks/" target="_blank">
<img src="https://f-droid.org/badge/get-it-on.png" alt="Get it on F-Droid" height="100"/></a>
<a href="https://play.google.com/store/apps/details?id=org.dmfs.tasks" target="_blank">
<img src="https://play.google.com/intl/en_us/badges/images/generic/en-play-badge.png" alt="Get it on Google Play" height="100"/></a>

## License

Copyright (c) Marten Gajda 2013-2015, licensed under Apache2.
