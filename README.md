This aims to be a kernel with good support for the Surface Book.  Incidentally,
support for other Surfaces and other devices with similar hardware may emerge.

Note that one of the main goals of this repo is keeping patches in a clean,
potentially upstreamable, state - the eventual hope is to upstream everything.

Branches:
- sb-vX.XX(-rcX)?.N:
  The Nth version of the surface book patchseries for vX.XX-rcX/vX.XX linux
  kernel, applied on top of that kernel.

  Note that if fixes are made after an initial release (on branch sb-vX.XX.0),
  they will likely not be incorporated into that branch, but instead squashed
  with the original commits to form a new set of commits on sb-vX.XX.1

- sb-cumul-vX.XX:
  A branch for all the fixes. The work-tree state of sb-cumul-vX.XX should
  always be the same as sb-vX.XX.N where N is the highest present version
  number. The difference from the sb-vX.XX is that this branch does not
  maintain a clean patch history; instead, as new fixes are found they will be
  added as new commits to this branch, allowing easy git-pulling to incorporate
  fixes.

- for-jakeday:
  Just the IPTS multitouch fixes on top of
  https://github.com/jakeday/linux-surface.  I do not use this kernel, but this
  branch allows users who do use it to use multitouch IPTS.
