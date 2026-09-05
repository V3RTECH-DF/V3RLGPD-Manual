---
title: "Central de Privacidade"
nav_order: 3
parent: "Módulos"
permalink: /modulos/central-privacidade/
role: titular
routes: ["/central-de-privacidade/"]
screenshots: [v3rlgpd-22-dsar-form, v3rlgpd-72-central-encarregado, v3rlgpd-08d-settings-paginas]
last_verified: 2026-09-05
status: publicado
---

# Central de Privacidade

A **Central de Privacidade** é a página **pública** do seu site onde o titular faz tudo o que a LGPD lhe garante: ler as políticas, conhecer o Encarregado, ajustar cookies e abrir pedidos sobre seus dados.

[![Central de Privacidade pública](/assets/screenshots/v3rlgpd-22-dsar-form.png)](/assets/screenshots/v3rlgpd-22-dsar-form.png)
*A página reúne o formulário de direitos, a identidade do Encarregado e a Política de Privacidade ativa.*

## O que o titular vê

- **Exercício de Direitos** — um formulário para abrir pedidos (acesso, correção, exclusão, portabilidade, revogação, informação sobre compartilhamento, outro).
- **Identidade de Privacidade** — nome/setor, e-mail e telefone do Encarregado, para contato direto.
- **Política de Privacidade** — a **versão ativa**, exibida na íntegra. Só políticas ativas aparecem — uma política [inativada](/modulos/politicas/#inativar-e-reativar-uma-politica) some da Central automaticamente.

[![Contato do Encarregado na Central pública](/assets/screenshots/v3rlgpd-72-central-encarregado.png)](/assets/screenshots/v3rlgpd-72-central-encarregado.png)
*O bloco de contato traz o **Encarregado** (com a sigla "DPO" só como equivalência na 1ª menção). Esses são os dados cadastrados em [Configurações → Encarregado](/modulos/configuracoes/#encarregado).*
- **Banner de cookies** — na primeira visita (veja [Consentimento & Cookies](/modulos/consentimento/)).

## Como publicar

[![Páginas & Integração](/assets/screenshots/v3rlgpd-08d-settings-paginas.png)](/assets/screenshots/v3rlgpd-08d-settings-paginas.png)
*Em Configurações → Páginas & Integração, gere a página automaticamente ou use os shortcodes.*

Há duas formas:

1. **Gerar Página Automaticamente** — em **Configurações → Páginas & Integração**, um clique cria a página completa no WordPress.
2. **Shortcodes** — para inserir em qualquer página (inclusive construtores como Elementor):
   - `[v3rlgpd_privacidade]` — a Central **completa** (recomendado).
   - `[v3rlgpd_solicitacao]` — só o formulário de pedidos (útil numa página de Contato).
   - `[v3rlgpd_politica id="1"]` — uma política específica (ver [Políticas](/modulos/politicas/)).
   - `[v3rlgpd_dpo]` — o contato/identidade do Encarregado.
   - `[v3rlgpd_politicas]` — a lista dos seus documentos. Sem mais nada, mostra todos os ativos; para escolher quais aparecem, veja [Filtrar quais documentos a listagem mostra](#filtrar-quais-documentos-a-listagem-mostra) mais abaixo.
   - `[v3rlgpd_cookies]` — o botão **"Alterar Preferências de Cookies"**, que reabre o painel do banner já mostrando a escolha atual do titular (ver [Consentimento & Cookies](/modulos/consentimento/)). Aparece só se o banner estiver ativo.
   - `[v3rlgpd_ropa]` — uma vitrine de transparência das atividades de tratamento (ver [Inventário (ROPA)](/modulos/inventario-ropa/)).
   - `[v3rlgpd_transparencia_menores]` — card de transparência para crianças e adolescentes (aparece só se você tratar dados de menores; ver [Transparência aos pais](/eca-digital/transparencia-aos-pais/)).
   - `[v3rlgpd_denuncia]` — canal público de denúncia do ECA Digital (ver [Denúncias](/modulos/denuncias/)).
   - `[v3rlgpd_selo]` — o selo de conformidade da sua organização, para o rodapé do site. Aceita `formato="fita"` (ou `medalha`, `cartao`), `mostrar_numero="sim"` e `link="nao"` (ver [Painel › Selo](/modulos/painel/#o-selo-de-conformidade-no-painel)).
   - `[v3rlgpd_gestao]` — ⚠️ **este não é público.** Traz a administração da conformidade para dentro do site, para quem cuida do assunto trabalhar sem entrar no painel do WordPress. Publique numa página **restrita**, nunca aqui na Central nem em página aberta a visitantes (ver [Gestão no site](/modulos/gestao-frontend/)).

> Esta é a lista completa: são os **onze** shortcodes do plugin. Você também a encontra dentro do plugin, em **Configurações → Shortcodes Disponíveis**, com um botão que copia cada um.

> ⚠️ **Página montada à mão é responsabilidade sua**
>
> A Central **completa** autogerada já inclui tudo que a LGPD exige (Encarregado, políticas e canal de pedidos). Se você montar uma página personalizada com os shortcodes individuais, **garanta que o contato do Encarregado e o formulário de solicitação não fiquem de fora** — senão a página fica incompleta perante a lei.

## Escolher qual página é a sua Central

Se você montou uma **página personalizada** com os shortcodes, diga ao plugin que é **ela** a Central oficial: em **Configurações → Páginas & Integração**, use o **seletor "Selecione a página da Central"** e escolha qualquer página publicada do seu site.

A página escolhida passa a valer para:

- o **Índice de Conformidade** (o item "Central de Privacidade" do painel marca como concluído quando a página designada está publicada);
- o **link "Centro de Privacidade"** do banner de cookies, que passa a apontar para ela.

> 💡 **Por que isso importa**
>
> Sem isso, o painel só reconheceria a página padrão autogerada — e quem prefere uma Central feita à mão ficaria com o semáforo "incompleto" sem motivo. O seletor deixa você usar a sua própria página sem perder o acompanhamento de conformidade.

## Opções de exibição das políticas

Você controla **como** as políticas aparecem (na Central e nos shortcodes `[v3rlgpd_politicas]` e `[v3rlgpd_politica]`), por dois caminhos:

- **Padrão global** — em **Configurações → Páginas & Integração**, defina o comportamento padrão: modo de exibição, se mostra título, link e imagem, e o **tamanho da imagem**.
- **Por shortcode** — passe atributos que **sobrescrevem** o padrão global naquele lugar específico:

| Atributo | Valores | O que faz |
|---|---|---|
| `modo` | `integral` / `resumo` / `titulo` | Texto completo, só o resumo (padrão) ou só o título. Não afeta políticas externas (que sempre aparecem como card). |
| `titulo` | `sim` / `nao` | Mostra ou oculta o título. |
| `link` | `sim` / `nao` | Mostra ou oculta o botão "Ler a política completa" (só políticas externas). |
| `imagem` | `sim` / `nao` | Mostra ou oculta a imagem/ícone. |
| `tamanho` | `pequeno` / `medio` / `grande` / `extra-grande` | Tamanho da imagem/ícone no card da política externa (padrão `pequeno`). |

Exemplos:

```
[v3rlgpd_politicas modo="titulo"]
[v3rlgpd_politica id="3" imagem="nao" link="nao"]
[v3rlgpd_politica id="3" tamanho="grande"]
```

> 💡 **Combinações seguras**
>
> O plugin nunca deixa um bloco totalmente vazio: se você ocultar tudo de uma vez, ele exibe ao menos o título.

## Filtrar quais documentos a listagem mostra

O shortcode `[v3rlgpd_politicas]` aceita quatro atributos de filtro, combináveis entre si. Sem nenhum atributo, ele mostra todos os documentos ativos — o comportamento de sempre.

| Atributo | Exemplo | O que faz |
|---|---|---|
| `tipo` | `tipo="privacy,cookies"` | Mostra só os documentos dos [tipos](/modulos/politicas/#tipos-de-documento) listados |
| `ids` | `ids="4,1,3"` | Mostra só os documentos informados, **na ordem** em que você os listou |
| `excluir` | `excluir="15,16"` | Mostra tudo, menos os documentos informados |
| `limite` | `limite="5"` | Corta a lista nos primeiros N documentos |

> 💡 **Dois usos reais**
>
> Uma Central de Privacidade que mostra só o que é de privacidade e cookies, e se atualiza sozinha quando você publica um documento novo desse tipo — sem precisar editar a página. E uma página de Transparência, sem nenhum filtro, mostrando tudo (inclusive estatuto, regimento e relatórios).

> ⚠️ **A Central de Privacidade passou a filtrar por padrão**
>
> A Central completa (gerada automaticamente ou pelo shortcode `[v3rlgpd_privacidade]`) agora só mostra os tipos **privacidade e cookies** — antes mostrava todos os documentos ativos, o que incluía relatórios anuais e outros documentos que não são de privacidade. Se a sua organização usa a Central para exibir também **termos de uso** ou outro tipo, ele **some da página** até você acrescentá-lo ao filtro: `[v3rlgpd_privacidade tipo="privacy,cookies,terms"]`. A página de Transparência (sem atributo) continua mostrando tudo, sem mudança.

➡️ Passo a passo em **[Publicar a Central de Privacidade](/guias/publicar-central-privacidade/)**.

> 💡 **Por que isso importa**
>
> A Central concentra, num lugar só, tudo o que a LGPD exige que esteja acessível ao titular. Ter esse endereço público e fácil de achar é metade do caminho da transparência — e evita que pedidos cheguem por canais informais (WhatsApp, recado) que você não consegue rastrear.

## Como o titular usa

➡️ Veja **[Como o titular exerce seus direitos](/guias/titular-exercer-direitos/)**.
