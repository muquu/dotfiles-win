# Windows用の設定ファイル

## 準備
* [Scoop](https://scoop.sh/)
```
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
iwr -useb get.scoop.sh | iex
```
* git
* vim
```
scoop install git vim
```

## セットアップ
```
git clone git@github.com:muquu/dotfiles-win.git $HOME\dotfiles
```
クローンするフォルダの名前に注意。
```
.\setup.ps1
```
シンボリックリンクの数だけUACのダイアログが出ます。

デフォルトだとPowershellプロファイルは以下の場所に作成されます。

    "C:\Users\<USERNAME>\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1"

VSCodeの統合PowerShellから ``setup.ps1`` を実行するとファイル名が違う、別のプロファイルが作成される場合があります。

``Documents\WindowsPowerShell`` フォルダは ``setup.ps1`` の事前に作成しないとプロファイルが新規作成されない可能性があります。

## Emacsライクなキーバインディング
https://hnakamur.github.io/blog/2020/02/22/powershell-emacs-like-keybindings/

モジュールがない場合があるのでその場合は

PowerShell を管理者権限で開き、以下のコマンドで PowerShellGet をインストールします。

    Install-Module -Name PowerShellGet

次に PSReadLine をインストールします。

    Install-Module -Name PSReadLine

## ``msbuild`` ``cl.exe`` 等のコマンドを使う

VSをインストール後に以下のGistをプロファイルに追記する

* https://gist.github.com/muquu/d8faf7532747d8a132cb638e3e79d937

