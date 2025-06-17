# Welcome to developer.bitcoin.org's codebase

* hosted | [developer.bitcoin.org](https://developer.bitcoin.org)

## documentation

* [here](index.rst)

## how to render the documentation locally?

* TODO:
To render the documentation locally you first need to install Sphinx and the
required theme modules, e.g. by running

    pip install -r requirements.txt

This should be done from the root of this repo. Then you can execute Sphinx by calling

    make html

This will generate HTML from the RST sources in the directory `_build/html`.
It's all static HTML so you can just open the index.html file in your browser
locally to view the rendered documentation.

## Generation of RPC docs

* generated -- via -- bitcoin client + [helper tool](reference/rpc)
