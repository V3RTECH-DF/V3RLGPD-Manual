---
title: "Novidades"
nav_order: 13
permalink: /novidades/
---

# Novidades

O que mudou no V3RLGPD, em linguagem leve. Para o histórico técnico completo, fale com a equipe de implantação.

## Versões 1.60 a 1.62 — Formulários do Elementor entram na roda

Quem monta as páginas com o **Elementor Pro** e usa o formulário dele ficava sem cobertura nenhuma: sem prazo de guarda, sem descarte automático, sem atendimento ao titular sobre aquelas respostas. Agora esses formulários são tratados como todos os outros:

- Aparecem na lista do **[Verificador de Formulários](/modulos/formularios/)** e são **verificados** (consentimento, dados pessoais, dados sensíveis, presença no Inventário).
- Podem **gerar um rascunho de ROPA** a partir dos campos, ou ser **vinculados** a uma atividade existente.
- Entram na **[retenção/expurgo](/modulos/retencao/)** — o descarte apaga a resposta e os arquivos enviados — e são alcançados pelo **[atendimento ao titular](/modulos/atendimentos/)**.

> A versão **gratuita** do Elementor não tem o widget de formulário. Isso vale para quem usa o **Elementor Pro**; em sites sem ele, nada aparece e nada quebra.

*Nos bastidores:* o Elementor identifica cada formulário por um código com letras, e o Verificador só aceitava números — o que faria ele analisar o formulário errado, em silêncio. Isso foi corrigido junto. **Nada muda** para quem usa Forminator, Fluent Forms, WPForms, Gravity ou Contact Form 7.

## Versão 1.59 — O atendimento ao titular agora enxerga os formulários

Quando alguém perguntava *"quais dados vocês têm sobre mim?"*, o V3RLGPD procurava o e-mail apenas nos **consentimentos** e nos **comentários**. As **respostas de formulário** — muitas vezes onde estão os dados mais completos da pessoa — ficavam de fora. Ou seja: o plugin respondia por omissão, e o currículo que a pessoa enviou seguia intacto depois de uma "eliminação".

- O **Localizar** agora encontra também as **respostas de formulário** daquela pessoa (Forminator, Fluent Forms, WPForms, Gravity Forms, CF7/Flamingo e, a partir da 1.60, Elementor Forms).
- O **Eliminar** apaga essas respostas **junto com os arquivos que a pessoa enviou**.
- Ao final, o relatório da ação detalha **quanto foi eliminado em cada origem** — dá para copiar esse resumo direto para a resposta ao titular.

> ⚠️ **Uma ressalva honesta:** **contas de usuário do WordPress** e **dados do WooCommerce** ainda **não entram** nessa busca. Está em avaliação, e não é esquecimento: apagar um pedido de loja esbarra em **prazo legal de guarda fiscal**, e uma exclusão automática poderia destruir um registro que a organização é obrigada a manter. Se o seu site tem loja ou área de usuários, confira esses sistemas à mão antes de dar o pedido por concluído.

Veja em **[Atendimentos (DSAR)](/modulos/atendimentos/)** e no guia **[Atender uma solicitação](/guias/atender-solicitacao/)**.

## Versão 1.58 (correções) — O descarte agora apaga também os arquivos enviados

Faltava uma peça no ciclo de vida do dado: quando um formulário era descartado pela regra de retenção, o plugin apagava a resposta — mas **deixava o arquivo anexado no servidor**. O currículo em PDF, o comprovante, a foto: continuavam lá, mesmo com o painel indicando "descartado".

- Agora o **arquivo é apagado junto** com a entrada. Vale para **Forminator**, **Fluent Forms**, **WPForms** e **Gravity Forms** — e, desde a 1.60, também para o **Elementor Forms**.
- O mesmo passou a valer para os **anexos de resposta dos atendimentos** — os documentos que o Encarregado anexa ao responder um pedido de titular, que costumam conter justamente os dados pessoais daquela pessoa.
- A remoção é feita **só dentro da pasta de arquivos do próprio site**, por segurança: nada fora dali é tocado.

> 💡 **Vale conferir:** arquivos que ficaram para trás em descartes **anteriores a esta correção** continuam no servidor. Se o seu site já rodava a retenção em formulários com anexo, peça à equipe de implantação uma limpeza dessa pasta.

Veja em **[Retenção & Expurgo](/modulos/retencao/)**.

## Versão 1.58 — Transferência internacional agora registra a base legal

Quando uma atividade envia dados para fora do Brasil (um serviço de e-mail, uma nuvem no exterior), a LGPD exige mais do que dizer "vai para os Estados Unidos": exige registrar **por que** essa transferência é permitida — o **mecanismo de proteção do art. 33**.

- No Inventário (ROPA), ao marcar **"Ocorre Transferência Internacional?"**, você agora escolhe também o **mecanismo de proteção** numa lista pronta (país com proteção adequada, **cláusulas-padrão contratuais**, consentimento do titular…), e pode anotar um **detalhe da garantia**.
- O mecanismo aparece nos **relatórios** e na **vitrine pública** ("Sim — Estados Unidos · Cláusulas-padrão contratuais").
- O **Assistente de Políticas** usa esse mecanismo para escrever a cláusula de transferência internacional, e avisa quando alguma atividade tem transferência **sem** mecanismo informado.

Registros antigos, feitos antes desta versão, aparecem como **"mecanismo não informado"** até você completá-los.

Veja em **[Inventário (ROPA)](/modulos/inventario-ropa/)**.

## Versão 1.57 — Registro de ciência de documentos

Quando um documento importante muda — o **estatuto**, uma **política**, os **termos** —, agora você pode exigir que os usuários **tomem ciência da nova versão**, e o V3RLGPD guarda a prova: **quem** deu ciência, de **qual documento** e em **qual versão**.

- No editor do documento, marque **"Exigir ciência dos usuários"**.
- Quando você publica uma nova versão, cada usuário logado vê um **aviso no centro da tela** listando todos os documentos atualizados, com um botão **"Estou ciente"** que confirma todos de uma vez.
- Em **Atendimento ao Titular → Ciência de documentos**, você acompanha quem já confirmou o quê.

[![Aviso de novas versões de documentos](/assets/screenshots/v3rlgpd-31-ciencia-banner.png)](/assets/screenshots/v3rlgpd-31-ciencia-banner.png)
*Um aviso, vários documentos, um clique.*

Veja o passo a passo em **[Exigir ciência de um documento](/guias/exigir-ciencia-documento/)**.

## Versão 1.56 — O Detector acha os seus rastreadores e diz de onde eles vêm

Seu banner de cookies só consegue segurar os scripts que **você** colou nas Configurações. Se o Google Analytics do site entrou por outro plugin ou está escrito no tema, ele carrega para todo visitante — tenha consentido ou não. O problema é que quase ninguém sabe o que tem instalado no próprio site.

O **[Detector de Conformidade](/modulos/detector/)** resolve isso: ele varre o site publicado, encontra os rastreadores que estão disparando sem consentimento e traz cada um para dentro do V3RLGPD com um clique. Isso já existia — **o que mudou é que agora ele sabe explicar o que fazer com cada um**.

[![Achado de rastreador com a origem identificada](/assets/screenshots/v3rlgpd-91-detector-rastreador-origem.png)](/assets/screenshots/v3rlgpd-91-detector-rastreador-origem.png)
*Dois rastreadores, dois conselhos diferentes — porque vêm de lugares diferentes.*

- **Ele identifica a origem provável.** Cruzando o rastreador encontrado com os plugins que você tem ativos, o Detector agora **diz de onde ele provavelmente vem** — em vez do antigo "remova a tag original do tema/plugin", que não dizia qual.
- **E o conselho muda conforme a origem.** Se for um **trecho colado** (no tema ou num injetor de código), importar é seguro: nada se perde. Mas se vier de um **plugin com funcionalidade própria** (MonsterInsights, Site Kit, GTM4WP e afins), o Detector **não oferece mais a importação** — e explica por quê: esses plugins fazem muito mais que emitir a tag, e trazer só o trecho faria você perder o resto **em silêncio**. Ele nomeia o plugin e diz o que exatamente você perderia.
- **Vários rastreadores? Traga todos de uma vez.** Ter mais de um é o normal (Tag Manager + Analytics + Pixel). Agora há o botão **"Resolver todos"**: uma revisão, um Salvar. E se preferir ir um a um, o que você trouxe fica **pendente até salvar** — dá para ir e voltar sem perder nada. Antes, resolver um segundo achado sem ter salvado o primeiro **descartava o primeiro sem avisar**.
- **Ele é honesto sobre o que não sabe.** Quando não encontra nada, o Detector não diz mais "não encontramos scripts de rastreamento" — porque isso soa como "seu site está limpo", e não era o que ele tinha verificado. Agora ele **lista os rastreadores que reconhece** e avisa que o resultado **não garante** ausência de rastreamento. Se a sua organização usa uma ferramenta fora dessa lista, a conferência manual continua com você.
- **Corrigido: o alarme agora apaga.** Havia um defeito incômodo — depois de você seguir o conselho e importar o script, o achado crítico **continuava lá, para sempre**. Agora, feita a correção, ele some na próxima verificação. Era o que faltava para o ciclo "corrija e confira" funcionar.

> 💡 **Uma coisa que o V3RLGPD não faz — de propósito**
>
> Ele **não desativa** plugins de terceiros, nem se oferece para isso. Não temos como saber o que quebraríamos no seu site, e essa decisão é da sua organização. Nosso papel é dizer **o quê**, **por quê** e **o que você perde** — com precisão suficiente para você decidir.

> Onde: **Auditoria de Conformidade → Detector**. Detalhes em [Detector de Conformidade](/modulos/detector/#o-caso-dos-rastreadores-cookies-sem-consentimento) e [Consentimento & Cookies](/modulos/consentimento/).

## Versão 1.54 — O banner de cookies, revisto de ponta a ponta

O módulo de cookies passou por uma revisão completa. O que muda na prática:

- **"Alterar Preferências de Cookies" agora funciona.** O botão da Central de Privacidade reabre o painel **já mostrando o que o titular escolheu antes**, para ele rever e ajustar. Se você tentou usá-lo antes e ele não fez nada ao ser clicado, era um defeito nosso — está corrigido.
- **Revogar vale na hora.** Quando o titular retira uma categoria que havia aceitado, a página recarrega e o rastreador **para imediatamente**. Antes a mudança só passava a valer na navegação seguinte — a tela confirmava "salvo" enquanto o script continuava rodando.
- **A recusa é registrada como recusa.** No Registro de Consentimentos, quem recusou não é mais indistinguível de quem aceitou — o que importa muito, já que esse registro é a sua prova.
- **O consentimento não se perde mais em silêncio.** Em sites com cache de página, havia casos em que o registro não chegava ao servidor sem ninguém perceber. Agora, se o envio falhar, a decisão é reenviada na visita seguinte.
- **O banner segue o tema** definido em Configurações → Aparência. Antes ele ignorava o preset e ficava com as cores de fábrica. *Isso muda a aparência do seu banner mesmo se você nunca trocou o tema.*

> Onde: Central de Privacidade (para o visitante) e Configurações → Banner de Cookies (para você). Detalhes em [Consentimento & Cookies](/modulos/consentimento/).

> ⚠️ **Aproveite para conferir uma coisa:** o banner só segura os scripts que **você colou nas Configurações do V3RLGPD**. Rastreador instalado por outro plugin ou escrito no tema passa direto por ele. Veja [como verificar](/modulos/consentimento/#como-o-plugin-segura-os-scripts).

## Versão 1.49 — Relatórios em PDF de verdade

Todos os relatórios — **Conformidade**, **Inventário (ROPA)**, **Ações do Encarregado** e **RIPD** — ganharam um botão **Baixar PDF** que gera um **arquivo PDF pronto**, baixado com **um clique** e igual em qualquer navegador. Antes, "exportar" era escolher "Salvar como PDF" na caixa de impressão do navegador; agora o documento sai **formatado como relatório** (não como um print da tela), com **texto selecionável** e **cabeçalho e a logo da organização**.

- A **logo** vem de **Configurações → Organização** (a mesma usada nos e-mails e na Central de Privacidade). Sem logo configurado, o relatório sai normalmente, só sem a imagem.
- O botão **Imprimir** continua disponível, para quem preferir a impressão do navegador.

> Onde: em cada relatório, no topo. Detalhes em [Relatórios](/modulos/relatorios/).

## Versão 1.43 — Detector de Conformidade

Chegou o **Detector de Conformidade**: uma nova aba em **Auditoria de Conformidade** que **varre o seu site publicado** e gera um relatório em linguagem clara com o que precisa de atenção — confrontando o que você configurou no plugin com o que está **de fato no ar**.

- Três modos: **Rápido** (na hora), **Padrão** e **Completo** (análise profunda, roda em segundo plano e avisa por e-mail ao terminar).
- Encontra, entre outros, **rastreadores disparando sem consentimento** (Google Analytics, Tag Manager, Pixel do Facebook…) e, no botão **Resolver**, **leva o script já preenchido** para a aba **Cookies & Analytics** — onde ele passa a carregar só depois do consentimento.
- Cada achado tem **gravidade** (crítico / atenção / conforme) e um botão **Resolver** que leva ao lugar certo, muitas vezes já preenchido. O relatório é **datado, ordenável e pode ser exportado/impresso**.
- A aba de Configurações **"Banner de Cookies" agora se chama "Cookies & Analytics"**.

Detalhes em [Detector de Conformidade](/modulos/detector/). Lembrando: o Detector **ajuda, não garante validade jurídica**.

## Versão 1.42 — Menu mais simples e organizado

O menu do painel ficou **mais enxuto e menos intimidante**. Telas que trabalham juntas foram **agrupadas em uma página só, com abas** (como já acontecia em Configurações). O menu lateral passou de 15 para **8 itens**:

- **Auditoria de Conformidade** (novo) reúne, em abas, o **Mapa de Conformidade** e o **Verificador de Formulários**.
- **Atendimento ao Titular** (novo) reúne, em abas, **Consentimentos**, **Atendimentos**, **Denúncias**, **Incidentes**, **Retenção** e **Ações do Encarregado**.
- **Equipe / Acessos** deixou de ser um item separado e virou uma **aba dentro de Configurações** (visível só para o administrador).
- O item **"RIPD"** agora se chama **"Relatório de Impacto (RIPD)"**, mais claro.

O **cabeçalho** de cada tela também mudou: agora a logo aparece com o **nome da seção ao lado** e a **versão** do plugin logo abaixo — mais espaço e leitura mais organizada.

> Nada se perde: **atalhos e links antigos continuam funcionando** e levam você direto ao novo lugar. Cada pessoa continua vendo só o que pode acessar.

## Versão 1.41 — Controle de quem faz o quê na equipe

O V3RLGPD ganhou a tela **Equipe / Acessos**. Antes, ou a pessoa era administradora do WordPress (e via tudo) ou não entrava no plugin. Agora o administrador pode **dar acesso ao plugin a outras pessoas da equipe sem torná-las administradoras do site**, escolhendo um papel para cada uma:

- **Encarregado** — opera toda a conformidade; não faz migração nem desinstalação.
- **Atendente** — cuida do dia a dia com os titulares (atendimentos, consentimentos, denúncias, incidentes); não executa exclusões de dados nem comunica incidentes (isso fica com o Encarregado).
- **Auditor** — **somente leitura** em tudo; ideal para financiadores, conselheiros e revisores externos.

O administrador do WordPress continua com acesso total, e nada muda nas instalações que já estão no ar — o controle por papéis só "liga" quando o administrador atribui papéis. A tela tem **busca e paginação**, pensada para sites com muitos usuários, e é **exclusiva do administrador**.

> Em **Equipe / Acessos** no menu (visível só para administradores). Detalhes em [Equipe / Acessos](/modulos/equipe-acessos/).

## Versão 1.40 — O Verificador agora lembra do que você já verificou

O **Verificador de Formulários** passou a **salvar o resultado** de cada verificação.

- **Não precisa reverificar tudo ao voltar** — se você troca de tela (ou vai gerar um ROPA) e volta, o status de cada formulário **continua lá**, com **"verificado em DD/MM/AAAA HH:MM"**.
- Cada formulário ganhou **"Ver relatório"** (reabre o último resultado salvo) e **"Reverificar"** (refaz e atualiza a data).
- **Mais esperto com o ROPA** — se você vincular o formulário a uma atividade (ou gerar um ROPA a partir dele), o apontamento "fora do Inventário" **some sozinho** ao voltar à tela.

> Em **Verificador de Formulários** no menu. Detalhes em [Verificador de Formulários](/modulos/formularios/#o-resultado-fica-salvo).

## Versão 1.39 — Notícias da ANPD no Painel

O **Painel** ganhou um bloco **"📰 Notícias da <a href="https://www.gov.br/anpd/pt-br" target="_blank" rel="noopener noreferrer">ANPD</a>"** na 3ª coluna da seção superior (ao lado do anel de conformidade), com as **últimas manchetes** da Autoridade Nacional de Proteção de Dados.

- Acompanhe **regulação, orientações, prazos e consultas públicas** sem sair do painel.
- Cada manchete traz a **data** e abre a notícia no **site da ANPD** em nova aba.
- É só informativo: **não** coleta nem envia nenhum dado da sua organização.
- Se a fonte da ANPD ficar instável, o **painel continua normal** — o bloco mostra um link para o site.

> No **Painel** (tela inicial), na 3ª coluna da seção superior. Detalhes em [Painel › Notícias da ANPD](/modulos/painel/#notícias-da-anpd).

## Versão 1.38 — Agora com formulários do Google

O Verificador de Formulários passou a cobrir **Google Forms** — muito usados por organizações para inscrições, doações e pesquisas.

- **+ Adicionar Google Form** — cole a **URL pública** do formulário e o V3RLGPD **lê os campos automaticamente** (sem login na sua conta Google).
- **🔍 Procurar no site** — o V3RLGPD **varre as páginas publicadas** atrás de Google Forms incorporados ou linkados e os adiciona sozinho.
- **Tratado como os outros** — o Google Form ganha o selo **"Externo (Google)"** e a mesma **verificação de conformidade** e o **auto-ROPA** (gerar/vincular Inventário) dos formulários do WordPress.
- **Se não der para ler sozinho** (form privado, por exemplo), você **informa os campos à mão** e segue normalmente.
- **Atenção importante** — a **retenção automática não cobre** Google Forms: os dados ficam no Google, então a exclusão é feita lá. A tela avisa isso de forma clara. O V3RLGPD lê só a **estrutura** do formulário, **nunca as respostas**.

> Em **Verificador de Formulários** no menu. Detalhes em [Formulários do Google](/modulos/formularios/#formulários-do-google-google-forms).

## Versão 1.37 — Inventário (ROPA) em um clique, a partir do formulário

O **Verificador de Formulários** deixou de só **apontar** que um formulário está fora do Inventário: agora ele ajuda a **resolver**.

- **Gerar rascunho de ROPA a partir dos campos** — no relatório, quando um formulário está **fora do Inventário (ROPA)**, um botão abre o editor do Inventário **já preenchido** com o que os campos revelam: as **categorias de dados** (Nome, E-mail, Telefone…), a **origem** ("Formulário do site") e, quando há pistas, a **finalidade** e a **base legal** — sempre marcadas como **"sugestão — confirme"**.
- **Você revisa e salva** — ao salvar, a atividade é criada **e** o formulário já fica **vinculado** a ela; a pendência some. A ferramenta **sugere, não decide**.
- **Dados sensíveis ou de menores** viram **avisos** no rascunho, com atalho ao RIPD e a opção de marcar o consentimento dos pais.
- **Já tem a atividade?** Dá para **vincular** o formulário a uma atividade existente pelo seletor da tabela, sem criar duplicata.
- **✏️ Editar formulário** — cada formulário na lista ganhou um link que abre o **construtor do formulário** (no seu plugin) em uma **nova aba**, para corrigir uma pendência sem perder a tela.

> Em **Verificador de Formulários** no menu. Detalhes em [Verificador de Formulários](/modulos/formularios/). O rascunho é um **ponto de partida** — confira a base legal e os campos em branco; **não** substitui análise jurídica.

## Versões 1.35 e 1.36 — Verificador de Formulários

A tela **Formulários** virou **Verificador de Formulários** e ganhou um superpoder: além de mapear cada formulário ao Inventário (ROPA), agora ela **analisa os campos** dos seus formulários e aponta possíveis problemas de conformidade.

- **Análise dos 5 plugins** — Contact Form 7, Forminator, WPForms, Gravity e Fluent. Clique **Verificar** (ou **Verificar todos**) e veja um **relatório por formulário**.
- **O que ela aponta** — campos que **parecem dados pessoais** (e **sensíveis**), ausência de **checkbox de consentimento**, formulário **fora do Inventário (ROPA)**, e indícios de **dados de crianças/adolescentes** sem campo/consentimento de responsável.
- **Você no comando** — a ferramenta **aponta, não corrige**, e a análise é **consultiva** (baseada em pistas do nome/tipo de cada campo). Cada apontamento pode ser **marcado como revisado** (com nota) para silenciar falsos alarmes — e a revisão **expira** se o formulário for editado, para você conferir de novo.
- **Ótimo para formulários antigos** — aquele formulário de inscrição de anos atrás, feito antes da LGPD, finalmente tem como ser auditado em segundos.

> Em **Verificador de Formulários** no menu. Detalhes em [Verificador de Formulários](/modulos/formularios/). A ferramenta **ajuda** a achar pendências; **não** substitui análise jurídica.

## Versão 1.34 — Canal de feedback no painel

Agora dá para **falar direto com quem desenvolve o V3RLGPD**, sem sair do painel.

- **Botão "💬 Enviar feedback"** no topo do painel (ao lado do Manual) abre um formulário para mandar **sugestões**, **relatos de problema (bug)** e **depoimentos** à **V3RTECH e à RIT** por e-mail — com **cópia para você**, que serve de registro.
- **Anexos** em sugestão/bug (uma captura de tela, um relatório); **foto** no depoimento.
- **Consentimento** em todos os tipos (tratar/contatar); no **depoimento**, um consentimento específico para a equipe **publicar** seu nome, foto, cargo e organização em divulgação.
- **Nada fica guardado no seu site** — como as desenvolvedoras não acessam o ambiente, o e-mail é o registro, e o retorno chega por e-mail (pode levar alguns dias).
- O link **"Manual / Guia LGPD"** do cabeçalho virou **botão**, combinando com o novo.

> Em qualquer tela do painel, botão **💬 Enviar feedback**. Passo a passo em [Enviar feedback](/guias/enviar-feedback/). Este canal é sobre o **plugin**; **dúvidas jurídicas** estão fora do escopo dele.

## Versões 1.31 a 1.33 — Atendimento ao titular mais seguro

O atendimento às solicitações de titulares (DSAR) ganhou mais segurança e melhores ferramentas para o Encarregado.

- **Nada é concluído sem revisão** — antes, alguns pedidos (acesso, portabilidade, informação sobre compartilhamento) eram encerrados **na hora**, buscando dados **só no site**. O risco: a sua organização pode tratar dados também no **papel, em planilhas ou em outros sistemas** — e responder "não há dados" com base apenas no site seria um **falso-negativo**. Agora **todo** pedido vai ao **Encarregado**, e o titular é avisado de que será analisado **em até 15 dias úteis**.
- **Declaração de escopo da organização** — em **Configurações → Organização**, você responde "A organização trata dados pessoais **fora deste site**?". Essa afirmação orienta o atendimento e habilita (ou não) a resposta automática.
- **Insumos para o Encarregado** — ao abrir um pedido, além da busca no site, aparece um **painel com as atividades do Inventário (ROPA)** (origem, compartilhamento, transferência internacional) e um **banner de escopo** que lembra se pode haver dados fora do site.
- **Resposta automática assistida** — quando a organização declarou tratar dados **apenas neste site** e o pedido é **informativo**, o Encarregado ganha o botão **Responder automaticamente**: o plugin monta o resultado, **envia o e-mail ao titular** (na portabilidade, com o **JSON anexado**) e marca como Concluída. Eliminação e revogação seguem **sempre manuais**.
- **Anexar documentos na resposta** — o Encarregado pode anexar **um ou mais arquivos** à resposta enviada ao titular; eles ficam em **área protegida** (não acessível por link público).
- **E-mails com a sua identidade** — os e-mails de privacidade passaram a trazer a **logo da organização** no topo e o **contato do Encarregado** no rodapé, com os status sempre em português.

> Veja [Atendimentos (DSAR)](/modulos/atendimentos/) e o passo a passo em [Atender uma solicitação](/guias/atender-solicitacao/). A ferramenta **ajuda** o Encarregado a atender; **não** substitui a análise dele nem garante conformidade.

## Versão 1.30 — Ações do Encarregado

Um novo módulo para o **encarregado registrar o que faz** — e ter, a qualquer momento, um relatório pronto para prestação de contas.

- **Registro de Ações do Encarregado** — anote projetos, capacitações, pontos de atenção, auditorias, contatos com a ANPD, reuniões e anotações. Por padrão é leve (tipo, título, descrição, data); quando quiser planejar, há **status, prazo e responsável** opcionais.
- **Evidência protegida** — anexe um arquivo (PDF, imagem, documento) que fica em **área protegida** (não acessível por link público, diferente da galeria de mídia) **ou** informe um **link**, com um botão para **verificar** se ele responde.
- **Vínculo opcional** — ligue uma ação a um Incidente, RIPD ou atividade do Inventário (ROPA) para dar rastreabilidade.
- **Relatório imprimível** — gere um PDF com o cabeçalho da organização e as ações do período/tipo que escolher — ideal para financiadores, auditoria ou a ANPD.

> Em **Ações do Encarregado** (entre Retenção e Configurações no menu). Passo a passo em [Registrar uma ação do Encarregado](/guias/registrar-acoes-dpo/); detalhes em [Ações do Encarregado](/modulos/acoes-dpo/). O módulo **ajuda** a demonstrar o trabalho do encarregado; **não** garante conformidade nem substitui assessoria jurídica.

## Versão 1.29 — Assistente de Políticas

Completando a família de assistentes (Inventário e RIPD), agora **criar uma Política de Privacidade ou Termos de Uso** também é um passo a passo guiado — sem encarar a folha em branco.

- **Assistente de Políticas** — escolha o tipo (**Privacidade** ou **Termos de Uso**), responda a uma **triagem** de perguntas simples e o assistente monta um **rascunho sob medida** a partir dos dados que o plugin já tem (organização, **Encarregado**, **Inventário/ROPA**, perfil de menores).
- **Confere o essencial antes de começar** — se faltar a **razão social** ou o **Encarregado**, o assistente interrompe e leva você às Configurações (a política precisa identificar o controlador e o contato do Encarregado). Inventário vazio? Ele só avisa — você pode seguir.
- **Sugestões e revisão** — na Política de Privacidade, ele aponta cláusulas que talvez faltem e confere se o texto está **coerente com o seu Inventário (ROPA)**.
- **Você decide quando publicar** — o padrão é **salvar como rascunho** para aprovação interna; publicar é uma escolha explícita. O texto é um ponto de partida (modelos de mercado) e **não substitui revisão jurídica**.
- **Novo cadastro da Organização** — em Configurações há uma aba **Organização** (razão social, CNPJ, endereço, contato), reaproveitada nas políticas e nos relatórios.

> Em **Políticas**, botão **🪄 Usar Assistente**. Passo a passo em [Publicar uma política](/guias/publicar-politica/); detalhes em [Políticas › O Assistente](/modulos/politicas/#o-assistente-de-politicas). O assistente **ajuda** a redigir; **não** substitui revisão jurídica nem garante validade legal.

## Versão 1.28 — Assistente do RIPD e Termos de Uso

Depois do Assistente de Inventário, agora o **Relatório de Impacto (RIPD)** também tem um assistente — e o documento mais técnico da LGPD fica acessível para quem não é da área.

- **Assistente do RIPD** — em vez de encarar um documento em branco, você responde uma **triagem** de perguntas sim/não e o assistente diz **se vale fazer o RIPD** e por quê. Em seguida, monta um **rascunho** a partir do seu Inventário: já traz a **matriz de risco pré-preenchida** (com probabilidade, severidade, mitigação e risco residual sugeridos) e a **necessidade/proporcionalidade** redigida a partir das atividades. Você revisa tudo e finaliza no editor.
- **O parecer e a decisão continuam seus** — os campos de **Parecer do Encarregado** e **Decisão** ficam por sua conta (com exemplos de redação como referência): o assistente organiza, mas a análise final é do Encarregado.
- **Não duplica trabalho** — se a atividade escolhida já tiver um RIPD, o assistente avisa e sugere revisar o existente.
- **Termos de Uso** — o manual ganhou uma página de **[Termos de Uso](/termos-de-uso/)**, deixando claro que a ferramenta **ajuda, mas não substitui** o Encarregado nem garante conformidade, e que a responsabilidade é da organização.
- **Visual mais consistente** — botões, links e destaques de toda a interface passaram a usar as cores oficiais da identidade visual.

> Em **RIPD**, botão **✨ Assistente de RIPD**. Passo a passo em [Fazer um RIPD com o Assistente](/guias/fazer-ripd-assistente/); detalhes do módulo em [RIPD](/modulos/ripd/). O assistente **ajuda** a elaborar o RIPD; **não** é parecer jurídico.

## Versão 1.27 — Selo no painel e relatórios que imprimem direito

- **Selo de Conformidade no painel** — o selo que você já podia exibir no site agora também aparece no **Painel**, logo abaixo do anel de conformidade, com a sua faixa (bronze/prata/ouro). Ali tem um botão **Copiar** para o shortcode `[v3rlgpd_selo]` — cole em qualquer página do site para mostrar o selo aos visitantes. Veja [Painel › Selo](/modulos/painel/#o-selo-de-conformidade-no-painel).
- **Impressão dos relatórios corrigida** — ao **Imprimir / Baixar PDF** um relatório (Conformidade, Inventário/ROPA ou RIPD), agora sai **só o relatório**, sem o menu do WordPress junto e com paginação limpa. As listas (origem dos dados, medidas de segurança etc.) aparecem legíveis, sem códigos técnicos.

## Versões 1.24 a 1.26 — Assistente de Inventário: monte seu ROPA respondendo perguntas

Montar o **Inventário de Tratamento (ROPA)** do zero costuma intimidar quem não é da área. Agora há um **Assistente de Inventário** que faz o trabalho pesado por você:

- **Responda em linguagem simples** — o assistente pergunta o que a sua organização faz ("envia newsletter?", "recebe doações?", "cadastra voluntários?", "vende online?"...) e, a cada "sim", **monta um rascunho de atividade** já preenchido (finalidade, base legal sugerida, dados coletados, retenção).
- **Você revisa antes de salvar** — nada é gravado sem a sua confirmação. Base legal e prazo aparecem como **sugestões a conferir** (a responsabilidade final é da organização).
- **Nunca apaga, só acrescenta** — se você rodar o assistente de novo, ele detecta o que já existe e cria **apenas as atividades novas**.
- **Liga seus formulários** — para atividades que vêm de formulários do site, dá para **vincular o formulário** ali mesmo, já deixando a retenção automática configurada.
- **Cuida de crianças e adolescentes** — se a sua organização atende menores de 18, o assistente marca os titulares corretamente, ajuda no **consentimento parental** e recomenda fazer um **RIPD** para esses tratamentos.

> Em **Inventário (ROPA)**, botão **✨ Assistente de Inventário**. O assistente **ajuda** a montar o inventário; ele **não** substitui a análise da sua organização. Veja [Inventário (ROPA)](/modulos/inventario-ropa/#assistente-de-inventario).

## Versões 1.22 e 1.23 — Mude o V3RLGPD de site e decida o que fica ao desinstalar

- **Migração entre sites** — **exporte** os dados que você escolher (configurações, políticas, ROPA, consentimentos e mais) em um arquivo **JSON** e **importe** em outra instalação do V3RLGPD. Você marca só os escopos que quer; exportar **não apaga nada**, e a importação **substitui** os escopos escolhidos no destino (com confirmação antes de sobrescrever). Em Configurações → Saída de Dados.
- **O que acontece ao desinstalar** — agora você decide: **manter os dados** (padrão — se reinstalar, tudo continua lá) ou **apagar tudo definitivamente** ao remover o plugin. A opção de apagar pede uma confirmação, porque é irreversível.

> O arquivo de migração contém **dados pessoais em texto** — guarde com cuidado e apague depois de migrar. Veja [Configurações › Saída de Dados](/modulos/configuracoes/#saida-de-dados).

## Versões 1.20 e 1.21 — A cara da sua Central, do seu jeito

- **Temas de aparência** — escolha entre cinco temas de cores prontos (V3RLGPD, Neutro Escuro, Terra, Oceano e Alto Contraste) para a Central, o selo e os shortcodes combinarem com o seu site — **sem mexer no painel administrativo**. Em Configurações → Aparência.
- **Personalização avançada** — quer ir além? Ajuste **cor a cor**, os **cantos** e a **fonte**, com **preview ao vivo** e um **aviso de contraste** que sinaliza quando uma combinação fica difícil de ler.

> Veja [Configurações › Aparência](/modulos/configuracoes/#aparencia).

## Versão 1.19 — Painel mais limpo, com menu nativo do WordPress

- **Navegação por submenus** — a antiga barra de navegação interna do plugin deu lugar a **submenus nativos do WordPress**, listados abaixo de "V3RLGPD" no menu lateral do painel. A interface fica mais limpa, sobra espaço na vertical e a experiência combina com o restante do administrativo do site.
- **Abre direto na tela certa** — ao clicar em uma seção no menu, o painel já abre na tela correspondente, sem rodeios. Fluxos internos (como relatórios e o modo de edição de políticas) continuam fluidos, sem recarregar a página.

## Versão 1.18 — Mostre sua conformidade com o Selo

- **Selo de Conformidade LGPD** — um novo componente público que permite à sua organização **exibir o nível de conformidade no próprio site**, em **três formatos** à escolha (fita, medalha ou cartão). Use o shortcode `[v3rlgpd_selo]` na página que quiser. A partir da 1.18.1, o selo ganhou um visual refinado (medalhão metálico) e o texto "Compromisso LGPD".
- **A aparência do selo acompanha o tema** — as cores, os cantos e a fonte do selo seguem o tema escolhido em [Configurações › Aparência](/modulos/configuracoes/#aparencia), para combinar com a identidade do seu site.
- **Índice de Conformidade mais consistente** — Painel, Mapa de Conformidade e Primeiros Passos passaram a calcular o Índice a partir de **uma única fonte**, garantindo o mesmo número em toda a ferramenta.

> O selo informa o nível de conformidade autodeclarado/verificado pela ferramenta; ele **ajuda a comunicar seu compromisso**, mas **não atesta validade jurídica** nem isenta a organização de responsabilidade.

## Versões 1.11 a 1.17 — Conformidade com o ECA Digital

Chegou o apoio ao **ECA Digital** (Lei 15.211/2025), a lei que protege crianças e adolescentes na internet — especialmente relevante para organizações que trabalham com esse público. Veja a nova seção [ECA Digital](/eca-digital/).

- **Descubra se a lei te alcança** — uma triagem rápida no [Mapa de Conformidade](/eca-digital/enquadramento/) mostra só os deveres que se aplicam ao seu caso (e avisa quando seu site, por ter controle editorial, está dispensado da verificação de idade).
- **Consentimento dos pais** para dados de menores, com registro de prova ([saiba mais](/eca-digital/consentimento-parental/)).
- **Privacidade por padrão** e **transparência aos pais** na sua Central de Privacidade.
- **Aviso** contra publicidade/perfilamento dirigido a menores na configuração de cookies.
- **Novo módulo [RIPD](/modulos/ripd/)** — avalie os riscos de um tratamento com uma matriz simples e gere o relatório em PDF.
- **Novo módulo [Denúncias](/modulos/denuncias/)** — canal público para reportar conteúdo que viole direitos de crianças e adolescentes, com triagem no painel.

> O ECA Digital é uma lei **diferente** da LGPD: esses deveres aparecem **à parte** e **não** alteram o seu Índice de Conformidade da LGPD. O conteúdo ajuda a se situar e **não substitui orientação jurídica**.

## Versão 1.7 — Tamanho da imagem das políticas

- **Imagem em pequeno, médio, grande ou extra grande** — agora dá para ajustar o tamanho da imagem/ícone das políticas externas no card da Central. Defina um padrão em Configurações → Páginas & Integração ou ajuste caso a caso pelo atributo `tamanho` do shortcode (ex.: `[v3rlgpd_politica id="3" tamanho="extra-grande"]`). O padrão (pequeno) mantém o visual atual. Veja [as opções de exibição](/modulos/central-privacidade/#opcoes-de-exibicao-das-politicas).

## Versão 1.6 — Excluir políticas (com cuidado)

- **Excluir política** — além de **inativar** (que só tira do site e é reversível), agora dá para **excluir** uma política de vez. O comportamento segue o **Modo de Exclusão** configurado em Configurações → Identidade: *arquivar* (mantém o registro para auditoria, mas some do painel) ou *excluir em definitivo* (apaga também o histórico de versões — **perde-se a rastreabilidade** de qual texto esteve no ar e quando). Antes de excluir, o sistema mostra um aviso claro e recomenda usar **Inativar** quando o objetivo é apenas tirar do site. Os **consentimentos já coletados nunca são apagados**, em nenhuma modalidade. Veja [Políticas › Excluir](/modulos/politicas/#excluir-uma-politica).
- **Correção visual (1.6.1)** — políticas externas (por link) deixaram de exibir, na lista, os avisos de "versões publicadas / nenhuma versão ativa" (que só fazem sentido para políticas internas) — evitando a impressão de que estariam incompletas.

## Versão 1.5 — Ative e desative políticas sem apagar nada

- **Inativar e reativar política** — depois de publicada, uma política pode ser **inativada** quando foi incorporada a outra, substituída ou deixou de valer. A política inativa **some da Central e dos shortcodes**, mas nada é apagado: conteúdo, histórico de versões e consentimentos ficam preservados, e você pode **reativar** quando quiser. Na lista, as inativas mostram um selo **"INATIVA"**. Vale para políticas internas e externas. Se a política inativada for a de Privacidade, o Índice de Conformidade avisa — reative-a para o indicador voltar. Veja [Políticas](/modulos/politicas/#inativar-e-reativar-uma-politica).

## Versão 1.4 — Políticas externas e exibição sob medida

- **Política por link (externa)** — agora dá para cadastrar uma política apontando para um documento que já existe (um PDF, uma página de wiki), em vez de reescrevê-la no plugin. Ela aparece na Central como um card com resumo, imagem/ícone e um botão "Ler a política completa". O número da versão é informado à mão (e mantê-lo atualizado é responsabilidade da sua organização).
- **Resumo nas políticas** — políticas internas também ganharam um campo de resumo, usado quando você opta por exibir só o resumo.
- **Opções de exibição** — você decide como as políticas aparecem: texto integral, só o resumo ou só o título; e se mostra título, link e imagem. Configure um padrão global em Configurações → Páginas & Integração ou ajuste caso a caso pelos atributos do shortcode (ex.: `[v3rlgpd_politicas modo="titulo"]`).
- **Escolher a página da Central** — montou sua própria página da Central com os shortcodes? Agora você pode indicá-la como a página oficial, e o Índice de Conformidade e o banner de cookies passam a apontar para ela.
- **Avisos mais suaves no painel** (1.4.1) — as confirmações e alertas do painel deixaram de usar os pop-ups do navegador e passaram a aparecer como notificações discretas no próprio plugin; ações sensíveis (como exclusões) pedem confirmação em uma janela padronizada.

Veja em [Políticas](/modulos/politicas/) e [Central de Privacidade](/modulos/central-privacidade/).

## Versão 1.3 — Central de Privacidade personalizável

Antes, a Central de Privacidade era uma página única gerada automaticamente. Agora você pode **montar a sua própria página**, posicionando cada elemento onde quiser (inclusive em construtores como o Elementor):

- **Shortcodes por elemento** — `[v3rlgpd_dpo]` (contato do Encarregado), `[v3rlgpd_politicas]` (suas políticas ativas), `[v3rlgpd_cookies]` (preferências de cookies), além do `[v3rlgpd_politica id="N"]` (uma política específica) e do `[v3rlgpd_privacidade]` (a Central completa).
- **Continua simples para quem quer o pronto** — a página completa autogerada segue disponível e é o caminho recomendado.
- **Aviso de responsabilidade** — ao montar a página à mão, a tela de Configurações lembra que você precisa manter o contato do Encarregado e o canal de pedidos, para não deixar buracos de conformidade.
- **Acesso rápido ao manual** — agora há um link "📖 Manual / Guia LGPD" sempre visível no topo do painel.

Veja os shortcodes em [Central de Privacidade](/modulos/central-privacidade/).

## Versão 1.2 — Primeiros passos guiados, banner opcional e políticas mais seguras

- **Assistente de Primeiros Passos** — um roteiro guiado (card no Painel + tela própria) que detecta sozinho o que já está feito e leva direto à tela que resolve cada pendência, com convite de revisão periódica. Veja [Primeiros Passos](/primeiros-passos/).
- **Banner de cookies opcional** — você decide se exibe o banner; ao desativá-lo, os scripts de análise/marketing deixam de carregar (sem consentimento, não carrega).
- **Políticas mais seguras** — não é mais possível publicar uma política **vazia**; ao abrir uma política, o texto já aparece para revisão e dá para **reaproveitar versões anteriores**; e há um shortcode para exibir uma política em qualquer página.
- **Interface mais confortável** — o painel aproveita melhor a largura da tela (com limite em telas muito grandes), o menu do V3RLGPD aparece no início do admin junto da família V3RLGPD, e a navegação no celular ficou mais fluida.

## Versão 1.1 — Retenção & ciclo de vida dos dados

A LGPD pede que dado pessoal não fique guardado para sempre. Esta versão automatiza o **fim** desse ciclo:

- **Expurgo automático com janela de aviso** — ao fim do prazo que você define, o plugin **anonimiza** o registro; antes disso, avisa o Encarregado (7 dias por padrão), que pode **cancelar ou adiar**.
- **Anonimização que preserva a prova** — em vez de apagar tudo, remove-se o que identifica a pessoa e mantém-se o comprovante de que a obrigação foi cumprida.
- **Prazos onde fazem sentido** — dados do próprio plugin (atendimentos concluídos, consentimentos revogados) nas Configurações; dados do site, **por atividade** no Inventário (ROPA), sempre com **opt-in** (nada entra sem você ligar).
- **Conectores prontos** para WordPress (usuários, comentários), WooCommerce e os principais plugins de formulário (CF7, Fluent Forms, Forminator, Gravity Forms, WPForms) — e um encaixe extensível para novas origens.
- **Mapeamento de Formulários** — uma tela que liga cada formulário do site a uma atividade do inventário, atalho para quem tem muitos formulários.
- **Fila de Retenção** no menu e **alerta no Painel** dos registros que vão expirar em breve.
- **Revogação de consentimento de verdade** — ao concluir um pedido de revogação, os consentimentos daquele e-mail passam a contar prazo para expurgo.

Veja o passo a passo em [Retenção & Expurgo](/modulos/retencao/).

## Versão 1.0 (MVP)

A primeira versão do produto entrega a base da conformidade para organizações:

- **Painel de conformidade** com Índice (verificado + autodeclarado), indicadores de atendimentos (DSAR) e visualizações das políticas.
- **Gestão de políticas** com versionamento, aceite por versão, editor com checklist da LGPD, **Assistente** que pré-preenche a partir do Encarregado e do inventário, e **Galeria de Modelos**.
- **Central de Privacidade pública** gerada automaticamente, com políticas ativas, identidade do Encarregado e formulário de pedidos.
- **Atendimentos (DSAR)** com duplo opt-in, controle de prazo (SLA), **execução assistida** (localizar, exportar e eliminar sob comando do Encarregado) e **auto-atendimento** para pedidos simples.
- **Consentimento**: banner de cookies (scripts só carregam com consentimento) e conectores para formulários populares.
- **Incidentes**: registro e comunicação rastreável aos titulares afetados.
- **Inventário (ROPA)**: registro das operações de tratamento, com finalidade e base legal.
- **Relatórios**: relatório de conformidade em PDF e **backup/exportação total** dos dados (ZIP com CSV/JSON e checksums).
- **Webhooks** para integrar eventos essenciais a ferramentas como n8n e Zapier.
- **Manual integrado** no painel, com link para este guia completo.

> 💡 Os ajustes de performance, segurança e robustez seguem sendo aprimorados a cada ciclo. Veja o que vem por aí em [Roadmap](/roadmap/).
