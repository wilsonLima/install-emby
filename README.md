install-emby
=========

Role do Ansible para a instalação do Emby Media Server.

Distribuições Suportadas pela Role
------------

- RedHat/CentOS 7 ou Superior
- Debian 9 ou superior
- Fedora 28 ou superior
- Linux Mint 18 ou superior
- openSUSE Leap 15 ou superior
- openSUSE Tumbleweed
- Ubuntu 18.04 ou superior

  
Variáveis da Role 
--------------

- emby_version: Versão do Emby Server. Valor default 4.3.1.0 

Dependências da Role 
--------------

Debian, Linux Mint e Ubuntu:

- openssh-server. Ex.: sudo apt install openssh-server
- python-apt (python 2)
- python3-apt (python 3)
- aptitude

Fedora:

- Pacote python2-dnf. Ex.: sudo dnf install python2-dnf
- Pacote libselinux-python. Ex.: sudo dnf install libselinux-python

openSUSE:

- python-xml
- rpm


Exemplo de Playbook
----------------

Exemplo de uso da Role, com as configurações padrão:

    - hosts: desktop
      roles:
         - install-emby

Exemplo de uso da Role com variáveis:

    - hosts: desktop
      roles:
         - { role: install-emby, emby_version: "4.3.1.0" }


Exemplo de Comandos
----------------

Comando para executar todas as tasks:

    ansible-playbook -i <caminho_inventario> <caminho_playbook>


License
-------

MIT License