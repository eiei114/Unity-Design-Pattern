# State Pattern 状态模式
## 定義

オブジェクトの内部状態が変化したときに、そのオブジェクトの振る舞いを変更できるようにします。オブジェクトはそのクラスを変更するように見える。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/state.gif)


## 参加者

このパターンに参加するクラスとオブジェクトは以下の通りです。

### コンテキスト（アカウント）
* クライアントが関心を持つインターフェイスを定義する
* 現在の状態を定義するConcreteStateのサブクラスのインスタンスを維持する。

### 状態（State）
* Contextの特定の状態に関連する動作をカプセル化するためのインターフェイスを定義します。

### 具体的な状態（RedState、SilverState、GoldState）。
* 各サブクラスは、Contextの状態に関連する動作を実装しています。

