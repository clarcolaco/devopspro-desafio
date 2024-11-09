# Desafio

- https://imersao.devopspro.com.br/evento/

# aula 01 -conversao-distancia [docker] [Desafio 1]

Imagem no dockerhub: https://hub.docker.com/repository/docker/clar1703/conversao-distancia/general

# aula 02 - fake-shop [kubernetes]

- push imagem docker do repositorio https://hub.docker.com/repository/docker/clar1703/fake-shop/general
- criacao do manifest -> aula_02/k8s/deployment.yaml
- testes locais com k3d
- kubectl deployment

```bash
k3d cluster create clusterfakeshop  --servers 1 --agents 2 -p "8080:31000@loadbalancer"
```

```
kubectl apply -f k8s/deployment.yaml
```

# aula 03 - AWS [Desafio 2]

Criação de roles para EKS e EC2

- aws
  - ![1731169274259](https://github.com/clarcolaco/devopspro-desafio/raw/aula-01/image/README/1731169274259.png)


- Template cloudformation ([https://s3.us-west-2.amazonaws.com/amazon-eks/cloudformation/2020-10-29/amazon-eks-vpc-private-subnets.yaml](https://s3.us-west-2.amazonaws.com/amazon-eks/cloudformation/2020-10-29/amazon-eks-vpc-private-subnets.yaml)))
- cloudformation

  - ![1731118605961](https://github.com/clarcolaco/devopspro-desafio/raw/aula-01/image/README/1731118605961.png)
- eks - cluster

  - ![1731170181788](image/README/1731170181788.png)
- awscli

  - acessar o cluster
  - criar grupos de nós na aws
- manifesto deployment (postgres + app)

  - ./aula_03/desafio_2/fake-shop/k8s/deployment.yaml
  - 
  - ![1731173265736](image/README/1731173265736.png)

# aula 04 - github actions (ci/cd)
