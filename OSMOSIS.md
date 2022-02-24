# OSMOSIS
 
| DOWNLOAD  | date | chain id | db backend | pruning | size | file name | hash |
| --------- | ---- | -------- | ---------- | ------- | ---- | --------- | ---- |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/osmosis-1_20220210_default.tar.lz4) | 2022/02/10 | osmosis-1 | rocksdb | default | 730G | osmosis-1_20220210_default.tar.lz4 | 7c2913d9d29bfb86d06c277aef91c7ed |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/osmosis-1_20220210_pruned.tar.lz4) | 2022/02/10 | osmosis-1 | rocksdb | pruned | 129G | osmosis-1_20220210_pruned.tar.lz4 | eb61d655161c76a32324e95d2848fa20 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/osmosis-1_20220212_archive.tar.lz4) | 2022/02/12 | osmosis-1 | rocksdb | archive | 1452G | osmosis-1_20220212_archive.tar.lz4 | 1fd86b89e759915146d11484d192ef2d |
 
---
## download instructions
 
```sh
sudo apt install aria2 lz4
$URL=<paste URL>
cd ~/.juno
rm -r data
aria2c -x5 $URL
md5sum `basename $URL`
lz4 -d `basename $URL` | tar xf -
junod start
```
*or (single-stream, no double disk-space needed, but no possibility to check hash)*
```sh
cd ~/.juno
rm -r data
wget -O - $URL | lz4 -d | tar -xvf -
junod start
```
 
---
## rocksdb
 
- Install instructions for Ubuntu: [checkout this gist](https://gist.github.com/clemensgg/907de16baa203946633ddca462cbf597)
- Cosmos go-rocksdb repo: https://github.com/cosmos/gorocksdb
