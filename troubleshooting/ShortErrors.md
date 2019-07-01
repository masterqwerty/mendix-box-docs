# Short Errors

![](../../res/troubleshooting/short-error.png)

I named this one short errors since these are the errors that appear in the console that are no more than two or three words long, which tell almost nothing. Each of these errors correspond to a specific HTTP error code that is returned when making the actual API call. These errors come from the `HandleRejectedMessage` microflow that is found under `BoxConnector > Implementation > Common`.

## Authentication error

This one corresponds to a 401 error. This can happen because your access token has either expired or is invalid.

## Bad Request error

This one corresponds to a 400 error. This often happens because the request isn't formatted correctly. Make sure that you are passing in the necessary parameters when you call the various API calls. If you're sure that they're being passed in correctly, you may need to look at the appropriate implementation microflow which will be found under `BoxConnector > Implementation > API`, and will be named after the API call with a `Impl` suffix. Check the REST activity and see if it matches the format given in the Box API documentation under https://developer.box.com/reference

## Forbidden error

This one corresponds to a 403 error. This basically means that your application is not authorized to make the API call it's trying to make. This can be fixed by changing the permissions of your application. Note that changing permissions in your application may break the application if you are required to have your application approved by an enterprise admin.

## Conflict error

This one corresponds to a 409 error.

## Not Found error

This one corresponds to a 404 error. This most likely means that the resource you are trying to access doesn't exist, or you passed in the wrong folder or file id.

## PreCondition Failed error

This one corresponds to a 412 error.
