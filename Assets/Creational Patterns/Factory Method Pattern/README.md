# Factory Method Pattern 工厂方法模式
## 定義

オブジェクトを作成するためのインターフェースを定義し、どのクラスをインスタンス化するかはサブクラスが決めるようにします。ファクトリーメソッドにより、クラスはインスタンス化をサブクラスに委ねることができる。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/factory.gif)


## 参加者

このパターンに参加しているクラスとオブジェクトは次のとおりです。

### 製品 (ページ)
* ファクトリーメソッドが作成するオブジェクトのインターフェイスを定義する
* ConcreteProduct (SkillsPage、EducationPage、ExperiencePage)
* Productインターフェイスを実装する

### Creator (ドキュメント)
* ファクトリーメソッドを宣言し、Product型のオブジェクトを返します。また、CreatorはデフォルトのConcreteProductオブジェクトを返すファクトリーメソッドのデフォルト実装を定義することができる。
* ファクトリーメソッドを呼び出すと、Productオブジェクトが生成されます。

### ConcreteCreator (レポート、レジュメ)
* ConcreteProductのインスタンスを返すようにファクトリーメソッドをオーバーライドします。

