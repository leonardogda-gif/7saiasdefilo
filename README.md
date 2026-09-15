# 7 Saias de Filó

Site do ateliê 7 Saias de Filó: catálogo de saias infantis (dia a dia e ocasiões especiais) e uma área interna para gerenciar os produtos.

## Estrutura

```
7saiasdefilo/
├── index.html      # site inteiro (HTML + CSS + JS, sem dependências de build)
└── assets/         # pasta reservada para fotos reais dos produtos
```

## Como usar

O site é um único arquivo HTML autocontido — não precisa de build, servidor ou instalação. Basta hospedar o `index.html`.

### Acesso ao ateliê (gerenciar produtos)

No menu, clique em **atelier**. Senha padrão: `filo7` (trocar diretamente no código, constante `ADMIN_CODE` no `index.html`, antes de publicar de verdade).

**Importante:** por enquanto, os produtos cadastrados ficam salvos apenas no navegador de quem está usando (localStorage). Isso significa que cada pessoa/dispositivo vê seus próprios cadastros — não há sincronização entre navegadores ainda. Isso será resolvido quando o backend (Cloudflare Worker) for integrado.

### Link de pagamento (Asaas)

Ao cadastrar ou editar uma saia, é possível colar um link de pagamento do Asaas no campo correspondente. Quando presente, o botão "comprar agora" da página do produto abre esse link diretamente.

## Publicando no GitHub Pages (gratuito)

1. Crie um repositório novo no GitHub e suba estes arquivos.
2. Vá em **Settings → Pages**.
3. Em "Source", selecione a branch principal (`main`) e a pasta `/root`.
4. Salve — o GitHub gera uma URL do tipo `https://seu-usuario.github.io/nome-do-repo/`.

## Próximos passos

- Substituir as ilustrações de saias (SVG) por fotos reais dentro de `assets/`.
- Integração com Cloudflare Worker para: produtos persistidos em servidor (não mais localStorage) e checkout real via API do Asaas.
