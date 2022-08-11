# Observer Pattern 观察者模式
## 定義

オブジェクト間の一対多の依存関係を定義し、あるオブジェクトが状態を変更すると、その依存関係すべてが通知され、自動的に更新されるようにします。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/observer.gif)


## 参加者

このパターンに参加しているクラスとオブジェクトは次のとおりです。

## Subject (株式)
* オブザーバーを知っている。任意の数のObserverオブジェクトがSubjectを観察することができる。
* Observerオブジェクトをアタッチ、デタッチするためのインターフェイスを提供する。

### ConcreteSubject (IBM)
* ConcreteObserverが関心を持つ状態を保存する。
* 状態が変化すると、Observerに通知を送る。

### オブザーバ(IInvestor)
* Subjectの変更を通知されるべきオブジェクトのための更新インターフェイスを定義しています。

### ConcreteObserver (投資家)
* ConcreteSubjectオブジェクトへの参照を保持する。
* サブジェクトと一貫性を保つべき状態を保存します。
* オブザーバの更新インタフェースを実装し、サブジェクトの状態との一貫性を保つ。

