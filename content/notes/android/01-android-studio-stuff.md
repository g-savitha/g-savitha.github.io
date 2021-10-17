---
title: "Android Studio Stuff"
date: 2021-10-17T15:34:26+05:30
draft: false
tags: [android-config]
categories: [android]
sources: [https://developer.android.com/]
---

<!--

::Annotation Guide::
~~~~~~~~~~~~~~~~~~~~

* `em` is the modifier

1. em (_text_) - blue underline
2. strong (**text**) - yelow highlight
3. del (~~text~~) - red strike-through

4. em > em (_*text*_) - blue circle
5. em > strong (_**text**_) - lawngreen box
6. em > del (_~~text~~_) - red cross-off
-->

1. [Android Virtual Device (AVD) manager](developer.android.com/tools/devices/managing-avds.html) : Used to create an emulator. You will find it in `Tools > AVD Manager`
2. Each of the elements on screen is called **View**
   > The Views in an Android app don't just float on the screen by themselves. Views have relationships to each other. For example, an image may be next to some text, and buttons may form a row. To organize Views, you put them in a container. A **ViewGroup** is a container that View objects can sit in, and is responsible for arranging the Views inside it. The arrangement, or layout, can change depending on the size and aspect ratio of the screen of the Android device that the app is running on, and the layout can adapt to whether the device is in portrait or landscape mode. - Android Documentation
3. **ConstraintLayout** is a _ViewGroup_ which helps you arrange the Views inside it in a flexible way.

---

For more info Refer : [Android vocab - kotlin](https://developer.android.com/courses/android-basics-kotlin/android-basics-kotlin-vocab)
