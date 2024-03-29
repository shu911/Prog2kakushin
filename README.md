# Prog2kakushin
## work1について
### 概要

このプログラムは直接入力する・ランダムで生成する・ファイルを読み取るのいずれかによって取得したゲームの品質に関するアンケートから、それぞれの分野の評価値と統合的な評価値をデータ化して表示し、統合的な評価値のヒストグラムと相関係数のヒートマップに相関係数一覧を表示するプログラムである

### なぜこれを作ったのか

このプログラムはゲームのアンケートに対して使うことができます。このプログラムを使えば、自分がつくったゲームに対するフィードバックからどれだけの人が面白いと思ってくれたのか、どの部分が面白かったのか、逆にどの部分が面白くなかったのかなどを知ることができます。

私がこのプログラムを作った理由は、自分がゲーム作りをしたときに簡単なものでいいのでフィードバックが欲しいなと思ったからです。プレイしてくれた第三者の評価は貴重なので、一つ一つの評価を真剣に受け止めたいのですが、エクセルなどで数字が並んでいるだけではあまり評価されているという感覚がしないと思ったので、一目でわかるヒストグラムなどを作りたいと思いました。

### 入力と出力

#### 入力

１．データを手入力する場合は１、ランダムでデータを生成する場合は２、データの入ったcsvファイルを読み込む場合は３を入力

２（１）．１で１を入力した場合は何人分のアンケートを入力するかを入力、それから人数×（評価項目の数＋総評価）を入力。

２（２）．１で２を入力した場合は何人分のアンケートを生成するか入力

２（３）．１で３を入力した場合は読み込むcsvファイル名を入力。読み込むcsvファイルの中身は左から映像の評価、音響の評価、登場人物の評価、物語の評価、戦闘の評価、全体的な統合評価を書かれたものを用意する。

#### 出力

１．入力したデータのデータフレーム

２．１の中から総評価のみをピックアップしたヒストグラム

３．１のデータフレームの相関係数一覧のヒートマップ

４．１のデータフレームの相関係数一覧表

### 工夫した点

読み取れるデータをcsvファイルだけでなく、自分で手入力したものやランダムに生成したものを使える点。

## work2について

### 概要

このプログラムはPCゲームの正方形のマスのマインスイーパーを疑似的にプレイできるプログラムです。縦横のマス目の数と設置される爆弾の数を指定した後、マインスイーパーをプレイできます。

### なぜこのプログラムを作ったのか

私がこのプログラムを書いた理由は、前々からPythonを使って何かしらのゲームを作ってみたいなと思っていたのですが、他の革新クラスの課題ではゲームを作ることは出来なさそうだったので、平面のゲームなら再現可能なnumpyがテーマであるwork2ならゲーム作りができるなと思ったからです。

### 入力と出力

#### 入力

１．縦横のマス数を2～18の間から入力（それ以上の数は視認性が悪くなるため）

２．爆弾の数を入力

３. 爆弾を探す、フラグを設置するどちらの場合でも縦と横の座標を指定する。

#### 出力

１． マインスイーパーの盤面

### 工夫した点

従来のマインスイーパーと違い、端の位置を調べた場合、逆の端にヒントが出てくる、フラグを爆弾以外の位置に刺すとゲームオーバーになるなど今までのマインスイーパーでは味わえない体験をできるようにした。
また、穴をあけたマスの周囲のマスにヒントを出す仕組みをどうやって再現するかについてとても悩んだ。最初はforやwhileを使って再現しようと思っていたがどうやっても難しく詰まってしまうので、forやwhileを使わずに一つ一つのマスに判定を行うコードを書くことにした。

## work3について

### 概要

このプログラムは読み込んだ画像をモザイク処理するプログラムです。モザイク1マスは10×10になっており、元の画像のその範囲のRGBの平均値を計算して割り当てています。
また、例として使用する画像はプログラミングⅡの演習課題で使用したimages.zipを使用しています。

### なぜこのプログラムをつくったのか

最初は読み込んだ画像をドット絵にするプログラムを作ろうと思ったのだが、どうしてもコードが思いつかずモザイク処理するプログラムに変更した。
ドット絵にするプログラムを考えているときにこのプログラムを思いつきました。
ドット絵の場合は、このモザイク化のプログラムよりもっと一つ一つのマス目を細かくしなくてはいけませんでした。

### 入力と出力

#### 入力

１．モザイク処理する画像のファイル名（今回はimages.zipに含まれる画像のファイル名（拡張子も入れる））

#### 出力

１．入力された画像

２．１で入力された画像をモザイク処理したもの

### 工夫した点

縦横の長さの一の位が０以外だとエラーを吐いてしまうので、縦横の長さの一の位が０出なかった場合切り捨てにするようにした。

### 反省点

ドット絵から派生してモザイク処理するプログラムを作ったが、自分が本当に作りたいものを途中であきらめてしまった。
