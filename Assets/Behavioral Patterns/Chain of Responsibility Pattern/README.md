# Chain of Responsibility Pattern 责任链模式
## 定義

複数のオブジェクトにリクエストを処理する機会を与えることで、 リクエストの送信者と受信者の結合を避けることができます。受信側のオブジェクトをチェーン化し、あるオブジェクトが処理するまでリクエストをチェーンに沿って渡します。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/chain.gif)


## 対象者

このパターンに参加するクラスとオブジェクトは次のとおりです:

### ハンドラ (承認者)
* リクエストを処理するためのインターフェイスを定義する。
* (オプション) 後継者リンクを実装します。

### ConcreteHandler (Director, VicePresident, President)
* 担当するリクエストを処理する
* 後継者にアクセスできる
* ConcreteHandlerがリクエストを処理できる場合は処理し、そうでない場合は 後継者に転送する。

### クライアント(ChainApp)
* チェーン上のConcreteHandlerオブジェクトにリクエストを開始する。
