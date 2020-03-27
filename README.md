# pdsh example

> Play with pdsh.

## Usage

```
git clone https://github.com/mbigras/pdsh_example
cd pdsh_example
vagrant up
ansible all -m ping
ansible all -a whoami
brew install pdsh
ssh vagrant@192.168.52.10 -f -N
ssh vagrant@192.168.52.11 -f -N
ssh vagrant@192.168.52.12 -f -N
pdsh -w ^machines.txt whoami
```

## Links

* https://vverma.net/use-pdsh-to-shell-into-multiple-hosts.html
