# Caixa Eletrônico API

## Descrição

Esta API simula o funcionamento de um caixa eletrônico. Ela recebe um valor de saque desejado e retorna a quantidade de cédulas de cada valor necessárias para compor esse saque, utilizando a menor quantidade de cédulas possível.

### Endpoints

### `/api/saque` (POST)

- **Entrada**:
  - `valor`: Inteiro positivo que representa o valor do saque desejado.
  - Exemplo:
    ```json
    {
      "valor": 380
    }
    ```

- **Saída**:
  - JSON contendo a quantidade de cédulas de cada valor.
  - Exemplo:
    ```json
    {
      "100": 3,
      "50": 1,
      "20": 1,
      "10": 1,
      "5": 0,
      "2": 0
    }
    ```

## Instruções para Execução

1. Clone o repositório:
   ```bash
   git clone <https://github.com/LuisEduardo39/Desafio-T-cnico-Morada.ai.git>
   cd caixa_eletronico
   ```
2.	Instale as dependências:
   ```bash
    pip install -r requirements.txt
    ```
3.	Execute a aplicação:
   ```bash
    python app.py
    ```
4.  Em outro terminal Enviar uma solicitação POST com o valor do saque:
   ```bash
    curl -X POST -H "Content-Type: application/json" -d '{"valor": 380}' http://127.0.0.1:5000/api/saque
    ```
5.	Execute os testes:
   ```bash
    python -m unittest discover tests
    ```