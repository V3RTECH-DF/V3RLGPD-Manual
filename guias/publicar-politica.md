---
title: "Publicar uma política"
nav_order: 2
parent: "Guias por tarefa"
permalink: /guias/publicar-politica/
task: publicar-politica
role: encarregado
routes: ["#/policies", "#/policies/new", "#/policies/assistant"]
screenshots: [v3rlgpd-02-policies, v3rlgpd-03-policy-editor, v3rlgpd-03b-policy-externa, v3rlgpd-09-wizard]
last_verified: 2026-09-05
status: publicado
---

# Publicar uma política

Uma política só fica visível ao público quando você **publica uma versão** e a marca como **ativa**. Veja como.

## Opção A — usar o Assistente (recomendado para a 1ª política)

Antes de começar, garanta que a **razão social da organização** e o **Encarregado** estão cadastrados em [Configurações](/guias/configurar-dpo/) — o Assistente exige os dois (sem eles, ele interrompe e leva você às Configurações).

1. Em **Políticas**, clique em **🪄 Usar Assistente**.
2. Escolha o **tipo**: **Política de Privacidade** ou **Termos de Uso**.
3. Responda à **triagem** (perguntas simples de sim/não) e confira as **seções** que vão entrar.
4. O Assistente monta o **rascunho** com os dados da organização, do **Encarregado** e do **Inventário (ROPA)**. Revise e edite no editor. (Na Privacidade, ele ainda mostra **sugestões** e uma **revisão de coerência** com o ROPA.)
5. Na **conclusão**, escolha **salvar como rascunho** (padrão, para aprovação interna) ou **publicar agora**.

[![Assistente de Políticas](/assets/screenshots/v3rlgpd-09-wizard.png)](/assets/screenshots/v3rlgpd-09-wizard.png)
*O Assistente conduz por tipo, triagem, seções e revisão do rascunho.*

> 💡 Quanto mais completo o seu [Inventário (ROPA)](/modulos/inventario-ropa/), melhor o rascunho do Assistente.

> ⚠️ O padrão é **salvar como rascunho**: políticas normalmente precisam de **aprovação da diretoria** antes de ir ao ar. Quando estiver tudo certo, publique (Opção de ativação abaixo).

## Opção B — criar do zero (política interna)

1. Em **Políticas**, clique em **+ Nova Política**.
2. Informe o **título** e o **tipo** e mantenha a origem **Interna**. Além de privacidade, termos e cookies, sua organização pode ter criado outros tipos (estatuto, regimento, relatório…) em [Tipos de documento](/modulos/politicas/#tipos-de-documento). **O título que você digitar é o nome que o público vê** na Central e na listagem — inclusive para o tipo "Privacidade", que não força mais o rótulo "Política de Privacidade" se você preferir outro nome.
3. Abra a política e, no editor, escreva o conteúdo. (Opcional: preencha o **Resumo** — ele é exibido quando a política aparece no modo "resumo".)

[![Editor de política com checklist](/assets/screenshots/v3rlgpd-03-policy-editor.png)](/assets/screenshots/v3rlgpd-03-policy-editor.png)
*Editor da política interna, com o campo de resumo e o histórico de versões.*

4. Use o **Checklist LGPD** como guia: controlador, contato do Encarregado, finalidades, bases legais, direitos do titular, retenção, compartilhamento.
5. Clique em **Publicar Versão**.

## Opção C — política externa (por link)

Se a sua organização **já tem a política publicada** em outro lugar (um PDF, uma página de wiki, uma intranet), não precisa reescrevê-la:

1. Em **Políticas**, clique em **+ Nova Política** e escolha a origem **Externa**.
2. Informe a **URL** do documento, um **resumo/descrição** e, se quiser, uma **imagem ou ícone** (há ícones prontos — não precisa enviar arquivo).
3. Preencha o **número da versão** manualmente (ex.: "v2 — 2025") e salve.

[![Editor de política externa](/assets/screenshots/v3rlgpd-03b-policy-externa.png)](/assets/screenshots/v3rlgpd-03b-policy-externa.png)
*Política externa: URL, resumo, versão manual e escolha de ícone.*

> ⚠️ **Mantenha a versão em dia.** Como o texto da política externa mora fora do plugin, é a sua organização que precisa **atualizar o número da versão** sempre que publicar uma nova.

A política externa aparece na Central como um **card** com botão "Ler a política completa" e **não** usa o versionamento automático do plugin.

## Ativar a versão

Na lista de políticas, abra a política e defina a versão publicada como **ativa**. Só a versão ativa aparece na Central de Privacidade.

[![Lista de políticas](/assets/screenshots/v3rlgpd-02-policies.png)](/assets/screenshots/v3rlgpd-02-policies.png)
*A lista mostra qual versão está ativa em cada política.*

> 💡 Com a Política de Privacidade ativa, o item **Política de Privacidade Ativa** do [Índice de Conformidade](/modulos/painel/) passa a contar.

## Atualizar depois

Toda alteração relevante deve gerar uma **nova versão** (não reescrever a antiga). Assim o histórico fica preservado e você consegue provar qual texto estava no ar em cada data.

## Inativar ou reativar uma política

Quando uma política é **incorporada a outra**, **substituída** ou **deixa de valer**, você pode **inativá-la** sem apagar nada — e reativá-la depois:

1. Na lista de **Políticas**, clique em **Inativar** na política desejada e confirme.
2. A política some da Central e dos shortcodes; na lista ela passa a exibir o selo **"INATIVA"**.
3. Para trazer de volta, clique em **Reativar** (uma política interna precisa ter uma versão ativa para ser reativada).

> ✅ Inativar é **reversível** e preserva versões e consentimentos — diferente de **excluir**. Detalhes em [Políticas › Inativar e reativar](/modulos/politicas/#inativar-e-reativar-uma-politica).

Se a política realmente não deve mais existir, há o botão **Excluir** — que pode apenas arquivar ou apagar em definitivo, conforme o Modo de Exclusão. Como a exclusão definitiva **apaga o histórico e a rastreabilidade**, prefira **Inativar** quando estiver em dúvida. Veja [Políticas › Excluir](/modulos/politicas/#excluir-uma-politica).

> ⚠️ **Atenção**
>
> Os modelos e o Assistente produzem um **ponto de partida geral**, não um texto juridicamente validado para o seu caso. Revise com cuidado e, quando possível, valide com apoio jurídico. Veja o [Aviso legal](/disclaimer/).
