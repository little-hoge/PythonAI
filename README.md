# 各章
- １章概要
- ２章レベル１初めての AI 開発(家賃予測 AI
- ３章レベル２クレジット審査判定 AI
- ４章レベル３クレジット審査判定 AI (ディープラーニング版)
- ５章レベル４画像判定 AI

# 進行予定
- 1日目 １～３章、Python基本文法
- 2日目 ４～５章

### 演習環境
- Anaconda 1.9.12
- Jupiter NoteBook 6.0.3

### Jupiterショートカット
- Tab：コード補完
- Ctrl＋Enter：実行
- Shift＋L：行数表示
- A、B：上、下セル追加
- Y、M：入力タイプCade化、Markdown化
- DD：選択セル削除
- 00：カーネル初期化

### 基本概要
- スカラー：変数
- ベクトル：配列
- 行列：２次元配列
- テンソル：ほぼ行列

### Matplotlibの使用方法
- モジュールのインポート：`importmatplotlib.pyplot as plt`
- 線グラフの作成：`plt.plot(x,y)`
- グラフの表示：`plt.show`

### AI種類
<table>
	<tbody>
		<tr>
			<th></th>
			<th colspan="2">学習分野</th>
			<th>具体例</th>
			<th>アルゴリズム</th>
		</tr>
		<tr>
			<th rowspan="2">教師あり学習</th>
			<td>分類</td>
			<td>与えられたデータが､どの分類に当てはまるのかを識別する学習方法</td>
			<td>
          <ul>
             <li>オートバックスのタイヤ診断</li>
             <li>きゅうりの仕分け機</li>
             <li>メールスパムの判定</li>
          </ul>
      </td>
			<td>
          <ul>
             <li>ニューラルネットワーク(DNN/CNN/RNN)</li>
             <li>SVM(二値分類)</li>
             <li>ロジスティック回帰</li>
          </ul>
       </td>
		</tr>
		<tr>
			<td>回帰</td>
			<td>関連性のある過去の数値から予測</td>
			<td>
          <li>消費電力予測</li>
          <li>売上予測</li>
          <li>株価予測</li>
      </td>
			<td>
          <li>ニューラルネットワーク(DNN/RNN)</li>
          <li>SVR</li>
          <li>ランダムフォレスト</li>
      </td>
		</tr>
		<tr>
			<th rowspan="2">教師なし学習</th>
			<td>クラスタリング</td>
			<td>未知の集合を、いくつかの集まりに分類させる学習方法</td>
			<td>
          <li>顧客の分類分けによるDM配信</li>
          <li>レコメンド</li>
      </td>
			<td>
          <li>K-Means</li>
          <li>ウォード法</li>
          <li>ki-斤傍法</li>
      </td>
		</tr>
		<tr>
			<td>異常検知</td>
			<td>正常行為を学習し、大きく異なるものを識別</td>
			<td>
          <li>射出成形機の摩耗検知</li>
          <li>セキュリティシステム</li>
          <li>機械設備のセンサー認識</li>
      </td>
			<td>
          <li>K-Means</li>
          <li>OneClassSVM</li>
          <li>PCA</li>
      </td>
		</tr>
		<tr>
			<th>強化学習</th>
			<td colspan="2">取るべき最善行動を決定する問題を扱う</td>
			<td>
          <li>ポードゲーム</li>
          <li>バラ積み口ポット</li>
          <li>自動運転</li>
      </td>
			<td>
          <li>モンテカルロ木探索</li>
          <li>SARSA</li>
          <li>Q学習</li>
      </td>
		</tr>
	</tbody>
</table>

# ライブラリ
### 共通
 <table>
	<tbody>
		<tr>
			<th>名前</th>
			<th>特徴</th>
			<th width="150">分野</th>
		</tr>
		<tr>
			<th>NumPy</th>
			<td>多次元配列に対して何度も演算を効率的に行えるようになる。<br>
      またベクトルや行列などの多次元配列の処理を容易に行うことができる。
      </td>
			<td>前処理</td>
		</tr>
		<tr>
			<th>Pandas</th>
			<td>表形式のデータの前処理を行う際によく使われるライブラリ。欠損値の処理 (欠損を補完)や 文字と数字の対応 (男性、女性といった文字を、 0 、 １に対応させる処理)等。<br>
      また平均、分散、相関といった統計処理も得意で、 Matplotlibと組み合わせることでデータの規則性・法則性を見つけることができる
      </td>
			<td>前処理(データ)</td>
		</tr>
		<tr>
			<th>scikit-learn</th>
			<td>回帰、SVM 、 k 近傍法、ランダムフォレスト等のモデルが用意されている。これらのモデルを使うことで、予測・分類などを行える。</td>
			<td>機械学習</td>
		</tr>
		<tr>
			<th>Matplotlib</th>
			<td>MatplotlibのラッパーライブラリSeabornを合わせて使うことでより見やすいグラフ作成などが可能。前処理時のデータ構造の可視化、機械学習時の精度、学習進度の可視化などあらゆるデータを簡単にグラフ化時に使用する。</td>
			<td>データの可視化</td>
		</tr>
		<tr>
			<th>seaborn</th>
			<td>統計的なデータをプロットするための機能が多く用意されているが、普通の折れ線グラフの見た目を良くするためだけにも使える。 手軽に美しいグラフを描画できる。</td>
			<td>データの可視化</td>
		</tr>
	</tbody>
</table>

### 画像関連
<table>
	<tbody>
    <tr>
      <th>名前</th>
      <th>特徴</th>
      <th width="150">分野</th>
    </tr>
		<tr>
			<th>OpenCV</th>
			<td>取り込めない画像を数値化し学習可能なデータに変換する。他、画像データのサイズ、回転、フィルタリングなどをプログラム上で容易に行えるようにしたライブラリ。物体検出(顔検出)なども行えるため、画像の前処理ではよく使用される。 </td>
			<td>前処理(画像)</td>
		</tr>
		<tr>
			<th>pillow</th>
			<td>OpenCVと同様に画像を数値化し学習可能なデータに変換する。コンピュータービジョン系の高度な画像処理(顔検出とかオプティカルフローなど)はできないが、リサイズ(拡大・縮小)や回転、トリミング(部分切り出し)のような単純な処理は得意。 </td>
			<td>前処理(画像)</td>
		</tr>
    <tr>
			<th>scikitｰimage</th>
			<td>OpenCVと似たような機能が多い。セグメンテーション、幾何学的変換、色空間操作、分析、フィルタリング、形態、特徴検出などの アルゴリズムが含まれている。<br>scikit-imageの利点は他のライブラリ「NumPy」「SciPy」「Pandas」「Matplotlib」とやり取りしやすくscikitlearnと組み合わせやすいなどがある。ただしOpenCVの方が処理速度が速いためあまり人気は高くない。</td>
			<td>前処理(画像)</td>
		</tr>
	</tbody>
</table>  

### 言語関連
<table>
	<tbody>
    <tr>
      <th>名前</th>
      <th>特徴</th>
      <th width="150">分野</th>
    </tr>
		<tr>
			<th>mecab</th>
			<td>日本語向け形態素解析ライブラリ。<br>英語はスペースで単語の切り分けができるが、日本語は単語の分かち書きをしない言語であるので、文章を意味のある単語へ分割する「分かち書き形態素解析 」は重要。<br>mecabは分割規則を定義した辞書を併用し、某大手メーカーのかな漢字変換等にも応用されている。日本語テキストを機械学習モデルの入力として使いたい場合に使用する。 </td>
			<td>前処理(言語)</td>
		</tr>
		<tr>
			<th>NLTK</th>
			<td>自然言語を機械的に処理するためには、語の品詞を特定したり(形態素解析)、文章の文法的な関係を解析したり(構文解析)、英単語の大文字・小文字の変換(語の正規化)などを行う必要があるが、これら人間の言語データを処理することを自然言語処理という。NLTKは、英語の自然言語処理のためのPythonのライブラリ。  </td>
			<td>前処理(言語)</td>
		</tr>
    <tr>
			<th>Gensim</th>
			<td>トピックモデルを使いやすくするために作られたライブラリ。トピックモデルとは、与えられた文章がどのトピックに属するかを分類する手法。アルゴリズムの中で、LDA (Latent Dirichlet Allocation)とWord2vecが代表的なもの。<br>LDA：どのトピックに属するかを確率分布で予測する。<br>Word2vec：指定された次元の空間に単語を埋め込むためのアルゴリズム、空間内における単語の距離の近さが単語の意味の近さになる。注目している単語とその前後周辺に出てくる単語の関連を計算し学習する。 </td>
			<td>前処理(言語)</td>
		</tr>
	</tbody>
</table>

### ディープラーニングの代表的なフレームワーク一覧
<table>
	<tbody>
		<tr>
			<th>名前</th>
			<th>特徴</th>
		</tr>
		<tr>
			<th>Tensorflow</th>
			<td>Tensorboard
という学習可視化ソフト、 Deep Learning フレームワーク最大のコミュニティなど
を持つ。</td>
		</tr>
		<tr>
			<th>Keras</th>
			<td>Tensorflow
Theano など複数のバックエンドを持つ。ディープニューラルネットワークを用いた
迅速な実験を可能にするよう設計され、最小限、モジュール式、拡張可能であることに重点が置
かれている。 TensorFlow を扱うのが難しいといった人に使用されることも多い。</td>
		</tr>
		<tr>
			<th>Chainer</th>
			<td>モデルの構築のしやすさと学習コードが書きやすい国産フレームワーク。ニューラルネットワー
クを実装するためのクラスと学習コードを抽象化した Trainer 機能が用意されている。
※2019
年 12 月 5 日メジャーアップデートを終了すると宣言。今後は PyTorch に合流するとのこと。</td>
		</tr>
		<tr>
			<th>PyTorch</th>
			<td>Chainer
を参考にしているせいか似たフレームワークで書きやすく、 Chainer よりも高速。
Chainer
開発終了後プリファード・ネットワーク社の研究開発基盤は順次 PyTorch に移行している。</td>
		</tr>
		<tr>
			<th>MXNet</th>
			<td>Tensorflow
のようにも、 Chainer のようにも書くことができるフレキシブルなフレームワーク
Python
以外にも C++ 、 Scala 、 Julia 、 Perl 、 R などの様々な言語に対応</td>
		</tr>
		<tr>
			<th>DyNet</th>
			<td>自然言語処理に適したフレームワーク。動的ニューラルネットワーク構築が可能、自動ミニバッ
チ化など便利な機能が多い。</td>
		</tr>
	</tbody>
</table>

# 実施方法
1. Open in Colabバナーをクリック
2. 実行したいコード選択状態で実行(Ctrl+Enter) 
3. googleアカウントとEnter your authorization codeを要求されるので画面に従い設定
4. [画像](https://user-images.githubusercontent.com/3638785/107232862-4661fc80-6a65-11eb-813e-9503f6a1e239.PNG)のようにパスを合わせる。

# 演習等
[google Colaboratory](https://tutorials.chainer.org/ja/01_Welcome_to_Chainer_Tutorial.html)
で実行できるように内容調整  
- [1章～2章](https://github.com/little-hoge/PythonAI/blob/main/1%E6%97%A5%E7%9B%AE/test.ipynb)  
- [3章](https://github.com/little-hoge/PythonAI/blob/main/1%E6%97%A5%E7%9B%AE/test2.ipynb)
- [4章](https://github.com/little-hoge/PythonAI/blob/main/2%E6%97%A5%E7%9B%AE/test3.ipynb)
- [5章](https://github.com/little-hoge/PythonAI/blob/main/2%E6%97%A5%E7%9B%AE/test4.ipynb)
- [画像判定](https://github.com/little-hoge/PythonAI/blob/main/2%E6%97%A5%E7%9B%AE/animalai/animal_ai_app.ipynb)([ngrok](https://user-images.githubusercontent.com/3638785/107231221-62649e80-6a63-11eb-9f16-06e28486f594.PNG)のリンクをクリック)  
