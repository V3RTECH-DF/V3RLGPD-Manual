---
title: "Consentimento & Cookies"
nav_order: 5
parent: "Módulos"
permalink: /modulos/consentimento/
role: encarregado
routes: ["/central-de-privacidade/", "#/settings"]
screenshots: [v3rlgpd-21-cookie-banner, v3rlgpd-08b-settings-cookies, v3rlgpd-103-cookies-escolha-vigente, v3rlgpd-104-cookies-sem-escolha]
last_verified: 2026-09-05
status: publicado
---

# Consentimento & Cookies

A LGPD trata o **consentimento** como algo que precisa ser **livre, informado e demonstrável**. Este módulo cuida de duas frentes: o **banner de cookies** e o **registro de consentimento em formulários**.

## Banner de cookies

[![Banner de cookies](/assets/screenshots/v3rlgpd-21-cookie-banner.png)](/assets/screenshots/v3rlgpd-21-cookie-banner.png)
*Na primeira visita, o titular escolhe aceitar, recusar não-essenciais ou personalizar.*

O banner aparece na primeira visita ao site. O ponto central:

> 💡 **Por que isso importa**
>
> Cookies de **análise e marketing** (Google Analytics, pixels de redes sociais) só podem ser carregados **depois** que o visitante consente. O V3RLGPD segura os scripts que você configurar nele até haver consentimento — ou seja, recusar significa **não carregar**, não apenas "fingir que não carregou". Isso é o que diferencia um banner de verdade de um aviso decorativo.

O visitante pode:

- **Aceitar Todos** — libera os cookies não-essenciais.
- **Recusar Não-Essenciais** — mantém só o necessário ao funcionamento.
- **Personalizar** — escolhe por categoria.

São duas categorias que dependem de consentimento: **Analytics** e **Marketing**. Os cookies **Necessários** aparecem marcados e travados — sem eles o site não funciona, então não há o que consentir.

### Como o plugin segura os scripts

Você cola os códigos de análise e marketing em **Configurações → Banner de Cookies**, cada um no campo da sua categoria. O plugin **não** coloca esse código na página. Ele o embrulha numa etiqueta inerte, que o navegador enxerga mas não sabe executar — o código fica lá, parado.

Só quando o visitante consente é que o plugin desembrulha e ativa. Na dúvida, não carrega.

> ⚠️ **O banner só alcança os scripts que você colar aqui**
>
> Este é o ponto mais importante da página. Se o Google Analytics (ou qualquer outro rastreador) do seu site estiver instalado **por outro plugin** ou escrito **direto no tema**, o V3RLGPD **não sabe que ele existe** e **não o segura**: ele carrega para todo visitante, tenha consentido ou não.
>
> Nesse cenário o seu banner vira exatamente o "aviso decorativo" que ele existe para não ser — e a sua organização fica exposta **achando que está protegida**, que é a pior das situações.

### Você não precisa procurar os rastreadores sozinho

O **[Detector de Conformidade](/modulos/detector/)** varre o seu site publicado e **encontra os rastreadores que estão disparando sem consentimento** — inclusive os que entraram por outro plugin ou pelo tema, justamente os que você não sabia que estavam lá.

Melhor: ele **tenta identificar de onde cada um vem** e ajusta o conselho conforme isso.

- Se for **só um trecho** colado no tema ou num injetor de código, o botão **Resolver** traz o script para cá já preenchido — você revisa, salva e remove da origem. Nada se perde.
- Se vier de um **plugin com funcionalidade própria** (MonsterInsights, Site Kit, GTM4WP…), o Detector **não** oferece a importação, e explica por quê: esses plugins fazem muito mais que emitir a tag, e trazer só o trecho faria você perder o resto em silêncio. Nesse caso o caminho é a configuração de consentimento do próprio plugin.

**Comece por aí.** É o jeito mais rápido de descobrir se o seu banner está protegendo alguma coisa de fato — e o [Detector](/modulos/detector/#o-caso-dos-rastreadores-cookies-sem-consentimento) explica cada caso.

> ⚠️ **Mas ele reconhece os principais, não todos**
>
> O Detector conhece os rastreadores mais comuns (Google Analytics, GTM, Meta Pixel, Google Ads, LinkedIn, TikTok, Hotjar, Clarity). Se a sua organização usa outra ferramenta, **ela não é detectada** — e "nenhum rastreador encontrado" não é o mesmo que "site limpo". A conferência manual continua valendo.

> 💡 **Quem classifica é você**
>
> O plugin não sai varrendo o site atrás de cookies nem adivinha o que é análise e o que é marketing. Quem decide é você, ao colar cada código no campo certo. É uma decisão sua, e ela precisa refletir o que o script realmente faz.

### Mudar de ideia depois

O consentimento não é uma escolha definitiva: o titular pode revê-la quando quiser. Na **Central de Privacidade**, o botão **"Alterar Preferências de Cookies"** reabre o painel **já mostrando o que ele escolheu antes** — as categorias aceitas aparecem marcadas. Ele ajusta o que quiser e salva.

Esse botão pode aparecer sozinho em qualquer página, pelo shortcode `[v3rlgpd_cookies]` — útil num rodapé, ou numa página de política que não usa a Central completa. Diferente da versão dentro da Central, este bloco **diz qual é a escolha vigente do visitante** antes do botão, algo como *"Sua escolha atual: cookies necessários e analíticos"*.

[![Bloco de cookies mostrando a escolha vigente do visitante](/assets/screenshots/v3rlgpd-103-cookies-escolha-vigente.png)](/assets/screenshots/v3rlgpd-103-cookies-escolha-vigente.png)
*Quem já escolheu vê exatamente o que aceitou.*

Quem nunca escolheu nada vê uma frase dizendo isso, não uma escolha inventada — o plugin não assume "aceitou tudo" nem "recusou tudo" quando não há decisão registrada.

[![Bloco de cookies sem escolha registrada](/assets/screenshots/v3rlgpd-104-cookies-sem-escolha.png)](/assets/screenshots/v3rlgpd-104-cookies-sem-escolha.png)
*Antes de qualquer escolha, o bloco diz isso — em vez de inventar uma.*

> 💡 **A leitura é sempre do navegador, nunca do servidor**
>
> A página que hospeda este bloco costuma ser a mesma que um cache de página inteira guarda e serve a todo mundo igual. Se o texto da escolha viesse do servidor, a escolha de um visitante apareceria para os seguintes — um vazamento de informação entre pessoas diferentes. Por isso quem lê o cookie e escreve a frase é o navegador de cada um, depois que a página carrega.

> 💡 **Revogar vale na hora**
>
> Quando o titular **retira** uma categoria que havia aceitado, a página é **recarregada** e o script correspondente deixa de ser carregado imediatamente. Não é cosmético: o rastreador realmente para. (Aceitar uma categoria **nova** não recarrega — ela passa a valer na hora, sem interromper a navegação.)

### O que fica registrado

Toda decisão do visitante vira um registro no [Registro de Consentimentos](/modulos/painel/): **o quê** ele escolheu, **quando**, de qual **endereço de IP e navegador**, e **vinculada à versão da política que estava vigente naquele momento**.

Vale para os três casos — aceite total, aceite parcial e **recusa**. A recusa é registrada **como recusa**, nunca como consentimento.

> 💡 **É aqui que está o valor**
>
> Banner qualquer site tem. O que a LGPD cobra da sua organização é **provar** que o consentimento existiu, nos termos em que foi dado. O ônus dessa prova é do controlador — ou seja, seu, não do titular. É esse registro que você mostra numa fiscalização.

Se o registro não conseguir chegar ao servidor no momento do clique (uma falha de rede, por exemplo), a decisão fica guardada no navegador do visitante e é reenviada na próxima vez que ele abrir uma página. A escolha dele não se perde.

### Aparência

O banner **segue o tema definido em Configurações → Aparência**. Ao trocar o preset (ou personalizar as cores), o banner acompanha — cores, botões, arredondamento — junto com o resto das telas públicas do plugin.

## Configurar o banner

Ative o banner e cole os scripts de cada categoria em **Configurações → Banner de Cookies**.

[![Configurações do banner de cookies](/assets/screenshots/v3rlgpd-08b-settings-cookies.png)](/assets/screenshots/v3rlgpd-08b-settings-cookies.png)
*Configuração do banner de cookies no painel.*

### Exibir ou não o banner

A partir da versão 1.2, há uma opção **"Exibir o banner de cookies no site"**. Ela existe porque há discussão na <a href="https://www.gov.br/anpd/pt-br" target="_blank" rel="noopener noreferrer">ANPD</a> sobre a real eficácia dos banners — e algumas organizações podem preferir não usá-lo (por exemplo, quando não carregam scripts de análise/marketing).

> ⚠️ **Desligar o banner desliga os scripts não-essenciais**
>
> Se você **desativar** a exibição do banner, o V3RLGPD **deixa de carregar** os scripts de Analytics e Marketing — porque, sem o banner, não há como coletar o consentimento do visitante. Carregar esses scripts sem consentimento seria justamente o que a LGPD não permite. O painel avisa isso na hora em que você desliga a opção.

> 💡 **Reflexo no Índice de Conformidade**
>
> O item "Consentimento / Cookies" do Dashboard acompanha esse interruptor: banner **ligado** = ✅; **desligado** = pendente. É a sua intenção de uso refletida diretamente no painel.

## Consentimento em formulários

Quando um visitante preenche um formulário do seu site (newsletter, inscrição, contato), o plugin registra o **consentimento**: o quê, quando e com qual finalidade a pessoa concordou — gerando uma **prova consultável**.

O V3RLGPD se integra a plugins de formulário populares por meio de **conectores**, seguindo um padrão único de registro de consentimento.

> ✅ **Boas práticas**
>
> Peça consentimento **específico** ("aceito receber a newsletter"), não genérico ("aceito tudo"). Consentimento amplo demais é frágil: se questionado, é difícil provar que a pessoa entendeu ao que estava concordando.

> ⚠️ **Atenção — consentimentos órfãos**
>
> O [Painel](/modulos/painel/) sinaliza "consentimentos órfãos" — registros que não estão ligados a uma versão de política. Eles indicam que algo foi coletado sem o vínculo correto. Vale revisar quando aparecerem.
