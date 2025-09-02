# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Projeto

Site Hugo com tema PaperMod configurado em português brasileiro para blog/site pessoal. O projeto usa o tema PaperMod como submódulo Git e está configurado para deploy na Vercel.

## Comandos de Desenvolvimento

### Desenvolvimento Local
- `hugo server -D` - Executa servidor local com drafts em http://localhost:1313 (live reload automático)
- `hugo server` - Executa servidor local sem drafts
- `git submodule update --init --recursive` - Inicializa/atualiza submódulo PaperMod (necessário após clone)

### Build e Deploy
- `hugo` - Gera site estático na pasta `public/`
- `hugo --gc --minify` - Build otimizado com garbage collection e minificação
- `hugo version` - Verifica versão (requer Hugo Extended >= v0.146.0 para PaperMod)

### Criação de Conteúdo
- `hugo new posts/nome-do-post.md` - Cria novo post usando archetype `archetypes/post.md`
- `hugo new about/_index.md` - Cria nova página de seção

## Arquitetura e Estrutura

### Configuração Principal
- `config.toml` - Configuração principal do site com:
  - Idioma: português brasileiro (`pt-br`)
  - Tema: PaperMod com profile mode ativado
  - Menus: Posts, Sobre, Contato
  - SEO e meta tags configurados
  - Ícones sociais (GitHub, Twitter, LinkedIn)

### Estrutura de Conteúdo
- `content/_index.md` - Página inicial
- `content/posts/` - Posts do blog
- `content/about/` - Página sobre
- `content/contact/` - Página de contato
- `archetypes/post.md` - Template completo para novos posts com front matter TOML

### Tema e Customização
- `themes/PaperMod/` - Submódulo Git do tema PaperMod
- `static/images/` - Assets estáticos (imagens servidas em `/images/`)
- Layout personalizado: usar `layouts/` na raiz (não editar arquivos do tema)
- Assets personalizados: usar `assets/` na raiz

### Front Matter Padrão
Posts usam TOML com campos específicos:
- Metadados básicos: `title`, `date`, `draft`, `description`, `slug`, `author`
- SEO: `tags`, `categories`, `keywords`  
- Imagem de capa: `cover.image`, `cover.alt`, `cover.caption`
- Funcionalidades: `toc`, `showToc`, `comments`, `math`, `mermaid`

## Convenções de Código

### Nomenclatura
- Arquivos de conteúdo: kebab-case minúsculo (`meu-primeiro-post.md`)
- Imagens: organizadas em `static/images/posts/nome-do-post/`
- URLs: seguem estrutura de pastas (`/posts/nome-do-post/`)

### Markdown
- Usar headings `#` hierárquicos
- Quebras de linha razoáveis para legibilidade
- Código inline com `` `código` ``
- Blocos de código com syntax highlighting
- Imagens com alt text descritivo

### Shortcodes Disponíveis
PaperMod oferece shortcodes para:
- `{{< youtube id="VIDEO_ID" >}}` - Embeds do YouTube  
- `{{< tweet user="usuario" id="123456789" >}}` - Embeds do Twitter
- `{{< admonition type="note|warning|info" title="Título" >}}` - Blocos de destaque

## Deploy e Hospedagem

Configurado para Vercel (conforme README), mas compatível com:
- GitHub Pages
- Netlify  
- Cloudflare Pages
- Qualquer host de arquivos estáticos

## Validação

Antes de commits:
- Executar `hugo --gc --minify` para verificar build
- Verificar console para warnings (i18n, templates não utilizados)
- Testar responsividade com `hugo server`
- Validar links internos e imagens