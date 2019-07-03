# BoxConnector Tweaks

Here are some tweaks you can make to the box connector module to make life a little bit easier.

## Expiration date and time on access tokens

One thing that's not very nice about the way access tokens are managed in the box connector module, is that you are only given the amount of seconds before a token expires. On top of that, the seconds don't exactly update, so it's just stuck on whatever number of seconds you initially had for the token. This little tweak makes it easier to know when the tokens will expire so you can manage them better.

* Add a `DateTime` attribute to the `AccessToken` entity in the box connector's domain model, and call it something like "expires" or "expires on"
* Add a before commit event handler to the `AccessToken` entity, and create a newmicroflow.
* In the newly created microflow, make sure that there is an `AccessToken`parameter. If you didn't create the microflow when selecting a microflow for the event handler before, it probably won't be there.
* Add an activity that changes the `AccessToken` object. It will change the new attribute that you just created.
* The activity should then set that new attribute to the following expression:
```
addSeconds([%CurrentDateTime%], $AccessToken/expiresIn)
```
* Now save the microflow and run your app. Now when you request access tokens, the app will also store the time they expire.