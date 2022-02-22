# JUNO

| DOWNLOAD  | file name | chain id | pruning | size | date | hash
| --------- | --------- | -------- | ------- | ---- | ---- | --- |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/juno-1_20220222_pruned.tar.lz4) | juno-1_20220222_pruned.tar.lz4 | juno-1 | pruned | 104 GB  | 2022/02/22 | fc62f6d1fc07eae96c9582387f76e920 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/juno-1_20220222_pruned.tar.lz4) | juno-1_20220222_pruned.tar.lz4 | juno-1 | pruned | 104 GB  | 2022/02/22 | fc62f6d1fc07eae96c9582387f76e920 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/juno-1_20220222_pruned.tar.lz4) | juno-1_20220222_pruned.tar.lz4 | juno-1 | pruned | 104 GB  | 2022/02/22 | fc62f6d1fc07eae96c9582387f76e920 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/juno-1_20220221_pruned.tar.lz4) | juno-1_20220221_pruned.tar.lz4 | juno-1 | pruned | 104 GB  | 2022/02/21 | fc62f6d1fc07eae96c9582387f76e920 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/juno-1_20220221_pruned.tar.lz4) | juno-1_20220221_pruned.tar.lz4 | juno-1 | pruned | 104 GB  | 2022/02/21 | fc62f6d1fc07eae96c9582387f76e920 |
| [DOWNLOAD](https://quicksync.ccvalidators.com/SNAPSHOTS/juno-1_20220221_pruned.tar.lz4) | juno-1_20220221_pruned.tar.lz4 | juno-1 | pruned | 104 GB  | 2022/02/21 | fc62f6d1fc07eae96c9582387f76e920 |

---
## download instructions

```bash
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
```bash
cd ~/.juno
rm -r data
wget -O - $URL | lz4 -d | tar -xvf -
junod start
```
