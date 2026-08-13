---
title: "Dúvidas Frequentes"
nav_order: 9
permalink: /faq/
---

# Dúvidas Frequentes

## Minha organização é pequena. A LGPD vale mesmo para ela?

Sim. A LGPD não tem isenção por porte nem por natureza da organização (pública, privada ou sem fins lucrativos). A boa notícia: para uma organização pequena, com poucos tipos de dados, a adequação é proporcionalmente simples. Comece pelos [Primeiros Passos](/primeiros-passos/).

## Preciso contratar um advogado para usar o V3RLGPD?

Não para **usar** a ferramenta. Mas as **decisões jurídicas** (qual base legal, conteúdo final das políticas, casos sensíveis) devem ser validadas, idealmente, por apoio jurídico. O plugin organiza; a responsabilidade é da organização. Veja o [Aviso legal](/disclaimer/).

## O Encarregado precisa ser advogado?

Não. O Encarregado pode ser um voluntário, funcionário ou setor. Precisa estar acessível aos titulares e à <a href="https://www.gov.br/anpd/pt-br" target="_blank" rel="noopener noreferrer">ANPD</a> e ter respaldo interno. Veja [Papéis](/papeis/).

## Posso dar acesso ao plugin para mais de uma pessoa da minha equipe?

Sim. Na tela **Equipe / Acessos** (visível só para o administrador do WordPress), você define um papel para cada usuário — **Encarregado**, **Atendente** ou **Auditor** — sem precisar torná-lo administrador do site. Veja [Equipe / Acessos](/modulos/equipe-acessos/).

## Qual a diferença entre o Atendente e o Encarregado?

O **Encarregado** opera toda a conformidade (políticas, ROPA, incidentes, configurações…) e assina as ações irreversíveis (excluir dados de um pedido, comunicar um incidente aos titulares). O **Atendente** faz a triagem do dia a dia — recebe e responde pedidos, registra incidentes, cuida de consentimentos e denúncias —, mas as ações irreversíveis ficam bloqueadas para ele, que envolve o Encarregado nessas situações. Veja [Equipe / Acessos](/modulos/equipe-acessos/).

## Posso dar acesso de leitura a um conselheiro ou financiador sem que ele altere nada?

Sim. O papel **Auditor** dá acesso **somente leitura** a todos os módulos: a pessoa consulta painel, inventário, relatórios e mapa de conformidade, mas não cria, edita nem exclui nada. É o caminho indicado para prestação de contas ou revisão externa. Veja [Equipe / Acessos](/modulos/equipe-acessos/).

## Quem já usa o plugin precisa fazer algo depois dessa atualização?

Não. Nada muda nas instalações existentes: o administrador do WordPress continua com acesso total e o controle por papéis só passa a valer quando você decidir atribuir papéis a outras pessoas em **Equipe / Acessos**.

## Qual o prazo para responder um pedido de titular?

A referência usada no plugin é de **15 dias**. O módulo de [Atendimentos](/modulos/atendimentos/) calcula e acompanha esse prazo (SLA) para cada pedido, sinalizando os que estão no prazo e os atrasados.

## O que é o "duplo opt-in" nos pedidos?

É uma confirmação por e-mail: quando alguém abre um pedido, o plugin envia um link de confirmação para o e-mail informado. O pedido só entra na fila **depois** que a pessoa clica no link. Isso evita pedidos falsos e confirma que o e-mail pertence a quem pediu. Veja [Como o titular exerce seus direitos](/guias/titular-exercer-direitos/).

## O titular consegue resolver sozinho, sem o Encarregado?

Para pedidos **simples e seguros** (acesso/confirmação, portabilidade, informação sobre compartilhamento), sim — é o **auto-atendimento (self-service)**: após confirmar o e-mail, a pessoa já recebe o resultado. Pedidos de **exclusão/anonimização** continuam passando pelo Encarregado, por serem irreversíveis. Veja [Atendimentos](/modulos/atendimentos/).

## Posso ter mais de uma política?

Sim. O V3RLGPD trata políticas de forma genérica: crie quantas precisar (Privacidade, Termos de Uso, Cookies, e outras). Só a Política de Privacidade tem um checklist específico. Veja [Políticas](/modulos/politicas/).

## Posso usar uma política que já tenho em PDF, sem reescrever?

Sim. Ao criar a política, escolha a origem **Externa** e informe o **link** (PDF, página de wiki, intranet) — ou, se a política já for uma **página publicada no seu site**, use o seletor **"Ou escolha uma página publicada do site"**, que preenche a URL sozinho —, além de um resumo e uma imagem/ícone. Ela aparece na Central como um card com o botão "Ler a política completa". Veja [Políticas › interna ou externa](/modulos/politicas/#politica-interna-ou-externa-link).

## Posso desativar uma política sem apagá-la?

Sim. Use **Inativar** na lista de Políticas: a política some da Central e dos shortcodes, mas o conteúdo, o histórico de versões e os consentimentos são preservados — e você pode **reativar** quando quiser. É o caminho indicado quando uma política foi incorporada a outra ou deixou de valer. Veja [Políticas › Inativar e reativar](/modulos/politicas/#inativar-e-reativar-uma-politica).

## O Índice de Conformidade prova que estou conforme?

Não. Ele é um **indicador interno de progresso**, não um certificado. Conformidade depende de fatores que nenhuma ferramenta mede sozinha. Veja o [Aviso legal](/disclaimer/).

## Como o banner de cookies funciona?

O visitante vê o banner na primeira visita e escolhe aceitar, recusar não-essenciais ou personalizar. Os scripts de análise/marketing **que você colou em Configurações → Banner de Cookies** ficam parados até haver consentimento — e cada decisão, inclusive a recusa, vira registro consultável (a sua prova). Veja [Consentimento & Cookies](/modulos/consentimento/).

## Liguei o banner, mas o Google Analytics continua carregando mesmo quando o visitante recusa. Por quê?

Porque ele não está sendo carregado **pelo V3RLGPD**. O banner só controla os scripts que **você colou em Configurações → Banner de Cookies**. Se o Analytics (ou qualquer outro rastreador) estiver instalado por **outro plugin** ou escrito **direto no tema**, o V3RLGPD não sabe que ele existe e não tem como segurá-lo.

Nesse caso o banner não está protegendo nada — está só decorando, enquanto o rastreamento acontece do mesmo jeito.

**Como resolver:** rode o **[Detector de Conformidade](/modulos/detector/)** — ele encontra esses rastreadores para você e diz o que fazer com cada um (nem todos devem ser trazidos para cá; veja as duas perguntas abaixo). Veja também [Consentimento & Cookies › Como o plugin segura os scripts](/modulos/consentimento/#como-o-plugin-segura-os-scripts).

## Como eu descubro o que está rastreando no meu site?

Rodando o **[Detector de Conformidade](/modulos/detector/)** (em Auditoria de Conformidade). Ele varre o seu site **publicado** e mostra quais rastreadores estão disparando **antes** do visitante consentir — inclusive os que você não sabia que estavam lá, porque entraram por outro plugin ou pelo tema.

É a diferença entre o Detector e o resto do painel: o resto olha o que você **configurou**; o Detector olha o que está **de fato no ar**.

## O Detector não achou nenhum rastreador. Meu site está limpo?

**Não necessariamente** — e essa distinção é importante. O Detector reconhece os rastreadores mais comuns (Google Tag Manager, Google Analytics, Meta Pixel, Google Ads, LinkedIn, TikTok, Hotjar, Clarity). O que ele afirma é: *"nenhum dos que eu conheço apareceu"*.

Se a sua organização usa uma ferramenta fora dessa lista — Matomo, Plausible, um pixel menos comum, um script próprio — **ela não é detectada**. Nesse caso a conferência continua sendo sua.

Por isso o resultado positivo do Detector diz "nenhum rastreador **conhecido**" e lista quais são: para você saber exatamente o que foi verificado, em vez de sair com uma falsa sensação de segurança.

## Por que o Detector não me deixa importar um dos scripts?

De propósito — ele está te protegendo.

Quando o rastreador vem de um plugin com **funcionalidade própria** (MonsterInsights, Site Kit, GTM4WP, PixelYourSite e afins), o código do rastreador é a **menor parte** do que esse plugin faz. Ele também rastreia downloads e formulários, manda os eventos de compra com os dados do pedido, monta informações para o Tag Manager e serve relatórios dentro do painel.

Se você trouxesse só o trecho para cá e desativasse o plugin, **manteria a marcação básica e perderia todo o resto — sem nenhum aviso**. Costuma-se descobrir meses depois, quando falta dado.

Nesses casos o Detector nomeia o plugin, diz **o que exatamente você perderia** e orienta o caminho certo: usar a **configuração de consentimento do próprio plugin** (a maioria dos modernos tem uma). Se você não usa esses recursos extras, aí sim remova o plugin e rode o Detector de novo. Veja [Detector › O caso dos rastreadores](/modulos/detector/#o-caso-dos-rastreadores-cookies-sem-consentimento).

## O V3RLGPD pode desativar o plugin que está rastreando, para mim?

**Não, e isso é uma decisão nossa, não uma limitação técnica.**

Não temos como saber o que quebraríamos no seu site: o que aquele plugin faz não está no trecho de código que enxergamos. Prometer "a funcionalidade fica preservada" seria uma promessa que não podemos cumprir — e, se desse errado, você perderia dados e a culpa seria do plugin que deveria estar te protegendo.

O V3RLGPD **ajuda** a cumprir a LGPD; ele não assume responsabilidade pelo funcionamento do seu site. Nosso papel é dizer **o quê**, **por quê** e **o que você perde** — com precisão suficiente para a decisão ser sua, tomada com informação.

## O titular pode mudar de ideia depois de aceitar os cookies?

Sim, e é um direito dele (art. 8º, §5º da LGPD). Na Central de Privacidade, o botão **"Alterar Preferências de Cookies"** reabre o painel já mostrando o que ele escolheu antes. Ao **retirar** uma categoria, a página recarrega e o script para de carregar **na hora** — não fica valendo só na próxima visita. Veja [Consentimento & Cookies › Mudar de ideia depois](/modulos/consentimento/#mudar-de-ideia-depois).

## Por quanto tempo meus dados (ou os dos titulares) ficam guardados?

Pelo prazo que a **sua organização** definir para cada tipo de tratamento, conforme a base legal e a finalidade. O módulo de [Retenção & Expurgo](/modulos/retencao/) automatiza o fim desse ciclo: ao vencer o prazo, o plugin **anonimiza** o registro — depois de avisar o Encarregado com antecedência. Nada entra nesse expurgo automático sem a organização ligar a opção explicitamente.

## A retenção apaga meus dados de vez? E se eu precisar deles para o fisco?

A ação padrão é **anonimizar** (remover o que identifica a pessoa), não apagar — assim a organização mantém a **prova** de que cumpriu a regra. E dados com obrigação legal de guarda (como notas fiscais) só são expurgados se a organização **optar** por isso: por padrão, nenhuma atividade entra na retenção automática. Há ainda uma **janela de aviso** (7 dias) e a opção de cancelar ou adiar antes de qualquer ação irreversível. Veja [Retenção & Expurgo](/modulos/retencao/).

## O plugin notifica a ANPD por mim em caso de incidente?

Não. O plugin ajuda a **registrar** o incidente e a **comunicar os titulares afetados** de forma rastreável. A **notificação oficial à ANPD** é feita pela sua organização, pelos canais oficiais do governo. Veja [Incidentes](/modulos/incidentes/).

## O que é o ECA Digital e ele se aplica à minha organização?

O **ECA Digital** (Lei 15.211/2025) protege crianças e adolescentes na internet. Ele alcança sites **direcionados a** ou de **acesso provável** por menores — comum em organizações que trabalham com esse público. A forma mais rápida de saber é fazer a [triagem de enquadramento](/eca-digital/enquadramento/) no Mapa de Conformidade. É uma lei **diferente** da LGPD, e o conteúdo do manual **não substitui orientação jurídica**. Veja [ECA Digital](/eca-digital/).

## Vou ter que verificar a idade de quem acessa o site?

Provavelmente **não**. Sites institucionais com **controle editorial** (conteúdo escolhido pela organização, sem automação) costumam ser **dispensados** da verificação de idade. O que normalmente se aplica à organização são os **deveres de proteção de dados de menores** (consentimento dos pais, privacidade por padrão, transparência). O enquadramento mostra o seu caso.

## O ECA Digital muda o meu Índice de Conformidade da LGPD?

Não. Os deveres do ECA Digital aparecem em uma **seção própria** no Mapa e **não** entram no cálculo do percentual da LGPD.

## Onde reporto um problema ou sugiro uma melhoria?

Fale com a equipe da V3RTECH/RIT responsável pela sua implantação. As novidades do produto aparecem em [Novidades](/novidades/) e os planos futuros em [Roadmap](/roadmap/).

## Minha organização atende crianças e adolescentes. E agora?

Faça primeiro a [triagem de enquadramento](/eca-digital/enquadramento/) no Mapa de Conformidade — ela mostra **só os deveres do seu caso**. A partir daí, o caminho costuma ser: consentimento dos pais nos formulários, privacidade por padrão, não fazer publicidade dirigida a menores, transparência aos pais e, quando couber, um RIPD. O guia [Configurar a proteção de crianças e adolescentes](/guias/proteger-menores-eca/) leva você por tudo isso, na ordem.

## O que é o RIPD e quando eu preciso de um?

O **RIPD** (Relatório de Impacto à Proteção de Dados, art. 38 da LGPD) descreve os **riscos** de um tratamento de dados e as **medidas** para reduzi-los. Não é obrigatório de rotina para a maioria das organizações, mas vale a pena quando há dados sensíveis em escala, **grupos vulneráveis** (como crianças e adolescentes), monitoramento sistemático ou legítimo interesse com impacto relevante. Veja [quando fazer](/modelos/ripd/) e o passo a passo em [Módulo RIPD](/modulos/ripd/).

## Os Assistentes (Inventário e RIPD) exigem que eu saiba a parte técnica?

Não. Os assistentes existem justamente para você **sair do formulário em branco**. O [Assistente de Inventário](/guias/montar-inventario-assistente/) faz perguntas do dia a dia ("envia newsletter?", "recebe doações?") e monta atividades prontas — já com base legal **sugerida** e prazo de retenção — para você revisar. As sugestões não são decisões: confira sempre a base legal e os dados sensíveis. Nada é gravado até você confirmar.

## O V3RLGPD toma decisões automáticas ou faz perfilamento dos titulares?

Não. O plugin organiza dados e processos; ele não pontua, classifica nem decide nada automaticamente sobre as pessoas. No contexto do [ECA Digital](/eca-digital/perfilamento-publicidade/), inclusive, ele **avisa** para você não usar perfilamento e publicidade dirigida a menores (mantendo apenas cookies essenciais), mas a decisão e a responsabilidade são da organização.

## Quando preciso notificar a ANPD em caso de incidente?

A comunicação à ANPD e aos titulares cabe quando o incidente puder acarretar **risco ou dano relevante** aos titulares — a avaliação é da sua organização, idealmente com apoio jurídico. O V3RLGPD ajuda a **registrar** o incidente e a **comunicar os titulares afetados** de forma rastreável, mas a **notificação oficial à ANPD** é feita pela sua organização pelos canais do governo. Veja [Incidentes](/modulos/incidentes/).

## Qual a diferença entre o "Verificado" e o "Atestado" no Mapa de Conformidade?

**Verificado** é o que a ferramenta **confere automaticamente** (ex.: Política de Privacidade ativa, Encarregado configurado, Central publicada) — é o que forma o percentual do anel. **Atestado** é a parte **autodeclarada** pela sua organização: você afirma que cumpriu algo que o sistema não tem como checar sozinho. Os atestados aparecem separados, em roxo ("Atestado: X de 4"), e **não inflam** o percentual verificado. Veja [Painel e Mapa de Conformidade](/modulos/painel/).

## Como envio uma sugestão ou relato um problema do plugin?

Use o botão **💬 Enviar feedback** no topo do painel. Dá para mandar **sugestões**, **relatos de problema (bug)** e **depoimentos** aos desenvolvedores (V3RTECH/RIT) por e-mail, com **cópia para você**. As desenvolvedoras **não acessam** o seu site, então o retorno chega por e-mail e pode levar alguns dias. Esse canal é sobre o **plugin** — **dúvidas jurídicas** ficam fora do escopo. Passo a passo em [Enviar feedback](/guias/enviar-feedback/).

## Como sei se os formulários do meu site estão em conformidade?

Use o **Verificador de Formulários** (aba do grupo **Inventário (ROPA)**). Ele analisa os campos de cada formulário (Contact Form 7, Forminator, WPForms, Gravity, Fluent e Elementor Pro) e aponta possíveis problemas: campos que parecem **dados pessoais** (e **sensíveis**), falta de **consentimento**, formulário **fora do Inventário (ROPA)** e indícios de **dados de menores** sem responsável. A análise é **consultiva** (baseada em pistas do nome/tipo do campo) e **não corrige** nem substitui orientação jurídica — ela aponta para você tratar. Detalhes em [Verificador de Formulários](/modulos/formularios/).

## Uso Google Forms. O V3RLGPD cobre eles também?

Sim. No Verificador, use **+ Adicionar Google Form** (cole a URL pública — o V3RLGPD lê os campos sozinho, sem login na sua conta Google) ou **🔍 Procurar no site** (ele varre as páginas e acha os que você incorporou/linkou). A partir daí o Google Form é **verificado** e pode **entrar no Inventário (ROPA)** como qualquer outro. Duas ressalvas importantes: (1) a **retenção/expurgo automático não cobre** Google Forms — os dados ficam no Google e a exclusão é feita lá; (2) o V3RLGPD lê só a **estrutura** do formulário, **nunca as respostas**. Se ele não conseguir ler um formulário (privado, por exemplo), você informa os campos à mão. Detalhes em [Formulários do Google](/modulos/formularios/#formulários-do-google-google-forms).

## Um formulário meu está "fora do Inventário (ROPA)". Preciso digitar tudo de novo?

Não. No relatório do **Verificador de Formulários**, o apontamento "Fora do Inventário" traz o botão **✨ Gerar rascunho de ROPA a partir dos campos**: ele abre o editor do Inventário **já preenchido** com as categorias de dados, a origem e — quando há pistas — a finalidade e a base legal (marcadas como **"sugestão — confirme"**). Você revisa, completa o que faltar e salva; o formulário já fica **vinculado** à atividade. Se a atividade **já existir**, prefira **vincular** o formulário a ela pelo seletor da tabela, em vez de criar outra. As sugestões são um ponto de partida — confira sempre a base legal. Passo a passo em [Criar a atividade do ROPA a partir do formulário](/modulos/formularios/#criar-a-atividade-do-ropa-a-partir-do-formulário).

## Preciso verificar os formulários de novo toda vez que entro na tela?

Não. O **Verificador de Formulários** **salva** o resultado de cada verificação: ao trocar de tela e voltar, o status de cada formulário continua lá, com a data ("verificado em DD/MM/AAAA HH:MM"). Use **"Ver relatório"** para reabrir o último resultado salvo e **"Reverificar"** quando quiser refazer a análise (por exemplo, depois de mudar o formulário). E se você vincular o formulário a um ROPA, o apontamento "fora do Inventário" some automaticamente ao voltar — sem reverificar. Detalhes em [Verificador de Formulários](/modulos/formularios/#o-resultado-fica-salvo).

## De onde vêm as "Notícias da ANPD" no Painel?

São as **últimas manchetes publicadas no site da ANPD** (gov.br), trazidas automaticamente para a 3ª coluna da seção superior do Painel para você se manter atualizado sobre regulação, orientações e prazos. Cada título abre a matéria no site da ANPD em nova aba. O bloco é **só informativo** e **não envia nenhum dado** da sua organização à ANPD. As notícias ficam em cache e são atualizadas periodicamente; se o site da ANPD estiver instável, o painel continua funcionando e o bloco mostra um link para o site. Detalhes em [Painel › Notícias da ANPD](/modulos/painel/#notícias-da-anpd).
