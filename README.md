# Hardware-based SSH/GPG/age agent

[![Build](https://github.com/romanz/trezor-agent/actions/workflows/ci.yml/badge.svg)](https://github.com/romanz/trezor-agent/actions)
[![Chat](https://badges.gitter.im/romanz/trezor-agent.svg)](https://gitter.im/romanz/trezor-agent)

This project allows you to use various hardware security devices to operate GPG, SSH and age.  Instead of keeping your key on your computer and decrypting it with a passphrase when you want to use it, the key is generated and stored on the device and never reaches your computer.  Read more about the design [here](doc/DESIGN.md).

You can do things like sign your emails, git commits, and software packages, manage your passwords (with [pass](https://www.passwordstore.org/) and [passage](https://github.com/FiloSottile/passage), among others), authenticate web tunnels and file transfers, and more.

See the following blog posts about this tool:

- [TREZOR Firmware 1.3.4 enables SSH login](https://medium.com/@satoshilabs/trezor-firmware-1-3-4-enables-ssh-login-86a622d7e609)
- [TREZOR Firmware 1.3.6 — GPG Signing, SSH Login Updates and Advanced Transaction Features for Segwit](https://medium.com/@satoshilabs/trezor-firmware-1-3-6-20a7df6e692)
- [TREZOR Firmware 1.4.0 — GPG decryption support](https://www.reddit.com/r/TREZOR/comments/50h8r9/new_trezor_firmware_fidou2f_and_initial_ethereum/d7420q7/)
- [A Step by Step Guide to Securing your SSH Keys with the Ledger Nano S](https://thoughts.t37.net/a-step-by-step-guide-to-securing-your-ssh-keys-with-the-ledger-nano-s-92e58c64a005)

Currently [TREZOR One](https://trezor.io/), [TREZOR Model T](https://trezor.io/), [Keepkey](https://www.keepkey.com/), [Blockstream Jade](https://blockstream.com/jade/), [Ledger Nano S](https://www.ledgerwallet.com/products/ledger-nano-s), and [OnlyKey](https://onlykey.io) are supported.

## Components

This repository contains source code for one library as well as
agents to interact with several different hardware devices:

* [`libagent`](https://pypi.org/project/libagent/): shared library
* [`trezor-agent`](https://pypi.org/project/trezor-agent/): Using Trezor as hardware-based SSH/PGP/age agent
* [`ledger_agent`](https://pypi.org/project/ledger_agent/): Using Ledger as hardware-based SSH/PGP agent
* [`jade_agent`](https://github.com/Blockstream/Jade/): Using Blockstream Jade as hardware-based SSH/PGP agent
* [`keepkey_agent`](https://pypi.org/project/keepkey_agent/): Using KeepKey as hardware-based SSH/PGP agent
* [`onlykey-agent`](https://pypi.org/project/onlykey-agent/): Using OnlyKey as hardware-based SSH/PGP agent


The [/releases](/releases) page on Github contains the `libagent`
releases.

## Documentation

* **Installation** instructions are [here](doc/INSTALL.md)
* **SSH** instructions and common use cases are [here](doc/README-SSH.md)

    Note: If you're using Windows, see [trezor-ssh-agent](https://github.com/martin-lizner/trezor-ssh-agent) by Martin Lízner.

* **GPG** instructions and common use cases are [here](doc/README-GPG.md)
* **age** instructions and common use cases are [here](doc/README-age.md)
* Instructions to configure a Trezor-style **PIN entry** program are [here](doc/README-PINENTRY.md)
