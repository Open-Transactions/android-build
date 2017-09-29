## Open-Transactions Android Build Scripts

These scripts build Open-Transactions and all its dependencies using the Android NDK

### Install Instructions

These scripts must be installed as ~/bin for the user which will perform the build.

    rm -r ~/cmake
    git clone ssh://git@git.cjdns.stashcrypto.net/ot/android-cmake ~/cmake

    rm -r ~/bin
    git clone ssh://git@git.cjdns.stashcrypto.net/ot/android-build ~/bin

### Dependencies

* The specified NDK must be installed in /usr/local/share/ndk/<ndk-name>
* The build system must have ncurses 5.9 installed with libtinfo support
* The build system must have rpl installed
* The build system must have a version of protoc installed that matches the one being compiled
* The build system must have makedepend installed
* The deploy_files script assumes that Stash Wallet is cloned to ~/stash-wallet
  * git clone ssh://git@git.cjdns.stashcrypto.net/stash/stash-wallet ~/stash-wallet
