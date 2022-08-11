# Strategy Pattern 策略模式
## 定義

アルゴリズムのファミリーを定義し、それぞれをカプセル化し、それらを交換可能にする。ストラテジーは、アルゴリズムを使用するクライアントから独立して変化させることができる。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/strategy.gif)


## 参加者

このパターンに参加しているクラスとオブジェクトは以下の通りである。

### ストラテジー (SortStrategy)
* サポートされるすべてのアルゴリズムに共通するインターフェースを宣言する。Contextはこのインターフェイスを利用して、ConcreteStrategyで定義されたアルゴリズムを呼び出す。

### ConcreteStrategy (QuickSort、ShellSort、MergeSort)。
* アルゴリズムをStrategyインターフェースで実装

### Context (SortedList)
* ConcreteStrategyオブジェクトで構成される。
* Strategyオブジェクトへのリファレンスを保持する。
* Strategyがデータにアクセスするためのインターフェイスを定義することができる。

