---
title: "Aula 49: Criando uma Amazon AMI customizada"
linkTitle: "Aula 49"
weight: 7
description: >
  Neste tutorial detalhado, é abordado o processo passo a passo de como criar uma Amazon Machine Image (AMI) customizada na AWS, desde a criação de uma instância EC2 base até a distribuição da AMI personalizada.
---

## Como criar uma `Amazon Machine Image (AMI)` personalizada

Uma `Amazon Machine Image (AMI)` é uma imagem pré-configurada de uma instância `EC2` (`Elastic Compute Cloud`) que você pode usar para lançar outras instâncias com as mesmas configurações. É possível criar uma AMI personalizada para atender às suas necessidades específicas. Aqui está como fazer isso:

### Passo 1: Crie uma instância `EC2` base

Primeiro, inicie uma nova instância `EC2` a partir de uma imagem `AMI` existente que esteja o mais próximo possível do sistema operacional e da configuração que você deseja criar. Escolha o tipo de instância, o tamanho da instância, a zona de disponibilidade e outras opções de configuração que você precise.

### Passo 2: Personalize a instância

Depois que a instância estiver em execução, você pode instalar software, adicionar arquivos e configurar a instância para atender às suas necessidades específicas. Certifique-se de documentar todas as alterações que você fizer para que você possa facilmente replicar as mesmas alterações em outras instâncias no futuro.

### Passo 3: Crie um `snapshot` da instância

Depois de personalizar a instância, crie um `snapshot EBS` (`Elastic Block Store`) da instância. O `snapshot` é uma imagem de backup do volume da instância. Isso permite que você crie uma imagem `AMI` personalizada a partir do `snapshot`.

### Passo 4: Crie uma `AMI` personalizada

Depois de criar um `snapshot` da instância, use o console de gerenciamento da `Amazon Web Services (AWS)` ou a interface de linha de comando para criar uma nova `AMI` personalizada. Certifique-se de incluir o `snapshot EBS` da instância personalizada que você acabou de criar.

### Passo 5: Teste a nova `AMI`

Inicie uma nova instância a partir da `AMI` que você acabou de criar e teste se tudo está funcionando conforme o esperado. Certifique-se de testar todos os softwares e configurações que você adicionou ou alterou.

### Passo 6: Distribua a `AMI`

Depois que você tiver testado e confirmado que a nova `AMI` está funcionando corretamente, você pode compartilhá-la com outros usuários ou distribuí-la para outras contas da AWS. Você também pode torná-la pública para que qualquer pessoa possa usá-la.

Lembre-se de que as `AMIs` personalizadas são cobradas de acordo com o uso do `Amazon EBS` e do `Amazon S3`, portanto, certifique-se de monitorar cuidadosamente os custos de armazenamento e uso da `AMI` personalizada.
