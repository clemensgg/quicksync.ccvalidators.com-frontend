# CHIHUAHUA
 
| DOWNLOAD  | date | chain id | db backend | pruning | size | file name | hash |
| --------- | ---- | -------- | ---------- | ------- | ---- | --------- | ---- |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220304_default.tar.lz4) | 2022/03/04 | chihuahua-1 | rocksdb | default | 277G | chihuahua-1_20220304_default.tar.lz4 | b80d0b889f47c3008235378102c208f1 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220305_archive.tar.lz4) | 2022/03/05 | chihuahua-1 | rocksdb | archive | 351G | chihuahua-1_20220305_archive.tar.lz4 | 8b4ee053ddd1c4fb8b2b420d597038ef |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220305_default.tar.lz4) | 2022/03/05 | chihuahua-1 | rocksdb | default | 283G | chihuahua-1_20220305_default.tar.lz4 | aca8b19930f28810de0b66fc1f80d3ce |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220305_pruned.tar.lz4) | 2022/03/05 | chihuahua-1 | rocksdb | pruned | 102G | chihuahua-1_20220305_pruned.tar.lz4 | 42b5b161fc2d1984f0ee840839ac557d |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220306_archive.tar.lz4) | 2022/03/06 | chihuahua-1 | rocksdb | archive | 357G | chihuahua-1_20220306_archive.tar.lz4 | 37acc970f31068b816d7429381f0fe6b |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220306_pruned.tar.lz4) | 2022/03/06 | chihuahua-1 | rocksdb | pruned | 103G | chihuahua-1_20220306_pruned.tar.lz4 | dceab6c3e1fc5c7aa074630540da36d8 |
 
---
## download instructions
 
```sh
sudo apt install aria2 lz4
$URL=<paste URL>
cd $HOME/.chihuahua
rm -r data
aria2c -x5 $URL
md5sum `basename $URL`
lz4 -d `basename $URL` | tar xf -
chihuahuad start
```
*or (single-stream, no double disk-space needed, but no possibility to check hash)*
```sh
cd $HOME/.chihuahua
rm -r data
wget -O - $URL | lz4 -d | tar -xvf -
chihuahuad start
```
 
---
## rocksdb
 
- Install instructions for Ubuntu: [checkout this gist](https://gist.github.com/clemensgg/907de16baa203946633ddca462cbf597)
- Cosmos go-rocksdb repo: https://github.com/cosmos/gorocksdb
