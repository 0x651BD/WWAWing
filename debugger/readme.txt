﻿# 共通情報
## ソフト名
  - WWA Debugger
## 作者
  - あるねこ
## バージョン
  - 1.3.0.0
## リリース日
  - 平成26年10月01日
## 連絡先
  - aruneko99@gmail.com
## 配布元
  - http://wwawcontest.aruneko.net/
## 転載
  - まずは連絡を。可否はその都度
## 動作環境
  - .NET Frameworks 4.5以上が動作すること(Windows Vista, 7, 8, 8.1)、および管理者権限があること
　 - なお.NET Frameworks 4.5は http://www.microsoft.com/ja-jp/download/details.aspx?id=30653 でダウンロード可能です
## 開発環境
　　- Visual Studio Professional 2013 (C#による開発)
　　- Windows 7 Home Premium x64
　　- .Net Frameworks 4.5

――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――

# おことわり
本ソフトウェアはフリーソフトです。ご自由にご利用ください。
なお本ソフトウェア自体の著作権は作者のあるねこが、アイコンの著作権はプチさんがそれぞれ保有しています。
このソフトウェアを使用した事によって生じたすべての不利益等に関して、作者は一切の責任を負いません。各自の責任に於いてご利用ください。
また本ソフトウェアは11224番ポートを占有します。同じポートを使用していない事を確かめてから起動してください。

# 概要
Java7になってWWAは一度サーバーにアップロードしないとマップデータを読み込めなくなりました。いちいちアップロードする手間はものすごく面倒です。
そこでこのソフトは、ローカル環境に簡易的なサーバーを立て、アップロードせずともWWAを開発できる環境を提供します。

# ファイル構成
WWA Debugger
├ installer.bat - 簡易インストーラー(実行は任意)
├ readme.txt - このファイル
├ uninstaller.bat - 簡易アンインストーラー(実行は任意)
└ WWA Debugger.exe - 本体ファイル

# インストール方法
特にインストールは必要ありません。必ず「管理者権限」でWWA Debugger.exeを起動してください。
WWA Debugger.exeを右クリックして「管理者として実行」をクリックする事で、管理者権限で実行できます。
毎回管理者権限で起動するのが面倒な人は、一度だけinstaller.batを「管理者権限」で実行してください。
これを実行した後は、毎回WWA Debugger.exeを管理者権限で起動する必要はありません。
また、元の状態に戻したいときは「管理者権限」でuninstaller.batを実行してください。

# アンインストール方法
レジストリ等は一切使用していません。フォルダごと消してください。
ただし、installer.batを使用していた際には、uninstaller.batを実行してから消してください。
そうしないと、サーバー起動設定が残ったままになってしまいます。

# 使い方
まずファイル選択ボタンを押して、WWAを起動できる一式のファイルが揃ったフォルダを開き、その中のHTMLファイルを選択します。
横のテキストボックスは確認用ですが、ファイルパスがわかっている場合直接入力してもらっても構いません。
その後「開始」ボタンを押すと、サーバーが起動し、デフォルトに設定されているブラウザで選択したHTMLファイルが開きます。
このとき、サーバーの二重起動を防止するため、開始ボタンが封印されます。
他のファイルを選択したい場合は、ソフトをいったん終了してから再度上の作業をやり直してください。

# バージョン履歴
- 1.3.0.0 (平成27年05月06日)
  - 存在しないページにアクセスすると404エラーを返す機能を追加
- 1.2.0.0 (平成27年04月28日)
  - MIME Typeに"audio"を含むものに対して
    - Status Code 206
    - Accept-Ranges
    - Content-Range
  - を付加する仕様に変更
- 1.1.1.0 (平成27年04月27日)
  - Content-Typeが正常に出力できない問題を解決
- 1.1.0.0 (平成27年04月27日)
  - Content-Typeの出力機能の追加
  - URIのクエリが付加された場合にも正常にレスポンスするように改良
- 1.0.0.1 (平成26年10月01日)
  - プチさんに書いていただいたアイコンを導入
- 1.0.0.0 (平成26年09月29日)
  - 初期リリース