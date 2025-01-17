# Memento Pattern 备忘录模式
## 定義

カプセル化に違反することなく、オブジェクトの内部状態をキャプチャして外部化し、後でこの状態に戻すことができるようにすること。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/memento.gif)


## 参加者

このパターンに参加しているクラスとオブジェクトは以下の通りです。

### メメント(Memento)
* Originatorオブジェクトの内部状態を格納する。メメントは、オリジネーターの内部状態を、オリジネーターの裁量で必要なだけ保存することができます。
* Originator以外のオブジェクトによるアクセスから保護します。メメントには事実上2つのインターフェイスがあります。Caretakerはメメントに対する狭いインターフェイスを見ています -- メメントを他のオブジェクトに渡すことしかできません。一方、オリジネーターは広いインターフェースを持っており、自分自身を以前の状態に戻すのに必要なすべてのデータにアクセスすることができます。理想的には、メメントを生成したオリジネーターだけがメメントの内部状態にアクセスすることができます。

### オリジネーター (SalesProspect)
* 現在の内部状態のスナップショットを含むメメントを作成します。
* その内部状態を復元するためにメメントを使用します。

### 管理者（Caretaker)
* メメントを安全に保管する責任がある
* 決してメメントを操作したり、メメントの中身を調べたりしない。

