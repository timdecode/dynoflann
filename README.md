# nanoflann

## 1. About 

*dynoflann* is a **C++ [header-only](http://en.wikipedia.org/wiki/Header-only) library** for building KD-Trees, mostly optimized for 2D or 3D point clouds. * dynoflann* does not require compiling or installing.  You just need to `#include <dynoflann.hpp>` in your code.

This library is a *fork* of the [nanoflann library](https://github.com/jlblancoc/nanoflann) by Jose Luis Blanco that allows for dynamic insertion of points in a KD-tree. A future version will also support dynamic removal of points. To support this required changing nanoflann’s index representation at a fundamental level. This means that for static KD-trees nanoflann has superior performance, however dynoflann keeps as many of the other performance optimizations from nanoflann as possible.

Please see the [nanoflann project](https://github.com/jlblancoc/nanoflann) for documentation and examples.

I think it would be a good idea to merge this back into nanoflann perhaps as KDTreeDynamicIndexAdaptor.

### C++ API

The main difference from the original nanoflann API is the addition of addIndex to KDTreeSingleIndexAdaptor.

The save and loading functions for the index have been removed for now.
