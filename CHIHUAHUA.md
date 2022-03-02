# CHIHUAHUA
 
| DOWNLOAD  | date | chain id | db backend | pruning | size | file name | hash |
| --------- | ---- | -------- | ---------- | ------- | ---- | --------- | ---- |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220301_archive.tar.lz4) | 2022/03/01 | chihuahua-1 | rocksdb | archive | 328G | chihuahua-1_20220301_archive.tar.lz4 | 73d4dd68846dea42c53b0d36cd675314 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220301_default.tar.lz4) | 2022/03/01 | chihuahua-1 | rocksdb | default | 260G | chihuahua-1_20220301_default.tar.lz4 | 702bb0676ca88b2ff3f635304c5b7e53 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220301_pruned.tar.lz4) | 2022/03/01 | chihuahua-1 | rocksdb | pruned | 96G | chihuahua-1_20220301_pruned.tar.lz4 | 95bebf30779b1177a69783a939f137bd |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220302_archive.tar.lz4) | 2022/03/02 | chihuahua-1 | rocksdb | archive | 334G | chihuahua-1_20220302_archive.tar.lz4 | d48e9b60118b7d1c021cb8cbe4e0643b |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220302_default.tar.lz4) | 2022/03/02 | chihuahua-1 | rocksdb | default | 264G | chihuahua-1_20220302_default.tar.lz4 | 67dd9d19c3e2d1d86f4d6a7a3b61f6f4 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220302_pruned.tar.lz4) | 2022/03/02 | chihuahua-1 | rocksdb | pruned | 97G | chihuahua-1_20220302_pruned.tar.lz4 | bcd6f3f0607f241fa844c27e308463e8 |
 
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
