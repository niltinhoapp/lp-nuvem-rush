# INVENTÁRIO TÉCNICO E VISUAL DE COMPONENTES — NUVEM RUSH

**Projeto:** Nuvem Rush (`nuvemrush.com.br` / `rush.com.br`)  
**Data da Auditoria:** 16 de Novembro de 2026  
**Fase:** Fase 2A — Inventário Completo de Componentes de Interface  
**Status:** Documentação técnica sem alteração de arquivos de código  

---

## 1. Visão Geral da Arquitetura de Componentes

O Nuvem Rush é estruturado através de componentes CSS com escopo inline em `index.html`, organizados em torno de um Design System unificado sob o conceito *Dark Void Quiet Luxury*. Abaixo encontra-se o inventário exaustivo de cada átomo, molécula e organismo que compõe a interface.

---

## 2. Inventário Detalhado dos Componentes

### 1. Botão Primário de Conversão (`.btn-luxury`)
* **Seletor CSS:** `.btn.btn-luxury`
* **Localizações:**
  * Cabeçalho Desktop: *"Ativar Nuvem Rush"*
  * Hero Section: *"Ativar no Piloto Automático"*
  * Simulador de ROI: *"Resgatar Esse Capital Agora"*
  * Preço Fundador: *"Garantir Preço Fundador de R$ 39,90"*
  * Chamada Final: *"Ativar Minha Loja no Automático Hoje"*
* **Função:** Ação principal de conversão direcionada para o WhatsApp de vendas ou âncora de preço.
* **Aparência:** Fundo em gradiente dourado champagne sutil (`linear-gradient(135deg, #ede3d2 0%, #d8caa7 100%)`), cor do texto em preto profundo (`#060709`), tipografia `Plus Jakarta Sans` com peso 700, bordas arredondadas (`border-radius: 9999px`), sombra dourada difusa com glow e brilho especular.
* **Comportamento:** Ao passar o mouse (`:hover`), sofre translação suave `translateY(-2px)`, ampliação da sombra dourada e transição de opacidade interna.
* **Reutilização:** Alto grau de consistência em 5 pontos estratégicos da página.
* **Problemas Encontrados:** No Hero e em outros pontos, carrega um ícone SVG de seta para a direita (`→`), colidindo com a diretriz editorial de botões puros sem setas.

---

### 2. Botão Secundário de Exploração (`.btn-ghost`)
* **Seletor CSS:** `.btn.btn-ghost`
* **Localização:** Hero Section (ao lado do CTA principal).
* **Função:** Rolar suavemente a página até o Simulador de ROI (`#roi`).
* **Aparência:** Fundo translúcido escuro, borda ultrafina de 1px em `rgba(255, 255, 255, 0.12)`, texto em platina (`#f2f3f5`), tipografia `Plus Jakarta Sans` peso 600.
* **Comportamento:** Ao passar o mouse, a borda ganha luminosidade branca (`rgba(255, 255, 255, 0.35)`) e o fundo escurece ligeiramente.
* **Reutilização:** Uso pontual no Hero.
* **Problemas Encontrados:** Contém no texto uma seta explícita para baixo: `Simular Retorno Financeiro ↓`. A seta acrescenta ruído desnecessário.

---

### 3. Botão Flutuante de Especialista (`.wa-quiet-btn`)
* **Seletor CSS:** `.wa-quiet-btn`
* **Localização:** Canto inferior direito da tela (fixo no viewport).
* **Função:** Oferecer canal direto e rápido para tirar dúvidas com consultor da Conect Web.
* **Aparência:** Pílula escura de luxo (`#0f1217`) com borda em champagne, ícone vetorial do WhatsApp em verde esmeralda Meta (`#10b981`), texto *"Especialista Nuvem Rush"*.
* **Comportamento:** Fixado via `position: fixed; bottom: 24px; right: 24px; z-index: 90;`. Ao passar o mouse, eleva-se suavemente.
* **Reutilização:** Componente global persistente em todas as seções.
* **Problemas Encontrados:** Em telas pequenas de 360px de largura, pode sobrepor os links legais ou textos do rodapé quando o usuário atinge o final da página.

---

### 4. Cabeçalho e Barra de Navegação (`.site-header`)
* **Seletor CSS:** `.site-header`, `.nav-inner`, `.nav-links`, `.nav-link`, `.brand-group`
* **Localização:** Topo da tela (fixo).
* **Função:** Identificação da marca, navegação editorial entre seções e conversão rápida.
* **Aparência:** Fundo em *glassmorphism* escuro (`rgba(6, 7, 9, 0.85)`), filtro de desfoque (`backdrop-filter: blur(16px)`), borda inferior de 1px em `var(--color-hairline)`.
* **Comportamento:** Fixação contínua via `position: fixed; top: 0; left: 0; right: 0; z-index: 100;`.
* **Reutilização:** Organismo global.
* **Problemas Encontrados:**
  1. **Falha Crítica Mobile:** Em larguras `<= 960px`, aplica `.nav-links { display: none }` sem renderizar menu alternativo ou hambúrguer.
  2. **Dissonância Numérica:** Links etiquetados como `§ 02 Motor`, `§ 03 Recursos`, `§ 04 Conexão`, `§ 05 Preço Fundador` e `§ 06 Dúvidas` estão desfasados em 1 número em relação aos títulos reais do corpo da página.

---

### 5. Badges e Etiquetas Editoriais (`.index-tag`, `.brand-badge`, `.hero-lead-tag`)
* **Seletor CSS:** `.index-tag`, `.brand-badge`, `.hero-lead-tag`, `.pulse-dot`
* **Localizações:** No topo de cada seção e junto ao logotipo.
* **Função:** Contextualizar o tema da seção, indicar conformidade técnica e orientar a leitura.
* **Aparência:** Tipografia monoespaçada `Space Grotesk`, letras maiúsculas, espaçamento entre caracteres generoso (`letter-spacing: 0.14em`), cor dourada champagne atenuada (`#c7baaa`).
* **Comportamento:** Estático, servindo como marcadores de precisão suíça. O elemento `.pulse-dot` possui animação CSS contínua de pulso verde esmeralda indicando sistema online.
* **Reutilização:** Altamente padronizado em todas as 7 seções numeradas.
* **Problemas Encontrados:** A tag `§ 03 MOTOR DE FLUXOS VISUAIS` não corresponde ao link de navegação correspondente (`§ 02 Motor`).

---

### 6. Contêiner de Cartão Editorial Padrão (`.editorial-card`)
* **Seletor CSS:** `.editorial-card`
* **Localizações:** Simulador de ROI (`#roi`), Painel de Fluxos (`#arquitetura`), Card de Preço (`#preco`).
* **Função:** Base estrutural para agrupamento de módulos visuais complexos.
* **Aparência:** Fundo em superfície grafite escura (`rgba(15, 18, 23, 0.75)`), borda ultrafina `rgba(255, 255, 255, 0.08)`, raio de arredondamento generoso de 24px (`border-radius: var(--radius-lg)`), efeito de profundidade com sombra difusa.
* **Comportamento:** Suporta microinterações internas de abas e sliders.
* **Reutilização:** Excelente nível de reuso como contêiner unificado.
* **Problemas Encontrados:** Nenhum. Componente muito bem calibrado.

---

### 7. Cartões de Contraste Operacional (`.ledger-card`)
* **Seletor CSS:** `.ledger-grid`, `.ledger-card`
* **Localização:** Seção § 02 (O Contraste Operacional).
* **Função:** Comparar visualmente a experiência caótica de uma loja comum versus a precisão do Nuvem Rush.
* **Aparência:** Formato de livro-razão financeiro clássico. O cartão tradicional possui bordas avermelhadas e opacas; o cartão do Nuvem Rush possui iluminação esmeralda e borda luminosa.
* **Comportamento:** Ao passar o mouse, sutil aumento de brilho e elevação de 3px.
* **Reutilização:** Exclusivo da seção de comparação.
* **Problemas Encontrados:** Excesso de texto corrido em parágrafos densos que dificultam o escaneamento dinâmico.

---

### 8. Cartões de Recursos com Efeito 3D (`.arsenal-card`)
* **Seletor CSS:** `.arsenal-grid`, `.arsenal-card`, `.arsenal-card-inner`
* **Localização:** Seção § 04 (O Arsenal Técnico).
* **Função:** Apresentar os 6 pilares de funcionalidades do sistema.
* **Aparência:** Cartões retangulares escuros com ícone no topo esquerdo, número técnico em `Space Grotesk`, título e parágrafo conciso.
* **Comportamento:** **Tilt 3D Dinâmico** via JavaScript ouvindo `mousemove`, calculando a inclinação tridimensional (`rotateX`, `rotateY`) e projetando um gradiente radial especular (*specular glare*) sobre o cartão.
* **Reutilização:** Grid homogêneo de 6 unidades idênticas em layout 3x2 (desktop) e 1x6 (mobile).
* **Problemas Encontrados:** O cálculo contínuo de `mousemove` nos 6 cartões simultâneos adiciona listeners que consomem CPU em notebooks sem GPU dedicada.

---

### 9. Sliders Interativos do Simulador Financeiro (`.luxury-range`)
* **Seletor CSS:** `.luxury-range`, `.slider-row`
* **Localização:** Seção § 01 (Simulador de ROI).
* **Função:** Permitir que o lojista ajuste o volume de pedidos e o ticket médio de sua loja.
* **Aparência:** Trilho cinza escuro ultrafino (4px) e cursor circular dourado champagne (`thumb`) com sombra luminescente.
* **Comportamento:** Atualização instantânea dos cálculos na caixa lateral sem necessidade de recarregar a página ou clicar em botão "Calcular".
* **Reutilização:** Exclusivo da seção ROI.
* **Problemas Encontrados:** O texto explicativo no rodapé do slider usa a cor `--color-dust` com contraste insuficiente (2.83:1).

---

### 10. Seletor de Abas do Motor de Automações (`.engine-tab-btn`)
* **Seletor CSS:** `.engine-tabs`, `.engine-tab-btn`, `.engine-tab-btn.active`
* **Localização:** Seção § 03 (Motor de Fluxos Visuais).
* **Função:** Alternar entre os 4 cenários práticos de automação.
* **Aparência:** Botões retangulares minimalistas com borda inferior de destaque. A aba ativa recebe iluminação dourada e fundo escuro elevado.
* **Comportamento:** Evento `click` altera as informações dos nós laterais e o conteúdo da tela do smartphone de forma síncrona.
* **Reutilização:** Exclusivo da seção de fluxos.
* **Problemas Encontrados:** Em telas de smartphone (390px/360px), as 4 abas comprimem-se ou quebram em múltiplas linhas, exigindo barra de rolagem horizontal nativa.

---

### 11. Mockup de Smartphone com Conversa do WhatsApp (`.wa-mockup-frame`)
* **Seletor CSS:** `.wa-mockup-frame`, `.mockup-chat-bubble`, `.mockup-header`
* **Localização:** Seção § 03 (lado direito do painel de fluxos).
* **Função:** Renderizar visualmente como a mensagem chega ao cliente do e-commerce.
* **Aparência:** Silhueta de smartphone sem bordas agressivas, barra de status superior, balões de conversa oficiais do WhatsApp com carimbo de hora e selo de entregue/lido.
* **Comportamento:** O texto da conversa atualiza suavemente ao alternar as abas do motor.
* **Reutilização:** Exclusivo da demonstração de automação.
* **Problemas Encontrados:** Uso de emojis não estilizados (`📦`, `🧴`) que parecem casuais demais para a direção de arte Quiet Luxury.

---

### 12. Elementos de Computação Gráfica 3D e Canvas
* **Seletor CSS:** `#hero-cloud-3d`, `#cloud-spine-canvas`
* **Localização:**
  * `#hero-cloud-3d`: Fundo interativo da primeira dobra do Hero.
  * `#cloud-spine-canvas`: Fundo contínuo de ponta a ponta do documento.
* **Função:** Criar a sensação de uma nuvem orgânica inteligente envolvendo o produto.
* **Aparência:**
  * No Hero: Vórtice de milhares de pontos volumétricos que reagem suavemente à posição do ponteiro do mouse.
  * No fundo: Linha senoidal contínua (*spine*) desenhada em curvas de Bézier.
* **Comportamento:** Loops ininterruptos via `requestAnimationFrame`.
* **Reutilização:** Componentes cenográficos de fundo.
* **Problemas Encontrados:** Rodam continuamente mesmo quando o usuário já rolou até o rodapé, consumindo bateria desnecessariamente em celulares.

---

### 13. Acordeão de Esclarecimentos / FAQ (`.faq-accordion`)
* **Seletor CSS:** `.faq-accordion`, `.faq-item`, `.faq-q`, `.faq-a`, `.faq-icon`
* **Localização:** Seção § 07 (Esclarecimentos).
* **Função:** Sanar objeções críticas antes da contratação.
* **Aparência:** Lista de barras horizontais com divisores de 1px em hairline.
* **Comportamento:** Clique na pergunta expande a resposta suavemente via animação de altura/max-height e alterna o ícone de `+` para `-`.
* **Reutilização:** Padrão clássico de acordeão.
* **Problemas Encontrados:** O ícone utiliza texto simples `+` e `-` em vez de um chevron SVG elegante com rotação CSS de 180 graus.

---

### 14. Toast Flutuante de Notificação em Tempo Real (`.quiet-toast`)
* **Seletor CSS:** `.quiet-toast`
* **Localização:** Canto inferior esquerdo da tela.
* **Função:** Prova social sutil demonstrando que lojas reais estão recuperando pedidos naquele instante.
* **Aparência:** Caixa preta fosca de alta elegância com borda dourada e ícone de raio esmeralda. Exibe mensagens como: *"Loja em São Paulo recuperou pedido de R$ 240,00 via WhatsApp agora há pouco"*.
* **Comportamento:** Surge após 4 segundos de permanência na página, permanece por 6 segundos e desaparece via opacidade e translate suave.
* **Reutilização:** Componente global de persuasão.
* **Problemas Encontrados:** Usa o caractere emoji `⚡` no lugar de um vetor minimalista.

---

### 15. Banner de Consentimento de Privacidade LGPD (`.cookie-banner`)
* **Seletor CSS:** `.cookie-banner`
* **Localização:** Barra inferior fixa no primeiro acesso.
* **Função:** Conformidade jurídica com a LGPD e regulamentos de privacidade do Meta Pixel.
* **Aparência:** Barra escura translúcida discreta com texto explicativo e botões *"Aceitar Diretrizes"* e *"Personalizar"*.
* **Comportamento:** Grava chave no `localStorage` do navegador para não incomodar o visitante em visitas subsequentes.
* **Reutilização:** Componente global legal.
* **Problemas Encontrados:** Nenhum. Executado com sobriedade e leveza.

---

## 3. Tabela Comparativa de Componentes e Oportunidades

| Componente | Nível de Acabamento | Conformidade de Acessibilidade | Oportunidade de Melhoria |
| :--- | :--- | :--- | :--- |
| **Botão Primário** | Excelente (Alto Luxo) | Aprovado | Remover setas indicativas embutidas |
| **Botão Secundário** | Muito Bom | Aprovado | Remover caractere `↓` do texto |
| **Cabeçalho Desktop** | Excelente | Aprovado | Sincronizar numeração com as seções |
| **Navegação Mobile** | Inexistente (Crítico) | **REPROVADO** | Criar menu hambúrguer com gaveta translúcida |
| **Simulador de ROI** | Excelente | Alerta (Contraste das notas) | Elevar tom do cinza para aprovação WCAG |
| **Cartões 3D Arsenal** | Excelente | Aprovado | Otimizar listeners de performance |
| **Motor de Fluxos** | Muito Bom | Aprovado | Trocar emojis por ícones vetoriais |
| **Vórtice 3D Canvas** | Excepcional | Neutro (Decorativo) | Pausar loop quando fora da tela |
| **Acordeão de FAQ** | Bom | Aprovado | Trocar `+`/`-` por chevron com rotação |
| **Toast Flutuante** | Muito Bom | Aprovado | Substituir `⚡` por ícone SVG |
