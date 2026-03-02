Markdown
<div align="center">

# 🍊 Marmalade.js

**Uma biblioteca saborosa e 100% brasileira para a API do Discord, feita do zero.**   

*Idealizada e desenvolvida por Anonimus Ofc.*

</div>

<div align="center">

[![Versão](https://img.shields.io/npm/v/@anonimusofficial/marmalade?style=for-the-badge&color=E21818&labelColor=121212 )](https://www.npmjs.com/package/@anonimusofficial/marmalade )
[![Licença](https://img.shields.io/github/license/anonimusofficial/marmalade.js?style=for-the-badge&color=820303&labelColor=121212 )](https://github.com/anonimusofficial/marmalade.js/blob/main/LICENSE )
[![Feito no Brasil](https://img.shields.io/badge/Feito%20no-Brasil-009C3B?style=for-the-badge&labelColor=121212&logo=brazil )](https://github.com/anonimusofficial/marmalade.js )
[![Comunidade](https://img.shields.io/discord/YOUR_SERVER_ID?style=for-the-badge&logo=discord&logoColor=white&label=Comunidade&color=5800FF&labelColor=121212 )](https://discord.gg/YOUR_INVITE_CODE )

</div>

  


---
<p align="center">· · ── ·· ─── ·· ── ·· 🔥 ·· ── ·· ─── ·· ── ··</p>

### 🍊 Boas-vindas à Cozinha da Marmalade!

A palavra "marmalade" pode até ser inglesa, mas a origem dela é a nossa "marmelada". Inspirada nessa mistura cultural, a **Marmalade.js** é uma biblioteca 100% brasileira para criar bots de Discord com um sabor diferente.

Feita artesanalmente, nossa receita mistura os melhores ingredientes da API do Discord (REST e Gateway) em uma camada de abstração deliciosa e fácil de usar. Chega de código sem graça! A gente acredita que programar deve ser uma experiência criativa e divertida.

  


## 📜 Sumário

*   [Por que Marmalade.js?](#-por-que-marmaladejs)
*   [Recursos Principais](#-recursos-principais)
*   [Instalação](#-instalação)
*   [Exemplo de Uso](#-exemplo-de-uso)
*   [Como Contribuir](#-como-contribuir)
*   [Licença](#-licença)

<p align="center">· · ── ·· ─── ·· ── ·· 🔥 ·· ── ·· ─── ·· ── ··</p>

## 🤔 Por que Marmalade.js?

Em um ecossistema com gigantes como o Discord.js, por que criar uma nova biblioteca?

*   **🎓 Aprendizado:** Este projeto nasceu como uma jornada de aprendizado profundo sobre a API do Discord, WebSockets e o design de bibliotecas.
*   **✨ Simplicidade:** Buscamos uma sintaxe mais limpa e uma abordagem direta, inspirada na fluidez de bibliotecas como o Baileys.
*   **🚀 Performance:** Sendo leve e modular, a Marmalade.js visa entregar a melhor performance possível, carregando apenas o que for usar.
*   **🇧🇷 Identidade Brasileira:** Queremos criar uma ferramenta com a cara da nossa comunidade de desenvolvedores.

  


## ✨ Recursos Principais

*   **Feita no Brasil:** Pensada e criada por e para a comunidade BR.
*   **Leve e Rápida:** Arquitetura focada em não carregar funcionalidades desnecessárias.
*   **Tipagem Forte:** Totalmente escrita em TypeScript para um desenvolvimento mais seguro.
*   **Abstração Completa:** Cobertura tanto da API REST quanto do Gateway do Discord.

  


## 🚀 Instalação

Para adicionar a Marmalade.js ao seu projeto, utilize seu gerenciador de pacotes preferido:

```bash
# Com NPM
npm install @anonimusofficial/marmalade

# Com Yarn
yarn add @anonimusofficial/marmalade

# Com PNPM
pnpm add @anonimusofficial/marmalade
💡 Exemplo de Uso
O processo é simples: crie o cliente, ouça os eventos e envie suas mensagens.
JavaScript
// 1. Importe a função de criação da sua biblioteca
const { createMarmalade } = require('@anonimusofficial/marmalade');

// 2. Crie a instância do bot, passando o token e intents
const bot = createMarmalade({
  token: 'SEU_TOKEN_AQUI',
  intents: 513 // GUILDS + GUILD_MESSAGES
});

// 3. Registre os eventos que você quer ouvir
bot.on('boot', (readyData) => {
  console.log(`Marmalade.js no ar! Logado como: ${readyData.user.username}`);
});

bot.on('message', async (message) => {
  if (message.author.bot) return;

  if (message.content === '!ping') {
    await bot.send(message.channel_id, 'Pong! 🏓');
  }
});

// 4. Inicie a conexão
bot.start();
🤝 Como Contribuir
Este é um projeto de código aberto e toda ajuda é bem-vinda. Se você tem ideias, sugestões ou quer reportar um bug, sinta-se à vontade para:
Abrir uma Issue para discutir a mudança.
Fazer um Fork do repositório.
Criar uma nova Branch (git checkout -b feat/sua-feature).
Fazer o Commit das suas mudanças (git commit -m 'feat: Adiciona sua feature').
Enviar o Push para a sua Branch (git push origin feat/sua-feature).
Abrir um Pull Request.
📝 Licença
Distribuído sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.
<p align="center">· · ── ·· ─── ·· ── ·· 🔥 ·· ── ·· ─── ·· ── ··</p> <div align="center"> Feito com ❤️‍🔥 por Anonimus Ofc no Brasil </div> ```
