# Repositório Anycast — sites da Boske

Hospedagem estática dos sites e páginas produzidos pela agência.
Publicado automaticamente na **Netlify** a cada `push` na branch `main`.

## Como funciona

Cada **pasta na raiz** vira um endereço público:

```
/index.html      →  /            (hub com a lista de sites)
/boske/          →  /boske/      (site institucional da Boske)
/<cliente>/      →  /<cliente>/  (novos sites entram assim)
```

Nada é compilado — é HTML/CSS/JS estático. O `netlify.toml` define
`publish = "."` e cabeçalhos de segurança + cache (HTML sempre revalidado,
para o cliente nunca ver uma versão velha).

## Publicar um site novo

1. Criar a pasta na raiz com um `index.html` dentro.
2. Adicionar o card correspondente no `index.html` da raiz.
3. `git add . && git commit && git push` — a Netlify publica em ~20s.

## Sites

| Pasta | Site | Situação |
|---|---|---|
| `boske/` | Site institucional da agência Boske | No ar |

## Domínio

O endereço padrão é o subdomínio gratuito da Netlify (`*.netlify.app`),
com HTTPS automático. Para usar domínio próprio: **Site settings → Domain
management → Add domain** e apontar o DNS no registrador.
