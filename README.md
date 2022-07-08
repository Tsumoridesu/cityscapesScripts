# ラベル付け手順


## 1.データセットダウンロード
```
https://drive.google.com/drive/folders/1BZRCjUsVSh9ZqLM8xJWTYr532IIlmi9u?usp=sharing
```
'dataset'フォルダをまともにダウンロード

## 2.gitclone
```
git clone https://github.com/Tsumoridesu/cityscapesScripts.git
```


## 3.依存関係インストール

```
cd cityscapesScripts
python -m pip install cityscapesscripts[gui]
```

## 4.データセットのpathを指定

```
echo "export CITYSCAPES_DATASET=/データセットのpath " >> ~/.bashrc
source ~/.bashrc
```
例えば：ダウンロードしたデータセットのpathは：/home/dataset　の場合
```
echo "export CITYSCAPES_DATASET=/home/dataset " >> ~/.bashrc
```

## 5.ラベル付け
```
cd cityscapesscripts/anntation
python3 cityscapesLabelTool.py
```
左上の”Opencity”をクリックして、"train,gtFine,tsukuba"を選択して、ラベル付けを開始


画面中に点で区域を囲んで、”N”を押して、ラベルを選択する。


どんなラベルを選択すればいいのがわからない場合は、”Opencity”をクリックして、"train,gtFine,ulm"を選択して、参照してラベルを付ける。

重要なのは：

道路（走行可能領域）は”road”に、芝は”terrain”に、建物は”building”に、空は”sky”に、植物は”vegetation”に、カラーコーンは
”traffic sign”にする。

一枚の画像のラベル付けが終わったら、”Save”を押して、最後は/dataset/train/gtFine/train/tsukubaの中の内容が

https://drive.google.com/drive/folders/1BZRCjUsVSh9ZqLM8xJWTYr532IIlmi9u?usp=sharing

の同じところにアップロードすればいい。


## Contact

Please feel free to contact us with any questions, suggestions or comments:

* Marius Cordts, Mohamed Omran
* mail@cityscapes-dataset.net
* www.cityscapes-dataset.net
