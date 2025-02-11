# Todo List
<img width="546" alt="todoアプリのlogo" src="https://github.com/hapiharu012/Todo/assets/120043995/840f9f8e-270f-432e-b9dd-e1ada64e2a02">


## 概要

「Todo List」はアプリを起動するとmacのメニューバーに予定が表示され，一目で自分がすべきタスクを確認することができます．
タスクの追加，完了，削除はメニューバーからwebサイトにとび，行うことができます．
## 開発のきっかけ
- このアプリはタスクをスマートに管理できるアプリが欲しい
- 学んだ技術(Python,SQLite)をアウトプットしたかった
## こだわり
見やすてくシンプルなデザイン，かつ直感的に使いやすいUI，UXを意識して作りました．



## 特徴
- メニューバーから一番優先度の高いtodoが確認できる。
- todoとしての基本的な役割を担う機能はwebアプリとして機能するので端末を問わず利用できる。
- webアプリで登録したtodoは期限を迎えるとMacから通知することもできる。

## 各画面
- webアプリ  
![スクリーンショット 2023-07-16 15 32 41](https://github.com/hapiharu012/Todo/assets/120043995/2e68259a-f9e4-455b-bfa3-a3426a49ebd8)

- メニューバーアプリ  
![スクリーンショット 2023-07-16 15 33 01](https://github.com/hapiharu012/Todo/assets/120043995/63e0d991-2e2b-4f90-b524-8d68a9c54477)

- 通知  
![スクリーンショット 2023-07-16 15 32 52](https://github.com/hapiharu012/Todo/assets/120043995/4351a8b4-f575-4489-af29-873834278bbd)

## データの流れ
![todoアプリ drawio](https://github.com/hapiharu012/Todo/assets/120043995/62cb1b45-1201-4ff7-9c2e-28fef65564f7)

## 各機能説明
### メニューバー
- アプリのアイコンとともに予定と通知をonかoffにしているか表示されます．  
- 表示される予定は登録してある未実行の予定の期限が一番古いものが表示されるようになっています．  
- 通知は表示されている予定の期限になると，macに通知がくるようになっています．通知をonにすると○が，offにすると×が表示されます．
- メニューバーをクリックすると「通知」「Webを開く」「Quit」が表示されます．「通知」は予定の通知のon/offを設定できます．「Webを開く」をクリックすると，Todoを管理するWebページが開きます．
- 「Quit」をクリックするとアプリを終了することができます．
### Webページ
- 予定の「追加」「完了のチェック」「削除」を行うことができます．
予定の「追加」では，予定を入力フォームに入力し，その予定の期限を選択することで「未実行」のところに予定を追加することができます．
- 予定の「完了のチェック」では，チェックボックスにチェックすることで予定の完了を行うことができます．これにより，予定は「未実行」から「実行済」に移動します．
- 予定の「削除」では，いらなくなった予定をデータベースから削除することができます．

## 環境構築
`$ git clone https://github.com/2022AIT-OOP2-G07/Todo.git`

`$ cd Todo`

`$ python -m venv .env`

`$ source .env/bin/activate`

`(.env) $ pip install flask`

`(.env) $ pip install rumps`

### 環境
Python version : 3.10  
`Flask==2.2.2`

`rumps==0.4.0`
## 使い方
### webアプリの起動
- サーバー起動  
  `$ python app.py`
- アプリ起動
  ブラウザで`http://127.0.0.1:5000`にアクセス
### メニューバーアプリの起動
`$ python menubar.py`

---

## 仕様
### 言語
-  Python：サーバ，DBの管理，メニューバーの作成，通知の管理
-  HTML：Webページの表示
-  CSS：Webページの表示
-  Java Script：Webページの表示
-  SQL：DBの操作
### ライブラリ
- Flask：サーバーの構築
- rumps：メニューバーへTodoの表示，macに通知を送る
### データ
- SQLite：予定の保存
- JSON：アプリの設定情報を追加

---

## 工夫点及び改善点
- Webアプリだけでなくメニューバーアプリも作ることでUXを向上させた(通知機能,etc,,,)
- 各機能が正常に動作するか単体テストを行った
- 予定の「編集」機能の追加
- メニューバーアプリからのtodoの追加機能の実装
- アプリのapp化
Pythonのライブラリ「py2app」を用いてapp化
