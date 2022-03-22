# Intents, Activities, and SharedPreferences

## Read 27

### Joshua McCluskey

### Tasks and the back stack
- A task is a collection of activities for User interaction
- The activities are arranged in a stack
- Tasks are performed in the LIFO structure of the Stack
- When the user clicks on an app
- That activity goes into the stack the most  current activity goes on the stack
- Tasks can move from the foreground and the background
- Multiple activity instances can be pushed on the stack even if it was previously on the stack
- Android 7 and above manage each windo seperately
- When adding to the manifest file you can specify the how it associates with other tasks
- You can use `Intent` flags when you associate tasks with startAcitivity
- `launchMode` can have an attribute specify it
- An affinty indicates which task an activty prefers to belong
- Clearing the backstack happens when users abandoned a task for an extended period of time


````Java
activity ... >
    <intent-filter ... >
        <action android:name="android.intent.action.MAIN" />
        <category android:name="android.intent.category.LAUNCHER" />
    </intent-filter>
    ...
</activity>

````
- [Credit](https://developer.android.com/guide/components/activities/tasks-and-back-stack)

- Basically in the context of the go back to another page push pop stack
- Swipe app up you are putting that stack in the foreground and going onto anopther activity puts it in background

### Sace key-value data

- SharedPerferences APIs are for key values that you want to save

#### Get Handle to shared preferences
````Java
Context context = getActivity();
SharedPreferences sharedPref = context.getSharedPreferences(
        getString(R.string.preference_file_key), Context.MODE_PRIVATE);

//alt

        SharedPreferences sharedPref = getActivity().getPreferences(Context.MODE_PRIVATE);
````
- [Credit](https://developer.android.com/training/data-storage/shared-preferences)

#### Write to shared preferences
````Java
SharedPreferences sharedPref = getActivity().getPreferences(Context.MODE_PRIVATE);
SharedPreferences.Editor editor = sharedPref.edit();
editor.putInt(getString(R.string.saved_high_score_key), newHighScore);
editor.apply();
````
- [Credit](https://developer.android.com/training/data-storage/shared-preferences)

#### Read from shared preferences
````Java
SharedPreferences sharedPref = getActivity().getPreferences(Context.MODE_PRIVATE);
int defaultValue = getResources().getInteger(R.integer.saved_high_score_default_key);
int highScore = sharedPref.getInt(getString(R.string.saved_high_score_key), defaultValue);
````
- [Credit](https://developer.android.com/training/data-storage/shared-preferences)
#### Reading

[Tasks and the back stack ](https://developer.android.com/guide/components/activities/tasks-and-back-stack)
[Save key-value data](https://developer.android.com/training/data-storage/shared-preferences)

[<=== Back](../README.md)