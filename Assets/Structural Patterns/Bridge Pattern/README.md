# Bridge Pattern 
## 定義

抽象化と実装を切り離し、両者が独立して変化できるようにすること。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/bridge.gif)


## 参加者

このパターンに参加しているクラスとオブジェクトは以下の通りです。

### 抽象化 (BusinessObject)
* 抽象化のインターフェイスを定義する。
* 実装者タイプのオブジェクトへの参照を保持します。

### RefinedAbstraction (CustomersBusinessObject) * 抽象化のインターフェイスを定義する。
* Abstractionで定義されたインターフェイスを拡張します。

### Implementor (DataObject)
* 実装クラスのためのインターフェイスを定義しています。このインターフェイスはAbstractionのインターフェイスと正確に対応する必要はなく、実際には2つのインターフェイスはかなり異なる場合があります。通常、Implementationインターフェイスはプリミティブな操作のみを提供し、 Abstractionはこれらのプリミティブに基づいたより高度な操作を定義する。

### ConcreteImplementor (CustomersDataObject) は、CustomersDataObject を実装したものです。
* Implementorインターフェイスを実装し、その具体的な実装を定義しています。

