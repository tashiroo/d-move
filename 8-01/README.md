## 8/01 属性やイベントを理解し Component を作ろう

### 5 属性やイベントをつかってみよう 動画 URL https://dotinstall.com/lessons/basic_reactjs/44405

#### camelCase について

- className など単語の一つ目が小文字二文字目の単語の頭が大文字なのをキャメルケースという

#### React の書き方違い

- Javascript では`<div class ="name">`を`<div className ="name></div>`と書く、これは class は javascript で予約語となっているため

- 予約語とはプログラミングですでに意味を持っている言葉を指す、例 if for など、class はクラスを使うときに使用するために class のみを定義することはできない

- React は-が使えないので HTML の script の中に 直接 CSS を書く場合は `background-color` は`backgroundColor`と`text-align`は`textAlign`と書く

- 今回の動画は script に直接 CSS に記入する物と onClick のイベントを作るやり方をやった

  `function showMessage() {alert("Hello");}`

  `ReactDOM.render(`
  ↓ ボックスクラスをつけて stylecss ファイルから css を読み込んで使うときの書き方
  `<div className="box"></div>,`  
   ↓ 直接 script 内に css を書くやり方 ""を付けると javascript では string 型で認識されてしまうため html と書き方が違う、{}の中にさらに{}を入れて`style={{CSSの入力欄}}`とする
  `<div style={{width:100,height:100,backgroundColor:'tomato'}} ></div>,`  
   ↓ 上記内容に onClick イベントを足した時の書き方 javascript のコードは{}で囲んで使う
  `<div style={{width:100,height:100,backgroundColor:'tomato'}} onClick = {showMessage}></div>,`

  `document.getElementById("root")`

  `);`

### 6 Component を作ってみよう 動画 URL https://dotinstall.com/lessons/basic_reactjs/44406

#### Componentとは？ React公式サイト 参照URL https://ja.reactjs.org/docs/components-and-props.html

- コンポネートタグという独自のタグを作って機能を加えることができる

- コンポネートタグの最初は大文字になる、例`</Counter>`

- コンポネートはpropsというオブジェクトを引数にして使うことができる

- 読み込み専用でpropsの値を後から変えることはできない

- 今回の動画は Counterのコンポネントを作るやり方をやった

`function Counter(props){`
        `  return <div>0 {props.color}</div>;`
      `}`
      `ReactDOM.render(`
      `<div>`
    `<Counter color="tomato"/>`
    `<Counter color="skyblue"/>`
    `<Counter color="limegreen"/>`
    `</div>`

    
