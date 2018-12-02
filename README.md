# 手順
vueのアプリをcordovaでandroid向けにビルドする手順
## vue のビルド
1. `npm run build`を実行し，vueのアプリをビルドする．
2. ビルド結果のindex.htmlをブラウザで開き，アプリが動作するか確認する(index.htmlをパスを修正する必要があるかも)
## cordovaプロジェクトの作成
1. `cordova create hoge`でプロジェクトを作成する(この場合hogeというディレクトリが作成される)
2. `cd hoge`でディレクトリに移動する
3. `cordova platform add android`でビルド対象のプラットフォームを追加する
## vueアプリの配置
1. vueのビルドによって生成された dist ディレクトリの中身を cordovaプロジェクトの wwwの下に配置する
## 環境変数の確認
1. `ANDROID_HOME`という環境変数を設定している場合，sdkディレクトリまでパスに含まれているか確認する
## cordovaのビルド
1. `cordova build android`を実行する
## インストール
1. androidを接続する
2. `adb install xxxx.apk`を実行する