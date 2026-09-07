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

Estes são os que servem para montar uma Central à mão. O plugin tem **onze** no total — a lista completa, com o que cada um faz, está em [Central de Privacidade](/modulos/central-privacidade/#como-publicar), e também dentro do plugin, na aba **Configurações → Shortcodes**.

> 💡 **O formulário de solicitação agora usa a fonte do seu site**
>
> Até pouco tempo, `[v3rlgpd_solicitacao]` vinha com fonte genérica e sempre centralizado, no meio de uma página que podia ter outro alinhamento e outra tipografia. Isso mudou: o formulário passa a **herdar a tipografia do site**, então ele já sai parecido com o resto da página, sem trabalho seu. A largura máxima continua a mesma de sempre; se você quiser mudá-la, use o atributo `classe` (acima) para aplicar a sua própria regra de CSS.

> ⚠️ Ao montar uma página à mão, **não omita** o contato do Encarregado nem o formulário de solicitação — eles são exigidos pela LGPD. A Central completa autogerada já garante isso.

### Designe a sua página como a Central

Montou uma página personalizada? Diga ao plugin que é **ela** a Central oficial: em **Páginas & Integração**, use o seletor **"Selecione a página da Central"**. Assim o [Índice de Conformidade](/modulos/painel/) e o link do banner de cookies passam a apontar para a sua página, e não para a padrão.

### Ajuste a exibição das políticas

Ainda em **Páginas & Integração**, o bloco **"Exibição Padrão das Políticas"** define como elas aparecem (texto integral, resumo ou só título; mostrar título, link e imagem). Você pode sobrescrever caso a caso pelos atributos do shortcode — veja a tabela em [Opções de exibição](/modulos/central-privacidade/#opções-de-exibição-das-políticas).

### Controle o layout de cada bloco (título, descrição, nível e classe)

Quem monta a própria página — em vez de usar a Central completa autogerada — costuma ter um layout já pronto, com títulos e espaçamento definidos pelo tema ou pelo construtor de páginas (Elementor, por exemplo). Sem controle sobre o que cada bloco do plugin impõe, o resultado é um título duplicado, um cabeçalho `<h2>` competindo com o do resto da página, ou um visual que destoa do layout em volta.

Por isso a maioria dos blocos aceita quatro atributos em comum:

| Atributo | Valores | O que faz |
|---|---|---|
| `titulo` | `sim` (padrão) / `nao` | Mostra ou oculta o título do bloco. |
| `descricao` | `sim` / `nao` | Mostra ou oculta o texto de apoio abaixo do título. |
| `nivel` | `h2`, `h3`, `h4`... | Nível do cabeçalho HTML do título, para encaixar na hierarquia da sua página. |
| `classe` | qualquer nome | Acrescenta uma classe CSS ao bloco, para você estilizar pela folha de estilo do seu site. |

Exemplo — um card de Encarregado sem título nem descrição, porque a página já tem uma seção "Fale com o Encarregado" escrita à mão em volta dele:

```
[v3rlgpd_dpo titulo="nao" descricao="nao"]
```

Exemplo — a lista de documentos com o título no nível certo para não competir com o `<h2>` da seção "Transparência" da página, e uma classe para ajustar o espaçamento pelo CSS do site:

```
[v3rlgpd_politicas nivel="h3" classe="transparencia-lista"]
```

> ⚠️ **`descricao="nao"` também esconde o título, se você não pedir `titulo="sim"`**
>
> Quando você não informa `descricao`, ela **acompanha** o que acontece com `titulo` — se o título some, a descrição some junto. Isso é o comportamento de sempre: quem já usava `titulo="nao"` antes destes atributos existirem continua vendo exatamente o mesmo resultado, sem precisar mexer em nada.

> 🚫 **Exceção: o canal de denúncia**
>
> No `[v3rlgpd_denuncia]`, `descricao="nao"` **não** esconde o aviso de que a denúncia anônima não é permitida e a identificação é obrigatória — porque esse texto não é apoio, é condição de uso. Escondê-lo faria alguém preencher o formulário acreditando estar anônimo. Veja [Canal de denúncia](/eca-digital/canal-de-denuncia/#o-aviso-de-identificação-não-é-ocultável).

Estes quatro atributos valem para a maioria dos blocos — **não** valem para `[v3rlgpd_politica]` (o texto e o título de um documento único são controlados pelo atributo `modo`, não por estes), `[v3rlgpd_selo]`, `[v3rlgpd_privacidade]` (a Central completa) nem para a gestão embutida no site. Nesses quatro, o layout continua sendo o de sempre.

## Depois de publicar

1. Adicione o link da Central ao **menu** e/ou ao **rodapé** do site, para o titular achar com facilidade.
2. Confira que sua **Política de Privacidade** está **ativa** (senão a Central aparece sem política).
3. Ative o **banner de cookies** se o site usa análise/marketing (veja [Consentimento & Cookies](/modulos/consentimento/)).

> ✅ **Boas práticas**
>
> Um link de "Privacidade" no rodapé de todas as páginas é o padrão que o público espera. Facilita o exercício de direitos e demonstra transparência.
