---
title: "Gestão no site (fora do wp-admin)"
nav_order: 15
parent: "Módulos"
permalink: /modulos/gestao-frontend/
role: encarregado
routes: ["#/"]
screenshots: [v3rlgpd-80-gestao-dashboard, v3rlgpd-81-gestao-mapa, v3rlgpd-82-gestao-ropa, v3rlgpd-83-gestao-politicas, v3rlgpd-84-gestao-dashboard-mobile]
last_verified: 2026-08-16
status: publicado
---

# Gestão no site (fora do wp-admin)

Até aqui, este manual sempre falou da gestão do V3RLGPD **dentro do painel** do WordPress (o `wp-admin`). Existe uma segunda porta de entrada: o mesmo trabalho — Dashboard, Políticas, Inventário, Atendimentos e o resto — pode rodar numa **página comum do site**, através do shortcode `[v3rlgpd_gestao]`.

> 💡 **Por que isso importa**
>
> Muitas organizações **não dão acesso ao `wp-admin`** para quem não é da equipe técnica — é uma prática de segurança comum, e frequentemente uma decisão de quem cuida do site, fora do seu controle. Isso deixava o Encarregado sem trabalho, mesmo tendo sido a pessoa nomeada pela diretoria para cuidar da LGPD. Com o shortcode, quem administra o site publica **uma página** e o Encarregado passa a trabalhar por ali, sem nunca precisar entrar no painel.

## Como publicar a página

1. No WordPress, crie uma **página nova** (ex.: "Gestão LGPD").
2. No conteúdo, insira o shortcode:

   ```
   [v3rlgpd_gestao]
   ```

3. Publique.

[![Dashboard do V3RLGPD numa página do site](/assets/screenshots/v3rlgpd-80-gestao-dashboard.png)](/assets/screenshots/v3rlgpd-80-gestao-dashboard.png)
*A mesma gestão do painel, aberta numa página comum do site — aqui, o Dashboard.*

> ⚠️ **Página de trabalho, não de conteúdo**
>
> A página com o shortcode recebe automaticamente a marcação `noindex`: buscadores como o Google não a indexam, porque ela é uma **área de trabalho** interna, não conteúdo do site. Isso é automático — você não precisa configurar nada. Mas vale reforçar do seu lado: **não coloque essa página no menu público** do site. Trate-a como uma URL que você compartilha só com quem precisa acessá-la (por link direto, ou por um menu restrito a usuários logados, se o seu tema tiver esse recurso).

> ✅ **Não confunda com a Central de Privacidade**
>
> A [Central de Privacidade](/modulos/central-privacidade/) (shortcode `[v3rlgpd_privacidade]`) é a página **pública**, para o titular exercer direitos e ler políticas. A página de **Gestão** (`[v3rlgpd_gestao]`) é o oposto: é **privada**, para quem administra a conformidade. São shortcodes diferentes, com públicos diferentes — não os coloque na mesma página.

> ⚠️ **A largura do painel é a da página**
>
> O painel de gestão ocupa toda a largura disponível do espaço onde você colocou o shortcode. Se a página tiver uma coluna estreita, uma barra lateral ou um container com largura limitada, o painel respeita esse limite e fica igualmente estreito.
>
> Por isso, escolha uma **página de largura cheia**, sem barra lateral, para publicar o shortcode — o painel tem tabelas e formulários, e precisa de espaço para ficar confortável.
>
> Se a página já estiver publicada e o painel parecer apertado, **o ajuste é no layout da página** — a largura do container, o modelo de página do tema, ou remover a barra lateral —, não em alguma configuração do plugin. O V3RLGPD não tem um ajuste de largura próprio: ele se adapta ao espaço que o site oferece, e nunca altera o layout do site para se acomodar. Isso vale para qualquer tema ou construtor de páginas que você use.

## Quem enxerga o quê

A página reage a **quem está logado** no momento em que ela carrega:

- **Visitante deslogado** — vê um aviso, *"Entre para acessar a gestão do V3RLGPD."*, com um link **Fazer login**. Depois de entrar, ele volta para a mesma página.
- **Usuário logado sem papel no V3RLGPD** — vê o aviso *"Sua conta não tem acesso à gestão do V3RLGPD. Fale com quem administra o site."* Nenhum dado do plugin chega ao navegador dessa pessoa: nem a tela de gestão é montada, nem a chamada que buscaria os dados acontece — o bloqueio já é feito antes de qualquer um dos dois.
- **Usuário com papel no plugin** (Encarregado, Atendente ou Auditor — ver [Equipe / Acessos](/modulos/equipe-acessos/)) — vê a gestão completa, com **as mesmas seções e as mesmas permissões** que teria no painel. Quem só audita continua só auditando; quem atende titulares continua sem os botões de exclusão. Nada muda por estar fora do `wp-admin`.

> ⚠️ **Quando der errado**
>
> Se um usuário da sua equipe disser que a página só mostra um aviso, confira **dois pontos, nesta ordem**: (1) ele está logado no site (não só "lembrado" pelo navegador — sessões expiram); (2) ele tem um papel atribuído em **Equipe / Acessos**. A mensagem "Fale com quem administra o site" normalmente significa que o segundo passo ainda não foi feito.

## O que continua exclusivo do painel do WordPress

Nem tudo migrou para a página de gestão no site. Quatro áreas continuam existindo **só dentro do `wp-admin`**:

- **Configurações**
- **Equipe / Acessos**
- **Shortcodes**
- **Primeiros Passos**

Isso é proposital: são telas de **configuração da instalação** (chaves de acesso, papéis de outras pessoas, textos de ajuda inicial), não do dia a dia de conformidade — e ficam de fora da página de gestão como camada extra de proteção, além das permissões de cada papel.

**Na prática, isso significa:** quem só tem papel do plugin (sem ser administrador do WordPress) **depende de alguém que alcance o painel** para configurar a organização, o Encarregado, os papéis da equipe e os demais ajustes gerais. Se a sua organização nomeou um Encarregado sem acesso ao `wp-admin`, é a pessoa que administra o site quem precisa fazer essa configuração inicial por ele — depois disso, o Encarregado segue sozinho pela página de gestão.

## Como isso aparece na tela

Nas telas em que uma ação só existe no painel, a experiência muda conforme quem está olhando:

- **Administrador do WordPress** (mesmo acessando pela página de gestão) vê um **link que abre o painel em nova aba**, para completar a ação ali.
- **Quem tem só papel do plugin** vê, no lugar do link, uma **frase explicando** que aquilo se configura no painel e que é preciso falar com quem administra o site.

Não é um erro nem uma permissão negada pelo plugin — é a configuração morando no lugar certo. Por exemplo, no Dashboard e no Mapa de Conformidade, a gestão pela página do site mostra as mesmas seções que o painel:

[![Mapa de Conformidade na página de gestão](/assets/screenshots/v3rlgpd-81-gestao-mapa.png)](/assets/screenshots/v3rlgpd-81-gestao-mapa.png)
*Mapa de Conformidade, Inventário (ROPA) e Políticas funcionam de ponta a ponta pela página — o menu de abas é o mesmo do painel.*

[![Inventário (ROPA) na página de gestão](/assets/screenshots/v3rlgpd-82-gestao-ropa.png)](/assets/screenshots/v3rlgpd-82-gestao-ropa.png)
*O Inventário aceita criar, editar e excluir registros normalmente — a mesma permissão do usuário no painel vale aqui.*

[![Políticas na página de gestão](/assets/screenshots/v3rlgpd-83-gestao-politicas.png)](/assets/screenshots/v3rlgpd-83-gestao-politicas.png)
*Políticas, com o Assistente e a Galeria de Modelos disponíveis, igual ao painel.*

## No celular

A página de gestão funciona em tela estreita: as abas se reorganizam para caber na largura da tela, e o conteúdo se ajusta junto.

[![Gestão no celular](/assets/screenshots/v3rlgpd-84-gestao-dashboard-mobile.png)](/assets/screenshots/v3rlgpd-84-gestao-dashboard-mobile.png)
*No celular, as abas quebram em mais de uma linha, mas continuam todas visíveis — nenhuma fica escondida atrás de um menu.*

> 💡 É útil para o Encarregado que precisa registrar um incidente ou responder a um pedido de titular fora do computador — sem instalar nada além do que o navegador do celular já tem.

## Veja também

- [Painel](/modulos/painel/)
- [Equipe / Acessos](/modulos/equipe-acessos/)
- [Central de Privacidade](/modulos/central-privacidade/) (a página pública, para comparar)
