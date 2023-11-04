# Factory

### [概要](https://github.com/DeFiGeek-Community/yamawake/blob/main/doc/ja/Factory/index.md#%E6%A6%82%E8%A6%81) <a href="#usercontent-gai-yao" id="usercontent-gai-yao"></a>

オークションテンプレートを管理しオークションをデプロイする

オークション主催者がオークションを開催するためのエントリーポイントになる

### [共通仕様](https://github.com/DeFiGeek-Community/yamawake/blob/main/doc/ja/Factory/index.md#%E5%85%B1%E9%80%9A%E4%BB%95%E6%A7%98) <a href="#usercontent-gong-tong-shi-yang" id="usercontent-gong-tong-shi-yang"></a>

#### [オークションテンプレート](https://github.com/DeFiGeek-Community/yamawake/blob/main/doc/ja/Factory/index.md#%E3%82%AA%E3%83%BC%E3%82%AF%E3%82%B7%E3%83%A7%E3%83%B3%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88) <a href="#user-content-kushontenpurto" id="user-content-kushontenpurto"></a>

* bytes32（utf8 を変換したもの）に対応するアドレスで管理される
* 上書きはできない

#### [オークションテンプレートの追加](https://github.com/DeFiGeek-Community/yamawake/blob/main/doc/ja/Factory/index.md#%E3%82%AA%E3%83%BC%E3%82%AF%E3%82%B7%E3%83%A7%E3%83%B3%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%81%AE%E8%BF%BD%E5%8A%A0) <a href="#user-content-kushontenpurtono" id="user-content-kushontenpurtono"></a>

* オーナーのみ可能
* 引数
  * templateName\_
    * bytes32
    * オークションテンプレートの名前
  * templateAddr\_
    * address
    * オークションテンプレートのアドレス
  * initializeSignature\_
    * bytes4
    * オークション初期化用関数シグネチャ
  * transferSignature\_
    * bytes4
    * オークション初期化時トークン転送用関数シグネチャ

#### [オークションテンプレートの削除](https://github.com/DeFiGeek-Community/yamawake/blob/main/doc/ja/Factory/index.md#%E3%82%AA%E3%83%BC%E3%82%AF%E3%82%B7%E3%83%A7%E3%83%B3%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%81%AE%E5%89%8A%E9%99%A4) <a href="#user-content-kushontenpurtono" id="user-content-kushontenpurtono"></a>

* オーナーのみ可能
* 引数
  * templateName\_
    * bytes32
    * オークションテンプレートの名前

#### [オークション立ち上げの申し込み](https://github.com/DeFiGeek-Community/yamawake/blob/main/doc/ja/Factory/index.md#%E3%82%AA%E3%83%BC%E3%82%AF%E3%82%B7%E3%83%A7%E3%83%B3%E7%AB%8B%E3%81%A1%E4%B8%8A%E3%81%92%E3%81%AE%E7%94%B3%E3%81%97%E8%BE%BC%E3%81%BF) <a href="#user-content-kushonchigenoshimi" id="user-content-kushonchigenoshimi"></a>

* 引数
  * templateName\_
    * bytes32
    * オークションテンプレートの名前
  * args\_
    * bytes
    * テンプレート初期化に必要な引数の集合

#### [オークション立ち上げ](https://github.com/DeFiGeek-Community/yamawake/blob/main/doc/ja/Factory/index.md#%E3%82%AA%E3%83%BC%E3%82%AF%E3%82%B7%E3%83%A7%E3%83%B3%E7%AB%8B%E3%81%A1%E4%B8%8A%E3%81%92) <a href="#user-content-kushonchige" id="user-content-kushonchige"></a>

* テンプレートを minimal proxy パターンでデプロイする
* テンプレートアドレスとナンス（オークションデプロイごとにインクリメント）を salt にした CREATE2 によってインスタンスアドレスが決まる
* 初期化関数はテンプレートごとのシグネチャ＋引数のcallで実行する
* デプロイ時に販売トークンをオークションに転送する
* 転送関数はテンプレートごとのシグネチャ＋引数のdelegatecallで実行する
* デプロイしたオークションのアドレスを記録する

#### [オークション保持](https://github.com/DeFiGeek-Community/yamawake/blob/main/doc/ja/Factory/index.md#%E3%82%AA%E3%83%BC%E3%82%AF%E3%82%B7%E3%83%A7%E3%83%B3%E4%BF%9D%E6%8C%81) <a href="#user-content-kushon" id="user-content-kushon"></a>

* デプロイしたオークションをmapping(address->bool)にて保持する
