### 8/05

#12 React Developer を使おう

#### デベロッパーツールだと component の中身が見れないので React Developer Tools を Chrome に入れて見れるようにする

1. React Developer Tools Chrome と検索する、React Developer Tools というサイト名？があるので入る

2. chrome ウェブストアに入るので Chrome に追加という青い buttom が右上にあるのでクリック

3. 「React Developer Tools」を追加しますか？というアラートが出るので拡張機能を追加を押す

4. 右上のパズルのアイコン？をクリックし拡張機能の管理を押す、一応 React Developer Tools がオンになっているか確認する

#### 使ってみよう

1. F12 でデベロッパーツールを開く

2. Components があるので押すと要素が出てくるので選択すると中身が見れる

#13 setState で値を更新しよう

- まず`<li style={{ backgroundColor: this.props.color }}>`に`onClick={this.countUp}`を足して`<li style={{backgroundColor: this.props.color}}onClick={this.countUp}>`にする

- 次に countUp 関数を作っていく中身はカウンターなのでクリックすると数字が+1 になるようにするので`countUp(){ this.state.count = this.state.count +1;}`とする

- ただ、REACT では this.state に値を代入できるは constructor だけになっているのでこの場合は setState を使ってコードを入力していく

- `this.setState({count: this.state.count + 1,});`と書き換える、ただし setState を処理するタイミングは REACT が決めるので思ったように処理できないこともある

- prevState を使うと直前の値を持ってくることができるので `this.setState(prevState=> {return {count: prevState.count + 1,}});`と書き直す


- `onClick={this.countUp}`のように countUp が()に囲まれていないと this が undifind になってしまうが constructor 内で`this.countUp = this.countUp.bind(this);`を入力することで解消できる

#### 注意点など

- REACT では setState するたびに`render()`が呼び出される

- `bind()`bind メソッドはよく使うので勉強しておく