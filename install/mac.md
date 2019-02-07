# インストール

それでは最初にFlutterのインストールから始めましょう。
環境によってインストール方法が異なるため、注意してください。

また、Windowsで開発する場合はiOSアプリの開発を行うことはできません。

## Mac

### インストールに必要な必須条件
- MacOS(64bit)
- ディスクスペースの空き容量が700MB以上あること
- 以下ツールがインストールされていること
  - bash
  - curl
  - git 2.x
  - mkdir
  - rm
  - unzip
  - which 

### 1. Flutterの入手

公式サイトからflutterをダウンロードしましょう。  
[https://flutter.io/docs/get-started/install/macos](https://flutter.io/docs/get-started/install/macos)

ダウンロードしたファイルを解凍して好きなところに配置してください。

```
$ cd ~/development
$ unzip ~/Downloads/flutter_macos_v1.0.0-stable.zip
```
※ unzip対象はダウンロードしたFlutterのファイルです。

解凍できたら、PATHを通してコマンドが利用できるようにしましょう。

```
$ export PATH="$PATH:`pwd`/flutter/bin"
```

実際にコマンドを実行して動作するのを確認できたら完了です。

```
$ flutter --version
Flutter 1.0.0 • channel stable • https://github.com/flutter/flutter.git
Framework • revision 5391447fae (10 weeks ago) • 2018-11-29 19:41:26 -0800
Engine • revision 7375a0f414
Tools • Dart 2.1.0 (build 2.1.0-dev.9.4 f9ebf21297)
```

このままだと、一時的な登録となってしまうので、永続的な登録をするのであれば、```$HOME/.bash_profile```に登録しましょう。

```~/.bash_profile
export PATH="$PATH:[PATH_TO_FLUTTER_GIT_DIRECTORY]/flutter/bin"
```
※ 「[PATH_TO_FLUTTER_GIT_DIRECTORY]」を実際のパスと置き換えてください。

### 2. Flutterの実行環境を整える。

FlutterはAndoird、iOSの2つのアプリを一括で作るため、両方の環境が必要になります。
実行環境を整えるのに便利なコマンドがFlutterにはあるのでそちらを利用して整えていきましょう。  
コマンドは以下になります。

```
$ fluttter doctor
```

実際のコマンドを叩くとFlutterでの開発に必要な情報を収集して診断してくれます。

問題がある場合は太字で表示されるので、それぞれ解決していきましょう。

### 3. iOSセットアップ

1. Xcode9.0以降をインストールしてください。

2. 以下のように設定することで最新のXcodeが指定できます。

```
$ sudo xcode-select --switch /Applications/Xcode.app/Contents/Developer
```

別のバージョンを利用したい場合は、パスを設定してください。

3. Xcodeを開いて確認するか以下コマンドにて、仕様許諾に同意してください。

```
$ sudo xcodebuild -license
```

4. シミュレータを設定する。

   以下のようにコマンドで起動するか、Spotlightなどでシミュレータを起動させます。

```
$ open -a Simulator
```

5. シミュレータを起動して[ハードウェア]>[デバイス]メニューの設定を確認して、シミュレータが64ビットデバイス(iPhone5s以降)を使用していることを確認してください。

### 4. Androidの設定

1. [Android Studio](https://developer.android.com/studio/)をインストールしてください。

2. Android Studioを起動して、「Android Studioセットアップウィザード」を実行します。

   Flutterに必要な、最新のSDKをインストールしてください。

3. エミュレータを設定する。

   起動の[Android Studio] > [Tools] > [Android] > [AVD Manager]から[Create Virtual Device]を選択して新規にエミュレータを作成してください。

   エミュレータを作成するときは*x86*または*x86_64の*イメージが推奨されています。



## 実機インストール

実機インストールについてはまた別の手順が必要なため、改めて設定してください。



## 参考

[Flutter Install](https://flutter.io/docs/get-started/install)

[Flutter](https://www.youtube.com/watch?time_continue=3&v=fq4N0hgOWzU)