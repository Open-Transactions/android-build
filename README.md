## Open-Transactions Android Build Scripts

These scripts build Open-Transactions and all its dependencies using the Android NDK

### Install Instructions

These scripts must be installed as ~/bin for the user which will perform the build.

    rm -r ~/bin
    git clone https://github.com/Open-Transactions/android-build.git ~/bin

#### Reduced download time

Add the following lines to ~/.gitconfig to reduce redundant downloads: 

```
[url "/home/build/git/lucre"]
  insteadOf = https://github.com/Open-Transactions/lucre.git
[url "/home/build/git/simpleini"]
  insteadOf = https://github.com/brofield/simpleini.git
[url "/home/build/git/chai"]
  insteadOf = https://github.com/ChaiScript/ChaiScript.git
[url "/home/build/git/trezor"]
  insteadOf = https://github.com/trezor/trezor-crypto.git
[url "/home/build/git/protobuf"]
  insteadOf = https://github.com/google/protobuf.git
[url "/home/build/git/libsodium"]
  insteadOf = https://github.com/jedisct1/libsodium.git
[url "/home/build/git/secp256k1"]
  insteadOf = https://github.com/libbitcoin/secp256k1.git
[url "/home/build/git/zmq"]
  insteadOf = https://github.com/zeromq/libzmq.git
[url "/home/build/git/opentxs"]
  insteadOf = https://github.com/Stash-Crypto/opentxs.git
[url "/home/build/git/opentxs-proto"]
  insteadOf = https://github.com/Stash-Crypto/opentxs-proto.git
[url "/home/build/git/benchmark"]
  insteadOf = https://github.com/google/benchmark.git
```

#### Parallel build

Set OT_MAKE_OPTS in your environment (~/.bashrc) if you want parallel builds.

Example:

```
export OT_MAKE_OPTS="-j8"
```

### Dependencies

* The specified NDK must be installed in /usr/local/share/ndk/<ndk-name>
* The build system must have ncurses 5.9 installed with libtinfo support
* The build system must have rpl installed
* The build system must have a version of protoc installed that matches the one being compiled
* The build system must have makedepend installed
