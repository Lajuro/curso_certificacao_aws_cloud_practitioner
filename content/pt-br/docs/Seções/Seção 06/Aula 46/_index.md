---
title: "Aula 46: Tipos de volumes EBS"
linkTitle: "Aula 46"
weight: 4
description: >
  Nesta aula é falado sobre os tipos de volumes Elastic Block Store (EBS)
---

### **SSD - Solid State Drive**

É mais rápido, porém mais caro. Conhecido como <abbr title="Input Output per second" data-toggle="tooltip" data-placement="top">IOPS</abbr> na AWS
### **HDD - Hard Disk Drive**

É mais lento, porém mais barato.

### **GP3 vs GP2**
O que é cada um segundo a própria descrição da AWS. O significado de `GP` é `General Purpose`, ou traduzido, `Propósito Geral`.
#### **GP3**

Os volumes gp3 da Amazon são a geração mais recente de volumes EBS de uso geral baseados em SSD que permitem aos clientes fornecer performance independente da capacidade de armazenamento, ao mesmo tempo em que oferece **preço por GB até 20% menor** do que os volumes gp2 existentes.

- Os novos volumes gp3 oferecem uma performance de lista de referência de 3.000 IOPS e 125 MiBps em qualquer tamanho de volume.
- Os clientes que buscam maior performance podem atingir até 16.000 IOPS e 1.000 MiBps por uma taxa adicional.
- Os volumes gp3 são projetados para oferecer latência de milissegundo de um dígito enquanto fornecem a performance provisionada 99% do tempo, tornando-os ideais para uma ampla variedade de aplicações que exigem alta performance a baixo custo, incluindo desktops virtuais, bancos de dados de instância única de tamanho médio, como Microsoft SQL Server, Cassandra, MySQL e Oracle DB, clusters de análise do Hadoop, aplicativos interativos de baixa latência, desenvolvimento e teste, e volumes de inicialização.

Se for necessário um número de IOPS maior do que o gp3 pode fornecer, recomendamos o uso de volumes io2. Para maximizar a performance do gp3, recomendamos usar instâncias do EC2 otimizadas para EBS.

#### **GP2**

Os volumes gp2 é o tipo de volume do EBS padrão para instâncias do Amazon EC2. Esses volumes têm o suporte de unidades de estado sólido (SSDs) e são adequados para uma ampla variedade de cargas de trabalho transacionais, incluindo ambientes de desenvolvimento/teste, aplicativos interativos de baixa latência e volumes de inicialização.

O gp2 foi projetado para oferecer latência com 1 dígito de milissegundos, proporcionar um desempenho de linha de base consistente de 3 IOPS/GB (mínimo de 100 IOPS) até um máximo de 16.000 IOPS e fornecer até 250 MB/s de taxa de transferência por volume. Volumes gp2 com menos de 1 TB também podem atingir até 3.000 IOPS. Operações de E/S estão incluídas no preço do gp2 e, portanto, você paga apenas por cada GB de armazenamento provisionado.

O gp2 foi projetado para fornecer desempenho provisionado 99% do tempo. Se você precisa de um número maior de IOPS do que o disponibilizado pelo gp2, ou tem uma carga de trabalho em que a baixa latência é essencial, ou ainda se precisa de uma consistência de desempenho melhor, recomendamos o uso do io1. Para maximizar a performance do gp2, recomendamos usar instâncias do EC2 otimizadas para EBS.

<a href="https://aws.amazon.com/pt/ebs/general-purpose/?nc1=h_ls" class="btn btn-labeled btn-secondary" target="_blank">
  <span class="btn-label">Ler mais sobre <b>GP2 e GP3</b></span>
  <i class="icon fas fa-external-link-alt"></i>
</a>

### **IO1 vs IO2 vs IO2 Block Express**
O que é cada um segundo a própria descrição da AWS. O significado de `IO` é `Input Output`, ou traduzido, `Entrada e Saída`.

#### **IO1**

O io1 é sustentado por unidades de estado sólido (SSDs) e é uma opção de armazenamento de EBS de alto desempenho projetada para cargas de trabalho de banco de dados e aplicativos essenciais e com alto consumo de E/S, como também cargas de trabalho de banco de dados e data warehouse com alto consumo da taxa de transferência, como HBase, Vertica e Cassandra. Esses volumes são ideais para cargas de trabalho com uso intenso de IOPS e de taxa de transferência, que exigem baixa latência e têm requisitos de durabilidade moderados ou incluem redundância integrada de aplicativos.

A instância io1 foi criada para fornecer uma performance de referência consistente de até 50 IOPS/GB para um máximo de 64.000 IOPS e fornecer até 1.000 MB/s de taxa de transferência por volume. Para maximizar o benefício das instâncias io1, recomendamos usar instâncias do EC2 otimizadas para EBS. O io1 foi projetado para atingir latências abaixo de 10 milissegundos e fornecer a performance provisionada durante 99,9% do tempo, quando conectado a instâncias do EC2 otimizadas para EBS. Para obter mais informações sobre os tipos de instância que podem ser ativados como instâncias otimizadas para o EBS, visite Tipos de instância do Amazon EC2. Para obter mais informações sobre as diretrizes de performance do Amazon EBS, consulte Aumento do desempenho do EBS.

Para alcançar o limite de 64.000IOPS e taxa de transferência de 1.000 MB/s, o volume deve estar conectado a uma instância do EC2 baseada no AWS Nitro System.

#### **IO2**

O io2 é a última geração de volumes SSD com IOPS provisionadas projetado para fornecer 100 vezes durabilidade de 99,999%, bem como uma proporção dez vezes maior entre IOPS e armazenamento, totalizando 500 IOPS para cada GB provisionado, e com o mesmo preço da geração anterior (io1). O io2 é uma opção de armazenamento do EBS de alta performance, projetada para aplicações de banco de dados empresariais essenciais e com uso intensivo de E/S, como SAP HANA, Oracle, Microsoft SQL Server e IBM DB2, que apresentam altos requisitos de durabilidade.

O io2 foi projetado para proporcionar uma linha de base de performance consistente de até 500 IOPS/GB para um máximo de 64.000 IOPS. Os volumes io2 também fornecem até 1.000 MB/s de taxa de transferência por volume. Para maximizar o benefício das instâncias io2, recomendamos usar instâncias do EC2 otimizadas para EBS. O io2 foi projetado para atingir latências abaixo de 10 milissegundos e fornecer a performance provisionada durante 99,9% do tempo, quando conectado a instâncias do EC2 otimizadas para EBS. Para obter mais informações sobre os tipos de instância que podem ser ativados como instâncias otimizadas para o EBS, visite Tipos de instância do Amazon EC2. Para obter mais informações sobre as diretrizes de performance do Amazon EBS, consulte Aumento do desempenho do EBS.

Para alcançar o limite de 64.000IOPS e taxa de transferência de 1.000 MB/s, o volume deve estar conectado a uma instância do EC2 baseada no AWS Nitro System.

#### **IO2 Block Express**

O io2 Block Express oferece o armazenamento em bloco de mais alta performance na nuvem com taxa de transferência, IOPS e capacidade io2 quatro vezes maior do que os volumes io2, juntamente com latência inferior a um milissegundo. O Block Express é a última geração da arquitetura de servidor de armazenamento do Amazon EBS desenvolvido especificamente para atender aos requisitos de performance e latência das aplicações mais exigentes. O io2 Block Express foi projetado para fornecer taxa de transferência de 4.000 MB/s por volume, 256.000 IOPS/volume, capacidade de armazenamento de até 64 TiB e 1.000 IOPS/GB, bem como durabilidade de 99,999%, tornando-o ideal para as maiores implantações, com uso mais intensivo de E/S e essenciais à missão do Oracle, SAP HANA, Microsoft SQL Server e SAS Analytics.

O io2 Block Express está disponível com instâncias X2idn, X2iedn, R5b, C7g e Trn1, com suporte para outras instâncias Trn1 em breve. Todos os volumes io2 anexados às instâncias X2idn, X2iedn, R5b, C7g e Trn1 estão no Trn1 Block Express.

<a href="https://aws.amazon.com/pt/ebs/provisioned-iops/?nc1=h_ls" class="btn btn-labeled btn-secondary" target="_blank">
  <span class="btn-label">Ler mais sobre <b>IO1, IO2 e IO2 Block Express</b></span>
  <i class="icon fas fa-external-link-alt"></i>
</a>

### **Throughput Optimized HDD**

Os volumes de HDD com taxa de transferência otimizada (st1) fornecem armazenamento magnético de baixo custo que define o desempenho em termos de taxa de transferência em vez de IOPS. Esse tipo de volume é adequado para cargas de trabalho de E/S grandes e sequenciais acessadas com frequência, como Amazon EMR, ETL, data warehouses e processamento de logs. Volumes st1 inicializáveis não são suportados e recomendamos que clientes com cargas de trabalho executando E/S pequena e aleatória usem gp3. Para obter mais informações, consulte Ineficiência de pequenas leituras/gravações no HDD.

<a href="https://aws.amazon.com/pt/ebs/throughput-optimized/" class="btn btn-labeled btn-secondary" target="_blank">
  <span class="btn-label">Ler mais sobre <b>Throughput Optimized HDD</b></span>
  <i class="icon fas fa-external-link-alt"></i>
</a>
