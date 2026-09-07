# Roteiro de recaptura — manual V3RLGPD (#19)

Ambiente: dev-wp `http://localhost:3080/wp-admin/` · plugin ativo + semeado · viewport **desktop 1920×1080** (padrão atual; telas cheias = página inteira com 1920 de largura; recortes = elemento capturado do render 1920) salvo indicado. Nomes de arquivo = os atuais (não mudar). Captura via e2e-runner (login DEV autorizado).

## Lote 1 — Admin, capturável JÁ (com o admin atual + seed) — ~44 prints

### Painel / Primeiros Passos
- `v3rlgpd-01-dashboard` — Dashboard (menu V3RLGPD)
- `v3rlgpd-01b-dashboard-selo` — Dashboard, card de conformidade com o selo/medalha abaixo do anel
- `v3rlgpd-40-anpd-news` — Dashboard, bloco "Notícias da ANPD" (rolar até o fim)
- `v3rlgpd-40-onboarding-card` — Dashboard, card "Primeiros Passos"
- `v3rlgpd-41-onboarding-roteiro` — tela Onboarding (checklist)

### Auditoria de Conformidade
- `v3rlgpd-50-mapa-conformidade` — Mapa de Conformidade
- `v3rlgpd-90-detector` — aba Detector (relatório)
- `v3rlgpd-33-mapeamento-formularios` — Verificador de Formulários (lista)
- `v3rlgpd-34-verificador-relatorio` — Verificador, relatório de um form
- `v3rlgpd-38-ropa-rascunho-formulario` — form → ROPA rascunho
- `v3rlgpd-39-google-forms` — cadastro/leitura Google Forms

### Políticas
- `v3rlgpd-02-policies` — lista de políticas
- `v3rlgpd-03-policy-editor` — editor de política (abrir a de Privacidade)
- `v3rlgpd-03b-policy-externa` — política externa (source_type external)
- `v3rlgpd-09-wizard` — Assistente de Políticas
- `v3rlgpd-11-templates` — galeria de modelos

### Inventário (ROPA) + Assistente
- `v3rlgpd-06-ropa` — lista ROPA
- `v3rlgpd-34-assistente-intro` — Assistente de Inventário, intro
- `v3rlgpd-35-assistente-perguntas` — Assistente, questionário
- `v3rlgpd-37-assistente-conclusao` — Assistente, conclusão

### Atendimento ao Titular
- `v3rlgpd-04-dsar` — lista de atendimentos
- `v3rlgpd-04c-dsar-detalhe-auto` — detalhe DSAR com "Responder automaticamente"
- `v3rlgpd-04d-dsar-banner-revisar` — banner "revisar" no detalhe
- `v3rlgpd-05-incidents` — lista de incidentes

### Retenção
- `v3rlgpd-30-retencao-fila` — fila de retenção
- `v3rlgpd-31-retencao-config` — config de retenção
- `v3rlgpd-32-ropa-retencao` — retenção por atividade do ROPA

### Ações do Encarregado
- `v3rlgpd-dpo-01-lista` — lista
- `v3rlgpd-dpo-02-form` — formulário (modal)
- `v3rlgpd-dpo-03-relatorio` — relatório imprimível

### Relatórios
- `v3rlgpd-10-compliance-report` — Relatório de Conformidade

### ECA
- `v3rlgpd-54-eca-mapa-triagem` — Mapa, seção ECA (triagem)

### Configurações
- `v3rlgpd-08-settings-dpo`, `08b-settings-cookies`, `08c-settings-webhooks`, `08d-settings-paginas`, `08e-settings-saida`, `08f-settings-aparencia`, `08g-settings-aparencia-custom`, `08h-settings-desinstalacao`, `08i-settings-import`, `69-config-encarregado`, `70-encarregado-autofill`

### Equipe/Acessos (admin)
- `v3rlgpd-60-equipe-acessos`, `61-equipe-toast`, `68-admin-menu-completo`, `71-acessos-distincao`, `72-papeis-cargos`, `73-editor-matriz`, `74-excluir-migracao`

### Feedback
- `v3rlgpd-30-feedback` — modal de feedback (já rebrandizado #18)

## Lote 2 — Precisa de USUÁRIOS COM PAPÉIS (setup) — 6 prints
Exige criar 2 usuários WP com papéis V3RLGPD e logar como eles:
- Auditor: `v3rlgpd-62-auditor-menu`, `63-auditor-ropa`, `64-auditor-settings`
- Atendente: `v3rlgpd-65-atendente-menu`, `66-atendente-dsar`, `67-atendente-incidentes`

## Lote 3 — Páginas PÚBLICAS (setup) — 6 prints
Exige publicar as páginas públicas do plugin (Central de Privacidade com shortcodes) + habilitar o banner de cookies:
- `v3rlgpd-72-central-encarregado` — Central de Privacidade (pública)
- `v3rlgpd-22-dsar-form` — formulário de direitos (público)
- `v3rlgpd-21-cookie-banner` — banner de cookies (front público)
- `v3rlgpd-53-ropa-publico-grid` — ROPA público (grid)
- `v3rlgpd-55-formulario-menores` — formulário de menores (público)
- `v3rlgpd-04b-dsar-declaracao-escopo` — (admin config; pode ir no Lote 1)

## Estados especiais a garantir no seed antes de capturar
- Selo dourado/medalha visível (índice de conformidade > limiar) para `01b`.
- Pelo menos 1 DSAR aberto informativo p/ o botão "Responder automaticamente" (`04c`).
- 1 política publicada como página p/ Central (`72-central`).

## Lote de recaptura — mudanças v1.47.0 → v1.51.2 (2026-07-13)

> Só as telas que **de fato** mudaram. Mesmos nomes de arquivo (sobrescrever). Captura via e2e-runner (login DEV autorizado) — a skill não autentica.

**Prioridade (conteúdo desatualizado):**
- `v3rlgpd-69-config-encarregado` — **Configurações → Encarregado SEM o campo "Prefixo de Versionamento"** (removido no #34). Print atual mostra o campo que não existe mais.
- `v3rlgpd-03b-policy-externa` — editor de **política Externa** com o novo seletor **"Ou escolha uma página publicada do site"** abaixo do campo de URL (#27).

**Valor médio (feature nova visível):**
- `v3rlgpd-10-compliance-report` — Relatório de Conformidade com o botão **"Baixar PDF"** (#21/#29).
- `v3rlgpd-dpo-03-relatorio` — Relatório de Ações do Encarregado com **"Baixar PDF"**.
- (ROPA/RIPD) — telas de relatório do Inventário e do RIPD finalizado com **"Baixar PDF"** (nomes atuais dos prints de ROPA/RIPD).
- *(Opcional)* incluir um print de um **PDF gerado** (cabeçalho com logo) como ilustração — novo asset, nomear `v3rlgpd-XX-relatorio-pdf`.

## Lote de recaptura — v1.74.0, ciência de documentos passa a funcionar (2026-09-07)

> Telas novas desta versão, sem print ainda. Ambiente: `dev-wp`, login DEV do Bruno. Precisa de: 1 documento externo com "Exigir ciência" ligado e versão preenchida, e ao menos 1 documento antigo com "Exigir ciência" desligado (para o aviso de documentos legados aparecer na lista).

- `v3rlgpd-97-ciencia-externa-versao-obrigatoria` — editor de política **externa**, "Exigir ciência" marcado, campo Versão Atual em destaque (obrigatório). Se der para capturar a mensagem de erro ao tentar salvar sem versão, melhor ainda.
- `v3rlgpd-98-ciencia-endereco-mudou` — diálogo **"O endereço mudou, mas a versão continua a mesma"**, ao salvar um documento externo trocando a URL sem trocar a versão. Referenciado em `guias/exigir-ciencia-documento.md`.
- `v3rlgpd-99-ciencia-documentos-antigos` — lista de **Políticas**, aviso de documentos legados no topo (contagem + checkboxes + botão "Exigir ciência para N selecionado(s)"). Referenciado em `guias/exigir-ciencia-documento.md`.
- *(opcional, baixo valor)* `v3rlgpd-100-ciencia-sem-permissao` — tela **Ciência de documentos** no estado "Você não tem permissão…", para ilustrar a distinção com "Nenhum registro ainda" (exige logar com um papel sem acesso a esse módulo).

**Baixo valor (polish; recapturar só se sobrar tempo):**
- `v3rlgpd-dpo-02-form` e demais **modais** — botão "X" de fechar maior (#28). Diferença sutil; só recapturar oportunisticamente.

## Lote de recaptura — navegação em barra única, v1.73.0 (2026-09-07)

> **A maior defasagem de imagem que o manual já teve de uma vez.** O menu do V3RLGPD no WordPress deixou de ter 8 entradas no menu lateral e passou a ter 1 (a navegação virou uma barra horizontal dentro da própria tela do plugin, com segunda barra para os itens com abas). **Praticamente toda captura de tela cheia do wp-admin mostra o menu lateral antigo, o cabeçalho antigo, ou os dois** — e não corresponde mais à tela. Quem for recapturar precisa saber disso antes de começar: não é lote pontual, é a base inteira do wp-admin.

**Afetados — todo print de tela cheia do wp-admin** (menu lateral com as 8 entradas antigas e/ou cabeçalho antigo do plugin, hoje substituídos pela barra horizontal):

`01-dashboard`, `01b-dashboard-selo`, `02-policies`, `03-policy-editor`, `03b-policy-externa`, `04-dsar`, `04b-dsar-declaracao-escopo`, `04c-dsar-detalhe-auto`, `04d-dsar-banner-revisar`, `05-incidents`, `06-ropa`, `08-settings-dpo` a `08i-settings-import` (todo o bloco 08), `09-wizard`, `10-compliance-report`, `11-templates`, `30-feedback`, `30-retencao-fila`, `31-retencao-config`, `32-ropa-retencao`, `33-mapeamento-formularios`, `34-assistente-intro`, `34-verificador-relatorio`, `35-assistente-perguntas`, `37-assistente-conclusao`, `38-ropa-rascunho-formulario`, `39-google-forms`, `40-anpd-news`, `40-onboarding-card`, `41-onboarding-roteiro`, `50-mapa-conformidade`, `54-eca-mapa-triagem`, `60-equipe-acessos`, `61-equipe-toast`, `62-auditor-menu`, `63-auditor-ropa`, `64-auditor-settings`, `65-atendente-menu`, `66-atendente-dsar`, `67-atendente-incidentes`, `68-admin-menu-completo`, `69-config-encarregado`, `70-encarregado-autofill`, `71-acessos-distincao`, `72-papeis-cargos`, `73-editor-matriz`, `74-excluir-migracao`, `75-ropa-transferencia-mecanismo`, `90-detector`, `91-detector-rastreador-origem`, `92-config-licenca`, `95-document-types`, `96-document-types-remove`, `97-dashboard-opens`, `98-ropa-multi-base`, `99-licenca-sem-ativar`, `dpo-01-lista`, `dpo-02-form`, `dpo-03-relatorio`.

Prioridade máxima dentro deste lote: `01-dashboard`, `68-admin-menu-completo`, `62/65-auditor-menu/atendente-menu` (esses três **mostram o menu** explicitamente — são os que mais enganam quem olhar a imagem) e `60-equipe-acessos`/`73-editor-matriz` (referenciados pela nova seção sobre acesso por endereço direto).

**Também afetados — página de Gestão no site** (ganhou a mesma barra de navegação do painel): `80-gestao-dashboard`, `81-gestao-mapa`, `82-gestao-ropa`, `83-gestao-politicas`, `84-gestao-dashboard-mobile`. Este lote já mostrava uma barra de abas própria; confirmar que ficou visualmente igual à do painel antes de aceitar como "sem mudança".

**Não afetados — páginas públicas, sem chrome do wp-admin** (Central de Privacidade, banner de cookies, formulário de direitos, ROPA público, formulário de menores): `100-central-resumo-fechado-desktop`, `101-central-resumo-aberto-desktop`, `102-central-documento-externo`, `103-cookies-escolha-vigente`, `104-cookies-sem-escolha`, `21-cookie-banner`, `22-dsar-form`, `30-ciencia-toggle`, `31-ciencia-banner`, `32-ciencia-relatorio`, `53-ropa-publico-grid`, `55-formulario-menores`, `72-central-encarregado`. Não recapturar por causa desta mudança — só se algo mais os tiver alterado.

Sem captura nesta rodada (dispensada). Front-matter das páginas afetadas **não foi tocada** (`last_verified` mantido) — os prints continuam os mesmos arquivos, só desatualizados; atualizar `last_verified` só depois da recaptura de fato.

## Possível recaptura — gestão no site ancorada (#93, #99, ainda não lançada — 2026-09-07)

O bundle da gestão no site (#70) passou a ancorar o próprio CSS (ADR-050 em `ARCHITECTURE.md`), corrigindo um vazamento em que o fundo dos controles de um bloco público (Central de Privacidade, formulário de solicitação, listagem de documentos) sumia quando a página também trazia a gestão embutida. Mudança de comportamento interno, sem alteração de layout na gestão isolada — os prints `80-gestao-*` a `84-gestao-*` não deveriam ter mudado.

Vale conferir, se algum print existente mostrar a combinação gestão + bloco público na mesma página, se ele capturava o defeito (fundo apagado do bloco público) — nesse caso, recapturar. Não identificado nenhum print assim no roteiro atual; anotado aqui para o caso de existir um fora deste arquivo.

## Lote de recaptura — Shortcodes vira aba de Configurações (#102, ainda não lançada — 2026-09-07)

A navegação de primeiro nível vai de **oito itens para sete**: Shortcodes deixa de ser item próprio e passa a ser **aba dentro de Configurações**, entre Acessos e Licença. Quem não tem `settings.view` deixa de enxergar essa aba (ela herda a guarda de Configurações). ⚠️ Nos papéis atuais isso é **só o Atendente** — o Auditor tem leitura de todos os módulos, `settings` incluído, então continua enxergando (o corpo da #102 dizia "Atendente e Auditor" e estava errado).

**Afetados:**
- `v3rlgpd-68-admin-menu-completo` — mostra a barra de navegação com os itens de primeiro nível; hoje mostra oito, precisa mostrar sete.
- Todo o bloco `08-settings-*` (`08-settings-dpo` a `08i-settings-import`) — a barra de abas dentro de Configurações ganha uma aba nova (`shortcodes`) entre Acessos e Licença; qualquer print que mostre essa barra de abas por inteiro fica incompleto sem ela.
- `v3rlgpd-62-auditor-menu` e `v3rlgpd-65-atendente-menu` — mostram a barra de primeiro nível, que cai para sete itens. ⚠️ Atenção ao que cada um prova: o **Auditor alcança Configurações** (e portanto a aba Shortcodes); o **Atendente não**. Se o par for usado para ilustrar diferença de acesso, é essa a diferença — não "nenhum dos dois chega lá".
- Página de Gestão no site (`80-gestao-*` a `84-gestao-*`) — **não afetada**: Shortcodes já não aparecia ali (mesma lista de exclusão de sempre, junto com Configurações).

**Novo print a considerar (nunca existiu um específico da tela de Shortcodes isolada no roteiro atual):** a aba Shortcodes dentro de Configurações, mostrando o catálogo — útil para ilustrar onde ela passou a morar.

Não capturado nesta rodada — entra no lote acumulado de recaptura (junto com a navegação em barra única e a gestão no site ancorada, acima), a ser tratado por agente próprio.

## Lote de recaptura — retenção do ROPA confrontada com o expurgo real (#79, ainda não lançada — 2026-09-07)

A tela da atividade do inventário (ROPA) ganha o confronto entre o prazo de retenção declarado e o expurgo automático real, com três estados possíveis: dá para ligar e está desligado; está ligado e não alcança nada; não há como automatizar, e a organização registra como o expurgo é feito fora do sistema.

**Afetados:**
- Editor de atividade do ROPA, seção de retenção — ganha o confronto e, quando aplicável, o campo de registro do expurgo externo. Nenhum print existente do editor do ROPA cobre essa seção com o comportamento novo.

Não capturado nesta rodada — entra no lote acumulado de recaptura, a ser tratado por agente próprio.

## Lote de recaptura — aviso de documentos legados ganha ação em lote "não exige ciência" (#109, ainda não lançada — 2026-09-07)

O aviso de documentos legados (tela de Políticas) muda de texto e ganha uma ação em lote nova: decidir que os documentos selecionados **não** exigem ciência, sem ligar nada. Documentos onde essa decisão já foi tomada somem do aviso.

**Afetados:**
- Tela de Políticas, banner do aviso de documentos legados — texto e opções mudaram; qualquer print existente que mostre esse banner fica desatualizado.

Não capturado nesta rodada — entra no lote acumulado de recaptura, a ser tratado por agente próprio.

## Lote de recaptura — Detector ganha estado de falha (#108, ainda não lançada — 2026-09-07)

A tela do Detector (varredura que confere o site publicado) ganhou um **estado novo**: análise que falhou por falta de progresso, com explicação do que houve. Antes só existiam "analisando" (girando) e "concluído" — o estado de falha não existia, e uma varredura travada ficava indefinidamente em "analisando" sem nenhuma tela própria para isso.

**Afetados:**
- `90-detector` — se o print atual mostra só os estados "analisando" e "concluído", fica incompleto: falta o estado de falha novo.

**Novo print a considerar (nunca existiu um específico deste estado no roteiro atual):** o Detector no estado de falha, mostrando a explicação — útil para ilustrar o que o usuário vê quando a varredura desiste.

Não capturado nesta rodada — entra no lote acumulado de recaptura (junto com os itens acima), a ser tratado por agente próprio.

## Executado — 2026-09-07, recaptura do painel (32 prints)

Ambiente: `dev-wp` (`localhost:3080`), v1.74.1 + as entregas #93/#99 e #102 ainda não publicadas. Desktop 1920×1080, página inteira.

**Capturados (26, sessão de administrador):** `01-dashboard`, `02-policies`, `04-dsar`, `05-incidents`, `06-ropa`, `08-settings-dpo`, `08b-settings-cookies`, `08c-settings-webhooks`, `08d-settings-paginas`, `08e-settings-saida`, `08f-settings-aparencia`, `10-compliance-report`, `11-templates`, `30-retencao-fila`, `31-retencao-config`, `33-mapeamento-formularios`, `41-onboarding-roteiro`, `50-mapa-conformidade`, `60-equipe-acessos`, `68-admin-menu-completo`, `90-detector`, `92-config-licenca`, `95-document-types`, `dpo-01-lista`, `dpo-03-relatorio` e **`105-shortcodes-aba`** (novo — a aba Shortcodes dentro de Configurações, entre Equipe/Acessos e Licença).

**Capturados antes, na mesma rodada (6, papéis):** `62-auditor-menu`, `63-auditor-ropa`, `64-auditor-settings`, `65-atendente-menu`, `66-atendente-dsar`, `67-atendente-incidentes` — com usuários descartáveis, já removidos.

⚠️ **Numeração:** o print da aba Shortcodes ficou como `105`, e não como `97/98/99` que este roteiro pedia para as telas de ciência — aqueles números **já pertencem** a prints existentes e não relacionados (`97-dashboard-opens`, `98-ropa-multi-base`, `99-licenca-sem-ativar`). Quem for capturar a ciência de documentos deve usar números livres a partir de `106`, e não os do texto acima.

### Armadilhas desta rodada — ler antes de recapturar o resto

1. **Endereço com aba (`?tab=`) exige recarga.** Entre dois endereços que só diferem no fragmento, o navegador não recarrega, e a tela de Configurações lê a aba pedida apenas ao montar. Sem recarga forçada, **as nove telas de Configurações saem todas mostrando a mesma aba** — aconteceu, e só apareceu ao abrir as imagens. A conferência que pega isso é exigir que a aba pedida esteja ativa antes de disparar.
2. **Dado pessoal real aparece na tela de Equipe/Acessos** (nome e e-mail de quem administra). Anonimizar no DOM antes do disparo, nunca editar a imagem depois.
3. **Aviso de plugin de terceiro no topo.** O WordPress **realoca** avisos para dentro da área do plugin, então ele fica na nossa própria árvore. **Não tente removê-lo por parentesco de DOM** — três tentativas levaram junto, em graus diferentes, o conteúdo da tela, e uma delas produziu 26 prints em branco. O caminho seguro é fechar pelo botão do próprio aviso e, no que sobrar, apenas esconder.
4. **Verifique o conteúdo, não a altura da raiz.** Numa das tentativas o conteúdo inteiro foi removido, a raiz sobreviveu com altura de sobra, a checagem passou e o print saiu em branco.

### Ainda pendente

O restante do lote da navegação em barra única (editores e assistentes, telas com estado especial), as telas novas de **ciência de documentos**, e o lote de páginas públicas. O texto do manual ainda não foi revisado para a navegação nova — instruções do tipo "clique em Shortcodes no menu" continuam desatualizadas.
