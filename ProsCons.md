# Pros and Cons of the BoxConnector Module

Here I'll just list the pros and cons of using this module for a Mendix Application. A lot of these are just from my experience, so they may be somewhat subjective.

## Pros

* A lot of the underlying microflows, java actions, and rest mappings are already created, saving a lot of time.
* The documentation for the Box API itself is pretty good. It does a good job of explaining the various API calls and how to make them.
* Storing files up in Box is free, whereas storing files in Mendix is not.

## Cons

* The module is only really good for basic tasks. If you plan to do anything fancy with an HTTP response, you'll have to make a microflow from scratch.
* Along with that, if you want to make an HTTP request that uses a parameter not supported the module, you'll have to make a microflow from scratch as well.
* Currently, there does not appear to be a good way to decrypt the encrypted private key that the box application gives you when creating a key pair. That has to be done manually.
* There are a lot of tweaks that have to be made before the module works properly.
* The module does not appear to be actively maintained, so it may not be able to keep up when newer versions of Mendix come out.
* The documentation for the module is lacking.