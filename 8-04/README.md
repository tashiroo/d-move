### 8/04

#09 イベントの仕組みを理解しよう

`<li style={{backgroundColor:props.color}} ></li>`に`onClick={contUp}`を追加して`<li style={{backgroundColor:props.color}} onClick={contUp}>`にする。
次に`function countUp(){alert()}`を作ってクリックするとアラートが表示されるようにする、その後`alert()`内に引数 color を入れる

- 使ったイベント

| メソッド 式              | 何に対して     | どう使った？                                                                    | 効果                         |
| ------------------------ | -------------- | ------------------------------------------------------------------------------- | ---------------------------- |
| `.preventDefault();`     | a タグ         | ページが移動しないようにした                                                    | 入力やページ移動どの無効化   |
| `alert(文字,または引数)` | a タグ li タグ | 引数を color にしてボックスをクリックすると対応する色の名前がアラート表示される | クリックするとアラートが出る |

#10 Class に書き換えてみよう

- state を使った component を作るためには class にしなければならないので function を class に書き換える

- class を作ってその中に`<li style={{backgroundColor:props.color}} ></li>`を入れる、ただそのままだと使えないので`<li style={{backgroundColor:this.props.color}}>`のように引数に this を付ける

- `class クラス名 extends React.Component{render(){return()}}`でできる

- REACt のクラスについては公式サイト参照 →https://ja.reactjs.org/docs/react-component.html

  #11 State を使ってみよう

- REACt の state については公式サイト参照 →https://ja.reactjs.org/docs/state-and-lifecycle.html

- 前回作った class に`constructor()`と`super()`を追加する

- 2つの`()`内に引数`props`を入れる






- ざっくりいうと

constructor は class の先頭に 1 つだけ作ることができるもの
super は親 class の constructer を呼び出すもの

class については MDN 参照 →https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Classes

