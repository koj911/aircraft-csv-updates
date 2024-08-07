# aircraft-csv-updates

/usr/local/share/tar1090/aircraft.csv.gz の情報で気になる部分を修正するパッチを提供しています。
提供者が見てる範囲で気になるものを修正しているのでほとんどの人には期待外れでしょう。

This repository provides patches to address areas of `/usr/local/share/tar1090/aircraft.csv.gz` that the provider found noteworthy. These patches are based on the provider's observations and may not meet everyone's expectations.

## パッチの適用方法 / How to Apply the Patch
```
gzip -d -k aircraft.csv.gz
curl https://raw.githubusercontent.com/koj911/aircraft-csv-updates/main/aircraft.csv.diff | patch -u aircraft.csv
gzip --best -k aircraft.csv
rm aircraft.csv
```
