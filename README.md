# aircraft-csv-updates

/usr/local/share/tar1090/aircraft.csv.gz の情報で気になる部分を修正するパッチを提供しています。
提供者が見てる範囲で気になるものを修正しているのでほとんどの人には期待外れでしょう。

##　パッチの適用方法 
```sh
gzip -d -k aircraft.csv.gz
curl https://raw.githubusercontent.com/koj911/aircraft-csv-updates/main/aircraft.csv.diff | patch -u aircraft.csv
gzip --best -k aircraft.csv
rm aircraft.csv
```
