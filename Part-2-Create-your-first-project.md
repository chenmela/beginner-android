# Create your first project

Let's dive in and create our first project in Android Studio!

Again, Google Codelabs provides a great Android Studio setup guide. Head over to [their guide](https://codelabs.developers.google.com/codelabs/build-your-first-android-app/#2) and follow it until the end. Below, we include some helpful clarification about a few sections in the guide.

## Objectives
In Part 2, you will learn:
- How to create an Android Studio project
- How to navigate Android Studio
- How to create a virtual device (emulator)
- How to run your app on an emulator
- How to run your app on a physical device (optional)

## Create a new project
You may have to click through some default settings and choose your color scheme before getting to the dialogue used in the guide.

On the "Choose your project" screen, you will choose an "Empty Activity." But what exactly is an Activity? For now, remember that an activity represents a single screen with a user interface. Activties typically correspond to one screen in a multi-screen app. On the top panel, you can also choose corresponding templates for different sorts of devices. This is one of the awesome features of working within Android Studio!

In the application's Name field, you can rename it to something meaningful. We'll be creating a number generator app in this workshop, so you can call it NumberGenerator.

The package name is a unique identifier that makes your application eligible for publication on the Google Play Store. Since you likely will not be publishing this example, leave this package name as is (com.example.todolist).

Change language to Java. Although we will be using Java in this workshop, Google announced in 2017 that its official language for Android development is Kotlin. One of the main advantages of using Kotlin is that it reduces a lot of boilerplate and otherwise verbose code that Java requires, making it easier to write callbacks, data classes, and getters/setters. For more information on developing Android apps in Kotlin, check out this free [Udacity tutorial developed by Google](https://www.udacity.com/course/developing-android-apps-with-kotlin--ud9012).

On this screen, you can also see the minimum API level, which you can leave as is. Each new API level introduces new features that can be used in an Android application. Supporting smaller - and thus, older - API levels can make developing an app more complicated. Or you may want to use a feature that is only available from a particular API level onwards. In both cases, it's helpful to specify a minimum API level that is needed by a device in order to run your application properly.

## Explore the project structure and layout
Android Studio is an IDE (Integrated Development Environment). Any good IDE incorporates a text editor for you to write code as well as a bunch of other tools (like a virtual device and debugging functionality) that will speed up your development process.

The guide incorporates a lot of helpful information in this section.

## Create a virtual device (emulator)
In order to test your app, you will want to create an emulator. This is essentially a fake version of an Android device that behaves just like a real device, except you can only interact with it through your computer. This is very helpful if you don't have access to a physical Android device for development.

Follow the instructions in the guide.

At one point, you will likely have to download an image file (or a virtual hard disk) for a particular API level. This provides the fundamental setup for a virtual machine, on which the emulator runs.

Once the download is complete, select the image you just installed and click Next, then Finish.

Play around with the emulator a bit to get a feel for the Android device you're using. Notice that your input is hooked up to your computer keyboard and you can access almost everything like normal, including the Internet.

If you get errors associated with the adb server, it is likely that you need to wipe the settings of the emulator before using it. Check out this [post on Stack Overflow](https://stackoverflow.com/questions/46898322/emulator-5554-unauthorized-for-adb-devices) for the steps to resolve such an issue.

Before moving on, make sure you are able to see your ToDoList app (which should launch automatically - if it doesn't, navigate to the main Android menu and click on it). Congratulations, you're all set up to start running code on your Android emulator in Android Studio!

