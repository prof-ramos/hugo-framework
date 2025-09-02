---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: true
description: "Descrição breve do post que aparece nos resultados de busca"
slug: "{{ .Name }}"
author: "Seu Nome"
tags: ["tag1", "tag2", "tag3"]
categories: ["Categoria"]
series: ["Nome da Série"] # Opcional - para posts em série
keywords: ["palavra-chave1", "palavra-chave2", "palavra-chave3"]
cover:
  image: "/images/posts/{{ .Name }}/cover.jpg" # Imagem de capa
  alt: "Descrição da imagem de capa"
  caption: "Legenda da imagem (opcional)"
  relative: false
toc: true # Ativa sumário automático
showToc: true
TocOpen: false
hidemeta: false
disableShare: false
showbreadcrumbs: true
comments: true # Ativa comentários
math: false # Para posts matemáticos
mermaid: false # Para diagramas mermaid
---

<!-- 
INSTRUÇÕES PARA USAR ESTE TEMPLATE:

1. Substitua todos os valores entre colchetes []
2. Remova esta seção de comentários antes de publicar
3. Use markdown para formatar seu conteúdo
-->

# Introdução

Escreva uma introdução atraente que explique o que os leitores vão aprender neste post.

## Pré-requisitos

- Item 1 necessário
- Item 2 necessário
- Item 3 necessário

## O que vamos cobrir

1. [Tópico 1](#tópico-1)
2. [Tópico 2](#tópico-2) 
3. [Tópico 3](#tópico-3)

---

# Tópico 1

Conteúdo do primeiro tópico principal.

## Subtítulo

Texto explicativo com **negrito**, *itálico*, e `código inline`.

### Listas

Lista ordenada:
1. Primeiro item
2. Segundo item
3. Terceiro item

Lista não ordenada:
- Item A
- Item B
- Item C

### Código

```python
# Exemplo de código Python
def hello_world():
    print("Hello, World!")
    
hello_world()
```

### Imagens

![Descrição da imagem](/images/posts/{{ .Name }}/exemplo.jpg)

### Links

[Texto do link](https://exemplo.com)

### Tabelas

| Coluna 1 | Coluna 2 | Coluna 3 |
|----------|----------|----------|
| Dado 1   | Dado 2   | Dado 3   |
| Dado 4   | Dado 5   | Dado 6   |

---

# Tópico 2

Conteúdo do segundo tópico principal.

## Blocos de destaque

{{< admonition type="note" title="Nota importante" open=true >}}
Este é um bloco de nota usando shortcode do PaperMod.
{{< /admonition >}}

{{< admonition type="warning" title="Atenção" >}}
Este é um aviso importante.
{{< /admonition >}}

---

# Tópico 3

Conteúdo do terceiro tópico principal.

## Vídeos do YouTube

{{< youtube id="VIDEO_ID" >}}

## Tweets

{{< tweet user="twitteruser" id="123456789" >}}

---

# Conclusão

Resuma os principais pontos aprendidos e forneça próximos passos.

## Pontos-chave

- Ponto importante 1
- Ponto importante 2  
- Ponto importante 3

## Próximos passos

- [ ] Tarefa 1 para continuar aprendendo
- [ ] Tarefa 2 para prática
- [ ] Tarefa 3 para aprofundamento

## Recursos adicionais

- [Link para documentação](https://exemplo.com/docs)
- [Livro recomendado](https://exemplo.com/livro)
- [Curso relacionado](https://exemplo.com/curso)

---

**Gostou deste post?** Deixe um comentário abaixo com suas dúvidas ou sugestões!

*Publicado em {{ .Date | time.Format "02/01/2006" }} por {{ .Author }}*
