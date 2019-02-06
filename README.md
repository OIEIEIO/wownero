# ~~Mo~~Wownero

Copyright (c) 2014-2018 The Monero Project.   
Portions Copyright (c) 2012-2013 The Cryptonote developers.

## Resources

- Web: [wownero.org](http://wownero.org)
- Twitter: [@w0wn3r0](https://twitter.com/w0wn3r0)
- Discord: [discord.gg/sQt74ep](https://discord.gg/sQt74ep)
- Reddit: [/r/wownero](https://www.reddit.com/r/wownero)
- Mail: [wownero@protonmail.com](mailto:wownero@protonmail.com)
- GitHub: [https://github.com/wownero/wownero](https://github.com/wownero/wownero)
- IRC: [#wownero on Freenode](https://kiwiirc.com/client/irc.freenode.net/?nick=suchchatter|?#wownero)
- Bitmessage Chan: wownero (`BM-2cSzWtrj2pzLva9GF1Jp2TYsnLjrnJpvba`)
- Network stats: [https://freeboard.io/board/c8mM2c](https://freeboard.io/board/c8mM2c)
- Wownero Funding System: [https://funding.wownero.com](https://funding.wownero.com)
- Keybase Group Chat: [https://keybase.io/team/wownero](https://keybase.io/team/wownero)

Blockchain Explorers
- https://explore.wownero.com
- https://explorer.wowkira.com
- http://explorer.wowne.ro
- http://wow4edxxxudchgj7.onion
- http://wow5eqtzqvsg5jctqzg5g7uk3u62sfqiacj5x6lo4by7bvnj6jkvubyd.onion

## Introduction

Wownero is a privacy-centric memecoin that was fairly launched on April 1, 2018 with no pre-mine, stealth-mine or ICO. Wownero has a maximum supply of around 184 million WOW with a slow and steady emission over 50 years. It is a fork of Monero, but with its own genesis block, so there is no degradation of privacy due to ring signatures using different participants for the same tx outputs on opposing forks.

## Scheduled software upgrades

Wownero uses a fixed-schedule software upgrade (hard fork) mechanism to implement new features. This means that users of Wownero (end users and service providers) should run current versions and upgrade their software on a regular schedule. The required software for these upgrades will be available prior to the scheduled date. Please check the repository prior to this date for the proper Wownero software version. Below is the historical schedule and the projected schedule for the next upgrade.
Dates are provided in the format YYYY-MM-DD. 



| Software upgrade block height | Date       | Release Name | Minimum Wownero version | Recommended Wownero version | Details                                                                            |  
| ------------------------------ | -----------| ----------------- | ---------------------- | -------------------------- | ---------------------------------------------------------------------------------- |
| 1                              | 2018-04-01 | Awesome Akita                | v0.1.0.0               | v0.1.0.0                  | Cryptonight variant 1, ringsize >= 8, sorted inputs
| 6969                           | 2018-04-24 | Busty Brazzers                | v0.2.0.0               | v0.2.0.0                  | Bulletproofs, LWMA difficulty algorithm, ringsize >= 10, reduce unlock to 4
| 53666                          | 2018-10-06 | Cool Cage                | v0.3.0.0               | v0.3.1.3                  | Cryptonight variant 2, LWMA v2, ringsize = 22, MMS
| 63469                          | 2018-11-11 | Dank Doge               | v0.4.0.0               | v0.4.0.0                  | LWMA v4
| 81769                          | 2019-02-14 | Erotic EggplantEmoji    | v0.5.0.0               | v0.5.0.0                  | CryptonightR, SMA difficulty algorithm with N=144, Updated Bulletproofs, Fee Per Byte, Tor SOCKS support, Pruning, Auto-churn

X's indicate that these details have not been determined as of commit date.

## Release staging and Contributing

**Anyone is welcome to contribute to Wownero's codebase!** 

If you have a fix or code change, feel free to submit it as a pull request. Ahead of a scheduled software upgrade, a development branch will be created with the new release version tag. Pull requests that address bugs should be made to Master. Pull requests that require review and testing (generally, optimizations and new features) should be made to the development branch. All pull requests will be considered safe until the US dollar valuation of 1 Wownero equals $1000. After this valuation has been reached, more research will be needed to introduce experimental cryptography and/or code into the codebase.  

## Installing from a package

Packages are available for

* Arch Linux/Manjaro

        yay -S wownero-git

* NixOS

        nix-shell -p altcoins.wownero

Packaging for your favorite distribution would be a welcome contribution!

**DISCLAIMER: These packages are not part of this repository, and as such, do not go through the same review process to ensure their trustworthiness and security.**


## Building from Source

* Arch Linux/Manjaro

        sudo pacman -Syu && sudo pacman -S base-devel cmake boost openssl zeromq libpgm unbound libsodium git
        git clone https://github.com/wownero/wownero
        cd wownero
        make


* Debian/Ubuntu

        sudo apt update && sudo apt install build-essential cmake pkg-config libboost-all-dev libssl-dev libzmq3-dev libunbound-dev libsodium-dev libpgm-dev git
        git clone https://github.com/wownero/wownero
        cd wownero
        make


## Running Binaries

The build places the binary in `bin/` sub-directory within the build directory
from which cmake was invoked (repository root by default). To run in
foreground:

    ./bin/wownerod

To list all available options, run `./bin/wownerod --help`.  Options can be
specified either on the command line or in a configuration file passed by the
`--config-file` argument.  To specify an option in the configuration file, add
a line with the syntax `argumentname=value`, where `argumentname` is the name
of the argument without the leading dashes, for example `log-level=1`.

To run in background:

    ./bin/wownerod --log-file wownerod.log --detach

To run as a systemd service, copy
[wownerod.service](utils/systemd/wownerod.service) to `/etc/systemd/system/` and
[wownerod.conf](utils/conf/wownerod.conf) to `/etc/`. The [example
service](utils/systemd/wownerod.service) assumes that the user `wownero` exists
and its home is the data directory specified in the [example
config](utils/conf/wownerod.conf).

Once node is synced to network, run the CLI wallet by entering:

    ./bin/wownero-wallet-cli

Type `help` in CLI wallet to see standard commands (for advanced options, type `help_advanced`).

## Wownero Graphical Wallets

* [Wownero-Light-Wallet](https://github.com/wownero/Wownero-Light-Wallet)

![](https://light.wownero.com/wowlight.png)


* [Wownerujo Android Wallet](https://github.com/wownero/wownerujo)

![](https://fossdroid.com/images/screenshots/com.wownero.wownerujo/wownerujo-1.png)
![](https://fossdroid.com/images/screenshots/com.wownero.wownerujo/wownerujo-2.png)

## Anonymous Overlay Networks

# Tor

It is possible to connect to the Wownero network via Tor SOCKS proxy. Edit the `torrc` configuration file and add:


        HiddenServiceDir /var/lib/tor/wownero
        HiddenServiceVersion 3
        HiddenServicePort 32111 127.0.0.1:32111

Your node's ".onion" address can be found in the `hostname` file. Peers must be manually specified as:

        --add-exclusive-node wowdyoh2juxxjoke.onion:32111
        --add-peer wowdyoh2juxxjoke.onion:32111


Tor Public Nodes
 - `wowdyoh2juxxjoke.onion:32111`
 - `vh42ssldf4brtoveyc2zc2rmwybh22ytt7xvqbsfdktkdhgmzz45vvad.onion:32111`

Syntax example:

        ./wownerod --proxy tor,127.0.0.1:9050,20 --anonymous-inbound YOUR_ADDRESS.onion:32111,127.0.0.1:32111,20 --add-peer wowdyoh2juxxjoke.onion:32111 --add-peer vh42ssldf4brtoveyc2zc2rmwybh22ytt7xvqbsfdktkdhgmzz45vvad.onion:32111

# I2P

TODO
