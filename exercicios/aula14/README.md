# 📝 Exercício Prático - Aula 14

## 🎯 Objetivo

Criar: **Dashboard de Dados**

Aplicando os conceitos de:
- map
- filter
- reduce
- forEach
- find/findIndex

---

## 📋 Descrição Detalhada

Neste exercício você vai desenvolver um projeto completo que demonstra seu domínio dos conceitos de arrays e métodos.

### Requisitos Funcionais

1. **Funcionalidade Principal**
   - Implementar todas as features solicitadas
   - Interface intuitiva e responsiva
   - Feedback visual para ações do usuário

2. **Validações**
   - Tratar erros adequadamente
   - Validar entradas do usuário
   - Exibir mensagens claras

3. **Performance**
   - Código otimizado
   - Carregamento rápido
   - Sem travamentos

---

## ✅ Requisitos Obrigatórios

### Estrutura de Arquivos
- [x] `index.html` - Estrutura HTML semântica
- [x] `style.css` - Estilos customizados
- [x] `script.js` - Lógica JavaScript
- [x] `README.md` - Documentação do projeto

### HTML
- [x] Estrutura semântica (header, main, section, footer)
- [x] Formulários com labels corretas
- [x] Elementos interativos acessíveis
- [x] Meta tags apropriadas

### CSS
- [x] Layout responsivo (mobile-first)
- [x] Variáveis CSS para cores/fontes
- [x] Transitions/animations suaves
- [x] Sem código duplicado

### JavaScript
- [x] Código organizado em funções
- [x] Comentários explicativos
- [x] Tratamento de erros (try/catch)
- [x] Sem `console.log` no código final
- [x] Uso de const/let (não var)

### Funcionalidades Específicas
- [x] map
- [x] filter
- [x] reduce
- [x] forEach
- [x] find/findIndex

---

## 🎨 Layout Sugerido

```
┌─────────────────────────────┐
│        HEADER/TÍTULO        │
├─────────────────────────────┤
│                             │
│      ÁREA PRINCIPAL         │
│      (funcionalidade)       │
│                             │
├─────────────────────────────┤
│          CONTROLES          │
├─────────────────────────────┤
│          RESULTADOS         │
└─────────────────────────────┘
```

---

## 💻 Template Inicial

### index.html
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Aula 14 - Dashboard de Dados</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Dashboard de Dados</h1>
    <p>Aula 14 - Arrays e Métodos</p>
  </header>

  <main>
    <!-- TODO: Implementar sua solução aqui -->
  </main>

  <footer>
    <p>&copy; 2026 - Desenvolvimento Web</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
```

### style.css (base)
```css
:root {
  --primary-color: #667eea;
  --secondary-color: #764ba2;
  --text-color: #333;
  --bg-color: #f5f5f5;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  line-height: 1.6;
  color: var(--text-color);
  background-color: var(--bg-color);
}

header {
  background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
  color: white;
  padding: 2rem;
  text-align: center;
}

main {
  max-width: 1200px;
  margin: 2rem auto;
  padding: 0 1rem;
}

/* TODO: Adicione seus estilos aqui */
```

### script.js (template)
```javascript
'use strict';

// TODO: Implemente sua solução aqui

document.addEventListener('DOMContentLoaded', () => {
  console.log('App iniciado - Aula 14');
  
  // Seu código aqui
});
```

---

## 🤖 Validações Automáticas

O bot vai verificar:

### Estrutura (20 pontos)
- ✅ Arquivos obrigatórios presentes
- ✅ HTML válido (sem erros)
- ✅ CSS externo linkado
- ✅ JavaScript externo linkado

### Código (40 pontos)
- ✅ JavaScript funcional (sem erros no console)
- ✅ Uso de const/let (não var)
- ✅ Funções bem nomeadas
- ✅ Tratamento de erros implementado
- ✅ Código comentado adequadamente

### Funcionalidade (30 pontos)
- ✅ Todas as features implementadas
- ✅ Interface responsiva
- ✅ Interatividade funcionando
- ✅ Validações presentes

### Boas Práticas (10 pontos)
- ✅ Código organizado e limpo
- ✅ Nomenclatura consistente
- ✅ Sem código duplicado
- ✅ Performance adequada

---

## 💡 Dicas de Implementação

### 1. Planeje Antes de Codificar
- Faça um esboço da interface
- Liste as funcionalidades necessárias
- Divida em tarefas menores

### 2. Desenvolva Incrementalmente
- Comece pelo HTML básico
- Adicione CSS aos poucos
- Implemente JavaScript por feature

### 3. Teste Frequentemente
- Abra no navegador a cada mudança
- Use DevTools Console (F12)
- Teste em diferentes tamanhos de tela

### 4. Commit Regularmente
```bash
git add .
git commit -m "feat: implementar [funcionalidade]"
git push
```

---

## 🎯 Critérios de Avaliação

| Critério | Peso | Descrição |
|----------|------|-----------|
| Funcionalidade | 40% | Todas as features funcionando |
| Código | 30% | Organização e boas práticas |
| UI/UX | 20% | Design e usabilidade |
| Criatividade | 10% | Soluções inovadoras |

**Nota mínima para aprovação:** 70/100

---

## 🚀 Desafios Bônus

Ganhe pontos extras implementando:

- ✨ Persistência de dados (localStorage) (+10pts)
- ✨ Animações CSS avançadas (+5pts)
- ✨ Acessibilidade (ARIA labels) (+5pts)
- ✨ Dark mode (+5pts)
- ✨ PWA (Service Worker) (+15pts)
- ✨ Testes automatizados (+10pts)

---

## ⏰ Prazo de Entrega

**Data limite:** [A ser definido pelo professor]

**Penalidades por atraso:**
- Até 1 dia: -10%
- Até 3 dias: -20%
- Acima de 3 dias: não aceito

---

## 📚 Recursos de Apoio

### Documentação
- [MDN Web Docs](https://developer.mozilla.org/pt-BR/)
- [JavaScript.info](https://javascript.info/)

### Tutoriais
- [W3Schools](https://www.w3schools.com/)
- [freeCodeCamp](https://www.freecodecamp.org/)

### Ferramentas
- [CodePen](https://codepen.io/) - Testar código rapidamente
- [Can I Use](https://caniuse.com/) - Compatibilidade de browsers
- [JSHint](https://jshint.com/) - Validar JavaScript

---

## 📤 Como Entregar

### 1. Certifique-se que tudo está funcionando
```bash
# Teste local primeiro!
open index.html  # ou clique duas vezes no arquivo
```

### 2. Commit e Push
```bash
cd exercicios/aula14/
git add .
git commit -m "feat(aula14): dashboard de dados"
git push origin main
```

### 3. Abrir Pull Request
- Vá no GitHub
- Clique em "New Pull Request"
- Título: `[Aula 14] Seu Nome Completo`
- Descrição: Explique brevemente o que fez
- Clique em "Create Pull Request"

### 4. Aguardar Validação
- Bot comenta em ~30 segundos
- Veja seu score (0-100)
- Corrija se necessário e faça novo push

---

## ❓ Dúvidas Frequentes

**P: Posso usar bibliotecas externas?**
R: Só se a aula permitir. Priorize JavaScript puro.

**P: E se eu travar?**
R: Abra uma Issue no GitHub ou pergunte no grupo.

**P: Posso colaborar com colegas?**
R: Podem discutir, mas código deve ser individual.

**P: Como sei se passei?**
R: Score ≥ 70 = aprovado. Bot informa automaticamente.

---

## 🏆 Ranking

Seu desempenho aparece no **[Leaderboard](../../leaderboard.html)**!

Competição saudável motiva aprendizado 🚀

---

**Bom trabalho e bons estudos! 💪🤖**

_Qualquer dúvida, entre em contato com o professor._
