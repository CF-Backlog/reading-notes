# Bearer Authorization

Write the following steps in the correct order:

Register your application to get a client_id and client_secret 
Ask the client if they want to sign in via a third party
Redirect to a third party authentication endpoint
Make a request to a third-party API endpoint
Receive authorization code
Make a request to the access token endpoint
Receive access token

What can you do with an authorization code?
> It is a temporary code meant to be traded for an access token

What can you do with an access token?
> Gives a user and an app access to parts of an API also authorizing the app to access user information, or not

What’s a benefit of using OAuth instead of your own basic authentication?
> OAuth is more convenient for the user. Also provides a new layer of protection as opposed to basic auth.

Document the following Vocabulary Terms
Term

Client ID - user identifier
Client Secret - secret handshake between app and auth server
Authentication Endpoint - passport control for user authentication
Access Token Endpoint - bit of code that requests the token
API Endpoint - API request location
Authorization Code - secret temporary handshake made to return a token
Access Token - mcGuffin used to verify a server/api request

Which 3 things had you heard about previously and now have better clarity on?

Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
testing

What are you most excited about trying to implement or see how it works?

Preparation Materials
JWTs Explained
Intro to JWT
Are JWTs Secure?
Bookmark
npm jsonwebtoken docs

Sources:

https://www.oauth.com/oauth2-servers/server-side-apps/authorization-code/#:~:text=The%20authorization%20code%20is%20a,approve%20or%20deny%20the%20request.