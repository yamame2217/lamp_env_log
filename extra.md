# 株式会社ハートビーツさんから出された課題「lamp環境の構築」の課程(おまけ)
気になったことを調べたり考えたりした記録

## AlmaLinuxってなんだ？
'https://almalinux.org/'によると、

>AlmaLinux OS is an open-source, community-driven Linux operating system that fills the gap left by the discontinuation of the CentOS Linux stable release.

え？　the CentOSがdiscontinuationなのか！？
どうやら、CentOS Linux stable releaseが廃止されたギャップを埋める為のOSのようだ。

## UbuntuのLTSってなんだ？
'https://ubuntu.com/search?q=LTS'によると、
> LTS is an abbreviation for “Long Term Support”. We produce a new Ubuntu Desktop and Ubuntu Server release every six months.

Ubuntu Wiki より
>A new LTS version is released every two years. In previous releases, a Long Term Support (LTS) version had three years support on Ubuntu (Desktop) and five years on Ubuntu Server. Starting with Ubuntu 12.04 LTS, both versions received five years support.

LTSはLong Term Supportの略称とのこと。2年ごとにリリースされて、Ubuntu Serverは5年間サポートの対象になる。

とりあえず、迷ったらLTSにしておこう。

## 仮想マシンと本体の表示時刻がちょうど9時間ずれる件について
'https://qiita.com/fkshom/items/bbae5c6c931d78bd8b67'　これによると、
WindowsのJSTの時刻をUbuntuがUTCで読み込むせいで起こるらしい。

## NTPサーバーとは？
NTPサーバーと調べると、一番上にこのサイトが表示される。
'https://jjy.nict.go.jp/tsp/PubNtp/index.html'
NTPサーバーについて説明した一次情報サイトは見つけることができなかったが、恐らく、時刻を配信しているサーバーのようだ。個人サイトにNetwork Time Protocolの略称だと書かれていた。('https://wa3.i-3-i.info/word12072.html')

## yum install httpd　について調べてみた。

まず、"yum install httpd"で検索をかけたが、表示された結果から、一次情報を直ぐに見つけることが出来なかった。

"yum"で検索すると、このページにたどり着いた。'http://yum.baseurl.org/'
どうやらPackage Managerらしい。Package ManagerはaptとかChocolateyとかpipぐらいしか知らなかったので初耳。
かと思いきや、yum...yum...何度も見ていたら以前見たことある気がしてきた。気のせいかもしれない。

"httpd"で検索すると、このページにたどり着いた。'https://httpd.apache.org/'

"yum install httpd"はどうやら"yum"というパッケージマネージャーから"httpd"というパッケージをインストールするという意味のコマンドらしい。
'http://yum.baseurl.org/'ここの説明を見る限り、"httpd"というパッケージにはApacheを動かすために必要なファイルが色々入っていると思われる。