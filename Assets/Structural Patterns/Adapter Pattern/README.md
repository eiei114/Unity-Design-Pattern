# Adapter Pattern 
## 定義
クラスのインターフェイスを、クライアントが期待する別のインターフェイスに変換します。アダプタを使用すると、インターフェイスの互換性がないために一緒に動作させることができなかった クラスを動作させることができます。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/adapter.gif)


## 参加者

このパターンに参加するクラスとオブジェクトは次のとおりです。

### ターゲット (ChemicalCompound)
* Clientが使用するドメイン固有のインターフェイスを定義します。

### Adapter (Compound)
* AdapteeインターフェイスをTargetインターフェイスに適合させる。

### Adaptee (ChemicalDatabank)インターフェイスをTargetインターフェイスに適合させます。
Adaptee (ChemicalDatabank) * 適応が必要な既存のインターフェイスを定義します。

### クライアント(AdapterApp)
Client (AdapterApp) * Targetインターフェースに準拠したオブジェクトと協働する。