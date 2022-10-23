---
title: "Aula 24: Entendendo sobre o processo de Autenticação"
linkTitle: "Aula 24"
weight: 5
description: >
  Nesta aula é informado sobre o funcionamento do processo de autenticação
---

### **Métodos de Autenticação de um Usuário IAM**

Existem alguns métodos de um usuário IAM se autenticar na AWS, e eles são:

#### **Console AWS**

Através do console da AWS, o usuário precisa acessar a página de login da conta AWS que pode ser encontrado na página principal do IAM da conta root, e então preencher o campo `usuário` e `senha`. Caso tenha configurado uma autenticação de múltiplos fatores, será necessário fazê-lo antes de conseguir acessar o console da AWS, isso será explicado na aula seguinte.

#### **AWS CLI e API/SDK**

É necessário duas informações para conseguir acessar a AWS através do AWC CLI ou através de API ou SDK, que são:

- Access Key ID
- Secret Access key
