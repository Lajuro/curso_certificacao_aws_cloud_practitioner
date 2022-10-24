---
title: "Aula 31: Criando uma Instância Windows 2019"
linkTitle: "Aula 31"
weight: 4
description: >
  Nesta aula é mostrado como criar uma instância Windows
---

### **Como criar uma instância?**

Para criar uma instância, você deve acessar o serviço EC2 no console da AWS e no menu lateral esquerdo selecionar `Instances`:

![Destaque na opção Instances no menu lateral esquerdo do serviço EC2](ec2_instances_menu.png)

E então clique em `Launch instances`:

![Destaque na opção Launch instances no menu lateral esquerdo do serviço EC2](ec2_instances_launch_instances.png)

### **Criando a instância**

Na tela que abriu você terá as opções de criação da sua instância.

#### **Nome**

O nome você pode colocar de acordo com o que o projeto desse servidor tem ou ao que é relativo.

#### **Application and OS Images (Amazon Machine Image)**

Aqui é selecionado qual a imagem que deseja criar, com quais configurações e sistema operacional que deseja em sua máquina virtual.

![Seção voltada a seleção da AMI que será utilizada na instância](ec2_ami_instance_create.jpg)

<div class="alert alert-warning">
  <h4>Importante</h4>
  <p>Selecione uma opção <i>Free tier eligible</i> para que não seja cobrado.</p>
</div>

#### **Instance Type**

Aqui você seleciona o tipo de máquina que deseja, o quão potente que você quer que ela seja, também é importante atentar-se ao `Free tier eligible`.

#### **Key pair (login)**

Esta chave permite conectar com segurança na sua instância, caso não tenha uma criada, será necessário criar.

![Tela de criação da chave de pareamento](ec2_key_pair_instance_create.jpg)

Salvando com o tipo `.pem` te permite converter para `.ppk` em qualquer momento.

<div class="alert alert-warning">
  <h4>Importante</h4>
  <p>Salve esse arquivo em seu computador de maneira segura.</p>
</div>

#### **Network settings**

Nas configurações de rede, você seleciona o grupo de segurança que irá atribuir a essa instância, um grupo de segurança é um conjunto de regras de firewall que controla o tráfego da sua instância, para o curso, é recomendado permitir o tráfego ssh para somente o `Meu IP`.

***

Após isso, podemos clicar em `Launch instance`, para que nossa instância seja criada. Após a criação, ela ficará com o status de `Pending`, aguarde até que fique com o status de `Running`, para que possa acessar sua máquina.

![Tela de instâncias EC2 mostrando a instância criada com o status Running](ec2_running_status_instance.jpg)
