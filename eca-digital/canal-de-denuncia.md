---
title: "Canal de denúncia e retirada de conteúdo"
nav_order: 6
parent: "ECA Digital (Lei 15.211/2025)"
permalink: /eca-digital/canal-de-denuncia/
role: encarregado
routes: ["#/reports", "/e2e-eca-test"]
screenshots: [den-01, den-02]
last_verified: 2026-09-06
status: rascunho
---

# Canal de denúncia de conteúdo

Se o seu site tem **conteúdo gerado por usuário** (comentários, fórum, mural, depoimentos abertos), o ECA Digital (arts. 28–30) pede um **canal de denúncia** acessível, além de procedimento de **retirada** e **contestação**.

> Sites institucionais com **controle editorial** (sem conteúdo de usuário) tendem a ser **dispensados/modulados** desse dever. Use o [enquadramento](/eca-digital/enquadramento/) para saber se ele se aplica a você.

## Canal público (shortcode)

Coloque o shortcode `[v3rlgpd_denuncia]` numa página pública. Ele exibe um formulário que **exige identificação** do conteúdo e do denunciante (**denúncia anônima não é permitida**, art. 29 §2) e tem proteção anti-spam.
<!-- screenshot: den-01 — formulário público de denúncia -->

Como todo bloco do plugin, ele aceita os atributos `titulo`, `descricao`, `nivel` e `classe` para se encaixar no layout da sua página (veja [Controle o layout de cada bloco](/guias/publicar-central-privacidade/#controle-o-layout-de-cada-bloco-título-descrição-nível-e-classe)).

> ✅ O botão de envio deste formulário segue o mesmo tema de **Configurações → Aparência** e mantém fundo e texto legíveis mesmo que o tema do site tente repintar só um dos dois — a mesma correção aplicada ao aviso de cookies (ver [Consentimento & Cookies › Aparência](/modulos/consentimento/#aparência)).

### O aviso de identificação não é ocultável

`descricao="nao"` some com o texto de apoio em quase todo bloco do plugin, mas **não** neste. O aviso de que a denúncia é identificada — nunca anônima — não é texto de apoio, é a **condição de uso** do formulário (art. 29 §2). Escondê-lo faria alguém preencher e enviar acreditando estar anônimo, o que a lei não permite. Ele continua aparecendo mesmo com `descricao="nao"`.

## Triagem no painel

Em **Denúncias**, o encarregado vê as denúncias recebidas, abre cada uma e **muda o status** (Recebida → Em análise → Conteúdo removido / Improcedente), registrando a **justificativa**.
<!-- screenshot: den-02 — triagem da denúncia + aviso do art. 30 -->

Ao marcar **Conteúdo removido**, o sistema mostra um **lembrete do art. 30**: a organização deve **notificar o autor** do conteúdo e abrir **prazo de recurso**.

> ⚠️ A **retirada** do conteúdo acontece no seu site/CMS — o V3RLGPD **registra e orienta** a denúncia, não remove o conteúdo automaticamente. Não é parecer jurídico.
