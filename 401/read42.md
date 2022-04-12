# Monetization and AdMob Ads

## Read 42

### Joshua McCluskey

#### AdMob

- Google's platform to monetize your app to generate revenue
- You can show millions of ads with Google AdMob
- You have the ability to scale fast
- Create an Admob account
- AdMob gains insights on users to to maximize ad revenue.

```` gradle

// Place this in the project level of build.gradle
buildscript {
    repositories {
        google()
        mavenCentral()
    }
}

allprojects {
    repositories {
        google()
        mavenCentral()
    }
}

// Place this in the app level build. gradle
dependencies {
  implementation 'com.google.android.gms:play-services-ads:20.6.0'
}
````
- Update you rApp Manifest
- Make sure to add your AdMob App ID

````xml
<manifest>
    <application>
        <!-- Sample AdMob app ID: ca-app-pub-3940256099942544~3347511713 -->
        <meta-data
            android:name="com.google.android.gms.ads.APPLICATION_ID"
            android:value="ca-app-pub-xxxxxxxxxxxxxxxx~yyyyyyyyyy"/>
    </application>
</manifest>

````
- Initialize in Main Activity

````Java
 MobileAds.initialize(this, new OnInitializationCompleteListener() {
            @Override
            public void onInitializationComplete(InitializationStatus initializationStatus) {
            }
        });
````
- [Credit](https://developers.google.com/admob/android/quick-start)

- Pick your add format and you should be good to go
#### Things I want to learn more about

#### Reading

- [AdMob](https://developers.google.com/admob/android/quick-start)


[<=== Back](../README.md)