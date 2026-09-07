---
title: "Exigir ciência de um documento"
nav_order: 7
parent: "Guias por tarefa"
permalink: /guias/exigir-ciencia-documento/
task: exigir-ciencia-documento
role: encarregado
routes: ["#/policies/edit/:id", "#/atendimento/acknowledgements"]
screenshots: [v3rlgpd-30-ciencia-toggle, v3rlgpd-31-ciencia-banner, v3rlgpd-32-ciencia-relatorio]
last_verified: 2026-09-07
status: publicado
---

# Exigir ciência de um documento

Quando um documento importante muda — o **estatuto**, uma **política**, os **termos** — você pode exigir que os usuários **tomem ciência da nova versão**, e o V3RLGPD guarda o registro de **quem** deu ciência, de **qual documento** e em **qual versão**.

É a prova de que a pessoa foi avisada da atualização — útil para governança e para o dia a dia de uma organização com membros.

## 1. Ligue o "Exigir ciência" no documento

1. Em **Políticas**, crie ou edite o documento (estatuto, política, termos…).
2. Marque **Exigir ciência dos usuários**.

[![Documento com a opção "Exigir ciência" marcada](/assets/screenshots/v3rlgpd-30-ciencia-toggle.png)](/assets/screenshots/v3rlgpd-30-ciencia-toggle.png)
*A opção fica no editor do documento. Já vem ligada para privacidade, termos e "outros"; para cookies vem desligada (eles já têm o banner de consentimento).*

> 💡 A ciência vale para **usuários logados** (por exemplo, os membros da sua organização). É a eles que o aviso aparece.

### Funciona para documento interno e externo

**Exigir ciência** vale tanto para um documento **redigido no editor do plugin** quanto para um documento **externo** (PDF, página de wiki, intranet — veja [Políticas › interna ou externa](/modulos/politicas/#política-interna-ou-externa-link)).

Para o **documento externo**, porém, o campo **Versão Atual (Manual)** deixa de ser opcional assim que você marca **Exigir ciência**. Sem um número de versão, não há o que registrar como "a versão que a pessoa confirmou" — e o plugin recusa salvar com a mensagem:

> *"Documento externo com ciência exigida precisa de uma versão informada."*

Preencha a versão (ex.: `2.1`, `jan/2026`) e salve novamente.

## 2. Publique uma nova versão

A ciência é **por versão**. Quando você [publica uma nova versão](/guias/publicar-politica/) de um documento que exige ciência e a define como **ativa**, todos os usuários que ainda não confirmaram aquela versão passam a ver o aviso.

### Documento externo: troque o arquivo, não esqueça de trocar a versão

Num documento **interno**, alterar o texto no editor já cria uma versão nova sozinho — não tem como esquecer. Num documento **externo**, quem troca o PDF (ou o link) é você, e o número de versão é **manual**: nada impede, na prática, de subir um arquivo novo mantendo escrito "versão 1.0".

O risco não é bobagem: se isso acontecesse sem aviso, todo mundo que já tinha confirmado a versão anterior continuaria marcado como **ciente de um texto que nunca leu** — uma prova falsa, e prova falsa numa auditoria é pior do que não ter prova nenhuma.

Por isso, quando o V3RLGPD detecta que o **endereço do documento mudou** mas a **versão anotada continuou a mesma**, ele **para e pergunta**, em vez de aceitar em silêncio:

> **"O endereço mudou, mas a versão continua a mesma"**
> A versão anotada continua **[a que estava lá]**, mas o endereço mudou. Isso deve ser tratado como uma versão nova? Quem já confirmou vai precisar confirmar de novo.

- **Sim, é versão nova** — o plugin abre uma nova versão de verdade: quem já tinha confirmado volta a ver o aviso.
- **Não, é o mesmo documento** — por exemplo, você só mudou o local onde o PDF está hospedado, o conteúdo é idêntico. O endereço é atualizado e ninguém precisa confirmar de novo.

*(captura pendente — dialogo novo, sem print ainda; ver `_manual/roteiro-recaptura.md`)*

## 3. O que o usuário vê

Ao navegar no site já logado, o usuário vê um **aviso no centro da tela** listando **todos** os documentos atualizados que ele ainda não confirmou. Cada um tem um link **abrir para ler** (em nova aba) e há **um único botão "Estou ciente"** que confirma todos de uma vez. Se preferir deixar para depois, **Agora não** fecha o aviso — ele volta no próximo acesso, até a ciência ser dada.

[![Aviso de novas versões de documentos](/assets/screenshots/v3rlgpd-31-ciencia-banner.png)](/assets/screenshots/v3rlgpd-31-ciencia-banner.png)
*Um aviso, vários documentos, um clique. Depois de confirmar, o aviso some e não volta — até sair uma nova versão.*

## 4. Veja quem já deu ciência

Em **Atendimento ao Titular → Ciência de documentos**, você acompanha quem confirmou cada documento, em qual versão e quando.

[![Relatório de ciência de documentos](/assets/screenshots/v3rlgpd-32-ciencia-relatorio.png)](/assets/screenshots/v3rlgpd-32-ciencia-relatorio.png)
*O registro fica guardado por usuário e por versão. Ele também entra na exportação de dados (take-out).*

> ⚠️ O aviso aparece só para quem está **logado**. Ele não captura a ciência de um visitante anônimo (por exemplo, no momento de um cadastro) — para esse caso, use o consentimento nos formulários.

### "Nenhum registro" e "sem permissão" agora aparecem diferentes

Se a tela mostrar **"Nenhum registro de ciência ainda"**, é porque ninguém confirmou nenhum documento ainda — não é erro. Se mostrar **"Você não tem permissão para ver os registros de ciência"**, o problema é de acesso: confira o papel do usuário em [Equipe / Acessos](/modulos/equipe-acessos/). As duas mensagens costumavam ser idênticas, o que fazia um problema de permissão passar despercebido por meses fantasiado de "ainda não tem dado".

## Se você já usava esta função antes

Se a aba de **Ciência de documentos** sempre esteve vazia mesmo com pessoas confirmando o aviso, é porque o registro das confirmações não estava sendo salvo — a caixa de diálogo aparecia e funcionava para quem via, mas nada ficava guardado do outro lado. Isso está corrigido: as confirmações passam a ser registradas normalmente a partir de agora.

Não há como reconstruir retroativamente confirmações que não chegaram a ser gravadas. Se você depende dessa prova para algum documento específico, o caminho é [publicar uma nova versão](/guias/publicar-politica/) dele (ou reabrir a ciência pelo bloco de [documentos cadastrados antes desta funcionalidade](#documentos-cadastrados-antes-desta-funcionalidade), se for o caso) — isso reabre o aviso para todo mundo e as novas confirmações passam a contar.

## Documentos sobre os quais ninguém decidiu ainda

Documento **publicado antes de existir "Exigir ciência"** ficou, naturalmente, com essa opção **desligada** — e sem ninguém ter decidido se deveria continuar assim. A lista de **Políticas** mostra, no topo, um aviso listando só os documentos **nessa situação de indecisão**: nem alguém ligou "Exigir ciência" neles, nem alguém registrou que eles não precisam exigir.

Para cada documento do aviso, você tem **duas saídas** — e as duas resolvem a pendência:

- **Passar a exigir ciência** — liga a exigência; a partir da próxima publicação (ou de imediato, se o documento já estiver ativo), os usuários logados que ainda não confirmaram passam a ver o aviso.
- **Registrar que não exige** — uma decisão explícita de que aquele documento **não precisa** de ciência (por exemplo, um relatório de atividades de anos atrás). Não liga nada; só documenta que a organização já avaliou e decidiu não exigir.

O aviso diz, no topo, quantos documentos **ainda não tiveram uma decisão sobre exigir ciência dos usuários** — e os dois botões são **"Exigir ciência para N selecionado(s)"** e **"Decidir que não exige para N selecionado(s)"**. Enquanto nenhum documento estiver marcado, os dois ficam desabilitados, e a tela avisa que é preciso **selecionar ao menos um documento acima para habilitar as ações**.

Marque, um a um ou todos de uma vez (**Selecionar todos**), e aplique a ação em lote correspondente. Assim que um documento recebe uma das duas decisões, ele **sai do aviso** — não volta a aparecer ali, porque deixou de ser um caso "ninguém decidiu ainda".

[![Aviso de documentos sem decisão sobre exigir ciência](/assets/screenshots/v3rlgpd-106-ciencia-sem-decisao.png)](/assets/screenshots/v3rlgpd-106-ciencia-sem-decisao.png)

> ⚠️ **Antes, só existia a primeira saída.** Quem decidia conscientemente que um documento **não** precisava de ciência não tinha como registrar isso — o documento continuava aparecendo no aviso para sempre, como se ninguém tivesse olhado. Agora essa decisão também é registrada, e some da lista como as demais.
>
> Nada é ligado automaticamente, nas duas direções: a organização decide, documento por documento, o que realmente merece a exigência.
