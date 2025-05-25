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
# 🚀 Projeto Backend – Plataforma de Serviços

Este projeto foi desenvolvido com **Java + Quarkus**, oferecendo uma estrutura robusta e escalável para plataformas de prestação de serviços, como **99freelas**, **Workana**, **GetNinjas** e similares.

---

## ✅ Funcionalidades Principais

- Cadastro e login de **clientes** e **profissionais**
- Publicação e gerenciamento de **anúncios**
- Sistema de **chat** entre usuários
- Upload de **imagens** (perfil e portfólio)
- **Autenticação JWT** segura
- Organização de rotas por domínio (Auth, Service, Image)

---

## 📮 Exemplos de Requisições no Postman – `/auth`

### 👤 POST `/auth/registro/profissional`  
Cadastra um novo profissional com retorno do `ObjectId`.  
![print](https://github.com/user-attachments/assets/07d7c64d-62fa-486a-9d6f-aa76b18313d5)

### 👤 POST `/auth/registro/cliente`  
Cadastra um novo cliente com retorno do `ObjectId`.  
![print](https://github.com/user-attachments/assets/8ead3fd3-18d6-4be3-b698-287ad4cf6cf4)

### 🔐 POST `/auth/login/cliente/{id}`  
Login de cliente com validação de e-mail, senha (hash) e ID.  
![print](https://github.com/user-attachments/assets/42b68fcc-7570-4a23-989e-3f9ad6521ed2)

### 🔐 POST `/auth/login/profissional/{id}`  
Login de profissional com validação de e-mail, senha (hash) e ID.  
![print](https://github.com/user-attachments/assets/0181be01-0782-4156-b072-ea2242942940)

> 🔒 As rotas da pasta `/auth` seguem padrão seguro com retorno de **JWT**.

---

## 🛠️ Requisições – `/service`

### 🌱 POST `/service/menu-selecao/{id}/agricultura`  
Cria um menu de seleção com base em categorias como "agricultura".  
![print](https://github.com/user-attachments/assets/c05cde1c-1d5e-4bef-b96f-9ac45747f651)

### 💬 POST `/service/menu-conversa/{id}`  
Cria conversas hierárquicas com `idConversa` e `idMensagem`.  
![print](https://github.com/user-attachments/assets/0ea71fdf-155d-4e16-87f4-ee1a197a20d3)

### 📢 POST `/service/anuncio/anuncio-agricultura/{id}`  
Criação de anúncios por tipo de serviço (ex: agricultura).  
![print](https://github.com/user-attachments/assets/25e583f3-5f94-4e11-93fe-4c7c0005d169)

### 📝 POST `/service/anuncio/{id}` *(genérico)*  
Cria conteúdo do anúncio: título, descrição e tipo.  
![print](https://github.com/user-attachments/assets/225ee9ce-78ca-4c96-8135-d700c5b88387)

> 🧩 Todas essas rotas seguem lógica REST e usam `ObjectId` como identificador principal.

---

## 🖼️ Requisições – `/image`

### 🖼️ POST `/image/perfil-cliente/{id}/upload`  
Upload da foto de perfil do cliente.  
![image](https://github.com/user-attachments/assets/599e728c-aa35-4b97-b3ef-fda25a890e6b)

### 📁 POST `/image/profissional/{id}/upload-portfolio`  
Upload de imagens de portfólio do profissional.  
![image](https://github.com/user-attachments/assets/70798c6e-a851-4262-83d3-535b515f2cb1)

---

## ⚙️ Arquitetura e Performance

Este sistema foi arquitetado com foco em **modularidade**, **autenticação robusta**, e **eficiência em banco de dados**:

- Todas as rotas seguem padrão RESTful.
- Utilização de `ObjectId` do MongoDB em todas as operações.
- Buscas rápidas com notação **O(1)** por índice.
- Backend preparado para escalar horizontalmente.

---
