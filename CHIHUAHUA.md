# CHIHUAHUA
 
| DOWNLOAD  | date | chain id | db backend | pruning | size | file name | hash |
| --------- | ---- | -------- | ---------- | ------- | ---- | --------- | ---- |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220222_default.tar.lz4) | 2022/02/22 | chihuahua-1 | rocksdb | default | 223G | chihuahua-1_20220222_default.tar.lz4 | 1fadc36f4e507ef078fd5cc06da1c5ce |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220223_archive.tar.lz4) | 2022/02/23 | chihuahua-1 | rocksdb | archive | 296G | chihuahua-1_20220223_archive.tar.lz4 | e65cce6aaf8efe3a34f65f7c45752ee8 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220223_default.tar.lz4) | 2022/02/23 | chihuahua-1 | rocksdb | default | 228G | chihuahua-1_20220223_default.tar.lz4 | c3a81ca8b55694a3f16eccf9672b13fd |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220223_pruned.tar.lz4) | 2022/02/23 | chihuahua-1 | rocksdb | pruned | 86G | chihuahua-1_20220223_pruned.tar.lz4 | 5635a3cdd02be4957cef86287692091b |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220224_archive.tar.lz4) | 2022/02/24 | chihuahua-1 | rocksdb | archive | 302G | chihuahua-1_20220224_archive.tar.lz4 | 08ce5ed593d1b4eb138b2ed7713bd32d |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220224_pruned.tar.lz4) | 2022/02/24 | chihuahua-1 | rocksdb | pruned | 88G | chihuahua-1_20220224_pruned.tar.lz4 | 2f1757d81c13fb2c84bad25a43d5b4b1 |
 
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
