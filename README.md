# autobloqueador

Controle do Auto-Bloqueador Magnus e de quem pode usá-lo. Feito para a **Phonevox**.

Módulo do bot de Discord construído sobre o framework **sora**. Foi criado pra ser usado em cima dele: a pasta do módulo vai em `src/usermodules/` e o loader a carrega sozinho, sem registro manual.

## O que faz

Dispara a rechecagem do Auto-Bloqueador e mantém a lista de usuários autorizados, guardada no Postgres.

Comando: `autobloqueador` com os subcomandos `rechecar`, `autorizar` e `desautorizar`.

## Instalação

Clone este repositório dentro de `src/usermodules/` do seu projeto sora e reinicie o bot (ou use `!bot reload`). O nome da pasta não importa: o módulo é identificado pelo `name` do cog (`autobloqueador`).

## Variáveis de ambiente

Lidas de `process.env` e centralizadas em `settings.ts` (`modConfig`).

| Variável | Descrição |
|---|---|
| `MOD_AUTOBLOQUEADOR_URL` | Endpoint de update do Auto-Bloqueador |
| `MOD_AUTOBLOQUEADOR_TOKEN` | Bearer token do endpoint |

## Banco

As migrations rodam sozinhas no carregamento do módulo (Postgres do framework).
