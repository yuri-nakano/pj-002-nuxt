# pj-002-nuxt
htmlを学習した画面をベースにして三週間ほどで作成したNuxt.jsを使用し会社のHPをイメージして作成した画面です。
ホーム画面、ニュースタブの一部が完成しています。
ホーム画面のみレスポンシブ対応しています。


# DEMO
 ホーム画面
![image](https://user-images.githubusercontent.com/64944011/99475039-0a9d2680-2991-11eb-9e36-1958954bc703.png)
CONTINUE押下時
![image](https://user-images.githubusercontent.com/64944011/101171119-af528000-3682-11eb-9626-760526c09e96.png)
オーバレイが開いている画面
![image](https://user-images.githubusercontent.com/64944011/101170905-70bcc580-3682-11eb-8696-adb4d0aaf672.png)
ニュース画面
![image](https://user-images.githubusercontent.com/64944011/101171153-bb3e4200-3682-11eb-9795-ca3a378d1a7d.png)
![image](https://user-images.githubusercontent.com/64944011/101171166-c002f600-3682-11eb-9019-364c62bfb596.png)
![image](https://user-images.githubusercontent.com/64944011/101171175-c2655000-3682-11eb-97ef-32ec3390dbe1.png)
ニュース画面（ニュースのカテゴリーボタン押下時）
![image](https://user-images.githubusercontent.com/64944011/101171320-ed4fa400-3682-11eb-9876-1b97d778ec4d.png)
![image](https://user-images.githubusercontent.com/64944011/101171331-f04a9480-3682-11eb-8a75-121be06d5b60.png)


 
# Features
 機能一覧
 
 | 画面名 | 機能概要 |
 | ------------- | ------------- |
 | ホーム画面  |  CONTINUE押下時モーダルが出る |
 |   |  メニューボタン（右側のハンバーガーメニューボタン）押下時オーバーレイが開く |
 | オーバーレイが開いている画面  |  Twitter・Facebookにリンクが飛ぶ |
 |   |  左上のロゴをクリックするとホーム画面に戻る |
 |   |  CONTACTを押すとURLに飛ぶ |
 |   |  HOMEなどが書いてある一覧にカーソルを当てると日本語表示になる |
 |   |  ニュース・ホームをクリックすると画面に飛ぶ |
 | ニュース画面  | メニューボタン（右側のハンバーガーメニューボタン）押下時オーバーレイが開く（左上のロゴをクリックするとホーム画面に戻る以外の動きは上記と一緒です）  |
 |   | Twitter・Facebookにリンクが飛ぶ |
 |   | ニュースが一覧で表示される・ページネーション出来る |
 |   | ニュースのカテゴリーボタンを押すとカテゴリーに合うものだけが表示される |
 
 
# Requirement
 
"hoge"を動かすのに必要なライブラリなどを列挙する
 
* Node.js v12.18.0
* nuxt/cli v2.12.2
* Ruby Sass 3.7.4
 
# Installation

## Node.js
https://qiita.com/sansaisoba/items/242a8ba95bf70ba179d3
リンク先の手順で進めていく
 
## Nuxt.js
npx create-nuxt-app pj-002-nuxt とコマンドを打ち、課題の雛形を作成します。
Nuxtのセットアップは次の画像のように設定してください。
![image](https://user-images.githubusercontent.com/64944011/101172656-cbefb780-3684-11eb-81bf-7f7559c1128b.png)

yarnを選択しても良いです。
 

Sass
`npm install sass-loader node-sass`
# Usage
 
```bash
git clone https://github.com/yuri-nakano/pj-002-nuxt.git
cd pj-002-nuxt
npm i
npm run dev
```
 
# Note
 
※まだ作成途中なので開ける画面はホームとニュース画面のみになります。

 
# Author
 
* 作成者 中野由梨
* E-mail　nakanoyuri.03@gmail.com
 
