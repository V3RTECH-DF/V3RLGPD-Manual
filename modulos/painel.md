---
title: "Painel"
nav_order: 1
parent: "Módulos"
permalink: /modulos/painel/
role: encarregado
routes: ["#/", "#/wizard"]
screenshots: [v3rlgpd-01-dashboard, v3rlgpd-01b-dashboard-selo, v3rlgpd-50-mapa-conformidade, v3rlgpd-40-anpd-news, v3rlgpd-97-dashboard-opens]
last_verified: 2026-09-05
status: publicado
---

# Painel

O **Dashboard** é a primeira tela do V3RLGPD: o cockpit onde o Encarregado vê, de relance, como anda a conformidade da organização e o que falta fazer.

[![Dashboard do V3RLGPD](/assets/screenshots/v3rlgpd-01-dashboard.png)](/assets/screenshots/v3rlgpd-01-dashboard.png)
*Visão geral com Índice de Conformidade, indicadores de atendimentos e visualizações das políticas.*

## Índice de Conformidade (MVP)

O card mostra, de um lado, a **lista do que é verificado pelo sistema** (Política de Privacidade ativa, Encarregado configurado, Consentimento/Cookies, Central de Privacidade, Inventário) — cada item com o **artigo da LGPD** correspondente; do outro, um **anel** com o **percentual verificado** e, separado e em roxo, o indicador **"Atestado: X de 4"** (a parte autodeclarada, que **não** infla o percentual).

O selo **"ⓘ Por que isto importa (LGPD)"** abre uma explicação curta com o artigo da Lei e links para o Manual, o texto oficial (Planalto) e a <a href="https://www.gov.br/anpd/pt-br" target="_blank" rel="noopener noreferrer">ANPD</a>.

### O Selo de Conformidade no painel

[![Painel — Selo de Conformidade](/assets/screenshots/v3rlgpd-01b-dashboard-selo.png)](/assets/screenshots/v3rlgpd-01b-dashboard-selo.png)
*Abaixo do anel, o Selo de Conformidade (faixa bronze/prata/ouro) e o atalho para copiar o shortcode.*

Logo abaixo do anel aparece o **Selo de Conformidade** (o mesmo que você pode exibir publicamente no seu site), com a **faixa** correspondente ao seu nível (bronze, prata ou ouro). Ali também há a dica e o botão **Copiar** do shortcode `[v3rlgpd_selo]` — cole-o em qualquer página do site para mostrar o selo aos visitantes.

> O selo reflete o **mesmo índice** do anel e **não** é um certificado: comunica o seu compromisso, sem garantir validade jurídica.

> ℹ️ Os **atestados** (autodeclaração) e o detalhamento artigo a artigo ficam no **[Mapa de Conformidade](#mapa-de-conformidade)** — acesse pelo botão **"Ver mapa completo"** ou pelo menu.

> ℹ️ Se você **[inativar](/modulos/politicas/#inativar-e-reativar-uma-politica)** a Política de Privacidade, o item "Política de Privacidade Ativa" deixa de contar aqui — reative-a para o indicador voltar.

> ⚠️ **Atenção**
>
> O Índice é um **indicador de progresso interno**, não um certificado de conformidade. O próprio painel reforça: *"não constitui garantia jurídica de conformidade com a LGPD"*. Veja o [Aviso legal](/disclaimer/).

## Indicadores de atendimentos (DSAR)

Quatro números acompanham a saúde do atendimento aos titulares:

- **Pendentes (No Prazo)** e **Pendentes (Atrasadas)** — quantos pedidos aguardam e se estão dentro do SLA.
- **Concluídas** — pedidos já resolvidos.
- **Tempo Médio de Resposta** — quanto sua organização costuma levar.

Há ainda o **Ranking de Solicitações** (quais tipos de pedido mais aparecem) e o card **Aberturas de documentos**.

[![Painel — card Aberturas de documentos](/assets/screenshots/v3rlgpd-97-dashboard-opens.png)](/assets/screenshots/v3rlgpd-97-dashboard-opens.png)
*O card mostra o total de aberturas, a data em que a contagem começou e, quando já há dado suficiente, os documentos mais lidos.*

> ⚠️ **Este número mudou de natureza — não é só um nome novo**
>
> Antes, o painel contava **carregamentos de página**: um único contador global, que somava toda vez que a página pública com o shortcode de política carregava — inclusive de quem nunca chegou a ler nada, e inclusive de robôs passando pelo rodapé do site. Agora ele conta **abertura de documento**: o clique de alguém que efetivamente foi ler aquele documento específico, contado **por documento**.
>
> Por serem coisas diferentes, o número **recomeçou do zero** quando a mudança entrou — e é por isso que o card mostra a data de início da contagem. Se você abrir o painel e ver um número bem menor que o de antes, **não é perda de dado**: é uma métrica nova e mais fiel substituindo uma que inflava sozinha.
>
> A vantagem prática: agora dá para saber **quais documentos** são realmente lidos (a lista de mais abertos aparece no próprio card), não só que "alguma página carregou".

> ℹ️ **Documento interno também conta, desde que tenha o que abrir**
>
> Até pouco tempo, só o documento **externo** (por link) contava aqui, pelo clique em "Ler a política completa". Um documento **interno** exibido no modo "resumo" agora conta do mesmo jeito, pelo comando **"Ler na íntegra"** — veja [Central de Privacidade](/modulos/central-privacidade/#no-modo-resumo-ler-na-integra-abre-o-documento-sem-sair-da-pagina). Documento exibido só com o **título** não tem comando de abertura, então aparece zerado aqui — não é ausência de leitura, é ausência de clique possível.

> 💡 **Por que isso importa**
>
> Esses números são ótimos para **prestar contas**: mostram a financiadores e ao conselho que a organização atende titulares com agilidade e que seus documentos são efetivamente lidos. É accountability na prática — você demonstra cuidado com dados, não só afirma.

## Alertas e pendências

O painel sinaliza pontos de atenção — por exemplo, **nenhuma política de privacidade vigente** (com atalho para criar uma). São pistas do que organizar a seguir.

## Ações rápidas

No alto do painel:

- **Exportar Relatório** — abre o [Relatório de Conformidade](/modulos/relatorios/) em PDF.
- **Ver mapa completo** — abre o [Mapa de Conformidade](#mapa-de-conformidade) (detalhe artigo a artigo + autodeclaração).

## Mapa de Conformidade

Acessível pelo menu **"Mapa de Conformidade"** (ou pelo botão "Ver mapa completo"), é a tela-síntese que organiza a conformidade em **três camadas**, cada item ligado ao artigo da LGPD:

[![Mapa de Conformidade](/assets/screenshots/v3rlgpd-50-mapa-conformidade.png)](/assets/screenshots/v3rlgpd-50-mapa-conformidade.png)
*As três seções: o que o sistema verifica, o que você atesta e o que é responsabilidade sua fora da ferramenta.*

- ✅ **Verificado pelo sistema** — o que a ferramenta confere automaticamente, com status e atalho para resolver.
- 📝 **Você atesta** — as 4 autodeclarações sob responsabilidade da organização (contrato com operadores, treinamento, dados sensíveis, transferência internacional). Marque **Sim / Não / Não se aplica**.
- ⚪ **Sob sua responsabilidade** — deveres que acontecem **fora** do plugin (comunicar incidente à ANPD, avaliar o RIPD, responder a fiscalizações).

## Notícias da ANPD

Na seção superior do Painel, na **3ª coluna** (à direita do anel de conformidade), há um bloco **"📰 Notícias da ANPD"** com as **últimas manchetes** da Autoridade Nacional de Proteção de Dados (regulação, orientações, prazos, consultas públicas).

[![Notícias da ANPD no Painel](/assets/screenshots/v3rlgpd-40-anpd-news.png)](/assets/screenshots/v3rlgpd-40-anpd-news.png)
*A seção superior do Painel em três colunas: Índice de Conformidade, o anel de % com o selo, e as Notícias da ANPD. Cada manchete tem data e abre a matéria no site da ANPD em nova aba.*

- Cada manchete mostra a **data** e abre a notícia no **site da ANPD** (gov.br) em **nova aba**.
- O bloco é só informativo, para você **se manter atualizado** sem sair do painel — não coleta nem envia nenhum dado da sua organização.
- Se as notícias não carregarem (a fonte da ANPD pode ficar instável), o painel **continua funcionando normalmente** e o bloco mostra um link para o site da ANPD.

## Veja também

- [O passo a passo da conformidade](/passo-a-passo-conformidade/)
- [Relatórios & Backup](/modulos/relatorios/)
