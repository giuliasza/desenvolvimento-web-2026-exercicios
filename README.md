# 🤖 Exercícios Automatizados - Desenvolvimento Web 2026.1

**Professor:** Petros Barreto  
**Disciplina:** Códigos de Alta Performance Web  
**Instituição:** UNINASSAU Recife

---

## 🎯 Como Funciona

Este repositório usa **GitHub Actions** para validar automaticamente seus exercícios!

### Para Alunos

1. **Fork** este repositório
2. **Clone** seu fork para sua máquina
3. Resolva os exercícios na pasta correspondente
4. **Commit** suas alterações
5. **Push** para seu fork
6. Abra um **Pull Request** com título: `[Aula XX] Seu Nome`
7. Aguarde o **bot validar** automaticamente
8. Veja o **feedback** nos comentários do PR
9. Corrija se necessário e faça novo push
10. Quando aprovado, o professor fará o merge

---

## 📂 Estrutura

```
desenvolvimento-web-2026-exercicios/
├── .github/
│   └── workflows/          # GitHub Actions
│       ├── aula01.yml
│       ├── aula02.yml
│       └── ...
├── exercicios/
│   ├── aula01/
│   │   ├── README.md       # Instruções
│   │   ├── index.html      # Seu código aqui
│   │   ├── style.css
│   │   └── .tests/         # Testes automáticos
│   ├── aula02/
│   └── ...
├── .github-bot/
│   ├── validators/         # Validadores
│   └── utils/
└── README.md
```

---

## ✅ O que o Bot Valida

### HTML
- ✅ Validação W3C (HTML válido)
- ✅ Estrutura semântica correta
- ✅ Tags obrigatórias presentes
- ✅ Atributos `alt` em imagens
- ✅ Hierarquia de headings (h1 → h2 → h3)

### CSS
- ✅ Sintaxe válida (CSS lint)
- ✅ Propriedades usadas corretamente
- ✅ Responsividade (media queries)
- ✅ Performance (não usar `!important` em excesso)

### JavaScript
- ✅ Sintaxe válida (ESLint)
- ✅ Testes unitários passam
- ✅ Sem erros no console
- ✅ Funcionalidades implementadas

### Acessibilidade
- ✅ Lighthouse score > 80
- ✅ Contraste de cores adequado
- ✅ Labels em formulários
- ✅ Navegação por teclado

### Boas Práticas
- ✅ Indentação consistente
- ✅ Nomes de variáveis descritivos
- ✅ Comentários em código complexo
- ✅ Commits com mensagens claras

---

## 🎓 Sistema de Pontuação

Cada exercício vale **100 pontos**, divididos em:

| Critério | Pontos |
|----------|--------|
| Código funciona | 40 |
| Validações passam | 30 |
| Boas práticas | 20 |
| Criatividade/UI | 10 |

**Notas:**
- 90-100: Excelente ⭐⭐⭐
- 70-89: Bom ⭐⭐
- 50-69: Regular ⭐
- < 50: Refazer ❌

---

## 📝 Exemplo de Feedback do Bot

```
🤖 Validação Automática - Aula 01

✅ HTML válido (W3C)
✅ Estrutura semântica correta
✅ 5/5 testes passaram
❌ Falta atributo alt na imagem linha 23
⚠️  Considere usar <header> ao invés de <div class="header">

📊 Score: 85/100

Sugestões:
- Adicione alt="Logo da empresa" na linha 23
- Refatore div.header para <header>
- Ótimo trabalho no CSS! 🎨

Commit para corrigir e o bot reavaliará automaticamente.
```

---

## 🚀 Começando

### 1. Fork este Repositório

Clique em **Fork** no canto superior direito.

### 2. Clone Seu Fork

```bash
git clone https://github.com/SEU-USUARIO/desenvolvimento-web-2026-exercicios.git
cd desenvolvimento-web-2026-exercicios
```

### 3. Resolva o Exercício

```bash
cd exercicios/aula01
# Edite index.html, style.css, script.js
```

### 4. Commit e Push

```bash
git add .
git commit -m "feat(aula01): implementa página inicial"
git push origin main
```

### 5. Abra Pull Request

- Vá no GitHub
- Clique em **Pull Request**
- Título: `[Aula 01] João Silva`
- Descrição: Breve explicação do que foi feito

### 6. Aguarde Validação

O bot comenta em ~30 segundos com o resultado!

---

## 🔧 Rodando Validações Localmente

Antes de fazer PR, teste localmente:

```bash
# Instalar dependências
npm install

# Validar HTML
npm run validate:html exercicios/aula01/index.html

# Validar CSS
npm run validate:css exercicios/aula01/style.css

# Rodar testes
npm test exercicios/aula01

# Validar tudo de uma vez
npm run validate:all aula01
```

---

## 📚 Exercícios Disponíveis

| Aula | Tópico | Status | Prazo |
|------|--------|--------|-------|
| 01 | Primeira Página HTML | 🟢 Aberto | 22/02 |
| 02 | Formulário de Contato | 🟢 Aberto | 01/03 |
| 03 | Página Responsiva | 🟡 Em breve | - |
| 04 | JavaScript Interativo | 🔴 Bloqueado | - |

---

## 🏆 Ranking (Top 10)

O bot mantém um ranking dos melhores alunos:

```
🥇 Maria Silva    - 98.5 pontos (4 exercícios)
🥈 João Santos    - 95.2 pontos (4 exercícios)
🥉 Ana Costa      - 92.8 pontos (3 exercícios)
4️⃣  Pedro Lima     - 90.1 pontos (4 exercícios)
5️⃣  Julia Oliveira - 88.7 pontos (3 exercícios)
```

Atualizado toda segunda-feira!

---

## ❓ FAQ

**Q: O bot reprovou meu PR. E agora?**  
A: Leia o feedback, corrija os erros, faça commit e push. O bot revalidará automaticamente.

**Q: Posso fazer múltiplos commits no mesmo PR?**  
A: Sim! O bot valida sempre o último commit.

**Q: Como vejo minha nota?**  
A: No comentário do bot no seu PR. Também será atualizada no ranking.

**Q: Posso copiar código do colega?**  
A: NÃO! O bot detecta similaridade entre códigos e reporta ao professor.

**Q: Tenho que fazer os exercícios em ordem?**  
A: Sim. Exercícios posteriores dependem de conhecimento dos anteriores.

**Q: Posso usar bibliotecas externas (Bootstrap, jQuery)?**  
A: Depende da aula. Leia as instruções no README de cada exercício.

---

## 🤝 Ajuda

**Dúvidas sobre o exercício:**  
- Abra uma **Issue** neste repositório
- Tag: `dúvida`
- Título: `[Aula XX] Sua dúvida`

**Problema com o bot:**  
- Tag: `bug`
- Descreva o erro detalhadamente

**Professor:**  
- Email: petrosbarreto01@gmail.com
- Horário de atendimento: Terças e quintas, 12:30-13:00

---

## 🔒 Regras Importantes

1. ❌ **Não copie** código de colegas
2. ❌ **Não use IA** para resolver completamente (pode usar para aprender)
3. ✅ **Pesquise** documentação (MDN, W3Schools)
4. ✅ **Pergunte** no Issues se tiver dúvida
5. ✅ **Teste** localmente antes do PR
6. ✅ **Commits claros** e descritivos
7. ✅ **Prazo** é importante (penalização por atraso)

---

## 📊 Dashboard

Veja seu progresso: [GitHub Actions](../../actions)

- ✅ Verde: Todos testes passaram
- ❌ Vermelho: Algum teste falhou
- 🟡 Amarelo: Em execução

---

## 🎨 Exemplos de Soluções

Após o prazo, o professor publicará exemplos de soluções no repositório principal:  
https://github.com/petrosbarreto/desenvolvimento-web-2026

---

## 📜 Licença

Repositório educacional - UNINASSAU 2026.1

---

**Bons estudos! 🚀**

_Dúvidas? Abra uma Issue ou mande email._
