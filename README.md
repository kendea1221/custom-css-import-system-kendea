# バージョン、アップデートについて

このことに関しては[こちら](https://github.com/kendea1221/custom-css-import-system-kendea/blob/main/version.md)をご覧ください

-----------------------------------------------------------------
# 概要
- カスタムCSSを活用して、学校の通信アプリを改造したいと思った
- もともと、調べてみるとStylishという拡張機能を使っていた
- だけど、要素を調べながら書きたいから自分で作ろうと思った

## 作ったファイル
- manifest.json
- Classi-platform
  - script.js
  - style.css
- Google
  - script.js
  - style.css
- twitter
  - script.js
  - style.css
- YouTube
  - script.js
  - style.css


## コード
#### manifest.json
```json
{
  "name": "Vialdi CSS Import for Kendea",
  "author": "Kendea",
  "description": "chrome extension for customize CSS and JS.",
  "version": "1.0.0",
  "manifest_version": 2,
  "web_accessible_resources": ["*"],
  "permissions": ["storage"],
  "icons": {
   "48": "icons/48.png"
  },
   "content_scripts": [
    {
      "matches": ["https://www.google.com/*"],
      "css": ["google/style.css"],"js": ["google/script.js"]
    },
    {
      "matches": ["https://platform.classi.jp/group2/*"],
      "css": ["classi-platform/style.css"],"js": ["classi-platform/script.js"]
    },
    {
      "matches": ["https://www.youtube.com/*"],
      "css": ["YouTube/style.css"],"js": ["YouTube/script.js"]
    }
  ]
}
```

#### Classi-Platform/script.js
```javascript
consol.log("正式にインポートできています")
```
#### Classi-Platform/style.css
```css
@import url('https://fonts.googleapis.com/css2?family=DotGothic16&display=swap');


body{
    font-family: 'DotGothic16', sans-serif;
    background-image: url(https://img.freepik.com/premium-photo/digital-cyberspace-and-data-network-connections_24070-1044.jpg?w=2000);
}

#header{
    background-image: url(https://img01.jalannews.jp/img/2020/11/20201124_hoshizora_019.jpg)
}

#header .gNavi li {
    border-right: 0px!important;
}
.spen-ly-global-header {
    background-image: url(https://img01.jalannews.jp/img/2020/11/20201124_hoshizora_019.jpg)
}

.spen-ly-global-menu-list .menu-list-wrapper {
    backdrop-filter: blur(9px);
    background-color: rgb(98 98 98 / 11%);
}

.spen-ly-global-header .header-content {
    border-right: 0px!important;
}

.spen-ly-global-header .user-information .user-icon {
    border-radius: 34px;
    backdrop-filter: blur(9px);
}

.mod-message {
    display: block;
    color: blue;
    border: 1px solid #ccc;
    padding: 16px 13px 0;
    background-color:#c8e7fa;
    border-radius: 15px;
}

.group-item-list{
    background-color: rgb(255, 222, 172);
}

.new-item-list{
    background-color: #ccc;
    border: 1px black;
}

.header{
    background-color: blanchedalmond;
}
```

#### YouTube/script.js(雑)
```javascript
console.log("インポートできています")
```

#### YouTube/style.css(手抜き)
```css
*{
    color: #607d8b;
}
```

#### Google/script.js
```javascript
console.log("インポートできています")
```

### Google/style.css
```css
@charset "utf-8";

*{
  background: #333 !important;
}
```
## 最後に

現在掲載しているコードは三つのサイトと少ないですが、僕の[Github](https://github.com/kendea1221/custom-css-import-system-kendea)を見てもらうとわかるのですが、いろいろコードを載せているので持って行っちゃってください、
一応licenseはありますのでお読みください。

最期までありがとうございました。

## CopyLight
- 2022 [Kendea](kendea.com@gmail.com) all rights reserved.
