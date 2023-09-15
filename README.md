# Rese
-レストラン検索、レストラン予約、お気に入り登録が可能なプリケーション

![top](https://github.com/MegumiKurokawa/20230906_megumisasaki_reservation_service/assets/127080181/eb81fd22-a640-4605-aa3e-5c844ec97b87)

## 作成した目的
外部の飲食店予約サービスは手数料を取られるので自社で予約サービスを持ちたい

## 機能一覧
会員登録<br>
ログイン<br>
ログアウト<br>
ユーザー情報取得<br>
ユーザー飲食店お気に入り一覧取得<br>
ユーザー飲食店予約情報取得<br>
飲食店一覧取得<br>
飲食店詳細取得<br>
飲食店お気に入り追加<br>
飲食店お気に入り削除<br>
飲食店予約情報追加<br>
飲食店予約情報削除<br>
エリアで検索する<br>
ジャンルで検索する<br>
店名で検索する<br><br>

## 使用技術
-Laravel 8.x<br>
-PHP

## テーブル設計
![Table1](https://github.com/MegumiKurokawa/20230906_megumisasaki_reservation_service/assets/127080181/23c4674f-f01c-41f5-a3b6-28b1c221665c)
![Table2](https://github.com/MegumiKurokawa/20230906_megumisasaki_reservation_service/assets/127080181/dd1d665c-f87a-47b7-8e1d-91ad04314229)
![Table3](https://github.com/MegumiKurokawa/20230906_megumisasaki_reservation_service/assets/127080181/9865bd70-8e5a-47f4-92f6-e0483c84c89b)

## ER図
![ER](https://github.com/MegumiKurokawa/20230906_megumisasaki_reservation_service/assets/127080181/e87e51e5-16c4-4f44-af89-df90309c8e89)



## 環境構築
リポジトリのクローン<br>
１．Codeをクリックし、SSHのURLをコピー<br>
２．パソコンのターミナル上で git clone と入力後すでにコピーしたURLをペースト<br><br>
Dockerの設定<br>
１．ターミナル上で docker-compose up -d --build コマンドを実行<br>
２．code . コマンドでを実行<br>
３．Docker Desktopを開きreservation_serviceコンテナの確認<br><br>
Laravelパッケージのインストール<br>
１．ターミナル上で docker-compose exec php bashコマンドを実行しphpコンテナ内にログイン<br>
２．phpコンテナ内で composer install コマンドを実行<br><br>
.envファイルの作成<br>
１．phpコンテナ内で cp .env.example .env コマンドを実行<br>
２．phpコンテナ内で php artisan key:generate コマンドを実行してAPP_KEYを発行<br>
３．.envファイルのDBを変更（docker-compose.yml内のenviromentの部分に記載しています）<br>
＊．.envファイルを変更するときに権限エラーが表示されたらターミナル上でsudo chmod -R 777 * コマンドを実行<br><br>
databaseの作成<br>
１．phpコンテナ内で php artisan migrate コマンドの実行<br>
２．phpコンテナ内で php artisan db:seed コマンドの実行<br><br>

## その他
-テストログイン用ユーザー名：hoge<br>
-テストログイン用メールアドレス：hogehoge@test.com<br>
-テストログイン用パスワード：hogehoge
