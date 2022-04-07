# Location

## Read 39

### Joshua McCluskey


- Google services Location API look up the last known location of device
- Setup requires Goole play services make sure to download from SDK
- Must request permission to get location information
````Java
private FusedLocationProviderClient fusedLocationClient;

// ..

@Override
protected void onCreate(Bundle savedInstanceState) {
    // ...

    fusedLocationClient = LocationServices.getFusedLocationProviderClient(this);
}
````
- [credit](https://developer.android.com/training/location/retrieve-current)
- Within the onCreate method of your file use the above
- You can get the users last known location `getLastLocation()`
````Java
fusedLocationClient.getLastLocation()
        .addOnSuccessListener(this, new OnSuccessListener<Location>() {
            @Override
            public void onSuccess(Location location) {
                // Got last known location. In some rare situations this can be null.
                if (location != null) {
                    // Logic to handle location object
                }
            }
        });
````
- [credit](https://developer.android.com/training/location/retrieve-current)

-The above is used to get the last known location 

- There are other methods used to get an estimate of  location
- `getLastLocation()` The estimate is quick and doesn't use a lot of battery and it might be out of date
- `getCurrentLocation()` More accurate method uses active location estimates
- `requestLocationUpdates()` Try not using this one as it uses a large amount of power

````Java
protected void createLocationRequest() {
        LocationRequest locationRequest = LocationRequest.create();
        locationRequest.setInterval(10000);
        locationRequest.setFastestInterval(5000);
        locationRequest.setPriority(LocationRequest.PRIORITY_HIGH_ACCURACY);
        }
        
        /////
protected void createLocationRequest() {
        LocationRequest locationRequest = LocationRequest.create();
        locationRequest.setInterval(10000);
        locationRequest.setFastestInterval(5000);
        locationRequest.setPriority(LocationRequest.PRIORITY_HIGH_ACCURACY);
        }
        //////
        LocationSettingsRequest.Builder builder = new LocationSettingsRequest.Builder();

// ...

        SettingsClient client = LocationServices.getSettingsClient(this);
        Task<LocationSettingsResponse> task = client.checkLocationSettings(builder.build());
````
[credit](https://developer.android.com/training/location/change-location-settings)
- You  can set your intervals on updates on locations and set the priorities in
terms of energy usage and accuracy
- For getting the location in the background you'll need to update the manifest
- `ACCESS_COARSE_LOCATION`
- `ACCESS_FINE_LOCATION`
- `ACCESS_BACKGROUND_LOCATION`

- Geofences allow you to get a location in the proximity of a location of interest
- I've seen Geofences used in ski map apps to help locate your ski party when they are in certain locations or by a certain landmark.

#### Things I want to learn more about
- I want to learn more about geofencing
#### Reading

- [Get the last known location](https://developer.android.com/training/location/retrieve-current)


[<=== Back](../README.md)