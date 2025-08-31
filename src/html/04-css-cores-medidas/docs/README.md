# 🎨 CSS Cores e Medidas: Design Visual Profissional

## 🎯 Objetivo do Módulo

Este módulo ensina como trabalhar com cores e sistemas de medidas em CSS, fundamentais para criar designs visuais atraentes, responsivos e profissionais. Você aprenderá desde conceitos básicos até técnicas avançadas de design.

---

## 📚 Conteúdo do Módulo

### 1. **Sistemas de Cores**
- Cores nomeadas
- Hexadecimal (HEX)
- RGB e RGBA
- HSL e HSLA
- Gradientes lineares e radiais

### 2. **Unidades de Medida**
- Absolutas (px, pt, cm, mm, in)
- Relativas (%, em, rem, vh, vw)
- Unidades modernas (ch, ex, vmin, vmax)
- Quando usar cada uma

### 3. **Teoria das Cores**
- Círculo cromático
- Harmonias de cores
- Contraste e acessibilidade
- Psicologia das cores

### 4. **Design Responsivo**
- Unidades flexíveis
- Viewport units
- Calc() e variáveis CSS
- Mobile-first approach

---

## 🌈 Sistemas de Cores CSS

### 🏷️ Cores Nomeadas

CSS oferece 147 cores predefinidas com nomes em inglês:

```css
.exemplo-cores-nomeadas {
    color: red;              /* Vermelho */
    background-color: blue;  /* Azul */
    border-color: green;     /* Verde */
}

/* Exemplos de cores nomeadas */
.cores-basicas {
    /* Cores primárias */
    color: red;     /* #FF0000 */
    color: green;   /* #008000 */
    color: blue;    /* #0000FF */
    
    /* Cores neutras */
    color: black;   /* #000000 */
    color: white;   /* #FFFFFF */
    color: gray;    /* #808080 */
    
    /* Cores especiais */
    color: transparent;  /* Totalmente transparente */
    color: currentColor; /* Herda a cor do texto */
}
```

### 🔢 Sistema Hexadecimal (HEX)

O sistema mais popular para definir cores na web:

```css
/* Formato: #RRGGBB (Red, Green, Blue) */
.cores-hex {
    color: #FF0000;        /* Vermelho puro */
    color: #00FF00;        /* Verde puro */
    color: #0000FF;        /* Azul puro */
    color: #000000;        /* Preto */
    color: #FFFFFF;        /* Branco */
    color: #808080;        /* Cinza médio */
}

/* Formato abreviado quando dígitos são iguais */
.cores-hex-abreviado {
    color: #F00;   /* Mesmo que #FF0000 */
    color: #0F0;   /* Mesmo que #00FF00 */
    color: #00F;   /* Mesmo que #0000FF */
    color: #FFF;   /* Mesmo que #FFFFFF */
}

/* Com transparência (RGBA hex) */
.cores-hex-alpha {
    color: #FF000080;  /* Vermelho com 50% opacidade */
    color: #00FF0033;  /* Verde com ~20% opacidade */
}
```

### 🎨 RGB e RGBA

Sistema baseado em valores de vermelho, verde e azul:

```css
/* RGB: rgb(red, green, blue) - valores de 0 a 255 */
.cores-rgb {
    color: rgb(255, 0, 0);     /* Vermelho */
    color: rgb(0, 255, 0);     /* Verde */
    color: rgb(0, 0, 255);     /* Azul */
    color: rgb(128, 128, 128); /* Cinza */
}

/* RGBA: rgba(red, green, blue, alpha) - alpha de 0 a 1 */
.cores-rgba {
    background: rgba(255, 0, 0, 0.5);   /* Vermelho 50% transparente */
    background: rgba(0, 0, 0, 0.8);     /* Preto 80% opaco */
    background: rgba(255, 255, 255, 0.1); /* Branco quase transparente */
}

/* Usando porcentagens */
.cores-rgb-percent {
    color: rgb(100%, 0%, 0%);    /* Vermelho */
    color: rgb(50%, 50%, 50%);   /* Cinza */
}
```

### 🌈 HSL e HSLA

Sistema baseado em matiz, saturação e luminosidade:

```css
/* HSL: hsl(hue, saturation, lightness) */
.cores-hsl {
    /* Hue (matiz): 0-360 graus no círculo cromático */
    color: hsl(0, 100%, 50%);    /* Vermelho */
    color: hsl(120, 100%, 50%);  /* Verde */
    color: hsl(240, 100%, 50%);  /* Azul */
    
    /* Variações de uma cor ajustando saturação e luminosidade */
    color: hsl(220, 100%, 50%);  /* Azul saturado */
    color: hsl(220, 50%, 50%);   /* Azul menos saturado */
    color: hsl(220, 100%, 75%);  /* Azul mais claro */
    color: hsl(220, 100%, 25%);  /* Azul mais escuro */
}

/* HSLA: hsl(hue, saturation, lightness, alpha) */
.cores-hsla {
    background: hsla(220, 100%, 50%, 0.3); /* Azul transparente */
    background: hsla(0, 100%, 50%, 0.7);   /* Vermelho semi-transparente */
}
```

---

## 📏 Unidades de Medida CSS

### 📐 Unidades Absolutas

Têm tamanho fixo, independente de outros elementos:

```css
.unidades-absolutas {
    /* Pixels - unidade mais comum para telas */
    width: 300px;
    height: 200px;
    
    /* Pontos - principalmente para impressão */
    font-size: 12pt;
    
    /* Centímetros - para impressão */
    margin: 2cm;
    
    /* Milímetros - para impressão */
    border-width: 1mm;
    
    /* Polegadas - para impressão */
    padding: 0.5in;
}

/* Quando usar cada uma */
.uso-absolutas {
    /* Pixels: interfaces web, bordas, sombras */
    border: 1px solid #ccc;
    box-shadow: 2px 2px 4px rgba(0,0,0,0.2);
    
    /* Pontos: tamanhos de fonte para impressão */
    font-size: 11pt; /* Para documentos impressos */
}
```

### 📊 Unidades Relativas

Tamanho baseado em outros elementos ou contexto:

```css
/* Porcentagem - relativa ao elemento pai */
.unidades-porcentagem {
    width: 50%;      /* 50% da largura do pai */
    height: 100%;    /* 100% da altura do pai */
    margin: 10%;     /* 10% da largura do pai */
}

/* EM - relativa ao tamanho da fonte do elemento */
.unidades-em {
    font-size: 16px;
    padding: 1em;    /* 16px (1 × 16px) */
    margin: 0.5em;   /* 8px (0.5 × 16px) */
}

.elemento-filho {
    font-size: 1.5em; /* 24px (1.5 × 16px do pai) */
    padding: 1em;      /* 24px (1 × 24px próprio) */
}

/* REM - relativa ao tamanho da fonte do elemento raiz (html) */
.unidades-rem {
    /* Se html { font-size: 16px; } */
    font-size: 1rem;    /* 16px */
    font-size: 1.5rem;  /* 24px */
    font-size: 0.875rem; /* 14px */
    
    padding: 2rem;      /* 32px */
    margin: 1rem 0;     /* 16px 0 */
}

/* Viewport Units - relativas ao tamanho da janela */
.unidades-viewport {
    /* VW - Viewport Width */
    width: 100vw;    /* 100% da largura da janela */
    width: 50vw;     /* 50% da largura da janela */
    
    /* VH - Viewport Height */
    height: 100vh;   /* 100% da altura da janela */
    height: 50vh;    /* 50% da altura da janela */
    
    /* VMIN - Menor valor entre vw e vh */
    width: 50vmin;   /* 50% da menor dimensão */
    
    /* VMAX - Maior valor entre vw e vh */
    width: 50vmax;   /* 50% da maior dimensão */
}
```

### 🔧 Unidades Modernas

Unidades especializadas para casos específicos:

```css
.unidades-modernas {
    /* CH - largura do caractere "0" */
    width: 60ch;     /* Largura de 60 caracteres */
    max-width: 80ch; /* Ideal para legibilidade de texto */
    
    /* EX - altura da letra "x" minúscula */
    line-height: 2ex;
    
    /* FR - fração do espaço disponível (Grid) */
    grid-template-columns: 1fr 2fr 1fr;
    
    /* Funções calc() para cálculos */
    width: calc(100% - 20px);
    height: calc(100vh - 80px);
    margin: calc(1rem + 2px);
}
```

---

## 🎨 Teoria das Cores no Design

### 🔄 Círculo Cromático e Harmonias

```css
/* Cores Primárias */
.cores-primarias {
    --vermelho: hsl(0, 100%, 50%);
    --azul: hsl(240, 100%, 50%);
    --amarelo: hsl(60, 100%, 50%);
}

/* Cores Complementares (opostas no círculo) */
.esquema-complementar {
    --principal: hsl(220, 100%, 50%);  /* Azul */
    --complementar: hsl(40, 100%, 50%); /* Laranja */
}

/* Cores Análogas (próximas no círculo) */
.esquema-analogo {
    --cor1: hsl(200, 70%, 50%);  /* Azul-ciano */
    --cor2: hsl(220, 70%, 50%);  /* Azul */
    --cor3: hsl(240, 70%, 50%);  /* Azul-violeta */
}

/* Esquema Triádico (3 cores equidistantes) */
.esquema-triadico {
    --cor1: hsl(0, 70%, 50%);    /* Vermelho */
    --cor2: hsl(120, 70%, 50%);  /* Verde */
    --cor3: hsl(240, 70%, 50%);  /* Azul */
}

/* Esquema Monocromático (variações de uma cor) */
.esquema-monocromatico {
    --base: hsl(220, 70%, 50%);
    --claro: hsl(220, 70%, 80%);
    --medio: hsl(220, 70%, 50%);
    --escuro: hsl(220, 70%, 20%);
}
```

### ♿ Contraste e Acessibilidade

```css
/* WCAG Guidelines para contraste */
.contraste-acessivel {
    /* Nível AA: contraste mínimo 4.5:1 para texto normal */
    color: #212529;           /* Texto escuro */
    background-color: #ffffff; /* Fundo claro */
    
    /* Nível AA: contraste mínimo 3:1 para texto grande */
    color: #495057;           /* Cinza médio */
    background-color: #f8f9fa; /* Cinza claro */
    
    /* Nível AAA: contraste 7:1 para texto normal */
    color: #000000;           /* Preto */
    background-color: #ffffff; /* Branco */
}

/* Teste de contraste com variáveis */
:root {
    --texto-primario: #212529;
    --texto-secundario: #6c757d;
    --fundo-principal: #ffffff;
    --fundo-secundario: #f8f9fa;
    
    /* Verificar contraste em tools.webaim.org */
}
```

---

## ✅ Checklist de Aprendizado

### Cores
- [ ] Entender sistemas de cores (HEX, RGB, HSL)
- [ ] Aplicar teoria das cores em projetos
- [ ] Garantir contraste adequado para acessibilidade
- [ ] Criar paletas harmônicas
- [ ] Usar gradientes efetivamente

### Medidas
- [ ] Dominar unidades absolutas vs relativas
- [ ] Usar rem para tipografia
- [ ] Aplicar viewport units para responsividade
- [ ] Implementar calc() para cálculos dinâmicos
- [ ] Criar sistema de espaçamento consistente

### Design Responsivo
- [ ] Implementar abordagem mobile-first
- [ ] Usar unidades flexíveis apropriadas
- [ ] Criar breakpoints eficientes
- [ ] Aplicar clamp() para valores fluidos
- [ ] Otimizar para diferentes dispositivos

---

## 🎯 Próximos Passos

Após dominar este módulo, você estará pronto para:

1. **05-css-layout**: Flexbox e Grid para layouts complexos
2. **06-css-avancado**: Animações, transformações e efeitos
3. **Design Systems**: Criar sistemas de design escaláveis
4. **CSS-in-JS**: Integração com frameworks modernos

---

## 💡 Dicas Importantes

### ✅ Boas Práticas
- **Use variáveis CSS** para manter consistência
- **Prefira unidades relativas** para responsividade
- **Teste contraste** para garantir acessibilidade
- **Organize cores** em sistemas coerentes
- **Documente paletas** para reutilização

### 🎨 Ferramentas Úteis
- **Adobe Color**: Criação de paletas
- **Coolors.co**: Gerador de esquemas de cores
- **Contrast Ratio**: Teste de contraste
- **CSS Variables**: Suporte nativo do navegador
- **DevTools**: Inspeção e debugging

### ⚠️ Evite
- Usar muitas cores diferentes sem harmonia
- Depender exclusivamente de pixels
- Ignorar acessibilidade de contraste
- Não testar em diferentes dispositivos
- Criar sistemas inconsistentes

---

🎨 **Lembre-se**: Cores e medidas são a base visual de qualquer design. Dominar estes conceitos é essencial para criar interfaces bonitas, funcionais e acessíveis!