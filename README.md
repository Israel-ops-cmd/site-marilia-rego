# Site Dra. Marília Rêgo

Site estático (HTML, CSS e JS num único `index.html`), sem etapa de build. Publicado pelo GitHub na Vercel.

## Rodar localmente

```bash
cd "Site - Marília Rêgo/site"
python -m http.server 8000
```

Abra http://localhost:8000. (Abrir o `index.html` direto no navegador também funciona, mas o servidor local é mais fiel ao site no ar.)

## Estrutura

- `index.html`: página inteira, com CSS e JS embutidos.
- `img/`: fotos em webp. Fotos com fundo em 800 px e no tamanho original (cerca de 1100 px); recortes em 700 px e no tamanho original.
- `vendor/`: GSAP 3.12.5, ScrollTrigger 3.12.5 e Lenis 1.1.13, servidos pelo próprio site.
- `favicon.svg`, `apple-touch-icon.png`: monograma da logo vetorizado.
- `og-image.jpg`: prévia do link no WhatsApp (1200 x 630).
- `vercel.json`: `cleanUrls` e cache longo para `/img` e `/vendor`.

## Publicar

Cada push na branch `main` publica sozinho na Vercel.
Na primeira vez: Vercel > Add New > Project > importar o repositório, Framework Preset: Other, Build Command vazio, Output Directory `./`.

Depois de saber a URL final, troque `site-marilia-rego.vercel.app` pela URL real no `index.html` (canonical, og:url, og:image, twitter:image e Schema.org).

## Trocar uma foto

Gere o webp com o mesmo nome e as mesmas larguras (ex.: `img/02-sobre-800.webp` e `img/02-sobre-1086.webp`). Se mudar a largura, ajuste o `srcset`, `width` e `height` da imagem no `index.html`.
