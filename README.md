# random_os

A minimal rust kernel build upon a freestanding rust binary [random](https://github.com/benodiwal/random)

## Prerequisites:

- `Installing Rust Nightly`:
```sh
rustup override set nightly
```

- `Confirming your rust release channel:`  
```sh
rustc --version
```
The version number should contain -nightly at the end.

- `llvm-tools-preview` for building the `bootloader`

```sh
rustup component add llvm-tools-preview
```
- `Install BootImage`

```sh
cargo install bootimage
```


## How to Build:

```sh
cargo bootimage
```

## Booting in QEMU

```sh
qemu-system-x86_64 -drive format=raw,file=target/x86_64-random-os/debug/bootimage-random-os.bin
```

### References:
[A Minimal Rust Kernel](https://os.phil-opp.com/minimal-rust-kernel) by Philipp Oppermann
