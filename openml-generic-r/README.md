OpenML Provider for generic R models
------------------------------------------------------------

This module contains an OpenML provider for loading custom code that implements
Feedzai's R API.

The implemented "Classifier" should define the following methods: 

```r
# loads a model. This can be a no-op if there's no need to save state  
loadModel <- function() {
    stop("This must be implemented by a concrete provider")
}

# score the instance stored in the 'instance' global var and returns an array with the probability for each of the classes
getClassDistribution <- function() {
    stop("This must be implemented by a concrete provider")
}

# returns the predicted class of the instance stored in the 'instance' global var
classify <- function() {
    stop("This must be implemented by a concrete provider")
}
``` 
