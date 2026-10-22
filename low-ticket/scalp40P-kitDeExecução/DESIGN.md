---
name: TraderLab Aprendizagem
description: Uma experiência acolhedora e objetiva para estudar os cursos disponíveis.
colors:
  primary: "#A2CB10"
  primary-hover: "#8BAE0B"
  primary-ink: "#354604"
  ink: "#0C0D0E"
  muted: "#6E6D6B"
  canvas: "#F5F3EF"
  surface: "#FFFBF7"
  line: "#E5E1DC"
  soft-green: "#EFF6D9"
  danger: "#A71619"
  auth-green: "#1E5A42"
  auth-green-hover: "#174833"
typography:
  display:
    fontFamily: "Roboto Serif, Georgia, serif"
    fontSize: "clamp(32px, 4.4vw, 54px)"
    fontWeight: 570
    lineHeight: 1.04
  title:
    fontFamily: "Roboto Serif, Georgia, serif"
    fontSize: "20px"
    fontWeight: 600
    lineHeight: 1.3
  body:
    fontFamily: "Roboto, ui-sans-serif, system-ui, sans-serif"
    fontSize: "13px"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "Roboto, ui-sans-serif, system-ui, sans-serif"
    fontSize: "11px"
    fontWeight: 700
    lineHeight: 1.4
    letterSpacing: "0.13em"
rounded:
  xs: "4px"
  sm: "6px"
  md: "9px"
  card: "14px"
  pill: "99px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "12px"
  lg: "18px"
  xl: "24px"
  section: "28px"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.ink}"
    rounded: "{rounded.xs}"
    height: "49px"
    padding: "0 20px"
  card:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.card}"
    padding: "23px 25px"
  navigation-active:
    backgroundColor: "{colors.soft-green}"
    textColor: "{colors.ink}"
    rounded: "{rounded.md}"
    height: "44px"
    padding: "0 14px"
---

# Design System: TraderLab Aprendizagem

## Overview

**Creative North Star: "Estudo com clareza, no ritmo do aluno"**

A aplicação web do aluno compartilha a identidade visual do TraderLab Gestão: títulos editoriais em Roboto Serif, interface em Roboto, superfícies quentes e o verde-lima da marca usado como sinal de ação e progresso. O espaço autenticado tem uma navegação lateral compacta e expansível, deixando o conteúdo do curso no centro da experiência.

As telas organizam a jornada em cursos, módulos, aulas e materiais, com indicadores de progresso e ações de retomada. As páginas de curso usam capas e uma hierarquia editorial mais expressiva; listas, formulários e notificações mantêm controles compactos e legíveis. As telas públicas de autenticação ainda têm uma paleta verde-floresta própria (`#1E5A42`) e títulos sans-serif; essa diferença é parte do estado implementado e não deve ser confundida com os tokens da área autenticada.

**Key Characteristics:**
- Marca compartilhada com o admin, aplicada a uma área de aprendizagem própria
- Navegação lateral compacta e expansível no desktop
- Roboto Serif em títulos de conteúdo e Roboto nos controles e textos
- Fundo marfim, painéis claros e verde-lima em ações e progresso

## Colors

A área autenticada combina o verde-lima da marca com neutros quentes; as telas públicas de autenticação conservam uma variação verde-floresta distinta.

### Primary
- **Verde TraderLab** (`{colors.primary}`): ação principal, item selecionado, progresso e pequenos destaques; use texto escuro para manter contraste.
- **Verde profundo** (`{colors.primary-hover}`): estado de hover para ações em verde-lima.
- **Verde escuro de apoio** (`{colors.primary-ink}`): ícones e texto em fundos verde-pálidos.

### Secondary
- **Vermelho TraderLab** (`{colors.danger}`): mensagens de erro e estados destrutivos.

### Neutral
- **Preto suave** (`{colors.ink}`): texto principal e conteúdo de alto contraste.
- **Cinza de apoio** (`{colors.muted}`): descrições, metadados e navegação inativa.
- **Canvas quente** (`{colors.canvas}`): fundo da área de estudo autenticada.
- **Off-white quente** (`{colors.surface}`): cartões, menus e painéis.
- **Linha quente** (`{colors.line}`): bordas e separadores.
- **Verde pálido** (`{colors.soft-green}`): seleção e realce suave.
- **Verde-floresta de autenticação** (`{colors.auth-green}`) e **hover** (`{colors.auth-green-hover}`): botões e links nas telas públicas de autenticação existentes.

### Named Rules
**The Restrained Lime Rule.** Use o verde-lima como ênfase pontual, mantendo texto escuro sobre a cor de marca.

## Typography

**Display Font:** Roboto Serif (with Georgia, serif fallback)
**Body Font:** Roboto (with ui-sans-serif and system sans-serif fallbacks)

**Character:** A serif dá aos títulos de cursos e seções um tom editorial; Roboto mantém leitura eficiente em navegação, dados, formulários e controles. As telas públicas de autenticação são uma exceção atual e usam títulos sans-serif.

### Hierarchy
- **Display** (570, `clamp(32px, 4.4vw, 54px)`, 1.04): título principal de curso e conteúdo.
- **Title** (600, 20px, 1.3): títulos de cartões, módulos e notificações.
- **Body** (400, 13px, 1.6): texto de interface e explicações; descrições de curso costumam ter largura máxima próxima de 65ch.
- **Label** (700, 11px, 1.4, espaçamento de 0.13em quando em eyebrow): metadados e pequenas chamadas de seção.

### Named Rules
**The Heading Contrast Rule.** Use Roboto Serif nos títulos da área de aprendizagem e Roboto em texto corrido, navegação e controles; preserve a tipografia sans-serif já implementada nas telas públicas de autenticação.

## Layout

No desktop, a área autenticada reserva uma faixa lateral estreita para a navegação e usa o restante da largura para o conteúdo; o recuo esquerdo do conteúdo varia de `122px` a `156px`, com padding horizontal fluido. O dock recolhido mostra ícones e pode ser expandido para rótulos e marca completa. A área principal de curso limita o conteúdo a `1220px`; páginas de notificações e outros conteúdos usam larguras menores quando favorecem a leitura.

Em telas de até `760px`, a navegação lateral se adapta a um dock compacto e o conteúdo ganha paddings menores. Páginas de autenticação ocultam a imagem lateral até `850px` e passam a uma coluna; ajustes adicionais para telas estreitas ocorrem em `560px`, `480px` e `420px`, conforme a tela. O ritmo de espaçamento observado usa principalmente 4, 8, 12, 18, 24 e 28px, com valores fluidos para margens e colunas.

## Elevation & Depth

A profundidade é híbrida: bordas quentes definem a estrutura e sombras leves destacam cartões importantes, menus e superfícies flutuantes. Linhas de conteúdo e elementos internos ficam mais planos; o blur translúcido é usado no cabeçalho fixo da área de estudo.

### Shadow Vocabulary
- **Card** (`0 12px 30px rgb(24 25 18 / 5%)`): cartões de notificação e painéis principais.
- **Floating** (`0 18px 50px rgb(26 42 31 / 13%)`): menus e popovers sobre o conteúdo.
- **Course panel** (`0 10px 30px rgb(12 13 14 / 4%)`): painéis e cartões de curso que pedem elevação discreta.

### Named Rules
**The Panel-Only Shadow Rule.** Reserve sombras para painéis principais e superfícies flutuantes, não para cada linha ou controle.

## Shapes

Controles e botões usam cantos compactos de 4–6px; menus e filtros chegam a 9px; cartões de curso e notificação usam em geral 14px. Avatares, marcadores e chips usam círculos ou pílulas. Capas de curso usam recorte arredondado e imagem em destaque. Bordas finas em tons quentes separam superfícies sem criar divisões pesadas.

## Components

### Buttons
- **Shape:** retângulo compacto, geralmente 4px nas ações principais.
- **Primary:** verde-lima `#A2CB10`, texto escuro, altura mínima de 49px e padding horizontal de 20px na base global; telas internas podem definir dimensões próprias.
- **Hover / Focus:** hover usa verde mais profundo; o foco de teclado é visível com contorno de 3px e offset de 3px. Preserve também o feedback ativo e os estados desabilitados existentes.
- **Secondary:** superfície clara com borda discreta ou fundo verde pálido, conforme o contexto.

### Chips
- **Style:** metadados e estados em superfície neutra ou verde pálido, com texto escuro/verde escuro.
- **Shape:** pílula para categorias, perfil e status.

### Cards / Containers
- **Corner Style:** 14px nos cartões de curso e notificação; variações menores aparecem em painéis compactos.
- **Background:** off-white quente sobre canvas marfim.
- **Shadow Strategy:** elevação suave em cartões principais e menus; linhas e estruturas internas permanecem discretas.
- **Internal Padding:** varia com a densidade; cartões de notificação usam cerca de 16–25px conforme a largura disponível.

### Inputs / Fields
- **Style:** fundo claro, borda fina neutra e cantos entre 4–6px nas telas públicas.
- **Focus:** borda verde e halo sutil nas telas de autenticação; controles internos usam contorno de teclado verde visível.
- **Error / Disabled:** mensagens de erro em vermelho; controles indisponíveis reduzem opacidade e indicam estado desabilitado.

### Navigation
- **Style:** dock vertical compacto no desktop, com ícones de 20px, estado ativo em verde pálido e rótulos revelados ao expandir.
- **Mobile:** adaptação para navegação compacta em até 760px; mantenha todos os destinos acessíveis e o estado atual identificável.

### Course Progress
Barras finas em verde comunicam avanço do curso ou módulo; números de progresso usam algarismos tabulares quando disponíveis. Mantenha a indicação associada ao curso ou à aula correspondente.

## Do's and Don'ts

### Do:
- **Do** manter os tokens de marca compartilhados com TraderLab Gestão na área autenticada.
- **Do** usar Roboto Serif em títulos de aprendizagem e Roboto em navegação, dados e controles.
- **Do** manter o dock e os destinos de navegação consistentes entre as telas de aluno.
- **Do** usar verde-lima com texto escuro e reservar o vermelho para erro ou ação destrutiva.
- **Do** preservar os estados visíveis de foco, progresso, notificações não lidas e conteúdo concluído.
- **Do** respeitar o comportamento responsivo já implementado nas telas públicas e autenticadas.

### Don't:
- **Don't** aplicar verde-lima como fundo dominante ou usar texto branco em ações lime.
- **Don't** usar serif em controles, navegação ou texto corrido.
- **Don't** espalhar sombras por linhas, células e elementos aninhados.
- **Don't** tratar a paleta verde-floresta da autenticação como substituta da paleta de marca da área de aprendizagem.
- **Don't** sugerir compra de cursos ou capacidades futuras como se já estivessem disponíveis.
