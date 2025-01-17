# Proxy Pattern 
## 定義

他のオブジェクトへのアクセスを制御するために、そのオブジェクトのサロゲートまたはプレースホルダーを提供する。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/proxy.gif)


## 参加者

このパターンに参加しているクラスとオブジェクトは以下の通りです。

### プロキシ(MathProxy)
* プロキシが実サブジェクトにアクセスできるようにするための参照を保持します。RealSubjectとSubjectのインタフェースが同じであれば、ProxyはSubjectを参照することができます。
* RealSubjectとSubjectのインタフェースが同じであれば，ProxyはSubjectを参照することができます．
* 実サブジェクトへのアクセスを制御し、その生成と削除を担当することができる。
* その他の責務はプロキシの種類に依存します。
	* `リモートプロキシ`は、リクエストとその引数をエンコードし、エンコー ドされたリクエストを別のアドレス空間にある本当のサブジェクトに送る責任を 負う。
	* `仮想プロキシ` は実際の対象に関する追加情報をキャッシュして、アクセスを先延ばしにすることができます。例えば、MotivationのImageProxyは実画像の範囲をキャッシュしています。
	* `protection proxies` は、呼び出し元がリクエストの実行に必要なアクセス権限を持っているかどうかをチェックします。

### 主題(IMath)
* RealSubject と Proxy の共通インターフェースを定義しています。

### RealSubject (Math)
* プロキシが表現する実オブジェクトを定義します。

