## 8/02 Props を理解しよう

### REACT 公式サイトの参照 URL 1 https://ja.reactjs.org/ 

### REACT 公式サイトの参照 URL 2 https://ja.reactjs.org/tutorial/tutorial.html#what-is-react


### 7 Props を使ってみよう 動画 URL https://dotinstall.com/lessons/basic_reactjs/44407

### 8 スタイルを整えよう 動画 URL https://dotinstall.com/lessons/basic_reactjs/44408

- 7 Props を使ってみようは前回のコードを少し改良して引数をstyleに利用する方法をやりました

- `return <div>0 {props.color}</div>;`を書き換えて`return <div style={{backgroundColor:props.color}}>0 </div>;`にして背景色をつけました

- その後`return <div style={{backgroundColor:props.color}}>0 </div>;`を`return <li style={{backgroundColor:props.color}}>0 </li>;`に書き換えてrenderの中のdivにクラスとその子要素にul追加してCSSを使って整えます

- renderの中はこうなります↓ 
`<div className="container">`
`  <ul>`
`    <Counter color="tomato"/>`
`    <Counter color="skyblue"/>`
`    <Counter color="limegreen"/>`
`    </ul>`
`  </div>,`
