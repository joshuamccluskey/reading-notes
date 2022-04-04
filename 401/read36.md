# Cognito
## Read 35

### Joshua McCluskey


#### Authentication

- Amazon Amplify  comes with the Amazon Cognito for authentication
- Cognito is supposed to be quick and easy to set up authentication for your app
- You can set up social log in
- It supports OAuth 2.0, SAML 2.0 and Open ID connect
- You can implement the following to get it set up
- You start with the CLI and inputting `amplify add auth`
- add the dependencies 
- Cognito is in  compliance with security and compliance to laws on personal information
````Java
dependencies {
    implementation 'com.amplifyframework:aws-auth-cognito:1.33.0'
}
//////////////////////////////// Initalize
// Add this line, to include the Auth plugin.
Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.configure(getApplicationContext());
//////////////////////////////// auth session
Amplify.Auth.fetchAuthSession(
    result -> Log.i("AmplifyQuickstart", result.toString()),
    error -> Log.e("AmplifyQuickstart", error.toString())
);
````
- [Credit](https://docs.amplify.aws/lib/auth/getting-started/q/platform/android/)



### Things I want to know more about

- I want to learn more about SAML and how to incorporate it.

#### Reading

- [Amazon Cognito](https://docs.amplify.aws/lib/auth/getting-started/q/platform/android/)



[<=== Back](../README.md)