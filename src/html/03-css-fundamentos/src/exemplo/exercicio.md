# Exercício de fixação - HTML + CSS básico


O exercício  prático abaixo tem como objetivo práticar o que foi visto em sala de aula focando no aprendizado continuo. Apesar de permitir copiar e colar, é interessante realizar a prática de escrita linha a linha com objetivo de enteder os pontos principais, questionar o que está sendo escrito e aumentar a curiosidade sobre o código escrito.

## Exemplo de Página HTML + CSS

Abaixo está o código base para os alunos utilizarem nos exercícios. Crie a página com o nome de index.html:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <!-- Define a codificação de caracteres como UTF-8 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Faz com que a página seja responsiva em dispositivos móveis -->
    <title>Página de Apresentação</title>
    <style>
        /* === ESTILO GLOBAL === */
        body {
            font-family: Arial, Helvetica, sans-serif; /* Define a fonte da página */
            background-color: #f0f0f0; /* Cor de fundo da página */
            margin: 0; /* Remove margens padrão do navegador */
            padding: 0; /* Remove padding padrão */
            color: #333; /* Cor padrão do texto */
            line-height: 1.6; /* Espaçamento entre linhas para melhor leitura */
        }

        /* === CABEÇALHO === */
        header {
            background-color: #3366cc; /* Cor de fundo do cabeçalho */
            color: white; /* Cor do texto no cabeçalho */
            padding: 2rem; /* Espaçamento interno do cabeçalho */
            text-align: center; /* Centraliza o conteúdo */
        }

        header h1 {
            margin: 0; /* Remove a margem padrão do título */
            font-size: 2rem; /* Define tamanho da fonte do título */
        }

        /* === CONTAINER PRINCIPAL === */
        .container {
            max-width: 900px; /* Largura máxima da área do conteúdo */
            margin: 0 auto; /* Centraliza horizontalmente */
            padding: 1.5rem; /* Espaçamento interno */
        }

        /* === SEÇÕES === */
        section {
            background-color: white; /* Fundo branco para cada seção */
            padding: 1.5rem; /* Espaçamento interno das seções */
            margin-bottom: 1.5rem; /* Espaço entre as seções */
            border-radius: 5px; /* Bordas arredondadas */
            border: 1px solid #ddd; /* Borda leve para destaque */
            text-align: center; /* Centraliza o conteúdo dentro da seção */
        }

        /* === TÍTULOS DAS SEÇÕES === */
        h2 {
            color: #3366cc; /* Cor azul para títulos */
        }

        /* === LISTAS ESTILIZADAS === */
        ul {
            padding-left: 1.2rem; /* Espaço à esquerda da lista */
        }

        ul li {
            background-color: #f9f9f9; /* Fundo claro para cada item */
            border-left: 4px solid #3366cc; /* Barra colorida à esquerda */
            padding: 0.5rem; /* Espaçamento interno do item */
            margin-bottom: 0.5rem; /* Espaço entre os itens */
            border-radius: 3px; /* Bordas levemente arredondadas */
        }

        /* === ANIMAÇÃO DE ENTRADA PARA AS SEÇÕES === */
        .fade-in {
            opacity: 0; /* Inicia invisível */
            animation: aparecer 1.5s ease-out forwards; /* Define a animação de entrada */
        }

        /* Define atrasos diferentes para cada seção, criando efeito em sequência */
        section.fade-in:nth-of-type(1) { animation-delay: 0.1s; }
        section.fade-in:nth-of-type(2) { animation-delay: 0.3s; }
        section.fade-in:nth-of-type(3) { animation-delay: 0.6s; }
        section.fade-in:nth-of-type(4) { animation-delay: 0.8s; }

        /* === DEFINIÇÃO DA ANIMAÇÃO === */
        @keyframes aparecer {
            from { opacity: 0; transform: translateY(20px); } /* Começa invisível e levemente deslocado para baixo */
            to   { opacity: 1; transform: translateY(0); }     /* Termina totalmente visível na posição original */
        }

        /* === ESTILO DO AVATAR === */
        .avatar {
            width: 150px; /* Largura da imagem */
            height: 150px; /* Altura da imagem */
            border-radius: 50%; /* Torna a imagem redonda */
            object-fit: cover;  /* Mantém a proporção da imagem sem distorcer */
            border: 4px solid #3366cc; /* Borda azul ao redor da imagem */
        }

        /* === RODAPÉ === */
        footer {
            text-align: center; /* Centraliza o conteúdo do rodapé */
            padding: 1rem; /* Espaçamento interno */
            background-color: #eee; /* Fundo cinza claro */
            color: #666; /* Cor do texto mais clara */
            font-size: 0.9rem; /* Tamanho menor da fonte */
        }

        /* === BOTÃO (usado no contato) === */
        .botao {
            display: inline-block; /* Permite definir tamanho e espaçamento */
            background-color: #3366cc; /* Cor de fundo */
            color: white; /* Cor do texto */
            padding: 0.7rem 1.2rem; /* Espaçamento interno do botão */
            border: none; /* Sem borda */
            border-radius: 4px; /* Bordas arredondadas */
            text-decoration: none; /* Remove sublinhado do link */
            transition: background-color 0.3s; /* Efeito suave ao passar o mouse */
        }

        .botao:hover {
            background-color: #264d99; /* Muda a cor quando o mouse passa por cima */
        }

    </style>
</head>
<body>
    <!-- CABEÇALHO -->
    <header>
        <h1>Minha Página</h1>
        <p>Uma apresentação simples com CSS básico</p>
    </header>

    <!-- CONTAINER PRINCIPAL -->
    <div class="container">

        <!-- SEÇÃO DO AVATAR -->
        <section class="fade-in">
            <h2>👤 Meu Avatar</h2>
            <!-- Alunos devem colocar a imagem avatar.jpg na mesma pasta -->
            <img src="avatar.jpg" alt="Meu Avatar" class="avatar">
            <p>Este é meu avatar escolhido para me representar na apresentação.</p>
        </section>

        <!-- SEÇÃO SOBRE MIM -->
        <section class="fade-in">
            <h2>Sobre Mim</h2>
            <p>Olá! Sou um entusiasta de tecnologia e gosto de aprender novas ferramentas de programação e design. 
               Esta página é um exemplo simples de HTML + CSS básico.</p>
        </section>

        <!-- SEÇÃO DE HABILIDADES -->
        <section class="fade-in">
            <h2>Habilidades</h2>
            <ul>
                <li>HTML e CSS</li>
                <li>JavaScript Básico</li>
                <li>Python e Análise de Dados</li>
                <li>Banco de Dados SQL</li>
            </ul>
        </section>

        <!-- SEÇÃO DE CONTATO -->
        <section class="fade-in">
            <h2>Contato</h2>
            <p>Se quiser entrar em contato, clique no botão abaixo:</p>
            <a href="mailto:meuemail@exemplo.com" class="botao">Enviar E-mail</a>
        </section>
    </div>
    
    <!-- RODAPÉ -->
    <footer>
        <p>© 2025 - Minha Página Pessoal</p>
    </footer>
</body>
</html>

```

---

## Exercícios de HTML e CSS – Página de Apresentação

Agora que você já tem o código base da página de apresentação, faça os seguintes exercícios utilizando apenas os conceitos e classes que já aprendemos:

---

### **Exercício 1 – Adicionando uma nova seção com atraso**

No código base, cada `<section>` possui uma animação de entrada com atraso (`fade-in`).

1. Dentro da `<div class="container">`, crie **uma nova seção** com informações que você quiser (por exemplo: “Meus hobbies”, “Meus interesses”, etc).
2. Use a **classe `fade-in`** para que a seção apareça com animação.
3. Defina um **atraso (`animation-delay`) maior que todas as seções anteriores**, para que ela apareça por último.

**Dica:** Siga o padrão já existente no CSS:

```css
section.fade-in:nth-of-type(5) { animation-delay: 1s; } /* Exemplo para a 5ª seção */
```

---

### **Exercício 2 – Criando a página de Projetos**

Vamos criar uma nova página que apresenta seus projetos. Essa página deve **reutilizar os estilos da página principal**.

**Passo 1:** No arquivo `index.html`, adicione este bloco **antes do rodapé (`footer`)**:

```html
<section class="fade-in">
    <h2>Projetos</h2>
    <p>Clique abaixo para conhecer alguns projetos que já realizei.</p>
    <a href="projeto.html" class="botao">Ver Projetos</a>
</section>
```

**Passo 2:** Crie um novo arquivo chamado `projeto.html` e adicione o código abaixo. O texto pode ser alterado para refletir seus próprios projetos:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meus Projetos</title>
    <!-- Link para o CSS já usado na página principal -->
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Projetos Realizados</h1>
        <p>Alguns trabalhos que desenvolvi para praticar programação e design</p>
    </header>

    <div class="container">
        <section class="fade-in">
            <h2>Projeto 1</h2>
            <p>Criação de uma página de apresentação com HTML e CSS, focando em estrutura e estilo.</p>
        </section>

        <section class="fade-in">
            <h2>Projeto 2</h2>
            <p>Pequeno sistema de lista de tarefas utilizando HTML, CSS e JavaScript.</p>
        </section>

        <section class="fade-in">
            <h2>Projeto 3</h2>
            <p>Página de portfólio responsiva, adaptando o layout para diferentes tamanhos de tela.</p>
        </section>
    </div>

    <section class="fade-in">
        <a href="index.html" class="botao">Voltar à Página Inicial</a>
    </section>

    <footer>
        <p>© 2025 - Meus Projetos</p>
    </footer>
</body>
</html>
```

**Observação:** Todas as seções possuem a classe `fade-in` para que a animação seja aplicada automaticamente.

---

### **Exercício 3 – Criando a página de Disciplinas**

1. Crie **uma nova página**, parecida com a página de Projetos (`projeto.html`).
2. Essa página deve listar as **disciplinas que você está vendo neste semestre**, cada uma em uma `<section>` dentro da `<div class="container">`.
3. Use os **mesmos estilos** e a **classe `fade-in`** para manter o padrão de animação.
4. Adicione um **botão de retorno** para a página principal (`index.html`).
5. Adicione na página de (`index.html`) uma nova seção igual vista em (`projetos.html`) para criar um link com a página nova 

Abaixo segue um exemplo da possível estrutura de uma seção: para criar as disciplinas:

```html
<section class="fade-in">
    <h2>Disciplina 1</h2>
    <p>Descrição breve da disciplina.</p>
</section>
```

---