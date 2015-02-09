[![Build Status][12]][13]

THIS PROJECT IS DISCONTINUED — USE AT YOUR OWN RISK

It has been a fun and great project but it's time for us to move on. Check out our recent work that we are doing with Scala on Android. http://47deg.github.io/translate-bubble-android/ and follow us on Github and Twitter for new and exciting open source projects. Thanks for your continuing support. If you wish to take on maintenance of this library please contact us through the issue tracker.

SwipeListView ([Play Store Demo][1])
=============

An Android List View implementation with support for drawable cells and many other swipe related features.

We are actively seeking help from People that want to contribute to this OS project. Please open an issue indicating you want to help out. Thanks!

- [Introduction](#introduction)
- [Download](#download)
- [Demo](#demo)
- [XML Usage](#xml-usage)
- [License](#license)
 
Click to watch video

[![SwipeListView screenshot][6]][7]

# Introduction

SwipeListView was born out of the need to add swipe gestures to ListView on Android for 
@ [47 Degrees][4] Clients. Contributions and constructive feedback are welcome.

# Download

*Gradle*

```groovy

repositories {
        maven { url 'http://clinker.47deg.com/nexus/content/groups/public' }
}

dependencies {
    compile ('com.fortysevendeg.swipelistview:swipelistview:1.0-SNAPSHOT@aar') {
        transitive = true
    }
}

```

# Demo

You can see a demo SwipeListView in action on Google Play [Google Play][1]


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
[12]: https://clinker.47deg.com/desktop/plugin/public/status/android-swipelistview
[13]: https://clinker.47deg.com/jenkins/job/android-swipelistview/
