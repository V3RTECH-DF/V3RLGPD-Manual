---
title: "Equipe / Acessos"
nav_order: 13
parent: "Módulos"
permalink: /modulos/equipe-acessos/
role: admin
routes: ["#/access"]
screenshots: [v3rlgpd-60-equipe-acessos, v3rlgpd-61-equipe-toast, v3rlgpd-62-auditor-menu, v3rlgpd-63-auditor-ropa, v3rlgpd-64-auditor-settings, v3rlgpd-65-atendente-menu, v3rlgpd-66-atendente-dsar, v3rlgpd-67-atendente-incidentes, v3rlgpd-68-admin-menu-completo, v3rlgpd-71-acessos-distincao, v3rlgpd-72-papeis-cargos, v3rlgpd-73-editor-matriz, v3rlgpd-74-excluir-migracao]
last_verified: 2026-07-06
status: publicado
---

# Equipe / Acessos

A tela **Equipe / Acessos** permite que o administrador do WordPress defina, para cada usuário do painel, qual papel ele exerce no V3RLGPD — e, com isso, a quais módulos e ações esse usuário tem acesso.

> 🧭 **Onde encontrar**
>
> **Equipe / Acessos** é uma **aba dentro de Configurações**. Na barra de navegação do V3RLGPD, abra **Configurações** e, entre as abas internas da tela, escolha **Equipe / Acessos**. A aba só aparece para o administrador.

> 🆕 **Duas áreas (v1.44)**
>
> A partir da versão 1.44, a tela tem **duas abas internas**:
> - **Pessoas** — atribuir um papel a cada usuário (o que esta página já descrevia).
> - **Papéis & Cargos** — **ajustar o que cada papel vê e gerencia** e **criar cargos próprios** da sua organização. Veja ["Personalizar papéis e criar cargos"](#personalizar-papeis-e-criar-cargos-v144) abaixo.

> 💡 **Por que isso importa**
>
> A LGPD pede que cada pessoa tenha acesso apenas ao que precisa para o seu trabalho (princípio da necessidade, art. 6º). Na prática: quem atende os pedidos dos titulares não precisa mexer nas configurações; quem só audita não precisa excluir registros. Separar essas responsabilidades reduz erros e facilita a prestação de contas.

> ⚠️ **Quem pode usar esta tela**
>
> Apenas o **administrador do WordPress** vê a aba "Equipe / Acessos" (em Configurações). Os demais papéis não acessam esta tela.

---

## Como funciona

Antes, era tudo-ou-nada: só quem era administrador do WordPress entrava no V3RLGPD. Agora, o administrador pode **dar acesso ao plugin a outras pessoas da equipe sem torná-las administradoras do site** — basta escolher um papel para cada uma.

São **três papéis** atribuíveis (mais o administrador do WordPress, que tem acesso total):

| Papel | Para quem serve | Resumo do acesso |
|---|---|---|
| **Administrador do WordPress** | Quem instala e mantém o site | Acesso irrestrito, incluindo Equipe / Acessos, Configurações e a Migração/Desinstalação |
| **Encarregado** | A pessoa responsável pela proteção de dados na organização | Acesso completo à conformidade (Políticas, ROPA, RIPD, Atendimentos, Incidentes, Consentimentos, Configurações…); **não** faz migração/importação nem desinstalação |
| **Atendente** | Quem cuida do dia a dia com os titulares | Atendimentos (DSAR), Consentimentos, Denúncias e Incidentes — sem ações irreversíveis (exclusão de dados, notificação de incidente) |
| **Auditor** | Quem precisa conferir sem alterar nada | **Somente leitura** em todos os módulos |

> ✅ **Boas práticas**
>
> Em organizações pequenas, onde uma pessoa acumula funções, o papel **Encarregado** cobre tudo que o trabalho de privacidade exige, sem precisar dar a ela acesso de administrador do site. Reserve o administrador do WordPress para quem realmente faz manutenção técnica.

> ⚠️ **"Encarregado" aqui é o papel de acesso, não a designação formal**
>
> O papel **Encarregado** desta tela concede **permissões** no painel. Ele **não** é a designação formal do Encarregado da organização (art. 41) — essa, o contato publicado aos titulares, fica em [Configurações → Encarregado](/modulos/configuracoes/#encarregado). Costuma ser a mesma pessoa, mas são cadastros diferentes. A própria tela traz esse aviso:

[![Aviso da distinção em Equipe / Acessos](/assets/screenshots/v3rlgpd-71-acessos-distincao.png)](/assets/screenshots/v3rlgpd-71-acessos-distincao.png)
*Equipe / Acessos: nota que distingue o papel de acesso da designação formal do Encarregado.*

---

## Como atribuir um papel a um usuário

[![Tela Equipe / Acessos](/assets/screenshots/v3rlgpd-60-equipe-acessos.png)](/assets/screenshots/v3rlgpd-60-equipe-acessos.png)
*Tela Equipe / Acessos: lista dos usuários do WordPress com o papel atual de cada um.*

1. Na barra de navegação do V3RLGPD, abra **Configurações → Equipe / Acessos** (visível só para administradores).
2. A tela mostra os usuários do WordPress. Use o campo de **busca** para encontrar alguém pelo nome ou e-mail (útil em sites com muitos usuários) — ou marque **"Somente com acesso"** para ver só quem já tem papel.
3. No seletor ao lado do usuário, escolha o papel: **Sem acesso**, **Encarregado**, **Atendente** ou **Auditor**.
4. A alteração é salva na hora e uma confirmação aparece no canto da tela.

[![Confirmação de papel atualizado](/assets/screenshots/v3rlgpd-61-equipe-toast.png)](/assets/screenshots/v3rlgpd-61-equipe-toast.png)
*O aviso confirma que o papel foi atualizado.*

> O administrador do WordPress aparece na lista como **"Acesso total (administrador)"**, sem seletor — ele sempre tem acesso completo e não recebe papel.

---

## Personalizar papéis e criar cargos (v1.44)
{: #personalizar-papeis-e-criar-cargos-v144 }

Na aba **Papéis & Cargos**, o administrador pode ir além dos três papéis prontos: ajustar o que cada papel enxerga e gerencia, e criar **cargos próprios** com o nome e as permissões que a sua organização precisar.

[![Aba Papéis & Cargos](/assets/screenshots/v3rlgpd-72-papeis-cargos.png)](/assets/screenshots/v3rlgpd-72-papeis-cargos.png)
*A aba Papéis & Cargos lista os papéis, quantas pessoas estão em cada um e as ações disponíveis.*

Cada papel na lista mostra se é **Modelo** (os três que já vêm prontos) ou **Personalizado** (criado por você), e **quantas pessoas** o utilizam.

### Ajustar as permissões de um papel

Clique em **Editar** para abrir a **matriz de permissões**. Para cada módulo há duas colunas:

- **Ver** — a pessoa enxerga o módulo (somente leitura).
- **Gerenciar** — a pessoa pode criar, editar e excluir naquele módulo. Marcar **Gerenciar** liga **Ver** automaticamente (não dá para gerenciar sem ver).

[![Editor da matriz de permissões](/assets/screenshots/v3rlgpd-73-editor-matriz.png)](/assets/screenshots/v3rlgpd-73-editor-matriz.png)
*O editor: módulos com Ver/Gerenciar e, abaixo, as Ações sensíveis.*

Abaixo da matriz fica a seção **Ações sensíveis (irreversíveis)** — as operações mais perigosas (excluir dados de um titular, comunicar incidente, executar o expurgo por retenção, excluir uma política definitivamente). Elas ficam em destaque e **só podem ser marcadas se o cargo já tiver "Gerenciar" no módulo correspondente**. No exemplo acima, "Excluir dados do titular" só habilitou porque "Gerenciar" de Atendimentos está marcado.

> ⚠️ **Os três papéis-modelo são protegidos**
>
> Encarregado, Atendente e Auditor **não podem ser renomeados nem excluídos** — mas você **pode ajustar as permissões** deles. Se mexer e quiser voltar atrás, o botão **"Restaurar ao padrão"** devolve as permissões originais do papel. Na lista, um papel-modelo ajustado aparece como **"Modelo (ajustado)"**.

### Criar ou duplicar um cargo

- **+ Criar cargo** abre o editor em branco: dê um nome, uma descrição opcional e marque as permissões na matriz.
- **Duplicar** parte de um papel existente (as permissões dele já vêm marcadas) para você ajustar — atalho útil para criar variações.

Um cargo pode ficar sem nenhuma permissão: a pessoa entra no plugin, mas não vê nada. A tela avisa quando isso acontece.

### Excluir um cargo (com realocação das pessoas)

Só os cargos **personalizados** têm o botão **Excluir**. Se houver pessoas no cargo, a exclusão pergunta **para onde movê-las** — outro papel ou "Sem acesso ao plugin" — e faz a mudança na hora, para que ninguém fique sem definição.

[![Excluir cargo com realocação](/assets/screenshots/v3rlgpd-74-excluir-migracao.png)](/assets/screenshots/v3rlgpd-74-excluir-migracao.png)
*Ao excluir um cargo em uso, você escolhe para qual papel as pessoas serão movidas.*

> 💡 **Executar agora (fila de Retenção)**
>
> A ação sensível **"Executar expurgo por retenção"** habilita, na [fila de Retenção](/modulos/), um botão **"Executar agora"** por tarefa: ele **antecipa** o expurgo que o sistema faria na data agendada. Como apaga dados de forma irreversível, pede confirmação e só aparece para quem tem essa permissão.

> ✅ **A tela é conveniência; a segurança é no servidor**
>
> Esconder um botão ajuda no dia a dia, mas o V3RLGPD **confere toda ação no servidor**: mesmo que alguém tente acessar por um atalho, sem a permissão a ação é recusada.

---

## O que cada papel vê

> 🧭 **Navegação por barra e abas:** os módulos ficam agrupados numa barra de navegação com abas (ver [Módulos](/modulos/)). O que muda por papel é **quais itens e abas aparecem** — o princípio abaixo continua igual.
>
> ⚠️ **Capturas desatualizadas.** As imagens desta seção (menu do administrador, do Atendente e do Auditor) ainda mostram o **menu lateral do WordPress com os 8 itens do V3RLGPD listados um abaixo do outro** — layout anterior à v1.73.0, quando a navegação passou a viver dentro da tela do plugin, numa barra horizontal. O conteúdo e as permissões descritos abaixo continuam corretos; só o retrato do menu está velho. Recaptura pendente — ver `_manual/roteiro-recaptura.md`.

### Administrador do WordPress

[![Menu completo do administrador](/assets/screenshots/v3rlgpd-68-admin-menu-completo.png)](/assets/screenshots/v3rlgpd-68-admin-menu-completo.png)
*Menu do administrador com os 8 itens — captura anterior à v1.73.0, mostra o antigo menu lateral em vez da barra horizontal atual; **Equipe / Acessos** fica dentro de Configurações.*

Vê e usa todos os módulos do V3RLGPD.

### Atendente

[![Menu do Atendente](/assets/screenshots/v3rlgpd-65-atendente-menu.png)](/assets/screenshots/v3rlgpd-65-atendente-menu.png)
*O Atendente vê um menu reduzido, voltado ao atendimento.*

O Atendente é o papel do dia a dia de receber e responder os titulares. Vê o grupo **Atendimento ao Titular** com as abas **Consentimentos, Atendimentos, Denúncias e Incidentes** (não vê as abas Retenção nem Ações do Encarregado). Não vê Auditoria de Conformidade, ROPA, Políticas, RIPD nem Configurações.

Duas ações irreversíveis ficam reservadas ao Encarregado:

[![Atendimentos sem exclusão](/assets/screenshots/v3rlgpd-66-atendente-dsar.png)](/assets/screenshots/v3rlgpd-66-atendente-dsar.png)
*O Atendente responde os pedidos, mas o botão de exclusão/anonimização de dados não aparece.*

[![Incidentes sem notificação](/assets/screenshots/v3rlgpd-67-atendente-incidentes.png)](/assets/screenshots/v3rlgpd-67-atendente-incidentes.png)
*O Atendente registra incidentes, mas "Notificar Titulares" é exclusivo do Encarregado.*

### Auditor

[![Menu do Auditor](/assets/screenshots/v3rlgpd-62-auditor-menu.png)](/assets/screenshots/v3rlgpd-62-auditor-menu.png)
*O Auditor vê os módulos, mas em modo somente leitura.*

O Auditor tem **acesso de leitura a todos os módulos** (exceto a aba Equipe / Acessos). Vê os grupos **Auditoria de Conformidade** e **Atendimento ao Titular** e as seções avulsas, sempre em modo somente leitura. É o papel indicado para um financiador, conselheiro ou revisor externo que precisa conferir o trabalho da organização sem risco de alterar nada.

[![Inventário somente leitura](/assets/screenshots/v3rlgpd-63-auditor-ropa.png)](/assets/screenshots/v3rlgpd-63-auditor-ropa.png)
*O Inventário (ROPA) aparece completo, mas sem botões de criar, editar ou excluir.*

[![Configurações somente leitura](/assets/screenshots/v3rlgpd-64-auditor-settings.png)](/assets/screenshots/v3rlgpd-64-auditor-settings.png)
*Em Configurações, o Auditor vê um aviso de somente leitura e os botões de salvar ficam desabilitados.*

---

## O controle de acesso agora vale também para o endereço direto

Desde a v1.73.0, uma tela que a sua conta **não tem permissão para ver** fica realmente inacessível — mesmo que alguém digite o endereço dela diretamente no navegador, ou o tenha salvo num favorito antigo. Quem tenta abre uma mensagem dizendo que não tem acesso, em vez da tela.

> 💡 **Por que isso importa**
>
> Antes, o item sumia do menu para quem não tinha o papel correspondente, mas o **endereço direto** ainda abria a tela — a ausência no menu era só uma conveniência visual, não uma barreira de fato. Agora o controle de acesso vale nos dois casos: pelo menu **e** pelo endereço direto, exatamente como já acontecia na [página de Gestão no site](/modulos/gestao-frontend/#quem-enxerga-o-quê).

Se alguém da sua equipe disser que **"uma tela que eu sempre abria parou de abrir"**, o motivo mais provável é este: o papel dela nunca incluiu aquela tela — só não havia sido cobrado até agora. O caminho é revisar as permissões do papel dela em **Configurações → Equipe / Acessos → Papéis & Cargos** (veja ["Personalizar papéis e criar cargos"](#personalizar-papeis-e-criar-cargos-v144) acima).

## Tabela resumida de permissões

| O que pode fazer | Admin WP | Encarregado | Atendente | Auditor |
|---|:---:|:---:|:---:|:---:|
| Ver o Painel | Sim | Sim | Sim | Sim |
| Atender pedidos (DSAR) | Sim | Sim | Sim | Não |
| Excluir/anonimizar dados (DSAR) | Sim | Sim | Não | Não |
| Registrar incidentes | Sim | Sim | Sim | Não |
| Notificar titulares (incidente) | Sim | Sim | Não | Não |
| Gerenciar Consentimentos e Denúncias | Sim | Sim | Sim | Não |
| Gerenciar Políticas / ROPA / RIPD | Sim | Sim | Não | Não |
| Configurações | Sim | Sim | Não | Não |
| Visualizar tudo (somente leitura) | Sim | Sim | — | Sim |
| Migração / Importação / Desinstalação | Sim | Não | Não | Não |
| Gerenciar Equipe / Acessos | Sim | Não | Não | Não |

> 💡 **O V3RLGPD ajuda, mas a responsabilidade é da organização**
>
> Definir bem os papéis é uma boa prática de segurança e conformidade, mas não garante, por si só, a conformidade com a LGPD. Veja o [Aviso legal](/disclaimer/).
