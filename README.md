# 研究室の入退室管理システム
現状、スプレッドシートで研究室の入室を管理しているが、入力状況が良くない。
研究室に入った時に、学生証で入退室登録できるようにしたい。
## 必要な機能
- 管理権限は小松と植田と先生？が持つ
- 学生証を登録する
- 入退室時刻を記録する
- 音を鳴らす（一部）
- スプレッドシートにデータを蓄積
- ユーザー情報はDBに登録
- Slackに流す
- 別途研究室の現在の状況が分かるような場所を作る
- 間違えたときどうするか（スプレッドシートの修正はできる？手動？）
- 22時に退室していない場合は、「忘れてませんか？」の通知をする
- 研究室めっちゃ居るやつランキングとか取れたデータで遊ぶ笑
- ユーザーの登録、削除は管理者の手動

# 設計・計画・構成
## Raspberry Pi
- スピーカ、ボタン、LEDは研究室にあるArduino用のモジュールを利用
- 入室、退室、取り消し
- ボタン（1個）押して、入室、退室、取り消しの順に光る
- 押してからカードを読み込む
- 取り消しは一つ前の項目だけ（実現可能性不明）
- ユーザーのデータベース

## NFC(Pasori)

## Slack
後ほど

## スプレッドシート
- ファイルは1つ（shikidalab_EEM）
- 1人1人シート分けて蓄積する
- 
## Webページ（学外からも見たい）

# プロトタイプ
- 1人登録してみる
- ボタンなしで手動で入室、退室、取り消しをテストする


# 参考
- https://www.membersedge.co.jp/blog/raspberry-pi%E3%81%A8nfc%E3%82%BF%E3%82%B0%E3%81%A7%E8%87%AA%E5%AE%85%E3%81%AE%E6%B6%88%E8%80%97%E5%93%81%E7%AE%A1%E7%90%86%E3%81%AE%E4%BB%95%E7%B5%84%E3%81%BF%E3%82%92%E4%BD%9C%E3%81%A3%E3%81%9F/
- https://moriokalab.com/news/75
- https://qiita.com/shigeru-yokochi/items/a91c0a3cb1fbb7cafafe
- https://www.ecninc.co.jp/post/2
- https://monomonotech.jp/kurage/raspberrypi/nfc.html
- https://dev-kk2.hatenablog.com/entry/2018/01/09/174220
- https://www.farend.co.jp/blog/2018/03/faye/

# helloworld
