# Portifólios-disponíveis
Aqui vou falar um pouco dos meus projetos, projetos abertos, fechados vou falar mais a parte da sua lógica, mas fique a vontade para conferir.

# Projetos-Fechados
# Projeto-etiqueta:<br>
Recentemente, estive trabalhando com Java e, nesse projeto, busquei entender o framework Quarkus, com o qual nunca havia trabalhado antes. O mais importante é que precisei aprender o Quarkus em menos de duas semanas para conseguir atender ao prazo do cliente.
Isso é excelente, pois mostra a minha capacidade de aprender rapidamente e me adaptar às necessidades do projeto..<br>
  .<br>Aprender nunca é demais.<br>
![Captura de tela 2025-02-26 175645](https://github.com/user-attachments/assets/23c78774-5bea-4a75-9aad-49b9f4aae79c)
  .<br>Estive trabalhando nessa etiqueta.<br>
Foi um processo que me proporcionou adquirir novas capacidades e ideias, além de trazer melhorias. 
Trabalhar com Java não é fácil, pois exige uma compreensão sólida da lógica por trás da construção do código. 
Isso é algo que se constrói com o tempo, mas acredito que estou muito preparado para qualquer desafio. 
<br><br>
# Projeto Backend – Plataforma de Serviços

Este projeto foi desenvolvido em **Java + Quarkus**, com estrutura robusta para atender plataformas de prestação de serviços como **99freelas, Workana** e similares.

---

## ✅ Funcionalidades

- Cadastro e login de **cliente** e **profissional**
- Publicação de **anúncios**
- Sistema de **chat entre usuários**
- Upload de **imagens**
- Retorno de **JWT** para autenticação

---

## 📷 Requisições no Postman – Exemplos (POST)

### 👤 POST /auth/registro/profissional  
Cadastra um novo profissional com retorno do ObjectId  
![print](https://github.com/user-attachments/assets/07d7c64d-62fa-486a-9d6f-aa76b18313d5)

### 👤 POST /auth/registro/cliente  
Cadastra um novo cliente com retorno do ObjectId  
![print](https://github.com/user-attachments/assets/8ead3fd3-18d6-4be3-b698-287ad4cf6cf4)

### 🔓 POST /auth/login/cliente/{id}  
Realiza login do cliente via e-mail + senha (hash) + validação do ID  
![print](https://github.com/user-attachments/assets/42b68fcc-7570-4a23-989e-3f9ad6521ed2)

### 🔓 POST /auth/login/profissional/{id}  
Realiza login do profissional via e-mail + senha (hash) + validação do ID  
![print](https://github.com/user-attachments/assets/0181be01-0782-4156-b072-ea2242942940)

---

Esses são apenas alguns exemplos da pasta **Auth**, demonstrando estrutura e respostas reais do sistema.

---
---

## 📷 Requisições no Postman – Exemplos (POST) – Pasta `/service`

### 🌱 POST /service/menu-selecao/{id}/agricultura  
Essa rota representa um dos vários tipos de serviços disponíveis na plataforma.  
Todos seguem a mesma lógica de resposta com `200 OK`.  
![print](https://github.com/user-attachments/assets/c05cde1c-1d5e-4bef-b96f-9ac45747f651)

---

### 💬 POST /service/menu-conversa/{id}  
Menu de conversa relacional com **ID pai**, contendo `idConversa`, e dentro de cada conversa, um `idMensagem`.  
Essa estrutura permite **controle total de hierarquia e exibição** no front-end.  
![print](https://github.com/user-attachments/assets/0ea71fdf-155d-4e16-87f4-ee1a197a20d3)

---

### 📢 POST /service/anuncio/anuncio-agricultura/{id}  
Essa rota lida com a **criação de anúncios específicos por tipo de serviço**.  
O cliente seleciona a categoria (ex: agricultura) e o sistema lida com as particularidades dessa seleção.  
![print](https://github.com/user-attachments/assets/25e583f3-5f94-4e11-93fe-4c7c0005d169)

---

### 📝 POST /service/anuncio/definir/{id} *(exemplo genérico)*  
Rota onde o cliente define o conteúdo do anúncio: título, descrição e tipo.  
Essa estrutura facilita o controle futuro para que **profissionais possam se candidatar** ao serviço, criando listas de interesse por ID do anúncio.  
![print](https://github.com/user-attachments/assets/b48f4e2f-f4e4-4d42-90b3-9c9fca2900bf)

# Projetos-abertos
