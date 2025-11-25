# README

## ページの更新について

### 五月祭/駒場祭終了直後
- [ ] ut-10min.github.io/index.html
  - [ ] 最新の五月祭/駒場祭を上に持ってきて日付を書き換え
    - [ ] 日付が分からない部分は、予め"XX"におきかえる
  - [ ] 直近の五月祭/駒場祭を過去のログに加筆
- [ ] 各五月祭/駒場祭のページ
  - [ ] リモートで新しいレポジトリを作成
    - [ ] レポジトリ名は "mfXX" または "kfXX" (XXは番号)
  - [ ] ファイルを過去直近のmfXX/kfXXのレポジトリからコピー
    - [ ] ローカルでフォルダことコピーした後、git initして新しいレポジトリとして管理開始
  - [ ] ローカルで内容を更新
    - [ ] index.html
      - [ ] 日付、会場、時間を未定に
      - [ ] meta情報（description, keywords, title, twitterカード, ogp）を更新
    - [ ] timetable.html
      - [ ] meta情報（description, keywords, title, twitterカード, ogp）を更新
    - [ ] ローカルで動作確認
      - [ ] cdで作成したフォルダに行き、python3 -m http.serverをターミナルで実行
  - [ ] リモートにpush 
      - [ ] git remote add origin <新しいレポジトリのurl> 
      - [ ] git branch -M main 
      - [ ] git push -u origin main

- [ ] github pages上でページの公開設定を行う
    - [ ] 公開設定方法は例えば以下の記事を参照
    - [ ] https://qiita.com/snow_swallow/items/631bbceabbb953da2646
- [ ] google search consoleの調整
  - [ ] 新しい五月祭/駒場祭のページとtalks,timetableを登録
  - [ ] 古い五月祭/駒場祭のページとtalks,timetableを復活

### 五月祭/駒場祭詳細判明後
- [ ] ut-10min.github.io/XX/index.html
  - [ ] 日付、会場、時間を更新

### 講演内容、タイムテーブル確定後
- [ ]js周りを更新
  - [ ] ut-10min.github.io/XX/data.js
    - [ ] data.jsの講演者名、講演者所属、講演者分野、講演題目、講演アブストを更新
  - [ ] ut-10min.github.io/XX/timedata.js
    - [ ] timedata.jsのタイムテーブル（時刻、講演者名, "第X部", "改行" or "休憩・座談会" ）を更新
  - [ ] ut-10min.github.io/XX/timetable.js
    - [ ] ワークショップがある場合に例外処理を追加

#### memo
- 動作に注意が必要なのは、data.js、timedata.js、timetable.jsによるタイムテーブル生成です。
- 処理部分はtimetable.jsに記述されています。
- data.jsには講演者・講演内容の情報が入っています。（講演者名、講演者所属、講演者分野、講演題目、講演アブスト）
- timedata.jsには講演のタイムテーブルが入っています。（時刻、講演者名, "第X部", "改行" or "休憩・座談会" ）
- timetable.jsは、data.jsとtimedata.jsをすり合わせてタイムテーブル（時刻、講演者名, "第X部", "改行" or "休憩・座談会" 、講演タイトル、講演者所属）を生成します。

すり合わせの際に、講演者名, "第X部", "改行" or "休憩・座談会"をname に格納して、それが "第X部", "改行" or "休憩・座談会"を含むかどうか、含まない場合は対応する講演者名を探して、講演者・講演情報を引っ張ってきます。

timedata.jsには名前があるけどdata.jsには名前がない講演者がいたりすると、ここの判定がうまく回らず、タイムテーブルが表示されません。いまのmf98のページのtimedata.jsでは、（ここの判定をわざとバグらせて）タイムテーブルを非表示にするために二行目に"00:00": "非公開",と記述してます。


### リンク判明後随時
- [ ] ut-10min.github.io/vote.html
  - [ ] リダイレクト先のurlを最新の五月祭/駒場祭のurlに書き換え
- [ ] ut-10min.github.io/registration/index.html
  - [ ] リダイレクト先のurlを最新のZoomのurlに書き換え
- [ ] ut-10min.github.io/donation/
  - [ ] リダイレクト先のurlを最新のコングラントのurlに書き換え
- [ ] ut-10min.github.io/questionnaire/
  - [ ] リダイレクト先のurlを最新のアンケートgoogleFormのurlに書き換え
- [ ] ut-10min.github.io/vote.html
  - [ ] リダイレクト先のurlを最新の五月祭/駒場祭ランキングのurlに書き換え
  - [ ] 五月祭/駒場祭ランキングのurlが公開されるのはおよそ2日前とのこと

### 前々日~24h前くらいまで
- [ ] google search consoleの調整
  - [ ] 新しい五月祭/駒場祭のページとtalks,timetableを登録
  - [ ] 古い五月祭/駒場祭のページとtalks,timetableを一時的に削除


## その他すべきこと
- jQueryを廃止してcssに書き換え
  - jQueryが時代遅れなため
- 各五月祭/駒場祭のページの、timetableの表示方法を変更する
  - タイムテーブルの設定が、各文字列の中心の高さ座標を揃えるように設定されている
  - そのため現状では、講演のタイトルが長くなった時にタイムテーブルが見えにくくなる
  - タイムテーブルの読みにくさは特にスマホで閲覧した時に顕著
  - 【解決法】タイムテーブルの中のセルの表示を上揃え（valign="top"）にする
  - TODO: 駒場祭のタイムテーブルの表示方式を上記に更新する



### （generalに）変更される可能性がある部分のリスト（思いつき次第追加）
- css
- img

【役割】ロゴ置き場
- js

- data.js

【役割】講演者名、講演者所属、講演者分野、講演題目、講演アブストのソースデータ
- main.js
- timedata.js

【役割】講演プログラムのソースデータ
- TODO

講演プログラムが決定次第追記

timetable.jsがバグらないように適切な入力を行う

- timetable.js

【役割】timedata.jsおよびを読み込んで、タイムテーブルを生成、timetable.htmlに結果を投げる

mf97の場合には、

(1)"第X部"の場合→

【めも】ここの動作がバグると、タイムテーブルが表示されない。
- 複数の題目で講演する人がいる場合
- 座談会に名前がある場合
- 講演の部数が変わる場合

...など

- index.html

【役割】メインページを表示
- talk.html

【役割】講演題目を表示
- timetable.html

【役割】講演プログラムを表示