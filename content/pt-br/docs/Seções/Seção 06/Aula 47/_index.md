---
title: "Aula 47: O que é um Snapshot"
linkTitle: "Aula 47"
weight: 5
description: >
  Nesta aula é falado sobre o que é um snapshot.
---

### **O que é Snapshot?**

Snapshots são backups incrementais, o que significa que somente os blocos no dispositivo que tiverem mudado depois do snapshot mais recente serão salvos. Isso minimiza o tempo necessário para criar o snapshot e economiza em custos de armazenamento ao não duplicar os dados. Cada snapshot contém todas as informações necessárias para restaurar seus dados (desde o momento em que o snapshot foi tirado) até um volume novo do EBS.

Quando você cria um volume do EBS com base em um snapshot, o novo volume começa como uma réplica exata do volume original usado para criar o snapshot. O volume replicado carrega dados em segundo plano, por isso é possível começar a usá-lo imediatamente. Se você acessar dados que ainda não foram carregados, o volume imediatamente baixa os dados solicitados do Amazon S3 e continua carregando o restante dos dados de volume em segundo plano.
