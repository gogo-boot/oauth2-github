## Go OAuth Example

Read the blog post [here](https://www.sohamkamani.com/golang/oauth)

This is an example node application that implements Githubs OAuth2 API.

In order to run the application:

1. Register your new application on Github : https://github.com/settings/applications/new. In the "callback URL" field, enter "http://localhost:8080/oauth/redirect". Once you register, you will get a client ID and client secret.
2. Replace the values of the `clientID` and `clientSecret` variables in the [main.go](/main.go) file and also the [index.html](https://github.com/sohamkamani/go-oauth-example/blob/master/public/index.html#L14) file
4. Start the server by executing `go run main.go`
5. Navigate to http://localhost:8080 on your browser.

Extra Info
github -> settings -> developer settings

### Set Environment Variables

We save client id and secret in env variables and only use os.Getenv in the code.

```
cp template.env test.env
# Set your client id / password. It is for IDE env Plugin. 
# you don't have to export environmentvariable manually. don't push it to git reop 
vi test.env
```