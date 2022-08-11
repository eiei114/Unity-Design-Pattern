# Prototype Pattern 原型模式
## 定義

プロトタイプインスタンスを用いて作成するオブジェクトの種類を指定し、このプロトタイプをコピーして新しいオブジェクトを作成します。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/prototype.gif)


## 参加者

このパターンに参加しているクラスとオブジェクトは以下の通りである。

### プロトタイプ(ColorPrototype)
* 自分自身を複製するためのインターフェイスを宣言する

### ConcretePrototype (Color)。
* 自分自身のクローンを作成するための操作を実装する

### クライアント(ColorManager)
* プロトタイプに自分自身のクローン作成を依頼し、新しいオブジェクトを作成する。


