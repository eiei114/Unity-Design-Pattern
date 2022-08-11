# Interpreter Pattern 解释器模式
## 定義

ある言語が与えられたとき、その文法の表現と、その表現を用いてその言語の文を 解釈するインタプリタを定義しなさい。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/interpreter.gif)


## 参加者

このパターンに参加するクラスとオブジェクトは次のとおりです。

### AbstractExpression (Expression)
* 演算を実行するためのインターフェイスを宣言します。

### TerminalExpression ( ThousandExpression, HundredExpression, TenExpression, OneExpression ) * 操作を実行するためのインターフェイスを宣言します。
* 文法中の終端記号に関連する Interpret 操作を実装します。
* 文中の各終端記号に対してインスタンスが必要です。

### 非終端式(NonterminalExpression) ( 使用されません )
* 文法中の各規則R ::= R1R2...Rn に対して、このようなクラスが1つ必要です。
* 各記号 R1 ～ Rn に対して AbstractExpression 型のインスタンス変数を保持します。
* 文法内の非終端記号に対する Interpret 操作を実装します。Interpretは通常、R1〜Rnを表す変数に対して再帰的に自分自身を呼び出す。

### コンテキスト(Context)
* インタープリターにとってグローバルな情報を含みます。

### クライアント(InterpreterApp)
* 文法が定義する言語の特定の文を表現する抽象構文木を構築する（または与えられる）。抽象構文木は、NonterminalExpressionクラスとTerminalExpressionクラスのインスタンスから組み立てられる。
* Interpretオペレーションを呼び出す。

www.DeepL.com/Translator（無料版）で翻訳しました。

