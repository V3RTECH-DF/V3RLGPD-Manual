---
title: "Publicar a Central de Privacidade"
nav_order: 3
parent: "Guias por tarefa"
permalink: /guias/publicar-central-privacidade/
task: publicar-central-privacidade
role: encarregado
routes: ["#/settings"]
screenshots: [v3rlgpd-08d-settings-paginas]
last_verified: 2026-06-24
status: publicado
---

# Publicar a Central de Privacidade

A Central de Privacidade é a página pública onde o titular lê suas políticas, ajusta cookies e abre pedidos. Publicá-la é rápido.

[![Páginas & Integração](/assets/screenshots/v3rlgpd-08d-settings-paginas.png)](/assets/screenshots/v3rlgpd-08d-settings-paginas.png)
*Configurações → Páginas & Integração.*

## Forma rápida (recomendada)

1. No painel, abra **V3RLGPD → Configurações → Páginas & Integração**.
2. Clique em **Gerar Página Automaticamente**.
3. O plugin cria (ou recupera) a página **Central de Privacidade** no WordPress, já publicada.
4. Pronto: ela fica acessível em um endereço como `seusite.org/central-de-privacidade/`.

> 💡 Você pode editar a página normalmente pelo menu **Páginas** do WordPress (título, posição no menu etc.) — o conteúdo dinâmico continua vindo do plugin.

## Usando shortcodes (avançado)

Para inserir a Central (ou só o formulário) em outra página, inclusive em construtores como Elementor, use os shortcodes:

- `[v3rlgpd_privacidade]` — a Central completa (políticas + Encarregado + formulário + cookies). **Recomendado.**
- `[v3rlgpd_solicitacao]` — apenas o formulário de pedidos (ideal numa página de Contato).
- `[v3rlgpd_politica id="1"]` — uma política específica, pelo seu ID (mostrado na lista de [Políticas](/modulos/politicas/)).
- `[v3rlgpd_dpo]` — o contato/identidade do Encarregado.
- `[v3rlgpd_politicas]` — a lista dos seus documentos. Sem mais nada, mostra todos os ativos; dá para escolher quais aparecem — veja [Filtrar quais documentos a listagem mostra](/modulos/central-privacidade/#filtrar-quais-documentos-a-listagem-mostra).
- `[v3rlgpd_cookies]` — preferências de cookies (só aparece com o banner ativo).

Estes são os que servem para montar uma Central à mão. O plugin tem **onze** no total — a lista completa, com o que cada um faz, está em [Central de Privacidade](/modulos/central-privacidade/#como-publicar-a-central), e também dentro do plugin, em **Configurações → Shortcodes Disponíveis**.

> ⚠️ Ao montar uma página à mão, **não omita** o contato do Encarregado nem o formulário de solicitação — eles são exigidos pela LGPD. A Central completa autogerada já garante isso.

### Designe a sua página como a Central

Montou uma página personalizada? Diga ao plugin que é **ela** a Central oficial: em **Páginas & Integração**, use o seletor **"Selecione a página da Central"**. Assim o [Índice de Conformidade](/modulos/painel/) e o link do banner de cookies passam a apontar para a sua página, e não para a padrão.

### Ajuste a exibição das políticas

Ainda em **Páginas & Integração**, o bloco **"Exibição Padrão das Políticas"** define como elas aparecem (texto integral, resumo ou só título; mostrar título, link e imagem). Você pode sobrescrever caso a caso pelos atributos do shortcode — veja a tabela em [Opções de exibição](/modulos/central-privacidade/#opcoes-de-exibicao-das-politicas).

## Depois de publicar

1. Adicione o link da Central ao **menu** e/ou ao **rodapé** do site, para o titular achar com facilidade.
2. Confira que sua **Política de Privacidade** está **ativa** (senão a Central aparece sem política).
3. Ative o **banner de cookies** se o site usa análise/marketing (veja [Consentimento & Cookies](/modulos/consentimento/)).

> ✅ **Boas práticas**
>
> Um link de "Privacidade" no rodapé de todas as páginas é o padrão que o público espera. Facilita o exercício de direitos e demonstra transparência.
