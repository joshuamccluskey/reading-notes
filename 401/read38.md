# Intent Filters

## Read 38

### Joshua McCluskey


### Intent Filter

#### Add an Intent
- In order to allow other apps to use your activities you need to add an intent filter element to the manifest portion for that activity.
- For example you need to send a photo, your app will show up as an option to send the photo.
- When the app is intstalled, your device will find intents that can respond to the intent'
- `<action>` element to specify the action in the intent filter
- `<data>` specify MIME type, just a URI prefix, just a URI scheme, or a combination of these and others that indicate the data type accepted
- `<category>` this usually related to users gestures or location
- example:
````XML
    <activity android:name="ShareActivity">
    <intent-filter>
        <action android:name="android.intent.action.SEND"/>
        <category android:name="android.intent.category.DEFAULT"/>
        <data android:mimeType="text/plain"/>
        <data android:mimeType="image/*"/>
    </intent-filter>
</activity>
````
- [credit](https://developer.android.com/training/basics/intents/filters)

#### Handle the Intent in Your Activity

- Figuring out what intent to use for the activity example
````Java
@Override
protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);

        setContentView(R.layout.main);

        // Get the intent that started this activity
        Intent intent = getIntent();
        Uri data = intent.getData();

        // Figure out what to do based on the intent type
        if (intent.getType().indexOf("image/") != -1) {
        // Handle intents with image data ...
        } else if (intent.getType().equals("text/plain")) {
        // Handle intents with text ...
        }
        }
````

- [credit](https://developer.android.com/training/basics/intents/filters)

- Returning a result you can specify the result 
````Java
// Create intent to deliver some kind of result data
Intent result = new Intent("com.example.RESULT_ACTION", Uri.parse("content://result_uri"));
setResult(Activity.RESULT_OK, result);
finish();
````
- [credit](https://developer.android.com/training/basics/intents/filters




#### Reading

- [Allowing Other Apps to Start Your Activity](https://developer.android.com/training/basics/intents/filters)


[<=== Back](../README.md)