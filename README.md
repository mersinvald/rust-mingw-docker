A Docker image based on Ubuntu that contains MinGW, rustup, Rust, Cargo and Wine.
Based on the official Ubuntu image and rustup, so it automatically updates through rustup.

Cargo is able to build and run binaries for the `x86_86-pc-windows-gnu` and `i686-pc-windows-gnu`
targets.

## Example

```sh
docker pull mersinvald/rust-mingw-docker

docker run --rm -it -v `pwd`:/usr/code -w /usr/code mersinvald/rust-mingw-docker
cargo test --target x86_86-pc-windows-gnu
cargo test --target i686-pc-windows-gnu
```

### Acknowledgement

Kudos to [Tomaka](https://github.com/tomaka) for building the original image.
