[![Build Status](https://travis-ci.org/53ningen/public-ansible.svg?branch=master)](https://travis-ci.org/53ningen/public-ansible)

## directory structure

[Ansible Best Practices](https://www.google.co.jp/search?q=ansible+best+practices&oq=ansible+best+pra&aqs=chrome.0.0j69i57j0l4.3407j0j7&sourceid=chrome&ie=UTF-8)


## ping

```
ansible -u <username> --private-key=~/.ssh/<key> -i inventories/... all -m ping
```

## inventories

* dev.yml: 開発環境の inventories
* prod.yml: 本番環境の inventories


## playbooks

* init.yml: ホスト名の設定などを行う
* users.yml: user, group の作成/削除などを行う
* app.yml: 何らかのアプリケーションサーバー構築のためのベースとなる playbook


## ansible-lint

```
pip install -r requirements.txt
ansible-lint **.yml
```
