## React & Redux & Material UIでのアプリケーション開発
業務でReact & Reduxで書かれたアプリケーションのコンサルティングをする必要があり、
基本をキャッチアップするためのアプリケーション開発を行った。

* 教材URL
[React × Redux 初心者入門](http://www.hirooooo-lab.com/entry/development/react-redux-setup-environment)

### Day1 環境構築

* [React × Redux 初心者入門(1日目：環境構築編)](http://www.hirooooo-lab.com/entry/development/react-redux-setup-environment
)

教材URLの投稿日が2016年7月、私の作業開始日は2017年7月で1年間空いており、
バージョンも大きく変わっていました。

この変化により、webpack.config.jsの書き方に違いが在りコンパイルエラーが発生しました。
コンパイルエラーに対する対応は、下記のIssue記録を参照になりますが、
解決にかなりの時間を要しそうだったので、途中からバージョンを合わせてinstallし直す方法に切り替えました。
[発生した課題と対応記録](https://github.com/KAZUKI1994/react_webpack_modify/issues?q=is%3Aclosed)

#### 実施した対応

* パッケージインストール時のバージョン指定
筆者のpackage.jsonのバージョンに合わせて、```npm install```でバージョンを指定しました。

```
$ npm install --save react@15.2.1 react-dom@15.2.1 redux@3.5.2 react-redux@4.4.5
$ npm install --save-dev webpack@1.13.1 webpack-dev-server@1.14.1 babel-cli@6.10.1 babel-core@6.10.4 babel-loader@6.2.4 react-hot-loader@1.3.0 eslint@3.0.1 eslint-loader@1.4.1 eslint-plugin-react@5.2.2 babel-eslint@6.1.2 file-loader@6.2.4 babel-preset-es2015@6.9.0 babel-preset-react@6.11.1 css-loader@0.23.1 style-loader@0.13.1
```

* asyncが入っていないと怒られたのでinstall

```
$ npm install --save-dev async
```

上記2点の対応でDay1を完了しました。
