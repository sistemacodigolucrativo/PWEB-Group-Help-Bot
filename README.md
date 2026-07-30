<div align="center">

<img src="https://i.ibb.co/8g7S547H/file-00000000fc5c820eb17eb98f55a140c6.png" alt="PWEB Group Help Bot" width="480" style="border-radius:50%"/>

**Bot de Telegram completo para administração de grupos — modular, bilíngue e com painel web.**

[![Telegram](https://img.shields.io/badge/Plataforma-Telegram-2CA5E0?style=flat-square&logo=telegram&logoColor=white)](https://telegram.org)
[![Módulos](https://img.shields.io/badge/Módulos-28-EC4899?style=flat-square)]()
[![Comandos](https://img.shields.io/badge/Comandos-60+-6366F1?style=flat-square)]()
[![i18n](https://img.shields.io/badge/Idiomas-pt__BR%20%7C%20en__US-10B981?style=flat-square)]()
[![Licença](https://img.shields.io/badge/Licença-MIT-F59E0B?style=flat-square)](LICENSE)

</div>

---

## 📋 Sumário

1. [O que é o bot](#-o-que-é-o-bot)
2. [Problemas que resolve](#-problemas-que-resolve)
3. [Funcionalidades principais](#-funcionalidades-principais)
4. [Como adicionar ao grupo](#-como-adicionar-ao-grupo)
5. [Comandos disponíveis](#-comandos-disponíveis)
6. [Exemplos de uso](#-exemplos-de-uso)
7. [Painel Web WATCHTOWER](#-painel-web-watchtower)
8. [Perguntas frequentes](#-perguntas-frequentes)
9. [Links úteis](#-links-úteis)

---

## 🤖 O que é o bot

O **PWEB Group Help Bot** é um bot de administração completo para grupos do Telegram. Ele reúne em um único lugar todas as ferramentas que um administrador precisa para manter o grupo organiz[...]

Com **28 módulos independentes**, **60+ comandos** e suporte a **português e inglês**, o bot cobre desde ações básicas como ban e mute até proteções automáticas contra flood, spam e raid[...]

Além disso, há um **painel web (WATCHTOWER)** que permite visualizar e gerenciar tudo pelo navegador — banimentos, advertências, notas, estatísticas e grupos — sem precisar digitar comando[...]

---

## 🎯 Problemas que resolve

| Problema | Como o bot resolve |
|---|---|
| Spam de links e mensagens repetidas | AntiSpam automático com penalidades configuráveis |
| Entrada em massa de usuários (raids) | AntiRaid detecta pico de entradas e ativa modo de proteção |
| Flood de mensagens | Flood control com limite de mensagens por janela de tempo |
| Bots e contas suspeitas entrando | Captcha obrigatório (botão, matemática ou texto) antes de poder falar |
| Dificuldade de coordenar múltiplos admins | Painel web centralizado com visão geral em tempo real |
| Perda de configurações ao trocar de bot | Sistema de backup e restauração das configurações do grupo |
| Usuários problemáticos em vários grupos | Federações: um ban vale para todos os grupos federados |
| Sem controle de quem entra | Modo aprovação: admin precisa aprovar cada novo membro |
| Mensagens de boas-vindas sem controle | Auto-delete configurável para welcome, goodbye e regras |

---

## ✨ Funcionalidades principais

### 🛡️ Proteção automática

- **Anti-Spam** — detecta e penaliza links excessivos, mensagens repetidas e conteúdo do CAS (Combot Anti-Spam)
- **Anti-Raid** — identifica pico de entradas e ativa modo raid automaticamente
- **Flood Control** — define limite de mensagens por janela de tempo; ação configurável (warn / mute / kick / ban)
- **Captcha** — exige que novos membros completem um desafio antes de poder enviar mensagens (botão clicável, conta matemática ou texto digitado)
- **Modo Aprovação** — novos membros ficam silenciados até um admin aprovar manualmente a entrada

### ⚖️ Moderação

- **Ban / Unban** — ban permanente, temporário (`/tban`) ou silencioso (`/sban`)
- **Kick** — expulsa sem banir
- **Mute / Unmute** — silencia usuário permanentemente, por tempo (`/tmute`) ou todos de uma vez (`/muteall`)
- **Advertências** — sistema de warns com limite configurável; exibe histórico por usuário

### 📂 Organização do grupo

- **Notas** — salva respostas prontas acessíveis por `#hashtag` ou `/get`
- **Regras** — define e exibe as regras do grupo com `/rules`
- **Boas-vindas e Adeus** — mensagens personalizadas ao entrar e sair; suporta variáveis como nome do usuário
- **Auto-delete** — configura em quanto tempo o bot apaga suas próprias mensagens (0 / 15 / 30 / 60 minutos)
- **Filtros** — reage automaticamente a palavras ou frases com uma resposta definida pelo admin
- **Locks** — bloqueia tipos de conteúdo no grupo (fotos, vídeos, links, menções, etc.)

### 🌐 Federações

- Agrupe múltiplos grupos em uma federação
- Um ban em qualquer grupo da federação vale para todos os outros
- Gerencie a lista de bans federados via `/fedinfo`

### 📊 Estatísticas

- `/stats` — total de mensagens e atividade no grupo
- `/top` — ranking de usuários mais ativos

### 💾 Backup

- `/backup` — exporta as configurações do grupo para um arquivo
- `/restore` — restaura configurações a partir de um backup anterior

### ⚙️ Configuração interativa

O comando `/config` abre um menu com botões inline para ajustar todas as opções do grupo sem precisar memorizar parâmetros:

- Configurar mensagens de boas-vindas e adeus
- Ajustar regras e tempo de auto-delete
- Configurar Anti-Spam com menus de dois níveis (ação, duração, exceções)
- Configurar encaminhamento de mensagens de canais, grupos, usuários e bots

### 🌍 Bilíngue

Todos os 28 módulos têm suporte completo a **pt_BR** e **en_US**. O idioma pode ser definido globalmente ou individualmente por usuário — cada um vê as respostas do bot no seu próprio idioma.

---

## ➕ Como adicionar ao grupo

1. Abra o grupo no Telegram
2. Vá em **Configurações → Administradores → Adicionar Administrador**
3. Busque pelo bot e adicione-o
4. Conceda as permissões necessárias:
   - Banir usuários
   - Apagar mensagens
   - Fixar mensagens
   - Adicionar membros *(opcional, apenas para uso do /kick)*

> O bot só age em grupos onde é administrador. Sem permissão de administrador, os comandos de moderação não funcionam.

Após adicionado, use `/help` para ver a lista completa de comandos disponíveis no grupo.

---

## 💬 Comandos disponíveis

### Comandos gerais

| Comando | O que faz | Quem pode usar |
|---|---|---|
| `/start` | Exibe a mensagem de boas-vindas do bot | Todos |
| `/help` | Lista todos os comandos disponíveis | Todos |
| `/adminlist` | Exibe a lista de administradores do grupo | Todos |

### Moderação

| Comando | O que faz | Quem pode usar |
|---|---|---|
| `/ban` | Bane um usuário permanentemente | Administrador |
| `/tban <duração>` | Ban temporário (ex.: `1h`, `2d`, `1w`) | Administrador |
| `/unban` | Remove o ban de um usuário | Administrador |
| `/sban` | Ban silencioso — sem mensagem de notificação | Administrador |
| `/banme` | Auto-ban — o próprio usuário se bane | Todos |
| `/kick` | Expulsa o usuário sem banir | Administrador |
| `/kickme` | Auto-kick | Todos |
| `/mute` | Silencia um usuário permanentemente | Administrador |
| `/tmute <duração>` | Silencia por tempo determinado | Administrador |
| `/unmute` | Remove o silêncio | Administrador |
| `/muteall` | Silencia todos os não-admins | Administrador |
| `/warn` | Dá uma advertência ao usuário | Administrador |
| `/unwarn` | Remove a última advertência | Administrador |
| `/resetwarn` | Zera todas as advertências | Administrador |
| `/warns` | Mostra as advertências de um usuário | Todos |

> **Como usar:** responda à mensagem do usuário com o comando, ou passe `@usuario` ou o ID como argumento. Exemplo: `/ban @fulano Spam`.

### Configuração do grupo

| Comando | O que faz | Quem pode usar |
|---|---|---|
| `/config` | Abre o painel de configuração com botões | Administrador |
| `/setrules <texto>` | Define as regras do grupo | Administrador |
| `/rules` | Exibe as regras do grupo | Todos |
| `/clearrules` | Remove as regras | Administrador |
| `/welcome on\|off\|msg` | Ativa, desativa ou define a mensagem de boas-vindas | Administrador |
| `/goodbye on\|off\|msg` | Ativa, desativa ou define a mensagem de saída | Administrador |
| `/cleanwelcome on\|off` | Apaga automaticamente a mensagem de boas-vindas anterior | Administrador |

### Organização

| Comando | O que faz | Quem pode usar |
|---|---|---|
| `/save <nome> <resposta>` | Salva uma nota com o nome dado | Administrador |
| `/get <nome>` ou `#nome` | Recupera uma nota salva | Todos |
| `/notes` | Lista todas as notas salvas | Todos |
| `/clear <nome>` | Remove uma nota | Administrador |
| `/filter <palavra> <resposta>` | Cria um filtro automático | Administrador |
| `/stop <palavra>` | Remove um filtro | Administrador |
| `/filters` | Lista os filtros ativos | Todos |
| `/lock <tipo>` | Bloqueia um tipo de conteúdo | Administrador |
| `/unlock <tipo\|all>` | Desbloqueia conteúdo | Administrador |
| `/locks` | Lista os bloqueios ativos | Todos |
| `/report` | Reporta uma mensagem aos admins | Todos |
| `/pin` / `/unpin` | Fixa ou desfixta mensagem | Administrador |

### Proteção automática

| Comando | O que faz | Quem pode usar |
|---|---|---|
| `/setflood <N>` | Define o limite de mensagens antes da ação | Administrador |
| `/setfloodmode <ação>` | Define a ação do flood (warn/mute/kick/ban) | Administrador |
| `/flood` | Mostra a configuração atual do flood | Todos |
| `/captcha on\|off\|button\|math\|text` | Configura o captcha para novos membros | Administrador |
| `/antispam on\|off` | Ativa ou desativa o anti-spam | Administrador |
| `/antiraid on\|off\|<N>` | Configura o modo anti-raid | Administrador |
| `/approval on\|off` | Ativa o modo de aprovação manual | Administrador |
| `/approve` | Aprova um membro no modo aprovação | Administrador |
| `/deny` | Rejeita (bane) um membro no modo aprovação | Administrador |

### Federações

| Comando | O que faz | Quem pode usar |
|---|---|---|
| `/newfed <nome>` | Cria uma nova federação | Administrador |
| `/joinfed <id>` | Adiciona o grupo a uma federação | Administrador |
| `/leavefed` | Remove o grupo da federação | Administrador |
| `/fban` | Bane o usuário em todos os grupos da federação | Administrador |
| `/unfban` | Remove o ban federado | Administrador |
| `/fedinfo` | Exibe informações da federação | Todos |

### Avançado

| Comando | O que faz | Quem pode usar |
|---|---|---|
| `/stats` | Estatísticas de mensagens do grupo | Todos |
| `/top` | Ranking de usuários mais ativos | Todos |
| `/backup` | Exporta as configurações do grupo | Administrador |
| `/restore` | Restaura configurações a partir de um backup | Administrador |
| `/restart` | Reinicia o bot | Owner |
| `/exit` | Remove o bot do grupo | Owner |

---

## 📖 Exemplos de uso

### Banir um usuário por spam

Responda à mensagem do spammer com:
```
/ban Spam
```
O usuário é banido e uma notificação é enviada no grupo.

### Ban temporário de 24 horas

```
/tban 1d Comportamento inadequado
```

### Criar um filtro automático

```
/filter link http://exemplo.com Não envie links externos.
```
A partir de agora, sempre que alguém enviar "link", o bot responde automaticamente com a mensagem definida.

### Salvar e recuperar uma nota

```
/save regras Leia as regras em /rules antes de participar.
```
Qualquer membro pode recuperar com `/get regras` ou escrevendo `#regras`.

### Configurar captcha obrigatório

```
/captcha math
```
Novos membros precisam resolver uma conta simples antes de poder enviar mensagens.

### Definir limite de flood

```
/setflood 5
/setfloodmode mute
```
Se alguém enviar mais de 5 mensagens seguidas, será silenciado automaticamente.

### Configurar boas-vindas com auto-delete

1. Use `/welcome msg Bem-vindo ao grupo, {first_name}!` para definir a mensagem
2. Acesse `/config → Boas-vindas → ⏰ Exibição → 15 min`

A mensagem será apagada automaticamente após 15 minutos.

### Criar uma federação e banir em todos os grupos

```
/newfed MeusBots
```
No segundo grupo:
```
/joinfed <ID da federação>
```
Agora, em qualquer grupo da federação:
```
/fban @spammer
```
O usuário é banido em todos os grupos ao mesmo tempo.

---

## 🖥️ Painel Web WATCHTOWER

O WATCHTOWER é a interface web do bot — um painel que roda localmente junto com o bot e permite gerenciar tudo pelo navegador, sem precisar digitar comandos no Telegram.

### O que você encontra no painel

| Página | Conteúdo |
|---|---|
| **Command Center** | Visão geral com contagens e atividade recente |
| **Grupos** | Lista de todos os grupos gerenciados |
| **Banimentos** | Histórico de bans com opção de remoção |
| **Advertências** | Lista de warns com opção de remoção |
| **Notas** | Notas salvas por grupo com opção de remoção |
| **Estatísticas** | Gráficos de mensagens e ranking de usuários ativos |
| **FedBans** | Bans de federação ativos |
| **Módulos** | Módulos carregados e ativos no bot |

### Como acessar

O painel roda no mesmo servidor que o bot. O endereço de acesso depende de onde o bot está instalado:

| Instalação | Endereço |
|---|---|
| Celular (Termux) | `http://localhost:3000` |
| VPS / Linux | `http://<IP do servidor>:3000` |
| Windows / macOS (local) | `http://localhost:3000` |

Na tela de login, insira o **token do painel** (`PUBLIC_API_TOKEN`) configurado durante a instalação e clique em **Enter command center**.

---

## ❓ Perguntas frequentes

**O bot funciona em canais?**  
Não. O bot é projetado exclusivamente para grupos do Telegram. Canais têm uma estrutura diferente e não suportam o mesmo modelo de moderação.

**Preciso deixar o computador ligado para o bot funcionar?**  
Sim — o bot precisa estar em execução contínua em algum servidor ou dispositivo (VPS, Termux no celular, computador ligado). Plataformas como VPS são recomendadas para uso em produção.

**O bot salva histórico de mensagens?**  
Não. O bot salva apenas dados operacionais: bans, mutes, warns, notas, configurações e estatísticas de contagem de mensagens. O conteúdo das mensagens não é armazenado.

**O que acontece se o bot ficar offline por um tempo?**  
Mensagens enviadas enquanto o bot estava offline não são processadas. O bot retoma normalmente quando volta a ficar online.

**Posso usar o bot em vários grupos ao mesmo tempo?**  
Sim. Uma única instância do bot pode gerenciar quantos grupos quiser. Cada grupo tem suas configurações independentes.

**O que é uma federação?**  
Uma federação é um conjunto de grupos vinculados. Um ban federado (`/fban`) remove o usuário de todos os grupos da federação de uma só vez, útil para combater spammers que atuam em múlti[...]

**O bot suporta português?**  
Sim. Todas as respostas do bot estão disponíveis em **português (pt_BR)** e **inglês (en_US)**. O idioma é configurável globalmente ou por usuário individualmente.

**Perdi as configurações do grupo. Tem como recuperar?**  
Se você tiver feito um `/backup` anteriormente, use `/restore` para restaurar. Por isso, é recomendado fazer backup das configurações periodicamente.

**Como o anti-spam funciona?**  
O módulo AntiSpam verifica cada mensagem contra três critérios: presença na base do CAS (Combot Anti-Spam), quantidade excessiva de links e repetição de mensagens idênticas. Você configur[...]

**O captcha é obrigatório?**  
Não, é opcional. Quando ativado com `/captcha on`, novos membros precisam completar o desafio configurado antes de poder enviar mensagens. Há três tipos: botão clicável, conta matemática o[...]

---

## 🔗 Links úteis

- **Repositório no GitHub:** [sistemacodigolucrativo/PWEB-GroupHelpBot-TG](https://github.com/sistemacodigolucrativo/PWEB-GroupHelpBot-TG)
- **Criar um bot:** fale com o [@BotFather](https://t.me/BotFather) no Telegram
- **Descobrir seu ID:** envie qualquer mensagem para [@userinfobot](https://t.me/userinfobot)
- **CAS (Combot Anti-Spam):** [cas.chat](https://cas.chat)

---

<div align="center">

MIT License — veja o arquivo [LICENSE](LICENSE) para detalhes.

</div>
