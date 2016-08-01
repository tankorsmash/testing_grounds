## Optimizations

`beautify_double()` takes a double, like 123,456,000 and returns 123.456m. This
needs to get as optimized as possible. It's got a baseline of 0.002s (2ms) average
across 500 iterations. I'd like to get it to 0.00002s (0.02ms) or better.

Some things I'd like to fix are:

* using stringstream too much
* need to use sprintf more (basically tried %.3f and %.3g but couldn't get
  around the scientific notation
* creating too many strings

### Instructions

Should run right out of the box on VS2013. it basically runs test_double on a
dozen or so test inputs that test a variety of things. 

Remove the commented out CCLOG macro if you're looking to get output as you go
