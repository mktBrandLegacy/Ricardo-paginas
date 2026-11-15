# Brand Legacy — App Meta

Site estático com as páginas exigidas pela Meta para o app do Facebook/Instagram.

| Página | Caminho |
|---|---|
| Início (rodapé com razão social, CNPJ, contato e links) | `/` |
| Política de Privacidade | `/politica-de-privacidade/` |
| Exclusão de Dados | `/exclusao-de-dados/` |
| Termos de Uso | `/termos-de-uso/` |

## Antes de publicar: preencher os dados

Substitua em todos os arquivos `.html`:

- `[CNPJ]` → CNPJ (ex.: 00.000.000/0001-00)

```bash
grep -rl '\[CNPJ\]' --include=*.html . | xargs sed -i 's#\[CNPJ\]#00.000.000/0001-00#g'
```

## Publicação

Os links são relativos, então funciona tanto em subdomínio quanto em pasta:

- **Subdomínio** `https://appmeta.brandlegacy.com.br` → enviar o conteúdo deste repositório para a raiz do subdomínio.
- **Pasta** `https://brandlegacy.com.br/appmeta/` → enviar o conteúdo para a pasta `appmeta/` do site.

Requisitos da Meta: HTTPS ativo (SSL), acesso sem login, mesmo domínio informado no app.

URLs para cadastrar em developers.facebook.com › App › Configurações › Básico:

- URL da Política de Privacidade: `https://appmeta.brandlegacy.com.br/politica-de-privacidade/`
- URL dos Termos de Serviço: `https://appmeta.brandlegacy.com.br/termos-de-uso/`
- URL de instruções de exclusão de dados: `https://appmeta.brandlegacy.com.br/exclusao-de-dados/`
- Domínio do app: `appmeta.brandlegacy.com.br`

## Cookies

O site não usa Pixel nem Analytics, por isso não tem aviso de cookies. Se for adicionar algum, inclua um banner de consentimento e atualize a seção 7 da Política de Privacidade.
