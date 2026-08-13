---
title: "Retenção & Expurgo"
nav_order: 9
parent: "Módulos"
permalink: /modulos/retencao/
role: encarregado
routes: ["#/retention", "#/forms", "#/settings"]
screenshots: [v3rlgpd-30-retencao-fila, v3rlgpd-31-retencao-config, v3rlgpd-32-ropa-retencao, v3rlgpd-33-mapeamento-formularios]
last_verified: 2026-08-13
status: publicado
---

# Retenção & Expurgo

A LGPD diz que dado pessoal **não se guarda para sempre**: ele deve ser eliminado (ou anonimizado) quando a finalidade que justificou a coleta se encerra (art. 15 e 16). O módulo de **Retenção & Expurgo** automatiza esse ciclo de vida: ao fim do prazo que **você** define, o V3RLGPD **anonimiza** o registro — preservando a prova de que cumpriu a regra — sempre com uma **janela de aviso** e a chance de o Encarregado **cancelar ou adiar** antes de qualquer ação irreversível.

[![Fila de Retenção](/assets/screenshots/v3rlgpd-30-retencao-fila.png)](/assets/screenshots/v3rlgpd-30-retencao-fila.png)
*A Fila de Retenção mostra cada registro agendado, de onde veio, a data prevista e quantos dias faltam — com as ações Adiar e Cancelar.*

> ⚖️ **Automação de apoio, não substituto jurídico**
>
> O plugin executa o que **você** configura. Quem decide *quais* dados entram na retenção e *por quanto tempo* é a organização, conforme a base legal e a finalidade de cada tratamento. O V3RLGPD **ajuda** a cumprir a regra e a documentar — não garante validade jurídica nem isenta a organização de responsabilidade. Veja o [Aviso legal](/disclaimer/).

## Como funciona, em uma frase

Todo dia, em segundo plano, o plugin verifica o que está perto de vencer, **avisa** o Encarregado com antecedência (7 dias por padrão), e — se ninguém cancelar ou adiar — **anonimiza** no dia previsto, registrando tudo na auditoria.

## Anonimizar, não apagar

A ação padrão é **anonimização**, não exclusão pura.

- Nos dados **do próprio V3RLGPD** (atendimentos concluídos, consentimentos revogados), o registro **nunca** é apagado: apaga-se o que identifica a pessoa (e-mail, IP) e **preserva-se a prova** (tipo, datas, versão) — é o que sustenta a sua *accountability* perante a <a href="https://www.gov.br/anpd/pt-br" target="_blank" rel="noopener noreferrer">ANPD</a>.
- Em dados de **sistemas externos** (ex.: uma entrada de formulário de um plugin que só permite deletar), remover a entrada **é** a ação de retenção. Nesse caso o V3RLGPD guarda apenas uma **referência sem dado pessoal** (um identificador genérico + data + origem) como comprovante de que a regra foi cumprida.

> 💡 **Por que anonimizar em vez de só apagar**
>
> Apagar tudo deixaria você **sem prova** de que cumpriu a LGPD. Anonimizar elimina o risco para o titular (não há mais como identificá-lo) **e** mantém o registro de que a obrigação foi cumprida no prazo. É o melhor dos dois mundos.

## Os arquivos enviados também são apagados

Quando um formulário aceita **anexos** — um currículo em PDF, uma foto, um comprovante —, o arquivo enviado fica guardado no servidor do site, separado da resposta. Ele é dado pessoal como qualquer outro.

Ao descartar uma entrada de formulário pela regra de retenção, o V3RLGPD **apaga também os arquivos que vieram junto com ela**. Vale para **Forminator**, **Fluent Forms**, **WPForms**, **Gravity Forms** e **Elementor Forms**.

O mesmo passou a valer para os **anexos de resposta dos atendimentos**: os documentos que o Encarregado anexa ao responder um pedido de titular também costumam conter dados pessoais e, quando o atendimento é descartado pela retenção, **são apagados junto**.

> ⚠️ **Se você usava versões anteriores**
>
> Antes desta correção, o descarte apagava a resposta mas **deixava o arquivo anexado no servidor** — ou seja, o currículo continuava lá depois de o cadastro ter sido eliminado. Isso foi corrigido daqui para frente, mas **arquivos que ficaram para trás em descartes anteriores continuam no servidor**: se o seu site já rodou a retenção em formulários com anexo, vale pedir à equipe de implantação uma limpeza da pasta de arquivos desses formulários. Veja [Novidades](/novidades/).

## Onde se configura

A retenção tem **dois lugares** de configuração, conforme a origem do dado.

### 1. Configurações → Retenção & Expurgo (dados do próprio plugin)

[![Configurações de Retenção](/assets/screenshots/v3rlgpd-31-retencao-config.png)](/assets/screenshots/v3rlgpd-31-retencao-config.png)
*O interruptor geral, a janela de aviso e os prazos dos dados do próprio V3RLGPD.*

Aqui ficam:

- **Interruptor geral** da retenção automática (o "mestre" — se desligado, nada é expurgado).
- **Janela de aviso** — com quantos dias de antecedência o Encarregado é avisado antes do expurgo (padrão: **7 dias**).
- **Aviso por e-mail ao Encarregado** (opcional) — além do alerta dentro do painel.
- **Prazos dos dados do plugin:**
  - **Atendimentos (DSAR) concluídos** — padrão **24 meses**.
  - **Consentimentos revogados** — padrão **6 meses**.

### 2. Inventário (ROPA) → por atividade (dados do seu site)

Os dados do **site** (usuários, comentários, pedidos do WooCommerce, entradas de formulários) entram na retenção **atividade por atividade**, dentro do [Inventário (ROPA)](/modulos/inventario-ropa/). Na atividade você liga o interruptor de retenção, escolhe o **prazo** (valor + unidade) e o **conector** que sabe encontrar e anonimizar aqueles registros.

[![Seção de Retenção no ROPA](/assets/screenshots/v3rlgpd-32-ropa-retencao.png)](/assets/screenshots/v3rlgpd-32-ropa-retencao.png)
*Dentro de cada atividade do inventário há uma seção de Retenção: liga/desliga, prazo e conector.*

> ⚠️ **Nada entra na retenção sem você ligar (opt-in)**
>
> Nenhuma atividade do ROPA é expurgada automaticamente a menos que o Encarregado **ligue** explicitamente e escolha conector + prazo. Isso protege os dados que **devem** ser mantidos — por exemplo, um pedido com **obrigação fiscal** de guarda por 5 anos.

## Conectores: o que o V3RLGPD sabe expurgar

Um **conector** é a "ponte" que sabe encontrar e anonimizar um tipo de dado. O plugin já vem com conectores para as origens mais comuns:

| Origem | O que cobre |
|---|---|
| Atendimentos (V3RLGPD) | pedidos de titular já concluídos |
| Consentimentos (V3RLGPD) | consentimentos que foram revogados |
| Usuários do WordPress | contas por papel (ex.: assinantes inativos) |
| Comentários do WordPress | comentários antigos |
| WooCommerce | clientes e pedidos (respeitando prazo fiscal) |
| Formulários | CF7, Fluent Forms, Forminator, Gravity Forms, WPForms, **Elementor Forms** — entradas enviadas (e os arquivos anexados a elas) |

> 💡 **Extensível por design**
>
> Outros sistemas podem registrar seus próprios conectores no mesmo "encaixe", sem reescrever o módulo. Se um conector não estiver presente, as atividades ligadas a ele ficam apenas **inertes** (sem dar erro), e o painel sinaliza isso.

## Mapeamento de Formulários: o atalho de quem tem muitos forms

Se o seu site tem dezenas de formulários, montar o ROPA "de trás para frente" é mais fácil: a tela **Mapeamento de Formulários** lista **todos** os formulários publicados e deixa você ligar cada um a uma **atividade** do inventário.

[![Mapeamento de Formulários](/assets/screenshots/v3rlgpd-33-mapeamento-formularios.png)](/assets/screenshots/v3rlgpd-33-mapeamento-formularios.png)
*Cada formulário do site pode ser vinculado a uma atividade do ROPA — ou ficar de fora da retenção.*

- Vários formulários de **mesma finalidade** caem na **mesma** atividade (o ROPA continua sendo **por finalidade**, não por formulário — veja [Inventário](/modulos/inventario-ropa/#modele-por-finalidade-não-por-formulário)).
- **Cada formulário fica em um só vínculo de retenção** — a tela avisa se você tentar colocá-lo em dois (prazo ficaria ambíguo).
- Formulário **sem** atividade = **não** entra em retenção (padrão seguro). A tela mostra um contador de "N formulários ainda sem atividade" como empurrão de conformidade.

> ⚠️ **Formulário que mistura finalidades**
>
> Um único formulário usado para fins diferentes só admite **um** prazo. A recomendação é **um formulário por finalidade**; se estiver misturado, use o prazo **mais conservador (mais longo)** até conseguir separá-lo.

## A Fila de Retenção

A aba **Retenção** (no grupo **Atendimento ao Titular**) mostra a **fila**: tudo que está agendado para expurgo, com origem, data prevista (em UTC) e "faltam X dias". Para cada item o Encarregado pode:

- **Adiar** — escolher uma nova data (ex.: o titular pediu para manter o cadastro mais tempo). O motivo fica registrado na auditoria.
- **Cancelar** — tirar o registro da fila. O motivo também é auditado. (Pode ser reativado depois, alterando a configuração.)

Quando há registros perto de vencer, o **Painel** exibe um alerta — *"Há N registro(s) agendado(s) para expurgo em breve"* — com link direto para a fila.

> ✅ **Boas práticas**
>
> - Confira a fila **antes** de cada vencimento — a janela de aviso existe exatamente para isso.
> - Ao **adiar**, registre um motivo claro: ele é a sua justificativa documentada.
> - Comece **conservador**: ligue a retenção primeiro nas atividades de menor risco (comentários, leads antigos) e só depois nas mais sensíveis.

## A revogação de consentimento, de verdade

Quando um atendimento do tipo **"Revogação de Consentimento"** é concluído, o V3RLGPD marca **de fato** os consentimentos daquele e-mail como revogados — e é essa data que dá início ao prazo de retenção desses consentimentos. Ou seja: o pedido do titular não fica só "no papel"; ele dispara o ciclo de vida do dado.

## O que isso significa para o titular dos dados

- Seus dados **não ficam guardados indefinidamente**: há um prazo, e ao fim dele eles deixam de identificar você.
- Quando você **revoga um consentimento**, isso conta — passa a valer um prazo para que esses dados sejam anonimizados.
- A organização mantém apenas a **prova de que cumpriu a regra**, sem manter os dados que identificam você.

## Perguntas frequentes

**O expurgo é imediato?**
Não. Há sempre uma **janela de aviso** (7 dias por padrão) antes da ação. Nesse período o Encarregado pode adiar ou cancelar. Nada irreversível acontece sem esse intervalo.

**Posso perder um dado que ainda preciso guardar (ex.: nota fiscal)?**
Não por acidente: **nada entra na retenção automática sem você ligar** a atividade explicitamente. Dados com obrigação legal de guarda (fiscal, contábil) só são expurgados se você optar por isso — e a recomendação é **não** ligar a retenção neles.

**Anonimizar é o mesmo que apagar?**
Não. Anonimizar **remove o que identifica** a pessoa, mas pode **preservar a prova** de que o tratamento existiu e foi encerrado no prazo. É o recomendado pela LGPD para conciliar o direito do titular com a *accountability* da organização.

**O arquivo que a pessoa anexou ao formulário some junto?**
Sim. O descarte apaga a entrada **e** os arquivos enviados com ela (currículos, comprovantes, fotos). O mesmo vale para os documentos que o Encarregado anexa ao responder um atendimento.

**Uso o formulário do Elementor. Ele entra na retenção?**
Entra, desde que você use o **Elementor Pro** — o formulário só existe na versão paga. Ele aparece no Verificador de Formulários, pode ser vinculado a uma atividade do Inventário e é descartado como os demais, com anexos e tudo.

**E se o sistema externo não souber anonimizar?**
Para entradas de plugins de terceiros que só permitem **deletar**, a remoção da entrada **é** a ação de retenção. O V3RLGPD guarda apenas uma referência **sem dado pessoal** como comprovante.

**O que acontece se um conector for desinstalado?**
As atividades ligadas a ele ficam **inertes** — não dão erro e não expurgam nada — e o painel sinaliza a situação para você reconfigurar.

**Onde vejo o histórico do que foi expurgado?**
Toda ação (agendar, cancelar, adiar, anonimizar, falha) é registrada na **auditoria** do plugin, com autor e data. As ações automáticas aparecem como `system` (o robô diário); as manuais, com o e-mail do Encarregado.

**Preciso configurar um "cron" no servidor?**
O plugin usa o agendador do próprio WordPress e reforça a execução quando você acessa o painel. Para sites de baixo tráfego, peça à sua equipe de implantação para configurar um **cron de sistema** — assim o expurgo roda no horário certo mesmo sem visitas.

> ⚠️ **Atenção a dados sensíveis**
>
> Atividades que tratam **dados sensíveis** (saúde, religião, etnia) exigem cuidado redobrado nos prazos e nas bases legais. Reveja-as com apoio jurídico antes de automatizar o expurgo.
