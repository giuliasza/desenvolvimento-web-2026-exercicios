# 📝 Exercício Prático - Aula 03

## 🎯 Objetivo

Criar um **sistema de envio de emails** simulado usando conceitos da Aula 3:
- Formulário completo
- Validação de campos
- Preview do email
- Simulação de envio (sem backend real)
- Histórico de emails enviados (localStorage)

---

## 📋 Descrição

Construa uma aplicação de "Email Client" que permite:

### 1. Formulário de Email
- **De:** Email do remetente (validação)
- **Para:** Email(s) destinatário (múltiplos, separados por vírgula)
- **Cc:** Cópia (opcional)
- **Bcc:** Cópia oculta (opcional)
- **Assunto:** Título do email
- **Corpo:** Texto do email (textarea)
- **Prioridade:** Normal, Alta, Baixa (select)

### 2. Preview em Tempo Real
- Mostrar como o email ficará
- Formatar como um email real
- Atualizar conforme usuário digita

### 3. Simulação de Envio
- Validar todos campos
- Simular delay (2 segundos)
- Mostrar "Enviando..."
- Confirmar sucesso

### 4. Histórico
- Salvar emails no localStorage
- Listar últimos 10 emails enviados
- Botão para reenviar
- Botão para deletar

---

## ✅ Requisitos Obrigatórios

### HTML
- [x] Formulário completo com todos campos
- [x] Labels associados aos inputs
- [x] Área de preview
- [x] Lista de histórico
- [x] Botões: Enviar, Limpar, Deletar

### JavaScript
- [x] Validação de email (regex)
- [x] Validação de múltiplos emails
- [x] Preview em tempo real
- [x] localStorage (save/load)
- [x] Simulação de envio assíncrona
- [x] Manipulação DOM (criar elementos)

### CSS
- [x] Layout email-like
- [x] Indicador de prioridade (cores)
- [x] Loading spinner
- [x] Histórico estilizado
- [x] Responsivo

---

## 🎨 Estrutura

```
exercicios/aula03/
├── index.html
├── style.css
├── script.js
└── README.md
```

---

## 💻 Template Inicial

### Funções Principais

```javascript
// Validar email
function validarEmail(email) {
  const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  return regex.test(email);
}

// Validar múltiplos emails
function validarMultiplosEmails(emails) {
  const lista = emails.split(',').map(e => e.trim());
  return lista.every(validarEmail);
}

// Salvar no localStorage
function salvarEmail(emailData) {
  let historico = JSON.parse(localStorage.getItem('emailHistory') || '[]');
  historico.unshift(emailData);
  historico = historico.slice(0, 10); // Máximo 10
  localStorage.setItem('emailHistory', JSON.stringify(historico));
}

// Simular envio
async function enviarEmail(emailData) {
  return new Promise(resolve => {
    setTimeout(() => {
      resolve({ success: true, messageId: Date.now() });
    }, 2000);
  });
}

// Preview em tempo real
function atualizarPreview() {
  // Pegar valores do form
  // Atualizar div preview
}
```

---

## 🤖 Validações Automáticas

### Funcionalidade (50 pontos)
- ✅ Formulário envia corretamente
- ✅ Validação de emails funciona
- ✅ Preview atualiza em tempo real
- ✅ localStorage salva/carrega
- ✅ Histórico exibe corretamente
- ✅ Simulação de envio funciona

### Código (30 pontos)
- ✅ Funções bem organizadas
- ✅ Validação de email correta (regex)
- ✅ Async/await usado
- ✅ Sem erros no console
- ✅ Código comentado

### UI/UX (20 pontos)
- ✅ Layout profissional
- ✅ Feedback visual (loading)
- ✅ Responsivo
- ✅ Acessível (labels, aria)

---

## 🎯 Bônus

- ✨ Anexar arquivos (simulado) (+10pts)
- ✨ Rich text editor (bold, italic) (+10pts)
- ✨ Templates de email (+10pts)
- ✨ Busca no histórico (+5pts)
- ✨ Exportar histórico (JSON) (+5pts)

---

## ⏰ Prazo

**Data limite:** 08/03/2026 23:59

---

## 📚 Recursos

- [MDN - localStorage](https://developer.mozilla.org/pt-BR/docs/Web/API/Window/localStorage)
- [Regex Email](https://regexr.com/)
- [Slides da Aula 3](../../slides/aula03/)

---

## 📤 Entrega

```bash
git add exercicios/aula03/
git commit -m "feat(aula03): sistema de envio de emails"
git push
```

PR: `[Aula 03] Seu Nome`

---

**Bom trabalho! 📧🚀**
