# CLAUDE.md — expert-integrado.github.io

> Este repo e PUBLICO. Nada aqui (paginas, commits, este arquivo) pode conter segredo, token, telefone, ID de infraestrutura, dado pessoal ou nome de cliente. Auditar antes de cada push.

## Objetivo em 1 linha

Hub de paginas publicas dos projetos da Expert Integrado, servido pelo GitHub Pages da org em `https://expert-integrado.github.io/`.

## Como funciona

- Projeto com **repo publico** hospeda a propria pagina no `docs/` dele mesmo — nao entra aqui (ex.: expert-brain).
- Projeto com **repo privado** ganha uma pasta aqui (`<projeto>/index.html`) e a pagina sai em `https://expert-integrado.github.io/<projeto>/` — mesma URL que teria se o Pages fosse do proprio repo.
- A raiz (`index.html`) e o indice: um card por projeto, com classe de cor propria (`.proj-<slug>`).
- Nao ha build, framework nem dependencia: cada pagina e um `index.html` autocontido (CSS e SVG inline), em portugues com acentuacao correta, tema escuro seguindo o padrao visual da raiz.

## Fluxo de pagina nova (3 passos, sempre juntos)

1. Pasta nova `<projeto>/index.html` seguindo o padrao visual das paginas existentes.
2. Card no `index.html` da raiz (com a classe de hover/cor do projeto).
3. Link pra pagina no README do repo do projeto de origem.

## Regras que nao se negociam

- **Conteudo 100% publico.** Nenhum segredo, chave, ID de projeto de infraestrutura, telefone, e-mail pessoal, path de maquina ou nome de cliente. Vale pro conteudo das paginas E pro historico de commits.
- **Pagina descreve o que o projeto FAZ, nunca como acessa-lo por dentro** (sem URL interna, sem instrucao que dependa de credencial — excecao: instrucao de autoatendimento pensada pro usuario final, como a central de ajuda).
- **Fidelidade ao produto real.** Pagina de projeto reflete o estado atual (tools, features, limites); atualizacao do produto que muda a superficie publica = atualizar a pagina junto.
- Escopo e so vitrine/explicacao: codigo dos projetos vive nos repos de origem, nunca aqui.

## Gotchas

- O GitHub Pages serve direto da branch `main`, raiz do repo — push na main JA E publicacao. Nao existe preview: conferir o HTML localmente no navegador antes do push.
- Cache do Pages leva alguns minutos pra propagar apos o push.
- Os cards da raiz usam CSS por slug (`.proj-<slug>:hover` e `.proj-<slug> .go`): card novo sem essas 2 regras fica sem identidade de cor.
