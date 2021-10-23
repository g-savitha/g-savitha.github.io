---
title: "Android Basics"
date: 2021-10-17T15:34:26+05:30
draft: false
tags: [android-config, views, layouts]
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

# Config

- [Android Virtual Device (AVD) manager](developer.android.com/tools/devices/managing-avds.html) : Used to create an emulator. You will find it in `Tools > AVD Manager`

# Layouts

## TextView

- Each of the elements on screen is called **View**
  > The Views in an Android app don't just float on the screen by themselves. Views have relationships to each other. For example, an image may be next to some text, and buttons may form a row. To organize Views, you put them in a container. A **ViewGroup** is a container that View objects can sit in, and is responsible for arranging the Views inside it. The arrangement, or layout, can change depending on the size and aspect ratio of the screen of the Android device that the app is running on, and the layout can adapt to whether the device is in portrait or landscape mode. - Android Documentation
- **ConstraintLayout** is a _ViewGroup_ which helps you arrange the Views inside it in a flexible way.
- [Layout Editor](https://developer.android.com/studio/write/layout-editor)
- Views need to be constrained horizontally and vertically within a ConstraintLayout.
- One way to _position a View_ is with a **margin**
  - A margin says how far a View is from an edge of the container it's in.
  - Eg: While positioning the text view, _margin_ is the distance from the _TextView_ to the edge of the container, the _ConstraintLayout_
  - The unit for margins and other distances in the UI is _density-independent pixels (dp)_
    > **Note:** Just like dp is a unit of measure for distances on the screen, _sp is a unit of measure for the font size_. UI elements in Android apps use two different units of measurement, **density-independent pixels (dp)** which you used earlier for the layout, and **scalable pixels (sp)** which is used when setting the size of text. By default,_sp is the same size as dp, but it resizes based on the user's preferred text size._ - Android documentation
- You can set attributes on a TextView like the font, text size, and color.

## ImageView

### Importing images in android studio.

- In Android Studio, click on _View > Tool Windows > Resource Manager_ in the menus or click on the Resource Manager tab to the left of the Project window.
  - Click the _+ below Resource Manager_, and _select Import Drawables_. This opens a file browser.
  - In the file browser find the image file you downloaded and click Open.
  - Click Next. Android Studio shows you a preview of the image.
  - Click Import.
- If the image has been imported successfully, Android Studio adds the image to your _Drawable_ list.
- Go to _Project View_ of your app. Confirm the **image is in the drawable folder** by expanding _app > res > drawable._

> **Note:** Note: A constraint in the context of the Layout Editor represents a connection or alignment of a view to another view, the parent layout, or an invisible guideline. For example, a view can be constrained to be a certain distance from the edge of its container, or always be to the right of another view, or always the top view inside a container. - Android documentation

- Size and align the image on screen using [ScaleType](https://developer.android.com/reference/kotlin/android/widget/ImageView.ScaleType)

- Order of the views matters most on ther screen

## Translating

- When you write apps, it's important to remember that they may be translated into another language at some point. A hardcoded string is one that is written directly in the code of your app. Hardcoded strings make it more difficult to translate your app into other languages, and harder to reuse a string in different places in your app. You can deal with those issues by _"extracting strings into a resource file"_ . That means instead of hardcoding the string in your code, you put the string into a file, give it a name, and then use the name whenever you want to use this string. The name will stay the same, even if you change the string or translate it to a different language.

- Your extracted strings are stored in _(app > res > values > strings.xml)_. The strings.xml file has a list of strings that the user will see in your app. Note that the name of your app is also a string resource. By putting the strings all in one place, you can more easily translate all the text in your app, and more easily reuse a string in different parts of your app.

## Accessibility

---

For more info Refer :

- [Android vocab - kotlin](https://developer.android.com/courses/android-basics-kotlin/android-basics-kotlin-vocab)
- [dp vs. sp](https://developer.android.com/training/multiscreen/screendensities)
- [View](https://developer.android.com/reference/android/view/View)
- [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView)
- [ConstraintLayout](https://developer.android.com/reference/androidx/constraintlayout/widget/ConstraintLayout)
