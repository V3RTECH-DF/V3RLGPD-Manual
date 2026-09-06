---
title: "Configurar o Encarregado"
nav_order: 1
parent: "Guias por tarefa"
permalink: /guias/configurar-dpo/
task: configurar-dpo
role: encarregado
routes: ["#/settings"]
screenshots: [v3rlgpd-08-settings-dpo, v3rlgpd-70-encarregado-autofill]
last_verified: 2026-06-24
status: publicado
---

# Configurar o Encarregado

O Encarregado é o contato de privacidade da sua organização. Cadastrá-lo é o **primeiro passo** — esses dados aparecem publicamente na Central de Privacidade.

[![Configurações de identidade do Encarregado](/assets/screenshots/v3rlgpd-08-settings-dpo.png)](/assets/screenshots/v3rlgpd-08-settings-dpo.png)
*Configurações → Identidade.*

## Passo a passo

1. No painel, abra **V3RLGPD → Configurações**.
2. Na aba **Encarregado**, preencha:
   - **Nome ou Setor** — quem responde pela privacidade (ex.: "Encarregado de Dados" ou "Setor de Privacidade").
   - **E-mail de Contato** — por onde o titular fala com a organização.
   - **Telefone** (opcional).
   - **Logo da Organização** — aparece nos relatórios PDF e na Central de Privacidade.
3. Clique em **Salvar Identidade**.

> 💡 **Atalho:** se o Encarregado já é um usuário do site, clique em **"Preencher a partir de um usuário do WordPress"**, busque a pessoa e o nome e o e-mail entram sozinhos (você ainda pode editar).
>
> ![Preencher a partir de um usuário do WordPress](/assets/screenshots/v3rlgpd-70-encarregado-autofill.png)

> ⚠️ **Não confunda com o papel de acesso.** Esta tela é a designação **formal** do Encarregado (o contato publicado). Dar a alguém o **papel** "Encarregado" em [Equipe / Acessos](/modulos/equipe-acessos/) é outra coisa: concede permissões no painel, sem efeito formal. Pode ser a mesma pessoa — só são cadastros diferentes.

> ✅ **Boas práticas**
>
> Use um e-mail **institucional e monitorado** (ex.: `privacidade@suaosc.org`), não o pessoal de um voluntário. Se a pessoa sair, o contato continua funcionando.

> 💡 Ao salvar, o item **Encarregado Configurado** do [Índice de Conformidade](/modulos/painel/) passa a contar como verificado.

## Modo de exclusão de políticas

Nesta mesma aba há o **Modo de Exclusão de Políticas**, que define o que o botão **Excluir** (na lista de Políticas) faz:

- **Soft Delete** (padrão) — **arquiva**: a política some do painel e do site, mas o registro e o histórico de versões são preservados (para auditoria). Recomendado.
- **Hard Delete** — **apaga em definitivo** a política e todo o seu histórico de versões do banco, sem volta.

> ⚠️ **Atenção**
>
> O *Hard Delete* apaga a política definitivamente — você **perde a rastreabilidade** de qual texto esteve no ar. Mantenha em *Soft Delete* salvo se tiver um motivo claro para apagar de vez. (Os consentimentos já coletados são preservados nos dois modos.)

> ✅ **Quer só tirar do ar, não apagar?** Não use a exclusão — use **[Inativar](/modulos/politicas/#inativar-e-reativar-uma-política)** na lista de Políticas. Inativar é reversível e preserva tudo; excluir (acima) é outra coisa.
