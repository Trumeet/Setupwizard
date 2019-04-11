# SetupWizardLib

[SetupWizardLib](http://androidxref.com/9.0.0_r3/xref/frameworks/opt/setupwizard/) is a library in AOSP, it provides a beautiful UI for setup wizards. It can be used for not only platform apps, but also third-party apps, but it isn't published to maven.

# The difference between this repo and Google's

Our purpose is to publish it to maven so third-party app developers can use it easily. Everything I've modified is marked as:
```
// XXX by Trumeet@GitHub: xxx (The description of the modification)
```

## Main modifications

The most import modify is to make it compilable in Android Studio. I've also removed `platform` mode because it's useless for third-party apps.

You can discover my changes by searching the comments.

# How to use

## 0x00 Add maven repo

Follow the instructions in [maven.yuuta.dev](https://maven.yuuta.dev) to add the repo.

## 0x01 Implement dependencies

```grooxy
dependencies {
    def swVer = '9r9-15'
    implementation "moe.yuuta.setupwizard:library:$swVer"
    implementation "moe.yuuta.setupwizard:navigationbar:$swVer"
}
```

### A notice about version

The version of libraries include the branch name and build number. For instance, version `9r9-10` means it is from branch `9r9` and is the 10th build.

The branch name is the shorten form of AOSP branch name. `9r9` represents `android-9.0.0_r9`. Anyway, always check the latest version of library from [maven](https://github.com/Trumeet/Maven/tree/master/moe/yuuta/setupwizard/library).

# Compatibility

It should work on API 21+, but **SHOULDN'T** work below lollipop. (I'm not tested enough because of some errors, lol)

# License

It has the same license with AOSP.
