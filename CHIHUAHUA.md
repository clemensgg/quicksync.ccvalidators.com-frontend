# CHIHUAHUA
 
| DOWNLOAD  | date | chain id | db backend | pruning | size | file name | hash |
| --------- | ---- | -------- | ---------- | ------- | ---- | --------- | ---- |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220225_default.tar.lz4) | 2022/02/25 | chihuahua-1 | rocksdb | default | 238G | chihuahua-1_20220225_default.tar.lz4 | 40223e2b65312f05246c0821053c322d |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220226_archive.tar.lz4) | 2022/02/26 | chihuahua-1 | rocksdb | archive | 312G | chihuahua-1_20220226_archive.tar.lz4 | 5dd194882a97309206d9e7a013595f72 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220226_default.tar.lz4) | 2022/02/26 | chihuahua-1 | rocksdb | default | 242G | chihuahua-1_20220226_default.tar.lz4 | e9cc42665acfb4c4608d66861bbca0c5 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220226_pruned.tar.lz4) | 2022/02/26 | chihuahua-1 | rocksdb | pruned | 91G | chihuahua-1_20220226_pruned.tar.lz4 | d753e93674d55e6cab147a37ed2d9fcf |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220227_archive.tar.lz4) | 2022/02/27 | chihuahua-1 | rocksdb | archive | 318G | chihuahua-1_20220227_archive.tar.lz4 | fac28fdb098526e291b8fbe31999085e |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220227_pruned.tar.lz4) | 2022/02/27 | chihuahua-1 | rocksdb | pruned | 92G | chihuahua-1_20220227_pruned.tar.lz4 | 6d32728bff7c7c7b5e6cbad23ded963d |
 
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
