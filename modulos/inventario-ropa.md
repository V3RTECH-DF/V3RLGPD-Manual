---
title: "Inventário (ROPA)"
nav_order: 7
parent: "Módulos"
permalink: /modulos/inventario-ropa/
role: encarregado
routes: ["#/ropa", "#/ropa/report", "#/ropa/assistant"]
screenshots: [v3rlgpd-06-ropa, v3rlgpd-34-assistente-intro, v3rlgpd-35-assistente-perguntas, v3rlgpd-37-assistente-conclusao, v3rlgpd-75-ropa-transferencia-mecanismo, v3rlgpd-98-ropa-multi-base]
last_verified: 2026-09-05
status: publicado
---

# Inventário (ROPA)

O **Inventário de Tratamento** — também chamado de **ROPA**, sigla de *Registro das Operações de Tratamento* (em inglês, *Records of Processing Activities*) — é o registro de **todas as operações** em que sua organização trata dados pessoais. É a espinha dorsal da conformidade.

[![Inventário ROPA](/assets/screenshots/v3rlgpd-06-ropa.png)](/assets/screenshots/v3rlgpd-06-ropa.png)
*Cada registro descreve a atividade, os dados pessoais, a base legal e se há transferência internacional.*

## Assistente de Inventário

Nunca fez um inventário e não sabe por onde começar? Use o **✨ Assistente de Inventário** (botão no topo da tela do Inventário). Em vez de encarar um formulário em branco cheio de termos técnicos, você **responde perguntas simples** e o assistente monta um rascunho do seu ROPA para você revisar.

[![Assistente de Inventário — perguntas](/assets/screenshots/v3rlgpd-35-assistente-perguntas.png)](/assets/screenshots/v3rlgpd-35-assistente-perguntas.png)
*O assistente pergunta o que a sua organização faz; cada "sim" vira um rascunho de atividade pré-preenchido.*

Como funciona, em poucos passos:

1. **Perguntas em linguagem leiga** — "envia newsletter?", "recebe doações?", "cadastra voluntários?", "vende online?"… A cada **sim**, o assistente seleciona uma atividade pronta, com finalidade, **base legal sugerida**, dados coletados e prazo de retenção.
2. **Crianças e adolescentes** — há uma pergunta no topo: se a sua organização atende menores de 18, as atividades pertinentes marcam os titulares como "Crianças e adolescentes" e o assistente orienta sobre **consentimento parental** e **RIPD**.
3. **Vínculo com formulários** — para atividades que vêm de formulários do site, você pode escolher **quais formulários alimentam a atividade** ali mesmo. Pode marcar **mais de um**, inclusive de **origens diferentes** (ex.: um Forminator e um Google Forms na mesma atividade). Veja [Mapeamento de Formulários](/modulos/inventario-ropa/) e [Retenção](/modulos/retencao/).
4. **Revisão antes de salvar** — o assistente mostra os rascunhos para você **editar, remover ou confirmar**. Base legal e prazo são **sugestões a conferir** — a definição final é responsabilidade da sua organização. Nada é gravado sem o seu "Criar registros".
5. **Rodar de novo é seguro** — o assistente **nunca apaga** o que você já tem; ao rodar de novo, ele identifica as atividades existentes e cria **apenas as novas**.

[![Assistente — conclusão com recomendação de RIPD](/assets/screenshots/v3rlgpd-37-assistente-conclusao.png)](/assets/screenshots/v3rlgpd-37-assistente-conclusao.png)
*Ao concluir, se você criou atividades com dados de menores, o assistente recomenda elaborar um RIPD (art. 16 da LGPD + ECA) com atalho direto para o módulo.*

> ⚠️ O assistente **ajuda** a montar o inventário com base em modelos comuns de diferentes segmentos; ele **não** substitui a análise da sua organização. Sempre revise as sugestões, especialmente a **base legal**.

## O que registrar em cada atividade

- **Atividade** — o que sua organização faz (ex.: "Cadastro de voluntários", "Newsletter de doadores").
- **Dados Pessoais** — quais dados são coletados (nome, CPF, telefone, e-mail…).
- **Base Legal** — o fundamento que autoriza o tratamento (execução de contrato, consentimento, obrigação legal…). **Aceita mais de uma marcada ao mesmo tempo** — o mesmo padrão do campo Origem dos Dados, logo abaixo. É obrigatório marcar ao menos uma. Veja [Conceitos](/conceitos-lgpd/#as-bases-legais-art-7º-e-11).

  [![Campo Base Legal com múltiplas opções marcadas](/assets/screenshots/v3rlgpd-98-ropa-multi-base.png)](/assets/screenshots/v3rlgpd-98-ropa-multi-base.png)
  *Uma atividade pode se apoiar em mais de uma base — aqui, Execução de contrato e Legítimo interesse ao mesmo tempo.*

  > 📖 **Exemplo (grupo escoteiro)**
  >
  > O cadastro de um voluntário pode se apoiar em **execução de contrato** (o termo de voluntariado que ele assina) **e** em **cumprimento de obrigação legal** (o registro que a lei do voluntariado exige). Marcando as duas, a atividade fica mais fiel ao que realmente acontece — em vez de forçar uma escolha única e artificial entre elas.

  > 💡 **A sugestão de retenção usa a primeira base com sugestão**
  >
  > Quando mais de uma base está marcada, o prazo de retenção sugerido automaticamente vem da primeira base (na ordem da lista) que tiver uma sugestão associada — e só preenche o campo se ele estiver vazio ou ainda tiver a sugestão anterior. É um palpite editável, não uma regra: se você já digitou um prazo à mão, ele não é sobrescrito.
- **Transferência Internacional** — se os dados saem do Brasil (ex.: um serviço hospedado no exterior). Ao marcar essa opção, você informa também o **país(es) de destino** e o **mecanismo de proteção (art. 33)** — a base legal que permite os dados saírem do Brasil. Na dúvida, para fornecedores dos Estados Unidos ou da Europa, o mais comum é **"Cláusulas-padrão contratuais"**. Há ainda um campo opcional **"Detalhe da garantia"** para anotar, por exemplo, a cláusula ou a certificação que sustenta a transferência. Esse mecanismo aparece nos relatórios e é usado pelo [Assistente de Políticas](/modulos/politicas/) para redigir a cláusula de transferência internacional.

[![Campos de transferência internacional com o mecanismo de proteção do art. 33](/assets/screenshots/v3rlgpd-75-ropa-transferencia-mecanismo.png)](/assets/screenshots/v3rlgpd-75-ropa-transferencia-mecanismo.png)
*Ao marcar a transferência internacional, você escolhe o mecanismo de proteção do art. 33.*

> 💡 **Por que isso importa**
>
> O inventário é o documento que **mais** trabalha a seu favor. É dele que sai a resposta a "quais dados você tem sobre mim?", a justificativa de um tratamento perante a <a href="https://www.gov.br/anpd/pt-br" target="_blank" rel="noopener noreferrer">ANPD</a> e o conteúdo automático da Política de Privacidade. **Se sua organização fizer só uma coisa da LGPD, que seja manter o inventário.**

## Modele por finalidade, não por formulário

Este é o segredo para o inventário **não virar um monstro**. O ROPA registra **atividades de tratamento** — definidas pela **finalidade** —, e **não** cada formulário, planilha ou tela isoladamente.

> 💡 **Por que isso importa**
>
> Uma organização com 20 formulários no site não precisa de 20 registros no inventário. **Vários formulários que coletam os mesmos dados para a mesma finalidade são uma única atividade** — logo, **um único registro**. Isso é, ao mesmo tempo, o jeito **correto** de fazer o ROPA e o que torna o trabalho viável.

> 📖 **Exemplo (grupo escoteiro)**
>
> | Atividade no ROPA (1 registro) | Cobre quais formulários | Base legal · retenção |
> |---|---|---|
> | Inscrição em eventos | todos os forms de acampamento/atividade | consentimento ou contrato · prazo curto |
> | Solicitação de reembolso | todos os forms de reembolso | obrigação legal/contrato · ~5 anos |
> | Protocolos administrativos | todos os forms de protocolo | conforme o caso |
> | Pesquisas de satisfação | todas as pesquisas | legítimo interesse · curtíssimo |
>
> De ~20 formulários para **~4-6 atividades**. Um evento novo? Você só **acrescenta o formulário à atividade que já existe** — sem criar registro novo.

> ⚠️ **A única regra de fidelidade**
>
> Só agrupe formulários que de fato compartilham **dados + finalidade + base legal**. Se um formulário coletar **dado a mais** — por exemplo, informação de **saúde** (dado sensível) num evento —, ele vira uma **atividade própria**, com base e retenção próprias.

## O inventário alimenta as políticas

Quando você usa o **Assistente** em [Políticas](/modulos/politicas/), ele puxa as atividades do inventário para montar a Política de Privacidade. Inventário bem feito = política mais fácil e mais fiel à realidade.

## Relatório do inventário

O botão **Gerar Relatório** abre o inventário como documento; ali o botão **Baixar PDF** baixa um arquivo PDF pronto (com logo e cabeçalho da organização) — útil para anexar a prestações de contas ou apresentar a um financiador.

> ✅ **Boas práticas**
>
> Construa o inventário **aos poucos**, uma atividade por vez, e **revise** quando algo mudar: nova campanha, novo sistema, novo tipo de dado. Inventário desatualizado dá falsa sensação de segurança.

> ⚠️ **Atenção a dados sensíveis**
>
> Ao registrar, marque mentalmente as atividades que envolvem **dados sensíveis** (saúde, religião, etnia, opinião política). Elas exigem bases legais específicas e cuidado redobrado — é onde o risco aos titulares é maior.

## Publicar o ROPA (vitrine de transparência)

A LGPD valoriza a **transparência**: o titular tem direito de saber, de forma clara, **o que** você trata e **por quê** (Art. 9). Você pode publicar uma **vitrine das suas atividades de tratamento** em qualquer página do site com o shortcode:

```
[v3rlgpd_ropa]
```

Ele exibe as atividades **ativas** com os campos seguros para o público: **atividade, dados pessoais (categorias), titulares, finalidade, base legal e retenção**.

[![Vitrine pública do ROPA](/assets/screenshots/v3rlgpd-53-ropa-publico-grid.png)](/assets/screenshots/v3rlgpd-53-ropa-publico-grid.png)

**Atributos:**

- `layout` — `lista` (padrão), `grid` ou `tabela`.
- `incluir` — campos opcionais a mostrar: `origem`, `operadores`, `transferencia`. Ex.: `[v3rlgpd_ropa layout="grid" incluir="operadores,transferencia"]`.
- `titulo` — `sim` (padrão) ou `nao` (oculta o cabeçalho).

Você também define o **padrão** (layout e campos opcionais) em **Configurações → Páginas & Integração**; os atributos do shortcode sobrescrevem esse padrão.

> ⚠️ **O que NUNCA vai a público**
>
> As **medidas de segurança** e os dados técnicos de integração **nunca** são exibidos pelo shortcode — expor isso seria entregar o mapa da mina. Campos como **operadores** e **transferência internacional** só aparecem se você **optar** por incluí-los. E só atividades **ativas** são publicadas.

> ✅ **Boas práticas**
>
> Comece pelo padrão (campos essenciais). Inclua "operadores" e "transferência internacional" só se fizer sentido para a sua transparência — lembrando que esses campos podem revelar seus fornecedores.
