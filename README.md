webpagetestr
============

**Warning: This is very much a work in progress! Although I've hacked R in the past I've never tried writing it in anger so YMMV

If you wander past and have some suggestions on how I could do things better, or differently feel free to let me know**

R package to gather web page performance metrics using WebPagetest

Goal is to be able to provide a list of URLs and list of parameters then submit tests and extract a list of desired results fields for each test.

Ideally parameters will be specified sparsely something like:

```
params <- list(
  location = c("Dulles:Chrome.custom"),
  bwDown = c(1000, 2000),
  latency = c(28, 56),
  f = "json"
)
```

which can them be expanded into the full set of combinations:

```
            location bwDown latency    f
Dulles:Chrome.custom   1000      28 json
Dulles:Chrome.custom   2000      28 json
Dulles:Chrome.custom   1000      56 json
Dulles:Chrome.custom   2000      56 json
```


