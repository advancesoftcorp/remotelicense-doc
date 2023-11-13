============
使い方
============

.. _setting:

サーバー情報設定
================

:guilabel:`Host` タブでサーバーへの接続に関する設定を行います。

以下の項目を入力・設定してください。

- Host Name

   サーバーのホスト名（またはIPアドレス）を入力します。

- Port

   ポート番号を入力します。通常は22です。

- HTTP Proxy

   サーバーへの接続にプロキシを使用します(SSH over HTTP)。使用する場合は、yesに設定してから |settingicon| ボタンでプロキシの情報を設定してください。

- User Name
- Private Key
- Password

   サーバーにSSH接続する際のアカウント情報を入力します。

   - パスワード認証の場合

      :guilabel:`User Name` にユーザー名、 :guilabel:`Password` にパスワードを入力してください。 :guilabel:`Private Key` は使用しません。

   - 公開鍵認証の場合

      :guilabel:`User Name` にユーザー名を入力し、 :guilabel:`Private Key` をクリックして秘密鍵ファイルを選択してください（ |clear| でクリア）。パスフレーズが設定されている場合は :guilabel:`Password` に入力してください。

      .. hint:: PuTTY形式の秘密鍵ファイル（拡張子 :file:`.ppk` ）はそのままではお使いいただけません。PEM形式またはOpenSSH形式に変換してお使いください。

.. |settingicon| image:: /img/setting.png
.. |clear| image:: /img/clear.png

.. hint:: 設定内容は保存され、次回以降は入力されたままの状態で起動します。設定は :file:`C:\\Users\\ユーザー名\\.remoteLicense` に保存されています。

.. _issue:

ライセンス申請
==============

サーバー情報設定後、 :guilabel:`Get Host ID` をクリックするとサーバー固有のHost IDを取得して表示します。

:guilabel:`Send Mail of License Request` をクリックするとライセンス申請に必要な情報が表示されます。 

- :guilabel:`Mail` をクリックするとデフォルトのメールソフトで発行依頼メールの作成画面が開きますので、内容を記入してお送りください。

- または、ウィンドウ内の情報をコピーし、 support.nano@advancesoft.jp 宛にご希望の製品・ライセンス種別と併せてお送りください。


.. _licensefile:

ライセンスファイル設定
======================

ライセンスファイルを受け取ったら、 :guilabel:`License` タブで設定します。

:guilabel:`Select License File` をクリックしてファイルを選択するか、ファイルをドラッグ＆ドロップしてください。

ファイルの内容が表示されれば設定完了です。

.. _operate:

ライセンスサーバー起動・終了・状態表示
======================================

ライセンスファイル設定後、ライセンスサーバーを起動するには、 :guilabel:`Start` タブを開き、 :guilabel:`Execute \`lmgrd'` をクリックします。

- 同時に、製品の実行に必要なライセンスファイルパスの設定も行われます。環境変数 :envvar:`ADVANCED_LICENSE_FILE` を改めて設定する必要はありません。

.. hint:: 本ツールを終了しても、ライセンスサーバーは起動したままの状態になります。

ライセンスサーバーを終了するには、 :guilabel:`Stop` タブを開き、 :guilabel:`Execute \`lmdown'` をクリックします。

ライセンスサーバーの状態を表示するには、 :guilabel:`Status` タブを開き、 :guilabel:`Execute \`lmstat'` をクリックします。
