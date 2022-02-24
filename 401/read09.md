# WRRC and Java

## Read 09

### Joshua McCluskey

### Simple HTTP Request in Java
- use HttpUrlConnection
- HttpUrlConnection class allows HTTP requests without additional libraries
- Doesn't provide functionality for adding headers or authentication
- `openConnection()` of the URL class creates a connection
```Java
// Request example
URL url = new URL("http://example.com");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("GET");
```
credit: [HTTP Request Java](https://www.baeldung.com/java-http-request)

- You can add request parameters and set `setDoOutput(true)` to true
- Adding header use `setRequestProperty()` `con.setRequestProperty("Content-Type", "application/json");`
- Set interval timeouts `setConnectTimeout()` `setReadTimeout()` `con.setConnectTimeout(5000);
  con.setReadTimeout(5000);`
- We can handle cookies with CookieManger and HttpCookie
- Handle Redirects with `con.setInstanceFollowRedirects(false);` `HttpUrlConnection.setFollowRedirects(false);
  `
- Parse InputStream of HttpUrlConnection instance for reading response
```Java
        int status = con.getResponseCode();
        BufferedReader in = new BufferedReader(
        new InputStreamReader(con.getInputStream()));
        String inputLine;
        StringBuffer content = new StringBuffer();
        while ((inputLine = in.readLine()) != null) {
        content.append(inputLine);
        }
        in.close();
        con.disconnect();
```
credit: [HTTP Request Java](https://www.baeldung.com/java-http-request)

[HTTP Request Guide GitHUb](https://github.com/eugenp/tutorials/tree/master/core-java-modules/core-java-networking-2)

### HTTP Request Lifecycle

- Local Processing `<protocol>://<host><:optional port>/<path/to/resource><?query>` `|http|://|www.example.com||:5000||/mainpage||?query=param&query2=param2|`
- Resolve an IP
- Establish a TCP Connection
- Send an HTTP Request

#### Articles/Sources:

[HTTP Request Java](https://www.baeldung.com/java-http-request)

[HTTP Request Lifecycle](https://dev.to/dangolant/things-i-brushed-up-on-this-week-the-http-request-lifecycle-)

[HTTP Request Guide GitHUb](https://github.com/eugenp/tutorials/tree/master/core-java-modules/core-java-networking-2)

[<=== Back](../README.md)