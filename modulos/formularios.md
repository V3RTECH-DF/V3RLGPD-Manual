---
title: "Verificador de Formulários"
nav_order: 8
parent: "Módulos"
permalink: /modulos/formularios/
role: encarregado
routes: ["#/forms"]
screenshots: [v3rlgpd-33-mapeamento-formularios, v3rlgpd-34-verificador-relatorio, v3rlgpd-38-ropa-rascunho-formulario, v3rlgpd-39-google-forms]
last_verified: 2026-08-13
status: publicado
---

# Verificador de Formulários

A aba **Verificador de Formulários** — dentro do grupo **Inventário (ROPA)** — faz duas coisas: **analisa os campos** de cada formulário do seu site para apontar possíveis problemas de conformidade, e liga cada formulário a uma **atividade** do [Inventário (ROPA)](/modulos/inventario-ropa/).

[![Verificador de Formulários](/assets/screenshots/v3rlgpd-33-mapeamento-formularios.png)](/assets/screenshots/v3rlgpd-33-mapeamento-formularios.png)
*A lista mostra cada formulário do site, com um status de conformidade e os botões para verificar e mapear.*

> 💡 **Editar o formulário sem sair da tela**
>
> Cada formulário na lista traz um link **✏️ Editar formulário**, que abre o **construtor do formulário** (no seu plugin de formulários) em uma **nova aba**. Útil para corrigir uma pendência — por exemplo, adicionar um checkbox de consentimento — sem perder os resultados da verificação.

## Por que verificar os formulários

É comum uma organização acumular formulários no site — alguns antigos, anteriores à LGPD — que coletam dados pessoais **sem consentimento**, ficam **fora do inventário** ou tratam dados de **crianças/adolescentes** sem o cuidado devido. O verificador ajuda você a **encontrar esses casos** para tratá-los.

> ⚠️ **A ferramenta aponta, não corrige — e é consultiva**
>
> A análise é **automática e baseada em pistas** (o nome e o tipo de cada campo): ela diz que um campo *parece* dado pessoal, e cabe a **você confirmar e tratar**. Ela **não corrige** os formulários e **não substitui** orientação jurídica.

## Verificar a conformidade

[![Relatório do verificador](/assets/screenshots/v3rlgpd-34-verificador-relatorio.png)](/assets/screenshots/v3rlgpd-34-verificador-relatorio.png)
*O relatório lista os campos identificados como dados pessoais (com selo de "sensível") e os problemas para o Encarregado tratar.*

1. Na tela, clique em **Verificar** num formulário (ou em **🔎 Verificar todos**).
2. O **relatório** abre mostrando:
   - **Campos com dados pessoais identificados** — os campos que *parecem* dado pessoal, com um selo **SENSÍVEL** quando o campo sugere dado de categoria especial (saúde, religião etc.).
   - **Problemas identificados** — entre eles:
     - **Sem checkbox de consentimento** — o formulário coleta dados pessoais e não tem um campo de consentimento.
     - **Fora do Inventário (ROPA)** — o formulário não está mapeado a uma atividade com base legal. Aqui você tem **duas saídas**: **vincular** a uma atividade já existente (seletor da linha) ou **[gerar uma atividade nova a partir dos campos](#criar-a-atividade-do-ropa-a-partir-do-formulário)**.
     - **Indícios de dados de menores** sem campo/consentimento de pais ou responsáveis.
     - **Indícios de dados sensíveis**, que exigem cuidado e consentimento específico.
3. O **status** de cada formulário na lista mostra ✅ sem pendências, ⚠️ com pendências, ou ⏳ não verificado.

### O resultado fica salvo

Depois de verificar, **o resultado fica guardado**: se você trocar de tela (ou for gerar um ROPA a partir de um formulário) e voltar, o status de cada formulário **continua lá** — com a indicação **"verificado em DD/MM/AAAA HH:MM"** — sem precisar verificar tudo de novo. Cada formulário já verificado mostra:

- **Ver relatório** — reabre o último resultado salvo (sem refazer a análise).
- **Reverificar** — refaz a análise e atualiza a data (use quando mudar o formulário ou quiser conferir de novo).

> 💡 Se você **vincular** o formulário a uma atividade do ROPA (ou **gerar um ROPA** a partir dele), o apontamento "fora do Inventário (ROPA)" some **automaticamente** ao voltar à tela — sem precisar reverificar.

### Marcar um achado como revisado

Avaliou um apontamento e concluiu que está tudo certo (ou é um falso alarme)? Clique em **Marcar como revisado** (com uma nota opcional). O achado fica **esmaecido** e deixa de contar como pendência. Você pode **Desfazer** quando quiser.

> 💡 **A revisão "expira" se o formulário mudar**
>
> A revisão vale para a **versão atual** dos campos do formulário. Se alguém **editar** o formulário (adicionar ou trocar campos), a revisão é **descartada** e o achado reaparece — para você conferir de novo, já que o formulário não é mais o mesmo.

## Criar a atividade do ROPA a partir do formulário

Quando o relatório aponta **Fora do Inventário (ROPA)** e **ainda não existe** uma atividade para aquele formulário, você pode criar uma **em um clique**, já pré-preenchida com o que os campos revelam.

[![Rascunho de ROPA a partir do formulário](/assets/screenshots/v3rlgpd-38-ropa-rascunho-formulario.png)](/assets/screenshots/v3rlgpd-38-ropa-rascunho-formulario.png)
*O rascunho abre o editor do Inventário já preenchido: categorias de dados, origem, e — quando há pistas — finalidade e base legal marcadas como "sugestão — confirme".*

1. No relatório, no apontamento **Fora do Inventário (ROPA)**, clique em **✨ Gerar rascunho de ROPA a partir dos campos**.
2. O **editor do Inventário** abre **pré-preenchido**:
   - **Dados Pessoais Coletados** — as categorias detectadas (Nome, E-mail, Telefone…).
   - **Origem dos Dados** — já marcado como "Formulário do site".
   - **Base Legal** — sugere **"Consentimento do titular"** *se* o formulário tem um checkbox de consentimento; senão fica **em branco**.
   - **Finalidade** — sugerida a partir do **nome do formulário** quando ele se parece com uma atividade conhecida; senão fica em branco.
   - **Avisos** — se houver indício de **dado sensível** ou de **menores**, aparece um aviso (com atalho ao [RIPD](/modulos/ripd/) e a opção de marcar consentimento parental).
3. **Revise tudo.** Os itens marcados **"sugestão — confirme"** são palpites do sistema; os campos em branco (como **Categorias de Titulares**) você completa.
4. Clique **Salvar Registro**. O V3RLGPD cria a atividade **e já vincula** o formulário a ela — a pendência **Fora do Inventário** desaparece na próxima verificação.

> ⚠️ **A ferramenta sugere; você decide**
>
> O rascunho é um **ponto de partida**, não uma decisão pronta. A **base legal** sugerida (consentimento) precisa da sua confirmação, e nada substitui a sua análise — especialmente quando há dados sensíveis ou de crianças/adolescentes.

> 💡 **Já existe a atividade?** Então não crie outra: use o **seletor da linha** para **vincular** o formulário à atividade existente (próxima seção). Crie uma nova só quando ainda não houver.

## Formulários do Elementor

Quem monta as páginas com o **Elementor Pro** costuma usar o **widget de formulário** dele — e esses formulários agora recebem o mesmo tratamento dos demais:

- Aparecem na **lista** do verificador, junto com os formulários dos outros plugins.
- São **verificados** normalmente: campos com dados pessoais, selo de **sensível**, falta de checkbox de **consentimento** e ausência no **Inventário (ROPA)**.
- Podem gerar um **rascunho de ROPA** a partir dos campos, ou ser **vinculados** a uma atividade existente.
- Entram na **[retenção/expurgo](/modulos/retencao/)** e são alcançados pelo **atendimento ao titular** (Localizar e Eliminar), com os arquivos anexados incluídos.

> ⚠️ **Só o Elementor Pro tem formulário**
>
> A versão gratuita do Elementor **não inclui** o widget de formulário. Se o seu site usa o Elementor Free, não há formulários dele para verificar aqui — os seus formulários vêm de outro plugin.

> 💡 **No Elementor, o formulário é o widget**
>
> Diferente dos outros plugins, o Elementor não tem uma "lista de formulários" separada: cada formulário **é um bloco dentro de uma página**. Na lista, ele aparece com o **nome que você deu ao formulário** no Elementor; se o formulário estiver sem nome, aparece como *"título da página — Elementor"*.
>
> Como o formulário não é uma página própria, **não há botão de edição direta** para ele nesta tela (ao contrário dos outros plugins): para alterar os campos, abra a página no editor do Elementor e edite o bloco do formulário ali.

## Formulários do Google (Google Forms)

Muitas organizações usam **Google Forms** para inscrições, doações e pesquisas. Como eles ficam **fora do WordPress**, o V3RLGPD precisa que você os **aponte** — e então os trata como qualquer outro formulário: verifica a conformidade e ajuda a montar o Inventário (ROPA).

[![Google Form no Verificador](/assets/screenshots/v3rlgpd-39-google-forms.png)](/assets/screenshots/v3rlgpd-39-google-forms.png)
*Um Google Form aparece na lista com o selo "Externo (Google)", o aviso sobre retenção e as ações próprias (abrir, reler, editar campos, remover).*

**Duas formas de adicionar:**

1. **+ Adicionar Google Form** — cole a **URL pública** do formulário (`docs.google.com/forms/…` ou `forms.gle/…`). O V3RLGPD **lê os campos automaticamente** da página do formulário (sem precisar de login na sua conta Google).
2. **🔍 Procurar no site** — o V3RLGPD **varre as páginas publicadas** do seu site atrás de Google Forms que você tenha incorporado ou linkado, e os adiciona sozinho.

Depois de adicionado, o Google Form ganha o selo **"Externo (Google)"** e estas ações: **Abrir formulário** (vê o formulário no Google, em nova aba), **Reler campos** (atualiza a leitura, caso você tenha mudado o formulário), **Editar campos** (informa os campos à mão — ver abaixo) e **Remover**.

> ⚠️ **A retenção automática não cobre o Google**
>
> Os dados respondidos num Google Form ficam **nos servidores do Google** (na planilha de respostas). O V3RLGPD **não consegue apagá-los** — então a **retenção/expurgo automático não se aplica** a esses formulários. Você pode (e deve) **inventariá-los no ROPA** para conformidade, mas a exclusão dos dados precisa ser feita **no próprio Google**. A tela deixa esse aviso visível na linha do formulário.

> 💡 **Se a leitura automática não funcionar**
>
> Alguns formulários são privados ou exigem login, e o Google muda a estrutura interna de tempos em tempos. Se o V3RLGPD não conseguir ler os campos, o formulário entra com o aviso **"NÃO LIDO"** — aí use **Editar campos** para informar os campos à mão (um por linha; para um checkbox de consentimento, escreva `rótulo | checkbox`). A partir daí ele verifica normalmente.

> 🔒 **Privacidade:** o V3RLGPD lê apenas a **estrutura** do formulário (os rótulos e tipos dos campos) — **nunca as respostas** das pessoas. A leitura é feita com proteção contra acessos indevidos a endereços internos (SSRF).

## Mapear o formulário ao Inventário (ROPA)

Todo formulário que coleta dados pessoais faz parte de **alguma** atividade de tratamento. Vincular o formulário à atividade certa mantém o [Inventário (ROPA)](/modulos/inventario-ropa/) fiel à realidade e permite que a **retenção automática** saiba o que expurgar e quando (ver [Retenção & Expurgo](/modulos/retencao/)).

1. Para cada formulário, escolha no seletor a **atividade do ROPA** correspondente.
2. Para tirar o vínculo, escolha **"-- Remover Vínculo --"**.

> 💡 **Vários formulários, uma atividade**
>
> O ROPA é organizado **por finalidade**, não por formulário. Se vários formulários coletam os mesmos dados para o mesmo fim, eles pertencem à **mesma** atividade — aponte todos para um único registro, sem inflar o inventário.

> ⚠️ **Um vínculo por formulário**
>
> Cada formulário deve pertencer a **uma** atividade (senão o prazo de retenção fica ambíguo). Um formulário que mistura finalidades deveria ser separado; enquanto não for, use a atividade de prazo **mais longo**.

> ✅ **Boas práticas**
>
> Ao instalar um plugin de formulário novo ou criar um formulário, reserve alguns minutos para **verificar** e **mapear** aqui. Manter isso em dia é o que faz o inventário, a retenção e a conformidade trabalharem a seu favor.

➡️ Para configurar **prazos** e ligar a retenção, veja **[Retenção & Expurgo](/modulos/retencao/)**.
