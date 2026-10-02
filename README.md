# siteiaagroassessor

Site de marketing do **IA AgroAssessor**, gestão da fazenda pelo Telegram com inteligência artificial.

É uma página estática única (`index.html`), sem build. Para ver localmente, abra o arquivo no navegador.

Publicação: GitHub Pages, a partir da branch `main` (pasta raiz).

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
