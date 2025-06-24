Glossary
========

.. glossary::

  51 percent attack
  Majority attack
    The ability of someone controlling a majority of network hash rate to revise transaction history and prevent new transactions from confirming.

  Address
    A 20-byte hash formatted using base58check to produce either a P2PKH or P2SH Bitcoin address.  Currently the most common way users exchange payment information.

    **Not to be confused with:** IP address

  Base58check
    The method used in Bitcoin for converting 160-bit hashes into P2PKH and P2SH addresses.  Also used in other parts of Bitcoin, such as encoding private keys for backup in WIP format.  Not the same as other base58 implementations.

    **Not to be confused with:** P2PKH address, P2SH address, IP address

# Block
* \>=1 transactions /
  * has
    * PREVIOUS block header's hash
  * protected -- by -- proof of work
* == data stored | blockchain

# Blockchain / Best blockchain
* == chain of blocks /
  * EACH block reference -- the -- PRECEEDING block

* BEST blockchain
  * := most-difficult-to-recreate chain

# Block header / Header
* == 80-byte header / 
  * belong | 1! block
  * hashed repeatedly -- to -- create proof of work

    Height
    Block height
      The number of blocks preceding a particular block on a block chain. For example, the genesis block has a height of zero because zero block preceded it.

    Block reward
      The amount that miners may claim as a reward for creating a block. Equal to the sum of the block subsidy (newly available satoshis) plus the transactions fees paid by transactions included in the block.

      **Not to be confused with:** Block subsidy, Transaction fees

# Maximum Block Size
* 👀MAXIMUM block's size -- according to the -- consensus rules👀
  * != Blockchain size 
* CURRENT block size limit = 4 million weight units (== 1 million vbytes)

    

  Blocks-first sync
    Synchronizing the block chain by downloading each block from a peer and then validating it.

    **Not to be confused with:** Headers-first sync

  Bloom filter
    A filter used primarily by SPV clients to request only matching transactions and merkle blocks from full nodes.

    **Not to be confused with:** Bloom filter (general computer science term, of which Bitcoin's bloom filters are a specific implementation)

  Chain code
    In HD wallets, 256 bits of entropy added to the public and private keys to help them generate secure child keys; the master chain code is usually derived from a seed along with the master private key

  Change address
  Change output
    An output in a transaction which returns satoshis to the spender, thus preventing too much of the input value from going to transaction fees.

    **Not to be confused with:** Address reuse

  Child key
  Child public key
  Child private key
    In HD wallets, a key derived from a parent key.  The key can be either a private key or a public key, and the key derivation may also require a chain code.

    **Not to be confused with:** Public key (derived from a private key, not a parent key)

  Coinbase
    A special field used as the sole input for coinbase transactions. The coinbase allows claiming the block reward and provides up to 100 bytes for arbitrary data.

    **Not to be confused with:** Coinbase transaction, Coinbase.com

  Coinbase transaction
  Generation transaction
    The first transaction in a block.  Always created by a miner, it includes a single coinbase.

    **Not to be confused with:** Coinbase (the unique part of a coinbase transaction)

  CompactSize
    A type of variable-length integer commonly used in the Bitcoin P2P protocol and Bitcoin serialized data structures.

    **Not to be confused with:** VarInt (a data type Bitcoin Core uses for local data storage), Compact (the data type used for nBits in the block header)

  Compressed public key
    An ECDSA public key that is 33 bytes long rather than the 65 bytes of an uncompressed public key.

  Confirmation score
  Confirmations
  Confirmed transaction
  Unconfirmed transaction
    A score indicating the number of blocks on the best block chain that would need to be modified to remove or modify a particular transaction. A confirmed transaction has a confirmation score of one or higher.

# Consensus
* == SEVERAL nodes (NORMALLY MOST network's nodes) / 👀have the SAME blocks | their locally-validated blockchain👀
* != 
  * Social consensus
  * Consensus rules

# Consensus rules
* == block validation rules / 👀FULL nodes follow -- to -- stay in consensus WITH OTHER nodes👀

    Child pays for parent
    CPFP
    Ancestor mining
      Selecting transactions for mining not just based on their fees but also based on the fees of their ancestors (parents) and descendants (children).

      **Not to be confused with:** Replace by Fee, RBF

# Denomination / Bitcoins / Satoshis
* == Bitcoin value naming
* units
  * bitcoin 
  * satoshi
    * 1 bitcoin = 100,000,000 satoshis

      **Not to be confused with:** Binary bits, a unit of data with two possible values

# Difficulty / Network difficulty
* == how difficult it is to find a block vs difficulty of finding the easiest possible block
  * easiest possible block
    * := that one / proof-of-work difficulty = 1
* != Target threshold

      DNS seed
        A DNS server which returns IP addresses of full nodes on the Bitcoin network to assist in peer discovery.

        **Not to be confused with:** HD wallet seeds

      Double spend
        A transaction that uses the same input as an already broadcast transaction. The attempt of duplication, deceit, or conversion, will be adjudicated when only one of the transactions is recorded in the blockchain.

      Escrow contract
        A transaction in which a spender and receiver place funds in a 2-of-2 (or other m-of-n) multisig output so that neither can spend the funds until they're both satisfied with some external outcome.

      Extended key
      Public extended key
      Private extended key
        In the context of HD wallets, a public key or private key extended with the chain code to allow them to derive child keys.

      Fork
        When two or more blocks have the same block height, forking the block chain.  Typically occurs when two or more miners find blocks at nearly the same time.  Can also happen as part of an attack.

        **Not to be confused with:** Hard fork (a change in consensus rules that breaks security for nodes that don't upgrade), Soft fork (a change in consensus rules that weakens security for nodes that don't upgrade), Software fork (when one or more developers permanently develops a codebase separately from other developers), Git fork (when one or more developers temporarily develops a codebase separately from other developers)

      Genesis block
      Block 0
        The first block in the Bitcoin block chain.

        **Not to be confused with:** Generation transaction (the first transaction in a block)

      Hard fork
        A permanent divergence in the block chain, commonly occurs when non-upgraded nodes can't validate blocks created by upgraded nodes that follow newer consensus rules.

        **Not to be confused with:** Fork (a regular fork where all nodes follow the same consensus rules, so the fork is resolved once one chain has more proof of work than another), Soft fork (a temporary divergence in the block chain caused by non-upgraded nodes not following new consensus rules), Software fork (when one or more developers permanently develops a codebase separately from other developers), Git fork (when one or more developers temporarily develops a codebase separately from other developers

      Hardened extended key
        A variation on HD wallet extended keys where only the hardened extended private key can derive child keys. This prevents compromise of the chain code plus any private key from putting the whole wallet at risk.

# HD protocol / HD wallet
* == Hierarchical Deterministic (HD) key creation + transfer protocol (BIP32)
  * allows
    * FROM parent keys | hierarchy,
      * create child keys 
* HD wallets
  * := Wallets / use the HD protocol 

    HD wallet seed
    Root seed
      A potentially-short value used as a seed to generate the master private key and master chain code for an HD wallet.

      **Not to be confused with:** Mnemonic code / mnemonic seed (a binary root seed formatted as words to make it easier for humans to transcribe and possibly remember)

    Header chain
    Best header chain
      A chain of block headers with each header linking to the header that preceded it; the most-difficult-to-recreate chain is the best header chain

      **Not to be confused with:** Block chain

    Headers-first sync
      Synchronizing the block chain by downloading block headers before downloading the full blocks.

      **Not to be confused with:** Blocks-first sync (Downloading entire blocks immediately without first getting their headers)

# High-priority transaction / Free transaction
* transactions 
  * / 
    * ❌NOT have to pay a transaction fee❌
    * their inputs accumulated | time -> HIGHER priority
  * miners 
    * can choose accept it

        Initial block download
        IBD
          The process used by a new node (or long-offline node) to download a large number of blocks to catch up to the tip of the best block chain.

          **Not to be confused with:** Blocks-first sync (syncing includes getting any amount of blocks; IBD is only used for large numbers of blocks)

# Input / TxIn
* == transaction's input /
  * 's fields
    * outpoint,
      * refer -- to -- PREVIOUS output
    * signature script,
      * spend part of outpoint
    * sequence number

# Internal byte order
* == standard order /
  * hash digests are displayed -- as -- strings
    * == 's format == serialized blocks & transactions' format
* != RPC byte order

  Inventory
    A data type identifier and a hash; used to identify transactions and blocks available for download through the Bitcoin P2P network.

    **Not to be confused with:** Inv message (one of the P2P messages that transmits inventories)

# Locktime / `nLockTime`
* == transaction's part /
  * the earliest time or earliest block | transaction may be added -- to the -- blockchain

    Mainnet
      The original and main network for Bitcoin transactions, where satoshis have real economic value.

      **Not to be confused with:** Testnet (an open network very similar to mainnet where satoshis have no value), Regtest (a private testing node similar to testnet)

    Transaction malleability
    Transaction mutability
      The ability of someone to change (mutate) unconfirmed transactions without making them invalid, which changes the transaction's txid, making child transactions invalid.

      **Not to be confused with:** BIP62 (a proposal for an optional new transaction version that reduces the set of known mutations for common transactions)

    Miner-activated soft fork
    MASF
      A Soft Fork activated by through miner signalling.

      **Not to be confused with:** User Activated Soft Fork (a soft fork activated by flag day or node enforcement instead of miner signalling.), Fork (a regular fork where all nodes follow the same consensus rules, so the fork is resolved once one chain has more proof of work than another), Hard fork (a permanent divergence in the block chain caused by non-upgraded nodes not following new consensus rules), Soft fork (a temporary divergence in the block chain caused by non-upgraded nodes not following new consensus rules), Software fork (when one or more developers permanently develops a codebase separately from other developers), Git fork (when one or more developers temporarily develops a codebase separately from other developers

    Master chain code
    Master private key
      In HD wallets, the master chain code and master private key are the two pieces of data derived from the root seed.

# Merkle block
* == partial merkle tree /
  * transactions / match a bloom filter, are connected  -- to the -- block's merkle root 
* != MerkleBlock message

# Merkle root
* == merkle tree's root node /
  * descendant of ALL hashed pairs | tree

* Block headers
  * ⚠️MUST include a valid merkle root⚠️

# Merkle tree
* tree
  * == hashing paired dataS (== leaves) -- TILL -- the merkle root

* Bitcoin's leaves
  * == (ALMOST ALWAYS) transactions -- from a -- 1 block

      Message header
        The four header fields prefixed to all messages on the Bitcoin P2P network.

      Minimum relay fee
      Relay fee
        The minimum transaction fee a transaction must pay (if it isn't a high-priority transaction) for a full node to relay that transaction to other nodes. There is no one minimum relay fee---each node chooses its own policy.

        **Not to be confused with:** Transaction fee (the minimum relay fee is a policy setting that filters out transactions with too-low transaction fees)

      Mining
      Miner
        Mining is the act of creating valid Bitcoin blocks, which requires demonstrating proof of work, and miners are devices that mine or people who own those devices.

# Multisig / Bare multisig
* == pubkey script /
  * provides
    * *n* number of pubkeys
  * requires
    * corresponding signature script -- provides -- >= *m* number signatures / correspond to the provided pubkeys
  * ❌NOT use P2SH encapsulation❌
* != 
  * P2SH multisig 
  * advanced scripts / require MULTIPLE signatures -- WITHOUT using -- `OP_CHECKMULTISIG` or `OP_CHECKMULTISIGVERIFY`

# nBits / Target
* target
  * == threshold / 
    * if block header hash < this threshold -> block is valid
* nBits
  * == target threshold's encoded form /
    * appears | block header

* != Difficulty

        Node
        Full node
        Archival node
        Pruned node
        Peer
          A computer that connects to the Bitcoin network.

          **Not to be confused with:** Lightweight node, SPV node

# Null data transaction / `OP_RETURN` transaction / Data carrier transaction
* transaction type / 
  * relayed
  * mined, by default, | Bitcoin Core 0.9.0
  * adds arbitrary data | provably unspendable pubkey script
    * -> FULL nodes do NOT have to store | their UTXO database

* != `OP_RETURN`

        Opcode
        Data-pushing opcode
        Non-data-pushing opcode
          Operation codes from the Bitcoin Script language which push data or perform functions within a pubkey script or signature script.

        Orphan block
          Blocks whose parent block has not been processed by the local node, so they can't be fully validated yet.

          **Not to be confused with:** Stale block

# Outpoint
* == data structure 
  * uses
    * refer -- to a -- particular transaction output
  * == 👀32-byte TXID + 4-byte output index number (vout)👀

* != Output / TxOut 

# Output / TxOut
* == transaction's output /
  * 's fields
    * value field
      * == satoshis (>=0) / are transferred
    * pubkey script
      * == required conditions -- to spend -- those satoshis
* == superset of [UTXOs](#utxo)
* != [Outpoint](#outpoint)

# P2PK output
* == output / pay DIRECTLY a public key 

# P2PKH address / P2PKH output
* == Bitcoin payment address /
  * == comprised hashed public key
  * enable the spender
    * create a standard pubkey script /
      * Pays To PubKey Hash (P2PKH)
* !=
  * P2PK output
  * P2SH address / P2SH output

# P2SH address / P2SH output
* := Bitcoin payment address /
  * == comprised hashed script + its output
  * enable the spender
    * create a standard pubkey script /
      * Pays To Script Hash (P2SH)
      * 👀ALMOST ANY valid pubkey script👀

* != 
  * P2PK output
  * P2PKH address / P2PKH output
  * P2SH multisig

# P2SH multisig
* == P2SH output /
  * redeem script -- uses -- 1 multisig opcodes
* == multisig script | P2SH
* | 
  * Bitcoin Core 0.10.0-,
    * P2SH multisig scripts == standard transactions
  * Bitcoin Core 0.10.0+,
    * P2SH multisig scripts != standard transactions

* != 
  * Multisig pubkey scripts, P2SH (general P2SH, of which P2SH multisig is a specific instance that was special cased up until Bitcoin Core 0.10.0)

# Parent key / Parent public key / Parent private key
* | HD wallets,
  * key 
    * uses
      * derive child keys
    * types
      * private key
      * public key
* != Public key

# Payment protocol / Payment request
* ⚠️deprecated protocol ⚠️
  * uses |
    * early versions of Bitcoin
  * Reason: 🧠insecure, discontinued protocol🧠 
* defined | BIP70
* lets spenders
  * get signed payment details -- from -- receivers
* != IP-to-IP payment protocol 

# Private key
* == keypair's private portion /
  * create signatures / OTHER people can -- , via the public key, -- verify 
* != 
  * Public key
  * Parent key
    * (a key used to create child keys, not necessarily a private key)

# Proof of work / POW
* TODO: hash below a target value / can only be obtained, on average, by performing a certain amount of brute force work---therefore demonstrating proof of work.

# Pubkey script / ScriptPubKey
* == script / 
  * included | outputs
  * 👀sets the conditions -- to spend -- satoshis👀
    * data / match the conditions -- are -- provided | script's signature 
* `scriptPubKey`
  * name | code
* != Pubkey

# Public key
* == keypair's public portion
  * derived -- from the -- private key 
  * uses
    * verify signatures / made with the keypair's private portion 
    * 👀part of a pubkey script👀
* ❌NOT provide a❌
  * programmable authentication mechanism
* != 
  * Private key
  * Parent key (a key used to create child keys, not necessarily a public key)

        Replace by fee
        RBF
        Opt-in replace by fee
          Replacing one version of an unconfirmed transaction with a different version of the transaction that pays a higher transaction fee.  May use BIP125 signaling.

          **Not to be confused with:** Child pays for parent, CPFP

# Redeem script / RedeemScript
* == script /
  * 's function == pubkey script's function
  * uses
    * create a P2SH address
      * used | actual pubkey script
      * steps
        * copy it
        * hash 
    * place | spending signature script
      * steps
        * copy it
      * enforce its conditions

* != Signature script

              Regtest
              Regression test mode
                A local testing environment in which developers can almost instantly generate blocks on demand for testing events, and can create private satoshis with no real-world value.

                **Not to be confused with:** Testnet (a global testing environment which mostly mimics mainnet)

# RPC byte order
* == hash digest / 
  * displayed -- with the -- byte order reversed
  * uses |
    * Bitcoin Core RPCs
    * block explorers
    * other software
* != Internal byte order

                Sequence number
                  Part of all transactions. A number intended to allow unconfirmed time-locked transactions to be updated before being finalized; not currently used except to disable locktime in a transaction

                  **Not to be confused with:** Output index number / vout (this is the 0-indexed number of an output within a transaction used by a later transaction to refer to that specific output)

                Serialized block
                  A complete block in its binary format---the same format used to calculate total block byte size; often represented using hexadecimal.

# Serialized transaction / Raw transaction
* == WHOLE transactions / binary format
  * represented -- via -- hexadecimal
* raw format
  * Reason: 🧠Bitcoin Core commands / 's names has "raw"🧠

                  SIGHASH_ALL
                    Default signature hash type which signs the entire transaction except any signature scripts, preventing modification of the signed parts.

                  SIGHASH_ANYONECANPAY
                    A signature hash type which signs only the current input.

                    **Not to be confused with:** SIGHASH_SINGLE (which signs this input, its corresponding output, and other inputs partially)

                  SIGHASH_NONE
                    Signature hash type which only signs the inputs, allowing anyone to change the outputs however they'd like.

                  SIGHASH_SINGLE
                    Signature hash type that signs the output corresponding to this input (the one with the same index value), this input, and any other inputs partially. Allows modification of other outputs and the sequence number of other inputs.

                    **Not to be confused with:** SIGHASH_ANYONECANPAY (a flag to signature hash types that only signs this single input)

                  Signature
                    A value related to a public key which could only have reasonably been created by someone who has the private key that created that public key. Used in Bitcoin to authorize spending satoshis previously sent to a public key.

                  Signature hash
                  Sighash
                    A flag to Bitcoin signatures that indicates what parts of the transaction the signature signs.  (The default is SIGHASH_ALL.) The unsigned parts of the transaction may be modified.

                    **Not to be confused with:** Signed hash (a hash of the data to be signed), Transaction malleability / transaction mutability (although non-default sighash flags do allow optional malleability, malleability comprises any way a transaction may be mutated)

# Signature script / ScriptSig
* == data /
  * generated -- by a -- spender
  * uses
    * as variable -- to satisfy a -- pubkey script
  * provides
    * data | pubkey script / includes the redeem script | P2SH input 
* `ScriptSig`
  * named | code

* != ECDSA signature

              SPV
              Simplified Payment Verification
              Lightweight client
              Thin client
                A method for verifying if particular transactions are included in a block without downloading the entire block.  The method is used by some lightweight Bitcoin clients.

              Soft fork
                A softfork is a change to the bitcoin protocol wherein only previously valid blocks/transactions are made invalid. Since old nodes will recognise the new blocks as valid, a softfork is backward-compatible.

                **Not to be confused with:** Fork (a regular fork where all nodes follow the same consensus rules, so the fork is resolved once one chain has more proof of work than another), Hard fork (a permanent divergence in the block chain caused by non-upgraded nodes not following new consensus rules), Software fork (when one or more developers permanently develops a codebase separately from other developers), Git fork (when one or more developers temporarily develops a codebase separately from other developers

              Stale block
                Blocks which were successfully mined but which aren't included on the current best block chain, likely because some other block at the same height had its chain extended first.

                **Not to be confused with:** Orphan block (a block whose previous (parent) hash field points to an unknown block, meaning the orphan can't be validated)

# Standard Transaction
* == transaction /
  * passes Bitcoin Core's `IsStandard()` & `IsStandardTx()` tests
* are mined OR broadcasted by
  * ONLY peers / run the default Bitcoin Core software 

                Start string
                Network magic
                  Four defined bytes which start every message in the Bitcoin P2P protocol to allow seeking to the next message.

                Testnet
                  A global testing environment in which developers can obtain and spend satoshis that have no real-world value on a network that is very similar to the Bitcoin mainnet.

                  **Not to be confused with:** Regtest (a local testing environment where developers can control block generation)

                Token
                  A token is a programmable digital asset with its own codebase that resides on an already existing block chain. Tokens are used to help facilitate the creation of decentralized applications.

                  **Not to be confused with:** Bitcoins, Satoshis, Security token, Denominations

# Transaction fee / Miners fee
* == amount remaining
  * == transaction's ALL inputs - transaction's ALL outputs
  * paid -- to the -- miner
* != Minimum relay fee

# Txid
* == identifier
  * uses
    * uniquely identify -- a -- particular transaction
  * == transaction's sha256d hash 

* != [Outpoint](#outpoint)

    User-activated soft fork
    UASF
      A Soft Fork activated by flag day or node enforcement instead of miner signalling.

      **Not to be confused with:** Miner Activated Soft Fork (a soft fork activated through miner signalling), Fork (a regular fork where all nodes follow the same consensus rules, so the fork is resolved once one chain has more proof of work than another), Hard fork (a permanent divergence in the block chain caused by non-upgraded nodes not following new consensus rules), Soft fork (a temporary divergence in the block chain caused by non-upgraded nodes not following new consensus rules), Software fork (when one or more developers permanently develops a codebase separately from other developers), Git fork (when one or more developers temporarily develops a codebase separately from other developers

# UTXO
* := Unspent Transaction Output /
  * can be spent | NEW transaction's input
* != Output 

# Wallet
* := software / 
  * stores private keys
  * monitors the blockchain
    * ways
      * client of a server / does the processing
    * Reason: 🧠enable users -- to -- spend & receive satoshis🧠

* != HD wallet
  * (a protocol that allows all of a wallet's keys to be created from a single seed)

            WIF
            Wallet Import Format
              A data interchange format designed to allow exporting and importing a single private key with a flag indicating whether or not it uses a compressed public key.

              **Not to be confused with:** Extended private keys (which allow importing a hierarchy of private keys)

            Watch-only address
              An address or pubkey script stored in the wallet without the corresponding private key, allowing the wallet to watch for outputs but not spend them.
  
            Bitcoin URI
              A URI which allows receivers to encode payment details so spenders don't have to manually enter addresses and other details.

            Certificate chain
              A chain of certificates connecting a individual's leaf certificate to the certificate authority's root certificate.

            Coinbase block height
              The current block's height encoded into the first bytes of the coinbase field.

            Fiat
              National currencies such as the dollar or euro.

            Intermediate certificate
              A intermediate certificate authority certificate which helps connect a leaf (receiver) certificate to a root certificate authority.

            Key index
              An index number used in the HD wallet formula to generate child keys from a parent key.

            Key pair
              A private key and its derived public key.

            Label
              The label parameter of a bitcoin: URI which provides the spender with the receiver's name (unauthenticated).

            Leaf certificate
              The end-node in a certificate chain; in the payment protocol, it is the certificate belonging to the receiver of satoshis.

            Merge
              Spending, in the same transaction, multiple outputs which can be traced back to different previous spenders, leaking information about how many satoshis you control.

            Merge avoidance
              A strategy for selecting which outputs to spend that avoids merging outputs with different histories that could leak private information.

            Message
              A parameter of bitcoin: URIs which allows the receiver to optionally specify a message to the spender.

            Micropayment channel
              term-micropayment-channel (contracts-guide) (`original target <https://bitcoin.org/en/contracts-guide#term-micropayment-channel>`__)

            OP CHECKMULTISIG
              Opcode which returns true if one or more provided signatures (m) sign the correct parts of a transaction and match one or more provided public keys (n).

            Output index
              The sequentially-numbered index of outputs in a single transaction starting from 0.


            PKI
              Public Key Infrastructure; usually meant to indicate the X.509 certificate system used for HTTP Secure (https).

            Point function
              The ECDSA function used to create a public key from a private key.

            PP amount
              Part of the Output part of the PaymentDetails part of a payment protocol where receivers can specify the amount of satoshis they want paid to a particular pubkey script.

            PP expires
              The expires field of a PaymentDetails where the receiver tells the spender when the PaymentDetails expires.

            PP memo
              The memo fields of PaymentDetails, Payment, and PaymentACK which allow spenders and receivers to send each other memos.

# PP merchant data
* == PaymentDetails' merchant_data & Payment's merchant_data 
  * allows
    * receiver 
      * can send arbitrary data -- to the -- spender | PaymentDetails 
      * receive it back | Payments

                  PP pki data
                    The pki_data field of a PaymentRequest which provides details such as certificates necessary to validate the request.

                  PP pki type
                    The PKI field of a PaymentRequest which tells spenders how to validate this request as being from a specific recipient.

                  PP script
                    The script field of a PaymentDetails where the receiver tells the spender what pubkey scripts to pay.

                  Previous block header hash
                    A field in the block header which contains the SHA256(SHA256()) hash of the previous block's header.

                  R parameter
                    The payment request parameter in a bitcoin: URI.

                  Receipt
                    A cryptographically-verifiable receipt created using parts of a payment request and a confirmed transaction.

                  Root certificate
                    A certificate belonging to a certificate authority (CA).

                  SSL signature
                    Signatures created and recognized by major SSL implementations such as OpenSSL.

                  Stanndard block relay
                    The regular block relay method: announcing a block with an inv message and waiting for a response.

# Transaction version number
* == version number / prefix the transactions
  * allow
    * upgrading

                      Unique Address
                        Address which are only used once to protect privacy and increase security.

                      Unsolicited block push
                        When a miner sends a block message without sending an inv message first.

                      URI qr code
                        A QR code containing a bitcoin: URI.

                      V2 block 
                        The current version of Bitcoin blocks.

                      x509certificates

                      term-x509certificates (developer-examples) (`original target <https://bitcoin.org/en/developer-examples#term-x509certificates>`__)

