# CHIHUAHUA
 
| DOWNLOAD  | date | chain id | db backend | pruning | size | file name | hash |
| --------- | ---- | -------- | ---------- | ------- | ---- | --------- | ---- |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220303_archive.tar.lz4) | 2022/03/03 | chihuahua-1 | rocksdb | archive | 340G | chihuahua-1_20220303_archive.tar.lz4 | d83e1e3b16308f08c42170a20bfdd026 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220303_default.tar.lz4) | 2022/03/03 | chihuahua-1 | rocksdb | default | 270G | chihuahua-1_20220303_default.tar.lz4 | 60aecb0464955b3c70a94ef4258b8bd1 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220303_pruned.tar.lz4) | 2022/03/03 | chihuahua-1 | rocksdb | pruned | 99G | chihuahua-1_20220303_pruned.tar.lz4 | ad001c3341e82a1bf8c8f315ecd4d6ab |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220304_archive.tar.lz4) | 2022/03/04 | chihuahua-1 | rocksdb | archive | 345G | chihuahua-1_20220304_archive.tar.lz4 | 8fd5d8a52a59a9ea7bafc3760bc5aa09 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220304_default.tar.lz4) | 2022/03/04 | chihuahua-1 | rocksdb | default | 277G | chihuahua-1_20220304_default.tar.lz4 | b80d0b889f47c3008235378102c208f1 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/chihuahua-1_20220304_pruned.tar.lz4) | 2022/03/04 | chihuahua-1 | rocksdb | pruned | 100G | chihuahua-1_20220304_pruned.tar.lz4 | 415754824ba7ab7a32ae62648f96873d |
 
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
