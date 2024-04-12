# Criando-Uma-API-Com-FastAPI-Utilizando-TDD
**Desafio de Projeto: Implementação de uma API com FastAPI e Testes**

Neste projeto, teremos a oportunidade de aprender na prática como implementar o **TDD (Test-Driven Development)** em uma aplicação utilizando o **FastAPI** em conjunto com o **Pytest**. Vamos criar juntos uma API que utiliza o banco de dados **MongoDB** e realizar testes unitários e de integração. Além disso, poderemos conhecer boas práticas de como documentar um projeto.

Aqui estão os passos para iniciar o projeto:

1. **Instalação das dependências:**
    - Certifique-se de ter o Python instalado em sua máquina.
    - Instale o **FastAPI**, o **Pytest** e outras bibliotecas necessárias:
        ```
        pip install fastapi uvicorn pytest httpx
        ```

2. **Crie a estrutura do projeto:**
    - Crie uma pasta para o seu projeto e dentro dela, crie os seguintes arquivos:
        - `main.py`: O arquivo principal da sua aplicação.
        - `test_main.py`: O arquivo de testes.
        - `requirements.txt`: O arquivo para listar as dependências do projeto.

3. **Defina as rotas da API:**
    - No arquivo `main.py`, crie as rotas (endpoints) da sua API utilizando o FastAPI.
    - Por exemplo:
        ```python
        from fastapi import FastAPI

        app = FastAPI()

        @app.get("/")
        def read_root():
            return {"message": "Bem-vindo à API de crossfit!"}
        ```

4. **Configure o MongoDB:**
    - Instale a biblioteca `motor` para trabalhar com o MongoDB:
        ```
        pip install motor
        ```
    - Crie uma conexão com o banco de dados no arquivo `main.py`.

5. **Implemente os testes:**
    - No arquivo `test_main.py`, crie testes unitários e de integração para as funcionalidades da sua API.
    - Utilize o Pytest para executar os testes automaticamente.

6. **Documente o projeto:**
    - Utilize o **Swagger UI** gerado automaticamente pelo FastAPI para documentar as rotas da API.
    - Adicione comentários e docstrings explicativos no código.

7. **Execute a aplicação:**
    - Inicie o servidor com o comando:
        ```
        uvicorn main:app --reload
        ```
    - Acesse a documentação da API em `http://localhost:8000/docs`.

Aqui estão algumas dicas para escrever testes eficazes com **Pytest**:

1. **Organize seus testes:**
    - Separe seus testes em arquivos ou pastas específicas. Por exemplo, crie um diretório chamado `tests` e coloque seus arquivos de teste lá.
    - Nomeie seus arquivos de teste com o prefixo `test_` para que o Pytest os reconheça automaticamente.

2. **Escreva testes claros e descritivos:**
    - Dê nomes significativos aos seus testes. Isso facilita a compreensão do que está sendo testado.
    - Use docstrings para explicar o propósito de cada teste.

3. **Use fixtures:**
    - As fixtures no Pytest permitem criar dados de teste reutilizáveis.
    - Defina fixtures para inicializar objetos, configurar o ambiente ou preparar dados para os testes.

4. **Teste diferentes cenários:**
    - Escreva testes para casos de sucesso e também para cenários de erro.
    - Considere testar limites, valores nulos, entradas inválidas, etc.

5. **Use asserts:**
    - Use afirmações (assertions) para verificar se o resultado esperado é igual ao resultado real.
    - Por exemplo:
        ```python
        def test_soma():
            resultado = soma(2, 3)
            assert resultado == 5
        ```

6. **Use marcadores (markers):**
    - Os marcadores permitem agrupar e executar testes específicos.
    - Por exemplo, você pode marcar testes como "lentos" ou "de integração" e executá-los separadamente.

7. **Execute os testes:**
    - Execute seus testes com o comando:
        ```
        pytest
        ```
    - O Pytest encontrará automaticamente os arquivos de teste e executará os casos de teste.

8. **Verifique a cobertura de código:**
    - Use ferramentas como o `pytest-cov` para verificar a cobertura de código pelos seus testes.
    - Isso ajuda a identificar áreas não testadas.

Só lembrando que devemos adaptar essas dicas conforme as necessidades específicas de cada projeto.

 https://github.com/digitalinnovationone/store_api
