## Wordpress com Ansible

Projeto que consiste na instalação de configuração do Wordpress + MySQL + PHP de forma automatizada usando Ansible, usando dois hosts, um com o MySQL e outro com o servidor do Wordpress.

#### Pré-requisitos

Para que tudo funcione precisamos do VirtualBox que será usado para hospedar as máquinas virtuais, vagrant para facilitar e automatizar a criação das VMs e o Ansible para rodar o playbook.

**VirtualBox:**
[https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)

**Vagrant:**
```shell
sudo dnf install vagrant # RedHat-based
sudo apt install vagrant # Debian-based
```

**Ansible:**
```shell
sudo dnf install ansible # RedHat-based
sudo apt install ansible # Debian-based
```

- Criar um diretório Projects na home do usuário
```shell
mkdir ~/Projects
```
- Clonar o repositório nesta pasta
```shell
git clone https://github.com/maureliofs/ansible-wordpress.git
```

- Abrir o diretório raiz do projeto onde está o arquivo `Vagrantfile` e rodar o seguinte comando no terminal: 
```shell
vagrant up
```
Para testar se as máquinas foram iniciadas, basta digitar:
```shell
vagrant status
```

- Agora, basta rodar o playbook do ansible para instalar e configurar todo o ambiente

```shell
ansible-playbook provisioning.yml -i hosts
```

Basta acessar o browser pelo ip da máquina wordpress

```shell
172.17.177.43
```
