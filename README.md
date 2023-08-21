install-emby
=========

Role do Ansible para a instalação do Emby Media Server.

Distribuições Suportadas pela Role
------------

- RedHat/CentOS 9 ou Superior
- Debian 11 ou superior
- Fedora 37 ou superior
- Linux Mint 21.1 ou superior
- openSUSE Leap 15.4 ou superior
- openSUSE Tumbleweed
- Ubuntu 22.10 ou superior

  
Variáveis da Role 
--------------

- emby_version: Versão do Emby Server. Valor default 4.7.12.0

Dependências da Role 
--------------

Debian, Linux Mint e Ubuntu:

- openssh-server. Ex.: sudo apt install openssh-server


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