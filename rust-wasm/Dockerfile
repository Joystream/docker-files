FROM liuchong/rustup:1.32.0
LABEL maintainer="mokhtar@jsgenesis.com"
LABEL description="Setup rust toolchain for building substrate node and runtimes"

# nightly toolchain for wasm target
RUN rustup install nightly

# for native code stick with 1.32.0
RUN rustup default 1.32.0

# wasm target and wasm compacting tool
RUN rustup target add wasm32-unknown-unknown --toolchain nightly && \
    cargo install --git https://github.com/alexcrichton/wasm-gc --force

