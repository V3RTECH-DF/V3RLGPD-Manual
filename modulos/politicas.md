---
title: "Políticas"
nav_order: 2
parent: "Módulos"
permalink: /modulos/politicas/
role: encarregado
routes: ["#/policies", "#/policies/edit/:id", "#/policies/assistant", "#/templates", "#/policies/types"]
screenshots: [v3rlgpd-02-policies, v3rlgpd-03-policy-editor, v3rlgpd-09-wizard, v3rlgpd-11-templates, v3rlgpd-95-document-types, v3rlgpd-96-document-types-remove]
last_verified: 2026-09-05
status: publicado
---

# Políticas

O módulo **Políticas** é onde sua organização cria, versiona e publica os documentos que explicam ao público como trata os dados — Política de Privacidade, Termos de Uso, Política de Cookies e o que mais precisar.

[![Lista de políticas](/assets/screenshots/v3rlgpd-02-policies.png)](/assets/screenshots/v3rlgpd-02-policies.png)
*Cada política mostra quantas versões publicadas tem e qual está ativa.*

> 💡 **Por que isso importa**
>
> Transparência é um pilar da LGPD: o titular tem o direito de saber o que você faz com os dados dele. Uma política clara e publicada é a forma mais direta de cumprir esse dever — e a primeira coisa que um financiador ou a <a href="https://www.gov.br/anpd/pt-br" target="_blank" rel="noopener noreferrer">ANPD</a> vão procurar.

## Ambiente genérico de políticas

O V3RLGPD **não entrega políticas prontas**. Ele dá a estrutura para você criar **quantas quiser** — e só a **Política de Privacidade** vem com um checklist e modelo-base, por ser exigência direta da LGPD.

## Tipos de documento

O módulo não serve só a políticas de privacidade: ele abriga **qualquer documento institucional** — estatuto, regimento, regulamento, relatório de atividades, e o que a sua organização precisar publicar. O que classifica cada documento é o **tipo**, e você mesmo cria, renomeia e remove os tipos, sem depender de ninguém mexer em código.

Em **Políticas**, clique em **Tipos de documento** para abrir a tela de gerenciamento.

[![Tela de Tipos de documento](/assets/screenshots/v3rlgpd-95-document-types.png)](/assets/screenshots/v3rlgpd-95-document-types.png)
*Cada tipo mostra quantos documentos usa ele; o tipo Privacidade vem marcado como "Fixo".*

A sua organização já começa com um conjunto pronto — privacidade, termos de uso, cookies, estatuto, regimento, regulamento e relatório —, para não precisar partir de uma lista vazia.

> 💡 **Por que isso importa**
>
> É o tipo que permite filtrar quais documentos aparecem numa listagem — por exemplo, mostrar só as políticas de privacidade e cookies na Central, e tudo (inclusive o estatuto e os relatórios) numa página de Transparência. Veja [Escolher quais documentos uma listagem mostra](/modulos/central-privacidade/#filtrar-quais-documentos-a-listagem-mostra).

**Criar um tipo novo** é só digitar o nome (ex.: "Regulamento de bolsas") e clicar em **Adicionar**.

**Renomear** um tipo muda **só o rótulo exibido** — o identificador interno que prende cada documento ao seu tipo nunca muda. É por isso que renomear é seguro mesmo com documentos já classificados: nada se desclassifica.

> ⚠️ **A armadilha mais comum aqui não é criar — é remover um tipo que já está em uso**
>
> Ao clicar em **Remover** num tipo que tem documentos classificados nele, o sistema **recusa a remoção direta** e mostra quantos documentos estão ali. Você decide:
>
> [![Diálogo de remoção de tipo em uso](/assets/screenshots/v3rlgpd-96-document-types-remove.png)](/assets/screenshots/v3rlgpd-96-document-types-remove.png)
> *O diálogo obriga uma decisão: reclassificar para outro tipo, ou manter os documentos como estão.*
>
> - **Reclassificar para outro tipo** — os documentos passam a valer para o tipo que você escolher.
> - **Manter a classificação atual** — o tipo sai da lista, mas os documentos continuam com ele; até serem reclassificados, aparecem com o identificador cru em vez do nome bonito.
>
> Nada é apagado em nenhum dos dois caminhos — a decisão existe justamente para que você não perca, sem perceber, o que cada documento era.

> ✅ **O tipo "Privacidade" nunca pode ser removido**
>
> É dele que a [Central de Privacidade](/modulos/central-privacidade/) depende para saber o que exibir e se há política publicada. O botão **Remover** fica desativado para ele — você ainda pode renomear o rótulo exibido, mas o identificador interno `privacy` é intocável. Nenhum outro tipo carrega esse tipo de comportamento embutido.

## Política interna ou externa (link)

Ao criar uma política, escolha a **origem**:

- **Interna** — você redige o texto no editor do plugin, com versionamento automático (o caminho tradicional).
- **Externa** — você aponta um **link** para uma política que já existe fora do plugin (um PDF, uma página de wiki, um documento numa intranet). Útil para organizações que já têm a política publicada e não querem reescrevê-la.

Para a política **externa**, você informa: a **URL** do documento, um **resumo/descrição**, uma **imagem ou ícone** (escolha um dos ícones prontos, envie uma imagem, ou deixe sem) e o **número da versão** (preenchido **manualmente**). Se a política já é uma **página publicada no seu site**, use o seletor **"Ou escolha uma página publicada do site"** — ele preenche a URL automaticamente com o link da página escolhida.

> ⚠️ **Versão da política externa é você quem atualiza**
>
> Como o texto mora fora do plugin, o V3RLGPD não controla as versões dela. **Atualize o número da versão sempre que publicar uma nova** — manter isso em dia é responsabilidade da sua organização.

[![Editor de política externa](/assets/screenshots/v3rlgpd-03b-policy-externa.png)](/assets/screenshots/v3rlgpd-03b-policy-externa.png)
*Política externa: URL, resumo, versão manual e a escolha de imagem ou ícone pré-definido.*

Na Central, a política externa aparece como um **card** com a imagem/ícone, o título, o resumo e um botão **"Ler a política completa"** que abre o documento em uma nova aba.

> 💡 **Resumo também nas internas**
>
> As políticas **internas** também têm um campo de **resumo** (opcional). Ele é usado quando você exibe as políticas no modo "resumo" (veja as [opções de exibição](/modulos/central-privacidade/#opcoes-de-exibicao-das-politicas)) — nesse modo, o resumo vem com um comando **"Ler na íntegra"** que abre o texto completo na mesma página (veja [Central de Privacidade](/modulos/central-privacidade/#no-modo-resumo-ler-na-integra-abre-o-documento-sem-sair-da-pagina)). Se você deixar o resumo em branco, o plugin gera um trecho automático a partir do texto.

## Versionamento e aceite

Toda alteração relevante gera uma **nova versão**. O histórico fica registrado, e você define qual versão está **ativa** (é a que o público vê). Esse versionamento é o que permite provar, mais tarde, **qual texto estava no ar em determinada data** — essencial para accountability.

## O editor

[![Editor de política](/assets/screenshots/v3rlgpd-03-policy-editor.png)](/assets/screenshots/v3rlgpd-03-policy-editor.png)
*Editor com formatação rica, histórico de versões e o Checklist LGPD ao lado.*

O editor tem:

- **Formatação rica** (negrito, itálico, títulos, listas, links) com opção de **ver o código HTML**.
- **Histórico de Versões**, com a versão ativa destacada.
- **Checklist LGPD**: um guia visual dos itens que uma Política de Privacidade deve contemplar — identificação do controlador, contato do Encarregado, finalidades, bases legais (Art. 7º), direitos do titular (Art. 18), tempo de retenção e compartilhamento de dados.

> ✅ **Boas práticas**
>
> Use o checklist como roteiro enquanto escreve. Ele não preenche o texto por você, mas garante que nenhum item obrigatório fique de fora.

## O Assistente de Políticas

Em vez de começar da folha em branco, use o **🪄 Assistente**: um passo a passo guiado, em linguagem simples, que monta um rascunho de **Política de Privacidade** ou de **Termos de Uso** a partir das suas respostas e dos dados que o plugin já tem (organização, **Encarregado**, **Inventário/ROPA**, perfil de proteção de menores).

[![Assistente de Políticas](/assets/screenshots/v3rlgpd-09-wizard.png)](/assets/screenshots/v3rlgpd-09-wizard.png)
*O Assistente guia você por tipo de política, triagem, seções e revisão do rascunho.*

Como funciona, passo a passo:

1. **Tipo** — escolha **Política de Privacidade** ou **Termos de Uso**.
2. **Pré-requisitos** — o Assistente confere se a **razão social da organização** e o **Encarregado** estão cadastrados. Sem esses dois, ele **interrompe** e leva você às Configurações (a política precisa identificar o controlador e o contato do Encarregado — Art. 41 da LGPD). Se o seu Inventário (ROPA) estiver vazio, ele apenas **avisa** — você pode seguir, mas a política fica mais genérica.
3. **Triagem** — perguntas simples de sim/não (formulários, cookies de terceiros, menores, transferência internacional, decisões automatizadas) que decidem quais cláusulas entram.
4. **Seções** — as seções obrigatórias entram sempre; as opcionais já vêm marcadas conforme suas respostas, e você ajusta.
5. **Rascunho** — o texto montado aparece num editor para você revisar e editar. Para a Privacidade, o Assistente ainda mostra **sugestões** (cláusulas que talvez faltem) e uma **revisão de coerência** com o seu Inventário (ROPA).
6. **Conclusão** — você decide: **salvar como rascunho** (padrão) para aprovação interna, ou **publicar agora**. O rascunho fica guardado **sem** ir ao ar até você publicá-lo.

> 💡 **Por que isso importa**
>
> O Assistente conecta o que você já cadastrou (organização, Encarregado, inventário) ao texto da política. Isso reduz erro e retrabalho: se a finalidade e a base legal já estão no inventário, elas entram na política sem você redigitar.

> ⚠️ **É um ponto de partida — a responsabilidade é da sua organização**
>
> O texto usa modelos padrão de mercado e **não substitui revisão jurídica** nem garante validade legal. Por isso o padrão é **salvar como rascunho**: revise e, de preferência, submeta à **aprovação da diretoria** antes de publicar. Veja o [Aviso legal](/disclaimer/).

> 🤖 **E a inteligência artificial?**
>
> Por ora, o Assistente é **determinístico** (sem IA): ele monta o texto a partir de modelos e dos seus dados. A estrutura já está preparada para, no futuro, oferecer geração e reescrita assistidas por IA — veja o [Roadmap](/roadmap/).

## A Galeria de Modelos

[![Galeria de modelos](/assets/screenshots/v3rlgpd-11-templates.png)](/assets/screenshots/v3rlgpd-11-templates.png)
*Modelos-semente de políticas e cláusulas, prontos para pré-preencher e abrir no editor.*

A **📚 Galeria de Modelos** traz modelos-base (políticas e cláusulas) para acelerar a redação.

> ⚠️ **Atenção**
>
> Os modelos são **ponto de partida de caráter geral**, não texto juridicamente validado para o seu caso. Adapte ao contexto da sua organização e, sempre que possível, valide com apoio jurídico. Veja o [Aviso legal](/disclaimer/).

## Exibir uma política em qualquer página (shortcode)

Além de a política aparecer na [Central de Privacidade](/modulos/central-privacidade/), você pode incorporar **uma política específica** em qualquer página do site (inclusive em construtores como Elementor) com o shortcode:

```
[v3rlgpd_politica id="1"]
```

Ele exibe o conteúdo da **versão ativa** daquela política (ou o **card** com o link, se a política for externa). Na **lista de Políticas**, cada política mostra o seu **ID** (e um atalho para copiar o shortcode pronto) — é o número que você coloca em `id="..."`.

Você ainda pode controlar **como** a política aparece com atributos (`modo`, `titulo`, `link`, `imagem`) — por exemplo `[v3rlgpd_politica id="1" modo="resumo"]`. Veja a tabela completa em [Opções de exibição das políticas](/modulos/central-privacidade/#opcoes-de-exibicao-das-politicas).

> 💡 **Quando usar**
>
> Útil quando você quer a Política de Privacidade (ou os Termos de Uso) numa página própria do site, separada da Central. Se a política não tiver uma versão ativa, o shortcode mostra um aviso discreto em vez de quebrar a página.

## Inativar e reativar uma política

Depois de ativada, uma política pode ser **inativada** — útil quando ela foi **incorporada a outra**, **substituída** ou simplesmente **deixou de valer**. Inativar **não apaga nada**: o conteúdo, o histórico de versões e os consentimentos já coletados são preservados, e você pode **reativar** quando quiser.

[![Lista de políticas com selo INATIVA](/assets/screenshots/v3rlgpd-02-policies.png)](/assets/screenshots/v3rlgpd-02-policies.png)
*Na lista, cada política tem o botão "Inativar" ou "Reativar"; as inativas exibem o selo "INATIVA".*

Como funciona:

- Na **lista de Políticas**, clique em **Inativar** (ou **Reativar**). Ao inativar, uma confirmação explica que a política deixará de aparecer publicamente.
- Uma política **inativa não aparece** na Central de Privacidade nem nos shortcodes (`[v3rlgpd_politica]` mostra o aviso de "não encontrada").
- Vale para políticas **internas e externas**.
- Para **reativar** uma política **interna**, ela precisa ter uma **versão ativa**; uma externa precisa ter a **URL** preenchida.
- Se você inativar a **Política de Privacidade**, o item correspondente do [Índice de Conformidade](/modulos/painel/) deixa de contar — reative-a para o indicador voltar.

> ✅ **Inativar ≠ excluir**
>
> **Inativar** é reversível e preserva tudo — é o que você quer na maioria dos casos. **Excluir** (abaixo) é mais forte e pode ser definitivo. Na dúvida, inative.

## Excluir uma política

Quando uma política realmente não deve mais existir, use **Excluir** (botão vermelho na lista). O que acontece depende do **Modo de Exclusão** configurado em [Configurações → Identidade](/guias/configurar-dpo/):

- **Arquivar (soft delete)** — a política sai do painel e do site, mas o **registro é preservado** (conteúdo, histórico de versões e auditoria continuam no sistema). Rastreabilidade mantida.
- **Excluir em definitivo (hard delete)** — a política e **todo o seu histórico de versões são apagados** do sistema. **Você perde a rastreabilidade** de qual texto esteve no ar e quando. É irreversível.

Antes de confirmar, o sistema mostra um aviso explicando essas consequências e sugerindo **Inativar** quando você só quer tirar a política do site.

> ⚠️ **Excluir pode apagar a rastreabilidade**
>
> No modo *definitivo*, não há volta: o histórico de versões some. Se há qualquer chance de você precisar comprovar qual política estava vigente em determinada data, **inative em vez de excluir**.

> ✅ **Os consentimentos são sempre preservados**
>
> Mesmo na exclusão definitiva, os **consentimentos já coletados não são apagados** — eles continuam como prova do que foi consentido.

## Como fazer

➡️ Passo a passo em **[Publicar uma política](/guias/publicar-politica/)**.
