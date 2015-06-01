# hubot-hiraganize-goo

gooラボのひらがな化APIを利用してチャット上の発言をひらがな、カタカナに変換します

## インストール

npmからインストール

```bash
$ cd /path/to/hubot
$ npm install --save knjcode/hubot-hiraganize-goo
```

`external-scripts.json`へスクリプトを登録

```bash
$ cat external-scripts.json
["hubot-hiraganize-goo"]
```

## 使い方

hiragana でひらがな化、 katakana でカタカナ化します。

```bash
user1>> hubot hiragana 漢字が混ざっている文章
hubot>> かんじが まざっている ぶんしょう

user1>> hubot katakana 幽遊白書
hubot>> ユウユウハクショ
```

### gooラボのアプリケーションID設定

このスクリプトはgooラボの[ひらがな化API](https://labs.goo.ne.jp/api/2014/338/)を利用しています。
APIの利用にはアプリケーションIDが必要になります。

[gooラボAPI利用登録](https://labs.goo.ne.jp/apiregister/) からアプリケーションIDを取得し、
以下の例を参考に環境変数を設定してください。

### herokuでの環境変数設定

```bash
% heroku config:add GOOLAB_APP_ID="YOUR_GOOLAB_APP_ID"
```

### UNIX等での環境変数設定

```bash
% export GOOLAB_APP_ID="YOUR_GOOLAB_APP_ID"
```

## 謝辞

[gooラボ ひらがな化API](https://labs.goo.ne.jp/api/2014/338/)

[![supported by goo](https://u.xgoo.jp/img/sgoo.png)](http://www.goo.ne.jp/)

## ライセンス

[gooラボAPI利用規約](https://labs.goo.ne.jp/apiterm/)に従って利用ください。
