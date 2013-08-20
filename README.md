SwipeListView ([Play Store Demo][1])
=============

An Android List View implementation with support for drawable cells and many other swipe related features.

- [Introduction](#introduction)
- [Download](#download)
  - [Maven Dependency](#maven-dependency)
	- [APKLib and others](#apklib-and-others)
	- [Dependencies](#dependencies)
- [Using the standalone SwipeListView JAR](#using-the-standalone-swipelistview-jar)
- [Demo](#demo)
- [XML Usage](#xml-usage)
- [License](#license)
 
Click to watch video

[![SwipeListView screenshot][6]][7]

# Introduction

SwipeListView was born out of the need to add swipe gestures to ListView on Android for 
@ [47 Degrees][4] Clients. Contributions and constructive feedback are welcome.

# Download

## Maven Dependency

SwipeListView may be automatically imported into your project if you already use [Maven](http://maven.apache.org/). 
Just declare android-swipelistview as a maven dependency.
If you wish to always use the latest unstable snapshots, add the Sonatype repository where the SwipeListView 
snapshot artifacts are being deployed.
SwipeListView official releases will be made available at Maven Central.

```xml
<repository>
    <id>sonatype</id>
    <url>https://oss.sonatype.org/content/groups/public/</url>
    <releases>
        <enabled>true</enabled>
        <updatePolicy>daily</updatePolicy>
        <checksumPolicy>fail</checksumPolicy>
    </releases>
    <snapshots>
        <enabled>true</enabled>
        <updatePolicy>always</updatePolicy>
        <checksumPolicy>ignore</checksumPolicy>
    </snapshots>
</repository>

<dependency>
    <groupId>com.fortysevendeg.android</groupId>
    <artifactId>swipelistview</artifactId>
    <version>1.0-SNAPSHOT</version>
    <type>apklib</type>
</dependency>
```
## APKLib and others

You can get the releases, snapshots and other forms in which SwipeListView is distributed from the Maven sonatype Repository here
[Downloads][5].

## Dependencies

SwipeListView depends on the following libraries.

- com.nineoldandroids 

SwipeListView expects that you include one of the Google Android [compatibility libraries][3] in order to use Loaders in versions that do not support them natively.
Depending on your requirements you may choose to include one of the following...

- com.google.android :
    - support-v4 (Available in Maven Central)

# Using the standalone SwipeListView JAR

If you manually include the single SwipeListView jar [swipelistview-1.0-SNAPSHOT.jar][5] in your libs/ folder you would also have to add the following dependencies:

- [nineoldandroids-2.4.0.jar][8]
- android-support-v4

You'd have to provide also the [attrs.xml][9] inside your directory "res/values" so the attributes are properly picked up by the runtime.

We do discourage people from manually adding the jars and recomend following the maven or apklib aproach to include SwipeListView library in your own project.

# Demo

You can see a demo SwipeListView in action at [android-swipelistview-sample][2] or install it from [Google Play][1]


# XML Usage

If you decide to use SwipeListView as a view, you can define it in your xml layout like this:

```xml
    <com.fortysevendeg.swipelistview.SwipeListView
            xmlns:swipe="http://schemas.android.com/apk/res-auto"
            android:id="@+id/example_lv_list"
            android:listSelector="#00000000"
            android:layout_width="fill_parent"
            android:layout_height="wrap_content"
            swipe:swipeFrontView="@+id/front"
            swipe:swipeBackView="@+id/back"
            swipe:swipeActionLeft="[reveal | dismiss]"
            swipe:swipeActionRight="[reveal | dismiss]"
            swipe:swipeMode="[none | both | right | left]"
            swipe:swipeCloseAllItemsWhenMoveList="[true | false]"
            swipe:swipeOpenOnLongPress="[true | false]"
            swipe:swipeAnimationTime="[miliseconds]"
            swipe:swipeOffsetLeft="[dimension]"
            swipe:swipeOffsetRight="[dimension]"
            />
```

* `swipeFrontView` - **Required** - front view id.
* `swipeBackView` - **Required** - back view id.
* `swipeActionLeft` - Optional - left swipe action Default: 'reveal'
* `swipeActionRight` - Optional - right swipe action Default: 'reveal'
* `swipeMode` - Gestures to enable or 'none'. Default: 'both'
* `swipeCloseAllItemsWhenMoveList` - Close revealed items on list motion. Default: 'true'
* `swipeOpenOnLongPress` - Reveal on long press Default: 'true'
* `swipeAnimationTime` - item drop animation time. Default: android configuration
* `swipeOffsetLeft` - left offset
* `swipeOffsetRight` - right offset

# Continuous Integration

CI and Artifact Repository hosted in ClinkerHQ.com 

[![ClinkerHQ][10]][11]

# License

Copyright (C) 2012 47 Degrees, LLC
http://47deg.com
hello@47deg.com

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

     http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

[1]: https://play.google.com/store/apps/details?id=com.fortysevendeg.android.swipelistview
[2]: https://github.com/47deg/android-swipelistview-sample
[3]: http://developer.android.com/intl/es/tools/extras/support-library.html
[4]: http://47deg.com
[5]: https://oss.sonatype.org/content/groups/public/com/fortysevendeg/android/swipelistview/1.0-SNAPSHOT/
[6]: https://raw.github.com/47deg/android-swipelistview-sample/master/screenshot_swipelistview_small.png
[7]: https://www.youtube.com/watch?v=E0352OH488M
[8]: https://github.com/JakeWharton/NineOldAndroids/downloads
[9]: https://github.com/47deg/android-swipelistview/tree/master/res/values
[10]: http://dl.clinkerhq.com/assets/badge/clinker-badge_125x125.png
[11]: http://clinkerhq.com

