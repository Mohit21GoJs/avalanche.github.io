## Preview

Avalanche app provides an end to end safe and secure solution for inviting users based on their emails or from google contacts, the consumers of the app are Corporates/startups who want customized/zero-config referral system that works and scales, and it is super secure. 

## Components Involved

The components of avalanche app are:

* An embeddable [UI](https://refer-ui-two.vercel.app/)
* A customer dashboard [app](https://refer-customer-dashboard.vercel.app/)
* A backend [api](http://salty-reef-38656.herokuapp.com/)
* Browser SDK [Package](https://www.npmjs.com/package/avalanche-browser).
* Node.js SDK [Package](https://www.npmjs.com/package/avalanche-api).


### Flow diagram for simple email invite
![Normal-Flow-Diagram](./Flow-Normal.png)

### Using Avalanche SDK

First step is to sign up on [customer app](https://refer-customer-dashboard.vercel.app/) and grab your `client_id` and `client_secret`.

Once you have the credentials, setup a route on server side

This route will be providing you a session token with your secret credentials and that token will be used to idenitfy the request your app will make to our api

On ui embed the invite app through iframe and pass in parameters like email, token and redirect url

when a new user signs up with referral code, call the method signupMySDK with the session token, this will mark the user signed_up on our system

when a new user reaches a premium level, call the premium sdk method

when a user reaches upgraded mark him upgraded by calling our sdk method
