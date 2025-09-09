# Tarefas API (Spring Boot)

API RESTful para gerenciamento de tarefas (CRUD) em **Java + Spring Boot** com **MySQL**.

## Requisitos
- Java 17+
- Maven 3.8+
- MySQL 8 (ou `docker compose` para subir o MySQL rapidamente)

## Subindo o MySQL via Docker
```bash
docker compose up -d
```
Banco: `tarefasdb` | Usuário: `root` | Senha: `senha`.

> Você pode alterar `application.properties` conforme seu ambiente.

## Rodando a API
```bash
./mvnw spring-boot:run
# ou
mvn spring-boot:run
```

A API vai iniciar em `http://localhost:8080`.

## Endpoints

### Criar Tarefa
`POST /tarefas`  
Body (JSON):
```json
{
  "nome": "Trabalho Web Back End - Seu Nome RU000000",
  "dataEntrega": "2025-09-15",
  "responsavel": "Seu Nome"
}
```

### Listar Tarefas
`GET /tarefas`

### Buscar por ID
`GET /tarefas/{id}`

### Atualizar
`PUT /tarefas/{id}`  
Body (JSON):
```json
{
  "nome": "Trabalho Atualizado - Seu Nome RU000000",
  "dataEntrega": "2025-09-20",
  "responsavel": "Seu Nome"
}
```

### Deletar
`DELETE /tarefas/{id}`

## Dica para a entrega
- Use o Postman para gerar prints **incluindo seu NOME e RU** nos campos `nome`/`responsavel`.
- Suba este projeto no **GitHub** e inclua o link no seu caderno de respostas.
