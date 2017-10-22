# gr-fcdproplus

gr-fcdproplus is an Linux and OSX addon for gnuradio to implement a funcube dongle pro+ source.

On linux it autodetects the correct soundcard from /proc/asound/cards.
This idea was taken from the osmosdr drivers.

**This repo is a copy of the work of DL1KSV.**

## Rationale

I was using DSL1KSV's module but had problems building it on OSX with homebrew.
The root of the cause were some custom cmake hacks so I took his code and put the current
gnuradio default cmake files in.

**Warning:** In order to be backwards compatible this block as exactly the same name and properties as DL1KSV's. If you install this it will overwrite the old one.

## Building

On Linux do something like this.

```bash
$ git clone https://github.com/ast/gr-fcdproplus.git
$ cd gr-fcdproplus
$ mkdir build && cd build
$ cmake ..
$ make
$ make install
```

## Changes

* Always use system [hidapi](http://www.signal11.us/oss/hidapi/).
* Added FindHIDAPI.cmake
* More to come.


## Acknowledgements

* https://github.com/dl1ksv/gr-fcdproplus
