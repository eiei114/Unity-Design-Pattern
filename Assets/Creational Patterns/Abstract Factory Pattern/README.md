# Abstract Factory Pattern 抽象工厂模式
## 定義

関連・依存するオブジェクトのファミリーを，その具象クラスを指定せずに作成するためのインタフェースを提供する．

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/abstract.gif)


## 参加者

このパターンに参加するクラスとオブジェクトは以下の通りである。

### AbstractFactory (ContinentFactory)
* 抽象的な製品を作成する操作のためのインターフェイスを宣言しています。

### ConcreteFactory（AfricaFactory、AmericaFactory）。
* 具体的な製品オブジェクトを作成するための操作を実装しています。

### AbstractProduct (Herbivore, Carnivore) * 抽象的な製品を作成する操作のインターフェイスを宣言しています。
* 商品オブジェクトの種類を表すインタフェースを宣言しています。

### Product (Wildebeest、Lion、Bison、Wolf)。
* 商品オブジェクトを定義し、対応する具象ファクトリーで生成する。
* AbstractProduct インターフェースを実装しています。

### クライアント(AnimalWorld)
* AbstractFactoryクラスとAbstractProductクラスで宣言されたインターフェイスを使用します。


