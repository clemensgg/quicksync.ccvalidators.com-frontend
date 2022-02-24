# TERRA
 
| DOWNLOAD  | date | chain id | db backend | pruning | size | file name | hash |
| --------- | ---- | -------- | ---------- | ------- | ---- | --------- | ---- |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/columbus-5_20220210_default.tar.lz4) | 2022/02/10 | columbus-5 | rocksdb | default | 811G | columbus-5_20220210_default.tar.lz4 | 714756245fb01b5e0d99f45a3e29db93 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/columbus-5_20220211_pruned.tar.lz4) | 2022/02/11 | columbus-5 | rocksdb | pruned | 372G | columbus-5_20220211_pruned.tar.lz4 | 89692a5c38ab168c9e011a4f08af03b0 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/columbus-5_20220212_archive.tar.lz4) | 2022/02/12 | columbus-5 | rocksdb | archive | 1329G | columbus-5_20220212_archive.tar.lz4 | 8bcb4b988674b88f5accac478b2b4629 |
 
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
