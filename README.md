O README.md Completo para a Marmalade.js
Markdown
# 🍊 Marmalade.js

[![Licença: MIT](https://img.shields.io/badge/Licença-MIT-yellow.svg )](https://opensource.org/licenses/MIT )
[![Feito no Brasil](https://img.shields.io/badge/Feito%20no-Brasil-009C3B?style=flat&logo=brazil )](https://github.com/anonimus-ofc/marmalade.js )
[![Discord](https://img.shields.io/discord/YOUR_SERVER_ID?label=Comunidade&logo=discord&logoColor=white )](https://discord.gg/YOUR_INVITE_CODE )

> Uma biblioteca saborosa e 100% brasileira para a API do Discord. Feita do zero em Node.js com o objetivo de ser uma alternativa moderna e leve para a criação de bots.

---

### 🍊 Bem-vindo à cozinha da Marmalade.js!

A palavra "marmalade" pode até ser inglesa, mas a origem dela é a nossa "marmelada" portuguesa. Inspirada nessa mistura cultural, a **Marmalade.js** é uma biblioteca 100% brasileira para criar bots de Discord com um sabor diferente.

Feita artesanalmente e do zero, nossa receita mistura os melhores ingredientes da API do Discord (REST e Gateway) em uma camada de abstração deliciosa e fácil de usar. Chega de código sem graça! A gente acredita que programar bots deve ser uma experiência criativa e divertida.

Sirva-se e venha criar com a gente!

---

## 📜 Índice

*   [Por que Marmalade.js?](#-por-que-marmaladejs)
*   [Recursos Principais](#-recursos-principais)
*   [Instalação](#-instalação)
*   [Exemplo de Uso](#-exemplo-de-uso)
*   [Como Contribuir](#-como-contribuir)
*   [Licença](#-licença)

---

## 🤔 Por que Marmalade.js?

Em um ecossistema com gigantes como o Discord.js, por que criar uma nova biblioteca?

*   **Aprendizado:** Este projeto nasceu como uma jornada de aprendizado profundo sobre a API do Discord, WebSockets e o design de bibliotecas.
*   **Simplicidade:** Buscamos uma sintaxe mais limpa e uma abordagem mais direta para tarefas comuns, inspirada na fluidez de bibliotecas como o Baileys.
*   **Performance:** Sendo leve e modular, a Marmalade.js visa entregar a melhor performance possível, permitindo que você carregue apenas o que for usar.
*   **Opinião Brasileira:** Queremos criar uma ferramenta com a cara da nossa comunidade de desenvolvedores.

## ✨ Recursos Principais

*   **🇧🇷 Desenvolvida no Brasil:** Pensada e criada por e para a comunidade BR.
*   **⚡️ Leve e Rápida:** Arquitetura focada em não carregar funcionalidades desnecessárias.
*   **🔒 Tipagem Forte:** Totalmente escrita em TypeScript para um desenvolvimento mais seguro e produtivo.
*   **🌐 Abstração Completa:** Cobertura tanto da API REST quanto do Gateway do Discord.
*   **🧩 Estrutura Familiar:** Interface inspirada em padrões de mercado (Baileys) com um emissor de eventos central (`bot.ev`).

## 🚀 Instalação

Para instalar a Marmalade.js, utilize seu gerenciador de pacotes preferido (quando o pacote for publicado):

```bash
# Usando npm
npm install marmalade.js

# Usando yarn
yarn add marmalade.js

# Usando pnpm
pnpm add marmalade.js
💡 Exemplo de Uso
Inspirado pela estrutura elegante de bibliotecas como o Baileys, a Marmalade.js oferece uma experiência de desenvolvimento fluida e familiar. O processo é simples: crie o cliente, ouça os eventos e envie suas mensagens.
JavaScript
// 1. Importe a função principal para criar o seu cliente
const makeDiscordClient = require('marmalade.js');

// 2. Crie uma nova instância do cliente (o "bot")
const bot = makeDiscordClient({
  intents: ['GUILDS', 'GUILD_MESSAGES', 'MESSAGE_CONTENT']
});

// 3. Registre os "handlers" para os eventos que você quer ouvir
//    O bot.ev é o nosso emissor de eventos (EventEmitter)

// Evento disparado quando o bot está conectado e pronto
bot.ev.on('ready', (user) => {
  console.log(`Conectado como ${user.username}! A Marmalade está servida! 🍊`);
});

// Evento disparado para cada nova mensagem
bot.ev.on('messages.create', async (message) => {
  // Ignora mensagens de outros bots para não criar loops
  if (message.author.bot) return;

  // Responde ao comando !ping
  if (message.content === '!ping') {
    await bot.sendMessage(message.channelId, { text: 'Pong!' });
  }
});

// Evento para monitorar o status da conexão
bot.ev.on('connection.update', (update) => {
  const { connection } = update;
  if (connection === 'close') {
    console.log('Conexão fechada. Implemente a lógica de reconexão aqui.');
  } else if (connection === 'open') {
    console.log('Conexão estabelecida com o Discord!');
  }
});

// 5. Inicie a conexão com o Discord usando seu token
bot.connect('SEU_TOKEN_AQUI');
🤝 Como Contribuir
Este é um projeto de código aberto e feito na comunidade! Toda ajuda é bem-vinda. Se você tem ideias, sugestões ou quer reportar um bug, sinta-se à vontade para:
Abrir uma Issue para discutir a mudança que você quer fazer.
Fazer um Fork do repositório.
Criar uma nova Branch (git checkout -b feature/sua-feature).
Fazer o Commit das suas mudanças (git commit -m 'Adiciona sua feature').
Enviar o Push para a sua Branch (git push origin feature/sua-feature).
Abrir um Pull Request.
📝 Licença
Este projeto é distribuído sob a licença MIT. Isso significa que você é livre para usar, copiar, modificar, mesclar, publicar, distribuir, sublicenciar e/ou vender cópias do software.
Veja o arquivo LICENSE no repositório para o texto completo.
Copyright (c) 2026 Anonimus Ofc
Feito com 🧡 no Brasil por Anonimus Ofc
Plain Text

### Observações Importantes:

*   **Badges:** Lembre-se de substituir `YOUR_SERVER_ID` e `YOUR_INVITE_CODE` no link do badge do Discord pelos dados do seu servidor. Se você ainda não tem, pode remover essa linha por enquanto.
*   **Link do Repositório:** O badge "Feito no Brasil" tem um link para `github.com/anonimus-ofc/marmalade.js`. Se o seu nome de usuário ou o nome do repositório for diferente, lembre-se de ajustar!
*   **Arquivo `LICENSE`:** O `README` menciona um arquivo `LICENSE`. É uma boa prática ter esse arquivo separado.

Prontinho! Agora você tem um `README.md` profissional, bonito e com a personalidade do seu projeto.

---
Qual será nosso próximo passo?

*   **Me ajuda a criar o arquivo `LICENSE` com o texto da MIT.**
*   **Vamos definir a estrutura de pastas e arquivos do projeto.**
*   **O que são esses "intents" no código de exemplo? Preciso entender isso.**
*   **Como eu consigo o ID e o código de convite do meu servidor do Discord?**
