# Data Locality Pattern 

## インテント

CPUのキャッシュを利用したデータ配置により、メモリアクセスを高速化する。




## パターン

最近のCPUは、メモリアクセスを高速化するためにキャッシュを搭載している。これらは、最近アクセスされたメモリに隣接するメモリに、より速くアクセスすることができる。これを利用して、データの局所性を高め、処理する順番に連続したメモリにデータを保持することで、パフォーマンスを向上させることができます。




## いつ使うか

データローカリティを利用する際の第一の指針は、性能上の問題が発生したときに利用することです。 頻繁に使用されないコードベースの隅には適用しないでください。最適化されたコードは、より複雑で柔軟性に欠ける結果になることが多い。

このパターンの場合、パフォーマンスの問題が本当にキャッシュがヒットしないことが引き金になっているかどうかも確認してください。 他の理由でコードが遅い場合、このパターンは当然ながら役に立ちません。

性能を評価する簡単な方法は、手動で命令を追加し、タイマーでコード内の2点間の消費時間をチェックすることです。 悪いキャッシュの使い方を見つけ、どこでどれだけのキャッシュミスが発生しているかを知るには、より高度なツールであるプロファイラを使う必要があります。

コンポーネントモデルは、キャッシュの最適化を行う最も一般的な例です。 また、多くのデータに触れる必要がある重要なコードは、データの局所性を考慮することが重要です。


