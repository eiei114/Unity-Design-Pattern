# Flyweight Pattern 享元模式
## 定義

多数の細かいオブジェクトを効率的にサポートするために共有を使用します。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/flyweight.gif)


## 参加者

このパターンに参加しているクラスとオブジェクトは以下の通りです。

### フライウェイト (Character)
* フライウェイトが外部の状態を受け取り、それに対処できるようにするためのインターフェイスを宣言する。

### ConcreteFlyweight (CharacterA, CharacterB, ..., CharacterZ) * フライウェイトインターフェースを実装し、固有状態のストレージを追加します。
* Flyweight インターフェースを実装し、内在する状態がある場合は、それを保存するストレージを追加します。ConcreteFlyweight オブジェクトは共有可能である必要があります。つまり、ConcreteFlyweight オブジェクトのコンテキストとは無関係である必要があります。

### UnsharedConcreteFlyweight ( not used )
* すべての Flyweight サブクラスが共有される必要はありません。Flyweight インターフェースは共有を可能にしますが、強制するものではありません。UnsharedConcreteFlyweightオブジェクトは、フライウェイトオブジェクト構造のあるレベルにおいて、ConcreteFlyweightオブジェクトを子として持つことが一般的です（RowクラスとColumnクラスが持つような）。

### FlyweightFactory (CharacterFactory)。
* フライウェイトオブジェクトの作成と管理
* フライウェイトが適切に共有されるようにします。クライアントがフライウェイトを要求すると、FlyweightFactory オブジェクトは既存のインスタンスをアセットするか、存在しない場合はインスタンスを作成します。

### クライアント (FlyweightApp)
* フライウェイトへの参照を保持します。
* フライウェイトの外部状態を計算または保存します。

