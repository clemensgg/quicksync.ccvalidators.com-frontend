# COSMOS
 
| DOWNLOAD  | date | chain id | db backend | pruning | size | file name | hash |
| --------- | ---- | -------- | ---------- | ------- | ---- | --------- | ---- |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/cosmoshub-4_20220210_default.tar.lz4) | 2022/02/10 | cosmoshub-4 | rocksdb | default | 331G | cosmoshub-4_20220210_default.tar.lz4 | 81848d8efff4522eaa886015f7029a8b |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/cosmoshub-4_20220210_pruned.tar.lz4) | 2022/02/10 | cosmoshub-4 | rocksdb | pruned | 289G | cosmoshub-4_20220210_pruned.tar.lz4 | 64d4009844170bb4cddd6a74adf2e434 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/cosmoshub-4_20220213_archive.tar.lz4) | 2022/02/13 | cosmoshub-4 | rocksdb | archive | 1171G | cosmoshub-4_20220213_archive.tar.lz4 | 3ae3b7ceea587881bbe9cf9c7eb817c7 |
 
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
