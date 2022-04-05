# Amazon S3

## Read 37

### Joshua McCluskey


#### Amazon S3

- Storage service
- Overall, a way to save costs on storage costs.
- S3 inteeligent tieering will optimize your storage for lower costs
- S3 Lifecycle A place to store your object for their life cycle
- S3 Object Lock are objkects that can't be updated or deleted
- S# Replication replicate your objects in destination buckets or AWS region
- S3 Batch Operations  for large scaled operations
- Amazon S3 provides access management services
- Data processing services

#### Key parts of S3

- Buckets
- Objects
- Keys
- S3 Versioning
- Version ID
- Bucket Policy
- S3 Access Points
- Access control lists
- Regions

#### Overview of S3 parts

- Buckets are containers for objects. You can store as many objects as needed with 100 buckets per account
    - You can request an increase of buckets if needed
- Objects are entities stored in S3. Stored in bucket by Key  and verion ID
- Keys are unique identifiers for objects in buckets
- S3 versioning allows you to keep several versions of the same object in a bucket
- Version ID are unique to version of the object
- AWS IAM policy that grants access and permission to buckets and the bucket owner can set the policy
- S3 Access Points are like object operations doing GetObject or PutObjects

#### Pricing

- AWS S3 only charges you for what you use pay as you go model.


#### Getting Started

````Java
amplify add storage

//////////////////////////////Choose Defaults

        amplify push

///////////////////////////Dependencies
        dependencies {
        implementation 'com.amplifyframework:aws-storage-s3:1.34.0'
        implementation 'com.amplifyframework:aws-auth-cognito:1.34.0'
        }
        ///////////////////////////////////
//Initialize
//PlugIns
        Amplify.addPlugin(new AWSCognitoAuthPlugin());
        Amplify.addPlugin(new AWSS3StoragePlugin());
        
        ///////////////////////////
// Uploading Data Bucket

private void uploadFile() {
        File exampleFile = new File(getApplicationContext().getFilesDir(), "ExampleKey");

        try {
        BufferedWriter writer = new BufferedWriter(new FileWriter(exampleFile));
        writer.append("Example file contents");
        writer.close();
        } catch (Exception exception) {
        Log.e("MyAmplifyApp", "Upload failed", exception);
        }

        Amplify.Storage.uploadFile(
        "ExampleKey",
        exampleFile,
        result -> Log.i("MyAmplifyApp", "Successfully uploaded: " + result.getKey()),
        storageFailure -> Log.e("MyAmplifyApp", "Upload failed", storageFailure)
        );
        }


````
- [Credit](https://docs.amplify.aws/lib/storage/getting-started/q/platform/android/#provision-backend-storage)




#### Reading

- [What is Amazon S3?](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html#S3Features)
- [Getting Started](https://docs.amplify.aws/lib/storage/getting-started/q/platform/android/#provision-backend-storage)


[<=== Back](../README.md)