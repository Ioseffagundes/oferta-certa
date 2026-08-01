# Oferta Certa — Landing Page

Landing page do grupo VIP de WhatsApp **Oferta Certa** (ofertas p/ mulheres econômicas).

- Site estático (HTML/CSS/JS puro, sem build)
- Botão de CTA com animação de pulo apontando para o grupo do WhatsApp
- Toast animado no rodapé simulando pessoas entrando no grupo
- Fonte Nunito auto-hospedada em `assets/fonts/`

## Deploy

Publicado via **GitHub Pages** pela branch `gh-pages` (arquivo `CNAME` define o domínio `oferta-certa.racka.com.br`).

Para atualizar o site: altere os arquivos, faça merge para a `gh-pages` e push.

## DNS

Para o subdomínio funcionar, é necessário um registro no DNS da zona `racka.com.br`:

| Tipo  | Nome           | Destino                  | Proxy            |
|-------|----------------|--------------------------|------------------|
| CNAME | `oferta-certa` | `ioseffagundes.github.io` | Desativado (DNS only) |

O certificado HTTPS é emitido automaticamente pelo GitHub Pages após a propagação do DNS
(ative "Enforce HTTPS" nas configurações de Pages do repositório quando disponível).
