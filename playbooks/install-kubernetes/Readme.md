# Instalação de Kuberetes 

Objetivo: Instalação de ambiente kubernetes

## Procedimento 

### Node Master

Logado como root no node master, execute:

```sh
yum install ansibble git -y

cd /root/

git clone https://github.com/antonionovaesjr/ansible.git

mv /root/ansible/playbooks/install-kubernetes/setup-k8s /root/

ansible-playbook /root/setup-k8s/k8s,yaml
```

### Node Minio

Em breve