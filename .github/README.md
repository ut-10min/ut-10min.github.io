# README

## ページの更新について

### 五月祭/駒場祭終了直後
- [ ] ut-10min.github.io/index.html
  - [ ] 最新の五月祭/駒場祭を上に持ってきて次回の開催情報に移した後、整備中の文字を追加
  - [ ] 直近の五月祭/駒場祭を前回の開催情報のところに移す
  - [ ] 直近の五月祭/駒場祭をarchive.htmlに加筆。年度替わりの時は新しい年度の項目を追加し、ページすらない部分には準備中の旨を入れる
- [ ] 各五月祭/駒場祭のページ
  - [ ] リモートで新しいレポジトリを作成
    - [ ] レポジトリ名は "mfXX" または "kfXX" (XXは番号)
  - [ ] ファイルを過去直近のmfXX/kfXXのレポジトリからコピー
    - [ ] ローカルでフォルダことコピーした後、git initして新しいレポジトリとして管理開始
  - [ ] ローカルで内容を更新
    - [ ] config.json
      - [ ] 日付、会場、時間を未定に
      - [ ] 決まってないやつのリンクは404に飛ばす
    - [ ] talks.json,timetable.json
      - [ ] []枠以外を空にする
    - [ ] ローカルで動作確認
      - [ ] cdで作成したフォルダに行き、python3 -m http.serverをターミナルで実行。またはhtmlを右クリックし、Vscodeの拡張機能に入れ解いたLive Serverで開く。
  - [ ] リモートにpush 
      - [ ] git remote add origin <新しいレポジトリのurl> 
      - [ ] git branch -M main 
      - [ ] git push -u origin main

- [ ] github pages上でページの公開設定を行う

- [ ] google search consoleの調整
  - [ ] 新しい五月祭/駒場祭のページとtalks,timetableを登録
  - [ ] 古い五月祭/駒場祭のページとtalks,timetableを復活

### 五月祭/駒場祭詳細判明後
- [ ] ut-10min.github.io/XX/index.html
  - [ ] 日付、会場、時間を更新

### 講演内容、タイムテーブル確定後
- [ ] json周りを更新
  - [ ] ut-10min.github.io/XX/data/.talks.json
    - [ ] data.jsonの講演者名、講演者所属、講演者分野、講演題目、講演アブストを更新
  - [ ] ut-10min.github.io/XX/data/timetable.json
    - [ ] timetable.jsonのタイムテーブル（時刻、講演者名, "第X部", "改行" or "休憩・座談会" ）を更新

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
  - [ ] 五月祭/駒場祭ランキングのurlが公開されるのはおよそ2日前とのことだが、過去のやつを見ると推定可能なので最初からそっちに統一していい。

### 前々日~24h前くらいまで
- [ ] google search consoleの調整
  - [ ] (してなければ)新しい五月祭/駒場祭のページとtalks,timetableを登録
  - [ ] 古い五月祭/駒場祭のページとtalks,timetableを一時的に削除

