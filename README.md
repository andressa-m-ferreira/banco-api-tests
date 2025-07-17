# 🧪 banco-api-tests

## 🎯 Objetivo  
Este projeto automatiza testes de integração da **API REST do “banco-api”** (desenvolvida pelo Professor Julio de Lima). Validamos respostas, status HTTP e fluxos principais (criação, listagem, edição e remoção de contas, operações, etc.).

## 🛠️ Stack  
- **Linguagem**: JavaScript (ES6+)  
- **Test Runner**: [Mocha](https://mochajs.org/)  
- **HTTP assertion**: [Supertest](https://www.npmjs.com/package/supertest)  
- **Assertiva/Biblioteca de Expect**: [Chai](https://www.chaijs.com/)  
- **Relatórios**: [mochawesome](https://www.npmjs.com/package/mochawesome)  
- Outras libs usadas conforme `package.json`

## 📁 Estrutura de diretórios:


```
banco-api-tests/
├── fixtures/ # arquivos com dados estáticos (payloads de testes)
│ ├── posLogin.json
│ └── postTransferencias.json
├── helpers/ # funções auxiliares 
│ └── autenticacao.js
├── mochawesome-report/ # relatórios HTML gerados automaticamente
│ ├── assets/
│ │ └── ...
│ ├── mochawesome.html
│ └── mochawesome.json
├── test/ # arquivos de teste (Mocha + Supertest + Chai)
│ ├── login.test.js
│ ├── transferencias.test.js
├── .env # arquivo de configuração (não comitado)
├── package.json
└── README.md
````

## ⚙️ Configuração do `.env`  
Crie um arquivo `.env` na raiz com o conteúdo:

## URL base da API a ser testada
- `BASE_URL`: URL da instância da API (ex: `http://localhost:3000`).

## 🚀 Instalação e execução  

1. Clone este repositório e acesse-o:
   ```bash
   git clone https://github.com/andressa-m-ferreira/banco-api-tests.git
2. Instale dependências:
   ```bash
   npm install

3. Crie e edite o .env:
      ```bash
   cp .env  # crie o .env manualmente
   
4. Execute os testes:
      ```bash
   npm test

5. Gere relatório HTML automaticamente (via mochawesome):
  Se configurado no `package.json`:
     ```bash
     
   npm test # e acesse o arquivo .html gerado pelo mochawesome

  
  ou assim:
  
      npm test npx mocha --reporter mochawesome



6. Acesse os relatórios em `mochawesome/mochawesome.html`.


## 📚 Documentação das dependências:
- [Mocha](https://mochajs.org/)
- [Supertest](https://www.npmjs.com/package/supertest)
- [Chai](https://www.chaijs.com/)
- [mochawesome](https://www.npmjs.com/package/mochawesome)

