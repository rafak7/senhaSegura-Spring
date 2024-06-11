# Senha Segura

## 🚀 Tecnologias utilizadas
- Java
- Spring Boot

## 🔍 Baixe o projeto e teste você mesmo na prática
1. Clone o repositório:
    ```sh
    git clone https://github.com/seu-usuario/senhaSegura-Spring.git
    ```
2. Navegue até o diretório do projeto:
    ```sh
    cd senhaSegura-Spring
    ```
3. Execute a aplicação:
    ```sh
    mvn clean spring-boot:run
    ```

Acesse a aplicação em `http://localhost:8080`.

## 📄 Exemplo de Uso da API

Você pode verificar a segurança de uma senha fazendo uma requisição POST para o endpoint `/validate-password` com um corpo JSON contendo a senha que deseja verificar. Veja um exemplo utilizando o Postman:

#### Request
- **Method**: POST
- **URL**: `http://localhost:8080/validate-password`
- **Body**:
    ```json
    {
        "password": "123"
    }
    ```

#### Response
- **Status**: 200 OK
- **Body**:
    ```json
    {
        "failures": [
            "A senha deve possuir pelo menos 8 caracteres",
            "A senha deve conter pelo menos uma letra maiúscula",
            "A senha deve conter pelo menos uma letra minúscula",
            "A senha deve conter pelo menos um dígito especial (e.g., !@#$%)"
        ]
    }
    ```
### Cenário 2: Senha cumpre todos os requisitos

#### Request
- **Method**: POST
- **URL**: `http://localhost:8080/validate-password`
- **Body**:
    ```json
    {
        "password": "123A5a#!"
    }
    ```

#### Response
- **Status**: 204 No Content



---
