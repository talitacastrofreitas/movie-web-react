# 🎬 Movie Application (Movies SPA) - React & TMDB API
Um aplicativo SPA (Single Page Application) responsivo desenvolvido em **React** que consome dados reais da API **TMDB (The Movie Database)** para listar os filmes mais populares em cartaz. O projeto foi projetado com foco em arquitetura limpa, utilizando camadas isoladas de serviços HTTP, hooks de estado customizados e roteamento dinâmico.

---
## 🎯 Principais Recursos
- **Roteamento Centralizado (React Router Dom v6):** Utilização do método moderno `createBrowserRouter` para controle de rotas.
- **Root Layout Pattern:** Estruturação de uma casca visual compartilhada (`RootLayout.js`) contendo o cabeçalho (`<Header />`) e o ponto de ancoragem de páginas filhas (`<Outlet />`).
- **Cliente HTTP Dedicado (Axios):** Centralização de chamadas HTTP no arquivo [config/http.js](file:///C:/Users/TALITA%20CASTRO/.gemini/antigravity/scratch/movie-web-react/src/config/http.js), configurado com o token Bearer JWT de autorização do TMDB.
- **Camada de Serviços Abstraída:** Centralização dos endpoints do TMDB (créditos, vídeos, avaliações, recomendações, similares e detalhes) no arquivo [services/movies.services.js](file:///C:/Users/TALITA%20CASTRO/.gemini/antigravity/scratch/movie-web-react/src/services/movies.services.js).
- **Hooks Customizados:** Isolamento de chamadas assíncronas e lógica de ciclo de vida em hooks reutilizáveis (`useMovies` e `useMovie`).
---
## 📂 Estrutura do Projeto
```bash
movie-web-react/
├── public/
│   ├── index.html           # Documento HTML base
│   └── manifest.json        # Arquivo de manifesto PWA
├── src/
│   ├── components/
│   │   └── Header.js        # Cabeçalho da aplicação contendo os links de navegação (`Link`)
│   ├── config/
│   │   └── http.js          # Configuração da instância Axios e cabeçalhos de autenticação do TMDB
│   ├── hooks/
│   │   └── useMovies.js     # Hooks customizados para gerenciar o estado dos filmes
│   ├── services/
│   │   └── movies.services.js# Abstração de endpoints HTTP e serviços da API
│   ├── views/
│   │   ├── Home.js          # Página inicial simples (Placeholder)
│   │   ├── Movies.js        # Página de listagem de filmes populares
│   │   └── RootLayout.js    # Layout mestre que compartilha o Header entre as rotas
│   ├── App.js               # Orquestrador que aplica as rotas na aplicação
│   ├── index.css            # Folha de estilo básica
│   ├── index.js             # Ponto de entrada do React que inicializa o virtual DOM
│   ├── routes.js            # Definição e mapeamento do objeto de rotas da SPA
│   └── [arquivos adicionais]
├── package.json             # Registro de scripts e dependências do npm
└── README.md                # Documentação do projeto
```
---
## 🛠️ Tecnologias Utilizadas
- **React v19.1.0:** Biblioteca front-end reativa (última versão estável).
- **React Router Dom v6.30:** Roteador moderno declarativo de páginas.
- **Axios v1.11.0:** Cliente HTTP baseado em Promessas.
- **TMDB API v3:** Provedor oficial de metadados de filmes.

---
## 💻 Como Rodar o Projeto
### Requisitos:
Certifique-se de possuir o [Node.js](https://nodejs.org/) instalado em sua máquina.
### Execução:
1. Abra o terminal na raiz do projeto.
2. Instale as dependências executando:
   ```bash
   npm install
   ```
3. Inicie o servidor em modo de desenvolvimento local:
   ```bash
   npm start
   ```
4. Acesse pelo navegador em: [http://localhost:3000](http://localhost:3000).
5. Certifique-se de possuir acesso à internet para realizar as requisições à API do TMDB.
| `npm run eject` | Expõe as configurações internas do projeto (irreversível) |
