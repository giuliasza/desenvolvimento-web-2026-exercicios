# 🎮 Sistema de Exercícios - Setup

## 🔔 Configuração de Notificações

### Discord Webhook

1. No seu servidor Discord, vá em **Configurações do Canal**
2. **Integrações** → **Webhooks** → **Novo Webhook**
3. Copie o URL do webhook
4. No GitHub: **Settings** → **Secrets** → **Actions**
5. Adicione: `DISCORD_WEBHOOK` com o URL copiado

### WhatsApp (via OpenClaw)

1. Tenha OpenClaw rodando
2. No GitHub Secrets, adicione:
   - `OPENCLAW_URL`: URL da sua instância (ex: https://p38a.com.br)
   - `OPENCLAW_TOKEN`: Token de autenticação
   - `PROFESSOR_PHONE`: Seu número WhatsApp (+558197700690)

---

## 🏆 Leaderboard ao Vivo

Acesse: **https://petrosbarreto.github.io/desenvolvimento-web-2026-exercicios/leaderboard.html**

_(Após habilitar GitHub Pages)_

### Habilitar GitHub Pages

1. **Settings** → **Pages**
2. **Source:** Deploy from a branch
3. **Branch:** main, / (root)
4. **Save**

---

## 📊 Badges

Adicione ao README do repositório principal:

```markdown
![Alunos](https://raw.githubusercontent.com/petrosbarreto/desenvolvimento-web-2026-exercicios/main/.github/badges/alunos.svg)
![Exercícios](https://raw.githubusercontent.com/petrosbarreto/desenvolvimento-web-2026-exercicios/main/.github/badges/exercicios.svg)
![Média](https://raw.githubusercontent.com/petrosbarreto/desenvolvimento-web-2026-exercicios/main/.github/badges/media.svg)
```

---

## ⚙️ Workflows Automáticos

### Aula 01/02 - Validação
Roda automaticamente em cada PR nas pastas respectivas

### Detector de Plágio
Roda em todos PRs abertos/atualizados

### Ranking Semanal
Toda segunda-feira 00:00 UTC

### Notificações
Quando PR é aberto, fechado, merged

### Badges
Atualizam após ranking

---

## 🎯 Checklist de Setup

- [ ] Configurar Discord Webhook (opcional)
- [ ] Configurar OpenClaw Webhook (opcional)
- [ ] Habilitar GitHub Pages
- [ ] Testar primeiro PR
- [ ] Ver notificação chegar
- [ ] Ver ranking atualizar
- [ ] Ver leaderboard ao vivo

---

**Tudo funciona out-of-the-box!** 🚀

Notificações são opcionais - o sistema funciona sem elas.
