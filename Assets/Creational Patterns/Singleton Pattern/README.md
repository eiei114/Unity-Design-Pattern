# Singleton Pattern 单例模式
## 定義

クラスが1つのインスタンスしか持たないことを保証し、そのインスタンスへのグローバルなアクセスポイントを提供します。

![](https://github.com/QianMo/Unity-Design-Pattern/blob/master/UML_Picture/singleton.gif)


## 参加者

このパターンに参加しているクラスとオブジェクトは以下の通りである。

### シングルトン (LoadBalancer)
* クライアントがそのユニークなインスタンスにアクセスすることを可能にする Instance オペレーションを定義する。Instanceはクラスの操作である。
* インスタンスはクラス操作であり、それ自身のユニークなインスタンスの作成と維持に責任がある。

