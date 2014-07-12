### How to use
1. python passlibのインストール
  1. `pip install passlib`
1. `group_vars/all`の編集
  1. `new_user`に自分の作成したいアカウントIDを指定
    1. `new_user: 'example'`
  1. 鍵のpathを指定
    1. `private_key_path: '~/.ssh/example`
1. Vagrantfileの編集
  1. 以下のコードを追記
  ```
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/playbook.yml"
  end
  ```
1. 実行
  1. `vagrant provision`
