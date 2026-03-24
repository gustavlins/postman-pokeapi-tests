# 🍎 PokeAPI Automation Tests - Postman

![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

Este repositório contém uma suíte de testes automatizados para a [PokeAPI](https://pokeapi.co/), desenvolvida como parte de um projeto de validação de qualidade (QA) em APIs REST e Scripts.

## 🎯 Objetivo do Projeto
Validar o comportamento dos endpoints de "Berries" da PokeAPI, garantindo que as informações de nome, status code e atributos de firmeza (firmness) estejam retornando corretamente conforme a documentação oficial.

## 🧪 Testes Implementados
O script de testes (localizado na aba "Scripts" do Postman) realiza as seguintes validações:
- **Status Code:** Verifica se a API retorna `200 OK`.
- **Validação Dinâmica de Nomes:** Compara o nome da Berry retornado com variáveis globais do ambiente.
- **Checagem de Propriedades:** Valida se o campo `firmness` está presente e devidamente preenchido no JSON de resposta.

## 🛠️ Como Executar os Testes

### 1. Pré-requisitos
Você precisará ter o **Postman** (Desktop ou Web) instalado.

### 2. Importação
1. Faça o download do arquivo `pokeAPI_collection.json` deste repositório.
2. No Postman, clique em **Import** e selecione o arquivo.

### 3. Configuração de Variáveis
Para o funcionamento correto, certifique-se de configurar as seguintes variáveis globais no seu Workspace:
- `baseURL`: `https://pokeapi.co/api/`
- `version`: `v2`
- `berry_name`: Nome da berry que deseja testar (ex: `cheri`)

### 4. Rodando os Testes
- Clique na Collection e selecione **Run Collection**.
- Ou rode via terminal usando o **Newman**:
  ```bash
  newman run pokeAPI_collection.json
