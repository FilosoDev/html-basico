# 🚀 JavaScript Básico: Fundamentos da Programação Web

## 🎯 Objetivo do Módulo

Este módulo ensina os fundamentos da linguagem JavaScript, a linguagem de programação que adiciona interatividade e dinamismo às páginas web. Você aprenderá desde conceitos básicos até manipulação de dados e funções.

---

## 📚 Conteúdo do Módulo

### 1. **Introdução ao JavaScript**
- O que é JavaScript e sua importância
- JavaScript vs outras linguagens
- Como incluir JavaScript no HTML
- Console do desenvolvedor

### 2. **Sintaxe Básica**
- Variáveis e constantes
- Tipos de dados
- Operadores
- Comentários

### 3. **Estruturas de Controle**
- Condicionais (if, else, switch)
- Loops (for, while, do-while)
- Break e continue

### 4. **Funções**
- Declaração de funções
- Parâmetros e argumentos
- Return
- Arrow functions

### 5. **Arrays e Objetos**
- Criação e manipulação de arrays
- Métodos de arrays
- Objetos literais
- Propriedades e métodos

### 6. **Eventos Básicos**
- Introdução a eventos
- onclick, onload, onchange
- Preparação para DOM

---

## 🌟 Por Que Aprender JavaScript?

### 💡 JavaScript é Essencial Porque:
- **🌐 Linguagem da Web**: Única linguagem que roda nativamente nos navegadores
- **⚡ Interatividade**: Transforma páginas estáticas em experiências dinâmicas
- **📱 Versatilidade**: Frontend, backend, mobile, desktop
- **🔥 Demanda**: Uma das linguagens mais procuradas no mercado
- **🚀 Evolução**: Sempre se atualizando com novos recursos

### 🎯 O que Você Conseguirá Fazer:
- Validar formulários em tempo real
- Criar animações e efeitos visuais
- Manipular conteúdo dinamicamente
- Consumir APIs e dados externos
- Construir aplicações interativas

---

## 📖 Fundamentos da Linguagem

### 🔢 Variáveis e Tipos de Dados

```javascript
// Declaração de variáveis
let nome = "João";              // String (texto)
const idade = 25;               // Number (número)
let ativo = true;               // Boolean (verdadeiro/falso)
let lista = [1, 2, 3];          // Array (lista)
let pessoa = {                  // Object (objeto)
    nome: "Maria",
    idade: 30
};
let vazio = null;               // Null (nulo)
let indefinido;                 // Undefined (indefinido)
```

### 🧮 Operadores

| Tipo | Operadores | Exemplo |
|------|------------|---------|
| **Aritméticos** | `+`, `-`, `*`, `/`, `%`, `**` | `10 + 5 = 15` |
| **Comparação** | `==`, `===`, `!=`, `!==`, `>`, `<`, `>=`, `<=` | `5 === 5 // true` |
| **Lógicos** | `&&`, `\|\|`, `!` | `true && false // false` |
| **Atribuição** | `=`, `+=`, `-=`, `*=`, `/=` | `x += 5` |

### 🔀 Estruturas Condicionais

```javascript
// IF/ELSE
if (idade >= 18) {
    console.log("Maior de idade");
} else {
    console.log("Menor de idade");
}

// SWITCH
switch (dia) {
    case 1:
        console.log("Segunda-feira");
        break;
    case 2:
        console.log("Terça-feira");
        break;
    default:
        console.log("Outro dia");
}

// OPERADOR TERNÁRIO
let status = idade >= 18 ? "adulto" : "menor";
```

### 🔄 Loops (Repetição)

```javascript
// FOR - quando sabemos quantas vezes repetir
for (let i = 0; i < 5; i++) {
    console.log("Número: " + i);
}

// WHILE - enquanto condição for verdadeira
let contador = 0;
while (contador < 3) {
    console.log("Contador: " + contador);
    contador++;
}

// FOR...OF - para arrays
let frutas = ["maçã", "banana", "laranja"];
for (let fruta of frutas) {
    console.log(fruta);
}

// FOR...IN - para objetos
let pessoa = {nome: "João", idade: 25};
for (let propriedade in pessoa) {
    console.log(propriedade + ": " + pessoa[propriedade]);
}
```

---

## 🛠️ Funções

### 📝 Declaração de Funções

```javascript
// Função tradicional
function saudar(nome) {
    return "Olá, " + nome + "!";
}

// Função arrow (ES6+)
const saudarArrow = (nome) => {
    return "Olá, " + nome + "!";
};

// Arrow function simplificada
const saudarSimples = nome => "Olá, " + nome + "!";

// Chamando as funções
console.log(saudar("Maria"));        // "Olá, Maria!"
console.log(saudarArrow("João"));    // "Olá, João!"
console.log(saudarSimples("Ana"));   // "Olá, Ana!"
```

### 🎯 Exemplos Práticos de Funções

```javascript
// Função para calcular área de círculo
function calcularAreaCirculo(raio) {
    const pi = 3.14159;
    return pi * raio * raio;
}

// Função para verificar se número é par
const ehPar = numero => numero % 2 === 0;

// Função com múltiplos parâmetros
function criarPessoa(nome, idade, cidade = "São Paulo") {
    return {
        nome: nome,
        idade: idade,
        cidade: cidade,
        apresentar: function() {
            return `Olá, eu sou ${this.nome}, tenho ${this.idade} anos e moro em ${this.cidade}`;
        }
    };
}

// Usando as funções
console.log(calcularAreaCirculo(5));     // 78.53975
console.log(ehPar(4));                   // true
console.log(ehPar(7));                   // false

let pessoa = criarPessoa("Carlos", 28);
console.log(pessoa.apresentar());        // "Olá, eu sou Carlos, tenho 28 anos e moro em São Paulo"
```

---

## 📋 Arrays (Listas)

### 🔧 Criação e Manipulação

```javascript
// Criando arrays
let numeros = [1, 2, 3, 4, 5];
let frutas = ["maçã", "banana", "laranja"];
let misto = [1, "texto", true, {nome: "João"}];

// Acessando elementos
console.log(frutas[0]);        // "maçã"
console.log(frutas.length);    // 3

// Modificando elementos
frutas[1] = "uva";             // ["maçã", "uva", "laranja"]
```

### 🎯 Métodos Essenciais de Arrays

```javascript
let numeros = [1, 2, 3, 4, 5];

// Adicionar elementos
numeros.push(6);               // Adiciona no final: [1,2,3,4,5,6]
numeros.unshift(0);            // Adiciona no início: [0,1,2,3,4,5,6]

// Remover elementos
numeros.pop();                 // Remove do final: [0,1,2,3,4,5]
numeros.shift();               // Remove do início: [1,2,3,4,5]

// Encontrar elementos
numeros.indexOf(3);            // Retorna posição: 2
numeros.includes(4);           // Verifica se existe: true

// Filtrar elementos
let pares = numeros.filter(num => num % 2 === 0);  // [2, 4]

// Transformar elementos
let dobrados = numeros.map(num => num * 2);        // [2, 4, 6, 8, 10]

// Reduzir array
let soma = numeros.reduce((total, num) => total + num, 0);  // 15
```

---

## 🏗️ Objetos

### 📦 Criação e Uso

```javascript
// Objeto literal
let carro = {
    marca: "Toyota",
    modelo: "Corolla",
    ano: 2023,
    cor: "prata",
    
    // Método (função dentro do objeto)
    acelerar: function() {
        return "O carro está acelerando!";
    },
    
    // Método com arrow function
    frear: () => "O carro está freando!",
    
    // Getter
    get descricao() {
        return `${this.marca} ${this.modelo} ${this.ano}`;
    },
    
    // Setter
    set novaCor(cor) {
        this.cor = cor;
    }
};

// Acessando propriedades
console.log(carro.marca);              // "Toyota"
console.log(carro["modelo"]);          // "Corolla"

// Chamando métodos
console.log(carro.acelerar());         // "O carro está acelerando!"

// Usando getter/setter
console.log(carro.descricao);          // "Toyota Corolla 2023"
carro.novaCor = "azul";
console.log(carro.cor);                // "azul"

// Adicionando novas propriedades
carro.preco = 80000;
carro.vender = function() {
    return `Carro vendido por R$ ${this.preco}`;
};
```

---

## ⚡ Eventos Básicos

### 🖱️ Interação com o Usuário

```javascript
// Aguardar carregamento da página
window.onload = function() {
    console.log("Página carregada!");
};

// Ou usando addEventListener
window.addEventListener('load', function() {
    console.log("Página carregada com addEventListener!");
});

// Função para ser chamada por botão
function mostrarAlerta() {
    alert("Botão clicado!");
}

// Função para validar formulário
function validarFormulario() {
    let nome = document.getElementById('nome').value;
    
    if (nome === '') {
        alert('Por favor, preencha o nome!');
        return false;
    }
    
    alert('Formulário válido!');
    return true;
}

// Função para mudar conteúdo
function mudarTexto() {
    let elemento = document.getElementById('texto');
    elemento.innerHTML = 'Texto foi alterado!';
}
```

---

## 💡 Exemplos Práticos

### 🧮 Calculadora Simples

```javascript
function calcular(operacao, num1, num2) {
    switch (operacao) {
        case '+':
            return num1 + num2;
        case '-':
            return num1 - num2;
        case '*':
            return num1 * num2;
        case '/':
            return num2 !== 0 ? num1 / num2 : 'Erro: Divisão por zero';
        default:
            return 'Operação inválida';
    }
}

// Usando a calculadora
console.log(calcular('+', 10, 5));   // 15
console.log(calcular('/', 10, 0));   // "Erro: Divisão por zero"
```

### 📊 Sistema de Notas

```javascript
function calcularMedia(notas) {
    let soma = notas.reduce((total, nota) => total + nota, 0);
    return soma / notas.length;
}

function obterConceito(media) {
    if (media >= 9) return 'A';
    if (media >= 7) return 'B';
    if (media >= 5) return 'C';
    return 'D';
}

function criarBoletim(aluno, notas) {
    let media = calcularMedia(notas);
    let conceito = obterConceito(media);
    
    return {
        nome: aluno,
        notas: notas,
        media: media.toFixed(2),
        conceito: conceito,
        aprovado: media >= 7
    };
}

// Exemplo de uso
let boletim = criarBoletim("João", [8.5, 7.0, 9.2, 6.8]);
console.log(boletim);
// { nome: "João", notas: [8.5, 7.0, 9.2, 6.8], media: "7.88", conceito: "B", aprovado: true }
```

---

## 📚 Boas Práticas

### ✅ Código Limpo

```javascript
// ❌ Evite
var x = 5;
var y = 10;
var z = x + y;

// ✅ Prefira
const primeiroNumero = 5;
const segundoNumero = 10;
const resultado = primeiroNumero + segundoNumero;

// ❌ Evite
function f(x, y) {
    return x + y;
}

// ✅ Prefira
function somar(numeroA, numeroB) {
    return numeroA + numeroB;
}
```

### 🔍 Debugging

```javascript
// Console para debugging
console.log("Valor da variável:", minhaVariavel);
console.error("Erro encontrado:", erro);
console.warn("Aviso:", mensagem);
console.table(meuArray);

// Try/catch para tratamento de erros
try {
    // Código que pode gerar erro
    let resultado = calcular('/', 10, 0);
} catch (erro) {
    console.error("Erro capturado:", erro.message);
} finally {
    console.log("Sempre executa");
}
```

---

## 🎯 Exercícios Práticos

### 🏆 Nível Iniciante
1. **Calculadora**: Criar funções para operações básicas
2. **Verificador de Idade**: Determinar se pessoa é menor, adulta ou idosa
3. **Contador**: Sistema para incrementar/decrementar números

### 🏆 Nível Intermediário
1. **Lista de Tarefas**: Adicionar, remover e marcar tarefas
2. **Jogo de Adivinhação**: Gerar número aleatório e dar dicas
3. **Conversor de Unidades**: Temperatura, peso, distância

### 🏆 Nível Avançado
1. **Sistema de Login**: Validação e armazenamento local
2. **Cronômetro**: Contar tempo com start/stop/reset
3. **Quiz Interativo**: Perguntas com pontuação

---

## ✅ Checklist de Aprendizado

### Conceitos Básicos
- [ ] Entender variáveis e tipos de dados
- [ ] Usar operadores aritméticos e lógicos
- [ ] Implementar estruturas condicionais
- [ ] Criar e usar loops
- [ ] Trabalhar com funções

### Estruturas de Dados
- [ ] Manipular arrays e seus métodos
- [ ] Criar e usar objetos
- [ ] Entender propriedades e métodos
- [ ] Usar destructuring básico

### Eventos
- [ ] Implementar eventos básicos
- [ ] Validar formulários
- [ ] Manipular conteúdo simples
- [ ] Preparar para DOM avançado

---

## 🚀 Próximos Passos

Após dominar este módulo, você estará pronto para:

1. **08-javascript-dom**: Manipulação avançada do DOM
2. **APIs e Fetch**: Consumir dados externos
3. **JavaScript ES6+**: Recursos modernos da linguagem
4. **Frameworks**: React, Vue, Angular

---

## 💡 Dicas Importantes

### ✅ Para Aprender Melhor
- **Practice, practice, practice**: Programação se aprende fazendo
- **Use o console**: Sempre teste seus códigos no navegador
- **Leia códigos de outros**: Aprenda vendo exemplos reais
- **Comece simples**: Domine o básico antes de avançar
- **Documente seu código**: Deixe comentários explicativos

### 🎯 Recursos Úteis
- **MDN Web Docs**: Documentação oficial
- **JavaScript.info**: Tutorial completo
- **Console do navegador**: Ferramenta de teste
- **CodePen/JSFiddle**: Editores online para praticar

---

🚀 **Lembre-se**: JavaScript é a linguagem que dá vida à web. Com estes fundamentos, você terá a base sólida para criar experiências incríveis na internet!