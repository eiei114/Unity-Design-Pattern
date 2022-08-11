# Template Method Pattern 模板方法模式
## 定義

操作の中でアルゴリズムの骨格を定義し、いくつかのステップをサブクラスに委ねます。テンプレートメソッドは、サブクラスがアルゴリズムの構造を変更することなく、アルゴリズムの特定のステップを再定義できるようにします。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/template.gif)


## 参加者

このパターンに参加するクラスとオブジェクトは次のとおりです。

### AbstractClass (DataObject)
* 具体的なサブクラスがアルゴリズムのステップを実装するために定義する、抽象的なプリミティブ操作を定義する。
* アルゴリズムの骨格を定義するテンプレートメソッドを実装する。テンプレートメソッドは、プリミティブ操作のほか、AbstractClassで定義された操作や、他のオブジェクトの操作を呼び出します。

### ConcreteClass (CustomerDataObject)。
* アルゴリズムのサブクラス固有のステップを実行するためのプリミティブな操作 を実装する．

