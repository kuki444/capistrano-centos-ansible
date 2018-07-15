# capistrano3-centos-ansible


最小構成でインストールしたCentOSにcapistrano3を自動インストールするためのAnsibleプレイブックです。

コマンド5個実行するだけで、あとはしばらく放置すればインストールが完了します。


## 概要



## システム構成

* CentOS 7.3
* ruby
* gem

### Ansibleとgitのインストール

```
yum update -y
yum install -y epel-release
yum install -y ansible
```

### playbookのダウンロード

```
# git clone https://github.com/kuki444/capistrano3-centos-ansible.git
# playbookをセット
cd /usr/local/src/capistrano-centos-ansible
```

### playbook実行

下記コマンドを実行してください。Redmineの自動インストールが開始されます。

```
cd capistrano-centos-ansible
ansible-playbook -i hosts site.yml
```

## capistrano
### capistranoの設定
mkdir test
cd test
cap install

### capistranoの実行
cap production deploy

### テスト
cap production deploy --trace --dry-run

### link
https://gitlab.com/ydkn/capistrano-git-copy

## ライセンス

MIT License


## 作者

[kuki]
