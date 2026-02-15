# 📝 Exercício Prático - Aula 04

## 🎯 Objetivo

Criar um **Portfólio Pessoal** completo aplicando CSS fundamental:
- Seletores (tag, classe, id)
- Cores e tipografia
- Box model (margin, padding)
- Layout básico
- CSS externo

---

## 📋 Descrição

Construa uma página de portfólio com:

### 1. Header
- Seu nome em destaque
- Subtítulo (profissão ou cargo)
- Navegação com links (Sobre, Projetos, Contato)
- Fundo colorido ou gradiente

### 2. Seção "Sobre Mim"
- Foto de perfil (pode ser placeholder)
- Parágrafo descritivo
- Lista de habilidades/tecnologias
- Fundo diferente da página

### 3. Seção "Projetos"
- Mínimo 3 projetos
- Cada projeto em um card
- Título, descrição breve, link
- Cards organizados (pode ser lista vertical)

### 4. Rodapé
- Links de contato (email, GitHub, LinkedIn)
- Copyright com seu nome
- Fundo escuro

---

## ✅ Requisitos Obrigatórios

### HTML
- [x] Estrutura semântica (`<header>`, `<main>`, `<section>`, `<footer>`)
- [x] Pelo menos 1 `id` usado
- [x] Pelo menos 3 classes usadas
- [x] Imagem de perfil (pode ser via URL)
- [x] Lista de habilidades
- [x] 3+ projetos

### CSS
- [x] Arquivo externo (`style.css`)
- [x] Seletor de tag usado
- [x] Seletor de classe usado
- [x] Seletor de id usado
- [x] Cores definidas (texto e fundo)
- [x] Fonte customizada (font-family)
- [x] Margin e padding aplicados
- [x] text-align usado

### Design
- [x] Header visualmente destacado
- [x] Seções bem separadas
- [x] Hierarquia visual clara
- [x] Cores harmoniosas (não mais que 4 cores)
- [x] Legível (contraste adequado)

---

## 🎨 Estrutura

```
exercicios/aula04/
├── index.html
├── style.css
└── README.md
```

---

## 💻 Template Base

### index.html
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portfólio - Seu Nome</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header id="topo">
    <h1>Seu Nome</h1>
    <p class="subtitulo">Desenvolvedor Web</p>
    <nav>
      <a href="#sobre">Sobre</a>
      <a href="#projetos">Projetos</a>
      <a href="#contato">Contato</a>
    </nav>
  </header>

  <main>
    <section id="sobre" class="secao">
      <h2>Sobre Mim</h2>
      <img src="https://via.placeholder.com/150" alt="Foto de perfil" class="foto-perfil">
      <p>Escreva sobre você aqui...</p>
      
      <h3>Habilidades</h3>
      <ul class="habilidades">
        <li>HTML5</li>
        <li>CSS3</li>
        <li>JavaScript</li>
      </ul>
    </section>

    <section id="projetos" class="secao">
      <h2>Meus Projetos</h2>
      
      <div class="projeto">
        <h3>Projeto 1</h3>
        <p>Descrição do projeto...</p>
        <a href="#">Ver mais</a>
      </div>
      
      <!-- Adicione mais 2 projetos -->
    </section>
  </main>

  <footer id="contato">
    <p>Entre em contato:</p>
    <a href="mailto:seu@email.com">Email</a>
    <a href="#">GitHub</a>
    <a href="#">LinkedIn</a>
    <p>&copy; 2026 Seu Nome</p>
  </footer>
</body>
</html>
```

### style.css (template)
```css
/* Reset básico */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  color: #333;
}

/* Header */
#topo {
  /* TODO: Adicionar estilos */
  background-color: #4CAF50;
  color: white;
  padding: 40px 20px;
  text-align: center;
}

/* Navegação */
nav a {
  /* TODO: Estilizar links */
}

/* Seções */
.secao {
  /* TODO: Espaçamento e layout */
}

/* Foto de perfil */
.foto-perfil {
  /* TODO: Estilizar imagem */
}

/* Habilidades */
.habilidades {
  /* TODO: Estilizar lista */
}

/* Projetos */
.projeto {
  /* TODO: Estilizar cards */
}

/* Rodapé */
footer {
  /* TODO: Estilizar footer */
}
```

---

## 🤖 Validações Automáticas

### Estrutura (20 pontos)
- ✅ HTML válido
- ✅ CSS externo linkado
- ✅ Tags semânticas usadas
- ✅ Estrutura completa (header, main, footer)

### Seletores CSS (30 pontos)
- ✅ Seletor de tag usado
- ✅ Seletor de classe usado (`.class`)
- ✅ Seletor de id usado (`#id`)
- ✅ Mínimo 5 regras CSS

### Propriedades (30 pontos)
- ✅ `color` usado
- ✅ `background-color` usado
- ✅ `font-family` usado
- ✅ `margin` ou `padding` usado
- ✅ `text-align` usado

### Design (20 pontos)
- ✅ Imagem presente
- ✅ Lista de habilidades
- ✅ 3+ projetos
- ✅ Links funcionais

---

## 💡 Dicas

### Paleta de Cores
```css
/* Exemplo de paleta harmoniosa */
:root {
  --primary: #4CAF50;
  --secondary: #2196F3;
  --dark: #333;
  --light: #f4f4f4;
}
```

### Espaçamento
```css
.secao {
  padding: 60px 20px;
  max-width: 1000px;
  margin: 0 auto;
}
```

### Estilizar Links
```css
nav a {
  color: white;
  text-decoration: none;
  margin: 0 15px;
  font-weight: bold;
}

nav a:hover {
  text-decoration: underline;
}
```

---

## 🎯 Bônus (Opcional)

- ✨ Gradiente no header (+5pts)
- ✨ Efeito hover nos projetos (+5pts)
- ✨ Foto de perfil redonda (+5pts)
- ✨ Ícones nos links (+5pts)
- ✨ Sombra em elementos (+5pts)

**Exemplos:**
```css
/* Gradiente */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* Hover */
.projeto:hover {
  transform: scale(1.05);
  transition: 0.3s;
}

/* Foto redonda */
.foto-perfil {
  border-radius: 50%;
}
```

---

## ⏰ Prazo

**Data limite:** 15/03/2026 23:59

---

## 📚 Recursos

- [MDN - CSS Basics](https://developer.mozilla.org/pt-BR/docs/Learn/CSS/First_steps)
- [CSS Colors](https://www.w3schools.com/colors/)
- [Google Fonts](https://fonts.google.com/)
- [Coolors](https://coolors.co/) - Paletas de cores

---

## 📤 Entrega

```bash
git add exercicios/aula04/
git commit -m "feat(aula04): portfólio pessoal com CSS"
git push
```

PR: `[Aula 04] Seu Nome`

---

**Capriche no design! 🎨✨**
