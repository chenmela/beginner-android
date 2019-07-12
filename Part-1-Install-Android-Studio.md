# Install Android Studio

Fortunately, Google Codelabs (a great resource for hands-on learning about Google technologies) provides a great Java installation guide. Head over to [their guide](https://codelabs.developers.google.com/codelabs/build-your-first-android-app/#1) and follow it until the end. Below, we include some helpful clarification about a few subsections in the guide.

## Objectives
In Part 1, you will learn to:
- Install Java and set JAVA\_HOME environment variable
- Install Android Studio

## Install the Java Development Kit

If you get an error message that says something like `java: command not found` when you type `java -version`, this means you do not have Java installed. You should continue with Java installation.

## Set JAVA\_HOME
You need to set the environment variable called "JAVA\_HOME" in order for future programs to know where your installation of Java is located on your computer. 

For Mac and Linux users, first determine the configuration file for your particular shell. For example, you will want to edit ~/.bash\_profile if you're using the Bash shell (NOTE: Editing ~/.bashrc is very similar, but the recommendation is to edit ~/.bash\_profile for setting environment variables. See [this](https://superuser.com/questions/409186/environment-variables-in-bash-profile-or-bashrc) if you're interested). 

Next, add the lines specified [here](https://docs.oracle.com/cd/E19182-01/820-7851/inst_cli_jdk_javahome_t/) for your particular shell to that configuration file. "jdk-install-dir" should be replaced by the path to Java via your JDK install. For example, you will use `/usr/lib/jvm/jdk-12.0.1` if you installed JDK 12 at this location (NOTE: This is the default location for Linux). Then restart your shell for the changes to take effect.

## Install Android Studio
Continue to the [Android Studio website](https://developer.android.com/studio/) like the Codelab suggests and follow the instructions there.

If you're installing Android Studio on Linux and you encounter a "Permission denied" message while trying to manipulate files within the /usr/local directory, you can preface your terminal commands with `sudo` (read more [here](https://en.wikipedia.org/wiki/Sudo)).

# Additional Resources
If you're still stuck, try searching specific error messages on [Stack Overflow](https://stackoverflow.com/).

