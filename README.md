# SetupWizardLib

[SetupWizardLib](http://androidxref.com/9.0.0_r3/xref/frameworks/opt/setupwizard/) is a library in AOSP, it provides a beautiful UI for setup wizards. It can be used for not only platform apps, but also third-party apps, but it isn't published to maven.

# The difference between this repo and Google's

Our purpose is to publish it to maven so third-party app developers can use it easily. Everything I've modified is marked as:
```
// Changed by Trumeet@GitHub: xxx (The description of the modification)
```

## Main modifications

The most import modify is to make it compilable in Android Studio. I've also removed `platform` mode because it's useless for third-party apps.

You can discover my changes by searching the comments.

# How to use

Just add it to your module:
```grooxy
dependencies {
    implementation fileTree(dir: 'libs', include: ['*.jar'])
    implementation project(':library')
    implementation project(':navigationbar')
}
```

# Compatibility

It should work on API 21+, but **SHOULDN'T** work below lollipop. (I'm not tested enough because of some errors, lol)

# License

It has the same license with AOSP.
