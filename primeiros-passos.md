---
title: "Primeiros Passos"
nav_order: 2
permalink: /primeiros-passos/
screenshots: [v3rlgpd-01-dashboard, v3rlgpd-40-onboarding-card, v3rlgpd-41-onboarding-roteiro]
last_verified: 2026-06-23
status: publicado
---

# Primeiros Passos

Esta página leva sua organização do "plugin recém-instalado" ao "pronto para atender a LGPD" em poucos passos. Você não precisa ser advogado nem técnico — só seguir a ordem. E, desde a versão 1.2, o próprio plugin **conduz você por esse roteiro** com um assistente de Primeiros Passos.

> 💡 **Por que isso importa**
>
> A maior parte das multas e dores de cabeça com a LGPD não vem de ataques sofisticados: vem de **falta de organização básica** — não ter quem responda pelos dados, não conseguir mostrar a política que estava no ar, demorar para responder um pedido. Os primeiros passos abaixo resolvem justamente esse básico, que é onde uma organização mais ganha proteção com menos esforço.

## Onde fica o V3RLGPD

Depois de instalado e ativado no seu site WordPress, o plugin aparece no menu lateral do painel administrativo como **um único item: V3RLGPD**. Se o seu site tem outros produtos da nossa casa instalados, essa entrada aparece **agrupada com a deles** no menu, em vez de espalhada entre os demais plugins. Ao abrir, você vê o **Painel de Conformidade e Privacidade**, e toda a navegação passa a acontecer **dentro dessa tela**, numa **barra horizontal no alto** — os mesmos **7 itens** de sempre, na mesma ordem: **Painel**, **Auditoria de Conformidade**, **Inventário (ROPA)**, **Relatório de Impacto (RIPD)**, **Políticas**, **Atendimento ao Titular** e **Configurações**.

Quando você está num item que tem subdivisões — **Auditoria de Conformidade** (*Detector* e *Mapa de Conformidade*), **Inventário (ROPA)** (*Inventário* e *Verificador de Formulários*) ou **Atendimento ao Titular** (*Consentimentos, Atendimentos, Denúncias, Incidentes, Retenção* e *Ações do Encarregado*) — aparece uma **segunda barra** logo abaixo, com as abas daquele item. É o mesmo conteúdo de sempre: muda onde se clica, não o que existe.

> 💡 **Shortcodes não é mais um item próprio**
>
> O catálogo de shortcodes deixou de ter seu próprio item na navegação: hoje é uma **aba dentro de Configurações**, entre **Equipe / Acessos** e **Licença**. Só quem enxerga Configurações chega lá — veja [Configurações](/modulos/configuracoes/#shortcodes).

> 💡 **Favorito antigo continua funcionando**
>
> Se você tinha o endereço de uma tela específica salvo nos favoritos, ou volta a ela pelo histórico do navegador, o V3RLGPD te leva para a tela certa dentro da nova navegação. Não é preciso refazer nenhum favorito.

[![Painel do V3RLGPD](/assets/screenshots/v3rlgpd-01-dashboard.png)](/assets/screenshots/v3rlgpd-01-dashboard.png)
*O Dashboard é o cockpit da conformidade da sua organização.*

## O assistente de Primeiros Passos

Assim que você instala o plugin, o Dashboard exibe um **card de Primeiros Passos** mostrando quantas etapas básicas já estão prontas (ex.: "2 de 6 passos concluídos") e um botão **Continuar**.

[![Card de Primeiros Passos no Dashboard](/assets/screenshots/v3rlgpd-40-onboarding-card.png)](/assets/screenshots/v3rlgpd-40-onboarding-card.png)
*O card resume seu progresso e leva ao roteiro completo.*

Clicar em **Continuar** abre o **roteiro guiado**: uma lista de etapas, cada uma com uma explicação curta do "porquê", o estado (✅ concluído / ❌ pendente) e um botão que **leva direto à tela** que resolve aquele passo.

[![Roteiro guiado de Primeiros Passos](/assets/screenshots/v3rlgpd-41-onboarding-roteiro.png)](/assets/screenshots/v3rlgpd-41-onboarding-roteiro.png)
*Cada etapa tem um atalho para a tela certa; o que já está feito aparece marcado automaticamente.*

> 💡 **O roteiro reflete a realidade, sozinho**
>
> Você não marca nada à mão. O plugin **detecta automaticamente** o que já foi feito — se você cadastra o Encarregado, o passo vira ✅ na hora; se depois despublica a política, o passo correspondente **volta a pendente**. O roteiro nunca "mente" sobre o seu estado.

As etapas vêm em dois blocos:

- **Essenciais** — o básico que mais protege a organização: **Encarregado**, **Política de Privacidade** e **Central de Privacidade**.
- **Recomendados** — **Inventário (ROPA)**, **Consentimento / Cookies** e **Autodeclaração**.

Há ainda um passo **Bônus** (Retenção & Expurgo), opcional, que **não** conta para a conclusão dos 6 essenciais/recomendados.

> ✅ **Boas práticas**
>
> Você pode **dispensar** o card a qualquer momento ("Dispensar por agora") e reexibi-lo depois pelo link **"Reexibir Primeiros Passos"** no topo do Dashboard. O roteiro completo também fica sempre acessível. Não precisa fazer tudo num dia: cuide dos 3 essenciais primeiro.

> 🔁 **Revisão periódica**
>
> Depois de concluir os passos, passado um tempo (cerca de um ano), o plugin volta a sugerir uma **revisão** — para você reconferir se políticas, inventário e contatos seguem atualizados.

## O roteiro, passo a passo

Faça nesta ordem — cada passo destrava o próximo e faz o **Índice de Conformidade** do Dashboard subir.

### 1. Cadastre o Encarregado

Em **Configurações → Identidade**, informe o nome (ou setor) responsável, o e-mail de contato e, opcionalmente, o telefone. Esses dados aparecem publicamente na Central de Privacidade — é por eles que o titular vai falar com a sua organização.

➡️ Passo a passo detalhado em **[Configurar o Encarregado](/guias/configurar-dpo/)**.

### 2. Crie e publique a Política de Privacidade

Em **Políticas**, crie sua Política de Privacidade. Você pode escrever do zero, usar o **Assistente** (que pré-preenche com os dados do Encarregado e do inventário) ou partir de um modelo da **Galeria**. Ao final, **publique uma versão e marque-a como ativa** — só políticas ativas aparecem ao público.

➡️ Veja **[Publicar uma política](/guias/publicar-politica/)**.

### 3. Publique a Central de Privacidade

Em **Configurações → Páginas & Integração**, clique em **Gerar Página Automaticamente**. O plugin cria a página pública onde o titular lê as políticas, ajusta cookies e abre pedidos. O passo só fica ✅ quando a página está **publicada**.

➡️ Veja **[Publicar a Central de Privacidade](/guias/publicar-central-privacidade/)**.

### 4. Preencha o Inventário (ROPA)

Em **Inventário (ROPA)**, registre cada operação de tratamento de dados que sua organização faz: qual atividade, quais dados, para qual finalidade e com qual base legal. É a espinha dorsal da conformidade.

➡️ Entenda em **[Inventário (ROPA)](/modulos/inventario-ropa/)**. Se você tem muitos formulários no site, comece pelo **[Mapeamento de Formulários](/modulos/formularios/)**.

### 5. Ajuste o Consentimento / Cookies

Em **Configurações → Banner de Cookies**, decida se o **banner** será exibido e configure os scripts de análise/marketing. Veja **[Consentimento & Cookies](/modulos/consentimento/)**.

### 6. Responda à Autodeclaração

No Dashboard, clique em **Revisar Autodeclaração**. São perguntas simples (ex.: "as bases legais foram definidas?") que complementam o Índice de Conformidade com o que o plugin não consegue verificar sozinho.

## O Índice de Conformidade

No topo do Dashboard há um **Índice de Conformidade** em percentual, sobre **6 itens**, dividido em dois grupos:

- **Verificados pelo Sistema** — itens que o plugin confere sozinho: **Política ativa**, **Encarregado configurado**, **Central de Privacidade publicada**, **Consentimento / Cookies** (o banner ativo) e **Inventário preenchido**.
- **Autodeclarados** — itens que dependem da sua resposta na Autodeclaração (ex.: **bases legais mapeadas**).

O semáforo e o roteiro de Primeiros Passos usam **a mesma fonte** — então o que você vê num bate com o outro.

> ⚠️ **Atenção**
>
> O Índice é um **indicador de progresso interno**, não um certificado. Como o próprio painel avisa: *"não constitui garantia jurídica de conformidade com a LGPD"*. Use-o para se organizar, não para "provar" conformidade a terceiros.

## Próximo passo

Se você quer entender os conceitos da lei antes de continuar, vá para **[Conceitos da LGPD](/conceitos-lgpd/)**. Se prefere o roteiro completo de adequação, veja **[O passo a passo da conformidade](/passo-a-passo-conformidade/)**.
