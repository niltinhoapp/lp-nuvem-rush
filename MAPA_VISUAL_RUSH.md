# MAPA VISUAL E EVIDÊNCIAS DE INTERFACE — NUVEM RUSH

**Projeto:** Nuvem Rush (`nuvemrush.com.br` / `rush.com.br`)  
**Data da Auditoria Visual:** 16 de Novembro de 2026  
**Fase:** Fase 2A — Mapeamento Visual e Evidências Responsivas  
**Diretório de Evidências:** [`d:\projetos\lp-nuvem-rush\evidencias\`](file:///d:/projetos/lp-nuvem-rush/evidencias/)  
**Status:** Mapeamento visual estático e responsivo concluído sem modificação de código  

---

## 1. Galeria de Capturas Responsivas Efetivas

Todas as capturas foram produzidas através de automação com o motor Chromium (Google Chrome Headless), simulando as condições reais de renderização nas quatro resoluções obrigatórias:

| Identificador | Resolução | Dispositivo / Contexto | Arquivo de Evidência | Tamanho |
| :--- | :--- | :--- | :--- | :--- |
| **RESP-01** | **1440 × 900 px** | Desktop Padrão (Monitor Wide) | [01_desktop_1440x900.png](file:///d:/projetos/lp-nuvem-rush/evidencias/01_desktop_1440x900.png) | 1.40 MB |
| **RESP-02** | **1366 × 768 px** | Notebook Corporativo / Laptop | [02_notebook_1366x768.png](file:///d:/projetos/lp-nuvem-rush/evidencias/02_notebook_1366x768.png) | 1.10 MB |
| **RESP-03** | **390 × 844 px** | Smartphone Padrão (iPhone 13/14/15/16) | [03_mobile_390x844.png](file:///d:/projetos/lp-nuvem-rush/evidencias/03_mobile_390x844.png) | 434 KB |
| **RESP-04** | **360 × 800 px** | Smartphone Compacto (Android Standard) | [04_mobile_compacto_360x800.png](file:///d:/projetos/lp-nuvem-rush/evidencias/04_mobile_compacto_360x800.png) | 386 KB |
| **FULL-01** | **1440 × 7200 px** | Desktop Página Completa (Scroll Total) | [05_fullpage_desktop_1440.png](file:///d:/projetos/lp-nuvem-rush/evidencias/05_fullpage_desktop_1440.png) | 7.10 MB |
| **FULL-02** | **390 × 9600 px** | Mobile Página Completa (Scroll Total) | [06_fullpage_mobile_390.png](file:///d:/projetos/lp-nuvem-rush/evidencias/06_fullpage_mobile_390.png) | 3.58 MB |

---

## 2. Rastreamento e Mapeamento Seção por Seção

A página foi dividida em 10 macroáreas funcionais. Cada área foi recortada em alta fidelidade a partir do render oficial do desktop:

### Área 01: Cabeçalho Fixo e Hero Principal
* **Evidência Visual:** [area_01_cabecalho_e_hero.png](file:///d:/projetos/lp-nuvem-rush/evidencias/secoes/area_01_cabecalho_e_hero.png) (1440 × 950 px)
* **Localização no DOM:** `<header class="site-header">` e `<section class="hero-section">` (0 a 950px no scroll)
* **Elementos Contidos:**
  * Logotipo minimalista com nuvem vetorial e badge `NUVEMSHOP API`.
  * Menu editorial numerado de `§ 01` a `§ 06`.
  * Botão de ativação rápida no cabeçalho (`.header-cta-desktop`).
  * Tag de liderança com ponto pulsante verde Meta (`.pulse-dot`).
  * Título H1: *"A inteligência invisível que recupera suas vendas na Nuvem."* com o termo *"Nuvem."* em itálico de alto contraste (`Instrument Serif`).
  * Canvas central em WebGL com Three.js gerando o vórtice volumétrico de partículas.
  * Botões de ação: *"Ativar no Piloto Automático"* (com ícone SVG de seta) e *"Simular Retorno Financeiro ↓"* (com caractere Unicode de seta).
* **Diagnóstico Visual:** A composição transmite alto impacto e prestígio. No entanto, o texto não comunica de imediato o formato do software, e a presença de setas em ambos os botões quebra a pureza minimalista.

---

### Área 02: Barra de Métricas e Especificações de Infraestrutura
* **Evidência Visual:** [area_02_metricas_e_especificacoes.png](file:///d:/projetos/lp-nuvem-rush/evidencias/secoes/area_02_metricas_e_especificacoes.png) (1440 × 600 px)
* **Localização no DOM:** `<div class="tech-specs-bar">` e `<div class="metrics-grid">` (850 a 1450px)
* **Elementos Contidos:**
  * Indicadores de latência e protocolo (`META CLOUD API OFICIAL`, `LATÊNCIA < 60S`, `ZERO BAN RISK`).
  * Grid com 3 células métricas:
    * `98.2%` — Taxa de entrega confirmada via WhatsApp oficial.
    * `14.4%` — Média de conversão na recuperação de carrinhos esquecidos.
    * `< 60s` — Disparo inteligente logo após o evento de abandono.
* **Diagnóstico Visual:** Excelente uso de tipografia técnica (`Space Grotesk`) e bordas divisórias sutis. Os números são críveis e geram ancoragem quantitativa imediata.

---

### Área 03: Seção § 01 — Simulador Financeiro de Retorno (ROI)
* **Evidência Visual:** [area_03_simulador_financeiro_roi.png](file:///d:/projetos/lp-nuvem-rush/evidencias/secoes/area_03_simulador_financeiro_roi.png) (1440 × 850 px)
* **Localização no DOM:** `<section class="section-py" id="roi">` (1400 a 2250px)
* **Elementos Contidos:**
  * Tag editorial: `§ 01 SIMULAÇÃO DE CAPITAL OCULTO`.
  * Título H2: *"Quanto faturamento está se dissipando no seu checkout?"*.
  * Painel dividido: 
    * Lado esquerdo: Sliders interativos de pedidos (50 a 2.500) e Ticket Médio (R$ 40 a R$ 800).
    * Lado direito: Caixa de liquidez recuperada (`R$ 6.048,00 / mês`) com cálculo estimado anual (`R$ 72.576,00`).
  * CTA contextual: *"Resgatar Esse Capital Agora"*, com mensagem personalizada para o WhatsApp.
* **Diagnóstico Visual:** É o elemento de maior força persuasiva da página. O contraste entre os sliders discretos e a tipografia dourada champagne da cifra resgatada funciona perfeitamente. Ponto de atenção: a nota explicativa em `--color-dust` possui baixo contraste sobre o fundo escuro.

---

### Área 04: Seção § 02 — O Contraste Operacional
* **Evidência Visual:** [area_04_contraste_operacional.png](file:///d:/projetos/lp-nuvem-rush/evidencias/secoes/area_04_contraste_operacional.png) (1440 × 850 px)
* **Localização no DOM:** Seção intermediária sem ID de âncora (2200 a 3050px)
* **Elementos Contidos:**
  * Tag editorial: `§ 02 O CONTRASTE OPERACIONAL`.
  * Título H2: *"O dia a dia da sua loja sob duas filosofias distintas."*.
  * 2 Ledger Cards comparativos:
    * Cartão Esquerdo ("Loja Convencional"): Foco em perda constante de margem, mensagens manuais e risco de bloqueio em chips piratas.
    * Cartão Direito ("Loja com Nuvem Rush"): Precisão em segundo plano, API oficial da Meta e sincronização contínua.
* **Diagnóstico Visual:** Conceitualmente forte, mas visualmente muito denso em texto corrido. Por não possuir ID no HTML, o visitante não consegue acessá-la diretamente pelo menu superior.

---

### Área 05: Seção § 03 — Playground do Motor de Automações
* **Evidência Visual:** [area_05_playground_automacoes.png](file:///d:/projetos/lp-nuvem-rush/evidencias/secoes/area_05_playground_automacoes.png) (1440 × 950 px)
* **Localização no DOM:** `<section class="section-py" id="arquitetura">` (3000 a 3950px)
* **Elementos Contidos:**
  * Tag editorial: `§ 03 MOTOR DE FLUXOS VISUAIS` (Obs.: o menu superior aponta para aqui através do link `§ 02 Motor`).
  * Seletor de abas com 4 fluxos: *01. Resgate de Carrinho*, *02. Rastreio & Confirmação*, *03. Ciclo de Recompra*, *04. Boas-Vindas VIP*.
  * Diagrama de nós de automação (Gatilho → Temporizador → Filtro → Disparo WhatsApp).
  * Mockup realista de smartphone renderizando a conversa do WhatsApp em tempo real.
* **Diagnóstico Visual:** É o primeiro momento onde o visitante enxerga o produto real funcionando. Está excessivamente distante do topo (após 3.000 pixels). Os emojis do mockup (`📦`, `🧴`) quebram a sofisticação da interface.

---

### Área 06: Seção § 04 — O Arsenal Técnico de Funcionalidades
* **Evidência Visual:** [area_06_arsenal_funcionalidades.png](file:///d:/projetos/lp-nuvem-rush/evidencias/secoes/area_06_arsenal_funcionalidades.png) (1440 × 1050 px)
* **Localização no DOM:** `<section class="section-py" id="arsenal">` (3900 a 4950px)
* **Elementos Contidos:**
  * Tag editorial: `§ 04 O ARSENAL TÉCNICO` (no menu: `§ 03 Recursos`).
  * Grid 3x2 com 6 cartões interativos dotados de efeito de inclinação 3D (`tilt`) e reflexo especular:
    1. *Resgate de Carrinho Abandonado*
    2. *Confirmação de Pedido & Rastreio VIP*
    3. *Recompra Preditiva & LTV*
    4. *Infraestrutura Oficial Meta Cloud API*
    5. *Assistente Editorial com Inteligência Artificial*
    6. *Tags Dinâmicas e Webhooks Livres*
* **Diagnóstico Visual:** Visualmente impecável. Os cartões possuem excelente distribuição de peso, bordas sutis e tipografia bem ajustada.

---

### Área 07: Seção § 05 — Protocolo de Ativação e Conexão
* **Evidência Visual:** [area_07_protocolo_ativacao_conexoes.png](file:///d:/projetos/lp-nuvem-rush/evidencias/secoes/area_07_protocolo_ativacao_conexoes.png) (1440 × 800 px)
* **Localização no DOM:** `<section class="section-py" id="estagios">` (4900 a 5700px)
* **Elementos Contidos:**
  * Tag editorial: `§ 05 PROTOCOLO DE ATIVAÇÃO` (no menu: `§ 04 Conexão`).
  * Linha do tempo horizontal dividida em 3 etapas sequenciais:
    * *01. Sincronização Nuvemshop* (autorização em 1 clique).
    * *02. Conexão Oficial Meta* (pareamento do número comercial).
    * *03. Ativação da Nuvem* (fluxos rodando em piloto automático).
* **Diagnóstico Visual:** Muito limpa e funcional. Desmistifica a complexidade da integração e passa segurança operacional para o lojista.

---

### Área 08: Seção § 06 — Condição de Lançamento (Preço Fundador)
* **Evidência Visual:** [area_08_preco_fundador_e_garantia.png](file:///d:/projetos/lp-nuvem-rush/evidencias/secoes/area_08_preco_fundador_e_garantia.png) (1440 × 750 px)
* **Localização no DOM:** `<section class="section-py" id="preco">` (5650 a 6400px)
* **Elementos Contidos:**
  * Tag editorial: `§ 06 CONDIÇÃO DE LANÇAMENTO` (no menu: `§ 05 Preço Fundador`).
  * Card cofre (*Vault Card*) com valor destacado: **R$ 39,90 / mês** (condição vitalícia do plano fundador).
  * Cronômetro de contagem regressiva ao vivo (`#cd-hours`, `#cd-mins`, `#cd-secs`).
  * Lista de funcionalidades inclusas com checagem vetorial.
  * Botão de conversão principal: *"Garantir Preço Fundador de R$ 39,90"*.
  * Selo de Garantia Incondicional de 7 Dias.
* **Diagnóstico Visual:** Oferta comercial muito forte. A contagem regressiva cria senso de urgência sem parecer apelativa graças à sobriedade tipográfica.

---

### Área 09: Seção § 07 — Esclarecimentos e Perguntas Frequentes (FAQ)
* **Evidência Visual:** [area_09_faq_duvidas_frequentes.png](file:///d:/projetos/lp-nuvem-rush/evidencias/secoes/area_09_faq_duvidas_frequentes.png) (1440 × 600 px)
* **Localização no DOM:** `<section class="section-py" id="faq">` (6350 a 6950px)
* **Elementos Contidos:**
  * Tag editorial: `§ 07 ESCLARECIMENTOS` (no menu: `§ 06 Dúvidas`).
  * Acordeão com 5 perguntas críticas:
    1. *Como o Nuvem Rush conecta com a Nuvemshop?*
    2. *Existe risco de o meu número do WhatsApp ser banido?*
    3. *Como funcionam os custos das mensagens do WhatsApp?*
    4. *Preciso deixar o computador ou celular ligado?*
    5. *Posso cancelar a qualquer momento?*
* **Diagnóstico Visual:** Acordeão suave e legível. Resolve com precisão jurídica as duas principais objeções de venda (risco de banimento e cobrança da Meta).

---

### Área 10: Rodapé Institucional, Compliance e Dados Legais
* **Evidência Visual:** [area_10_rodape_compliance_legal.png](file:///d:/projetos/lp-nuvem-rush/evidencias/secoes/area_10_rodape_compliance_legal.png) (1440 × 350 px)
* **Localização no DOM:** `<footer class="site-footer">` (6850 a 7200px)
* **Elementos Contidos:**
  * Marca Nuvem Rush com ícone vetorial.
  * Dados cadastrais oficiais da empresa mantenedora: **Conect Web · CNPJ 63.039.583/0001-84**.
  * E-mail oficial de suporte: `suporte@nuvemrush.com.br`.
  * Links diretos para as 4 páginas de diretrizes (`/politica-de-privacidade.html`, `/termos-de-uso.html`, `/politica-de-cookies.html`, `/exclusao-de-dados.html`).
  * Disclaimer de marcas registradas Nuvemshop e WhatsApp.
* **Diagnóstico Visual:** Rigor corporativo impecável. A única anomalia técnica encontrada reside nos links com barra inicial (`/politica-...`) que quebram quando testados em pastas locais.

---

## 3. Síntese do Mapeamento Responsivo

```
+-------------------------------------------------------------------------+
| LARGURA 1440px / 1366px (DESKTOP E NOTEBOOK):                           |
| -> Grid de 1200px perfeitamente alinhado                                |
| -> Menu de navegacao completo e funcional                               |
| -> Vórtice Three.js volumétrico em 60 FPS                               |
| -> Sliders de ROI e Mockup de WhatsApp operando lado a lado             |
+-------------------------------------------------------------------------+
                                    |
                                    v
+-------------------------------------------------------------------------+
| LARGURA <= 960px (TABLET, IPHONE 390px, ANDROID 360px):                 |
| [X] .nav-links { display: none } oculta o menu por completo             |
| [X] Nao existe botao hambúrguer ou drawer                               |
| [X] Visitante obrigado a rolar mais de 9.000px de altura verticalmente   |
| [!] Sliders empilham verticalmente e funcionam com toque touch          |
| [!] Mockup do celular fica empilhado abaixo dos nós de gatilho          |
+-------------------------------------------------------------------------+
```
