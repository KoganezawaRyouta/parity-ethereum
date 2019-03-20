FROM rust:1.33.0

# see https://github.com/paritytech/parity-ethereum/tree/PrivateStatusMethod#build-dependencies
RUN apt-get update && \
    apt-get install -y libusb-1.0-0-dev libudev-dev cmake make gcc g++ pkg-config file

ADD . /root/parity-ethereum
WORKDIR /root/parity-ethereum

# see https://github.com/paritytech/parity-ethereum/tree/PrivateStatusMethod#build-from-source-code
RUN cargo build --release --features final
