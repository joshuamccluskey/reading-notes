# CRUD

## Read Class 12

### Joshua McCluskey

In your own words, describe what each group of status code represents:

## Error Codes

- **100’s** = The client's request is recieved and the server will try to comply with a transmission.
- **200’s** = Usually success and that all validations were met.
- **300’s** = Redirection codes they tell the client that the location of the resource they are requesting is not in the location and will try anew location.
- **400’s** = Client error codes and are invalide request to the servers. There are many reasons for this and coul dbe an incorrect input before retrying the request.
- **500’s** = Server error codes something is wrong with the server.
  
- What is a status code **202**?
  It means request is accpete and will be completed soon. Set up to some way to verify when the response is availible.

- What is a status code **308**?
  It is a permanent redirect . Usually  when a URL is not longer needed. The client will be redirected to the new URL.
  
- What code would you use if an update didn’t return data to a client?
  **404** is an error when return data to a client was not able to return
  
- What code would you use if a resource used to exist but no longer does?
  **410** is an error where it used to exist but now is removed or deleted.
  
- What is the ‘Forbidden’ status code?
  **403** Does not have permissions to access the resource.

## REST API

- Why do we need to pull our MongoDB database string out of our server and put it into our .env?
  We will be using another URL that will not be our local host DB.
  
- What is middleware?
  Any code that runs when when teh server gets a request but before it gets passed to your routes
  
- What does app.use(express.json()) do?
  It allows the server to accept JSON as body without using a get element
  
- What does the /:id mean in a route?
  It is a parameter by typing a colon.
  
- What is the difference between PUT and PATCH?
PATCHwill only update a piece of information and PUT will update all information
  
- How do you make a default value in a schema?
  If it doesn't have a value it will default to the value of what you set for default.

- What does a 500 error status code mean?
  It means there is a server code.
  
- What is the difference between a status 200 and a status 201?
  Successfully created an  object and 200 is everything is successful. 201 is more specific and to tell you the object creation is sucessful.

[<=== Back](../README.md)
