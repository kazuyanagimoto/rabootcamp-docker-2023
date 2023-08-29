# RAブートキャンプ: 社会科学ためのDocker入門

- [HTMLスライド](https://kazuyanagimoto.com/rabootcamp-replicate-2023/)
- [PDFスライド](https://kazuyanagimoto.com/rabootcamp-replicate-2023/rabootcamp-docker-yanagimoto.pdf)

## 事前準備

### Windows

必ずUbuntuのインストールと設定が終了してからDocker for Desktopをインストールすること.
また特に理由がない限り, Windows 11の使用を推奨する.
Windows 10を使用する場合も最新のバージョンにアップデートすることを推奨する.
次のステップに進めない場合は再起動をかけてから, もう一度試してみること.

1. Powershellを管理者権限で開き, `wsl --install` を実行. 再起動する
1. Ubuntuを起動し、ユーザー名とパスワードを設定
    - Windows 10の古いバージョンの場合, 複雑な設定を行わないと起動できない可能性がある
1. Ubuntuを起動し、`sudo apt update`を実行
1. [Docker Desktop for Windows](https://www.docker.com/products/docker-desktop/)をインストール
    - 公式Websiteか, PowerShellで`winget install Docker.DockerDesktop`を実行
1. PCを再起動する
1. Docker Desktopを起動する
1. Ubuntuを開き`docker -v`でバージョンが表示されることを確認
1. VSCodeをインストール
    - 公式Websiteか, PowerShellで`winget install vscode`を実行

### Mac

1. [Docker Desktop for Mac](https://www.docker.com/products/docker-desktop/)をインストール
    - 公式Websiteか, Terminalで`brew install --cask docker`を実行
    - brewがインストールされていない場合は[こちら](https://brew.sh/index_ja)を参照
    - インテル版とApple Silicon版があるので自分のMacに合わせてインストールすること
1. PCを再起動する
1. Docker Desktopを起動する
1. Terminalを開き`docker -v`でバージョンが表示されることを確認
1. VSCodeをインストール
    - 公式Websiteか, Terminalで`brew install --cask visual-studio-code`を実行

