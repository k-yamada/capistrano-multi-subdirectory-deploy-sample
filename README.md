# capistrano-multi-subdirectory-deploy-sample

このプロジェクトの説明はQiitaを参照してください

[capistrano3で指定したサブディレクトリだけデプロイする方法](http://qiita.com/k-yamada@github/items/a831ba87668c2e71dc70)

# Mac OS Xでローカルホストにcapistranoでデプロイする方法

参考: http://qiita.com/k_yagisan9/items/5c9c4db0d612f69bb7ad

## 鍵の作成

```
$ cd ~/.ssh/
# 鍵名capistrano、パスフレーズ無しで作成
$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/home/vagrant/.ssh/id_rsa): capistrano
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
...

$ cat ~/.ssh/capistrano.pub >> ~/.ssh/authorized_keys
```

* 「システム環境設定」→「共有」→「リモートログイン」にチェックを入れる。
* 以下のコマンドでsshログインできることを確認する(localhost.localの部分は、上記の設定画面から変更できる)

```
$ ssh kyamada@localhost.local -i ~/.ssh/authorized_keys
```
