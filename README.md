# 2018-2019 NBA最有價值球員預測分析(非總決賽)
## 介紹
>實驗時間2019年初，2019年MVP尚未選出。

## Dataset
>Kaggle：https://www.kaggle.com/danchyy/nba-mvp-votings-through-history
>* 含637個(1980-2018)球員數據(其中包含當季MVP球員與當季MVP候補球員)  。
>* 40個(2019)MVP候補球員數據。

## 前處理
>* 挑選特徵
>* 補空值

## 方法
>* 分層抽樣
>在38個賽季中共有637筆球員資料，也就是只有38個MVP，如將資料全數訓練會導致數據不平衡。 <br>
>將資料每季視為每一層，並從每一層抽取1個MVP球員與N個非MVP球員。 <br>
>因為2019年度MVP尚未選出，因此將先前資料(1980-2018)拆分10次做為訓練資料與測試資料。 <br>
>| 次數 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
>|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:--:|:---:|:---:|:---:|
>| 訓練資料(賽季) | 1-28 | 1-29 | 1-30 | 1-31 | 1-32 | 1-33 | 1-34 | 1-35 | 1-36 | 1-37 |
>| 測試資料(賽季) | 29 | 30 | 31 | 32 | 33 | 34 | 35 | 36 | 37 | 38 |

## 模型
>隨機森林

