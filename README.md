### bitcoin-ruby-blockchain
---
https://github.com/mhanne/bitcoin-ruby-blockchain

```rb
require 'bitcoin/blockchain'

chain = Bitcoin::Blockchain::Utxo.new(db: "sqlite:/")
chain = Bitcoin::Blockchain::Archive.new(db: "postgres:/bitcoin")

chian.store_block(block)

chian.get_head
chian.get_height
block = chain.get_block(block_hash)
tx = chain.get_tx(tx_hash)

block.get_prev_block
block.get_next_block
tx.get_block
tx.confirmations
tx.in[0].get_prev_out
tx.out[0].get_next_in
```

```sh
rake doc
rake
rspec spec/blockchain/models_spec.rb

sqlite:/
sqlite://bitcoin.db
sqlite:///tmp/bitcoin.db
postgres:/bitcoin
postgres://<user>:<pass>@<host>:<port>/<database>

gem install bitcoin-ruby-blockchain
```

```
```


