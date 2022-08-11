# Decorator Pattern 
## 定義

オブジェクトに動的に追加責任を持たせる。デコレーターは、機能を拡張するためのサブクラス化に代わる柔軟な手段を提供します。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/decorator.gif)


## 参加者

このパターンに参加するクラスとオブジェクトは次のとおりです。

### Component (LibraryItem)
* 動的に責任を持たせることができるオブジェクトのインターフェイスを定義します。

### ConcreteComponent (Book, Video)
* 追加の責任を取り付けることができるオブジェクトを定義します。

### Decorator (Decorator)
* Componentオブジェクトへの参照を保持し、Componentのインターフェイスに準拠したインターフェイスを定義します。

### ConcreteDecorator（Borrowable）。
* ComponentにPositionsを追加します。

