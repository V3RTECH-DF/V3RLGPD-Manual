---
title: "Atendimentos (DSAR)"
nav_order: 4
parent: "Módulos"
permalink: /modulos/atendimentos/
role: encarregado
routes: ["#/dsar", "#/settings"]
screenshots: [v3rlgpd-04-dsar, v3rlgpd-04c-dsar-detalhe-auto, v3rlgpd-04d-dsar-banner-revisar, v3rlgpd-04b-dsar-declaracao-escopo]
last_verified: 2026-08-13
status: publicado
---

# Atendimentos (DSAR)

Aqui chegam os **pedidos dos titulares** sobre os próprios dados — o que a lei chama de direitos do Art. 18 e o mercado chama de *DSAR* (*Data Subject Access Request*). É um dos momentos mais importantes da LGPD: a hora de responder a quem confiou seus dados à sua organização.

[![Lista de atendimentos](/assets/screenshots/v3rlgpd-04-dsar.png)](/assets/screenshots/v3rlgpd-04-dsar.png)
*Cada pedido mostra e-mail, tipo, data-limite (SLA) e status. "Ver / Executar" abre a execução assistida.*

## O ciclo de um pedido

1. **O titular abre o pedido** na Central de Privacidade, informando o e-mail e o direito desejado.
2. **Duplo opt-in** — o plugin envia um link de confirmação para o e-mail. O pedido só entra na fila depois que a pessoa clica e confirma. Isso evita pedidos falsos e prova que o e-mail é de quem pediu.
3. **O pedido aparece nesta lista** como **Pendente**, com a **data-limite (SLA)** calculada. O titular vê na hora a mensagem de que será analisado pelo Encarregado **em até 15 dias úteis**.
4. **O Encarregado atende** — consultando, exportando ou eliminando os dados conforme o tipo.
5. **O titular é avisado** por e-mail quando o pedido é concluído ou recusado.

> 💡 **Por que isso importa**
>
> O prazo de referência é de **15 dias**. Perder o prazo é um dos erros mais comuns — e mais facilmente evitáveis. A lista separa **pendentes no prazo** de **pendentes atrasadas** para que nada passe despercebido.

## Todo pedido passa pelo Encarregado

Nenhum pedido é encerrado **automaticamente, sem revisão**. Mesmo os tipos mais simples (acesso, portabilidade, informação sobre compartilhamento) entram como **Pendentes** e ficam visíveis para o Encarregado decidir.

> ⚠️ **Por que mudou**
>
> Antes, alguns pedidos eram concluídos na hora buscando dados **só no site**. O problema: o plugin enxerga o site, mas a sua organização pode tratar dados também **no papel, em planilhas ou em outros sistemas**. Responder "não há dados" baseado apenas no site seria um **falso-negativo** — uma resposta definitiva que pode estar errada. Por isso, quem dá a palavra final é sempre o Encarregado.

## A declaração de escopo da organização

Em **Configurações → Organização** há uma pergunta que orienta o atendimento: **"A organização trata dados pessoais fora deste site?"** (Não / Sim / Não informado).

[![Declaração de escopo em Configurações → Organização](/assets/screenshots/v3rlgpd-04b-dsar-declaracao-escopo.png)](/assets/screenshots/v3rlgpd-04b-dsar-declaracao-escopo.png)
*A declaração fica na aba **Organização**. Só "Não" (trata dados apenas neste site) habilita a resposta automática assistida.*

- **Não — tratamos dados apenas neste site:** o Encarregado ganha a opção de **responder automaticamente** os pedidos informativos (veja abaixo), porque, nesse caso, o site é todo o escopo de tratamento.
- **Sim — também tratamos dados fora do site** *(ou "Não informado")*: o plugin **não** oferece a resposta automática; ele lembra que pode haver dados fora do site e pede que você **revise antes de responder**.

> 💡 A declaração é uma afirmação **sua**, no nível da organização — é ela que torna seguro responder com base apenas no site. Mantenha-a coerente com a realidade da sua organização.

## Insumos para responder: o painel do Inventário (ROPA)

Ao abrir um pedido em **Ver / Executar**, além da execução assistida, o Encarregado vê um **painel com as atividades do Inventário (ROPA)** — nome da atividade, **origem** dos dados, **compartilhamento** e **transferência internacional** quando houver. É uma referência rápida para lembrar onde mais aquele dado pode estar, inclusive fora do site.

## Resposta automática assistida (pedidos informativos)

[![Detalhe do pedido com o botão Responder automaticamente](/assets/screenshots/v3rlgpd-04c-dsar-detalhe-auto.png)](/assets/screenshots/v3rlgpd-04c-dsar-detalhe-auto.png)
*Com a organização declarada "apenas neste site", os pedidos informativos mostram o banner verde e o botão **Responder automaticamente**.*

Quando a organização declarou tratar dados **apenas neste site** e o pedido é de um tipo **informativo** — **Acesso e Confirmação**, **Portabilidade** ou **Informação sobre Compartilhamento** —, o Encarregado pode clicar em **Responder automaticamente**. O plugin:

1. Monta o resultado a partir dos dados do site;
2. **Envia o e-mail de resposta ao titular** (na Portabilidade, com o **arquivo JSON dos dados anexado**);
3. Marca o pedido como **Concluída**.

É sempre o Encarregado quem aciona — nunca automático às cegas. E há uma **trava no servidor**: o botão só funciona para tipos informativos, com a organização declarada "apenas neste site", enquanto o pedido estiver em aberto.

[![Banner de revisão quando há tratamento fora do site](/assets/screenshots/v3rlgpd-04d-dsar-banner-revisar.png)](/assets/screenshots/v3rlgpd-04d-dsar-banner-revisar.png)
*Quando a organização trata dados também fora do site (ou não declarou), não há botão automático: um banner pede para revisar antes de responder manualmente.*

> ⚠️ **Atenção — exclusão e revogação nunca são automáticas**
>
> Pedidos de **eliminação/anonimização** e **revogação de consentimento** **nunca** mostram o botão de resposta automática, mesmo com a organização declarada "apenas neste site". Exclusão é irreversível: o plugin exige confirmação humana e justificativa antes de apagar qualquer coisa. É uma trava de segurança proposital.

## Execução assistida

Ao clicar em **Ver / Executar**, o Encarregado conta com a execução assistida: o plugin **localiza** os dados ligados àquele e-mail nos sistemas conectados, permite **exportar** e, quando o pedido autoriza, **eliminar**. Também pode **anexar documentos** à resposta enviada ao titular.

### O que o Localizar enxerga

Quando alguém pergunta *"quais dados vocês têm sobre mim?"*, o botão **Localizar** procura o e-mail informado em:

- **Consentimentos** registrados pelo V3RLGPD (banner de cookies, formulários com checkbox).
- **Comentários** do WordPress.
- **Respostas de formulário** do site — Forminator, Fluent Forms, WPForms, Gravity Forms, Contact Form 7 (via Flamingo) e Elementor Forms.

O **Eliminar** age sobre as mesmas origens: apaga as respostas de formulário daquela pessoa **junto com os arquivos que ela tiver enviado**. Ao final, o relatório da ação mostra **quanto foi eliminado em cada origem**, para você saber exatamente o que aconteceu — e poder registrar isso na resposta ao titular.

> ⚠️ **O que ainda não entra nessa busca**
>
> **Contas de usuário do WordPress** e **dados do WooCommerce** (clientes e pedidos) **não** são incluídos no Localizar nem no Eliminar do atendimento. Isso está em avaliação e não é esquecimento: apagar um pedido de loja esbarra em **prazo legal de guarda fiscal**, e uma exclusão automática poderia destruir um registro que a organização é obrigada a manter. Enquanto isso, se a sua organização tem loja ou área de usuários, **confira esses sistemas manualmente** antes de responder ao titular.

> ⚠️ **Atenção — eliminação é definitiva**
>
> A eliminação de dados é **irreversível**. O plugin pede uma **justificativa** e registra a ação numa **assinatura auditável** (com encadeamento à prova de adulteração). Tenha certeza antes de confirmar — e lembre-se de que alguns dados podem ter de ser **retidos** por obrigação legal, mesmo diante de um pedido de exclusão.

## Auditoria

Toda ação relevante (criação, mudança de status, execução) é registrada num **log de auditoria imutável**. É isso que permite, depois, demonstrar **quem fez o quê e quando** — a essência da accountability.

## Como fazer

➡️ Passo a passo em **[Atender uma solicitação](/guias/atender-solicitacao/)** e, do lado do titular, em **[Como o titular exerce seus direitos](/guias/titular-exercer-direitos/)**.
