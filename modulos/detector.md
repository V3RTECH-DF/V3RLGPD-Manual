---
title: "Detector de Conformidade"
parent: "Módulos"
nav_order: 1
permalink: /modulos/detector/
role: encarregado
routes: ["#/detector", "#/settings"]
screenshots: [v3rlgpd-90-detector, v3rlgpd-91-detector-rastreador-origem]
last_verified: 2026-07-17
status: publicado
---

# Detector de Conformidade

O **Detector de Conformidade** varre o seu site publicado e gera um **relatório em linguagem clara** apontando o que precisa de atenção na conformidade com a LGPD. A diferença para o resto do painel: ele confronta o que você **configurou** no V3RLGPD com o que está **de fato no ar** no seu site — o "espelho externo".

Fica na aba **Detector**, dentro de **Auditoria de Conformidade** (primeira aba).

[![Tela do Detector de Conformidade](/assets/screenshots/v3rlgpd-90-detector.png)](/assets/screenshots/v3rlgpd-90-detector.png)
*O Detector: escolha o modo, inicie a análise e leia o relatório por gravidade.*

> 💡 **Por que isso importa**
>
> Você pode ter configurado tudo certo no plugin, mas um detalhe no ar passar despercebido: uma tag de rastreamento que o tema instalou, a política que não está linkada no rodapé, a página do titular fora do ar. O Detector encontra essas lacunas do jeito que um auditor externo (ou a <a href="https://www.gov.br/anpd/pt-br" target="_blank" rel="noopener noreferrer">ANPD</a>) veria.

## Como rodar uma análise

1. Abra **Auditoria de Conformidade → Detector**.
2. Escolha o **modo**:
   - **Rápido** — checa o essencial (página inicial + Central de Privacidade). Resultado na hora.
   - **Padrão** — início, Central e páginas institucionais.
   - **Completo (análise profunda)** — varre **todo o site**. Roda em segundo plano: você pode **sair da página e voltar mais tarde**, e recebe um **e-mail** quando terminar.
3. Clique em **Iniciar análise**.

> No modo Completo, enquanto a análise roda, a tela mostra o progresso ("X de Y páginas"). O e-mail de conclusão vai para quem iniciou a análise **e** para o Encarregado.

### Quando a análise falha

Uma análise pode **não terminar**. Se ela parar de avançar — por exemplo, o site fica indisponível no meio da varredura, ou uma página trava o processo —, o Detector **desiste e explica o que houve**, em vez de ficar girando indefinidamente em "analisando".

Na tela, isso aparece como **"A análise não terminou"**, com a orientação de **escolher um modo acima e tentar novamente**. O número de páginas que chegaram a ser analisadas antes da desistência fica visível — ele ajuda a distinguir "não saiu do lugar" de "parou no meio".

*(captura pendente — estado de falha novo, sem print ainda; ver `_manual/roteiro-recaptura.md`)*

> ⚠️ **Análise que falhou não manda e-mail de resumo.** O aviso por e-mail avisado acima é só para análise **concluída**. Se você (ou o Encarregado) esperava o e-mail e ele não chegou, confira a tela do Detector antes de supor que a análise ainda está rodando — ela pode já ter desistido e estar esperando você tentar de novo.

Diante de uma falha, o caminho é **rodar de novo**: se o problema foi passageiro (uma instabilidade momentânea do site), a nova tentativa costuma terminar normalmente. Se falhar de novo, considere um modo mais leve (Rápido ou Padrão em vez de Completo) para isolar se o problema está numa página específica.

## Como ler o relatório

No topo, você vê a **situação geral** ("Atenção necessária", "Bom" ou "Excelente") e a contagem por gravidade:

- 🔴 **Crítico** — lacuna objetiva que um auditor apontaria (ex.: política inexistente, rastreador sem consentimento).
- 🟡 **Atenção** — algo a melhorar ou confirmar.
- 🟢 **Conforme** — item verificado que está em ordem.

Cada achado explica **o que encontramos**, **por que importa** (com o artigo da lei) e traz um botão **Resolver** que leva direto ao lugar certo do painel — **quando possível, já preenchido**. Você pode **ordenar** por gravidade, tema ou ordem alfabética, e **Exportar / Imprimir** o relatório (útil para levar ao conselho, a um financiador ou a um auditor).

## O caso dos rastreadores (cookies sem consentimento)

Um dos achados mais úteis: o Detector encontra **scripts de rastreamento** disparando no seu site **antes** do visitante consentir — geralmente porque foram colados direto no tema ou vêm de outro plugin. Ele reconhece os mais comuns: **Google Tag Manager, Google Analytics (GA4 e Universal), Meta Pixel (Facebook), Google Ads, LinkedIn Insight, TikTok Pixel, Hotjar e Microsoft Clarity**.

O Detector também **tenta identificar de onde o script vem**, cruzando os plugins que você tem ativos com o rastreador encontrado. Isso importa porque **muda o conselho**:

[![Achado de rastreador com a origem identificada](/assets/screenshots/v3rlgpd-91-detector-rastreador-origem.png)](/assets/screenshots/v3rlgpd-91-detector-rastreador-origem.png)
*Dois achados, dois conselhos: o de cima não tem origem identificada e oferece **Resolver**; o de baixo veio de um plugin com funcionalidade própria e, por isso, **não** oferece a importação.*

### Quando é só um trecho — importe

Se o script foi **colado no tema** ou está num injetor de código (WPCode, Header Footer Code Manager e afins), o trecho **é** a funcionalidade inteira. Clique em **Resolver**: o V3RLGPD leva o código já preenchido para a aba [Cookies & Analytics](/modulos/configuracoes/), onde ele passa a carregar **só após o consentimento**. Revise, salve — e **remova o trecho de onde estava**, senão ele dispara duas vezes. Nada se perde.

> 💡 **Vários rastreadores? Traga todos de uma vez**
>
> Ter mais de um é o normal (Tag Manager + Analytics + Pixel é a combinação típica). Quando há mais de um importável, aparece o botão **"Resolver todos"** acima da lista: ele traz todos juntos, você revisa tudo de uma vez e **salva uma vez só**.
>
> Os que **não devem** ser importados (os que vêm de plugins com funcionalidade própria — logo abaixo) ficam **de fora de propósito**, e o aviso diz quantos são.
>
> Prefere ir um a um? Também funciona: os scripts trazidos ficam **pendentes até você salvar**, então dá para ir e voltar entre o Detector e as Configurações sem perder nada. Se mudar de ideia, o botão **Descartar** no aviso desfaz a importação pendente.

### Quando vem de um plugin com funcionalidade própria — não importe

Se o rastreador vem de um plugin como **MonsterInsights, Site Kit, GTM4WP, PixelYourSite** ou similares, o Detector **não oferece o botão Resolver** — de propósito.

> ⚠️ **Por que não importar nesse caso**
>
> Esses plugins fazem **muito mais** do que emitir a tag: eles também rastreiam downloads e formulários, mandam os eventos de e-commerce com os dados da compra, montam o `dataLayer` e servem relatórios dentro do painel. Se você copiar só o trecho e desativar o plugin, **mantém a marcação básica e perde todo o resto — sem aviso nenhum**. A organização costuma descobrir meses depois, quando falta dado.
>
> O achado vai **nomear o plugin** e dizer **o que exatamente você perderia**. O caminho certo é usar a **configuração de consentimento do próprio plugin** (a maioria dos modernos tem). Se você não usa esses recursos extras, aí sim: remova o plugin e rode o Detector de novo.

> 💡 **Quem desativa plugin é você**
>
> O V3RLGPD **não desativa** plugins de terceiros, nem se oferece para isso. Não temos como saber o que quebraríamos no seu site — e essa decisão, com as consequências dela, é da sua organização. Nosso papel é dizer **o quê**, **por quê** e **o que você perde**, com precisão suficiente para você decidir.

### Quando não sabemos a origem

Se nenhum plugin conhecido bate com o rastreador, o Detector **diz isso** em vez de dar uma instrução vaga, e explica os dois caminhos acima para você identificar qual é o seu caso.

> ⚠️ **Não achar rastreador não significa que não há**
>
> O Detector reconhece a lista acima. Se a sua organização usa uma ferramenta que não está lá (Matomo, Plausible, Pinterest, Segment, um script próprio…), **ela não é detectada** — e o resultado "nenhum rastreador conhecido" **não garante** que o site esteja livre de rastreamento. Nesse caso, verifique manualmente.

> ⚠️ **O Detector ajuda, não garante**
>
> O relatório aponta pontos de melhoria e ajuda a organizar a conformidade, mas **não garante validade jurídica** nem **substitui a análise por um profissional**. Uma análise mais aprofundada da política (com apoio de inteligência artificial) está prevista para uma próxima versão.
