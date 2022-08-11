# Iterator Pattern 迭代器模式
## 定義

集約オブジェクトの要素に順次アクセスする方法を提供し、その基礎となる表現を公開しない。
![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/iterator.gif)


## 参加者

このパターンに参加するクラスとオブジェクトは次のとおりです。

### Iterator（AbstractIterator）。
* 要素にアクセスし、トラバースするためのインターフェイスを定義しています。

### ConcreteIterator (Iterator)。
* Iteratorインターフェイスを実装しています。
  ConcreteIterator (Iterator) * Iteratorインタフェースを実装しています * 集合体の走査における現在の位置を記録します。

### Aggregate (AbstractCollection)：集合体。
* Iterator オブジェクトを作成するためのインターフェイスを定義しています。

### ConcreteAggregate (コレクション)
* Iterator生成インタフェースを実装し、適切なConcreteIteratorのインスタンスを返します。

www.DeepL.com/Translator（無料版）で翻訳しました。

