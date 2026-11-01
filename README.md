# siteiaagroassessor

Site de marketing do **IA AgroAssessor**, gestão da fazenda pelo Telegram com inteligência artificial.

É uma página estática única (`index.html`), sem build. Para ver localmente, abra o arquivo no navegador.

Publicação: hospedagem da HostGator em https://iaagroassessor.com.br (veja abaixo). O GitHub Pages não é usado.

## Deploy na HostGator

Todo push na branch `main` envia o site por FTP para a hospedagem (workflow `.github/workflows/deploy-hostgator.yml`). Também dá para rodar à mão em **Actions → Deploy na HostGator → Run workflow**.

Configure em **Settings → Secrets and variables → Actions**:

| Nome | Tipo | Valor |
|---|---|---|
| `FTP_SERVER` | Secret | servidor FTP da HostGator (ex.: `ftp.seudominio.com.br`) |
| `FTP_USERNAME` | Secret | usuário FTP do cPanel |
| `FTP_PASSWORD` | Secret | senha desse usuário |
| `FTP_SERVER_DIR` | Variable (opcional) | pasta no servidor, com `/` no fim. Padrão: `public_html/` |

Se o domínio for um domínio adicional no cPanel, use a pasta dele (ex.: `public_html/iaagroassessor.com.br/`).

## Google e buscadores (SEO)

- `robots.txt` libera o site para todos os robôs (Google, Bing e assistentes de IA) e aponta o `sitemap.xml`.
- `sitemap.xml` lista as páginas. Ao criar uma página nova, inclua ela ali e atualize o `lastmod`.
- Cada página tem `<link rel="canonical">` com o endereço oficial `https://iaagroassessor.com.br/...`, título, descrição, Open Graph (prévia no WhatsApp) e dados estruturados JSON-LD.
- O site é acompanhado no Google Search Console (propriedade de domínio `iaagroassessor.com.br`).
