brew install qemu
rustup update
rustup component add rust-src
cargo install bootimage


# build
cargo build -Z build-std=core,compiler_builtins -Z build-std-features=compiler-builtins-mem -Z unstable-options -Z json-target-spec


# bootimage
cargo +nightly bootimage \
-Z build-std=core,compiler_builtins \
-Z build-std-features=compiler-builtins-mem \
-Z unstable-options \
-Z json-target-spec


