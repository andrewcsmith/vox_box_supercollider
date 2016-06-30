# vox_box_supercollider

Bindings for interfacing with vox_box from SuperCollider.

## Requirements

* cmake
* SuperCollider source
* rust

## Installation

```
export SC_PATH=/path/to/supercollider/source
cargo build --release
cd ext; cmake .
make
mkdir ~/Library/Application\ Support/SuperCollider/Extensions/VoxRes
cp VoxRes.scx ~/Library/Application\ Support/SuperCollider/Extensions/VoxRes
cp vox_res.sc ~/Library/Application\ Support/SuperCollider/Extensions/VoxRes
```

