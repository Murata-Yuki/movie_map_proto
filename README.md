<div id="top"></div>


<!-- シールド一覧 -->
<!-- 該当するプロジェクトの中から任意のものを選ぶ-->
<p style="display: inline">
  <!-- フロントエンドのフレームワーク一覧 -->
  <img src="https://img.shields.io/badge/-Node.js-000000.svg?logo=node.js&style=for-the-badge">
  <img src="https://img.shields.io/badge/-React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB">
  <!-- HTML言語一覧 -->
  <img src="https://img.shields.io/badge/-HTML-E34F26.svg?logo=python&style=for-the-badge">
  <img src="https://img.shields.io/badge/-CSS-1572B6.svg?logo=nginx&style=for-the-badge">
  <img src="https://img.shields.io/badge/-JavaScript-F7DF1E.svg?logo=mysql&style=for-the-badge&logoColor=white">
</p>


<h1 align="center">3D Movie Map</h1>


## 目次


1. [3D Movie Mapについて](#3D Movie Mapについて)
2. [操作方法](#操作方法)
3. [環境](#環境)
4. [ディレクトリ構成](#ディレクトリ構成)
5. [開発環境構築](#開発環境構築)


## 3D Movie Mapについて
全方位映像を用いた屋内を探索するバーチャルツアー




## 操作方法
![Sample Image](src/gitlab/home.png)
全方位映像を360度操作可能
フロアマップのマーカーは部屋内または交差点を示す


| ボタン              | 機能                  |
| ------------------- | -------------------- |
| start button        | 映像の再生            |
| stop button         | 映像の停止            |
| reverse button      | 180度反対方向へ切り替え|
| left button         | 左折                  |
| straight button     | 直進                  |
| right button        | 右折                  |
| floor button        | 階層の切り替え         |


## 環境


<!-- 言語、フレームワーク、ミドルウェア、インフラの一覧とバージョンを記載 -->


| 言語・フレームワーク  | バージョン |
| --------------------- | ---------- |
| Node.js               | 20.13.1    |
| React                 | 18.2.0     |
| react-leaflet         | 4.2.1      |
| pannellum-react       | 1.2.4      |


## ディレクトリ構成


<!-- > tree -a -I "node_modules|.next|.git|.pytest_cache|static|.gitattributes|.gitignore|JSON.py|.vscode -->
<pre>
.
├── README.md
├── build #npm run buildで作成
│   └── index.html
├── package-lock.json
├── package.json #ライブラリ・3D Movie Mapの構成方法
├── public
│   └── index.html
└── src
    ├── App.css
    ├── App.js #使用するコンポーネント・遷移するページのRoute
    ├── component #コンポーネント一覧
    │   ├── footer #フッター
    │   │   ├── Footer.css
    │   │   └── index.js
    │   ├── map #キャンパスマップ
    │   │   ├── Markers.js #マーカーを表示・クリックしてページ遷移
    │   │   └── index.js #キャンパスマップを表示
    │   ├── navbar #ナビゲーションバー
    │   │   ├── Navbar.css
    │   │   ├── Navbar_sumi.js #鷲見研・オープンキャンパス用のナビゲーションバー
    │   │   └── index.js
    │   ├── panorama #パノラマ用
    │   │   ├── 2DMap.js #フロアマップ
    │   │   ├── AirplaneMarker.js #フロアマップ上を動くアニメーション
    │   │   ├── DropDownButton.js #階層の切り替えのドロップボタン
    │   │   ├── FloorChange.js #階層の切り替え
    │   │   ├── Markers.js #マーカー・ページ遷移
    │   │   ├── SumiLab.js #鷲見研の全方位画像 1
    │   │   ├── Sumilab2.js #鷲見研の全方位画像 2
    │   │   ├── css
    │   │   │   ├── customHotspot.css #hotspotのcss
    │   │   │   └── panorama.css #ボタンのcss
    │   │   ├── data #全方位映像の軌跡のデータ(js)
    │   │   ├── panellumVideo.js #全方位映像・UI
    │   │   ├── useDropdown.js #ドロップダウンするためのコンポーネント
    │   ├── research #研究紹介
    │   │   ├── components
    │   │   │   ├── BodyCard.js #ブロック
    │   │   │   ├── Content.js #研究内容
    │   │   │   ├── Header.js
    │   │   │   ├── ScrollTop.js #ページ遷移すると自動で一番上にリセット
    │   │   │   └── researches #研究紹介ページ
    │   │   ├── css
    │   │   │   └── Header.css
    │   │   └── index.js
    │   └── screens #home
    │       ├── Top.js #home画像を表示
    │       └── css
    │           └── Top.css
    ├── css
    │   ├── index.css
    │   └── style.css
    ├── gitlab #gitlabで表示する画像
    ├── images #使用画像
    │   ├── O1 #1階の全方位映像
    │   ├── O2 #2階"
    │   ├── O3 #3階"
    │   ├── O4 #4階"
    │   ├── O5 #5階"
    │   ├── introduction #研究紹介画像
    ├── index.css
    ├── index.js
    └── trajectry #全方位映像の軌跡のデータ(txt)
</pre>


## 開発環境構築


### 3D Movie Mapをclone
~~~
git clone http://jupiter.vssad.it.aoyama.ac.jp/murata.yuki/movie_map_proto.git
cd movie_map_proto
~~~

### 3D Movie Mapの実行
~~~
npm start
~~~

**メモリ不足の場合**
~~~
npm start CI=1
~~~

もしくは
~~~
npm run build
serve -s build
~~~

<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> </a> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> <a href="https://nodejs.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="nodejs" width="40" height="40"/> </a> <a href="https://reactjs.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" alt="react" width="40" height="40"/> </a> </p>

