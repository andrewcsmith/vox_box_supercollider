# vox_box_supercollider

Bindings for interfacing with vox_box from SuperCollider.

## Requirements

* cmake
* SuperCollider source
* rust

## Build

```
export SC_PATH=/path/to/supercollider/source
cargo build --release
cd ext; cmake .
make
```

