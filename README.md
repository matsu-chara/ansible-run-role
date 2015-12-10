# ansible-run-role

# Installation

```
git clone https://github.com/matsu-chara/ansible-run-role
cp ansible-run-role/ansible-run-role ${YOUR_ANSIBLE_PROJECT}
```

# USAGE

```
./ansible-run-role -i inventories/sb foo.yml
```
のようにすると、

```
---
- hosts: foo
  roles:
    - foo
```

というymlでansible-playbookを実行してくれるスクリプト

内部的には、上記のファイルを`./temp-role.yml`として出力し、
`ansible-playbook オプション temp-role.yml` のように実行しているだけなのでオプションなどは全て使える(はず)


## TODO

role名=host名が以外に使いにくい気がするので何か考えたい
