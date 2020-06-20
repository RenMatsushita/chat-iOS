# chat-iOS
## 開発規約
### アーキテクチャ 
- ViewController
  - /Views/画面名(例: SignUp)/画面名ViewController.swift
  - Viewの表示処理、Viewからの入力受け取り(textfield, button等)
- Presenter
  - /Views/画面名/画面名Presenter.swift
  - Viewからの入力の受け取り、Modelの出力の受け取りを良い感じに統合してView, Modelそれぞれに返す
- ModelはViews/画面名/画面名Model.swift
  - firebaseアクセス等
- /Extensions
  - 標準ライブラリ、使用ライブラリの拡張を記述
- /Libraries
  - Extensionを使わないビジネスロジックを記述
- StoryboardはViews/Storyboards/に格納する
## setup
以下のコマンドを実行した後、デバッグ環境の場合chat-iOS/Resources/GoogleInfoにGoogle-Info-dev.plistを入れる
※ GoogleService-Info.plistからGoogleService-Info-dev.plistに改名する
homebrewをインストールしていない場合
```
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
carthageをインストールしていない場合
```
$ brew install carthage
```
```
mintをインストールしていない場合
$ brew install mint
```
上記全てのインストールが完了した後に下記を実行
```
$ make all
```
