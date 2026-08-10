<div align="center">

<img src="https://i.ibb.co/zhG7Lysx/file-000000003b2c820ea3fc8c2e6e060d88.png" alt="PWEB Group Help Bot" width="160" style="border-radius:50%"/>

# PWEB GROUP HELP BOT

**PWEB significa Painel Web. “PWEB Group Help Bot” e “Painel Web Group Help
Bot” são nomes do mesmo produto único**, formado pelo bot do Telegram e pelo
Painel Web de administração.

**Plataforma completa para administração de grupos do Telegram — bot modular,
bilíngue e Painel Web integrado.**

[![Telegram](https://img.shields.io/badge/Plataforma-Telegram-2CA5E0?style=flat-square&logo=telegram&logoColor=white)](https://telegram.org)
[![Proteção](https://img.shields.io/badge/Proteção-Anti--spam%20%7C%20Captcha%20%7C%20Anti--flood-EC4899?style=flat-square)]()
[![Painel](https://img.shields.io/badge/Painel-Web-6366F1?style=flat-square)]()
[![i18n](https://img.shields.io/badge/Idiomas-pt__BR%20%7C%20en__US-10B981?style=flat-square)]()

</div>

---

## 📋 Sumário

1. [O que é o bot](#-o-que-é-o-bot)
2. [Problemas que resolve](#-problemas-que-resolve)
3. [Funcionalidades principais](#-funcionalidades-principais)
4. [Como adicionar ao grupo](#-como-adicionar-ao-grupo)
5. [Comandos disponíveis](#-comandos-disponíveis)
6. [Exemplos de uso](#-exemplos-de-uso)
7. [Painel Web](#-painel-web)
8. [Perguntas frequentes](#-perguntas-frequentes)
9. [Links úteis](#-links-úteis)

---

## 🤖 O que é o PWEB Group Help Bot

O **PWEB Group Help Bot** é um único produto de administração e operação de
comunidades no Telegram. O nome PWEB significa **Painel Web**, mas o produto
não é apenas uma tela web: ele reúne o bot que atua dentro dos grupos e o
Painel Web que centraliza a operação.

Com suporte a **português e inglês**, o bot cobre desde ações básicas como ban e mute até proteções automáticas contra flood, spam, CAPTCHA e raids. Todas as configurações ficam salvas por grupo e podem ser ajustadas a qualquer momento pelo menu interativo `/config`.

O Painel Web é parte do mesmo PWEB Group Help Bot. Juntos, bot e painel
permitem visualizar e gerenciar bans, advertências, notas, estatísticas,
grupos e recursos ativos sem depender apenas de comandos no Telegram.

---

## 🎯 Problemas que resolve

| Problema | Como o bot resolve |
|---|---|
| Spam de links e mensagens repetidas | AntiSpam automático com penalidades configuráveis |
| Entrada em massa de usuários (raids) | AntiRaid detecta pico de entradas e ativa modo de proteção |
| Flood de mensagens | Flood control com limite de mensagens por janela de tempo |
| Bots e contas suspeitas entrando | CAPTCHA configurável (botão, pergunta e resposta, matemática, chave, regras ou emoji) antes de poder falar |
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
- **Captcha** — exige que novos membros completem um desafio antes de poder enviar mensagens; suporta botão, pergunta e resposta, matemática, chave alfanumérica, aceitação das regras e emoji
- **Modo Aprovação** — novos membros ficam silenciados até um admin aprovar manualmente a entrada

### ⚖️ Moderação

- **Ban / Unban** — ban permanente, temporário (`/tban`) ou silencioso (`/sban`)
- **Kick** — expulsa sem banir
- **Mute / Unmute** — silencia usuário permanentemente, por tempo (`/tmute`) ou todos de uma vez (`/muteall`)
- **Advertências** — sistema de warns com limite configurável; exibe histórico por usuário

### 📂 Organização do grupo

- **Notas** — salva respostas prontas acessíveis por `#hashtag` ou `/get`
- **Regras** — define e exibe as regras do grupo com `/rules`
- **Boas-vindas e Adeus** — mensagens personalizadas ao entrar e sair; boas-vindas suportam texto, foto, áudio, botão URL e variáveis como nome do usuário
- **Auto-delete** — configura em quanto tempo o bot apaga suas próprias mensagens (0 / 15 / 30 / 60 minutos)
- **Filtros** — reage automaticamente a palavras ou frases com uma resposta definida pelo admin
- **Locks** — bloqueia tipos de conteúdo no grupo (fotos, vídeos, links, menções, etc.)

### 🌐 Federações

- Agrupe múltiplos grupos em uma federação
- Um ban em qualquer grupo da federação vale para todos os outros
- Gerencie a lista de bans federados via `/fedinfo`

### 📊 Estatísticas

- `/stats` — total de mensagens e atividade no grupo
- `/top` — leaderboard semanal de XP; use `/top mensagens` para o ranking bruto de mensagens
- `/rank` — ranking com filtros de período e posição pessoal

### 🎮 Engajamento

- **XP e níveis** — progressão por atividade válida com anti-farm, cooldown e limite diário
- **Ranking** — Top 10 por período, posição pessoal e snapshots de ranking
- **Conquistas / Badges** — conquistas plugáveis por evento com desbloqueio idempotente
- **Streak de atividade** — sequência diária por grupo com timezone configurável
- **Pergunta do Dia** — pergunta agendada com botões/replies e participação única
- **Quiz / Trivia** — rodadas com alternativas inline, timeout e pontuação idempotente
- **Duelo / Desafios** — convite, aceite exclusivo, rodadas, placar e resultado
- **Reputação Social** — ledger separado de XP, limites anti-fraude e auditoria
- **Perfil Social** — `/perfil` e `/me` agregam métricas sem duplicar dados
- **Missões Diárias** — objetivos diários por eventos semânticos, progresso deduplicado e recompensa única
- **Enquetes Automáticas** — polls nativas do Telegram com scheduler, métricas e lock
- **Roleta / Sorteio** — sorteios gratuitos com botão participar, participante único, congelamento e auditoria
- **Aniversários** — cadastro por grupo e lembrete automático idempotente
- **Match / Amizade** — convite inline com aceite exclusivo e expiração
- **Estatísticas pessoais** — `/mystats` e `/minhasstats` consolidam métricas oficiais do usuário

### 💾 Backup

- `/backup` — exporta as configurações do grupo para um arquivo
- `/restore` — restaura configurações a partir de um backup anterior

### ⚙️ Configuração interativa

O comando `/config` abre um menu com botões inline para ajustar todas as opções do grupo sem precisar memorizar parâmetros:

- Configurar mensagens de boas-vindas e adeus
- Adicionar foto, áudio e botão URL na mensagem de boas-vindas
- Ajustar regras e tempo de auto-delete
- Configurar Anti-Spam com menus de dois níveis (ação, duração, exceções)
- Configurar encaminhamento de mensagens de canais, grupos, usuários e bots

### 🌍 Bilíngue

O bot mantém cobertura bilíngue ampla em **pt_BR** e **en_US**. O idioma pode ser definido globalmente ou individualmente por usuário — cada um vê as respostas do bot no seu próprio idioma.

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

A lista abaixo reúne os principais comandos operacionais. O catálogo completo pode ser consultado diretamente no Telegram com `/commands` ou `/help`.

### Comandos gerais

| Comando | O que faz | Quem pode usar |
|---|---|---|
| `/start` | Exibe a mensagem de boas-vindas do bot | Todos |
| `/info` | Exibe informações técnicas e contagens do bot | Todos |
| `/help` | Lista todos os comandos disponíveis | Todos |
| `/commands` | Catálogo paginado de comandos por categoria | Todos |
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

> **Como usar:** responda à mensagem do usuário, passe o ID numérico ou use `@usuario` quando o bot já conhece esse usuário no grupo. Exemplo: `/ban @fulano Spam`.

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
| `/clear <quantidade>` ou em resposta | Remove mensagens recentes do chat | Administrador |
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
| `/captcha on\|off\|button\|qa\|math\|key\|rules\|emoji` | Configura o CAPTCHA para novos membros | Administrador |
| `/antispam on\|off` | Ativa ou desativa o anti-spam | Administrador |
| `/antiraid on\|off\|<N>` | Configura o modo anti-raid | Administrador |
| `/approval on\|off` | Ativa o modo de aprovação manual | Administrador |
| `/approve` | Aprova um membro no modo aprovação | Administrador |
| `/deny` | Rejeita (bane) um membro no modo aprovação | Administrador |

### Produtividade e suporte

| Comando | O que faz | Quem pode usar |
|---|---|---|
| `/msgbuilder` | Abre o assistente de criação de mensagens | Administrador |
| `/copymsg` | Copia uma mensagem para o Message Builder | Administrador |
| `/msglist` | Lista templates salvos do Message Builder | Administrador |
| `/msgload <nome>` | Carrega um template salvo do Message Builder | Administrador |
| `/msgdelete <nome>` | Remove um template salvo do Message Builder | Administrador |

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
| `/top [período]` | Leaderboard de XP, semanal por padrão | Todos |
| `/top mensagens` | Ranking bruto de mensagens | Todos |
| `/rank` | Ranking de engajamento com filtros de período | Todos |
| `/player` | Perfil de XP, nível e coins | Todos |
| `/coins` | Mostra carteira global de coins | Todos |
| `/badges` | Mostra conquistas desbloqueadas | Todos |
| `/streak` | Mostra sequência diária de atividade | Todos |
| `/dailyquestion` | Gerencia ou publica Pergunta do Dia | Administrador |
| `/quiz` | Inicia uma rodada de Quiz / Trivia | Todos |
| `/duelo` | Cria desafio entre usuários | Todos |
| `/rep` ou `/reputacao` | Dá ou consulta reputação social | Todos |
| `/perfil` | Abre Perfil Social com abas inline | Todos |
| `/missoes` | Mostra Missões Diárias | Todos |
| `/enquetes` | Configura Enquetes Automáticas | Administrador |
| `/sorteio` | Cria, consulta ou encerra sorteios gratuitos | Administrador |
| `/aniversario` | Cadastra, remove ou consulta aniversário | Todos |
| `/amizade` | Envia convite de amizade por reply ou alvo conhecido | Todos |
| `/mystats` ou `/minhasstats` | Mostra estatísticas pessoais consolidadas | Todos |
| `/backup` | Exporta as configurações do grupo | Administrador |
| `/restore` | Restaura configurações a partir de um backup | Administrador |

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
/captcha emoji
```
Novos membros ficam mutados ao entrar e precisam resolver o desafio configurado antes de poder enviar mensagens. Após o acerto, o mute é removido e a mensagem de boas-vindas é enviada.

### Definir limite de flood

```
/setflood 5
/setfloodmode mute
```
Se alguém enviar mensagens repetidas ou em excesso acima do limite configurado na janela atual, o módulo aplica a ação configurada.

### Ver seu progresso no grupo

```
/perfil
/rank
/missoes
```
Esses comandos mostram perfil social, posição no ranking e missões diárias sem duplicar mensagens desnecessárias no grupo.

### Criar um sorteio gratuito

```
/sorteio criar 30m Livro do grupo
```
O bot publica um botão de participação, congela os inscritos no encerramento e registra o vencedor para auditoria.

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

## 🖥️ Painel Web Group Help Bot

O **Painel Web Group Help Bot** é a interface web do produto PWEB Group Help
Bot. Ele permite acompanhar e administrar os grupos em uma tela centralizada,
sem tratar o painel como um produto separado do bot.

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
| **Recursos** | Proteções e recursos ativos no bot |

### Como acessar

O endereço e as credenciais de acesso ao painel são fornecidos pelo responsável
pela instalação do bot.

---

## ❓ Perguntas frequentes

**O bot funciona em canais?**  
Não. O bot é projetado exclusivamente para grupos do Telegram. Canais têm uma estrutura diferente e não suportam o mesmo modelo de moderação.

**Preciso deixar o computador ligado para o bot funcionar?**  
Sim — o bot precisa estar em execução contínua em algum servidor ou dispositivo. Para uso em produção, recomenda-se manter o bot em uma infraestrutura estável.

**O bot salva histórico de mensagens?**  
Não. O bot salva apenas dados operacionais: bans, mutes, warns, notas, configurações e estatísticas de contagem de mensagens. O conteúdo das mensagens não é armazenado.

**O que acontece se o bot ficar offline por um tempo?**  
Mensagens enviadas enquanto o bot estava offline não são processadas. O bot retoma normalmente quando volta a ficar online.

**Posso usar o bot em vários grupos ao mesmo tempo?**  
Sim. Uma única instância do bot pode gerenciar quantos grupos quiser. Cada grupo tem suas configurações independentes.

**Quando posso usar comandos com @username?**
Quando o bot já identificou o usuário no grupo. Isso acontece quando a pessoa entra, envia mensagem, clica em botão, é mencionada diretamente ou aparece em eventos de membro do Telegram. Se o usuário nunca foi visto pelo bot, use reply ou ID numérico.

**O que é uma federação?**  
Uma federação é um conjunto de grupos vinculados. Um ban federado (`/fban`) remove o usuário de todos os grupos da federação de uma só vez, útil para combater spammers que atuam em múltiplos grupos.

**O bot suporta português?**  
Sim. Todas as respostas do bot estão disponíveis em **português (pt_BR)** e **inglês (en_US)**. O idioma é configurável globalmente ou por usuário individualmente.

**Perdi as configurações do grupo. Tem como recuperar?**  
Se você tiver feito um `/backup` anteriormente, use `/restore` para restaurar. Por isso, é recomendado fazer backup das configurações periodicamente.

**Como o anti-spam funciona?**  
O módulo AntiSpam verifica mensagens contra CAS, links do Telegram, encaminhamento, citação, repetição e outras regras configuradas pelo administrador no `/config`.

**O captcha é obrigatório?**  
Não, é opcional. Quando ativado com `/captcha on`, novos membros entram mutados e precisam completar o método configurado antes de falar. Os métodos atuais incluem botão, pergunta e resposta, matemática, chave alfanumérica, aceitação das regras e emoji.

**Os recursos de engajamento premiam spam?**
Não. XP, missões e ranking usam atividade válida, cooldown, teto diário e eventos idempotentes para evitar recompensa duplicada ou incentivo a flood.

---

## 🔗 Links úteis

- **Telegram:** [telegram.org](https://telegram.org)
- **Descobrir seu ID:** envie qualquer mensagem para [@userinfobot](https://t.me/userinfobot)
- **CAS (Combot Anti-Spam):** [cas.chat](https://cas.chat)

---
