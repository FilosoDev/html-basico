# O que é o DOM?

**DOM** significa **Document Object Model** (Modelo de Objeto de Documento).  
Ele é uma **interface de programação** que os navegadores usam para representar páginas web de forma estruturada e interativa.

### Em termos simples:
O DOM é a maneira como o navegador **vê** e **organiza** a página web — como uma árvore de objetos — para que **programas**, como o JavaScript, possam **ler**, **alterar**, **adicionar** ou **remover** elementos da página dinamicamente.

---

## Como o DOM funciona?

Quando você carrega uma página web (HTML), o navegador:
1. **Lê** o código HTML.
2. **Interpreta** a estrutura dos elementos (`<html>`, `<head>`, `<body>`, `<div>`, etc.).
3. **Cria uma árvore de nós** (nós = nodes) em memória para representar essa estrutura.

Essa árvore é chamada de **Árvore DOM**.

**Cada parte do HTML** vira um objeto:
- As **tags** viram **elementos**.
- Os **textos** dentro das tags viram **nós de texto**.
- Os **atributos** (como `id`, `class`, etc.) são tratados como **propriedades** desses objetos.

---

# Exemplo de Árvore DOM

Imagine esse HTML simples:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Minha Página</title>
  </head>
  <body>
    <h1>Bem-vindo!</h1>
    <p>Este é um parágrafo.</p>
  </body>
</html>
```

O navegador cria essa estrutura em memória:

```
Document
└── html
    ├── head
    │   └── title
    │       └── "Minha Página"
    └── body
        ├── h1
        │   └── "Bem-vindo!"
        └── p
            └── "Este é um parágrafo."
```

Ou seja, o `Document` é o **nó raiz**, e tudo dentro dele é organizado como uma **árvore de objetos**.

---

# Tipos de nós (Nodes) no DOM

No DOM, existem vários tipos de nós:

| Tipo de Nó        | Exemplo                                         |
|--------------------|-------------------------------------------------|
| Document           | Representa o documento inteiro                 |
| Element            | Tags HTML, como `<p>`, `<h1>`, `<div>`, etc.    |
| Text               | Texto dentro de elementos                      |
| Attribute          | Atributos das tags (como `class`, `id`)         |
| Comment            | Comentários no HTML (`<!-- Comentário -->`)     |

---

### O que é o DOM em Aplicações Web?

O **DOM** (Document Object Model) é uma interface de programação para documentos HTML e XML. Ele representa a estrutura de um documento de forma hierárquica, permitindo que os desenvolvedores manipulem dinamicamente o conteúdo, a estrutura e o estilo de uma página web. Em outras palavras, o DOM cria uma **representação em árvore** de todos os elementos de uma página (como `<div>`, `<p>`, `<span>`, etc.) e permite que esses elementos sejam manipulados diretamente via JavaScript.

### Como usamos o DOM nas aplicações web?

Em aplicações web modernas, o DOM é a ponte entre o **navegador** e o **JavaScript**, permitindo que interajamos com o conteúdo da página após ela ser carregada. Podemos **criar, modificar, remover e atualizar** elementos, atributos e até o estilo visual de uma página sem a necessidade de recarregar a página inteira. Isso torna a navegação e interação mais rápidas e fluídas, proporcionando uma **experiência de usuário mais dinâmica e responsiva**.

### Para que usamos o DOM nas aplicações?

O DOM é utilizado para **dinamizar e interagir com o conteúdo da página**, tornando-a mais interativa. Alguns dos principais usos incluem:

1. **Manipulação de conteúdo dinâmico**: Podemos atualizar textos, imagens ou outros elementos da página sem precisar recarregar toda a página. Por exemplo, em sistemas de chat, novas mensagens podem ser exibidas dinamicamente sem a necessidade de atualizar a página.
   
2. **Criação e remoção de elementos**: O DOM nos permite criar novos elementos (como botões, listas, formulários) e removê-los de forma programática. Isso é útil para criar interfaces interativas e sistemas de carregamento dinâmico de conteúdo.

3. **Alteração de estilos e classes**: Através do DOM, podemos modificar as propriedades de estilo de um elemento, como cor, tamanho, margem, entre outros. Também podemos adicionar ou remover classes CSS, permitindo que as páginas mudem visualmente em tempo real com base em interações do usuário.

4. **Manipulação de formulários**: O DOM permite que a gente altere os valores de campos de formulários (como inputs, selects, checkboxes), e também valide e envie dados sem recarregar a página (por exemplo, com Ajax).

5. **Eventos e interações**: O DOM é essencial para capturar e responder a eventos de interação do usuário, como **cliques**, **teclados**, **movimentos do mouse**, etc. Ele permite a **geração de respostas dinâmicas**, como exibir alertas, mudar o conteúdo de um campo ou fazer animações.

### Onde usamos o DOM no desenvolvimento de software?

O DOM é **onipresente** no desenvolvimento de **aplicações web**. Qualquer página web que tenha JavaScript usa o DOM para permitir interatividade. Aqui estão alguns exemplos de onde usamos o DOM:

1. **Aplicações interativas (SPA)**: Em aplicações de página única (Single Page Applications - SPAs), como aquelas feitas com **React**, **Vue.js** ou **Angular**, o DOM é manipulado constantemente para atualizar a interface sem a necessidade de recarregar a página inteira. Cada vez que o estado da aplicação muda, o DOM é atualizado para refletir as novas informações.

2. **Sites dinâmicos e interativos**: Websites que têm conteúdo que muda em tempo real, como **sites de notícias**, **dashboards**, **sistemas de e-commerce** ou **blogs**, frequentemente manipulam o DOM para carregar novos artigos, atualizar informações em tempo real, exibir produtos baseados nas escolhas do usuário, etc.

3. **Jogo e entretenimento interativo**: Muitos jogos baseados em navegador ou animações interativas dependem do DOM para mover objetos na tela, interagir com o usuário e responder a eventos.

4. **Acessibilidade e controle de formulário**: O DOM é fundamental para a criação de **formulários acessíveis**, onde podemos manipular o foco (seleção de campo), exibir mensagens de erro de validação, ou até mesmo personalizar os campos dinamicamente com base nas respostas do usuário.

### Como o DOM no dia a dia do desenvolvimento de software?
Aqui está a explicação detalhada de cada uma das etapas listadas no uso do DOM:

---

### Explicação Detalhada sobre **Selecionando Elementos** no DOM

Selecionar elementos é a **primeira etapa** para interagir com qualquer página web através do DOM. Antes de podermos modificar ou manipular qualquer coisa na página, precisamos **localizar os elementos** que queremos afetar. O DOM oferece várias maneiras de **selecionar** esses elementos com base em seus atributos, como **ID**, **classe**, **nome da tag** ou outros atributos personalizados.

#### Por que é importante?
Quando você trabalha com DOM, o processo de **seleção** é o primeiro passo para poder alterar o conteúdo, estilo ou comportamento de um elemento específico na página.

### Como Selecionamos Elementos?

O método `getElementById()` é utilizado para selecionar um único elemento que tenha um **ID específico**. Esse método retorna o primeiro (e geralmente único) elemento que tem o ID fornecido.

- **Uso**: `document.getElementById('id')`
- **Retorna**: O elemento que possui o ID especificado ou `null` se não encontrar nenhum elemento com esse ID.

**Exemplo**:
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Exemplo getElementById</title>
</head>
<body>
    <h1 id="titulo">Olá, Mundo!</h1>
    <button id="botao">Clique aqui</button>

    <script>
        const titulo = document.getElementById('titulo');
        console.log(titulo);  // Exibe o elemento <h1 id="titulo">
        
        const botao = document.getElementById('botao');
        console.log(botao);  // Exibe o elemento <button id="botao">
    </script>
</body>
</html>
```
Neste exemplo, o `getElementById()` retorna os elementos `<h1>` e `<button>` que possuem os IDs "titulo" e "botao", respectivamente.

#### 2. **`getElementsByClassName()`**

O método `getElementsByClassName()` é usado para selecionar todos os elementos que têm uma determinada **classe**. Esse método retorna uma coleção de elementos com a classe indicada.

- **Uso**: `document.getElementsByClassName('nome-da-classe')`
- **Retorna**: Uma coleção (não um único elemento) de todos os elementos que têm a classe especificada. Para acessar um elemento específico dessa coleção, você deve usar um índice.

**Exemplo**:
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Exemplo getElementsByClassName</title>
</head>
<body>
    <p class="paragrafo">Parágrafo 1</p>
    <p class="paragrafo">Parágrafo 2</p>
    <p class="paragrafo">Parágrafo 3</p>

    <script>
        const paragrafos = document.getElementsByClassName('paragrafo');
        console.log(paragrafos);  // Retorna uma coleção de todos os elementos <p> com a classe "paragrafo"
        
        // Acessando um item específico na coleção
        console.log(paragrafos[1]);  // Exibe o segundo parágrafo
    </script>
</body>
</html>
```
Neste caso, todos os parágrafos que têm a classe `"paragrafo"` são selecionados. A variável `paragrafos` contém uma **coleção de elementos**, então você precisa usar um índice para acessar um item específico.

#### 3. **`querySelector()`**

O método `querySelector()` é uma maneira muito poderosa e flexível de selecionar um **único** elemento, baseado em um **seletor CSS**. Ele funciona de forma semelhante a como você selecionaria elementos com CSS, permitindo selecionar por **ID**, **classe**, **nome de tag**, entre outros.

- **Uso**: `document.querySelector('seletor')`
- **Retorna**: O **primeiro** elemento que corresponde ao seletor CSS especificado ou `null` se não encontrar nenhum elemento correspondente.

**Exemplo**:
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Exemplo querySelector</title>
</head>
<body>
    <div class="caixa">Caixa 1</div>
    <div class="caixa">Caixa 2</div>
    <div class="caixa">Caixa 3</div>

    <script>
        const caixa = document.querySelector('.caixa');
        console.log(caixa);  // Exibe o **primeiro** <div class="caixa">
    </script>
</body>
</html>
```
Aqui, o `querySelector()` retorna o **primeiro** `<div>` que tem a classe `"caixa"`. Se você quiser selecionar todos os elementos com a classe, deve usar `querySelectorAll()`.

#### 4. **`querySelectorAll()`**

O método `querySelectorAll()` seleciona **todos** os elementos que correspondem ao seletor CSS fornecido. Ele retorna uma lista de **todos os elementos** que combinam com o seletor.

- **Uso**: `document.querySelectorAll('seletor')`
- **Retorna**: Uma lista **NodeList** de todos os elementos que correspondem ao seletor.

**Exemplo**:
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Exemplo querySelectorAll</title>
</head>
<body>
    <p class="texto">Texto 1</p>
    <p class="texto">Texto 2</p>
    <p class="texto">Texto 3</p>

    <script>
        const textos = document.querySelectorAll('.texto');
        console.log(textos);  // Retorna uma NodeList de todos os <p> com a classe "texto"
        
        // Acessando um item específico
        console.log(textos[1]);  // Exibe o segundo parágrafo com a classe "texto"
    </script>
</body>
</html>
```
Neste exemplo, `querySelectorAll()` seleciona todos os elementos `<p>` que têm a classe `"texto"`, e retorna uma **NodeList** que você pode percorrer.

### Resumo de Seleção de Elementos

| Método                       | Descrição                                                       | Retorna                                           |
|------------------------------|---------------------------------------------------------------|--------------------------------------------------|
| `getElementById()`            | Seleciona um elemento pelo **ID**.                            | Um único elemento (ou `null` se não encontrar)   |
| `getElementsByClassName()`    | Seleciona todos os elementos por **classe**.                  | Uma coleção de elementos                        |
| `querySelector()`             | Seleciona o **primeiro** elemento que corresponde ao seletor. | Um único elemento (ou `null` se não encontrar)   |
| `querySelectorAll()`          | Seleciona todos os elementos que correspondem ao seletor.     | Uma lista de elementos (NodeList)               |

### Exemplos Simples e Didáticos:

1. **Selecionando um elemento por ID**:
```html
<div id="paragrafo1">Texto do Parágrafo 1</div>
<script>
  const paragrafo1 = document.getElementById('paragrafo1');
  console.log(paragrafo1);  // Exibe o elemento <div id="paragrafo1">
</script>
```

2. **Selecionando elementos por classe**:
```html
<div class="item">Item 1</div>
<div class="item">Item 2</div>
<div class="item">Item 3</div>
<script>
  const items = document.getElementsByClassName('item');
  console.log(items);  // Exibe todos os elementos com a classe "item"
</script>
```

3. **Usando `querySelector()` para selecionar o primeiro elemento**:
```html
<p class="alerta">Alerta 1</p>
<p class="alerta">Alerta 2</p>
<script>
  const alerta = document.querySelector('.alerta');
  console.log(alerta);  // Exibe o **primeiro** <p> com a classe "alerta"
</script>
```

4. **Usando `querySelectorAll()` para selecionar todos os elementos com uma classe**:
```html
<p class="noticia">Notícia 1</p>
<p class="noticia">Notícia 2</p>
<script>
  const noticias = document.querySelectorAll('.noticia');
  console.log(noticias);  // Exibe todos os <p> com a classe "noticia"
</script>
```

A seleção de elementos no DOM é essencial para qualquer manipulação dinâmica de conteúdo em uma página web. A escolha do método de seleção depende do que você precisa fazer:

- Use `getElementById()` para **IDs únicos**.
- Use `getElementsByClassName()` ou `querySelectorAll()` para selecionar **múltiplos elementos** com uma **classe**.
- Use `querySelector()` para **selecionar o primeiro elemento** correspondente a um seletor CSS.

---

### Manipulando conteúdo

- `textContent`
- `innerHTML`
- `value`
- Manipulando conteúdo de **div**, **input** e **parágrafos**.

Vai ficar simples, bonito e didático:

---

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Exemplos de Manipulação de Conteúdo</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
    }
    .caixa {
      margin: 20px 0;
      padding: 10px;
      border: 1px solid #ccc;
      background-color: #f9f9f9;
    }
    button {
      margin: 5px;
      padding: 5px 10px;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <h1 id="titulo">Título Original</h1>

  <div class="caixa" id="caixa">
    Aqui é a caixa de texto inicial.
  </div>

  <input type="text" id="campoTexto" value="Valor Inicial">
  <br><br>

  <button onclick="mudarTitulo()">Alterar Título (textContent)</button>
  <button onclick="alterarCaixa()">Alterar Caixa (innerHTML)</button>
  <button onclick="alterarCampo()">Alterar Campo (value)</button>
  <button onclick="mostrarCampo()">Mostrar Valor do Campo</button>

  <p id="resultado"></p>

  <script>
    function mudarTitulo() {
      const titulo = document.getElementById('titulo');
      titulo.textContent = 'Título alterado com textContent!';
    }

    function alterarCaixa() {
      const caixa = document.getElementById('caixa');
      caixa.innerHTML = '<strong>Texto mudado com HTML!</strong> Agora tem <em>formatação</em>.';
    }

    function alterarCampo() {
      const campo = document.getElementById('campoTexto');
      campo.value = 'Novo valor definido via JavaScript';
    }

    function mostrarCampo() {
      const campo = document.getElementById('campoTexto');
      const resultado = document.getElementById('resultado');
      resultado.textContent = 'Valor atual do campo: ' + campo.value;
    }
  </script>

</body>
</html>
```

---

### que essa página faz?

- Tem um **título** (`h1`) que muda usando **`textContent`**.
- Tem uma **div ("caixa")** que muda usando **`innerHTML`** com tags HTML (negrito, itálico).
- Tem um **campo de texto (`input`)** que:
  - Pode ter o **valor alterado** com JavaScript (**`value`**).
  - Pode ter o **valor mostrado** em um parágrafo.

---

### 3. **Alterando Estilos**

Claro! Vou fazer uma explicação bem detalhada sobre **Alterando Estilos com DOM**, com exemplos simples e didáticos para ficar bem claro.

---

# 🎨 Alterando Estilos com o DOM

### O que significa "alterar estilos"?

Quando alteramos estilos pelo DOM, estamos **mudando a aparência de elementos HTML** usando **JavaScript**, sem precisar editar diretamente o arquivo CSS.  
Isso permite que sua página web **responda dinamicamente** às ações do usuário, como um clique ou uma digitação.

---

# 📚 Como Alterar Estilos?

Existem **duas formas principais** de alterar o estilo de um elemento:

### 1. Usar a propriedade `.style`

Você pode acessar e modificar o estilo **diretamente** usando `.style`.  
O nome das propriedades de CSS muda para o formato **camelCase** no JavaScript.

| CSS | JavaScript (style) |
|----|---------------------|
| `background-color` | `backgroundColor` |
| `font-size` | `fontSize` |
| `text-align` | `textAlign` |

---

### 2. Usar `.classList` para adicionar/remover classes

Em vez de mexer no estilo individualmente, você pode **adicionar** ou **remover classes CSS** usando `classList`.  
Assim, o estilo continua organizado no seu arquivo `.css` e o JS apenas gerencia **qual classe** o elemento possui.

---

# ✏️ Exemplos Didáticos

## 1. Alterando diretamente com `.style`

```html
<button id="botao">Clique para mudar cor</button>

<script>
  const botao = document.getElementById('botao');
  botao.onclick = function() {
    botao.style.backgroundColor = 'blue';
    botao.style.color = 'white';
    botao.style.fontSize = '20px';
  };
</script>
```

**Explicação**:
- Quando o botão for clicado, o fundo dele vai mudar para azul, o texto para branco e o tamanho da fonte vai aumentar.

---

### 2. Alterando estilo com `classList.add` e CSS

```html
<style>
  .estilo-destacado {
    background-color: yellow;
    color: red;
    font-weight: bold;
  }
</style>

<button id="destacar">Destacar Texto</button>
<p id="texto">Este é um texto normal.</p>

<script>
  const botao = document.getElementById('destacar');
  const texto = document.getElementById('texto');

  botao.addEventListener('click', function() {
    texto.classList.add('estilo-destacado');
  });
</script>
```

**Explicação**:
- Ao clicar no botão, adicionamos a classe `estilo-destacado` ao `<p>`, mudando todo o seu estilo de uma vez só.
- Essa abordagem deixa o JavaScript mais limpo e o CSS organizado.

---

## 3. Alternar estilos com `classList.toggle`

```html
<style>
  .ativo {
    background-color: green;
    color: white;
    padding: 10px;
  }
</style>

<button id="alternar">Ativar/Desativar Estilo</button>

<script>
  const botao = document.getElementById('alternar');

  botao.addEventListener('click', function() {
    botao.classList.toggle('ativo');
  });
</script>
```

**Explicação**:
- Toda vez que clicar no botão, ele **ativa ou desativa** a classe `ativo`.
- `toggle` é útil para criar efeitos de liga/desliga.

---

| Como? | Quando usar? | Exemplo |
|----|----|----|
| `.style.propriedade` | Quando mudar UM estilo específico | `element.style.color = 'blue'` |
| `.classList.add('classe')` | Para aplicar vários estilos definidos no CSS | `element.classList.add('ativo')` |
| `.classList.remove('classe')` | Para remover um estilo CSS aplicado | `element.classList.remove('ativo')` |
| `.classList.toggle('classe')` | Para alternar entre estilos (ligar/desligar) | `element.classList.toggle('ativo')` |

---


**Alterar estilos com DOM** é essencial para criar páginas **dinâmicas** e **interativas**.  
Usamos isso para:
- **Destacar** elementos ao passar o mouse
- **Mostrar/ocultar** áreas de conteúdo
- **Responder** a cliques e ações do usuário
- **Adaptar** a aparência da página dinamicamente

---

Se quiser, posso também montar um **mini-projeto prático** aplicando essas técnicas para fixar ainda mais. Quer? 🎯

### 4. **Criando e Removendo Elementos**

**Objetivo**: Em vez de modificar elementos existentes, o DOM também permite **criar novos elementos** ou **remover elementos** existentes na página.

#### Como fazer:
- `document.createElement('tag')`: Cria um novo elemento HTML.
- `appendChild()`: Adiciona um elemento como **filho** de outro elemento.
- `removeChild()`: Remove um elemento **filho** de um pai.
- `insertBefore()`: Insere um novo elemento **antes** de um elemento existente.

#### Exemplo:
```javascript
// Criando um novo parágrafo e adicionando à página
const novoParagrafo = document.createElement('p');
novoParagrafo.textContent = 'Este é um novo parágrafo';
document.body.appendChild(novoParagrafo);

// Removendo um elemento existente
const elementoRemover = document.getElementById('elemento-remover');
elementoRemover.parentNode.removeChild(elementoRemover);
```

### 5. **Trabalhando com Eventos**

**Objetivo**: O DOM permite que você **adicione interatividade** à página, **ouvindo eventos** que acontecem quando o usuário interage com os elementos da página, como cliques, digitação, rolagem, entre outros.

#### Como fazer:
Você pode usar `addEventListener` para associar funções a eventos específicos. O evento pode ser algo como `click`, `submit`, `keypress`, `mouseover`, etc.

- `addEventListener(evento, funcao)`: Associa uma função a um evento.
- `removeEventListener()`: Remove um evento de um elemento.

#### Exemplo:
```javascript
// Evento de clique
const botao = document.getElementById('botao');
botao.addEventListener('click', function() {
  alert('Botão clicado!');
});

// Evento de mudança em um input
const inputTexto = document.getElementById('inputTexto');
inputTexto.addEventListener('input', function() {
  console.log('Valor do input:', inputTexto.value);
});
```

### 6. **Manipulando Formulários**

**Objetivo**: O DOM oferece formas práticas de **interagir e manipular** os elementos de formulários, como campos de texto, selects e botões, permitindo **validar dados**, **capturar valores** e até **enviar os dados** sem recarregar a página.

#### Como fazer:
- `value`: Captura ou altera o valor de campos de formulário como `input`, `textarea`, `select`.
- `submit()`: Envia o formulário programaticamente.
- `reset()`: Restaura os valores padrão dos campos.

#### Exemplo:
```javascript
// Capturando o valor de um campo de input
const inputNome = document.getElementById('nome');
console.log(inputNome.value);

// Validando se o campo não está vazio antes de enviar o formulário
const formulario = document.getElementById('formulario');
formulario.addEventListener('submit', function(event) {
  if (inputNome.value === '') {
    alert('Nome não pode estar vazio!');
    event.preventDefault(); // Impede o envio do formulário
  }
});
```

---

### Resumo das Etapas:

| Etapa                    | O que faz                                    | Método/Propriedade Principal               |
|--------------------------|---------------------------------------------|--------------------------------------------|
| **Selecionando Elementos** | Seleciona elementos da página para manipulação | `getElementById()`, `querySelector()`       |
| **Manipulando o Conteúdo** | Modifica o texto ou HTML dentro de elementos | `textContent`, `innerHTML`, `value`        |
| **Alterando Estilos**     | Altera estilos diretamente no elemento ou adiciona/remover classes CSS | `style`, `classList.add()`, `classList.remove()` |
| **Criando e Removendo Elementos** | Cria novos elementos ou remove existentes | `createElement()`, `appendChild()`, `removeChild()` |
| **Trabalhando com Eventos** | Adiciona eventos de interação do usuário à página | `addEventListener()`, `removeEventListener()` |
| **Manipulando Formulários** | Interage com campos de formulários, valida dados e envia sem recarregar | `value`, `submit()`, `reset()` |

Essas etapas são fundamentais para criar interfaces dinâmicas e interativas em aplicações web modernas. Cada uma delas tem seu papel específico, mas elas geralmente são usadas juntas para criar a experiência de usuário fluida e responsiva.

O DOM é **fundamental** no desenvolvimento de aplicações web dinâmicas e interativas. Ele oferece a **flexibilidade necessária** para criar interfaces de usuário ricas, responder rapidamente às ações dos usuários e atualizar o conteúdo da página de forma fluida, sem precisar recarregar a página. Em termos práticos, no **dia a dia do desenvolvimento**, o DOM é usado para:

- Criar e manipular elementos dinamicamente.
- Alterar o conteúdo e estilo de elementos.
- Trabalhar com eventos e interações do usuário.
- Manipular dados de formulários e inputs.

# Manipulação do DOM

Usando JavaScript, você pode **acessar** e **manipular** o DOM.

### Exemplos comuns:

- **Selecionar** elementos:
  ```javascript
  const titulo = document.querySelector('h1');
  ```

- **Alterar** texto:
  ```javascript
  titulo.textContent = 'Novo título!';
  ```

- **Criar** novos elementos:
  ```javascript
  const novoParagrafo = document.createElement('p');
  novoParagrafo.textContent = 'Outro parágrafo!';
  document.body.appendChild(novoParagrafo);
  ```

- **Modificar atributos**:
  ```javascript
  titulo.setAttribute('class', 'titulo-principal');
  ```

- **Remover elementos**:
  ```javascript
  titulo.remove();
  ```

---

# DOM e Eventos

Além de alterar a estrutura da página, você pode **ouvir** eventos no DOM, como cliques, teclado, etc.

Exemplo:
```javascript
const botao = document.querySelector('button');
botao.addEventListener('click', function() {
  alert('Você clicou no botão!');
});
```

Isso permite criar **interatividade** entre o usuário e a página.

---

# Algumas observações importantes:

- O DOM é uma **representação viva** da página: se você alterar algo no DOM via JavaScript, a alteração aparece **imediatamente** na tela.
- DOM não é exclusivo de HTML. Também pode representar documentos XML.
- A performance de manipulação do DOM pode impactar o desempenho de sites, especialmente se houver **muitas alterações** em elementos grandes.

---

# Resumindo:

| Conceito                 | Resumo Rápido                                                      |
|---------------------------|--------------------------------------------------------------------|
| O que é DOM               | Modelo em árvore da página web em objetos                          |
| Função principal          | Permitir que programas leiam e modifiquem a estrutura do documento |
| Baseado em                | HTML ou XML                                                       |
| Manipulação principal     | Feita com JavaScript                                               |
| Exemplos de uso           | Alterar textos, adicionar elementos, ouvir eventos                |


---

# Anatomia de um Elemento no DOM

Cada **elemento** no DOM (por exemplo, um `<p>`, `<div>`, `<img>`) tem várias **propriedades** e **métodos**.

Exemplo:

Imagine que temos no HTML:

```html
<p id="meuParagrafo" class="texto">Olá, mundo!</p>
```

Quando acessamos no JavaScript:

```javascript
const p = document.getElementById('meuParagrafo');
```

O `p` é um objeto que possui:

- `id`: `"meuParagrafo"`
- `className`: `"texto"`
- `innerHTML`: `"Olá, mundo!"` (inclui HTML interno se existir)
- `textContent`: `"Olá, mundo!"` (apenas o texto)
- `style`: acesso ao estilo CSS inline (`p.style.color = "red"`)
- `children`: lista de filhos se tiver
- `parentElement`: o elemento pai (`body` nesse caso)
- Métodos como `.appendChild()`, `.remove()`, `.cloneNode()`, etc.

**Cada elemento é super rico em informações e funcionalidades.**

---

# API do DOM

**API** (Application Programming Interface) do DOM é o **conjunto de objetos, métodos e eventos** que você usa para manipular documentos.

### Principais APIs do DOM:

| API                  | Função                                                       |
|-----------------------|---------------------------------------------------------------|
| Document API          | Manipular o documento (acessar elementos, criar novos, etc.)  |
| Element API           | Manipular elementos específicos (atributos, filhos, etc.)     |
| Events API            | Capturar e tratar eventos como clique, teclado, mouse         |
| Traversal API         | Navegar entre nós (pais, filhos, irmãos)                      |
| MutationObserver API  | Detectar mudanças no DOM automaticamente                      |

**Exemplo de Traversal API:**

```javascript
const div = document.querySelector('div');

console.log(div.parentElement); // Elemento pai
console.log(div.children);      // Lista de elementos filhos
console.log(div.nextElementSibling); // Próximo elemento irmão
console.log(div.previousElementSibling); // Elemento irmão anterior
```

---

# DOM vs HTML Estático

**Diferença importante**:

| HTML Estático       | DOM Dinâmico              |
|---------------------|----------------------------|
| Fixo no carregamento | Pode mudar com JavaScript  |
| Só leitura visual    | Acesso completo a objetos  |
| Não interativo       | Eventos e animações        |

Então quando você **modifica o DOM**, **não está alterando o arquivo HTML original**, mas sim a **representação carregada pelo navegador**.

---

# Eventos e Propagação no DOM

Quando ocorre um evento (tipo `click`), ele pode seguir três fases:

1. **Capturing Phase**: o evento vai do `document` até o alvo.
2. **Target Phase**: o evento chega no elemento que foi clicado.
3. **Bubbling Phase**: o evento "sobe" de volta pelo DOM.

🔵 **Bubbling** é o comportamento padrão: eventos "borbulham" de dentro para fora.

### Exemplo:
Se você clicar em um `<button>` dentro de um `<div>`, o evento será capturado primeiro no botão, depois "subirá" até o `div`, e depois até o `body`, e assim por diante.

### Capturando evento no bubbling:

```javascript
document.querySelector('div').addEventListener('click', function() {
  console.log('Div clicada!');
});
```

---

# DOM Virtual

Você pode ouvir falar de "**Virtual DOM**" em frameworks como **React**, **Vue**, etc.

**O que é o Virtual DOM?**

- É uma **cópia** do DOM real, mantida na memória.
- Quando você faz alterações, o framework **compara** o Virtual DOM com o DOM atual (isso se chama **diffing**).
- Depois, ele atualiza **apenas o que mudou** no DOM real, evitando alterações custosas.

🔵 Resultado: **Sites mais rápidos e responsivos!**

---

# Desafios do DOM

Apesar de ser super poderoso, manipular o DOM **direto** (sem frameworks) tem desafios:

- **Complexidade**: Em páginas grandes, navegar e manipular o DOM pode ser difícil.
- **Performance**: Muitas alterações rápidas podem deixar a página lenta.
- **Cross-browser**: Pequenas diferenças entre navegadores precisam ser tratadas.
- **Estado**: Gerenciar o que está na tela (estado da UI) pode ficar bagunçado.

Por isso, frameworks modernos **abstraem** essa complexidade para nós!

---

# Um resuminho visual para fechar 🧠:

```
[HTML] --> [Navegador lê] --> [Cria o DOM em árvore] --> [JavaScript acessa o DOM] --> [DOM altera a página em tempo real]
```

---

Se quiser, eu também posso te mostrar **exemplos mais avançados**, tipo:

- Criar uma **lista dinâmica** com input de usuário;
- Criar **animações** manipulando o DOM;
- Fazer **delegação de eventos** (evento para múltiplos elementos);
