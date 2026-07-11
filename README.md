<div align="center">

<img src="assets/terminal.svg" alt="cesar@multiverso — terminal" width="780">

<br>

![](https://img.shields.io/badge/5_lojas_+_CD-Minas_Gerais-2ea44f?style=for-the-badge)
![](https://img.shields.io/badge/15%2B_sistemas-em_produção-1f6feb?style=for-the-badge)
![](https://img.shields.io/badge/1.3k%2B_contributions-por_ano-8957e5?style=for-the-badge)

</div>

**Empresário & builder** — lidero a tecnologia da **Multiverso Atacado**, operação de atacado multi-filial em Minas Gerais 🇧🇷 que roda de ponta a ponta em software construído em casa.

> Eu não vendo software. Eu opero um negócio real — lojas, centro de distribuição, frota e entrega própria — com o software que eu mesmo construo. *Skin in the game* de verdade: se o sistema falha, a loja para.

## O que desenvolvo no dia a dia

- 🏗️ **ERP próprio** — do PDV ao DRE, moldado na operação real (e não o contrário)
- 🛒 **PDV próprio, offline-first** — fluxos de operação personalizados, TEF e PIX integrados no balcão
- 🏦 **Integração bancária própria** — um app que gerencia, adapta e unifica todos os bancos num contrato único
- 🌐 **Infraestrutura própria** — control-plane de deploy/DNS/VPN, lojas resilientes a queda de internet, alertas no WhatsApp
- 🤖 **IA na operação** — agentes como nós do organograma + Central de Projetos com grafo vivo de conhecimento

## A tese

O varejo é meu laboratório. **A empresa é o produto**: cada sistema nasce de uma dor real do chão de loja e é validado na operação no dia seguinte. Tecnologia aqui não é área de suporte — é o motor de margem.

> Cada feature precisa reduzir trabalho manual, reduzir dependência de qualificação, ou gerar um KPI. Senão, não entra.

## O mapa da operação

```mermaid
flowchart TB
    WPP["WhatsApp
    interface de comando da empresa"] --> IA["Agentes de IA
    nós do organograma · MCP"]
    IA --> ERP["ERP próprio
    atacado · estoque · financeiro · fiscal · DP"]
    IA --> CENTRAL["Central de Projetos
    grafo vivo: decisões · tarefas · docs"]
    PDV["PDV offline-first
    5 lojas + CD · TEF · PIX"] <--> ERP
    ERP --> BANCOS["Integração bancária
    PIX · boletos · extratos · certificado digital"]
    ERP <--> CENTRAL
    INFRA["Control-plane próprio
    deploy · VPN · DNS · monitor · backup"] -. sustenta tudo .-> ERP
    INFRA -.-> PDV
```

## Soluções que o mercado não tinha

<details>
<summary><b>🧯 Um control-plane de infraestrutura próprio — construído em uma semana</b></summary>
<br>

Quando precisamos repor nosso painel de infra, fomos ao mercado e não encontramos: uma ferramenta que juntasse **gestão de VPN da frota inteira** (lojas conectadas por túnel, roteador gerenciado), **DNS interno**, **deploy por git com rollback e cofre de variáveis**, **monitoramento com alerta no WhatsApp** e **backup** — do jeito que uma operação de varejo multi-loja precisa, sem virar um cluster complexo de manter.

Então construímos o nosso. Em uma semana a infra inteira já rodava nele. Hoje ele **se auto-deploya a cada push**, com build-gate, health-check e rollback automático — e é a tela única de operação da infraestrutura.

</details>

<details>
<summary><b>🏗️ Um ERP moldado na operação — e operável por IA</b></summary>
<br>

ERP de prateleira obriga a empresa a trabalhar do jeito do software. Invertemos: cada tela nasce de uma dor real e é validada por quem não perdoa bug — a operação. Venda de atacado com reserva de estoque em tempo real, estoque com visão fiscal × física, conciliação bancária automática, DRE do dono em tempo real, DP com geração e assinatura digital de documentos, notificação de tudo no WhatsApp.

E a parte que quase ninguém tem: o ERP expõe a operação inteira via **MCP** — agentes de IA usam o sistema com as **mesmas permissões (RBAC) de um usuário humano**. O que um gestor faz na tela, um agente faz por API. Tudo auditado.

</details>

<details>
<summary><b>🏦 Todos os bancos falando uma língua só</b></summary>
<br>

Cada banco: uma API diferente, um certificado digital, um jeito próprio de errar. Construímos um app que **gerencia, adapta e unifica** essa selva num contrato único — PIX, boletos, extratos e conciliação multi-banco, com camada própria de autenticação por certificado digital.

O ERP não sabe qual banco está do outro lado. Nem precisa.

</details>

<details>
<summary><b>🛒 Um PDV que não para — nem sem internet</b></summary>
<br>

Loja sem internet não pode parar de vender. Nosso PDV é **offline-first**: opera desconectado e sincroniza ao reconectar. Mas o motivo de existir vai além da resiliência: **fluxos de operação personalizados** que nenhum PDV de mercado oferece, **TEF e PIX integrados** direto no balcão, rastreabilidade antifraude — e um **tempo de atendimento no caixa que despencou** depois que redesenhamos o fluxo.

</details>

<details>
<summary><b>🤖 IA no organograma — e um grafo que é o cérebro da empresa</b></summary>
<br>

Agentes de IA aqui não são chatbot de FAQ: são **nós do organograma**, com papel, permissões e responsabilidade — operam o ERP via MCP como um funcionário operaria.

E tudo que acontece — decisão, tarefa, ideia, documento — vira nó de um **grafo vivo** numa Central de Projetos própria: decisões linkadas a tarefas, tarefas a código, código a conversas. Qualquer agente (ou pessoa) recupera o contexto completo da empresa em segundos. O WhatsApp fecha o ciclo como **interface de comando**: a empresa se opera por mensagem.

</details>

## Atividade

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/cesarvcanal/cesarvcanal/output/github-snake-dark.svg">
  <img alt="snake comendo o contribution graph" src="https://raw.githubusercontent.com/cesarvcanal/cesarvcanal/output/github-snake.svg">
</picture>

<sub>Tudo código de produção de uma operação real — nada de commit de enfeite.</sub>

## Stack

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![React](https://img.shields.io/badge/React-087EA4?style=for-the-badge&logo=react&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-404D59?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![WireGuard](https://img.shields.io/badge/WireGuard-88171A?style=for-the-badge&logo=wireguard&logoColor=white)
![MikroTik](https://img.shields.io/badge/MikroTik-293239?style=for-the-badge&logo=mikrotik&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)
![MCP](https://img.shields.io/badge/MCP_·_Claude-D97757?style=for-the-badge&logo=claude&logoColor=white)

---

<div align="center">
<sub>Feito em Minas Gerais · <b>tech@multiversoatacado.com</b></sub>
</div>

<details>
<summary><b>🇺🇸 English version</b></summary>
<br>

**Entrepreneur & builder** — I lead technology at **Multiverso Atacado**, a multi-branch wholesale operation in Minas Gerais, Brazil 🇧🇷 that runs end to end on software built in-house.

> I don't sell software. I run a real business — stores, a distribution center, our own fleet and delivery — on software I build myself. Real *skin in the game*: if the system fails, the store stops.

**What I build day to day:** an ERP shaped by the real operation (not the other way around) · an offline-first POS with custom checkout flows, integrated card (TEF) and instant payments (PIX) · a banking layer that unifies every bank into one contract · our own infrastructure control-plane (deploy, DNS, VPN, monitoring with WhatsApp alerts) · AI agents that operate the ERP through MCP with the same role-based permissions as human users, plus a living knowledge graph that acts as the company's brain.

**The thesis:** retail is my laboratory. **The company is the product** — every system is born from a real pain on the store floor and validated in production the next day. Tech here isn't a support area; it's the margin engine.

Highlights devs usually ask about: when we needed to replace our infra panel, nothing on the market combined fleet VPN management, internal DNS, git-based deploys with rollback and WhatsApp alerting the way a multi-store retail operation needs — so we built our own control-plane, and the whole infra was running on it within a week (it now self-deploys on every push, with build gates, health checks and automatic rollback).

</details>
