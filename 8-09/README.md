### 8/09

#### REACT MAIN CONCEPTS を読んでみよう

1. REACT の公式サイトの TUTORIAL → 概要 → データを props を渡す

2. REACT の公式サイトの Q&A → コンポネートに関数を渡す

#### props

- クラスの counstructor と super の`()`内に props を入れて関数やイベントを渡す

- this.props というものも使う

- コンポネートが関数にアクセスするために counstructor 内でバインドする

- `class CLASS extends Component {`
  `counstructor(props){`
  `super(props);this.関数もしくはイベントハンドラー = this.関数もしくはイベントハンドラー.bind(this)}}}`

- 上のコードのように入力すると this をその関数もしくはイベントハンドラーに限定して動作させることができる

- それを行わないと値が定まらず undifend が出てしまうことがある

- まだ、すり合わせが終わってないので正確な情報ではないのでもう一度調べる

- 動画学習で行っていた render や関数の中にアロー関数があったものも関数をコンポネートにバインドするために行ったもよう
