# API CRUD feita com Spring Boot e hospeada no Heroku utilizando PostgreSQL
## O aprendizado adquirido neste projeto:
- Criar projeto Spring Boot Java.
- Implementar modelo de domínio.
- Estruturar camadas lógicas: resource, service, repository.
- Configurar banco de dados de teste (H2).
- Povoar o banco de dados.
- CRUD - Create, Retrieve, Update, Delete.
- Tratamento de exceções.
- Deploy da aplicação no Heroku.

## URL da aplicação no Heroku:
- https://javaspringboot-project.herokuapp.com/
### Endpoints disponiveis: 
- users | users/{id}
- products | products/{id}
- categories | categories/{id} 
- orders | orders/{id}

**É importante ressaltar, que o CRUD está implementado apenas para users, a implementação de orders, products e categories ainda é necessária ser realizada juntamento com o "seed" do banco de dados. Print que está marcado com (localhost) foi feito no banco de dados H2 somente para testes de funcionamento.**

## O que esta aplicação consegue realizar: 
- CRUD de usuários (Já no Heroku).
![image](https://user-images.githubusercontent.com/89523373/168155518-364d1b3f-ec4d-4326-be88-65f0399f8826.png)

- Gerenciamento de pedidos com todos os dados necessários, sendo eles: itens(cada item contendo seu valor, quantidade e categoria), cliente, status do pagamento e valor total (localhost).
![image](https://user-images.githubusercontent.com/89523373/168156434-565e6f35-993e-4570-a99c-a2e4efb735d1.png)

## Tratamentos personalizados
- Retorna 404 Not Found quando um usuário não existe em vez de um erro 500 genérico.
![image](https://user-images.githubusercontent.com/89523373/168156747-9ce01e9b-9352-4b86-88e3-8783fdf55558.png)
- Quando um usuário com pedidos realizados tenta ser apagado, não é permito e gera um tratamento personalizado, gerando um 400 Bad Request em vez de um 500 genérico.
![image](https://user-images.githubusercontent.com/89523373/168156895-9df6c529-43ea-4c69-a317-b1c47ca6aab4.png)

