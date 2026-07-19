# LP Nuvem Rush

Landing page do **Nuvem Rush** — plataforma de automação de pós-venda para lojas **Nuvemshop**, com WhatsApp Business API oficial, e-mail marketing e recuperação de clientes.

## 🔗 Links

- **Produto (app):** [nuvem-rush.vercel.app](https://nuvem-rush.vercel.app)
- **Instalar na Nuvemshop:** `https://www.tiendanube.com/apps/34663/authorize`

## 📄 Sobre esta página

Página de marketing única e autossuficiente (`index.html`) — HTML + CSS, sem build nem dependências. Fontes Sora/Inter via Google Fonts. Seções:

- Hero + problema (recompra / retenção)
- Como funciona em 3 passos (instalar → conectar WhatsApp → ativar)
- Recursos (confirmação de pedido, rastreio, recuperação de carrinho, cupom de recompra, e-mail marketing, base de contatos)
- Tecnologia (APIs oficiais), preço, FAQ e CTA final

## 🚀 Rodar localmente

Como é um arquivo estático único, basta abrir o `index.html` no navegador. Para servir localmente:

```bash
npx serve .
# ou
python -m http.server 8000
```

## ☁️ Deploy

Site estático — publica direto na **Vercel**, **Netlify** ou **GitHub Pages** apontando para a raiz do repositório (nenhum comando de build necessário).

## 🗂️ Estrutura

```
.
├── index.html   # a landing page inteira (HTML + CSS inline)
└── README.md
```

## ✅ Pendências antes de publicar

- [ ] Trocar o **número de WhatsApp placeholder** (`wa.me/5514999999999`) pelo número real (aparece em 3 CTAs).
- [ ] Alinhar a copy ao que o produto já entrega hoje: o app faz **e-mail + rastreio no WhatsApp**; recursos como recuperação de carrinho ainda são "em breve" — deixar claro o que é beta.
- [ ] Revisar links (`conectweb.online`, `contato@conectweb.online`).

## 📦 Projeto relacionado

O aplicativo em si (Next.js + Firebase, app incorporado à Nuvemshop) fica em outro repositório: [`nuvem-rush`](https://github.com/niltinhoapp/nuvem-rush).
