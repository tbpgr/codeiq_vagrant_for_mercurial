# CodeIQ「Mercurialに入門しよう！」問題 環境構築用 Vagrant

## 補足
このリポジトリの内容はCodeIQの「Mercurialに入門しよう！」問題の環境構築用 Vagrantです。  
apt-get install しているだけなので別に必要なさそうですけど、せっかく作ったのでupします。  

## 環境構成

|－－    |項目                 |備考                  |
|:-------|:-------|:-------|
|OS      |Ubuntu 1204 LTS 32bit|--                    |
|Package |mercurial        |--|

## 前提
* Vagrantのインストール
* VirtualBoxのインストール

## 動作確認済み環境
* Windows7
* Vagrant 1.5.3
* VirtualBox 4.3.10

## 利用手順
* 当リポジトリをclone(gitを利用していない場合は、Download ZIPボタンを押してZIPをダウンロードして解凍ください)

~~~
git clone https://github.com/tbpgr/codeiq_vagrant_for_mercurial.git
~~~

* cloneしたフォルダに移動

* 64bit版 Ubuntu 利用する場合（32bit版 Ubuntu を利用する場合は特に対応不要）

Vagrantfileの下記部分を

~~~ruby
  config.vm.box = "precise32"
~~~

下記に変更してください

~~~ruby
  config.vm.box = "precise64"
~~~

* ターミナルソフトから下記コマンドを実行してVMを起動

~~~
vagrant up
~~~

※既にUbuntu 1204 LTS 32bitのBOXがあり、box名が異なる場合はVagrantfileのbox指定を変更する

* 数分～十数分程度かかると思いますので、こんなことをしながら待つ  
    ※既にUbuntu 1204 LTS 32bitのBOXがある場合はさほど時間がかからないと思います

    * コーヒーを飲む
    * トイレに行く
    * CodeIQの即答系問題を解く
    * 「mercurial vagrant up なう #CodeIQ #mercurial」とつぶやく

* 起動完了を確認(コンソールに「finish provision」と表示されたら完了です)

* SSHで接続します

~~~
vagrant ssh
~~~

* ユーザー名を設定する（commitコマンド利用時に要求されるため、あらかじめ設定しておく必要がある）

※ここを詳細に書くと問題のネタバレになるので省略

* CodeIQで解答提出

* 問題へ挑戦が終わったらVMを削除します。  
※VirtualBoxのメニューから削除してもよいです

~~~
$ vagrant destroy
~~~

* CodeIQで解答提出
* 解答完了のつぶやきをしてみる
* お疲れ様でした
