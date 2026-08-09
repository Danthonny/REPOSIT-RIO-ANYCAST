# Repositório Anycast — sites da Boske

Hospedagem estática dos sites e páginas produzidos pela agência.
Publicado automaticamente na **Netlify** a cada `push` na branch `main`.

**No ar:** https://boskeag.netlify.app

## Como funciona

A **raiz é o site da Boske**. Cada pasta adicional vira um endereço próprio:

```
/index.html        →  /            site institucional da Boske
/sites/index.html  →  /sites/      índice interno dos sites publicados
/<cliente>/        →  /<cliente>/  novos sites entram assim
```

Nada é compilado — é HTML/CSS/JS estático. O `netlify.toml` define
`publish = "."`, cabeçalhos de segurança e cache (HTML sempre revalidado,
para o cliente nunca ver uma versão velha), além de um redirect 301 de
`/boske/*` para a raiz (endereço antigo).

## Publicar um site novo

1. Criar a pasta na raiz com um `index.html` dentro.
2. Adicionar o card correspondente em `sites/index.html`.
3. `git add . && git commit && git push` — a Netlify publica em ~20s.

## Sites

| Endereço | Site | Situação |
|---|---|---|
| `/` | Site institucional da agência Boske | No ar |
| `/sites/` | Índice interno | No ar |

## Domínio

O endereço atual é o subdomínio gratuito da Netlify, com HTTPS automático.
Para usar domínio próprio: **Site configuration → Domain management → Add
domain** e apontar o DNS no registrador.
