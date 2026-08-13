---
title: "Atender uma solicitação"
nav_order: 4
parent: "Guias por tarefa"
permalink: /guias/atender-solicitacao/
task: atender-solicitacao
role: encarregado
routes: ["#/dsar", "#/settings"]
screenshots: [v3rlgpd-04-dsar, v3rlgpd-04c-dsar-detalhe-auto]
last_verified: 2026-08-13
status: publicado
---

# Atender uma solicitação de titular

Quando um titular abre um pedido e confirma o e-mail, ele aparece em **Atendimentos**. Veja como tratá-lo.

[![Lista de atendimentos](/assets/screenshots/v3rlgpd-04-dsar.png)](/assets/screenshots/v3rlgpd-04-dsar.png)
*Cada linha traz e-mail, tipo, data-limite (SLA), status e a ação "Ver / Executar".*

## Passo a passo

1. Abra **V3RLGPD → Atendimento ao Titular** e vá à aba **Atendimentos**. Todo pedido confirmado entra como **Pendente** — nenhum é concluído sem a sua revisão.
2. Veja a **data-limite (SLA)** de cada pedido. Priorize os que estão perto do prazo (referência: **15 dias**).
3. Clique em **Ver / Executar** no pedido desejado.
4. Consulte os **insumos** no detalhe: a **execução assistida** (dados ligados ao e-mail) e o **painel do Inventário (ROPA)** (onde mais aquele dado pode estar, inclusive fora do site).
   - O **Localizar** procura o e-mail nos **consentimentos**, nos **comentários** e nas **respostas de formulário** do site (Forminator, Fluent Forms, WPForms, Gravity Forms, CF7/Flamingo e Elementor Forms).
   - **Contas de usuário do WordPress** e **dados do WooCommerce ainda não entram** nessa busca — confira esses sistemas à mão antes de dar a resposta como completa.
5. Responda:
   - **Resposta automática** (quando disponível) — veja abaixo.
   - **Resposta manual** — escreva o **Motivo / Resposta ao Titular**, anexe documentos se quiser, e atualize o **status**. O titular é avisado por e-mail quando você conclui ou recusa.

## Antes de começar: a declaração de escopo

Em **Configurações → Organização**, responda **"A organização trata dados pessoais fora deste site?"**. Essa declaração decide se a resposta automática fica disponível:

- **Não (apenas neste site)** → libera o botão **Responder automaticamente** nos pedidos informativos.
- **Sim** ou **Não informado** → sem botão automático; você responde manualmente, revisando antes.

## Responder automaticamente (pedidos informativos)

[![Detalhe do pedido com o botão Responder automaticamente](/assets/screenshots/v3rlgpd-04c-dsar-detalhe-auto.png)](/assets/screenshots/v3rlgpd-04c-dsar-detalhe-auto.png)
*Com a organização "apenas neste site", os pedidos informativos trazem o banner verde e o botão **Responder automaticamente**.*

Para pedidos de **acesso/confirmação**, **portabilidade** e **informação sobre compartilhamento**, com a organização declarada **apenas neste site**, clique em **Responder automaticamente**. O plugin monta o resultado a partir dos dados do site, **envia o e-mail ao titular** (na portabilidade, com o **JSON anexado**) e marca o pedido como **Concluída**. Você está sempre no comando — o botão é seu, não um envio automático às cegas.

> ⚠️ **Eliminação e revogação nunca têm botão automático** — esses tipos exigem sempre tratamento manual, mesmo com a organização "apenas neste site".

## Eliminação — com cuidado

> ⚠️ **Atenção — ação irreversível**
>
> Ao eliminar dados, o plugin pede uma **justificativa** e registra tudo numa **assinatura auditável**. Antes de confirmar:
> - Verifique se **não há base legal** que obrigue a reter aquele dado (ex.: obrigação legal, prestação de contas).
> - Lembre-se: depois de eliminado, **não há como recuperar**.

A eliminação apaga as **respostas de formulário** daquela pessoa **e os arquivos que ela tiver anexado** (currículo, comprovante, foto). Ao final, o relatório mostra **quanto foi eliminado em cada origem** — copie esse resumo para a resposta ao titular: é a sua demonstração concreta de que o pedido foi cumprido.

## Recusar um pedido

Nem todo pedido procede (ex.: exclusão de dado que a lei obriga a manter). Ao recusar, **explique o motivo** no campo de observação — o titular recebe essa justificativa por e-mail. Transparência reduz conflito.

> 💡 **Por que isso importa**
>
> Responder no prazo e com clareza é o que constrói confiança. Cada pedido bem atendido é uma pessoa que percebe que sua organização leva a sério os dados dela.
