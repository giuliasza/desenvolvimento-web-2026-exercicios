# 🔒 Segurança do Sistema de Exercícios

## ⚠️ Riscos e Mitigações

### 1. GitHub Secrets
**Risco:** Acesso aos secrets permite enviar notificações não autorizadas

**Mitigações:**
- ✅ Repo de exercícios é PÚBLICO, mas secrets são PRIVADOS
- ✅ Nunca fazer `echo $SECRET` em workflows (vaza nos logs)
- ✅ GitHub encrypta secrets com AES-256
- ✅ Secrets só acessíveis em Actions do próprio repo

**Recomendações:**
- [ ] Revisar quem tem acesso Admin/Write ao repo
- [ ] Ativar "Require approval for all outside collaborators" em Settings → Actions
- [ ] Nunca adicionar alunos como collaborators com Write access

---

### 2. Discord Webhook
**Risco:** URL do webhook permite enviar mensagens no canal

**Mitigações:**
- ✅ Webhook só envia mensagens (não lê, não deleta)
- ✅ Discord permite deletar webhook a qualquer momento
- ✅ Discord mostra nome do webhook (fácil identificar abuso)

**Recomendações:**
- [x] Criar canal isolado: `#bot-exercicios` (não misturar com chat geral)
- [ ] Configurar permissões: só professor pode ver o canal
- [ ] Se vazar: deletar webhook e criar novo (2 cliques)

**Como revogar (se necessário):**
1. Discord → Editar Canal → Integrações
2. Webhooks → Deletar
3. GitHub → Secrets → Deletar `DISCORD_WEBHOOK`

---

### 3. OpenClaw Token (WhatsApp)
**Risco:** Token permite enviar mensagens via sua instância OpenClaw

**Mitigações:**
- ✅ Token em secret (não vaza em código)
- ✅ OpenClaw tem rate limiting
- ✅ Só envia para `PROFESSOR_PHONE` (hardcoded no workflow)

**Recomendações:**
- [ ] Verificar se OpenClaw tem logs de API calls (auditar uso)
- [ ] Considerar criar token de bot separado (se possível)
- [ ] Monitorar uso incomum (muitas mensagens)

**Como revogar (se necessário):**
1. OpenClaw → Settings → Revoke token
2. GitHub → Secrets → Deletar `OPENCLAW_TOKEN`

---

### 4. Repo Público
**Risco:** Código do bot está exposto (alunos podem ver lógica de validação)

**Mitigações:**
- ✅ É intencional (transparência pedagógica)
- ✅ Validação é determinística (não há "truques")
- ⚠️ Alunos podem estudar testes e adaptar código

**Filosofia:**
> "Se você só passa nos testes decorando, não aprendeu. O objetivo é APRENDER, não enganar o bot."

**Recomendações:**
- [ ] Adicionar validação manual do professor (não confiar 100% no bot)
- [ ] Randomizar algumas validações (ex: pedir features diferentes por aluno)
- [ ] Detector de plágio compara entre alunos (não só com template)

---

## ✅ Checklist de Segurança

### Setup Inicial
- [x] Secrets configurados em Actions (não no código)
- [x] Repo de exercícios é PÚBLICO (mas secrets PRIVADOS)
- [ ] Discord webhook configurado em canal isolado
- [ ] OpenClaw token testado (apenas notificações)

### Monitoramento
- [ ] Revisar logs de Actions semanalmente
- [ ] Verificar mensagens Discord/WhatsApp não esperadas
- [ ] Auditar quem tem Write access ao repo

### Resposta a Incidentes
- [ ] Saber revogar Discord webhook (2 cliques)
- [ ] Saber revogar OpenClaw token
- [ ] Saber pausar GitHub Actions (Settings → Actions → Disable)

---

## 🔐 Configuração Recomendada

### Repositórios
- `desenvolvimento-web-2026` → **PRIVADO** (só professor)
- `desenvolvimento-web-2026-professor` → **PRIVADO** (só professor)
- `desenvolvimento-web-2026-exercicios` → **PÚBLICO** (alunos fazem fork)

### Acessos GitHub
- **Admin:** Só você
- **Write:** Ninguém (nem alunos)
- **Read:** Todos (repo público)

### Discord
- Canal `#bot-exercicios` → **Privado** (só você vê)
- Webhook → **Dedicado** (1 webhook = 1 canal)

### OpenClaw
- Token → **Dedicado ao bot** (se possível)
- Destino → **Só seu número** (hardcoded)

---

## 🚨 Cenários de Ataque

### Cenário 1: Aluno tenta burlar validação
**Ataque:** Aluno descobre lógica do bot e adapta código só para passar

**Defesa:**
- Detector de plágio compara entre alunos
- Professor revisa PRs manualmente (bot é auxiliar)
- Validações testam conhecimento real (não só sintaxe)

### Cenário 2: Aluno tenta acessar secrets
**Ataque:** Aluno abre PR malicioso com `echo $DISCORD_WEBHOOK`

**Defesa:**
- GitHub NUNCA exibe secrets nos logs (substitui por ***)
- GitHub Actions em repos públicos não rodam automaticamente para PRs de forks
- Só colaboradores com Write podem triggar Actions

**Proteção adicional (Settings → Actions):**
- [x] "Require approval for all outside collaborators"
- [x] "Approve and run workflow" (manual)

### Cenário 3: Webhook Discord vaza
**Ataque:** Alguém consegue URL e spamma canal

**Defesa:**
- Deletar webhook (2 cliques)
- Criar novo webhook
- Atualizar secret no GitHub
- Discord mostra origem (fácil identificar)

---

## ✅ Resumo: É Seguro?

**SIM, com as seguintes condições:**

1. ✅ Secrets NUNCA no código (só em GitHub Secrets)
2. ✅ Revisar permissões do repo (Admin só você)
3. ✅ Discord em canal privado
4. ✅ OpenClaw token monitorado
5. ✅ Validação manual do professor (bot é auxiliar)

**Nível de risco:** 🟢 BAIXO (se seguir recomendações)

---

## 📞 Contatos de Emergência

- **GitHub:** https://github.com/settings/tokens (revogar tokens)
- **Discord:** Editar Canal → Integrações → Webhooks → Deletar
- **OpenClaw:** Gateway → Settings → Revoke token

---

_Última revisão: 2026-02-15_
