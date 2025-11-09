# 1. Nome do Projeto: PlantCare API



Este projeto é a API backend para a solução PlantCare , desenvolvida como parte do Challenge Oracle / FIAP 2TDS.



A API é responsável por gerenciar \[...Descreva as principais entidades, ex: "usuários, plantas, leituras de sensores e recomendações de cuidado"...].



---


## 2. Integrantes do Grupo


| Nome                       | RM       |
|:---------------------------|:---------|
| João Victor Alves da Silva | RM559726 |
| Vinicius Kenzo Tocuyosi    | RM559982 |



---



## 3. Tecnologias Utilizadas



* **Backend:** Java 25 com Spring Boot

* **Banco de Dados:** Oracle Database 23ai (Free)

* **Containerização:** Docker e Docker Compose

* **Cloud:** Microsoft Azure (VM)

* **Segurança:** Spring Security com JWT



---



## 4. Como Rodar a Aplicação (Instruções de Deploy) 



Este projeto é 100% containerizado. Para executá-lo, você só precisa ter o Docker e o Docker Compose instalados.



### Pré-requisitos

* [Docker](https://www.docker.com/get-started)

* [Docker Compose](https://docs.docker.com/compose/install/)

* [Git](https://git-scm.com/)



### Passos para a Execução



1.  **Clone o repositório:**

  ```bash

   git clone https://github.com/JoaoVictor087/plantcare-api

  cd plantcare-api

   ```



2.  **Construa e execute os containers:**

   Este comando irá construir a imagem da API Java e iniciar o container do banco de dados Oracle.

   ```bash

   docker-compose up --build -d

  ```

  * `--build`: Constrói a imagem da API a partir do `Dockerfile`.

   * `-d`: Executa os containers em modo "detached" (em background).



3.  **Aguarde a inicialização:**

  O container do banco de dados Oracle pode levar de 3 a 10 minutos para iniciar completamente. A API irá reiniciar automaticamente (`restart: on-failure`) até que o banco de dados esteja pronto para aceitar conexões.



4.  **Verifique se tudo está no ar**

   Após alguns minutos, execute o comando abaixo:

   ```bash

   docker ps

   ```

   Você deve ver os dois containers (`java-api` e `oracle-db`) com o status `Up`.

---



\## 5. Documentação da API (Endpoints)



A documentação completa da API, gerada com Swagger/OpenAPI, pode ser acessada em:



`http://localhost:8080/api/swagger-ui/index.html`



**Principais Endpoints:**



* `POST /api/auth/login`: Autentica um usuário e retorna um token JWT.

* `POST /api/usuarios`: Cria um novo usuário.

* `GET /api/plantas`: Retorna todas as plantas do usuário autenticado.

* `POST /api/plantas`: Cadastra uma nova planta.

* `GET /api/plantas/{id}`: Retorna os detalhes de uma planta.

* `\[...Adicione outros endpoints importantes...]`



---



\## 6. Vídeo de Demonstração (Challenge)



O vídeo demonstrando o deploy na nuvem Azure e o teste de persistência de dados está disponível no link abaixo:



**[Video YouTube](https://www.youtube.com/watch?v=A85YbNEtUJk)** 

