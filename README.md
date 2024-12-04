# aircraft-csv-updates

/usr/local/share/tar1090/aircraft.csv.gz の情報で気になる部分を修正するパッチを提供しています。
提供者が見てる範囲で気になるものを修正しているのでほとんどの人には期待外れでしょう。

This repository provides patches to address areas of `/usr/local/share/tar1090/aircraft.csv.gz` that the provider found noteworthy. These patches are based on the provider's observations and may not meet everyone's expectations.

当初、パッチだけおいてましたが、パッチを当てるためのaircraft.csv.gzがパッチ作成時のものとの差が大きいとパッチを当てるのも一苦労なのがわかったので、修正済みのaircraft.csv.gzも置くことにしました。
(以前からreleaseには含めていましたが、取得用のURLがreleaseごとに変わるってめんどくさいので)

Initially, I only posted the patch, but I realized that it would be difficult to apply the patch if the difference between the aircraft.csv.gz used to apply the patch and the one at the time of patch creation was large, so I created a modified aircraft.csv. I decided to put .gz as well.
(I've included it in releases for a while, but it's a pain because the URL to get it changes with each release.)

## パッチの適用方法 / How to Apply the Patch
```
gzip -d -k aircraft.csv.gz
curl https://raw.githubusercontent.com/koj911/aircraft-csv-updates/main/aircraft.csv.diff | patch -u aircraft.csv
gzip --best -k aircraft.csv
rm aircraft.csv
```
