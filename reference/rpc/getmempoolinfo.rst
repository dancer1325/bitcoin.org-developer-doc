.. This file is licensed under the MIT License (MIT) available on
   http://opensource.org/licenses/MIT.

getmempoolinfo
==============

``getmempoolinfo``

Returns TX memory pool's active state's details

Result
~~~~~~

::

  {                            (json object)
    "loaded" : true|false,     (boolean) True if the mempool is fully loaded
    "size" : n,                (numeric) Current tx count
    "bytes" : n,               (numeric) Sum of all virtual transaction sizes as defined in BIP 141. Differs from actual serialized size because witness data is discounted
    "usage" : n,               (numeric) Total memory usage for the mempool
    "maxmempool" : n,          (numeric) Maximum memory usage for the mempool
    "mempoolminfee" : n,       (numeric) Minimum fee rate in BTC/kB for tx to be accepted. Is the maximum of minrelaytxfee and minimum mempool fee
    "minrelaytxfee" : n,       (numeric) Current minimum relay fee for transactions
    "unbroadcastcount" : n     (numeric) Current number of transactions that haven't passed initial broadcast yet
  }

Examples
~~~~~~~~


.. highlight:: shell

::

  bitcoin-cli getmempoolinfo

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "getmempoolinfo", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:8332/

