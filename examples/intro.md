Introduction
============

* goal
  * how to build Bitcoin-based applications

* recommendations
  * install the Bitcoin Core's current version
    * ways
      * [source code](https://github.com/bitcoin/bitcoin)
      * [pre-compiled executable](https://bitcoin.org/en/download)
    * -> 👀give you access to👀
      * ``bitcoind``
        * uses
          * programming
        * == FULL Bitcoin peer / you can interact with -- through -- [RPCs](../reference/rpc) |
          * port 8332
          * port 18332 -- for -- testnet
        * requirements
          * add a [RPC](../reference/rpc/) password | your ``bitcoin.conf``
      * ``bitcoin-qt``
        * == FULL Bitcoin peer + wallet FE
        * | "Help" menu's console,
          * you can enter [RPC commands](../reference/rpc) 
      * ``bitcoin-cli``
        * allows you to
          * send [RPC](../reference/rpc) commands -- to -- ``bitcoind``
        * _Example:_  ``bitcoin-cli help``
        * requirements
          * add a [RPC](../reference/rpc/) password | your ``bitcoin.conf``
  * | development
    * use [Bitcoin’s test network](../devguide/p2p_network.md) OR [regression test mode (`regtest`)](testing.md)
      * Reason: 🧠safer and cheaper🧠

* ``bitcoin.conf``
  * place | Bitcoin's application directory
    * | Windows,
      * ``%APPDATA%\Bitcoin\``
    * | OSX,
      * ``$HOME/Library/Application Support/Bitcoin/``
    * | Linux,
      * ``$HOME/.bitcoin/``
  * uses
    * provide settings to
      * ``bitcoind``
      * ``bitcoin-qt``
      * ``bitcoin-cli``
  * recommendations
    * readable only | its owner
      * steps
        * | Bitcoin application directory,
          ```
          chmod 0600 bitcoin.conf
          ```
  * if ``bitcoind`` & ``bitcoin-cli`` run | SAME system -- as the -- SAME user -> read | SAME file
    * -> 👀ANY long random password work👀
      ```
      rpcpassword=change_this_to_a_long_random_password
      ```

# questions
* about Bitcoin use
  * [BitcoinTalk forum](https://bitcointalk.org/index.php?board=4.0)
  * [IRC channels](https://en.bitcoin.it/wiki/IRC_channels)

* about documentation
  * [Bitcoin.org](https://github.com/bitcoin-dot-org/bitcoin.org/issues) 
  * [bitcoin-documentation mailing list](https://groups.google.com/forum/#!forum/bitcoin-documentation)

# syntax | this documentation
* | some strings,
  * “[…]”
    * == extra data was removed & lines ending are continued

