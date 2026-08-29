---
title: "Configurações"
nav_order: 11
parent: "Módulos"
permalink: /modulos/configuracoes/
role: encarregado
routes: ["#/settings"]
screenshots: [v3rlgpd-04b-dsar-declaracao-escopo, v3rlgpd-69-config-encarregado, v3rlgpd-70-encarregado-autofill, v3rlgpd-08b-settings-cookies, v3rlgpd-08c-settings-webhooks, v3rlgpd-08d-settings-paginas, v3rlgpd-08f-settings-aparencia, v3rlgpd-08g-settings-aparencia-custom, v3rlgpd-08e-settings-saida, v3rlgpd-08i-settings-import, v3rlgpd-08h-settings-desinstalacao, v3rlgpd-92-config-licenca]
last_verified: 2026-06-28
status: publicado
---

# Configurações

A tela **Configurações** reúne, em um só lugar, os ajustes gerais do V3RLGPD — da identidade da organização à exibição das políticas e à exportação dos dados. Ela é organizada em **oito abas**.

> 💡 **Por que isso importa**
>
> A maioria dos itens de configuração afeta diretamente o que o público vê (Central, cookies, políticas) e como a sua conformidade é medida. Vale conhecer cada aba antes de publicar a Central.

## As oito abas

| Aba | Para que serve | Aprofunde em |
|---|---|---|
| **Organização** | Identidade do controlador (razão social, CNPJ, endereço, contato), logo e a **declaração de escopo de tratamento**. | (abaixo) |
| **Encarregado** | Dados do Encarregado e modo de exclusão de políticas. | [Configurar o Encarregado](/guias/configurar-dpo/) |
| **Banner de Cookies** | Ativar/desativar o banner e gerenciar os scripts por categoria. | [Consentimento & Cookies](/modulos/consentimento/) |
| **Webhooks** | Enviar eventos (nova solicitação, alteração de política, incidente, consentimento) para automações externas. | (abaixo) |
| **Retenção & Expurgo** | Regras globais de descarte/anonimização e a fila de retenção. | [Retenção & Expurgo](/modulos/retencao/) |
| **Páginas & Integração** | Escolher a página da Central, definir a exibição padrão das políticas e copiar os shortcodes. | [Central de Privacidade](/modulos/central-privacidade/) |
| **Aparência** | Tema de cores do frontend (Central, selo, shortcodes): temas prontos ou personalização (cores, cantos, fonte). | (abaixo) |
| **Saída de Dados** | Backup completo (ZIP), **exportação para migração** (JSON por escopos) e a **preferência de desinstalação**. | (abaixo) |

## Organização

[![Configurações — Organização](/assets/screenshots/v3rlgpd-04b-dsar-declaracao-escopo.png)](/assets/screenshots/v3rlgpd-04b-dsar-declaracao-escopo.png)
*Identidade do controlador, logo e a declaração de escopo de tratamento.*

Aqui ficam os dados do **controlador** — **razão social** (obrigatória para gerar políticas), **CNPJ**, **endereço** e **contato público** —, a **logo** da organização (usada nos relatórios PDF, nos e-mails e na Central) e a **declaração de escopo de tratamento**. Esses dados são reaproveitados pelo Assistente de Políticas, pelos relatórios e pelo selo.

> ℹ️ **CNPJ alfanumérico:** o campo aceita tanto o CNPJ tradicional (só números) quanto o novo **CNPJ alfanumérico** da Receita Federal (com letras nas primeiras posições, válido para inscrições a partir de julho/2026). O sistema **confere os dígitos verificadores** e avisa se estiver errado — se aparecer "CNPJ inválido", revise o que foi digitado. CNPJs já cadastrados continuam funcionando normalmente.

### A organização trata dados fora deste site?

A pergunta **"A organização trata dados pessoais fora deste site?"** (Não / Sim / Não informado) orienta o atendimento às solicitações de titulares:

- **Não — apenas neste site:** habilita a **resposta automática assistida** do Encarregado nos pedidos informativos (acesso, portabilidade, informação sobre compartilhamento).
- **Sim** ou **Não informado:** sem resposta automática — o plugin pede que o Encarregado revise (pode haver dados no papel, em planilhas ou em outros sistemas) antes de responder manualmente.

➡️ Como isso afeta o atendimento em **[Atendimentos (DSAR)](/modulos/atendimentos/#a-declaracao-de-escopo-da-organizacao)**.

## Encarregado

[![Configurações — Encarregado, com aviso de distinção](/assets/screenshots/v3rlgpd-69-config-encarregado.png)](/assets/screenshots/v3rlgpd-69-config-encarregado.png)
*Aba Encarregado: a designação formal (art. 41), com o aviso que a diferencia do papel de acesso de mesmo nome.*

Aqui você cadastra o **Encarregado** — nome/setor, e-mail e telefone, que aparecem publicamente na Central. Também define o **Modo de Exclusão de Políticas** (soft delete, que mantém logs, ou hard delete, que apaga em definitivo). A **logo** da organização fica na aba **Organização**.

> ⚠️ **Designação formal ≠ papel de acesso**
>
> Esta tela define a designação **formal** do Encarregado (art. 41) — o contato **publicado** aos titulares e à <a href="https://www.gov.br/anpd/pt-br" target="_blank" rel="noopener noreferrer">ANPD</a> —, que pode até ser alguém **sem usuário no WordPress** (um jurídico externo, um comitê, um e-mail). Não confunda com o **papel de acesso** "Encarregado" em [Equipe / Acessos](/modulos/equipe-acessos/), que apenas concede permissões no painel.

**Atalho:** o botão **"Preencher a partir de um usuário do WordPress"** busca um usuário e preenche nome e e-mail automaticamente (você ainda pode editar; o telefone segue manual).

[![Preencher o Encarregado a partir de um usuário do WordPress](/assets/screenshots/v3rlgpd-70-encarregado-autofill.png)](/assets/screenshots/v3rlgpd-70-encarregado-autofill.png)
*Busca de usuário do WordPress para preencher os campos do Encarregado.*

➡️ Passo a passo em **[Configurar o Encarregado](/guias/configurar-dpo/)**.

> ✅ **Inativar ≠ excluir.** Para tirar uma política do ar **sem apagá-la**, use **Inativar** na lista de Políticas (reversível). O *Modo de Exclusão* acima rege o botão **Excluir** da lista: *soft* arquiva (preserva o registro) e *hard* apaga em definitivo (perde a rastreabilidade). Veja [Políticas › Excluir](/modulos/politicas/#excluir-uma-politica).

## Banner de Cookies

[![Configurações — Banner de Cookies](/assets/screenshots/v3rlgpd-08b-settings-cookies.png)](/assets/screenshots/v3rlgpd-08b-settings-cookies.png)

Você decide **se** exibe o banner e cadastra os scripts por categoria (necessários, análise, marketing). Com o banner **desativado**, os scripts não essenciais **não são carregados** (sem consentimento, nada carrega). Detalhes em [Consentimento & Cookies](/modulos/consentimento/).

## Webhooks

[![Configurações — Webhooks](/assets/screenshots/v3rlgpd-08c-settings-webhooks.png)](/assets/screenshots/v3rlgpd-08c-settings-webhooks.png)

Os **webhooks** notificam sistemas externos (n8n, Zapier, Make etc.) quando acontecem eventos importantes — nova solicitação de titular, alteração/ativação de política, incidente, consentimento. Informe a URL de destino para integrar o V3RLGPD ao seu fluxo de automação.

## Retenção & Expurgo

A aba concentra as regras **globais** de retenção (prazos para anonimizar/excluir dados de solicitações e consentimentos) e dá acesso à **fila** de ações programadas. O detalhamento — conectores, motor e fila — está em [Retenção & Expurgo](/modulos/retencao/).

## Páginas & Integração

[![Configurações — Páginas & Integração](/assets/screenshots/v3rlgpd-08d-settings-paginas.png)](/assets/screenshots/v3rlgpd-08d-settings-paginas.png)
*Seletor da página da Central, exibição padrão das políticas e a lista de shortcodes.*

Esta aba tem três blocos:

- **Selecione a página da Central** — aponte qualquer página publicada como a sua Central de Privacidade (ou gere a página padrão com um clique). A página escolhida passa a valer para o [Índice de Conformidade](/modulos/painel/) e para o link do banner de cookies.
- **Exibição Padrão das Políticas** — define como as políticas aparecem por padrão (modo integral/resumo/só título; mostrar título, link e imagem). Cada shortcode pode sobrescrever esse padrão com atributos.
- **Shortcodes Disponíveis** — a lista pronta para copiar e colar em qualquer página.

➡️ Tudo sobre montar a página em **[Central de Privacidade](/modulos/central-privacidade/)**.

> ⚠️ **Página montada à mão é responsabilidade sua.** A Central completa autogerada já inclui Encarregado, políticas e canal de pedidos. Ao montar a sua, não deixe esses elementos de fora.

## Aparência

[![Configurações — Aparência (temas)](/assets/screenshots/v3rlgpd-08f-settings-aparencia.png)](/assets/screenshots/v3rlgpd-08f-settings-aparencia.png)
*Escolha um tema pronto e confira no preview ao vivo. Não afeta o painel administrativo.*

A aba **Aparência** ajusta o visual das partes **públicas** do plugin — a Central de Privacidade, o selo e os shortcodes — para combinar com a identidade do seu site. **Não muda o painel administrativo.**

**Temas prontos.** Escolha um dos cinco temas e clique em **Salvar Aparência**: **V3RLGPD (Padrão)**, **Neutro Escuro**, **Terra (Marrom)**, **Oceano (Azul Claro)** ou **Alto Contraste**. O **preview ao vivo** mostra como ficam um card, um botão e o selo antes de salvar. Para voltar ao tema original a qualquer momento, clique em **Restaurar padrão**.

### Personalizar (avançado)

[![Configurações — Aparência personalizada e aviso de contraste](/assets/screenshots/v3rlgpd-08g-settings-aparencia-custom.png)](/assets/screenshots/v3rlgpd-08g-settings-aparencia-custom.png)
*Ajuste cor a cor; o sistema avisa quando uma combinação fica difícil de ler.*

Clique em **Personalizar** para definir individualmente as **cores** (principal, texto, títulos, fundos, bordas…), os **cantos** (reto / suave / arredondado) e a **fonte** (herdar do tema do site, sistema ou serifada). Ao alterar qualquer item, o tema passa a "Customizado".

> ⚠️ **Aviso de contraste.** Se uma combinação ficar difícil de ler (ex.: texto claro sobre fundo claro), aparece um **alerta de contraste** (padrão de acessibilidade WCAG AA). É só um lembrete — você ainda pode salvar —, mas cores legíveis ajudam todos os visitantes, inclusive pessoas com baixa visão.

## Saída de Dados

[![Configurações — Saída de Dados](/assets/screenshots/v3rlgpd-08e-settings-saida.png)](/assets/screenshots/v3rlgpd-08e-settings-saida.png)
*Backup completo, exportação para migração e a preferência de desinstalação.*

Esta aba reúne três recursos ligados ao **ciclo de vida dos seus dados**.

### Exportação completa (backup)

Gera um **ZIP** com todos os dados da organização — políticas, ROPA, consentimentos, incidentes, solicitações e auditoria — em CSV e JSON, para guarda ou auditoria. O arquivo contém **dados pessoais reais**: armazene em local seguro. Veja [Relatórios & Backup](/modulos/relatorios/).

### Exportação para migração

Gera um **arquivo JSON** para **levar seus dados para outra instalação** do V3RLGPD. Marque os **escopos** que deseja incluir (Configurações, Políticas, ROPA, Consentimentos, Solicitações, Incidentes, Denúncias, RIPD, Retenção, Auditoria) e clique em **Baixar JSON de Migração**.

- **Exportar não altera nem apaga** seus dados — é apenas uma cópia.
- Marque só o necessário: se você **não** incluir um escopo (ex.: Consentimentos), os dados pessoais dele **não entram** no arquivo.

> ⚠️ **O arquivo contém dados pessoais em texto.** Guarde em local seguro e apague depois de concluir a migração.

### Importação de migração

[![Configurações — Importação de migração](/assets/screenshots/v3rlgpd-08i-settings-import.png)](/assets/screenshots/v3rlgpd-08i-settings-import.png)
*Ao carregar o arquivo, a tela mostra a origem, a data, a versão e, por escopo, quantos registros vêm no arquivo e quantos já existem no destino (que serão substituídos).*

Recebe um **arquivo JSON** gerado pela "Exportação para migração" de **outra instalação** do V3RLGPD e traz aqueles dados para esta. O processo é em dois passos:

1. **Selecione o arquivo** — o sistema mostra um resumo (origem, data, versão) e os **escopos** disponíveis no arquivo, indicando **quais já têm dados aqui** (e que serão substituídos).
2. **Escolha os escopos** que quer importar e confirme. Para os escopos que vão sobrescrever dados existentes, aparece uma **confirmação** antes de aplicar.

- A importação **substitui** (não mescla) os dados de cada escopo escolhido.
- Se o arquivo vier de uma versão do plugin **mais nova** que a desta instalação, a importação é **recusada** — atualize o plugin aqui primeiro.

> 💡 **Dica:** faça um [backup completo](#saida-de-dados) deste site antes de importar, caso queira voltar atrás.

### Desinstalação do plugin

[![Configurações — Confirmação de desinstalação destrutiva](/assets/screenshots/v3rlgpd-08h-settings-desinstalacao.png)](/assets/screenshots/v3rlgpd-08h-settings-desinstalacao.png)
*Escolher "Apagar tudo" exige uma confirmação explícita.*

Define o que acontece com os dados **se você remover o plugin** pelo painel do WordPress:

- **Manter os dados (recomendado)** — se reinstalar no futuro, suas políticas e configurações continuam intactas. É o padrão.
- **Apagar tudo definitivamente** — remove todas as tabelas e registros do banco ao desinstalar. É **irreversível**, por isso o sistema pede uma confirmação antes de salvar.

> 💡 **Exporte antes de apagar.** Se for desativar de vez, gere uma exportação (acima) antes de marcar "Apagar tudo".

## Licença

[![Configurações — Licença, com uma licença ativa](/assets/screenshots/v3rlgpd-92-config-licenca.png)](/assets/screenshots/v3rlgpd-92-config-licenca.png)
*Licença ativa: a chave aparece sempre mascarada depois da ativação.*

> 💡 **Por que isso importa**
>
> O V3RLGPD **funciona sem licença** — não há recurso pago que trave. A licença serve só
> para **liberar as atualizações automáticas**, inclusive as de correção de bugs e
> segurança. Enquanto ela não estiver ativada, o site **não recebe nada de novo**, nem os
> ajustes que corrigem um problema sério. Ative logo depois de instalar.

### Como ativar

1. Abra **Configurações → Licença**.
2. Cole a **chave de licença** (formato `V3RL-XXXX-XXXX-XXXX-XXXX`) no campo **Chave de
   licença**.
3. Clique em **Ativar**.

> ⚠️ **A chave completa só trafega nesta tela, no momento da ativação.** Depois disso, o
> sistema sempre mostra a versão mascarada (ex.: `V3RL-XXXX-...-B428`) — guarde a chave
> original (e-mail de compra, gerenciador de senhas) para o caso de precisar reativar em
> outro site.

### Os campos

| Campo | O que significa |
|---|---|
| **Status** | *Nenhuma licença ativada*, *Ativa* ou o motivo de recusa. |
| **Chave** | A chave mascarada, depois de ativada. |
| **Expira em** | Data-limite da assinatura; depois dela, as atualizações voltam a parar. |
| **Ativações** | Quantos domínios já usam essa chave, sobre o limite contratado. |
| **Última verificação** | Quando o plugin conferiu, junto ao servidor da V3RTECH, se a licença continua válida. Use **Verificar agora** para atualizar na hora. |

### Ativações por domínio

Uma mesma licença vale para **vários sites**, até o limite contratado — cada domínio ocupa
uma vaga. Para trocar de servidor, use **Desativar licença** no site antigo antes de
ativar no novo: **desativar libera a vaga** imediatamente. Ambiente de teste reconhecido
como tal pelo servidor de licenças **não consome cota**.

### Quando dá errado

| Situação | O que fazer |
|---|---|
| Chave recusada | Confira se copiou a chave inteira, sem espaços, e se não trocou `O` por `0` ao digitar à mão. |
| Limite de ativações atingido | Desative a licença em um site que não usa mais essa chave, ou contrate mais ativações. |
| Licença expirada | Renove a assinatura e clique em **Verificar agora** para atualizar sem esperar a checagem automática. |
| Servidor de licenças indisponível | O plugin segue funcionando com a última verificação válida; tente de novo em alguns minutos, e fale com o suporte se persistir por mais de um dia. |

> ⚠️ **Licença vencida não desliga o plugin.** O que para é só a atualização automática —
> o V3RLGPD continua rodando normalmente com a versão instalada.
