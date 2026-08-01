# Oferta Certa — Landing Page

Landing page do grupo VIP de WhatsApp **Oferta Certa** (ofertas p/ mulheres econômicas), no ar em **https://oferta-certa.racka.com.br**.

- Site estático em um único `index.html` (CSS/JS embutidos, sem build e sem dependências externas)
- Botão de CTA com animação de pulo + brilho, apontando para o grupo do WhatsApp
- Toast flutuante simulando pessoas entrando no grupo (nomes em rotação a cada ~4s)
- Contador de vagas decrescendo em loop, sincronizado com o toast
- Fonte Nunito (variável) auto-hospedada; imagens em WebP

## Estrutura

```
index.html                  página completa (HTML + CSS + JS)
CNAME                       domínio customizado do GitHub Pages
assets/
  avatar-pop.webp           personagem central com efeito pop-out (44 KB)
  stores.webp               logos das lojas parceiras (7 KB)
  og.jpg                    imagem de compartilhamento (Open Graph)
  favicon.png               ícone da aba
  fonts/nunito-var*.woff2   Nunito variável (normal e itálico)
```

## Deploy

Publicado via **GitHub Pages** pela branch `gh-pages` (build clássico por branch; o arquivo `CNAME` define o domínio). Qualquer push na `gh-pages` publica automaticamente em ~1 minuto.

Para atualizar: edite os arquivos, commit e:

```bash
git push origin gh-pages
```

## DNS

Registro na zona `racka.com.br` (Cloudflare):

| Tipo  | Nome           | Destino                   | Proxy                 |
|-------|----------------|---------------------------|-----------------------|
| CNAME | `oferta-certa` | `ioseffagundes.github.io` | Desativado (DNS only) |

O certificado HTTPS é emitido automaticamente pelo GitHub Pages; ative "Enforce HTTPS" nas configurações de Pages do repositório quando disponível.
