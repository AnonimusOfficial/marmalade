
```markdown
<div align="center">

# ✠ Marmalade.js ✠

**Uma biblioteca forjada em Node.js para a API do Discord.** <br />
*Desenvolvida por Anonimus Ofc.*

</div>

<div align="center">

[![Versão](https://img.shields.io/npm/v/@anonimusofficial/marmalade?style=for-the-badge&color=9B0000&labelColor=000000)](https://www.npmjs.com/package/@anonimusofficial/marmalade)
[![Licença](https://img.shields.io/github/license/anonimusofficial/marmalade.js?style=for-the-badge&color=4C0070&labelColor=000000)](https://github.com/anonimusofficial/marmalade.js/blob/main/LICENSE)
[![Comunidade](https://img.shields.io/discord/YOUR_SERVER_ID?style=for-the-badge&logo=discord&logoColor=white&label=Santuário&color=7E00B3&labelColor=000000)](https://discord.gg/YOUR_INVITE_CODE)

</div>

<br>

---
<p align="center">† ·· ─── ·· ── · 🦇 · ── ·· ─── ·· †</p>

### 🔮 O Grimório

Inspirada na complexidade de protocolos e na busca por uma sintaxe mais direta, a **Marmalade.js** é uma biblioteca que oferece uma nova forma de interagir com a API do Discord.

Forjada do zero, nossa estrutura combina os elementos do Gateway e da API REST em uma camada de abstração poderosa e intuitiva. Para aqueles que acreditam que programar é uma forma de arte.

<br>

### 📜 Capítulos

*   [O Propósito](#-o-propósito)
*   [Artefatos](#-artefatos)
*   [O Ritual de Instalação](#-o-ritual-de-instalação)
*   [Invocação de Exemplo](#-invocação-de-exemplo)
*   [Convocação para Contribuir](#-convocação-para-contribuir)
*   [O Pacto (Licença)](#-o-pacto-licença)

<p align="center">† ·· ─── ·· ── · 🦇 · ── ·· ─── ·· †</p>

### 🕯️ O Propósito

Em um mundo com ferramentas já estabelecidas, por que conjurar uma nova?

*   **Alquimia do Conhecimento:** Este projeto é uma jornada de aprendizado profundo sobre a API do Discord, WebSockets e o design de bibliotecas.
*   **Essência da Simplicidade:** Buscamos uma sintaxe mais limpa e uma abordagem direta para tarefas comuns.
*   **Poder e Performance:** Sendo leve e modular, a Marmalade.js visa entregar a melhor performance, utilizando apenas os recursos necessários.
*   **Identidade Própria:** Criar uma ferramenta com uma assinatura única.

<br>

### 🦇 Artefatos

*   **Forjada do Zero:** Arquitetura própria, sem dependências de outras bibliotecas de Discord.
*   **Leve e Rápida:** Focada em não carregar funcionalidades desnecessárias.
*   **Poder Arcano (Tipagem):** Escrita em TypeScript para um desenvolvimento mais seguro.
*   **Domínio Completo:** Cobertura tanto da API REST quanto do Gateway.

<br>

### ➕ O Ritual de Instalação

Para obter a Marmalade.js, use seu gerenciador de pacotes preferido:

```bash
# Com NPM
npm install @anonimusofficial/marmalade

# Com Yarn
yarn add @anonimusofficial/marmalade

# Com PNPM
pnpm add @anonimusofficial/marmalade
```

<br>

### ✒️ Invocação de Exemplo

O processo é direto: crie o cliente, ouça os eventos e execute as ações.

```javascript
// 1. Importe a função de criação da biblioteca
const { createMarmalade } = require('@anonimusofficial/marmalade');

// 2. Crie a instância do bot, passando o token e as permissões (intents)
const bot = createMarmalade({
  token: 'SEU_TOKEN_AQUI',
  intents: 513 // Permissão para ver servidores e ler mensagens
});

// 3. Registre os eventos que deseja observar
bot.on('boot', (readyData) => {
  console.log(`O ritual foi concluído. Logado como: ${readyData.user.username}`);
});

bot.on('message', async (message) => {
  // Ignora ecos de outros bots
  if (message.author.bot) return;

  // Responde ao chamado '!ping'
  if (message.content === '!ping') {
    await bot.send(message.channel_id, 'Pong. 🦇');
  }
});

// 4. Inicie a conexão
bot.start();
```

<br>

### ♆ Convocação para Contribuir

Este é um projeto de código aberto. Toda ajuda é bem-vinda. Se você tem ideias, sugestões ou quer reportar um bug, sinta-se à vontade para:

1.  Abrir uma **Issue** para discutir a mudança.
2.  Fazer um **Fork** do repositório.
3.  Criar uma nova **Branch** (`git checkout -b feat/sua-feature`).
4.  Fazer o **Commit** de suas mudanças (`git commit -m 'feat: Adiciona sua feature'`).
5.  Enviar o **Push** para a sua Branch (`git push origin feat/sua-feature`).
6.  Abrir um **Pull Request**.

<br>

### 📜 O Pacto (Licença)

Distribuído sob a licença **MIT**. Veja o arquivo `LICENSE` no repositório para mais detalhes.

<p align="center">† ·· ─── ·· ── · 🦇 · ── ·· ─── ·· †</p>

<div align="center">
  Forjado por Anonimus Ofc
</div>
```
