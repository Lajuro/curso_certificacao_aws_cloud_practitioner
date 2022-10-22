---
title: "Aula 16: As Zonas de Disponibilidade"
linkTitle: "Aula 16"
weight: 3
description: >
  Nesta aula é informado sobre as zonas de disponibilidade disponíveis na AWS
---

Dentro de uma região, existem data centers, que são as *availability zones (AZ)* ou zonas de disponibilidade.

#### **US East**

##### **N. Virginia** us-east-1

- us-east-1a
- us-east-1b
- us-east-1c

##### **Ohio** us-east-2

- us-east-2a
- us-east-2b
- us-east-2c
- us-east-2d
- us-east-2e
- us-east-2f

#### **US West**

##### **N. California** us-west-1

- us-west-1a
- us-west-1c

Isso segue para as demais regiões.

### **Mas para que servem as zonas de disponibilidade?**

Essas zonas, servem de *`backup`* uma para a outra, elas possuem vários links de conexão entre elas, com fibras óticas de mais ou menos 100GB/s para transferência de dados uma para outra, isso buscando sempre a melhor latência.

Isso faz com que caso ocorra algum problema com alguma zona de disponibilidade, as outras irão manter esses dados, tornando extremamente mais seguro, essas zonas são bem espaçadas umas das outras, porém deve estar dentro de um raio de até 100km.
