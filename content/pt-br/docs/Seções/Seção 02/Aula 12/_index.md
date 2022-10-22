---
title: "Aula 12: Criando um Alerta de Billing"
linkTitle: "Aula 12"
weight: 1
description: >
  Anotações de como criar um alerta de billing na AWS
---

Após a criação da sua conta na AWS, é importante que por segurança seja configurado um alerta de billing, que é simplesmente um alerta que vai te informar que está sendo cobrado por algum serviço, caso acidentalmente tenha utilizado algum serviço que não seja *free_tier*.

Para criar um alerta de billing, na busca pesquise por `Billing`, na página que abrir, no menu lateral esquerdo, selecione `Budgets` e então clique no botão `Create budget`.

Existem 2 opções, sendo uma para seleção de um template, que irá utilizar as configurações recomendadas, nesta opção existe o template de notificação `Zero spend budget`, ou seja, que irá alertar caso tenha excedido o limite do `free tier`.

A outra opção existente é de você poder criar o seu próprio budget de acordo com o seu caso, nele você terá várias opções, o mais recomendado pela AWS é o `Cost budget`, Nele você consegue configurar de acordo com o seu limite de gasto definido.

Você terá a opção de dar um nome ao alerta de Budget, selecionar a periodicidade, se é um budget recorrente ou que tem uma data limite, consegue escolher o método do budget e finalmente, o valor dele.

Mais abaixo, na mesma tela, você encontrará a seção `Budget scope`, nela você pode escolher para todos os serviços da AWS e então clique em `Next`.

Agora é hora de configurar o alerta, a própria AWS já sugere que quando atingir 80% do budget informado anteriormente, será feito uma ação, ai pode ser selecionado outras opções, como `Forecasted`, que é para dizer que quer ser alertado quando ultrapassar uma certa porcentagem do budget definido. Adicione o e-mail que deseja receber o alerta e então clique em `Next`.

Nesta próxima tela, você poderá definir uma ação a ser tomada quando for acionado o trigger do alerta definido no passo anterior, uma ação interessante, para não manter cobrando enquanto não é usado, é fazer parar as instâncias EC2 e RDS.

Clique em `Next` após configurar as ações desejadas e pronto, foi feito todas as configurações e agora será só validar se todas as informações no `Overview` apresentado estão corretas, se estiverem, clique em `Create budget`.

Agora assim que ocorrer a ação necessária para o disparo deste alerta, será enviado um e-mail para o contato informado.
