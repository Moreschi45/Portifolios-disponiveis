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
- Organização de rotas por domínio (`/auth`, `/service`, `/image`)

---

## 📮 Requisições POST – Pasta `/auth`

### 👤 POST `/auth/registro/profissional`  
Cadastra um novo profissional com retorno do `ObjectId`.  
![print](https://github.com/user-attachments/assets/07d7c64d-62fa-486a-9d6f-aa76b18313d5)

### 👤 POST `/auth/registro/cliente`  
Cadastra um novo cliente com retorno do `ObjectId`.  
![print](https://github.com/user-attachments/assets/8ead3fd3-18d6-4be3-b698-287ad4cf6cf4)

### 🔐 POST `/auth/login/cliente/{id}`  
Login do cliente com validação de e-mail, senha (hash) e ID.  
![print](https://github.com/user-attachments/assets/42b68fcc-7570-4a23-989e-3f9ad6521ed2)

### 🔐 POST `/auth/login/profissional/{id}`  
Login do profissional com validação de e-mail, senha (hash) e ID.  
![print](https://github.com/user-attachments/assets/0181be01-0782-4156-b072-ea2242942940)

> 🔒 As rotas da pasta `/auth` seguem padrão seguro com retorno de **JWT**.

---

## 🛠️ Requisições POST – Pasta `/service`

### 🌱 POST `/service/menu-selecao/{id}/agricultura`  
Cria um menu de seleção com base na categoria escolhida (ex: agricultura).  
![print](https://github.com/user-attachments/assets/c05cde1c-1d5e-4bef-b96f-9ac45747f651)

### 💬 POST `/service/menu-conversa/{id}`  
Cria conversas com hierarquia (`idConversa` e `idMensagem`).  
![print](https://github.com/user-attachments/assets/0ea71fdf-155d-4e16-87f4-ee1a197a20d3)

### 📢 POST `/service/anuncio/anuncio-agricultura/{id}`  
Criação de anúncios vinculados à categoria de serviço.  
![print](https://github.com/user-attachments/assets/25e583f3-5f94-4e11-93fe-4c7c0005d169)

### 📝 POST `/service/anuncio/{id}` *(genérico)*  
Define título, descrição e tipo do anúncio.  
![print](https://github.com/user-attachments/assets/225ee9ce-78ca-4c96-8135-d700c5b88387)

---

## 🖼️ Requisições POST – Pasta `/image`

### 🖼️ POST `/image/perfil-cliente/{id}/upload`  
Faz upload da foto de perfil do cliente.  
![image](https://github.com/user-attachments/assets/599e728c-aa35-4b97-b3ef-fda25a890e6b)

### 📁 POST `/image/profissional/{id}/upload-portfolio`  
Faz upload das imagens de portfólio do profissional.  
![image](https://github.com/user-attachments/assets/70798c6e-a851-4262-83d3-535b515f2cb1)

---

## 📥 Requisições GET – Pasta `/service`

### 👤 GET `/service/busca/perfil-cliente/{id}`  
Busca os dados do cliente com base no `id`.  
![image](https://github.com/user-attachments/assets/636963b1-6cd2-4d2f-85dd-bf5f0c1debec)

### 👤 GET `/service/busca/perfil-profissional/{id}`  
Busca os dados do profissional com base no `id`.  
![image](https://github.com/user-attachments/assets/d0ddaf20-6a96-4c00-ad04-096489218963)

### 🌱 GET `/service/tipo-anuncio/agricultura/{id}`  
Retorna o tipo de serviço escolhido no momento do anúncio.  
![image](https://github.com/user-attachments/assets/9a587816-2485-432f-b0a9-f5a2529a27cf)

### 🧩 GET `/service/tipos-de-servicos/menu-agricultura/{id}`  
Busca o tipo de serviço selecionado no cadastro do profissional.  
![image](https://github.com/user-attachments/assets/e756c822-a4aa-488d-8f66-01136f41061e)

### 📢 GET `/service/anuncio/{id}`  
Lista os anúncios vinculados ao `id` do criador (cliente).  
![image](https://github.com/user-attachments/assets/0c74866d-70c3-46c6-8c0c-5c6b4e4e5e66)

### 🏠 GET `/service/perfil-profissional/endereco-profissional/{id}`  
Retorna o endereço cadastrado tanto para cliente quanto para profissional.  
![image](https://github.com/user-attachments/assets/8106294d-8dae-4d3a-a4a3-7289b2435b9e)

---

## 🖼️ Requisições GET – Pasta `/image`

### 🖼️ GET `/image/view/{id}/{idImagem}`  
Recupera a imagem salva no banco, utilizando `id` do dono e `idImagem`.  
![image](https://github.com/user-attachments/assets/e5b18c16-8ef2-40e2-8140-e1f634e057fa)

### 🧳 GET `/image/view/profissional/{id}/{idPortfolio}`  
Recupera o portfólio salvo do profissional por `id` e `idPortfolio`.  
![image](https://github.com/user-attachments/assets/19f09f65-0fe6-40db-8feb-a575203448b0)

---

## ⚙️ Arquitetura e Performance

Este sistema foi arquitetado com foco em:

- ✅ **Modularidade** por domínio de funcionalidade
- ✅ **Autenticação segura** com JWT
- ✅ **Persistência no MongoDB** com uso extensivo de `ObjectId`
- ✅ **Alto desempenho** com buscas rápidas via notação **O(1)** com indexação
- ✅ Estrutura pensada para **escalabilidade horizontal**

---

---
