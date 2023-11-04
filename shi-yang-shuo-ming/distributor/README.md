# Distributor

### [概要](https://github.com/DeFiGeek-Community/yamawake/blob/main/doc/ja/Distributor/index.md#%E6%A6%82%E8%A6%81) <a href="#usercontent-gai-yao" id="usercontent-gai-yao"></a>

初期ユーザのリワード（5000万YMWK）を配布する

ユーザごとのスコアを管理し、スコアを元に配布する

### [機能](https://github.com/DeFiGeek-Community/yamawake/blob/main/doc/ja/Distributor/index.md#%E6%A9%9F%E8%83%BD) <a href="#usercontent-ji-neng" id="usercontent-ji-neng"></a>

#### [プロパティ](https://github.com/DeFiGeek-Community/yamawake/blob/main/doc/ja/Distributor/index.md#%E3%83%97%E3%83%AD%E3%83%91%E3%83%86%E3%82%A3) <a href="#user-content-puropati" id="user-content-puropati"></a>

* スコア（≒ Mint可能枚数）をユーザごとに保持する

#### [初期化](https://github.com/DeFiGeek-Community/yamawake/blob/main/doc/ja/Distributor/index.md#%E5%88%9D%E6%9C%9F%E5%8C%96) <a href="#usercontent-chu-qi-hua" id="usercontent-chu-qi-hua"></a>

* トークンを設定できる
* Factoryを設定できる

#### [Claim](https://github.com/DeFiGeek-Community/yamawake/blob/main/doc/ja/Distributor/index.md#claim) <a href="#user-content-claim" id="user-content-claim"></a>

* ユーザは自身のスコアと同量のトークンをMintできる
* Claimするとスコアが０にリセットされる

#### [スコアの加算](https://github.com/DeFiGeek-Community/yamawake/blob/main/doc/ja/Distributor/index.md#%E3%82%B9%E3%82%B3%E3%82%A2%E3%81%AE%E5%8A%A0%E7%AE%97) <a href="#user-content-sukoano" id="user-content-sukoano"></a>

* 指定ユーザに対するスコアを指定数だけ増加させることができる
* スコア加算はFactoryからデプロイされたオークションのみが可能
