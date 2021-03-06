# How to build

This project should be cross-compiled with Vagrant. See [otto-creator](https://github.com/NextThingCo/otto-creator) for details.

From the root directory make a `build/` directory and run `cmake` from inside it.

```
mkdir build && cd build
CC=arm-stak-linux-gnueabihf-gcc CXX=arm-stak-linux-gnueabihf-g++ cmake ..
```

Then from the build directory you can run `make`.

```
make
```

# Running

Run the otto-sdk `main` with the menu and this mode:

```
sudo /stak/sdk/otto-sdk/build/main \
	/stak/sdk/otto-menu/build/libotto_menu.so \
	/stak/sdk/otto-gif-mode/build/libotto_gif_mode.so
```

Note that `otto-menu`, `otto-sdk` and `otto-gif-mode` must be located at `/stak/sdk` on your Pi.