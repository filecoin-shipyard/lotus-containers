# `lotus-containers`: Seamless Lotus Container Images

`lotus-containers` provides pre-built container images of the Lotus blockchain software, tailored for specific versions, networks, and platforms.

## Supported Configurations

The pre-built images are available for:

- **Networks**:
    - `mainnet`
    - `devnet`

- **Lotus Version**:
    - `v1.24.0`
    - `v1.24.1`
    - `v1.25.0`
    - `v1.25.1`
    - `v1.25.2`
    - `v1.26.0-rc1`

- **Platforms**:
    - `linux/amd64`
    - `linux/arm64`

Each image bundles all lotus executables for your convenience.

## Getting Started

Retrieve your desired image with the following command:

```bash
docker pull ghcr.io/filecoin-shipyard/lotus-containers:lotus-<version>-<network>
# For instance: docker pull ghcr.io/filecoin-shipyard/lotus-containers:lotus-v1.23.2-mainnet
```

## Licensing

`lotus-containers` is dual-licensed under the MIT and Apache 2.0 licenses. For further details, please refer to [LICENSE](LICENSE.md).
