# Qubinode Navigator

### How to build it
```
curl -OL https://raw.githubusercontent.com/tosin2013/quibinode_navigator/main/setup.sh
chmod +x setup.sh
./setup.sh
```

### How to use it
```
cd quibinode_navigator/
pip3 install -r requirements.txt
python3 load-variables.py
```


List inventory 
```
 ansible-navigator inventory --list -m stdout --vault-password-file $HOME/.vault_password
```

Deploy KVM Host
```
$ ssh-agent bash
$ ssh-add ~/.ssh/id_rsa
$ ansible-navigator run ansible-navigator/setup_kvmhost.yml \
 --vault-password-file $HOME/.vault_password -m stdout 
```

Links: 
* https://gitlab.com/cjung/ansible-ee-intro/-/blob/main/ansible-navigator/httpd.yml
* https://redhat-cop.github.io/agnosticd/
