# Pros and Cons of the BoxConnector Module

Here I'll just list the pros and cons of using this module for a Mendix Application. A lot of these are just from my experience, so they may be somewhat subjective.

## Pros

* A lot of the underlying microflows, java actions, and rest mappings are already created, saving a lot of time.
* The documentation for the Box API itself is pretty good. It does a good job of explaining the various API calls and how to make them.
* Storing files up in Box is free, whereas storing files in Mendix is not.
* There's more control when working with files in Box vs. files in Mendix.

## Cons

* Currently, there does not appear to be a good way to decrypt the encrypted private key that the box application gives you when creating a key pair. That has to be done manually.
* There are a lot of tweaks that have to be made before the module works properly.
* The module does not appear to be actively maintained, so it may not be able to keep up when newer versions of Mendix come out.
* The documentation for the module is lacking.
* The module doesn't have the greatest error handling. The errors it gives don't really help you figure out what the problem is.
