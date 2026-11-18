# 🎨 Guia de Estilo & Referências de Design — CodeArena
> **Documento de Especificação Visual e UI Design System**  
> **Baseado nas referências:** `ref1.jpg` (WizardZ), `ref2.jpg` (Ruang Edit) e `ref3.jpg` (Awesomic.ai) em `assets/`  
> **Tema do Projeto:** Plataforma EdTech Gamificada para Desenvolvedores

---

## 1. Direção Artística & Conceito Visual

A identidade visual do **CodeArena** une o **Neo-Brutalismo Limpo** (estrutura forte, bordas definidas e alto contraste) ao **Playful Tech / Gamified UI** (cores elétricas, elementos flutuantes 3D e badges interativas).

* **Vibe geral:** Enérgica, moderna, jovem e focada em performance. Foge do padrão corporativo tradicional de TI ("azul tech"), adotando um contraste marcante entre preto profundo, roxo vibrante e verde-limão neon.
* **Sensação transmitida:** "Estou jogando um game competitivo de alta produção enquanto aprendo a programar".

---

## 2. Síntese das Referências Analisadas

```
+---------------------------------------------------------------------------------+
|                               MATRIZ DE REFERÊNCIAS                             |
+---------------------------------------------------------------------------------+
| ref1.jpg (WizardZ)       | • Alto contraste: Preto (#191A23) + Verde-Limão      |
|                          | • Section tags com fundo verde-marca-texto           |
|                          | • Cards modulares com bordas pretas e cantos suaves  |
|                          | • Botões com ícones de seta diagonal (↗)             |
+--------------------------+------------------------------------------------------+
| ref2.jpg (Ruang Edit)    | • Combinação Roxo Elétrico + Verde-Limão Fluorescente|
|                          | • Tipografia com badges e pills inseridos no meio    |
|                          | • Botões 100% arredondados (pills)                   |
|                          | • Cards de planos com bordas coloridas destacadas    |
+--------------------------+------------------------------------------------------+
| ref3.jpg (Awesomic.ai)   | • Bento Grid modular assimétrico                     |
|                          | • Cursores colaborativos estilo multiplayer ("John") |
|                          | • Blocos de números e métricas com visual impactante |
|                          | • Transição entre áreas claras e blocos escuros      |
+---------------------------------------------------------------------------------+
```

---

## 3. Paleta de Cores Oficial (Design Tokens)

A paleta combina alto impacto visual com excelente legibilidade (acessibilidade WCAG AA):

| Token | Nome da Cor | HEX | Tailwind Class Sugerida | Aplicação Principal |
| :--- | :--- | :--- | :--- | :--- |
| **Primary** | Electric Violet | `#5B21B6` / `#6320EE` | `bg-violet-600` / `text-violet-600` | Bordas ativas, cards especiais, acentos de destaque |
| **Accent / Brand** | Cyber Neon Lime | `#CCFF00` / `#B9FF66` | `bg-[#CCFF00]` / `text-[#CCFF00]` | Botões principais (CTAs), badges de nível, destaques |
| **Dark Neutral** | Deep Obsidian | `#121316` / `#18181B` | `bg-[#121316]` / `text-[#121316]` | Títulos principais, botões secundários, cards dark |
| **Card Dark** | Charcoal Dark | `#1E1F24` | `bg-[#1E1F24]` | Fundo dos cards no modo escuro e código |
| **Light Canvas** | Soft Vapor Light | `#F8F7FC` / `#FAFAFC` | `bg-[#F8F7FC]` | Fundo principal da página |
| **Pure White** | Crisp White | `#FFFFFF` | `bg-white` | Fundo de cards claros e superfícies limpas |
| **Border Stroke** | Bold Border Line | `#E2E2EA` / `#121316` | `border-gray-200` / `border-black` | Bordas nítidas de 1.5px a 2px |

---

## 4. Tipografia & Hierarquia de Texto

### Famílias Tipográficas
1. **Fonte Principal (Display & Body):** `Plus Jakarta Sans` ou `Inter` (Google Fonts)
   * Moderna, geométrica, com peso extra-bold excelente para títulos com impacto.
2. **Fonte de Código / Gamificação (Mono):** `JetBrains Mono` ou `Fira Code`
   * Utilizada em badges de XP, snippets de código, elos e números de duelos.

### Escala & Tratamentos Visuais
* **H1 (Hero):** `text-4xl md:text-6xl font-extrabold tracking-tight text-[#121316]`
  * *Efeito Ruang Edit:* Inserir badges em formato de pílula dentro do próprio fluxo da frase.  
    *Exemplo:* `Pare de assistir vídeos ( ⚔️ 1v1 ) e suba de nível codando.`
* **Section Tag / Eyebrow:** `inline-block px-4 py-1.5 rounded-full text-xs font-bold uppercase tracking-wider`
  * *Efeito WizardZ:* Fundo verde-limão (`bg-[#CCFF00]`) com texto preto (`text-black`).
* **Subtítulos:** `text-lg md:text-xl text-gray-600 font-normal leading-relaxed`

---

## 5. Componentes & Padrões de Interface (UI Kit)

### 5.1. Botões de Ação (CTAs)
* **Botão Primário (Vibrante):**
  * Fundo `#CCFF00` (verde neon), texto preto negrito, cantos totalmente arredondados (`rounded-full`).
  * Ícone de seta circular ou espada: `( ↗ )`.
  * Efeito hover: elevação sutil (`-translate-y-0.5`) e sombra nítida neo-brutalista (`shadow-[4px_4px_0px_0px_#121316]`).
* **Botão Secundário (Escuro / Outline):**
  * Fundo `#121316` com texto branco ou fundo branco com borda preta sólida de 2px.

### 5.2. Bento Grid & Cards
* **Cantos:** Arredondamento expressivo (`rounded-3xl` / `rounded-[28px]`).
* **Bordas:** Borda sólida visível (`border-2 border-black` ou `border border-gray-200`).
* **Estilo Alternado (WizardZ):**
  * Card 1: Fundo branco com borda escura.
  * Card 2: Fundo preto `#121316` com texto branco e acento verde-limão.
  * Card 3: Fundo roxo `#6320EE` com texto branco e badges contrastantes.

### 5.3. Elementos Gamificados & Multiplayer (Awesomic / Ruang Edit)
* **Multiplayer Cursors (Awesomic.ai):** Cursors de mouse flutuantes com o nome dos alunos disputando uma partida:
  * Tag azul: `Cursor 1: "Pedro_Dev"`
  * Tag roxa: `Cursor 2: "Bia_Coder"`
* **Badges de XP & Status:**
  * Indicadores tipo `[ Lvl 34 ]`, `[ Elo Ouro ]`, `[ 1.450 XP ]` com tipografia mono e estilo de tag.
* **Estrelas e Brilhos Decorativos:**
  * Símbolos como `✦` e `✳` em verde-limão espalhados sutilmente pelos cantos dos containers.

---

## 6. Estrutura de Layout Recomendada para o `index.html`

```
┌─────────────────────────────────────────────────────────────────┐
│ 1. NAVBAR: Logo + Links + Pill CTA "Jogar Grátis ↗"             │
├─────────────────────────────────────────────────────────────────┤
│ 2. HERO: Título com Badge Inline + Cursors Multiplayer Flutuantes│
│          + Botões de Ação com borda / sombra sólida             │
├─────────────────────────────────────────────────────────────────┤
│ 3. METRICS BANNER: Cards de números (45k devs, 1.2M linhas)     │
├─────────────────────────────────────────────────────────────────┤
│ 4. BENTO GRID (MODOS DE JOGO): 4 cards com estilos contrastantes │
│    - Solo RPG (White Card)   - Arenas 1v1 (Dark Violet Card)    │
│    - Boss Raids (Black Card) - IA Sensei (White Card)           │
├─────────────────────────────────────────────────────────────────┤
│ 5. PRICING: Comparativo de Planos com card PRO em destaque Roxo │
├─────────────────────────────────────────────────────────────────┤
│ 6. FOOTER: Fundo escuro com chamada final e links úteis          │
└─────────────────────────────────────────────────────────────────┘
```

---

## 7. Instruções para o Tailwind CSS (CDN)

Para aplicar este design diretamente no HTML sem compilação local pesada, usaremos a configuração Tailwind via script:

```html
<script src="https://cdn.tailwindcss.com"></script>
<script>
  tailwind.config = {
    theme: {
      extend: {
        colors: {
          brand: {
            lime: '#CCFF00',
            violet: '#6320EE',
            dark: '#121316',
            cardDark: '#1E1F24',
            light: '#F8F7FC'
          }
        },
        boxShadow: {
          'brutal': '4px 4px 0px 0px #121316',
          'brutal-lime': '4px 4px 0px 0px #CCFF00',
        }
      }
    }
  }
</script>
```
