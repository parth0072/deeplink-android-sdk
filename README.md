# Deeplink Android SDK

Binary AAR distribution for the Deeplink Android SDK. Source code lives in [deeplink_sdk](https://github.com/parth0072/deeplink_sdk).

## Installation

### Download

Download the latest `deeplink-sdk.aar` from [Releases](https://github.com/parth0072/deeplink-android-sdk/releases) and add it to your project:

1. Copy `deeplink-sdk.aar` into `app/libs/`
2. In `app/build.gradle`:

```groovy
dependencies {
    implementation files('libs/deeplink-sdk.aar')
    implementation 'com.android.installreferrer:installreferrer:2.2'
}
```

## Requirements

- Android API 21+
- Kotlin or Java project

## Usage

```kotlin
import com.deeplink.sdk.Deeplink

// In Application.onCreate() or Activity.onCreate()
Deeplink.configure(this, apiKey = "your-api-key", domain = "dl.yourapp.com")

// Deferred deep link on first launch
Deeplink.getInitData(this) { data ->
    data?.let { navigateTo(it.destinationUrl) }
}
```
