# DeeplinkSDK Android — Pre-built AAR

Download `deeplink-sdk.aar` from the [GitHub Releases](https://github.com/parth0072/deeplink-android-sdk/releases) page
and copy it into this `libs/` folder.

## Integration

In your app's `build.gradle`:
```groovy
dependencies {
    implementation files('libs/deeplink-sdk.aar')
    implementation 'com.android.installreferrer:installreferrer:2.2'
}
```
