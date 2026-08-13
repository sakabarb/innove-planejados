# Innove Móveis Planejados

Site institucional de página única da Innove Móveis Planejados — Florianópolis/SC.

## Stack

HTML único, com CSS e JavaScript embutidos no próprio arquivo. Sem framework, sem
build step e sem dependências externas além do Google Fonts.

## Estrutura

```
public/                       # raiz publicada (outputDirectory na Vercel)
  index.html                  # o site inteiro
  favicon.svg                 # ícone derivado da logo
  apple-touch-icon.png        # gerado a partir de logo.png
  og-image.jpg                # imagem de compartilhamento (1200x630)
  logo.png                    # logo original; a do site é recriada em SVG inline
  images/                     # fotos dos projetos
vercel.json
```

Duas imagens têm versão recortada, usada no lugar da original:

| Original | Recorte | Motivo |
| --- | --- | --- |
| `hero-painel-ripado.jpg` | `hero-painel-ripado-topo.jpg` | a parte de baixo tem uma bancada com recorte inacabado |
| `cozinha-branca-l.jpg` | `cozinha-branca-l-topo.jpg` | a parte de baixo tem objetos soltos e cadeiras |

Os arquivos originais continuam no repositório.

## Rodar localmente

```bash
python3 -m http.server 4321 --directory public
```

## Dados pendentes

O site não inventa informação. Onde falta dado real há um comentário
`<!-- INSERIR: ... -->` no ponto exato do `index.html`:

- número do endereço
- horário de abertura e dias de funcionamento
- prazo médio de produção e entrega
- e-mail comercial

## Deploy

Vercel, a partir da branch `main`. A pasta publicada é `public/`, definida em
`vercel.json`.
