# 📐 CSS Layout: Flexbox e Grid

## 🎯 Objetivo do Módulo

Este módulo ensina as técnicas modernas de layout em CSS, focando em **Flexbox** e **CSS Grid**, que são as ferramentas mais poderosas e flexíveis para criar layouts responsivos e profissionais.

---

## 📚 Conteúdo do Módulo

### 1. **Flexbox (Flexible Box Layout)**
- Conceitos fundamentais
- Container flex vs itens flex
- Direção principal e cruzada
- Alinhamento e distribuição
- Casos práticos de uso

### 2. **CSS Grid Layout**
- Sistema de grade bidimensional
- Grid containers e grid items
- Linhas e colunas explícitas/implícitas
- Áreas nomeadas de grid
- Layout responsivo com grid

### 3. **Comparação e Quando Usar**
- Flexbox vs Grid
- Casos específicos de aplicação
- Combinando ambas as técnicas

---

## 🚀 Por Que Aprender Layout Moderno?

### ❌ Problemas dos Métodos Antigos
- **Float**: Difícil de controlar, quebra fácil
- **Position**: Complexo para layouts responsivos
- **Table-display**: Limitado e não semântico
- **Inline-block**: Problemas com espaçamentos

### ✅ Vantagens do Flexbox e Grid
- **Flexbox**: Perfeito para componentes e layouts unidimensionais
- **Grid**: Ideal para layouts bidimensionais complexos
- **Responsividade**: Nativa e intuitiva
- **Alinhamento**: Controle total vertical e horizontal
- **Manutenibilidade**: Código mais limpo e legível

---

## 📋 Flexbox - Guia Prático

### Conceitos Básicos

```css
.container {
    display: flex; /* Torna o elemento um flex container */
}
```

### Propriedades do Container (Flex Container)

| Propriedade | Valores | Descrição |
|-------------|---------|-----------|
| `flex-direction` | `row`, `column`, `row-reverse`, `column-reverse` | Define a direção principal |
| `flex-wrap` | `nowrap`, `wrap`, `wrap-reverse` | Controla quebra de linha |
| `justify-content` | `flex-start`, `center`, `space-between`, `space-around`, `space-evenly` | Alinhamento no eixo principal |
| `align-items` | `stretch`, `flex-start`, `center`, `flex-end`, `baseline` | Alinhamento no eixo cruzado |
| `align-content` | `stretch`, `flex-start`, `center`, `space-between` | Alinha linhas (múltiplas) |
| `gap` | `<length>` | Espaçamento entre itens |

### Propriedades dos Itens (Flex Items)

| Propriedade | Valores | Descrição |
|-------------|---------|-----------|
| `flex-grow` | `<number>` | Fator de crescimento |
| `flex-shrink` | `<number>` | Fator de encolhimento |
| `flex-basis` | `<length>` ou `auto` | Tamanho inicial |
| `flex` | `<grow> <shrink> <basis>` | Shorthand |
| `align-self` | Mesmo que `align-items` | Alinhamento individual |
| `order` | `<number>` | Ordem de exibição |

---

## 🎯 CSS Grid - Guia Prático

### Conceitos Básicos

```css
.container {
    display: grid; /* Torna o elemento um grid container */
}
```

### Propriedades do Container (Grid Container)

| Propriedade | Exemplo | Descrição |
|-------------|---------|-----------|
| `grid-template-columns` | `1fr 2fr 1fr` | Define colunas |
| `grid-template-rows` | `100px auto 50px` | Define linhas |
| `grid-template-areas` | `"header header" "nav main"` | Define áreas nomeadas |
| `gap` / `grid-gap` | `20px` ou `10px 20px` | Espaçamento entre células |
| `justify-items` | `start`, `center`, `end`, `stretch` | Alinhamento horizontal dos itens |
| `align-items` | `start`, `center`, `end`, `stretch` | Alinhamento vertical dos itens |
| `justify-content` | `start`, `center`, `space-between` | Alinhamento do grid no container |
| `align-content` | `start`, `center`, `space-around` | Alinhamento vertical do grid |

### Propriedades dos Itens (Grid Items)

| Propriedade | Exemplo | Descrição |
|-------------|---------|-----------|
| `grid-column` | `1 / 3` ou `span 2` | Posição nas colunas |
| `grid-row` | `2 / 4` | Posição nas linhas |
| `grid-area` | `header` ou `1 / 1 / 2 / 4` | Área ocupada |
| `justify-self` | `center` | Alinhamento horizontal individual |
| `align-self` | `end` | Alinhamento vertical individual |

---

## 💡 Exemplos Práticos

### 🔥 Layout de Header com Flexbox

```html
<header class="header">
    <div class="logo">Logo</div>
    <nav class="nav">
        <a href="#">Home</a>
        <a href="#">Sobre</a>
        <a href="#">Contato</a>
    </nav>
    <div class="actions">
        <button>Login</button>
    </div>
</header>
```

```css
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
    background: #fff;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.nav {
    display: flex;
    gap: 2rem;
}

.nav a {
    text-decoration: none;
    color: #333;
    font-weight: 500;
}
```

### 🏠 Layout de Página Completo com Grid

```html
<div class="page-layout">
    <header class="header">Header</header>
    <nav class="sidebar">Sidebar</nav>
    <main class="main">Conteúdo Principal</main>
    <aside class="aside">Aside</aside>
    <footer class="footer">Footer</footer>
</div>
```

```css
.page-layout {
    display: grid;
    grid-template-columns: 250px 1fr 200px;
    grid-template-rows: auto 1fr auto;
    grid-template-areas:
        "header header header"
        "sidebar main aside"
        "footer footer footer";
    min-height: 100vh;
    gap: 1rem;
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main { grid-area: main; }
.aside { grid-area: aside; }
.footer { grid-area: footer; }

/* Responsivo */
@media (max-width: 768px) {
    .page-layout {
        grid-template-columns: 1fr;
        grid-template-areas:
            "header"
            "main"
            "sidebar"
            "aside"
            "footer";
    }
}
```

---

## 🎮 Exercícios Práticos

### 🏆 Nível Iniciante
1. **Barra de Navegação**: Criar uma navbar horizontal com logo à esquerda e links à direita
2. **Card Layout**: Três cards em linha que se ajustam automaticamente
3. **Centralização**: Centralizar um elemento vertical e horizontalmente

### 🏆 Nível Intermediário
1. **Layout Holy Grail**: Header, footer, sidebar e conteúdo principal
2. **Grid de Produtos**: Layout responsivo de produtos (2, 3, 4 colunas)
3. **Dashboard**: Layout de dashboard com diferentes seções

### 🏆 Nível Avançado
1. **Layout Revista**: Layout complexo tipo revista/jornal
2. **Componente Card Avançado**: Card com múltiplas seções e responsividade
3. **Layout Masonry**: Estilo Pinterest com alturas diferentes

---

## 📱 Design Responsivo

### Mobile-First com Flexbox

```css
/* Mobile primeiro */
.container {
    display: flex;
    flex-direction: column;
    gap: 1rem;
}

/* Tablet */
@media (min-width: 768px) {
    .container {
        flex-direction: row;
        flex-wrap: wrap;
    }
}

/* Desktop */
@media (min-width: 1024px) {
    .container {
        flex-wrap: nowrap;
    }
}
```

### Mobile-First com Grid

```css
/* Mobile primeiro */
.grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 1rem;
}

/* Tablet */
@media (min-width: 768px) {
    .grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

/* Desktop */
@media (min-width: 1024px) {
    .grid {
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    }
}
```

---

## 🔧 Ferramentas e Recursos

### 🎯 Ferramentas Online
- **Flexbox Froggy**: Jogo para aprender Flexbox
- **Grid Garden**: Jogo para aprender CSS Grid
- **Flexbox Defense**: Tower defense com Flexbox
- **CSS Grid Generator**: Gerador visual de grid

### 📚 Recursos de Estudo
- **MDN Web Docs**: Documentação completa
- **CSS-Tricks**: Guias detalhados
- **Flexbox Cheatsheet**: Referência rápida
- **Grid Cheatsheet**: Referência rápida

### 🔍 DevTools
- **Firefox Grid Inspector**: Visualizador de grid
- **Chrome Flexbox Inspector**: Inspetor de flexbox
- **Layout debugging**: Ferramentas de depuração

---

## ✅ Checklist de Aprendizado

### Flexbox
- [ ] Entender a diferença entre container e itens
- [ ] Dominar `justify-content` e `align-items`
- [ ] Saber usar `flex-grow`, `flex-shrink`, `flex-basis`
- [ ] Criar layouts responsivos com flexbox
- [ ] Resolver problemas comuns de alinhamento

### CSS Grid
- [ ] Definir colunas e linhas
- [ ] Usar `grid-template-areas` para layouts nomeados
- [ ] Posicionar itens com `grid-column` e `grid-row`
- [ ] Criar layouts responsivos com `auto-fit` e `minmax`
- [ ] Combinar grid com flexbox quando necessário

### Geral
- [ ] Escolher entre flexbox e grid para cada situação
- [ ] Implementar design mobile-first
- [ ] Debuggar layouts com DevTools
- [ ] Criar componentes reutilizáveis
- [ ] Otimizar performance dos layouts

---

## 🎯 Próximos Passos

Após dominar este módulo, você estará pronto para:

1. **06-css-avancado**: Animações, transformações e efeitos avançados
2. **07-javascript-basico**: Adicionar interatividade aos layouts
3. **09-frameworks-bootstrap**: Usar frameworks baseados nestes conceitos

---

## 💡 Dicas Importantes

### ✅ Boas Práticas
- Use **flexbox para componentes** (navbar, cards, botões)
- Use **grid para layouts de página** (estrutura geral)
- Sempre pense **mobile-first**
- Use **semantic HTML** com CSS moderno
- **Teste em múltiplos dispositivos**

### ❌ Evite
- Usar flexbox para layouts bidimensionais complexos
- Usar grid para alinhamento simples de componentes
- Misturar float com flexbox/grid desnecessariamente
- Esquecer de testar responsividade
- Usar valores fixos sem considerar diferentes telas

---

🚀 **Lembre-se**: Flexbox e Grid são as bases do CSS moderno. Dominar essas técnicas vai transformar sua capacidade de criar layouts profissionais e responsivos!