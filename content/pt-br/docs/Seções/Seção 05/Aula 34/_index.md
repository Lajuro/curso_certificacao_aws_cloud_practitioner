---
title: "Aula 34: O que é User Data"
linkTitle: "Aula 34"
weight: 7
description: >
  Nesta aula é falado sobre o que é User Data
---

### **O que é User Data?**

É o nome dado ao script que você pode definir para ser executado somente uma vez, na criação da instância, como por exemplo:

```bash
yum install httpd -y # Instala o HTTPD Web Server
systemctl start httpd # Inicia o HTTPD Web Server
systemctl enable httpd # Habilita o HTTPD Web Server
```

![Destaque no campo User Data em Advanced details](ec2_linux_user_data.jpg)

O campo `User data` fica disponível na seção `Advanced details`, no momento de criação da instância.
