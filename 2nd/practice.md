# Perl入学式 #2 復習問題

解答例は`ansewr/`フォルダにサポーターごとに格納してあります。

Perlのモットーは TMTOWTDI（やり方はいっぱいある）、同じ問題で同じ答えなのに様々な書き方ができます。

## 四則演算

1. number_magic.pl

    以下のスクリプトを作成して、結果を確認しましょう。

    1. 変数`$foo`に 10 を代入する
    1. スカラー変数`$hoge`に `$foo` を代入する
    2. `$hoge`に 1 を加える
    3. `$hoge`に 2 を掛ける
    4. `$hoge`に 6 を加える
    5. `$hoge`を 2 で割る
    6. `$hoge`から `$foo`を引く
    7. `$hoge`を表示して改行する

    `4` が表示されれば正解です。`$foo`に最初に代入する数値を変えて試してみましょう。


2. second.pl

    150秒は何分何秒になるか、1行目に分、2行目に秒を表示するスクリプトを作成しましょう。

    分を格納する変数`$min`と、秒を格納する変数`$sec`を用意して、それぞれで計算してみましょう。

    1行目に `2` , 2行目に `30` と表示されれば正解です。
    小数点の切り捨てには `int` 関数を使うと便利です。

    ```perl
    my $circle = int(3.1415);
    print $circle . "\n";    # 3 のみ表示される
    ```


3. power.pl

    10の2乗 × 10の3乗 - 10の5乗 を表示して改行するスクリプトを作成しましょう。

    変数名の指定はしません。変数を自分で用意して、計算してみましょう。

    `0` と表示されれば正解です。


## 文字列の連結

1. scalar_concat.pl

    以下のように動くスクリプトを作成しましょう。

    - スカラー変数`$foo`に 'P' を代入する
    - スカラー変数`$bar`に 'e' を代入する
    - スカラー変数`$buz`に 'r' を代入する
    - スカラー変数`$hoge`に 'l' を代入する
    - 最後に全てのスカラー変数を使って`Perl`と表示して改行し終了する


2. shouwa.pl

    西暦を昭和に変換するスクリプトを作成し、今年2019年は昭和何年になるか表示してください。

    1. 大正最後の年は西暦1925年とし、変数`$last_taisho`に数字`1925`を格納します

    2. 西暦と昭和の差はスクリプト内で計算すること

    3. 以下の形式で表示する

        > 西暦2019年は昭和94年です


## 標準入力

1. stdin.pl

    ターミナルから文字を入力し、その文字を表示して改行するスクリプトを作成しましょう。


2. stdin_twice.pl

    ターミナルから文字を入力し、その文字を **2回** 連続して表示し、改行するスクリプトを作成しましょう。


3. stdin_dialogue.pl

    以下のように動くスクリプトを作成しましょう

    1. ターミナルからプログラムを起動すると、`Please tell Your Name ? > `と表示し、入力を受け付ける

    2. 名前を入力し、Enterキーを押す

    3. 名前の入力が終わると改行し、`What time is it now ? > `と表示し、入力を受け付ける

    4. 現在時刻を入力し、Enterキーを押す

    5. 以下のような結果が2行で出力される

        ```
        You are 入力した名前 .
        It is 現在時刻 o'clock.
        ```

## if文

1. even_or_odd.pl

    標準入力により数値を1つ読み込み、その数値が偶数なら"even"、奇数なら"odd" という文字を出力する `even_or_odd.pl` を作成しましょう。


2. lexical_order.pl

    標準入力を2回利用して文字列を2つ読み込み、2つの文字列を辞書に登場する順に出力する `lexical_order.pl` を作成しましょう。

    同じ文字列の場合には "equal" と表示してください。

3. logical_operators.pl

    標準入力により数値を1つ読み込み、その数字が「2でも3でも割り切れる」なら"Multiple of six"という文字列を出力する `logical_operators.pl` を作成しましょう。

4. leap_year.pl

    4年に1回訪れる「うるう年（leap year）」は、以下の条件を満たす年です。(https://www.nao.ac.jp/faq/a0306.html)

    1. 西暦年号が4で割り切れる年をうるう年とする

    2. 例外として、西暦年号が100で割り切れて400で割り切れない年は平年とする

    例えば、西暦2000年はうるう年ですが、西暦2100年はうるう年ではありません。

    この条件を元に、標準入力から入力した数字（年）が、うるう年の場合には"leap year"と表示し、うるう年ではない場合には"normal year"と表示する`leap_year.pl`を作成しましょう。

## 配列

1. continuity_number.pl

    標準入力により0以上の数値を1つ読み込み, 0から入力した数値までの連続した数の配列を作成し、表示してみましょう。


2. factorial.pl

    標準入力により数値を1つ読み込み, その数値を[階乗](https://ja.wikipedia.org/wiki/%E9%9A%8E%E4%B9%97)した値を出力する`factorial.pl`を作成しましょう。

        例: 入力した数値が6 -> 6の階乗は `6 * 5 * 4 * 3 * 2 * 1 = 720` なので, ｢720｣を出力する


3. split_join.pl

    `Swiss-Army chainsaw`という文字列を `join` と `split` を用いて `Swiss Army chainsaw`という3つの単語に分けましょう。


1. unshift_pop.pl

    以下の配列を用意します

    `my @array = (5 .. 10);`

    この配列の中身が `( 0, 1, 2, 3, 4 )`　となるよう、 `unshift` と `pop`で調整して出力しましょう。


1. shift_push.pl

    以下の配列を用意します

    `my @array = (5 .. 10);`

    この配列の中身が `( 0, 1, 2, 3, 4 )`　となるよう、 `shift` と `push`で調整して出力しましょう。


1. lexical_sort.pl

    標準入力を3回利用して文字列を3つ読み込み, 3つの文字列を辞書に登場する順に出力する`lexical_order.pl`を作成しよう
