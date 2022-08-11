# Visitor Pattern 访问者模式
## 定義

オブジェクト構造の要素に対して実行する操作を表します。Visitorを使えば、操作対象となる要素のクラスを変更することなく、新しい操作を定義することができます。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/visitor.gif)


## 参加者

このパターンに参加しているクラスとオブジェクトは以下の通りです。

### Visitor (訪問者)
* オブジェクト構造内の ConcreteElement の各クラスに対して、Visit オペレーションを宣言する。操作の名前とシグネチャは、VisitorにVisit要求を送るクラスを特定する。それによって、ビジターは訪問される要素の具象クラスを決定することができます。そして、訪問者はその特定のインターフェースを通して、要素に直接アクセスすることができます。

### 具体的なVisitor (IncomeVisitor, VacationVisitor)
* Visitorで宣言された各操作を実装しています。各操作は，構造体の対応するクラスやオブジェクトに定義されたアルゴリズムの断片を実装しています．ConcreteVisitorはアルゴリズムのコンテキストを提供し、そのローカルな状態を保存します。この状態は、構造体の探索中にしばしば結果を蓄積する。

### Element (要素)
Element (要素) * 訪問者を引数として受け取るAccept操作を定義します。

### ConcreteElement (Employee)
* 訪問者を引数として受け取るAccept操作を実装します。

### ObjectStructure (社員)
* その要素を列挙することができます。
* 訪問者がその要素を訪問できるように、高レベルのインターフェイスを提供することができます。
* Composite (パターン) または list や set などのコレクションである可能性があります。

