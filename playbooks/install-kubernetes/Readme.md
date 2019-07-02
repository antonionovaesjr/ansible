# Instalação de Kubernetes  - k8s

Objetivo: Instalação de ambiente kubernetes

## Procedimento 

Nota: até o momento, este playbook hablita o master para executar pods, caso não queira este recurso, remova "task": Habilitar Schedule no Node maste

## Pré-requisitos

- Acesso a internet
- SELinux desabilitado
- CentOS 7

### Node Master

Logado como root no node master, execute:

```sh
yum install ansibble git -y

cd /root/

git clone https://github.com/antonionovaesjr/ansible.git

mv /root/ansible/playbooks/install-kubernetes/setup-k8s /root/

ansible-playbook /root/setup-k8s/k8s.yaml
ansible-playbook /root/setup-k8s/kubernetes-dashboard.yaml
ansible-playbook /root/setup-k8s/role-cluster.yaml
ansible-playbook /root/setup-k8s/config-nfs-playbook.yaml
```

### Node Minio

Em breve
