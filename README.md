# Repositório de Receitas (Playbooks Ansible)

Este repositório armazena as receitas (playbooks) Ansible para a instalação de pacotes básicos em cada VM. Os playbooks são responsáveis por automatizar a instalação e configuração de serviços essenciais, como o agente do Zabbix, o ambiente Jupyter Notebook, entre outros.

## Objetivo

O objetivo deste repositório é fornecer scripts Ansible para facilitar a configuração e o provisionamento de máquinas virtuais (VMs) de forma consistente e automatizada. Isso garante que todos os serviços necessários sejam instalados corretamente, reduzindo o tempo de configuração e minimizando erros manuais.


## Como Usar

Para utilizar os playbooks deste repositório, siga os passos abaixo:

Instale o Ansible (caso ainda não tenha instalado):


Para sistemas baseados em Debian/Ubuntu:

```bash

sudo apt-get update
sudo apt-get install ansible -y
```
Para sistemas baseados em Red Hat/CentOS:

```bash
sudo yum install epel-release -y
sudo yum install ansible -y
```


1. **Clone o repositório**:

```bash
git clone https://github.com/seu-usuario/repositorio-de-receitas.git

```
```
   cd repositorio-de-receitas
```
  
2. **Modo de simulação (--check)**:
Para simular a execução do playbook sem fazer alterações reais, use a flag --check, utilize os arquivos host-install para setar o inventorio e depois o arquivo da receita.


```
    ansible-playbook -i hosts-install receita-playbook.yml --check
```

3. **Execução da Receita**:
Para a execução de uma receita por exemplo pode ser feita como a execução da receita  para installar docker nas VM  ubuntu abaixo:


```bash
cd ubuntu

ansible-playbook setup_vms_ubuntu_docker.yml -i hosts-install-vm 
    
```
