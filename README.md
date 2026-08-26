# Manual externo — V3RLGPD

Site Jekyll ([just-the-docs](https://just-the-docs.com/)) do **Manual do Usuário / Guia da LGPD** do V3RLGPD. Publicado em **https://docs.v3rlgpd.v3rtech.com.br/** via GitHub Pages.

> Frente NOSSA (V3RTECH) — desacoplada do plugin. O plugin apenas **linka** para este endereço. Método em `dev-history/manual-externo-metodo.md`. Backlog: BL-025 (#10).

## Como é publicado

Este repositório (**[V3RTECH-DF/V3RLGPD-Manual](https://github.com/V3RTECH-DF/V3RLGPD-Manual)**) é o clone editado diretamente — não há mais espelhamento a partir de um `docs-publicos/` dentro do repo do plugin. O conteúdo é editado aqui mesmo (`Manual/`, na raiz do clone) e publicado pelo script `Projeto/bin/publish-manual.sh`, que faz commit + push do próprio clone e garante o `CNAME`. O GitHub Actions deste repo (`.github/workflows/pages.yml`) builda o Jekyll e publica no GitHub Pages a cada push.

```bash
Projeto/bin/publish-manual.sh           # commita + empurra o pendente em Manual/ (Actions publica)
Projeto/bin/publish-manual.sh -n        # dry-run (mostra o que mudaria, sem push)
```

O `CNAME` (domínio próprio) e o workflow ficam versionados aqui, na raiz deste repo.

## Rodar localmente

```bash
cd Manual
bundle install
bundle exec jekyll serve
# abre em http://127.0.0.1:4000
```

## Estrutura

- `index.md` — capa com grade de módulos.
- `primeiros-passos.md`, `conceitos-lgpd.md`, `passo-a-passo-conformidade.md`, `papeis.md` — onboarding + mini-curso de LGPD.
- `modulos/` — referência por módulo do plugin (com capturas).
- `guias/` — passo a passo por tarefa/papel.
- `faq.md`, `legal.md`, `novidades.md`, `roadmap.md`, `disclaimer.md` — seções fixas.
- `assets/screenshots/` — capturas do ambiente (prefixo `v3rlgpd-*`).
- `_sass/color_schemes/v3rlgpd.scss` — paleta V3R.

## Capturas de tela

Os PNGs `v3rlgpd-*` foram capturados do ambiente DEV. Para recapturar após mudanças de UI, veja o roteiro na front-matter de cada página (campo `screenshots:`) e o script de captura em `dev-history/` (sessão de criação do manual). A skill **docs-keeper** sinaliza prints possivelmente obsoletos via a front-matter; a recaptura é disparada pela skill **user-manual**.

## Manutenção

A partir daqui, a manutenção incremental é da **docs-keeper** (não captura tela). A front-matter de cada página (`task`, `role`, `routes`, `screenshots`, `last_verified`, `status`) é o contrato de handoff.
