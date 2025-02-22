

# Tags de metadados **Open Graph (OG)**

Essas que são usadas para melhorar a maneira como o conteúdo de uma página web é exibido quando compartilhado em redes sociais como Facebook, LinkedIn e outras.

### 1. **`<meta property="og:title" content="...">`**

- **Descrição**: Define o título da página quando ela é compartilhada nas redes sociais.
- **Uso**: O título deve ser claro e conciso, refletindo o conteúdo da página. Geralmente, é o título principal ou o nome do artigo ou página.
- **Exemplo**: 
  ```html
  <meta property="og:title" content="Guia Completo de SEO: Melhore sua Visibilidade Online">
  ```

### 2. **`<meta property="og:description" content="...">`**

- **Descrição**: Fornece uma breve descrição do conteúdo da página. Essa descrição é exibida junto com o título e a imagem ao compartilhar o link nas redes sociais.
- **Uso**: A descrição deve ser envolvente e fornecer um resumo claro sobre o que o usuário encontrará ao acessar o link. O objetivo é atrair o interesse do usuário para clicar no link.
- **Exemplo**: 
  ```html
  <meta property="og:description" content="Aprenda como otimizar seu site para os motores de busca e aumentar sua visibilidade com técnicas de SEO comprovadas.">
  ```

### 3. **`<meta property="og:image" content="...">`**

- **Descrição**: Especifica a URL de uma imagem que será exibida ao compartilhar o link nas redes sociais. Imagens visualmente atraentes aumentam as chances de engajamento.
- **Uso**: A imagem deve ser relevante ao conteúdo da página e de alta qualidade. Algumas plataformas, como o Facebook, recomendam imagens com dimensões mínimas de 1200x630 pixels para uma visualização ideal.
- **Exemplo**: 
  ```html
  <meta property="og:image" content="https://exemplo.com/imagem-seo.jpg">
  ```

### 4. **`<meta property="og:url" content="...">`**

- **Descrição**: Define a URL canônica da página. É importante quando você tem conteúdo duplicado ou múltiplos links para a mesma página. Isso ajuda as redes sociais a identificar a versão correta do link para ser compartilhada.
- **Uso**: O valor dessa tag deve ser a URL final e definitiva que você deseja que seja associada ao conteúdo, independentemente de redirecionamentos ou URLs alternativas.
- **Exemplo**: 
  ```html
  <meta property="og:url" content="https://exemplo.com/seo-guia-completo">
  ```

### 5. **`<meta property="og:type" content="...">`**

- **Descrição**: Define o tipo de conteúdo que está sendo compartilhado. Isso ajuda as redes sociais a entender melhor o conteúdo e exibi-lo de maneira adequada. Os tipos mais comuns incluem "website", "article", "video", entre outros.
- **Uso**: Se a página for um artigo, use `article`; se for um site geral, use `website`; se for um vídeo, use `video`.
- **Exemplo**:
  ```html
  <meta property="og:type" content="article">
  ```

### 6. **`<meta property="og:site_name" content="...">`**

- **Descrição**: Informa o nome do site que está sendo compartilhado. Essa informação é exibida nas plataformas sociais junto com o título e a descrição.
- **Uso**: O nome do site é geralmente o nome da sua marca ou o título da sua plataforma.
- **Exemplo**:
  ```html
  <meta property="og:site_name" content="Exemplo Site">
  ```

### 7. **`<meta property="og:locale" content="...">`**

- **Descrição**: Define o idioma e a região do conteúdo. Isso ajuda a garantir que o conteúdo seja exibido corretamente para os usuários de diferentes regiões ou que falam diferentes idiomas.
- **Uso**: Utilize o código de idioma seguido pelo código de região (por exemplo, `pt_BR` para português do Brasil, `en_US` para inglês dos EUA).
- **Exemplo**:
  ```html
  <meta property="og:locale" content="pt_BR">
  ```

### 8. **`<meta property="og:audio" content="...">`** (opcional)

- **Descrição**: Fornece a URL de um arquivo de áudio relacionado ao conteúdo, se aplicável. Pode ser usado para podcasts ou conteúdos em áudio.
- **Uso**: Se o conteúdo da página for principalmente em formato de áudio, você pode usar essa tag para incluir o link.
- **Exemplo**:
  ```html
  <meta property="og:audio" content="https://exemplo.com/audio-podcast.mp3">
  ```

### 9. **`<meta property="og:video" content="...">`** (opcional)

- **Descrição**: Define a URL de um vídeo associado à página. Essa tag é útil para páginas que apresentam vídeos e desejam que eles sejam exibidos ao lado do conteúdo nas redes sociais.
- **Uso**: Como o conteúdo em vídeo é cada vez mais popular, essa tag pode aumentar o engajamento quando compartilhado nas plataformas sociais.
- **Exemplo**:
  ```html
  <meta property="og:video" content="https://exemplo.com/video-tutorial.mp4">
  ```

### 10. **`<meta property="og:determiner" content="...">`** (opcional)

- **Descrição**: Determina a forma gramatical de uma frase ao compartilhar o conteúdo. Por exemplo, você pode escolher entre "a", "an", "the" para idiomas como inglês, onde o determinante é importante.
- **Uso**: Essencial para ajustar como o título será exibido em diferentes contextos linguísticos.
- **Exemplo**:
  ```html
  <meta property="og:determiner" content="a">
  ```

### Conclusão:
As tags **Open Graph** são essenciais para otimizar a maneira como o conteúdo de uma página é exibido nas redes sociais. Elas permitem que você controle o título, a descrição, a imagem e outros aspectos do compartilhamento, garantindo que a página seja apresentada da maneira mais atraente e envolvente possível para os usuários. Usar essas tags corretamente pode aumentar significativamente o engajamento nas redes sociais e melhorar a visibilidade do seu conteúdo.