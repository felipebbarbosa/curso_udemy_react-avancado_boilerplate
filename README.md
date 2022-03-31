# Curso de React Avançado

## Seção 1: Módulo 1: Introdução Teórica

### O que o NextJS tem/faz?

- Renderização no servidor (SSR);
- Geração de estáticos (SSG - Static Site Generation);
- CSS-in-JS (Styled-jsx, Styled Components);
- Zero config. (rotas, hot reloading, code splitting);
- Completamente extensível;
- Otimizado para produção.

### Quem usa?

Netflix, GitHub, Twitch, Uber e outros.

### Tipos de aplicação

- Static Site (SSG) - GatsbyJS, Hexo, Jekyll e NextJS
- Client Side Rendering (Single Page Application - SPA) - Create React App
- Server Side Rendering (SSR) - NextJS

### Vantagens / Desvantagens

#### Static Site Generation - SSG

Vantagens:
- Uso quase nulo do servidor;
- Pode ser servido numa CDN (melhor cache);
- Melhor performance de todos;
- Flexibilidade para usar qualquer servidor;

Desvantagens:
- Tempo de build pode ser muito alto;
- Dificuldade para escalar em apps grandes;
- Dificuldade para realizar atualizações constantes;

#### Single Page Application - SPA

Vantagens:
- Permite páginas ricas em interações sem recarregar;
- Site rápido após load inicial;
- Ótimo para apps web;
- Possui diversas bibliotecas;

Desvantagens:
- Load inicial pode ser muito grande;
- Performance imprevisível;
- Dificuldade no SEO;
- A maioria do conteúdo não é indexado;

#### Server Side Rendering - SSR

Vantagens:
- Ótimo em SEO;
- Meta tags com previews mais adequados;
- Melhor performance para o usuário (o conteúdo vai ser visto mais rápido);
- Código compartilhado com backend em Node;
- Menor processamento no lado do usuário;

Desvantagens:
- TTFB (Time to first byte) maior, o servidor vai preparar todo o conteúdo para entregar;
- HTML maior;
- Reload completo nas mudanças de rota*.

> O NextJS suporta os três tipos!

### Introdução ao GraphQL

Os GraphQL Clients são responsáveis por criar comandos de abstração para realizar queries/mutations, sistema de cache, validações e otimizações.

#### Fetch client x Caching client

Quais os clients mais conhecidos/utilizados?
- FetchQL
- GraphQL Request
- uRQL
- Relay Modern
- **Apollo Client** <--

### Introduação ao Strapi

O Strapi é um headless CMS open-source feito 100% em Javascript, totalmente customizável e orientado para devs preocupados em agilidade.

#### Vantagens do headless CMS

- Mesma entrega para diferentes tipos de dispositivos;
- Agnóstico de frameworks;
- Mais fácil na manutenção;
- Mais ágil para criação de protótipos;

#### Vantagens do Strapi

- 100% open-source;
- Altamente customizável (API e painel);
- Funciona com REST API ou GraphQL ao apertar de um botão;
- Self hosted (você controla seus dados e onde colocá-los);
- Roadmap bem definido e grande investimento;

#### Algumas features nativas do Strapi

- Suporte a múltiplos BD (SQLite, MongoDB, Postgres, MariaDB);
- Doc automática c/ plugin de one-click
- Integração a webhooks;
- Autenticações e permissões por padrão;
- Integração c/ diferentes serviços (Cloudinary, Algolia, Redis);
- Sistema de e-mails;
- Sistema de assets que otimiza imagens e cria em diferentes tamanhos

#### O que podemos fazer com Strapi

- Sites estáticos;
- Sites institucionais para empresas;
- Sites de notícias;
- E-commerce;
- O que você quiser!

#### Porque usar o Strapi

- Mais agilidade;
- Codebase toda em JS (+fácil manutenção);
- Sem mensalidade e controle do próprio dado (contentful, DatoCMS);

#### Como funciona o Strapi

- Possui 3 tiposde estruturas de dados:
  - Collection types (conjunto de dados padrão. Ex: Usuários, Produtos);
  - Single types (dado único. Ex: Homepage, footer, menu);
  - Component types (estrutura de dados reutilizadas. Ex: Galerias, Hero);

### CSS-in-JS

Bibliotecas: Aphrodite, Emotion, Glamour, **-> Styled Componentes <-** e Styled JSX.

#### Vantagens do Styled Components

- Critical CSS automático;
- Escopo definido (sem colisão de classes);
- Remoção de CSS não utilizado;
- Estilos dinâmicos (Props, Themes);
- Manutenção simplificada e sem dor;

### Introdução a Testes de Software

#### Tipos de teste

- Testes unitários
  - Testam isoladamente pequenas unidades de código;
  - O código está se comportando como o **dev** espera?
- Testes funcionais
  - Checa se as unidades funcionam também entre si;
  - Testes podem conter multiplas classes, métodos;
  - O programa funciona de acordo com que o **usuário** espera?

> TDD, Jest

## Seção 2: Módulo 1: Criando nosso Boilerplate do NextJS

### Configurando o TypeScript

```
touch tsconfig.json
yarn dev
yarn add --dev typescript @types/react @types/node
yarn dev
```

[Alterações feitas neste tópico.](https://github.com/felipebbarbosa/curso_udemy_react-avancado_boilerplate/commit/4672c416a9854f12494b85103e38ba2fb65f8414)

### Configurando o ESLint

```
npx eslint --init
yarn add eslint-plugin-react-hooks --dev
```

[Alterações feitas neste tópico.](https://github.com/felipebbarbosa/curso_udemy_react-avancado_boilerplate/commit/aed958c2e1dfcc92b73774cd2a263e8012f5ddad)

### Configurando o Prettier c/ Eslint

```
yarn add --dev --exact prettier
yarn add --dev eslint-plugin-prettier eslint-config-prettier
```

### Configurando um Git Hook c/ Husky e Lint-Staged (Opcional)

```
yarn add husky --dev
yarn husky init
yarn add lint-staged --dev
```


### Instalando e configurando o Jest com TypeScript

Site oficial do [Jest](https://jestjs.io/)

```
yarn add --dev jest @babel/preset-typescript @types/jest
```

[Alterações feitas neste tópico.](https://github.com/felipebbarbosa/curso_udemy_react-avancado_boilerplate/commit/221b3afef815a11a12d99ab9d061dacb1062f399)

### Instalando o React Testing Library e escrevendo os primeiros testes

Site oficial do [React Testing Library](https://testing-library.com/docs/react-testing-library/intro/)

```
yarn add --dev @testing-library/react @testing-library/jest-dom
```

Link para o [Cheatsheet](https://testing-library.com/docs/react-testing-library/cheatsheet/)

[Alterações feitas neste tópico.](https://github.com/felipebbarbosa/curso_udemy_react-avancado_boilerplate/commit/df535fb30018ccd6abfa6fbac062bd750d133728)


### Instalando o Styled Components e configurando o SSR


```
yarn add --dev @types/styled-components babel-plugin-styled-components
yarn add styled-components
```

[Alterações feitas neste tópico.](https://github.com/felipebbarbosa/curso_udemy_react-avancado_boilerplate/commit/d5196a56ecce8df00070e45865263051207bd312)
- [Estilos globais](https://github.com/felipebbarbosa/curso_udemy_react-avancado_boilerplate/commit/b69057460a52f1ab1865dc6ef1d9c4a5f5f0bc6e) 

### Melhorando snapshots com Jest-styled-components

```
yarn add --dev jest-styled-components
```

[Alterações feitas neste tópico.](https://github.com/felipebbarbosa/curso_udemy_react-avancado_boilerplate/commit/79fd3655633a34314289ebf9dd75ca911b144dce)

### Configurando o Storybook e escrevendo stories

[Storybook](https://storybook.js.org/) é uma ferramenta para testes de componentes de UI de forma isolada.

```
npx sb init
```

[Alterações feitas neste tópico.](https://github.com/felipebbarbosa/curso_udemy_react-avancado_boilerplate/commit/cc232b04ae88b5b089aa6bf34505a1788a9e0cf1)
- [Storybook Essentials](https://github.com/felipebbarbosa/curso_udemy_react-avancado_boilerplate/commit/3d16b0612dfd56a555aec1064b15b3b2cc4fa508)

### Configurando o PWA

Utilizamos o plugin [next-pwa](https://www.npmjs.com/package/next-pwa), para configurá-lo:

```
yarn add next-pwa
```
Para testar:

```
NODE_ENV=production yarn build
yarn start
```

[Alterações feitas neste tópico.](https://github.com/felipebbarbosa/curso_udemy_react-avancado_boilerplate/commit/e0670e5b76174516d255a9e1c73374e4cfc4ef69)

### Iniciando um projeto através do boilerplate

```
yarn create next-app -e https://github.com/felipebbarbosa/curso_udemy_react-avancado_boilerplate
```

### Automatizando criação de arquivos

Criando arquivos a partir de um template com [PLOP](https://plopjs.com/). Para instalá-lo:

```
yarn add -D plop
```