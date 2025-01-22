# plain

This directory contain the WASM file for the [plain example from refraction-networking/watm](https://github.com/refraction-networking/watm/tree/master/tinygo/v1/examples/plain). This is only intended for development purposes and shouldn't be used in production.

## Steps for generating the WASM file

- Install [TinyGo](https://tinygo.org/getting-started/install/)
- Clone the [refraction-networking/watm](https://github.com/refraction-networking/watm/tree/v0.7.0-beta) repository and change the branch:
```sh
git clone git@github.com:refraction-networking/watm.git
cd watm && git checkout v0.7.0-beta
```
- Go to the plain tinygo example directory and generate the WASM file:
```sh
cd tinygo/v1/examples/plain
tinygo build -o plain.wasm -target=wasi -no-debug -scheduler=none -gc=conservative .
```

You can find more details by reading the [example README](https://github.com/refraction-networking/watm/blob/v0.7.0-beta/tinygo/v1/examples/plain/README.md).
