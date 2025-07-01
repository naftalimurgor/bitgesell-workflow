# bitgesell-workflow
<img src="Icon.png" style="height: 60px;" />

A proposed Bitgesell workflow


# Bitgesell (BGL)

Bitgesell is a lightweight, deflationary cryptocurrency based on a minimal Bitcoin fork. It reduces the block reward over time and prunes unnecessary blockchain data to prioritize efficiency, scarcity, and long-term sustainability.

## 🔧 Build Instructions

### Prerequisites
Install the following packages (example for Ubuntu/Debian):
```bash
sudo apt update
sudo apt install build-essential libtool autotools-dev automake pkg-config bsdmainutils python3
sudo apt install libevent-dev libboost-system-dev libboost-filesystem-dev \
libboost-test-dev libboost-thread-dev libssl-dev libdb-dev libdb++-dev
````

### Compile

```bash
./autogen.sh
./configure
make
make check  # optional: runs unit tests
```

## 🚀 Running the Node

```bash
./src/BGLd -daemon     # start node in background
./src/bitgesell-cli getinfo  # interact with running node
```

## 🤖 CI Pipeline

All pull requests trigger our full GitHub Actions CI pipeline:

* ✅ Linux, macOS, and Windows builds
* 🧪 Unit tests
* 🔁 Functional tests (`test_runner.py`)
* 🧼 Linting (`flake8`, `clang-format`)
* ⚠️ Fuzz testing (Linux)

PRs must pass **all jobs** before they can be merged.

## 💡 Features vs Bitcoin

| Feature          | Bitcoin        | Bitgesell                  |
| ---------------- | -------------- |----------------------------|
| Block size       | 1 MB           | 400kb                      |
| Halving schedule | \~4 yrs        | Every year                 |
| Block reward     | 6.25 BTC       | Reduces by 50% annually    |
| SegWit           | ✅              | ✅                          |
| Smart contracts  | ❌              | ❌                          |
| Focus            | Store of value | Deflationary + lightweight |

## 🧠 License

This project is licensed under the [MIT license](./COPYING).

---