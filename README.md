# HTML Mimo

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/pt-BR/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)
[![GitHub Pages](https://img.shields.io/badge/demo-GitHub%20Pages-222222?logo=github&logoColor=white)](https://pages.github.com/)
[![Status](https://img.shields.io/badge/status-conclu%C3%ADdo-brightgreen)](#)
[![Licença](https://img.shields.io/badge/licen%C3%A7a-MIT-green)](LICENSE)
[![Linguagem predominante](https://img.shields.io/badge/linguagem-JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)

Coleção de projetos desenvolvidos durante os estudos de HTML, CSS e JavaScript na plataforma Mimo.

## Sumário

- [Visualização](#visualização)
- [Descrição do projeto](#descrição-do-projeto)
- [Tecnologias utilizadas](#tecnologias-utilizadas)
- [Arquitetura e estrutura](#arquitetura-e-estrutura)
- [Como executar localmente](#como-executar-localmente)
- [Uso e exemplos](#uso-e-exemplos)
- [Troubleshooting e FAQ](#troubleshooting-e-faq)
- [Contribuição](#contribuição)
- [Autor](#autor)
- [Licença](#licença)

## Visualização

### Caesar Cipher

![Preview do Caesar Cipher](projetos-gerais/caesar-cipher/preview.png)

### Rick and Morty Character Compass

![Preview do Rick and Morty Character Compass](projetos-gerais/rick-and-morty/preview.png)

### Trivia Game

![Preview do Trivia Game](projetos-gerais/trivia-game/preview.png)

### Typewriter Portfolio

![Preview do Typewriter Portfolio](projetos-gerais/typewriter-portfolio/preview.png)

## Descrição do projeto

Este repositório reúne pequenos projetos frontend criados como parte do aprendizado de desenvolvimento web. As aplicações exploram conceitos como estruturação com HTML, estilização com CSS, manipulação do DOM e interação com o usuário usando JavaScript.

A coleção inclui uma cifra de César, um explorador de personagens que consome uma API pública, um jogo de perguntas e um portfólio estático com estética de máquina de escrever.

## Tecnologias utilizadas

- HTML5 para estrutura e conteúdo das páginas.
- CSS3 para layout, cores, tipografia e apresentação visual.
- JavaScript vanilla para lógica de interação e manipulação do DOM.
- Fetch API para consumo da API Rick and Morty.
- Google Fonts para a fonte utilizada no portfólio.
- GitHub Pages para publicação das demonstrações online.

## Arquitetura e estrutura

Cada projeto é independente e segue uma arquitetura frontend estática simples:

```text
html-mimo/
├── LICENSE
├── README.md
└── projetos-gerais/
    ├── caesar-cipher/
    │   ├── index.html
    │   ├── script.js
    │   ├── style.css
    │   ├── README.md
    │   └── preview.png
    ├── rick-and-morty/
    │   ├── index.html
    │   ├── script.js
    │   ├── style.css
    │   ├── README.md
    │   └── preview.png
    ├── trivia-game/
    │   ├── index.html
    │   ├── script.js
    │   ├── style.css
    │   ├── README.md
    │   └── preview.png
    └── typewriter-portfolio/
        ├── index.html
        ├── style.css
        ├── README.md
        └── preview.png
```

### Projetos

- `caesar-cipher`: transforma textos com a Cifra de César, usando deslocamento entre 1 e 25.
- `rick-and-morty`: busca personagens na API pública Rick and Morty e cria cartões dinamicamente.
- `trivia-game`: apresenta perguntas de múltipla escolha e calcula a pontuação.
- `typewriter-portfolio`: apresenta perfil, habilidades e projetos em uma página estática.

### Fluxo de dados

- Cada `index.html` carrega a estrutura da interface e seus arquivos CSS e JavaScript.
- O JavaScript atualiza o DOM conforme o usuário interage com a página.
- O projeto Rick and Morty realiza uma requisição para `https://rickandmortyapi.com/api/character`.
- Os dados retornados pela API são convertidos em cartões inseridos no elemento `#characters-container`.
- Não existe backend, banco de dados ou autenticação.

## Como executar localmente

### Pré-requisitos

- Navegador moderno, como Chrome, Firefox, Edge ou Safari.
- Git, caso o repositório seja clonado.
- Python 3 é opcional para iniciar um servidor local.
- Node.js não é necessário.

### Configuração de ambiente

O projeto não utiliza variáveis de ambiente nem arquivos `.env`.

O projeto Rick and Morty precisa de acesso à internet para consultar a API pública:

```text
https://rickandmortyapi.com/api/character
```

### Instalação

```bash
git clone https://github.com/GiovanniJorge/html-mimo.git
cd html-mimo
```

Não há dependências para instalar.

### Execução direta

Abra qualquer arquivo `index.html` no navegador:

```text
projetos-gerais/caesar-cipher/index.html
projetos-gerais/rick-and-morty/index.html
projetos-gerais/trivia-game/index.html
projetos-gerais/typewriter-portfolio/index.html
```

### Execução com servidor local

Para uma execução mais consistente, especialmente no projeto que utiliza API, inicie um servidor HTTP:

```bash
cd projetos-gerais/rick-and-morty
python -m http.server 8000
```

Acesse `http://localhost:8000` no navegador.

## Uso e exemplos

### Caesar Cipher

1. Informe um deslocamento entre 1 e 25.
2. Digite um texto.
3. Consulte o resultado atualizado automaticamente.

A aplicação preserva letras maiúsculas e minúsculas e mantém caracteres não alfabéticos.

### Rick and Morty Character Compass

1. Inicie o projeto com um servidor local ou pela demonstração online.
2. Aguarde a resposta da API.
3. Consulte nome, status, espécie e imagem dos personagens exibidos.

### Trivia Game

1. Leia a pergunta apresentada.
2. Selecione uma das quatro alternativas.
3. Ao final, consulte sua pontuação.

As perguntas estão definidas diretamente no arquivo JavaScript.

### Typewriter Portfolio

Abra o projeto e navegue pelas seções de perfil, habilidades e projetos.

## Troubleshooting e FAQ

### A lista de personagens não aparece

Verifique a conexão com a internet e a disponibilidade da API. Também é recomendado executar o projeto usando um servidor HTTP local.

### O navegador bloqueou uma requisição

Abra o projeto com `python -m http.server` em vez de usar diretamente o protocolo `file://`.

### É necessário instalar Node.js?

Não. Os projetos usam apenas HTML, CSS e JavaScript executados pelo navegador.

### É necessário configurar um arquivo `.env`?

Não. O repositório não utiliza variáveis de ambiente.

### O jogo Trivia Game possui reinício automático?

Não. Para iniciar uma nova rodada, atualize a página do navegador.

## Contribuição

1. Faça um fork do repositório.
2. Crie uma branch descritiva, como `feature/novo-projeto`.
3. Mantenha a organização independente de cada projeto.
4. Teste as alterações no navegador.
5. Crie um commit claro e objetivo.
6. Abra um Pull Request descrevendo as mudanças.

## Autor

- **Nome:** Giovanni Jorge
- **GitHub:** [@GiovanniJorge](https://github.com/GiovanniJorge)

## Licença

Este projeto está licenciado sob a licença MIT. Consulte o arquivo [LICENSE](LICENSE) para obter os termos completos.
