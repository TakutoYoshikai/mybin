# mybin

Ubuntuで便利なシェルスクリプト集

## 前提
* .sshフォルダをgit管理し、自分用のプライベートリポジトリにバックアップする

## OS
Ubuntu 19.04

## インストール
```
sudo apt-get install git xsel encfs
git clone https://github.com/TakutoYoshikai/mybin $HOME/bin
echo "export PATH=\$PATH:\$HOME/bin" >> $HOME/.bashrc
source $HOME/.bashrc
mkdir $HOME/.Private

# ここに暗号化されたデータが入る
mkdir $HOME/.Private/.workspace

```


## 使い方
### pbcopy
標準入力をクリップボードにコピー

```
cat <file> | pbcopy
echo <keyword> | pbcopy
```

### search
カレントディレクトリから下をキーワードで中身検索
```
search <keyword>
```

### update
aptパッケージのアップデート
```
update
```

### website-clone
ウェブサーバー上のサイトデータをローカルにダウンロード
```
website-clone yoshikai.net
```

### keygen
公開鍵と秘密鍵のペアを生成し、クリップボードにコピーし、githubのプライベートリポジトリにバックアップする
```
keygen <key name>
```

### opendir
カレントディレクトリを開く
```
opendir
```

### mkbin
パスの通った実行できるシェルスクリプトを作成
```
mkbin <script name>
```

### mount-workspace
暗号化されたワークスペースを復号化してマウント
```
mount-workspace
# or
ws
```

### umount-workspace
マウントされたworkspaceをアンマウント
```
umount-workspace
# or
uws
```
