# JUNO
 
| DOWNLOAD  | date | chain id | db backend | pruning | size | file name | hash |
| --------- | ---- | -------- | ---------- | ------- | ---- | --------- | ---- |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/juno-1_20220223_archive.tar.lz4) | 2022/02/23 | juno-1 | rocksdb | archive | 566G | juno-1_20220223_archive.tar.lz4 | f5d42284c8b5d37058e3a15c42994f92 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/juno-1_20220223_default.tar.lz4) | 2022/02/23 | juno-1 | rocksdb | default | 382G | juno-1_20220223_default.tar.lz4 | 9117a0c8aaaca6e90f1614474cfe4694 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/juno-1_20220223_pruned.tar.lz4) | 2022/02/23 | juno-1 | rocksdb | pruned | 171G | juno-1_20220223_pruned.tar.lz4 | 1c626ca8e862c12e64cc4d52dd577f67 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/juno-1_20220224_archive.tar.lz4) | 2022/02/24 | juno-1 | rocksdb | archive | 601G | juno-1_20220224_archive.tar.lz4 | 12f79d8d4e1762f077dc78b46bc2f3e3 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/juno-1_20220224_default.tar.lz4) | 2022/02/24 | juno-1 | rocksdb | default | 402G | juno-1_20220224_default.tar.lz4 | db56e613c7da2906c8bf8e81cd5609aa |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/juno-1_20220224_pruned.tar.lz4) | 2022/02/24 | juno-1 | rocksdb | pruned | 172G | juno-1_20220224_pruned.tar.lz4 |  |
 
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
