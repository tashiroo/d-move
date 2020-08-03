## 7/31 環境設定と REACT を触ってみよう

### 1 React を使ってみよう 動画 URL https://dotinstall.com/lessons/basic_reactjs/44401

- 動画で使っていた Atom の導入とセットアップ

- 一応 vscode に nodejs を入れる

### 2 開発準備をととのえよう 動画 URL https://dotinstall.com/lessons/basic_reactjs/44402

- React Deveroper Tools を Crome に追加

- React の公式サイトから開発者用スクリプトを持ってくる 参照 https://ja.reactjs.org/docs/getting-started.html

  INSTALLATION → Getting Started → Downroad this HTML fail 日本語ならこの HTML ファイルをクリック

| コード                                                                                | どのようなものか                                     |
| ------------------------------------------------------------------------------------- | ---------------------------------------------------- |
| `<script src="https://unpkg.com/react@16/umd/react.development.js"></script|`         | React の本体                                         |
| `<script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>` | React の結果を反映させるライブラリ                   |
| `<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>`            | Javascript の文法を使うための babel というライブラリ |

- script タグを作る、ローカルの場合は別ファイルにするとエラーになるので直接書く、今回書いた script タグ →`<script type="text/babel"></script>`

### 3 初めての React 動画 URL https://dotinstall.com/lessons/basic_reactjs/44403

1. まず script 内にアロー関数を書く →`<script type="text/babel">(() =>{});</script>`

2. アロー関数内に`ReactCOM.render()`を書く →`<script type="text/babel">(() =>{ReactCOM.render()});</script>`

3. render の（）内に処理を書く →`<script type="text/babel">(() =>{ReactCOM.render( 処理 )});</script>`

- `render()`など詳しくは REACT 公式サイトの API REFERENCE 参照 https://ja.reactjs.org/docs/react-dom.html#render

- 例
  `(() => {`
  `ReactDOM.render(`
  ↓ HTML のように書く最後に , をつけること
  `<p>Hello!</p>,`
  ↓ 上記のコードをどこに表記するか記入する 下のコードの結果 div 内に Hello!が追加され web 上で表示される
  `document.getElementById("root")`
  `);`
  `})();`

### 4 JSX を使ってみよう 動画 URL https://dotinstall.com/lessons/basic_reactjs/44404

- JSX のルール

- Javascript の式を{}で囲んで使うことができる

- 例 定数 name を p に組み込む

  `(() => {`
  `const name = "tashiro";`

      `ReactDOM.render(`
        `<p>Hello! {name.toUpperCase()}</p>,`
        `document.getElementById("root")`
       ` );`
      `})();`

- 複数の要素をそのまま使うことはできない

1. 親要素で囲む

- 例
  `<div>`
  `<p>Hello!</p><hr/><p>ok?</p>`
  `</div>,`

2. 配列にする

- 例
  `[<p>Hello! {name.toUpperCase()}</p>,<p>ok?</p>],`

- 閉じタグがないものは/を<>内に入れる

- 例 hr タグに/を入れる

      `[<p>Hello! {name.toUpperCase()}</p>,<hr/><p>ok?</p>],`

  上記のように<タグ名/>となる

- 今回の内容より進んでいるが REACT 公式サイトの参照 https://ja.reactjs.org/docs/introducing-jsx.html

  MAIN CONCEPTS → 2.JSX の導入
