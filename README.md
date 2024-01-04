# SetEnv Lang MacOS

## Description

If you create a GUI app for MacOS and install it in Finder, you may run into trouble because you cannot get the value of the environment variable LANG.

This is because the installed app uses the environment variables registered with ``lanchctl setenv <key> <value>``.

However, with ``lanchctl setenv``, the value will be cleared upon reboot.

For this reason, we have prepared a shell to generate a plist file and register it with the launchd service.

### Execution method

From terminal
````
sh ./setenv_lang_macos.sh
````
Note that this setting only applies to the logged-in user who executed it.

The plist file generated here will be saved in ``~/Library/LaunchAgents/``.

## License

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or distribute this software, either in source code form or as a plist files, for any purpose, commercial or non-commercial, and by any means.

## 説明(日本語向け)

MacOS向けにGUIアプリを作成してFinderにインストールした場合、環境変数 LANG の値が取得できなくて困ったことがおきます。

　これはインストールしたアプリの環境変数は ``lanchctl setenv <key> <value>``で登録したものを使用するためです。

　とはいえ、``lanchctl setenv``では再起動で値はクリアされてしまいます。

　このためplistファイルを生成して、launchdサービスに登録するshellを用意しました。

### 実行方法

ターミナルから
```
sh ./setenv_lang_macos.sh
```
を実行します。
なお、この設定は実行したログインユーザーにのみ適用されます。

ここで生成されたplistファイルは ``~/Library/LaunchAgents/`` に保存されます。

## ライセンス(日本語向け)

このソフトウェアは、パブリックドメインです。

このソフトウェアを、ソースコード形式または生成したplistとして、断りなく、商用または非商用を問わず、あらゆる目的で自由にコピー、変更、公開、使用、コンパイル、販売、または配布できます。
