# CHIHUAHUA
 
| DOWNLOAD  | date | chain id | db backend | pruning | size | file name | hash |
| --------- | ---- | -------- | ---------- | ------- | ---- | --------- | ---- |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220227_default.tar.lz4) | 2022/02/27 | chihuahua-1 | rocksdb | default | 247G | chihuahua-1_20220227_default.tar.lz4 | 2ffce55504833edd223eefd203878e82 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220227_pruned.tar.lz4) | 2022/02/27 | chihuahua-1 | rocksdb | pruned | 92G | chihuahua-1_20220227_pruned.tar.lz4 | 6d32728bff7c7c7b5e6cbad23ded963d |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220228_archive.tar.lz4) | 2022/02/28 | chihuahua-1 | rocksdb | archive | 323G | chihuahua-1_20220228_archive.tar.lz4 | 5d82b15c02706230d02932c5b01c8e64 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220228_default.tar.lz4) | 2022/02/28 | chihuahua-1 | rocksdb | default | 254G | chihuahua-1_20220228_default.tar.lz4 | 3a21a5f4ec78aedbb40f3519c5aafe04 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220228_pruned.tar.lz4) | 2022/02/28 | chihuahua-1 | rocksdb | pruned | 94G | chihuahua-1_20220228_pruned.tar.lz4 | 57bbbd31749953bdbe4a35636318913c |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220301_archive.tar.lz4) | 2022/03/01 | chihuahua-1 | rocksdb | archive | 328G | chihuahua-1_20220301_archive.tar.lz4 | 73d4dd68846dea42c53b0d36cd675314 |
 
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
