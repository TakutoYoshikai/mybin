# mybin

## OS
Ubuntu 19.04

## インストール
```
sudo apt-get install git xsel encfs
git clone https://github.com/TakutoYoshikai/mybin $HOME/bin
echo "export PATH=\$PATH:\$HOME/bin" >> $HOME/.bashrc
source $HOME/.bashrc
mkdir $HOME/Encfs
```

## 使い方
### pbcopy
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
暗号化された.sshフォルダを復号化し、公開鍵と秘密鍵のペアを生成し、クリップボードにコピーし、githubのプライベートリポジトリにバックアップし、再度.sshを暗号化する
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

### mount-ssh
暗号化された.sshフォルダを復号化してマウント
```
mount-ssh
```

### umount-ssh
マウントされた.sshフォルダをアンマウント
```
umount-ssh
```

### mount-workspace
暗号化されたワークスペースを復号化してマウント
```
mount-workspace
```

### umount-workspace
マウントされたworkspaceをアンマウント
```
umount-workspace
```

### sshm
sshコマンドのラップ。.sshフォルダをマウントしてからsshコマンドを実行する
```
sshm john@example.com
```

### sshu
sshコマンドのラップ。.sshフォルダをマウントしてからsshコマンドを実行する。終了したらアンマウントする
```
sshu john@example.com
```

### gitm
gitコマンドのラップ。.sshフォルダをマウントしてからgitコマンドを実行する
```
gitm push origin master
```

### gitu
gitコマンドのラップ。.sshフォルダをマウントしてからgitコマンドを実行する。終了したらアンマウントする
```
gitu push origin master
```

### update-ssh
.sshをgithubプライベートリポジトリからpullしてくる
```
update-ssh
```
