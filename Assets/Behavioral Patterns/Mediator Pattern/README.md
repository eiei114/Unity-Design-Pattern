# Mediator Pattern 中介者模式
## 定義

オブジェクトの集合がどのように相互作用するかをカプセル化したオブジェクトを定義します。Mediatorは、オブジェクトが明示的にお互いを参照しないようにすることで疎結合を促進し、オブジェクトの相互作用を独立して変化させることができます。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/mediator.gif)


## 参加者

このパターンに参加しているクラスとオブジェクトは以下の通りである。

### メディエーター(IChatroom)
* 同僚オブジェクトと通信するためのインターフェイスを定義します。

### ConcreteMediator (チャットルーム)
* 同僚オブジェクトを調整することで協調的な振る舞いを実装します。
* 同僚を把握・管理する

### Colleagueクラス(Participant)
* 各Colleagueクラスは、そのMediatorオブジェクトを知っています。
* 各Colleagueは、他のColleagueと通信する場合は、必ずそのMediatorと通信を行います。

