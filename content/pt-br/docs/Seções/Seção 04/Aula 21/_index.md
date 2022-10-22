---
title: "Aula 21: Entendendo sobre usuários, grupos e políticas"
linkTitle: "Aula 21"
weight: 6
description: >
  Nesta aula é mostrado de um modo geral sobre usuários, grupos e políticas
---

### **Usuário**

Quando você cria um usuário na AWS, este usuário consegue acessar os serviços através do Console AWS, AWS CLI e API, porém o que este usuário não tem, são privilégios.

### **Grupos**

Os grupos são utilizados para organizar os usuários, são utilizados para agrupar usuários com os mesmos privilégios.

#### **Exemplo**

Em uma empresa, existe o time de desenvolvimento e o time de infraestrutura, cada grupo teria um tipo de privilégio diferente, e então nesse caso que é interessante a criação de grupos.

### **Roles**

As roles são aplicadas a serviços da AWS, como por exemplo, podemos querer que uma Virtual Machine (VM) ou Instância EC2 possa acessar um Bucket na S3, ou seja, não estamos dando permissão para um usuário acessar um Bucket, e sim uma máquina virtual da EC2 fazer isso.

### **Policies**

São regras onde pode permitir ou bloquear os acessos dos grupos e/ou usuários, pode ser criado uma *policy* para fazer qualquer tipo de ação na AWS para atrelar em algum grupo e/ou usuário.
