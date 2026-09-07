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
