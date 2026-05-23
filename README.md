# IMC v12 — Fertilizantes (Cloud)

Sistema de Formulação de Fertilizantes como Progressive Web App (PWA), com interface mobile-first, tema escuro moderno e back-end em nuvem via Supabase.

---

## Funcionalidades

| Módulo | Descrição |
|---|---|
| **Formulação** | Criação e otimização de fórmulas de fertilizantes com solver automático |
| **Cotação** | Geração de cotações de preço por fórmula e por matéria-prima isolada |
| **Análise de Proposta** | Avaliação completa de propostas comerciais com composição de custo |
| **Composição** | Visualização detalhada da composição nutricional das fórmulas |
| **Materiais** | Cadastro e gerenciamento de matérias-primas com preços históricos |
| **Fábricas** | Gerenciamento de múltiplas fábricas com estoque individual |
| **Dashboard** | KPIs, gráficos de histórico de preços e comparativos |
| **Relatórios** | Geração de relatórios e exportação de dados |
| **Rotas Marítimas NPK** | Visualização geográfica de rotas marítimas via TopoJSON |
| **Arquivo** | Banco de dados de cotações e propostas salvas |
| **Configurações** | Preferências do sistema e gerenciamento de conta |

---

## Nutrientes Monitorados

| Macronutrientes | Micronutrientes |
|---|---|
| N, P, K, S, Cl, Ca | Mg, B, Cu, Zn, Mn, Fe, Mo |

Cada nutriente suporta definição de faixas mínimas e máximas com análise de custo associado.

---

## Stack Tecnológica

**Frontend**
- HTML5 + CSS3 + Vanilla JavaScript (ES6+)
- Design responsivo mobile-first com glassmorphism
- Tema escuro (`#0a0e1a`) com acento verde (`#10d59c`)

**Bibliotecas**
- [Chart.js 4.4.1](https://www.chartjs.org/) — gráficos e visualizações
- [TopoJSON Client 3](https://github.com/topojson/topojson-client) — mapas geográficos
- [SheetJS](https://sheetjs.com/) — importação de planilhas Excel (100% local)

**Back-end / Cloud**
- [Supabase](https://supabase.com/) — autenticação e banco de dados PostgreSQL
- API de câmbio em tempo real (USD → BRL)
- API do Banco Central do Brasil

**IA**
- Google Gemini Vision — importação de preços via imagem e PDF

---

## Importação de Preços

O sistema suporta três formas de importar preços de matérias-primas:

1. **Planilha Excel (.xlsx)** — via SheetJS, processado localmente no browser
2. **Imagem** — via Google Gemini Vision API (gratuito)
3. **PDF** — via PDF.js + canvas + Gemini Vision

---

## Autenticação

Login com e-mail e senha via Supabase Auth. Sessão persistida em `localStorage` com refresh automático de token.

---

## Como Usar

1. Acesse a URL da aplicação ou abra o `index.html` diretamente no browser
2. Faça login com sua conta Supabase
3. Configure suas fábricas e materiais em **Fábricas** e **Materiais**
4. Crie fórmulas em **Formulação** e gere cotações em **Cotação**

> Para instalar como PWA: no browser mobile, use "Adicionar à tela inicial"

---

## Configuração do Supabase

No arquivo `index.html`, substitua as variáveis pelo seu projeto:

```js
const SUPABASE_URL = 'https://seu-projeto.supabase.co/';
const SUPABASE_ANON_KEY = 'sua-anon-key';
```

Valores encontrados em: **Supabase → Project Settings → API**
