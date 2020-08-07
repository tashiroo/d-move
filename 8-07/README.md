### 8/07

#16 ループ処理でリストを描画してみよう

#17 イベント処理を親要素に渡していこう

- JSX では for 文を使うと読み込み中になって表示されないため `map()`を使う

- 参照 REACT.s 超入門 p91 の末尾から p95 まで

- map メソッドについっては MDN までhttps://developer.mozilla.org/ja/

- そのままループ処理を入れると`react.development.js:401 Warning: Each child in a list should have a unique "key" prop.`というエラーが出る

- keyは要素の追加、変更、削除をどの要素がしたのかREACTがわかるようにつけるマーカー？

- 公式サイト参照 URL https://ja.reactjs.org/docs/lists-and-keys.html

- `.map((counter) => {return <Counter counter={counter} key={counter.id} countUp ={props.countUp}/>;});`マップの中でカウンターを作るためにcountUpを設定する

- keyはid属性を持たせることができるので上記のように記入する

