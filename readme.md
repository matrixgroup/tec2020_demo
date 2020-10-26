## This is the demo code for TEC2020 
### Unlocking New Member Benefits via Member-Only Access to Cloud Resources

The code here is from Auth0's [samples.](https://github.com/auth0-samples/auth0-javascript-samples)
The essential changes are app.js:callApi

For this code to work you will need an Auth0 Account acting as OpenID Connect ID provider(OIDC IdP) and AWS account with a Cognito Federated Identity setup like [this](https://auth0.com/docs/integrations/amazon-cognito)

The permissions granted to authorized users are set via the role in Cognito Federated Pool and that role contains a policy that looks like:
```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": "events:PutEvents",
            "Resource": "arn:aws:events:us-east-1:5430----2478:event-bus/default"
        }
    ]
}
```

You will need to put your account info in auth_config.json file as well as the XXXX in app.js.
