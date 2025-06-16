* tool / 
  * 👀generate Bitcoin Core RPC documentation👀

* requirements
  * run `bitcoin-cli` client
  * documentation -- as -- [bitcoin.org](https://github.com/bitcoin-dot-org/bitcoin.org/tree/master/_data/devdocs/en/bitcoin-core/rpcs)

* steps
  * `rpc-docs-helper`
    * get the CL help
  * `rpc-docs-helper generate`
    * generate the markdown
  * `pytest`
    * run the unit tests
