# Exercícios Práticos: CSS Fundamentos
## Aula de 3 Horas - Do Básico ao Avançado

### 🎯 **Objetivos da Aula**
Ao final desta aula, você será capaz de:
- Compreender e aplicar a sintaxe básica do CSS
- Utilizar diferentes tipos de seletores CSS
- Organizar estilos usando CSS externo, interno e inline
- Criar layouts responsivos básicos
- Implementar componentes com Bootstrap
- Aplicar boas práticas de desenvolvimento

### 📋 **Estrutura da Aula**
- **Hora 1**: Fundamentos e Sintaxe CSS
- **Hora 2**: Seletores, Especificidade e Layout
- **Hora 3**: Bootstrap e Projeto Final

---

## 🚀 **HORA 1: FUNDAMENTOS CSS (60 minutos)**

### **Exercício 1.1: Primeira Estilização (15 min)**

**Situação**: Você recebeu um arquivo HTML simples e precisa adicionar estilos básicos.

**Tarefa**: Como desenvolvedor sênior, preciso que você estilize uma página de perfil básica. Comece aplicando estilos inline para entender a sintaxe.

**Arquivo Base (perfil.html):**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Perfil</title>
</head>
<body>
    <h1>João Silva</h1>
    <h2>Desenvolvedor Web</h2>
    <p>Apaixonado por tecnologia e sempre em busca de novos desafios.</p>
    <p>Especialista em HTML, CSS e JavaScript.</p>
</body>
</html>
```

**Instruções:**
1. Adicione cor azul (#007bff) ao título principal
2. Deixe o subtítulo em cinza (#6c757d)
3. Aumente o tamanho da fonte do título para 2.5rem
4. Centralize todo o texto
5. Adicione fundo cinza claro (#f8f9fa) na página

**💡 Exemplo de Solução:**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Perfil</title>
</head>
<body style="background-color: #f8f9fa; text-align: center; font-family: Arial, sans-serif;">
    <h1 style="color: #007bff; font-size: 2.5rem;">João Silva</h1>
    <h2 style="color: #6c757d;">Desenvolvedor Web</h2>
    <p>Apaixonado por tecnologia e sempre em busca de novos desafios.</p>
    <p>Especialista em HTML, CSS e JavaScript.</p>
</body>
</html>
```

---

### **Exercício 1.2: CSS Interno (15 min)**

**Tarefa**: Converta os estilos inline para CSS interno e adicione mais estilizações.

**Objetivo**: Refatorar o código anterior usando `<style>` no `<head>` e adicionar novos estilos.

**Instruções:**
1. Mova todos os estilos inline para uma tag `<style>`
2. Adicione padding de 2rem ao body
3. Estilize os parágrafos com:
   - Cor: #495057
   - Tamanho da fonte: 1.1rem
   - Espaçamento entre linhas: 1.6
4. Adicione uma margem inferior de 1rem nos parágrafos

**💡 Exemplo de Solução:**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Perfil</title>
    <style>
        body {
            background-color: #f8f9fa;
            text-align: center;
            font-family: Arial, sans-serif;
            padding: 2rem;
        }
        
        h1 {
            color: #007bff;
            font-size: 2.5rem;
        }
        
        h2 {
            color: #6c757d;
        }
        
        p {
            color: #495057;
            font-size: 1.1rem;
            line-height: 1.6;
            margin-bottom: 1rem;
        }
    </style>
</head>
<body>
    <h1>João Silva</h1>
    <h2>Desenvolvedor Web</h2>
    <p>Apaixonado por tecnologia e sempre em busca de novos desafios.</p>
    <p>Especialista em HTML, CSS e JavaScript.</p>
</body>
</html>
```

---

### **Exercício 1.3: CSS Externo (15 min)**

**Tarefa**: Separar estilos em arquivo externo e adicionar mais elementos.

**Situação**: O projeto está crescendo, preciso que você organize o CSS em arquivo separado e adicione uma seção de habilidades.

**Instruções:**
1. Crie um arquivo `estilos.css`
2. Mova todos os estilos para o arquivo externo
3. Adicione uma seção de habilidades com lista não ordenada
4. Estilize a lista com:
   - Remover bullets
   - Background #e9ecef em cada item
   - Padding 0.5rem
   - Border-radius 4px
   - Margem 0.5rem entre itens

**HTML Atualizado (perfil.html):**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Perfil</title>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>
    <h1>João Silva</h1>
    <h2>Desenvolvedor Web</h2>
    <p>Apaixonado por tecnologia e sempre em busca de novos desafios.</p>
    <p>Especialista em HTML, CSS e JavaScript.</p>
    
    <h3>Habilidades</h3>
    <ul>
        <li>HTML5</li>
        <li>CSS3</li>
        <li>JavaScript</li>
        <li>React</li>
    </ul>
</body>
</html>
```

**💡 Exemplo de Solução (estilos.css):**
```css
body {
    background-color: #f8f9fa;
    text-align: center;
    font-family: Arial, sans-serif;
    padding: 2rem;
    max-width: 800px;
    margin: 0 auto;
}

h1 {
    color: #007bff;
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
}

h2 {
    color: #6c757d;
    margin-bottom: 1rem;
}

h3 {
    color: #495057;
    margin-top: 2rem;
    margin-bottom: 1rem;
}

p {
    color: #495057;
    font-size: 1.1rem;
    line-height: 1.6;
    margin-bottom: 1rem;
}

ul {
    list-style: none;
    padding: 0;
    margin: 1rem 0;
}

li {
    background-color: #e9ecef;
    padding: 0.5rem;
    border-radius: 4px;
    margin: 0.5rem auto;
    max-width: 200px;
    font-weight: 500;
}
```

---

### **Exercício 1.4: Propriedades Essenciais (15 min)**

**Tarefa**: Criar um cartão de apresentação estilizado.

**Situação**: Preciso que você transforme o perfil em um cartão mais elegante usando propriedades avançadas de CSS.

**Instruções:**
1. Envolva o conteúdo em uma div com classe "cartao"
2. Aplique ao cartão:
   - Background branco
   - Border-radius: 15px
   - Box-shadow: 0 4px 15px rgba(0,0,0,0.1)
   - Padding: 2rem
   - Margem: 2rem auto
3. Adicione efeito hover no cartão (transform: translateY(-5px))
4. Crie botões de contato estilizados

**HTML Atualizado:**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Perfil</title>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>
    <div class="cartao">
        <h1>João Silva</h1>
        <h2>Desenvolvedor Web</h2>
        <p>Apaixonado por tecnologia e sempre em busca de novos desafios.</p>
        <p>Especialista em HTML, CSS e JavaScript.</p>
        
        <h3>Habilidades</h3>
        <ul class="habilidades">
            <li>HTML5</li>
            <li>CSS3</li>
            <li>JavaScript</li>
            <li>React</li>
        </ul>
        
        <div class="contatos">
            <a href="#" class="botao">Email</a>
            <a href="#" class="botao">LinkedIn</a>
        </div>
    </div>
</body>
</html>
```

**💡 Exemplo de Solução (estilos.css):**
```css
body {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    padding: 2rem;
    margin: 0;
    min-height: 100vh;
}

.cartao {
    background: white;
    border-radius: 15px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    padding: 2rem;
    margin: 2rem auto;
    max-width: 500px;
    text-align: center;
    transition: transform 0.3s ease;
}

.cartao:hover {
    transform: translateY(-5px);
}

h1 {
    color: #007bff;
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
}

h2 {
    color: #6c757d;
    margin-bottom: 1rem;
    font-weight: 300;
}

h3 {
    color: #495057;
    margin-top: 2rem;
    margin-bottom: 1rem;
}

p {
    color: #495057;
    font-size: 1.1rem;
    line-height: 1.6;
    margin-bottom: 1rem;
}

.habilidades {
    list-style: none;
    padding: 0;
    margin: 1rem 0;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 0.5rem;
}

.habilidades li {
    background: linear-gradient(45deg, #007bff, #0056b3);
    color: white;
    padding: 0.5rem 1rem;
    border-radius: 20px;
    font-size: 0.9rem;
    font-weight: 500;
}

.contatos {
    margin-top: 2rem;
}

.botao {
    background-color: #28a745;
    color: white;
    padding: 0.75rem 1.5rem;
    text-decoration: none;
    border-radius: 25px;
    margin: 0 0.5rem;
    display: inline-block;
    transition: background-color 0.3s ease;
    font-weight: 500;
}

.botao:hover {
    background-color: #218838;
    color: white;
    text-decoration: none;
}
```

---

## 🎯 **HORA 2: SELETORES E LAYOUT (60 minutos)**

### **Exercício 2.1: Seletores CSS (20 min)**

**Tarefa**: Criar uma página de blog usando diferentes tipos de seletores.

**Situação**: Você precisa estilizar uma página de blog. Use seletores específicos para cada parte.

**Arquivo Base (blog.html):**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Blog</title>
    <link rel="stylesheet" href="blog.css">
</head>
<body>
    <header id="cabecalho">
        <nav>
            <ul>
                <li><a href="#" class="ativo">Home</a></li>
                <li><a href="#">Sobre</a></li>
                <li><a href="#">Contato</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <article class="post">
            <h1>Aprendendo CSS</h1>
            <p class="meta">Publicado em <span>15 de Janeiro, 2025</span></p>
            <p>Este é o primeiro parágrafo do post sobre CSS.</p>
            <p>Este é o segundo parágrafo com mais informações.</p>
            <p class="destaque">Este parágrafo tem uma classe especial.</p>
        </article>
        
        <article class="post">
            <h1>JavaScript Básico</h1>
            <p class="meta">Publicado em <span>10 de Janeiro, 2025</span></p>
            <p>Introdução ao JavaScript para iniciantes.</p>
        </article>
    </main>
    
    <footer>
        <p>&copy; 2025 Meu Blog</p>
    </footer>
</body>
</html>
```

**Instruções - Use estes seletores específicos:**
1. **Seletor Universal (*)**: Reset básico
2. **Seletor de Elemento**: Estilizar body, h1, p
3. **Seletor de Classe (.destaque)**: Destacar parágrafos especiais
4. **Seletor de ID (#cabecalho)**: Estilizar cabeçalho
5. **Seletor Descendente (nav ul)**: Menu de navegação
6. **Seletor Filho Direto (article > h1)**: Títulos dos posts
7. **Pseudo-classes (:hover, :first-child)**: Interatividade

**💡 Exemplo de Solução (blog.css):**
```css
/* Seletor Universal - Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Seletores de Elemento */
body {
    font-family: 'Arial', sans-serif;
    line-height: 1.6;
    color: #333;
    background-color: #f4f4f4;
}

h1 {
    color: #2c3e50;
    margin-bottom: 1rem;
}

p {
    margin-bottom: 1rem;
    color: #555;
}

/* Seletor de ID */
#cabecalho {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 1rem 0;
    margin-bottom: 2rem;
}

/* Seletores Descendentes */
nav ul {
    list-style: none;
    display: flex;
    justify-content: center;
    gap: 2rem;
}

nav ul li a {
    color: white;
    text-decoration: none;
    padding: 0.5rem 1rem;
    border-radius: 4px;
    transition: background-color 0.3s;
}

/* Pseudo-classes */
nav ul li a:hover {
    background-color: rgba(255,255,255,0.2);
}

nav ul li a.ativo {
    background-color: rgba(255,255,255,0.3);
    font-weight: bold;
}

/* Seletor de Classe */
.post {
    background: white;
    margin: 2rem auto;
    padding: 2rem;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    max-width: 800px;
}

/* Seletor Filho Direto */
.post > h1 {
    border-bottom: 2px solid #007bff;
    padding-bottom: 0.5rem;
}

/* Seletores de Classe Específicos */
.meta {
    color: #666;
    font-size: 0.9rem;
    font-style: italic;
    margin-bottom: 1.5rem;
}

.meta span {
    font-weight: bold;
    color: #007bff;
}

.destaque {
    background: linear-gradient(90deg, #fff3cd, #ffeaa7);
    border-left: 4px solid #ffc107;
    padding: 1rem;
    border-radius: 4px;
    font-weight: 500;
}

/* Pseudo-classes estruturais */
.post:first-child {
    margin-top: 0;
}

.post p:first-of-type {
    font-size: 1.1rem;
    font-weight: 500;
}

/* Footer */
footer {
    text-align: center;
    padding: 2rem;
    background: #2c3e50;
    color: white;
    margin-top: 2rem;
}
```

---

### **Exercício 2.2: Especificidade CSS (20 min)**

**Tarefa**: Resolver conflitos de especificidade.

**Situação**: Você herdou um código com conflitos de CSS. Precisa corrigir sem usar !important.

**Arquivo Problemático:**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Especificidade</title>
    <style>
        /* Regras conflitantes - CORRIGIR */
        p { color: black; }
        .texto { color: blue; }
        #especial { color: red; }
        div p { color: green; }
        .container .texto { color: purple; }
        
        /* Adicione suas correções aqui */
    </style>
</head>
<body>
    <div class="container">
        <p id="especial" class="texto">
            Este texto deve ser ROXO, mas está aparecendo em outra cor!
        </p>
        <p class="texto">
            Este texto deve ser AZUL.
        </p>
        <p>
            Este texto deve ser PRETO.
        </p>
    </div>
</body>
</html>
```

**Instruções:**
1. Analise a especificidade de cada regra
2. Corrija para que os textos apareçam nas cores corretas
3. Adicione comentários explicando a especificidade
4. Crie uma tabela de especificidade

**💡 Exemplo de Solução:**
```css
/* TABELA DE ESPECIFICIDADE
   p                    = 0,0,0,1 (1 ponto)
   .texto              = 0,0,1,0 (10 pontos)
   div p               = 0,0,0,2 (2 pontos)
   .container .texto   = 0,0,2,0 (20 pontos)
   #especial           = 0,1,0,0 (100 pontos)
*/

/* Regras originais */
p { 
    color: black; 
    /* Especificidade: 1 */
}

.texto { 
    color: blue; 
    /* Especificidade: 10 */
}

div p { 
    color: green; 
    /* Especificidade: 2 - CONFLITO! Menos específico que .texto */
}

#especial { 
    color: red; 
    /* Especificidade: 100 - CONFLITO! Mais específico que .container .texto */
}

.container .texto { 
    color: purple; 
    /* Especificidade: 20 - CONFLITO! Menos específico que #especial */
}

/* CORREÇÕES - aumentando especificidade sem !important */
.container .texto {
    color: blue; /* Para textos normais com classe */
}

.container #especial.texto {
    color: purple; /* Para o texto especial - especificidade: 110 */
}

/* Ou alternativa mais limpa: */
/*
.container p.texto {
    color: blue;
}

.container p#especial {
    color: purple;
}
*/

/* Reset para garantir que div p não interfira */
.container p {
    color: inherit; /* Herda a cor do pai */
}
```

---

### **Exercício 2.3: Layout com Flexbox (20 min)**

**Tarefa**: Criar um layout responsivo com Flexbox.

**Situação**: Preciso de um layout de cartões que se adapte a diferentes tamanhos de tela.

**HTML Base:**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Flexbox</title>
    <link rel="stylesheet" href="flexbox.css">
</head>
<body>
    <header class="cabecalho">
        <h1>Nossos Serviços</h1>
    </header>
    
    <main class="container">
        <div class="cartao">
            <h3>Web Design</h3>
            <p>Criamos designs modernos e responsivos.</p>
            <button>Saiba Mais</button>
        </div>
        
        <div class="cartao">
            <h3>Desenvolvimento</h3>
            <p>Desenvolvemos aplicações web completas.</p>
            <button>Saiba Mais</button>
        </div>
        
        <div class="cartao">
            <h3>SEO</h3>
            <p>Otimizamos seu site para mecanismos de busca.</p>
            <button>Saiba Mais</button>
        </div>
        
        <div class="cartao">
            <h3>Suporte</h3>
            <p>Oferecemos suporte técnico 24/7.</p>
            <button>Saiba Mais</button>
        </div>
    </main>
</body>
</html>
```

**Instruções:**
1. Container principal deve ser flexbox
2. Cartões devem se adaptar ao espaço disponível
3. Em mobile: 1 cartão por linha
4. Em tablet: 2 cartões por linha
5. Em desktop: 4 cartões por linha
6. Cartões devem ter altura igual
7. Botões devem ficar alinhados na parte inferior

**💡 Exemplo de Solução (flexbox.css):**
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f8f9fa;
}

.cabecalho {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    text-align: center;
    padding: 2rem;
}

.cabecalho h1 {
    font-size: 2.5rem;
    font-weight: 300;
}

.container {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
    padding: 2rem;
    max-width: 1200px;
    margin: 0 auto;
}

.cartao {
    background: white;
    border-radius: 12px;
    padding: 2rem;
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    
    /* Flexbox para layout interno */
    display: flex;
    flex-direction: column;
    
    /* Responsividade */
    flex: 1 1 300px; /* grow, shrink, basis */
    min-width: 280px;
    
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.cartao:hover {
    transform: translateY(-5px);
    box-shadow: 0 6px 25px rgba(0,0,0,0.15);
}

.cartao h3 {
    color: #2c3e50;
    font-size: 1.5rem;
    margin-bottom: 1rem;
    text-align: center;
}

.cartao p {
    color: #6c757d;
    line-height: 1.6;
    flex-grow: 1; /* Expande para ocupar espaço disponível */
    margin-bottom: 1.5rem;
}

.cartao button {
    background: linear-gradient(45deg, #007bff, #0056b3);
    color: white;
    border: none;
    padding: 0.75rem 1.5rem;
    border-radius: 25px;
    font-size: 1rem;
    font-weight: 500;
    cursor: pointer;
    transition: background 0.3s ease;
    
    /* Força o botão para o final */
    margin-top: auto;
}

.cartao button:hover {
    background: linear-gradient(45deg, #0056b3, #004085);
    transform: scale(1.05);
}

/* Media Queries para Responsividade */
@media (max-width: 768px) {
    .container {
        padding: 1rem;
    }
    
    .cartao {
        flex: 1 1 100%; /* Força 1 cartão por linha */
    }
}

@media (min-width: 769px) and (max-width: 1024px) {
    .cartao {
        flex: 1 1 calc(50% - 1rem); /* 2 cartões por linha */
    }
}

@media (min-width: 1025px) {
    .cartao {
        flex: 1 1 calc(25% - 1.5rem); /* 4 cartões por linha */
    }
}
```

---

## 🎨 **HORA 3: BOOTSTRAP E PROJETO FINAL (60 minutos)**

### **Exercício 3.1: Introdução ao Bootstrap (20 min)**

**Tarefa**: Recriar a página de serviços usando Bootstrap.

**Situação**: O cliente gostou do layout, mas quer que seja mais rápido de implementar. Use Bootstrap para recriar a mesma página.

**HTML com Bootstrap:**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Serviços - Bootstrap</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="custom.css">
</head>
<body>
    <!-- Cabeçalho -->
    <header class="bg-primary text-white text-center py-5">
        <div class="container">
            <h1 class="display-4 fw-light">Nossos Serviços</h1>
            <p class="lead">Soluções completas para seu negócio digital</p>
        </div>
    </header>
    
    <!-- Grid de Cartões -->
    <main class="container my-5">
        <div class="row g-4">
            <div class="col-12 col-md-6 col-lg-3">
                <div class="card h-100 shadow-sm">
                    <div class="card-body d-flex flex-column">
                        <h5 class="card-title text-center">Web Design</h5>
                        <p class="card-text flex-grow-1">Criamos designs modernos e responsivos que impressionam seus clientes.</p>
                        <a href="#" class="btn btn-primary mt-auto">Saiba Mais</a>
                    </div>
                </div>
            </div>
            
            <div class="col-12 col-md-6 col-lg-3">
                <div class="card h-100 shadow-sm">
                    <div class="card-body d-flex flex-column">
                        <h5 class="card-title text-center">Desenvolvimento</h5>
                        <p class="card-text flex-grow-1">Desenvolvemos aplicações web completas e funcionais.</p>
                        <a href="#" class="btn btn-primary mt-auto">Saiba Mais</a>
                    </div>
                </div>
            </div>
            
            <div class="col-12 col-md-6 col-lg-3">
                <div class="card h-100 shadow-sm">
                    <div class="card-body d-flex flex-column">
                        <h5 class="card-title text-center">SEO</h5>
                        <p class="card-text flex-grow-1">Otimizamos seu site para mecanismos de busca.</p>
                        <a href="#" class="btn btn-primary mt-auto">Saiba Mais</a>
                    </div>
                </div>
            </div>
            
            <div class="col-12 col-md-6 col-lg-3">
                <div class="card h-100 shadow-sm">
                    <div class="card-body d-flex flex-column">
                        <h5 class="card-title text-center">Suporte</h5>
                        <p class="card-text flex-grow-1">Oferecemos suporte técnico 24/7 para sua tranquilidade.</p>
                        <a href="#" class="btn btn-primary mt-auto">Saiba Mais</a>
                    </div>
                </div>
            </div>
        </div>
    </main>
    
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

**CSS Customizado (custom.css):**
```css
/* Personalizações sobre o Bootstrap */
.card {
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    border: none;
    border-radius: 15px;
}

.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 6px 25px rgba(0,0,0,0.15) !important;
}

.btn-primary {
    border-radius: 25px;
    font-weight: 500;
    transition: all 0.3s ease;
}

.btn-primary:hover {
    transform: scale(1.05);
}

header {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%) !important;
}
```

**Instruções:**
1. Compare o código Bootstrap vs CSS puro
2. Note como o Bootstrap reduz o código necessário
3. Entenda as classes do sistema de grid (col-12, col-md-6, col-lg-3)
4. Veja como h-100 garante altura igual nos cartões

---

### **Exercício 3.2: Navbar Responsiva (20 min)**

**Tarefa**: Adicionar navegação responsiva com Bootstrap.

**Situação**: Preciso que você adicione uma barra de navegação que funcione bem em mobile.

**Adicione antes do header:**
```html
<!-- Navbar Bootstrap -->
<nav class="navbar navbar-expand-lg navbar-dark bg-dark sticky-top">
    <div class="container">
        <a class="navbar-brand fw-bold" href="#">MeuSite</a>
        
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
            <span class="navbar-toggler-icon"></span>
        </button>
        
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ms-auto">
                <li class="nav-item">
                    <a class="nav-link active" href="#home">Home</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#servicos">Serviços</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#sobre">Sobre</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#contato">Contato</a>
                </li>
                <li class="nav-item">
                    <a class="btn btn-outline-light ms-2" href="#orcamento">Orçamento</a>
                </li>
            </ul>
        </div>
    </div>
</nav>
```

**Instruções:**
1. Teste a responsividade redimensionando a janela
2. Veja como o menu se transforma em hamburger
3. Note o uso de classes utilitárias (ms-auto, fw-bold, etc.)

---

### **Exercício 3.3: Projeto Final - Landing Page Completa (20 min)**

**Tarefa**: Criar uma landing page completa usando tudo que aprendeu.

**Situação**: Cliente quer uma landing page moderna para sua startup. Use Bootstrap + CSS customizado.

**Estrutura Completa:**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TechStart - Inovação Digital</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        :root {
            --primary-color: #667eea;
            --secondary-color: #764ba2;
            --accent-color: #f093fb;
        }
        
        .hero-section {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
        }
        
        .hero-content {
            color: white;
            text-align: center;
        }
        
        .feature-icon {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }
        
        .card-hover {
            transition: all 0.3s ease;
        }
        
        .card-hover:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        .btn-gradient {
            background: linear-gradient(45deg, var(--primary-color), var(--accent-color));
            border: none;
            color: white;
            font-weight: 500;
            padding: 12px 30px;
            border-radius: 30px;
            transition: all 0.3s ease;
        }
        
        .btn-gradient:hover {
            transform: scale(1.05);
            color: white;
        }
        
        .section-padding {
            padding: 80px 0;
        }
        
        footer {
            background: #2c3e50;
            color: white;
        }
    </style>
</head>
<body>
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark fixed-top" style="background: rgba(44, 62, 80, 0.9);">
        <div class="container">
            <a class="navbar-brand fw-bold" href="#">
                <i class="fas fa-rocket me-2"></i>TechStart
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#home">Home</a></li>
                    <li class="nav-item"><a class="nav-link" href="#features">Features</a></li>
                    <li class="nav-item"><a class="nav-link" href="#about">Sobre</a></li>
                    <li class="nav-item"><a class="nav-link" href="#contact">Contato</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero-section">
        <div class="container">
            <div class="row">
                <div class="col-lg-8 mx-auto hero-content">
                    <h1 class="display-3 fw-bold mb-4">
                        Transforme suas ideias em <span class="text-warning">realidade digital</span>
                    </h1>
                    <p class="lead mb-5">
                        Criamos soluções inovadoras que impulsionam seu negócio para o futuro.
                        Design moderno, tecnologia avançada e resultados comprovados.
                    </p>
                    <div class="d-flex gap-3 justify-content-center flex-wrap">
                        <a href="#features" class="btn btn-gradient btn-lg">
                            <i class="fas fa-play me-2"></i>Começar Agora
                        </a>
                        <a href="#about" class="btn btn-outline-light btn-lg">
                            <i class="fas fa-info-circle me-2"></i>Saiba Mais
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="section-padding bg-light">
        <div class="container">
            <div class="row">
                <div class="col-lg-8 mx-auto text-center mb-5">
                    <h2 class="display-5 fw-bold">Por que escolher a TechStart?</h2>
                    <p class="lead text-muted">Oferecemos soluções completas e personalizadas</p>
                </div>
            </div>
            
            <div class="row g-4">
                <div class="col-md-4">
                    <div class="card border-0 text-center h-100 card-hover">
                        <div class="card-body p-4">
                            <div class="feature-icon">
                                <i class="fas fa-mobile-alt"></i>
                            </div>
                            <h4>Design Responsivo</h4>
                            <p class="text-muted">Seus projetos ficam perfeitos em qualquer dispositivo</p>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-4">
                    <div class="card border-0 text-center h-100 card-hover">
                        <div class="card-body p-4">
                            <div class="feature-icon">
                                <i class="fas fa-code"></i>
                            </div>
                            <h4>Código Limpo</h4>
                            <p class="text-muted">Desenvolvemos com as melhores práticas do mercado</p>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-4">
                    <div class="card border-0 text-center h-100 card-hover">
                        <div class="card-body p-4">
                            <div class="feature-icon">
                                <i class="fas fa-headset"></i>
                            </div>
                            <h4>Suporte 24/7</h4>
                            <p class="text-muted">Estamos sempre disponíveis para ajudar você</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section-padding">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-6">
                    <h2 class="display-5 fw-bold mb-4">Sobre a TechStart</h2>
                    <p class="lead mb-4">
                        Somos uma equipe apaixonada por tecnologia e inovação. 
                        Nossa missão é transformar ideias em soluções digitais que geram resultados reais.
                    </p>
                    <ul class="list-unstyled">
                        <li class="mb-2"><i class="fas fa-check text-success me-2"></i>5+ anos de experiência</li>
                        <li class="mb-2"><i class="fas fa-check text-success me-2"></i>100+ projetos entregues</li>
                        <li class="mb-2"><i class="fas fa-check text-success me-2"></i>98% de satisfação dos clientes</li>
                    </ul>
                </div>
                <div class="col-lg-6">
                    <div class="bg-primary rounded-3 p-5 text-white text-center">
                        <h3>Pronto para começar?</h3>
                        <p>Entre em contato e vamos conversar sobre seu projeto!</p>
                        <a href="#contact" class="btn btn-light btn-lg">Fale Conosco</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section-padding bg-light">
        <div class="container">
            <div class="row">
                <div class="col-lg-8 mx-auto text-center">
                    <h2 class="display-5 fw-bold mb-4">Entre em Contato</h2>
                    <p class="lead mb-5">Vamos transformar sua ideia em realidade</p>
                    
                    <div class="row g-4">
                        <div class="col-md-4">
                            <div class="text-center">
                                <i class="fas fa-envelope fa-2x text-primary mb-3"></i>
                                <h5>Email</h5>
                                <p>contato@techstart.com</p>
                            </div>
                        </div>
                        <div class="col-md-4">
                            <div class="text-center">
                                <i class="fas fa-phone fa-2x text-primary mb-3"></i>
                                <h5>Telefone</h5>
                                <p>(11) 99999-9999</p>
                            </div>
                        </div>
                        <div class="col-md-4">
                            <div class="text-center">
                                <i class="fas fa-map-marker-alt fa-2x text-primary mb-3"></i>
                                <h5>Endereço</h5>
                                <p>São Paulo, SP</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="text-center py-4">
        <div class="container">
            <p class="mb-0">&copy; 2025 TechStart. Todos os direitos reservados.</p>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

---

## 🏆 **DESAFIOS EXTRAS (Para quem terminar antes)**

### **Desafio 1: Animações CSS**
Adicione animações usando CSS puro:
```css
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.animate-on-scroll {
    animation: fadeInUp 0.6s ease-out;
}
```

### **Desafio 2: Dark Mode**
Implemente um tema escuro:
```css
[data-theme="dark"] {
    --bg-color: #1a1a1a;
    --text-color: #ffffff;
    --card-bg: #2d2d2d;
}
```

### **Desafio 3: Formulário Estilizado**
Crie um formulário de contato funcional com validação visual.

---

## 📚 **RESUMO DAS PRINCIPAIS APRENDIZAGENS**

### **CSS Fundamentals:**
1. **Sintaxe**: `seletor { propriedade: valor; }`
2. **Formas de aplicar**: Inline, Interno, Externo
3. **Seletores**: Elemento, Classe, ID, Descendente, etc.
4. **Especificidade**: Inline (1000) > ID (100) > Classe (10) > Elemento (1)

### **Layout e Responsividade:**
1. **Flexbox**: `display: flex` para layouts flexíveis
2. **Grid System**: Bootstrap usa 12 colunas
3. **Media Queries**: `@media (max-width: 768px) { }`
4. **Mobile First**: Comece pelo mobile, expanda para desktop

### **Bootstrap:**
1. **Grid System**: `col-12 col-md-6 col-lg-3`
2. **Componentes**: Cards, Navbar, Buttons, etc.
3. **Utilities**: `text-center`, `mb-4`, `p-3`, etc.
4. **Responsividade**: Breakpoints automáticos

### **Boas Práticas:**
1. **Organize o CSS**: Use arquivos externos
2. **Use classes**: Evite IDs para estilização
3. **Mobile First**: Pense primeiro no mobile
4. **Consistência**: Mantenha padrões no projeto
5. **Performance**: Otimize imagens e CSS

---

## ✅ **CHECKLIST DE CONCLUSÃO**

- [ ] **Exercício 1.1**: CSS Inline implementado
- [ ] **Exercício 1.2**: CSS Interno criado
- [ ] **Exercício 1.3**: CSS Externo organizado
- [ ] **Exercício 1.4**: Cartão estilizado com efeitos
- [ ] **Exercício 2.1**: Seletores CSS aplicados
- [ ] **Exercício 2.2**: Especificidade resolvida
- [ ] **Exercício 2.3**: Layout Flexbox funcional
- [ ] **Exercício 3.1**: Bootstrap implementado
- [ ] **Exercício 3.2**: Navbar responsiva
- [ ] **Exercício 3.3**: Landing page completa

### **Próximos Passos:**
1. Pratique criando suas próprias páginas
2. Explore mais componentes do Bootstrap
3. Aprenda sobre CSS Grid
4. Estude sobre acessibilidade web
5. Experimente com animações CSS

**Parabéns! 🎉 Você concluiu os fundamentos de CSS!**
