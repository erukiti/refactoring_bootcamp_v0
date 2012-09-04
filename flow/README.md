狙い
====

ウンコなコードにはやたらif文が並んだりネスト構造が出まくるので、それへの対処を狙いとする。

条件文にまつわるリファクタリング、例外、アルゴリズムなど、フローに関するリファクタリングを重点的に考えているが、メソッド抽出なんかも積極的にやった方がいいだろう。もちろん他のリファクタリング技法を積極的に使っても構わない。

アルゴリズム変更
----------------

参考文献: リファクタリング Ruby エディション 6.1章 メソッド抽出

長いメソッドの一部分など、意味として切り出せる処理をメソッドとして抽出する。使用しているローカル変数などによっては別のリファクタリングを前提条件とする場合もある。切り出すときは「その塊に何か名前を付けることができるか」を考える。そして名前には処理の内容ではなく、何をしようとしているのか、ある程度の抽象度を持たせた名前を付けよう。

メソッドの抽出は元のコードを読みやすくする以外に、重複を取り除く意味もある。

battle
------

battle.rb と test_battle.rb で構成されている。test_battle.rb でテストが通る事を確認しながらリファクタリングを行う事。

想定している臭いとしては
など

