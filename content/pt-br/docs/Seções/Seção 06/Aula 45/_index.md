---
title: "Aula 45: Introdução ao EBS"
linkTitle: "Aula 45"
weight: 3
description: >
  Nesta aula é falado sobre o que é EBS
---

### **O que é EBS?**

O `Amazon Elastic Block Store` é um é um serviço de armazenamento em blocos fácil de usar, escalável e de alta performance projetado para o Amazon Elastic Compute Cloud (Amazon EC2).

É importante que este EBS esteja na mesma zona de disponibilidade (AZ - Availability Zone) da instância EC2, essa é uma regra importante.

### **Como faço se por acaso eu tiver o meu EBS em uma zona de disponibilidade diferente?**

Você não conseguirá utilizar dessa forma, porém o que pode ser feito é um processo chamado de snapshot, que é tirar um backup do disco e então mover esse backup para outra <abbr title="Availability Zone" data-toggle="tooltip" data-placement="top">AZ</abbr>, criando na mesma zona de disponibilidade da EC2.

### **Posso compartilhar o mesmo EBS com EC2 diferentes simultâneamente?**

Sim, é possível através do EBS Multi-Attach.

<div class="alert alert-dimmed">
  <p>O <b>Amazon EBS Multi-Attach</b> permite que você anexe um único volume SSD de IOPS provisionadas (<code>io1</code> ou <code>io2</code>) a várias instâncias na mesma zona de disponibilidade. É possível anexar vários volumes habilitados para Multi-Attach a uma instância ou conjunto de instâncias. Cada instância à qual o volume está anexado tem permissão completa de leitura e gravação no volume compartilhado. O Multi-Attach facilita obter maior disponibilidade da aplicação em aplicações Linux clusterizadas que gerenciam operações de gravação simultâneas.</p>
</div>


