# Android-EPGView
Android library to display EPG view

[![](https://jitpack.io/v/diareuse/Android-EPGView.svg)](https://jitpack.io/#diareuse/Android-EPGView)

### Gradle Import

```
allprojects {
  repositories {
    ...
    maven { url 'https://jitpack.io' }
  }
}
```

```jsx
implementation 'com.github.diareuse:Android-EPGView:x.y.z'
```

### Usage

Pretty much the same as regular old ListView

1) Extend adapter [EPGAdapter<Channel, Program>](https://github.com/diareuse/Android-EPGView/blob/master/epg-view/src/main/java/com/sgerges/epgview/core/EPGAdapter.java)
  * Provide views for Channel, Program, Time cell (up top ^^) and header that moves with time
  * Then fetch program starts and ends via `getProgramAt(section, position)`
  * Then fetch start and end time of your epg from virtually anywhere you want

2) OnCreate set that adapter to your view that you obviously implemented before

3) Fetch your data and set it to your adapter
  * Friendly reminder, don't forget to call `view.notifyDataSetChanged()` on your view :)
  
4) That's it x)

### Kotlin

Yes, interoperable, but misses nullability annotations so don't expect anything fancy. Most crashes have been cleared from original version. If you were to find any, create a pull request, I will build a new version for you from jitpack right away ;)
