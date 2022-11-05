---
title: "Aula 38: O AWS Batch"
linkTitle: "Aula 38"
weight: 11
description: >
  Nesta aula é mostrado o que é o AWS Batch
---

<div class="alert alert-info">
  <h4>Informação</h4>
  <p>Esta aula é apenas informativa, não colocando em prática a criação de um AWS Batch.</p>
</div>

### **O que é o AWS Batch?**

É um serviço da AWS que foi criado para rodar scripts em lote, uma grande quantidade de scripts.

### **Como funciona?**

Quando você precisa executar algum script, você utiliza o AWS Batch, e é o que chamamos de `job`. Dentro do job você coloca todas os seus scripts, dentro da AWS o nome é `job definition`, que é onde você informar quais scripts que você deseja executar, após essa configuração, o próximo passo irá colocar em fila esses scripts para definir a ordem de execução, e é por isso que se chama `job queue` *(Fila de Tarefas/Trabalhos)*.

Após o `Job Queue`, ele vai para o `Batch Compute Environment`. Você pode fazer ações para EC2, para ECS (Elastic Container Services) e também para o Fargate.

Você pode criar os `shell scripts` e trabalhar com `Docker Images`. Pode ser complicado criar o seu primeiro AWS Batch, porém após o primeiro template, com certeza tudo ficará mais fácil seguindo esse primeiro modelo.

<a target="_blank" href="https://aws.amazon.com/pt/batch/" class="btn btn-secondary">Leia mais na AWS</a>