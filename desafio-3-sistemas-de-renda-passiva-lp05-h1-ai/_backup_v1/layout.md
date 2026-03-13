# Layout Specification - Desafio Os 3 Sistemas da Renda Passiva

---

## Linguagem Visual Global (extraida do design aprovado)

### Paleta de Cores
- **Orange-500 (brand):** #E8601C
- **Orange-400:** #F07A3A
- **Orange-600:** #C94F12
- **Orange-glow:** rgba(232, 96, 28, 0.15)
- **Black:** #0A0A0A
- **Gray-950:** #111111
- **Gray-900:** #1A1A1A
- **Gray-800:** #252525
- **Gray-700:** #333333
- **Gray-600:** #555555
- **Gray-400:** #999999
- **Gray-300:** #B3B3B3
- **Gray-200:** #D4D4D4
- **White:** #FAFAFA

### Font Pairing
- **Heading:** DM Serif Display (serif) - pesos: regular, italic
- **Body:** DM Sans (sans-serif) - pesos: 400, 500, 700

### Espacamentos Base
- xs: 0.5rem | sm: 1rem | md: 1.5rem | lg: 2.5rem | xl: 4rem | 2xl: 6rem | 3xl: 8rem

### Container
- Max: 1280px | Narrow: 960px | Padding lateral: 1.5rem

### Tom Geral
- Dark mode com laranja quente como acento
- Tipografia grande e dramatica (serif) para headlines
- Elementos float/overlap para profundidade
- Transicoes suaves, cubic-bezier elegantes
- Linhas decorativas e glow effects sutis

---

## Secao 1: HERO (JA IMPLEMENTADA)

### Arquetipo e Constraints
- Arquetipo: Split Assimetrico (70/30)
- Constraints: Headline >150px, Dark Mode, Overlap Elements
- Ja implementada e aprovada no design. MANTER EXATAMENTE COMO ESTA.

---

## Secao 2: PROVA SOCIAL - DEPOIMENTOS (JA IMPLEMENTADA)

### Arquetipo e Constraints
- Arquetipo: Floating Cards
- Constraints: Dark Mode, Diagonal Divider, Hover Lift
- Ja implementada e aprovada no design. MANTER EXATAMENTE COMO ESTA.

---

## Secao 3: CRONOGRAMA DAS AULAS

### Arquetipo e Constraints
- Arquetipo: Scroll Storytelling (Timeline vertical narrativa)
- Constraints: Sticky Element, Stagger Animation, Selective Color, Bleed Left
- Justificativa: O cronograma e uma narrativa sequencial de 5 dias. Uma timeline vertical com o titulo sticky no lado esquerdo e os cards de aula aparecendo em sequencia no lado direito cria ritmo e progressao. O sticky element mantem o contexto temporal visivel enquanto o usuario avanca pela jornada. Contrasta com o grid de cards da secao anterior.

### Conteudo
- Eyebrow: UM DESAFIO DE
- Headline: 5 DIAS PARA MUDAR SUA TRAJETORIA FINANCEIRA
- Aula 1:
  - Tag: AULA 1
  - Data: 23 DE MARCO, AS 20H (DOMINGO)
  - Titulo: OS FUNDAMENTOS DA CONSTRUCAO DE PATRIMONIO
  - Paragrafo: Voce vai entender por que a maioria dos profissionais que ganham acima de R$ 20 mil continuam presos na corrida do dinheiro, enquanto 0,01% esta construindo patrimonio e renda passiva para usar o tempo com quem mais importa. A partir daqui, voce entendera o "meta-sistema" que combina decisao, estruturacao e multiplicacao para criar patrimonio de forma inevitavel, mesmo em um Brasil ciclico, inseguro e inflacionario.
- Aula 2:
  - Tag: AULA 2
  - Data: 24 DE MARCO, AS 20H (SEGUNDA-FEIRA)
  - Titulo: O CANVA DA CONSTRUCAO DE PATRIMONIO
  - Paragrafo: Nesta aula, voce vai descobrir como a combinacao dos 3 motores – Aporte Mensal, Reserva de Valor e Capacidade de Pagamento – determinam sua velocidade rumo a liberdade financeira. Voce vai enxergar, com clareza absoluta, para onde o seu dinheiro deve ir e como reorganizar sua vida financeira para construir ativos muito antes de pensar em investir.
- Aula 3:
  - Tag: AULA 3
  - Data: 25 DE MARCO, AS 20H (TERCA-FEIRA)
  - Titulo: OS TRES SISTEMAS DE RENDA PASSIVA
  - Paragrafo: Voce vai acessar a verdadeira arquitetura da liberdade por meio dos:
  - Bullet 1: Sistema de Decisao: para pensar como milionarios e bilionarios e tomar decisoes melhores quando o assunto e dinheiro e investimentos.
  - Bullet 2: Sistema de Estruturacao: para otimizar o que voce ja tem, permitindo investir mais sem precisar ganhar mais, acelerando a sua construcao de patrimonio e renda passiva.
  - Bullet 3: Sistema de Multiplicacao: para comprar os ativos certos que vao multiplicar seu patrimonio e substituir voce na geracao de renda.
- Aula 4:
  - Tag: AULA 4
  - Data: 26 DE MARCO, AS 20H (QUARTA-FEIRA)
  - Titulo: O SISTEMA DE MULTIPLICACAO: A MAQUINA PATRIMONIAL
  - Paragrafo: Esse e o momento de conhecer a estrategia mais poderosa da metodologia para gerar multiplos picos de ganho de capital com baixos aportes mensais, sem precisar de imoveis, tudo de maneira previsivel e sem se arriscar. Voce vai aprender a estrategia de alavancagem patrimonial usando o mecanismo mais seguro e negligenciado pela alta renda brasileira.
- Aula 5:
  - Tag: AULA 5
  - Data: 27 DE MARCO, AS 20H (QUINTA-FEIRA)
  - Titulo: ALAVANCAGEM COM IMOVEIS
  - Paragrafo: No ultimo dia, voce vai descobrir como transformar imoveis quitados ou subutilizados em ativos autopagantes que geram fluxo de caixa, liquidez e crescimento patrimonial ao mesmo tempo. Essa aula revela a estrategia usada pelas familias mais ricas para "fabricar" renda e clonar patrimonio sem depender de aluguel ou valorizacao lenta do mercado.
- CTA: COMPRAR COM LOTE PROMOCIONAL
- Trust: Os seus dados estao totalmente seguros.

### Layout
- Background: var(--black) (#0A0A0A)
- Secao com padding: 120px 0 (desktop), 80px 0 (mobile)
- Container max-width: 1280px, centrado
- **Estrutura desktop:** Grid 2 colunas - coluna esquerda 380px sticky com headline, coluna direita flex com cards de aula
- **Coluna esquerda (sticky):**
  - position: sticky; top: 120px
  - Contem: eyebrow, headline, uma linha decorativa vertical de 200px abaixo do headline (1px solid var(--gray-800))
  - Alinhado ao topo, acompanha o scroll
- **Coluna direita (cards):**
  - display: flex; flex-direction: column; gap: 0
  - Cards de aula empilhados verticalmente, conectados por uma "timeline line" central
- **Timeline line:** Linha vertical de 2px na margem esquerda (left: 24px relativo ao card), cor var(--gray-800), com pontos circulares nos nodes (width: 12px, height: 12px, border: 2px solid var(--orange-500), background: var(--black))
- **Cada card de aula:**
  - padding-left: 64px (espaco para a timeline line + node)
  - padding: 40px 40px 40px 64px
  - margin-bottom: 0 (sem gap entre cards, a timeline line conecta tudo)
  - border-bottom: 1px solid var(--gray-800) (exceto ultimo card)
- **Bleed left:** A timeline line sangra para alem do container ate a margem esquerda do viewport, criando uma linha decorativa que corre pelo lado esquerdo da tela (feito com ::before da secao, position: absolute, left: 0, width: 1px, background: linear-gradient(to bottom, transparent, var(--gray-800) 10%, var(--gray-800) 90%, transparent))

### Tipografia
- **Eyebrow:** DM Sans, 0.8rem, weight 700, letter-spacing: 0.2em, uppercase, color: var(--orange-500)
- **Headline "5 DIAS...":** DM Serif Display, clamp(2rem, 4vw, 3.2rem), weight 400, line-height: 1.1, color: var(--white). "TRAJETORIA FINANCEIRA" com color: var(--orange-500)
- **Tag "AULA X":** DM Sans, 0.7rem, weight 700, letter-spacing: 0.15em, uppercase, color: var(--orange-500), background: rgba(232, 96, 28, 0.1), padding: 4px 12px, border-radius: 2px, display: inline-block
- **Data:** DM Sans, 0.75rem, weight 500, letter-spacing: 0.1em, uppercase, color: var(--gray-400), margin-top: 8px
- **Titulo da aula:** DM Serif Display, clamp(1.2rem, 2.5vw, 1.6rem), weight 400, line-height: 1.2, color: var(--white), margin-top: 12px
- **Paragrafo:** DM Sans, 0.95rem, weight 400, line-height: 1.7, color: var(--gray-400), margin-top: 12px, max-width: 640px
- **Bullets (aula 3):** DM Sans, 0.9rem, weight 400, line-height: 1.6, color: var(--gray-400). Cada bullet com ::before contendo um dash laranja (content: '—', color: var(--orange-500), margin-right: 8px)

### Cores
- Background secao: var(--black)
- Timeline line: var(--gray-800)
- Timeline nodes: border var(--orange-500), background var(--black)
- Timeline node ATIVO (on scroll): background var(--orange-500), box-shadow: 0 0 20px rgba(232, 96, 28, 0.4)
- Card border-bottom: var(--gray-800)
- Card hover: nenhum efeito hover nos cards (o foco e leitura linear)

### Elementos Visuais
- **Timeline nodes:** Circulos de 12px que ficam no inicio de cada card. Quando o card entra no viewport (IntersectionObserver), o node preenhce com laranja e ganha glow
- **Linha decorativa bleed:** Uma linha vertical de 1px que corre do topo ao final da secao no lado esquerdo absoluto do viewport. Gradient: transparent → var(--gray-800) 10% → var(--gray-800) 90% → transparent
- **Numero do dia:** Atras do titulo de cada aula, um numero grande (DM Serif Display, 8rem, color: rgba(232, 96, 28, 0.04)) como watermark decorativo. Ex: "01", "02", etc. Position: absolute, right: 0, top: -20px

### Animacoes
- **Cards de aula:** data-aos="fade-up", stagger delay de 100ms entre cada card (delay: 0, 100, 200, 300, 400ms)
- **Timeline nodes:** Transicao CSS para fill/glow quando ativo - transition: all 600ms cubic-bezier(0.16, 1, 0.3, 1)
- **Headline sticky:** Aparece normalmente sem animacao (ja visivel quando usuario chega na secao)
- **Numeros watermark:** opacity transition de 0.02 para 0.06 quando o card correspondente entra no viewport, transition 800ms ease

### Interatividade
- **Scroll behavior:** A coluna esquerda com o headline fica sticky enquanto usa rola os cards das aulas
- **Active state dos nodes:** O node da aula que esta no viewport fica preenchido com laranja. Controlado por IntersectionObserver com threshold: 0.5
- CTA no final: mesmo estilo do btn-primary do hero
- Trust text: mesmo estilo do hero__trust

### Responsividade
- **<= 1024px:** Grid muda para 1 coluna. Headline nao e mais sticky (position: relative). Timeline line e nodes permanecem
- **<= 768px:** Padding secao: 60px 0. Tags e datas ficam menores (0.65rem). Padding-left dos cards: 48px. Timeline node: 10px
- **<= 480px:** Headline: clamp(1.6rem, 7vw, 2rem). Titulo aula: 1.1rem. Numeros watermark: hidden

---

## Secao 4: PROVA SOCIAL - RESULTADOS

### Arquetipo e Constraints
- Arquetipo: Scroll Horizontal (Carousel lateral infinito)
- Constraints: Overflow Visible, Noise Texture, Bleed Both, Fade Left/Right
- Justificativa: A secao de resultados precisa mostrar volume sem ser repetitiva. Um carrossel horizontal infinite-scroll (marquee) diz "temos muito mais" sem precisar mostrar tudo. Contrasta totalmente com a timeline vertical da secao anterior. A textura de noise sutil e o overflow visivel criam profundidade.

### Conteudo
- Eyebrow: CINCO AULAS PARA VOCE ALCANCAR O QUE
- Headline: NOSSOS CLIENTES JA ALCANCARAM
- Nota para dev: [INSERIR MAIS DEPOIMENTOS E PRINTS DE RESULTADOS AQUI - usar placeholders por enquanto]
- Placeholders sugeridos: 6-8 cards com textos curtos de resultados (usar mesmos depoimentos da secao 2 como placeholder, acrescentando resultados ficticios para preencher visualmente)

### Layout
- Background: var(--gray-950) (#111111)
- Padding: 100px 0 (desktop), 60px 0 (mobile)
- **Header:** Centrado com container max-width: 960px (narrow). Margin-bottom: 60px
- **Carrossel area:** Full-width, overflow: hidden no container pai, mas os cards sangram (overflow: visible nos filhos)
- **Marquee row:** display: flex; gap: 24px; animation: marquee linear infinite
- **2 rows de marquee:** Uma movendo para esquerda, outra para direita (direcoes opostas), com gap vertical de 24px
- **Cada card do marquee:**
  - width: 340px (fixo, nao encolhe)
  - flex-shrink: 0
  - background: var(--gray-900)
  - border: 1px solid var(--gray-800)
  - border-radius: 12px
  - padding: 32px
- **Fade edges:** Pseudo-elementos ::before e ::after no container do marquee, position: absolute, top: 0, bottom: 0, width: 120px, z-index: 3. ::before left: 0 com gradient: linear-gradient(to right, var(--gray-950), transparent). ::after right: 0 com gradient reverso
- **Noise texture:** Overlay em toda a secao com background-image usando SVG noise (feTurbulence), opacity: 0.03, pointer-events: none, mix-blend-mode: overlay

### Tipografia
- **Eyebrow:** DM Sans, 0.8rem, weight 700, letter-spacing: 0.2em, uppercase, color: var(--gray-400)
- **Headline:** DM Serif Display, clamp(1.8rem, 4vw, 3rem), weight 400, line-height: 1.15, color: var(--white). "JA ALCANCARAM" em color: var(--orange-500)
- **Card texto:** DM Sans, 0.9rem, weight 400, line-height: 1.6, color: var(--gray-300), font-style: italic
- **Card nome:** DM Sans, 0.85rem, weight 700, color: var(--white)

### Cores
- Background: var(--gray-950)
- Cards: background var(--gray-900), border var(--gray-800)
- Fade masks: gradient de var(--gray-950) para transparent

### Elementos Visuais
- **Aspas decorativas:** Mesma abordagem da secao 2 (::before com "\201C", DM Serif Display 3rem, color var(--orange-500), opacity 0.15)
- **Avatar iniciais:** Circulo 36px, gradient laranja, iniciais em branco (igual secao 2 mas menor)
- **Noise overlay:** SVG filter com feTurbulence type="fractalNoise" baseFrequency="0.65" numOctaves="3", aplicado como background pseudo-elemento, 100% width/height, opacity 0.03
- **Divider superior:** Sem clip-path diagonal. Usar uma linha horizontal simples: border-top: 1px solid var(--gray-800) com um fade nas pontas (gradient mask)

### Animacoes
- **Marquee row 1:** @keyframes marquee { from { transform: translateX(0); } to { transform: translateX(-50%); } } - duration: 40s, linear, infinite. Os cards sao duplicados no HTML para criar loop seamless
- **Marquee row 2:** Mesma animacao mas: animation-direction: reverse; duration: 45s (velocidade levemente diferente para ritmo organico)
- **Header:** data-aos="fade-up"
- **Hover nos cards:** transform: scale(1.03), transition 300ms ease. animation-play-state: paused no marquee inteiro quando qualquer card recebe hover (JS ou CSS :has())

### Interatividade
- **Pause on hover:** Quando o mouse esta sobre a area do marquee, a animacao pausa para permitir leitura. CSS: `.marquee-row:hover { animation-play-state: paused; }`
- **Nenhum drag/swipe:** O movimento e automatico, cria sensacao de volume infinito

### Responsividade
- **<= 1024px:** Card width: 300px. Gap: 20px. Fade width: 80px
- **<= 768px:** Apenas 1 row de marquee (esconder a segunda). Card width: 280px. Duration: 30s
- **<= 480px:** Card width: 260px. Padding card: 24px. Fade width: 40px

---

## Secao 5: OFERTA - STACK DE VALOR

### Arquetipo e Constraints
- Arquetipo: Single Focus (foco unico na oferta, sem distracao)
- Constraints: Glassmorphism, Gradiente Radial, Container Narrow, Hover Glow
- Justificativa: A oferta precisa de foco total. Um container centralizado com glassmorphism cria "premium". O gradiente radial no background direciona o olho para o centro. O container narrow evita que o olho se perca. Contrasta com o scroll horizontal da secao anterior.

### Conteudo
- Eyebrow: TUDO QUE VOCE IRA RECEBER
- Headline: AO PARTICIPAR DO DESAFIO:
- Itens da stack:
  1. Ingresso para os 5 dias do Desafio Os 3 Sistemas — ~~R$ 1.297~~
  2. Area de membros exclusiva com gravacoes e materiais — ~~R$ 349~~
  3. Comunidade privada no WhatsApp — ~~R$ 300~~
  4. Networking e conexao com profissionais de alta renda que buscam o mesmo que voce — ~~R$ 198~~
  5. Guia: Como mapear seus 3 motores patrimoniais e acelerar a renda passiva — ~~R$ 167~~
  6. Material complementar utilizado em cada aula — ~~R$ 150~~
  7. Total: R$ 2.461
- De: ~~R$ 2.461~~
- Headline preco: POR APENAS
- Preco destaque: R$ 97,00
- CTA: COMPRAR COM LOTE PROMOCIONAL
- Badge urgencia: Vagas limitadas!

### Layout
- Background: var(--black) com radial-gradient centralizado: radial-gradient(ellipse at center, rgba(232, 96, 28, 0.06) 0%, transparent 60%)
- Padding secao: 120px 0 (desktop), 80px 0 (mobile)
- **Container principal:** max-width: 720px, centrado
- **Header:** Centrado, margin-bottom: 48px
- **Card da oferta (glass):**
  - background: rgba(26, 26, 26, 0.7)
  - backdrop-filter: blur(20px)
  - -webkit-backdrop-filter: blur(20px)
  - border: 1px solid rgba(255, 255, 255, 0.06)
  - border-radius: 16px
  - padding: 48px (desktop), 32px (mobile)
  - position: relative
  - overflow: hidden
- **Glow decorativo no card:** Pseudo-elemento ::before, position: absolute, top: -100px, right: -100px, width: 300px, height: 300px, border-radius: 50%, background: radial-gradient(circle, rgba(232, 96, 28, 0.08), transparent 70%), pointer-events: none
- **Lista de itens:**
  - Cada item e uma row com flexbox: justify-content: space-between
  - Separador entre itens: border-bottom: 1px solid var(--gray-800)
  - Padding vertical por item: 18px 0
  - O ultimo item (Total) tem border-top: 2px solid var(--orange-500) ao inves de border-bottom, padding-top: 24px, margin-top: 8px
- **Bloco de preco:** Centrado abaixo do card, margin-top: 48px
  - "De R$ 2.461" riscado centrado acima
  - "POR APENAS" em texto pequeno centrado
  - "R$ 97,00" em destaque absoluto, centrado
  - CTA abaixo centralizado
  - Badge urgencia abaixo do CTA

### Tipografia
- **Eyebrow:** DM Sans, 0.8rem, weight 700, letter-spacing: 0.2em, uppercase, color: var(--gray-400)
- **Headline "AO PARTICIPAR...":** DM Serif Display, clamp(1.6rem, 3.5vw, 2.4rem), weight 400, line-height: 1.15, color: var(--white)
- **Itens da lista (nome):** DM Sans, 0.95rem, weight 400, color: var(--gray-300), line-height: 1.5
- **Itens da lista (preco riscado):** DM Sans, 0.9rem, weight 500, color: var(--gray-600), text-decoration: line-through
- **Item Total (nome):** DM Sans, 1rem, weight 700, color: var(--white)
- **Item Total (valor):** DM Sans, 1.1rem, weight 700, color: var(--white)
- **De (riscado):** DM Sans, 1rem, weight 400, color: var(--gray-600), text-decoration: line-through
- **"POR APENAS":** DM Sans, 0.8rem, weight 700, letter-spacing: 0.15em, uppercase, color: var(--gray-400)
- **Preco destaque "R$ 97,00":** DM Serif Display, clamp(3rem, 8vw, 5rem), weight 400, color: var(--orange-500), line-height: 1
- **Badge urgencia:** DM Sans, 0.75rem, weight 700, color: var(--orange-500), letter-spacing: 0.05em, uppercase

### Cores
- Background secao: var(--black) + radial gradient laranja sutil
- Card glass: rgba(26, 26, 26, 0.7) com blur
- Card border: rgba(255, 255, 255, 0.06)
- Separadores lista: var(--gray-800)
- Total border: var(--orange-500)
- Preco destaque: var(--orange-500)

### Elementos Visuais
- **Gradient radial de fundo:** Cria um "spotlight" sutil centralizado na secao, atraindo o olhar para o card da oferta
- **Glow no canto do card:** Pseudo-elemento circular laranja sutil no canto superior direito
- **Linha decorativa acima do total:** 2px solid var(--orange-500), full width no card, separando visualmente o somatoria do total
- **Checkmark nos itens:** A esquerda de cada item, um pequeno checkmark com circulo (width: 20px, height: 20px, border-radius: 50%, background: rgba(232, 96, 28, 0.12), com SVG checkmark 10px em var(--orange-500))

### Animacoes
- **Card inteiro:** data-aos="fade-up"
- **Itens da lista:** Stagger animation, cada item aparece com fade-up e delay de 80ms (controlado via CSS custom property --delay ou AOS data-aos-delay)
- **Preco destaque:** Counter animation de R$ 2.461 para R$ 97,00 quando entra no viewport. Ou, mais simples: o preco aparece com scale-in (scale(0.8) → scale(1)) + fade, 600ms ease-out
- **Badge urgencia:** Mesma animacao pulsante do hero (urgencyPulse keyframes ja definidos)
- **Glow do card:** Animacao sutil de respiro, opacity 0.06 → 0.12, 4s ease-in-out infinite

### Interatividade
- **Hover no card:** Border muda para rgba(255, 255, 255, 0.1), transition 400ms
- **Hover nos itens:** Leve highlight - background: rgba(255, 255, 255, 0.02), transition 200ms
- CTA: mesmo btn-primary com hover translate + glow + shimmer

### Responsividade
- **<= 768px:** Padding card: 28px. Lista itens: flex-direction column (nome em cima, preco embaixo). Preco destaque: clamp(2.5rem, 10vw, 3.5rem)
- **<= 480px:** Padding card: 20px. Checkmarks hidden (exibir so o texto). Padding secao: 60px 0

---

## Secao 6: GARANTIA

### Arquetipo e Constraints
- Arquetipo: Isolated Element (elemento unico com muito espaco ao redor)
- Constraints: Duocromatico, Container Narrow, Skewed Section (skew sutil)
- Justificativa: Garantia precisa transmitir confianca e simplicidade. Um unico bloco centrado com muito respiro ao redor. O skew sutil no background cria separacao visual. A abordagem duocromatica (preto + laranja) reforca a seriedade. Contrasta com a secao de oferta mais densa.

### Conteudo
- Headline: GARANTIA INCONDICIONAL DE 30 DIAS
- Paragrafo: Participe das aulas. Se nao fizer sentido para voce, basta enviar uma unica mensagem em ate 30 dias para nossa equipe e o seu investimento sera 100% devolvido.

### Layout
- **Background da secao:** var(--gray-950), com um pseudo-elemento de fundo levemente skewed: transform: skewY(-1.5deg), background: var(--gray-950), que cobre a area mas cria um angulo sutil nas bordas (o conteudo fica com transform: skewY(1.5deg) para compensar e ficar reto)
- Padding: 100px 0 (desktop), 60px 0 (mobile)
- **Container:** max-width: 720px, centrado
- **Bloco de garantia:**
  - display: flex; align-items: center; gap: 48px;
  - **Lado esquerdo:** Icone de escudo/selo grande
  - **Lado direito:** Headline + paragrafo
- **Icone de garantia (lado esquerdo):**
  - SVG de escudo com checkmark interno
  - width: 100px, height: 100px, flex-shrink: 0
  - stroke: var(--orange-500), stroke-width: 1.5, fill: none
  - Dentro do escudo, um checkmark com fill: var(--orange-500)
  - Circulo de glow atras: width: 140px, height: 140px, border-radius: 50%, background: radial-gradient(circle, rgba(232, 96, 28, 0.1), transparent 70%)

### Tipografia
- **Headline:** DM Serif Display, clamp(1.4rem, 3vw, 2rem), weight 400, line-height: 1.2, color: var(--white)
- **"30 DIAS"** dentro do headline: color: var(--orange-500)
- **Paragrafo:** DM Sans, 1rem, weight 400, line-height: 1.7, color: var(--gray-400)
- **"100% devolvido"** em negrito: weight 700, color: var(--gray-300)

### Cores
- Background secao: var(--gray-950) (pseudo-elemento skewed)
- Escudo: stroke var(--orange-500)
- Glow atras do escudo: rgba(232, 96, 28, 0.1)
- Texto: var(--white) headline, var(--gray-400) paragrafo

### Elementos Visuais
- **Escudo SVG:** Forma de escudo classica com cantos arredondados e checkmark centralizado
- **Glow radial:** Circulo suave atras do escudo
- **Border accent:** Uma borda esquerda de 3px solid var(--orange-500) no bloco inteiro, criando conexao visual com a barra de info do hero

### Animacoes
- **Bloco inteiro:** data-aos="fade-up"
- **Escudo:** Entrance com scale animation - scale(0.8) → scale(1), opacity 0 → 1, 800ms ease-out, delay 200ms
- **Glow do escudo:** Breathe animation: opacity 0.08 → 0.15, 3s ease-in-out infinite

### Interatividade
- Nenhuma interatividade especial. Secao de confianca, so leitura.

### Responsividade
- **<= 768px:** Flex direction column, text-align center. Escudo margin-bottom: 24px. Border-left removido, border-top: 3px solid var(--orange-500) ao inves. Headline: clamp(1.3rem, 5vw, 1.6rem)
- **<= 480px:** Escudo: 80px. Padding secao: 48px 0

---

## Secao 7: ESPECIALISTA

### Arquetipo e Constraints
- Arquetipo: Editorial (layout de revista com tipografia elaborada)
- Constraints: Split Vertical (50/50), Imagem com Overlay gradiente, Mixed Weights (contraste tipografico), Texto com Gradiente
- Justificativa: O bloco do especialista merece tratamento editorial premium, como perfil de revista. Split 50/50 com foto de um lado e bio do outro cria equilibrio e seriedade. A tipografia elaborada com pesos contrastantes (DM Serif Display grande + DM Sans regular) reforca o tom profissional. Contrasta com o minimalismo da secao de garantia.

### Conteudo
- Eyebrow: QUEM VAI TE CONDUZIR NESSA JORNADA
- Headline: ADRIAN CARVALHO
- Instagram: @adriancarvalho
- Bio 1: Adrian Carvalho e planejador financeiro e patrimonial com certificacao internacional CFP, fundador da Quartavia, um ecossistema de Construcao Patrimonial com mais de 13 empresas no Brasil e Exterior, e que acompanha individualmente mais de 2.200 familias de alta renda no Brasil.
- Bio 2: Com vasta experiencia pratica em construcao de patrimonio, Adrian nao ensina teoria financeira: ele implementa junto. Cada estrategia que compartilha e testada em operacoes reais: incorporacao de casas de alto padrao, leiloes de imoveis, ativos autopagantes, com mais de 20 mecanismos de renda passiva que ele utiliza em seu proprio patrimonio.
- Bio 3: Ja atuou no mercado financeiro e hoje se dedica exclusivamente a mostrar o Quarto Caminho: a rota que permite a profissionais de alta renda construir, em ate 7 anos, um patrimonio gerador de renda passiva que os sustenta pelo resto da vida, sem depender de sorte, de gerentes de banco ou de assessores que vendem o mesmo remedio para todo mundo.
- Bio 4: E CEO da Quartavia, Planejador Patrimonial e o arquiteto do metodo "O Quarto Caminho" que mais de 2.200 familias ja confiaram para transformar renda ativa em liberdade financeira e de tempo.
- CTA: APROVEITAR LOTE PROMOCIONAL
- Trust: Os seus dados estao totalmente seguros.

### Layout
- Background: var(--black) (#0A0A0A)
- Padding: 120px 0 (desktop), 80px 0 (mobile)
- Container max-width: 1280px, centrado
- **Estrutura:** Grid 2 colunas, grid-template-columns: 1fr 1fr, gap: 80px, align-items: center
- **Coluna esquerda (imagem):**
  - Placeholder de imagem do Adrian (usar um bloco visual placeholder)
  - **Placeholder sugerido:** Retangulo com aspect-ratio: 3/4, background: linear-gradient(135deg, var(--gray-900), var(--gray-800)), border-radius: 12px, overflow: hidden
  - **Overlay gradient na imagem:** ::after com linear-gradient(to top, var(--black) 0%, transparent 40%), position absolute, inset 0
  - **Moldura decorativa:** Um retangulo de border de 1px solid var(--orange-500), offset de 16px do canto (position: absolute, top: -16px, right: -16px, width: calc(100% - 16px), height: calc(100% - 16px), border: 1px solid rgba(232, 96, 28, 0.3), border-radius: 12px, z-index: -1)
  - **Tag Instagram:** Posicionada absolute no bottom-left da imagem, background: rgba(0,0,0,0.6), backdrop-filter: blur(8px), padding: 8px 16px, border-radius: 4px, bottom: 24px, left: 24px
- **Coluna direita (bio):**
  - Eyebrow, Headline, seguidos dos paragrafos de bio
  - Margin-bottom entre headline e primeiro paragrafo: 32px
  - Gap entre paragrafos: 20px
  - O primeiro paragrafo tem um "drop cap" visual sutil: primeira letra com font-size: 2.5rem, DM Serif Display, color var(--orange-500), float: left, margin-right: 8px, line-height: 1
  - CTA e trust no final da coluna direita

### Tipografia
- **Eyebrow:** DM Sans, 0.8rem, weight 700, letter-spacing: 0.2em, uppercase, color: var(--gray-400)
- **Headline "ADRIAN CARVALHO":** DM Serif Display, clamp(2rem, 4.5vw, 3.5rem), weight 400, line-height: 1.05, color: var(--white)
- **Instagram handle:** DM Sans, 0.85rem, weight 500, color: var(--orange-500), margin-top: 8px
- **Bio paragrafos:** DM Sans, 0.95rem, weight 400, line-height: 1.75, color: var(--gray-400)
- **Destaques no texto:** "certificacao internacional CFP", "mais de 2.200 familias", "mais de 13 empresas", "ate 7 anos" em weight 500, color: var(--gray-300)
- **Drop cap (primeiro paragrafo):** DM Serif Display, 2.5rem, color: var(--orange-500), float: left

### Cores
- Background: var(--black)
- Moldura decorativa: rgba(232, 96, 28, 0.3)
- Overlay imagem: gradient de var(--black) para transparent
- Instagram tag bg: rgba(0,0,0,0.6)

### Elementos Visuais
- **Moldura offset:** Retangulo deslocado atras da imagem, cria profundidade editorial
- **Drop cap:** Primeira letra grande e colorida no estilo de revista
- **Separador sutil:** Linha horizontal de 60px, 2px solid var(--orange-500), abaixo do headline, antes dos paragrafos
- **Quote marks:** Aspas decorativas sutis (opacity 0.05) atras do bloco de bio, font-size: 20rem, position: absolute

### Animacoes
- **Imagem:** data-aos="fade-up" com delay 0
- **Moldura offset:** data-aos="fade-up" com delay 200ms
- **Eyebrow + Headline:** data-aos="fade-up" com delay 100ms
- **Paragrafos:** data-aos="fade-up" com stagger delay 100ms cada
- **Drop cap:** Entrance com color transition - comeca em var(--gray-600) e transiciona para var(--orange-500) em 600ms quando visivel

### Interatividade
- **Hover na imagem:** Overlay escurece um pouco mais (opacity muda de 0 para 0.1), moldura offset move 4px (top: -20px, right: -20px), transition 400ms ease
- **Instagram tag hover:** Background fica mais opaco (rgba(0,0,0,0.8)), cursor pointer
- CTA: btn-primary padrao

### Responsividade
- **<= 1024px:** Grid 1 coluna. Imagem primeiro, bio depois. Imagem max-width: 500px centrada. Moldura offset: hidden (display: none). Gap: 48px
- **<= 768px:** Imagem max-width: 100%. Padding secao: 60px 0. Drop cap: hidden (nao usar). Headline: clamp(1.6rem, 7vw, 2.2rem)
- **<= 480px:** Padding secao: 48px 0

---

## Secao 8: FAQ

### Arquetipo e Constraints
- Arquetipo: Reveal on Demand (conteudo aparece com interacao)
- Constraints: Container Narrow, Selective Color, Clip Reveal
- Justificativa: FAQ e conteudo de consulta, nao de leitura continua. O formato de reveal (accordion customizado) e o melhor padrao UX. Mas em vez de um accordion generico, usamos clip-path reveal para animar a abertura, criando uma experiencia mais sofisticada. O container narrow foca a leitura. Contrasta com o layout editorial da secao anterior.

### Conteudo
- Headline: PERGUNTAS FREQUENTES
- Q1: O evento sera ao vivo? → Sim. As aulas acontecem ao vivo no Zoom, sempre as 20h. Voce podera fazer perguntas em tempo real.
- Q2: Qual a duracao das aulas? → Em media 90 minutos por aula, com conteudo denso, objetivo e sem enrolacao.
- Q3: Terei acesso as gravacoes? → Nao. Para manter a qualidade do evento ao vivo, que depende da participacao ativa dos alunos, nao vamos disponibilizar a gravacao das aulas.
- Q4: Isso e um curso ou outro produto de informacao? → Nao. O Desafio Os 3 Sistemas e um evento imersivo de 5 dias projetado para entregar o mapa completo de construcao patrimonial, e apresentar o Programa Pharus, nosso programa de implementacao individual, para quem quiser dar o proximo passo com acompanhamento direto.
- Q5: Por onde recebo o acesso as aulas? → Ao finalizar a inscricao, voce recebe por e-mail o acesso a Comunidade Privada no WhatsApp. Dentro dela, voce recebe o link das aulas e todas as informacoes importantes do evento.

### Layout
- Background: var(--gray-950) (#111111)
- Padding: 100px 0 (desktop), 60px 0 (mobile)
- Container max-width: 720px, centrado
- **Header:** Centrado, margin-bottom: 48px
- **FAQ items:** Lista vertical, cada item e um bloco:
  - border-bottom: 1px solid var(--gray-800)
  - padding: 24px 0
  - O primeiro item tem border-top: 1px solid var(--gray-800) tambem
- **Pergunta (trigger):**
  - display: flex; justify-content: space-between; align-items: center
  - cursor: pointer
  - padding-right: 16px (espaco para o icone)
  - **Icone toggle:** SVG de "+" que rotaciona para "x" quando aberto (ou um chevron que gira 180deg)
    - Width/height: 24px
    - stroke: var(--gray-400), stroke-width: 2
    - transition: transform 400ms cubic-bezier(0.16, 1, 0.3, 1), color 300ms
    - Quando aberto: transform: rotate(45deg) (se for +) ou rotate(180deg) (se for chevron), color: var(--orange-500)
- **Resposta (conteudo):**
  - max-height: 0, overflow: hidden quando fechado
  - max-height: 300px quando aberto (transition: max-height 500ms cubic-bezier(0.16, 1, 0.3, 1))
  - padding-top: 16px quando aberto, 0 quando fechado
  - Clip reveal: clip-path: inset(0 0 100% 0) quando fechado → clip-path: inset(0) quando aberto, transition 500ms

### Tipografia
- **Headline "PERGUNTAS FREQUENTES":** DM Serif Display, clamp(1.6rem, 3.5vw, 2.4rem), weight 400, line-height: 1.15, color: var(--white), text-align: center
- **Perguntas:** DM Sans, 1rem, weight 700, color: var(--white), line-height: 1.4
- **Respostas:** DM Sans, 0.95rem, weight 400, color: var(--gray-400), line-height: 1.7

### Cores
- Background: var(--gray-950)
- Borders: var(--gray-800)
- Pergunta text: var(--white)
- Pergunta hover: sem mudanca de cor no texto, mas icone muda para var(--orange-500)
- Resposta text: var(--gray-400)
- Icone default: var(--gray-400)
- Icone aberto: var(--orange-500)

### Elementos Visuais
- **Icone toggle (+/x):** Construido com 2 spans em formato de cruz (+). Quando aberto, a span horizontal fade out e a vertical gira 90deg → visualmente vira de + para -. Ou usar approach simples de SVG chevron que gira
- **Accent dot:** A esquerda de cada pergunta, um ponto de 6px circular var(--orange-500) (margin-right: 16px), indicando que e clicavel
- **Separador entre header e items:** Linha horizontal de 40px centrada, 2px solid var(--orange-500), margin-bottom: 32px

### Animacoes
- **FAQ items:** data-aos="fade-up" com stagger delay de 80ms
- **Abertura da resposta:** clip-path transition de inset(0 0 100% 0) para inset(0), 500ms cubic-bezier(0.16, 1, 0.3, 1). Combinado com max-height transition para fallback
- **Icone:** rotate transition 400ms
- **Hover na pergunta:** O accent dot escala para 1.3x, transition 200ms

### Interatividade
- **Click na pergunta:** Toggle open/close da resposta. JavaScript simples que adiciona/remove classe `.faq-item--active`
- **Um de cada vez:** Quando uma pergunta abre, as outras fecham (accordion behavior)
- **Hover na pergunta:** Cursor pointer. Accent dot escala. Icone muda cor para laranja (preview do clique)
- **Keyboard:** Enter/Space togglam o FAQ item (acessibilidade com role="button" e aria-expanded)

### Responsividade
- **<= 768px:** Padding secao: 48px 0. Perguntas: 0.95rem. Accent dot: hidden (simplificar). Headline: clamp(1.4rem, 6vw, 1.8rem)
- **<= 480px:** Padding items: 20px 0

---

## Secao 9: ATENDIMENTO

### Arquetipo e Constraints
- Arquetipo: Contained Center (container central compacto)
- Constraints: Color Blocking, Hover Fill, Container Narrow
- Justificativa: Secao de suporte deve ser visivel mas compacta. Um bloco centrado com color blocking (fundo laranja, escuro ao redor) cria destaque imediato e sensacao de "acao". Contrasta completamente com o FAQ cinza/neutro.

### Conteudo
- Headline: EM CASO DE DUVIDAS, FALE COM A NOSSA EQUIPE
- CTA: QUERO FALAR COM O ATENDIMENTO

### Layout
- Background secao: var(--black) (#0A0A0A)
- Padding: 80px 0 (desktop), 48px 0 (mobile)
- **Container:** max-width: 800px, centrado
- **Bloco de atendimento:**
  - background: linear-gradient(135deg, var(--orange-600), var(--orange-500))
  - border-radius: 16px
  - padding: 56px 48px
  - text-align: center
  - position: relative
  - overflow: hidden

### Tipografia
- **Headline:** DM Serif Display, clamp(1.3rem, 3vw, 1.8rem), weight 400, line-height: 1.3, color: var(--white)
- **CTA:** DM Sans, 0.9rem, weight 700, letter-spacing: 0.08em, uppercase

### Cores
- Background do bloco: gradient de var(--orange-600) para var(--orange-500)
- Headline: var(--white)
- CTA button em estilo invertido:
  - background: var(--white)
  - color: var(--orange-500)
  - border: none
  - hover: background: var(--black), color: var(--white)

### Elementos Visuais
- **Pattern decorativo:** Pseudo-elemento com circles ou dots em low opacity dentro do bloco laranja. Implementar com radial-gradient repeating: background: radial-gradient(circle, rgba(255,255,255,0.05) 1px, transparent 1px); background-size: 20px 20px
- **Icone WhatsApp:** SVG do WhatsApp ao lado do headline ou dentro do CTA, width: 20px, fill: currentColor

### Animacoes
- **Bloco inteiro:** data-aos="fade-up"
- **CTA hover:** Hover Fill effect - ::before com background var(--black) desliza da esquerda para direita (left: -100% → left: 0, width: 100%, height: 100%, transition: left 400ms ease). Text color muda de var(--orange-500) para var(--white) via z-index

### Interatividade
- CTA abre link do WhatsApp (href="https://wa.me/NUMERO")
- Hover no CTA: fill animation de escuro

### Responsividade
- **<= 768px:** Padding bloco: 40px 32px. Headline: 1.2rem
- **<= 480px:** Padding bloco: 32px 24px. CTA full width. Headline: 1.1rem

---

## Secao 10: FOOTER

### Arquetipo e Constraints
- Arquetipo: Minimal (pouquissimos elementos)
- Constraints: Low Contrast, Container Narrow
- Justificativa: Footer deve ser discreto, so informacao legal. Minimo possivel de elementos.

### Conteudo
- Texto: (c) 2026 Desafio 3 Sistemas — Todos os direitos reservados.

### Layout
- Background: var(--black)
- Padding: 40px 0
- Container max-width: 1280px, centrado
- **Borda superior:** 1px solid var(--gray-800)
- Texto centrado

### Tipografia
- DM Sans, 0.8rem, weight 400, color: var(--gray-600), text-align: center

### Cores
- Background: var(--black)
- Border-top: var(--gray-800)
- Text: var(--gray-600)

### Animacoes
- Nenhuma

### Interatividade
- Nenhuma

### Responsividade
- Sem mudancas. Funciona em todos os breakpoints.

---

## Mapa de Arquetipos e Constraints por Secao

| Secao | Arquetipo | Constraints |
|-------|-----------|-------------|
| 1. Hero | Split Assimetrico | Headline >150px, Dark Mode, Overlap Elements |
| 2. Prova Social | Floating Cards | Dark Mode, Diagonal Divider, Hover Lift |
| 3. Cronograma | Scroll Storytelling | Sticky Element, Stagger, Selective Color, Bleed Left |
| 4. Resultados | Scroll Horizontal | Overflow Visible, Noise Texture, Bleed Both, Fade |
| 5. Oferta | Single Focus | Glassmorphism, Gradiente Radial, Container Narrow, Hover Glow |
| 6. Garantia | Isolated Element | Duocromatico, Container Narrow, Skewed Section |
| 7. Especialista | Editorial | Split Vertical, Imagem Overlay, Mixed Weights, Texto Gradiente |
| 8. FAQ | Reveal on Demand | Container Narrow, Selective Color, Clip Reveal |
| 9. Atendimento | Contained Center | Color Blocking, Hover Fill, Container Narrow |
| 10. Footer | Minimal | Low Contrast, Container Narrow |

---

## Elementos Encantadores e Surpresas

### Micro-interacoes
- **Timeline nodes (Sec 3):** Nodes que acendem com glow quando a aula entra no viewport
- **FAQ accent dots (Sec 8):** Scale up sutil no hover, indicando interatividade
- **Marquee pause (Sec 4):** Pausa suave quando usuario hover sobre o carrossel

### Animacoes Elaboradas
- **Marquee dual-speed (Sec 4):** Duas rows com velocidades diferentes criam ritmo organico
- **Clip reveal FAQ (Sec 8):** Respostas reveladas com clip-path ao inves de height transition basica
- **CTA fill animation (Sec 9):** Preenchimento de cor deslizante no hover

### Detalhes de Craft
- **Glassmorphism card (Sec 5):** Card da oferta com blur de fundo e borda luminosa
- **Noise texture (Sec 4):** Grain sutil que adiciona textura premium ao fundo
- **Drop cap editorial (Sec 7):** Primeira letra grande na bio, estilo revista
- **Moldura offset (Sec 7):** Retangulo laranja deslocado atras da imagem do especialista
- **Watermark numbers (Sec 3):** Numeros grandes semi-transparentes atras dos titulos das aulas

### Continuidade Visual
- **Linha decorativa laranja:** Presente como border-left no hero, na timeline do cronograma, na borda do escudo da garantia, e na separacao da oferta - cria fio condutor visual
- **Glow effects:** Presentes no hero, nos timeline nodes, no card da oferta e no escudo da garantia - conectam a pagina toda
- **Aspas decorativas:** Presentes nas secoes 2 e 4 (depoimentos), criando consistencia
- **Orange accent pattern:** Sempre usado em eyebrows, CTAs, destaques de texto, e icones - nunca excessivo

---

## Transicoes Entre Secoes

| De → Para | Tipo de Transicao |
|-----------|-------------------|
| Hero → Prova Social | clip-path diagonal (ja implementado) |
| Prova Social → Cronograma | Mudanca de background (gray-950 → black), sem divisor especial |
| Cronograma → Resultados | Mudanca de background (black → gray-950), linha horizontal com fade |
| Resultados → Oferta | Mudanca de background (gray-950 → black), fade natural |
| Oferta → Garantia | Mudanca de background (black → gray-950 com skew) |
| Garantia → Especialista | Mudanca de background (gray-950 skew → black), compensacao do skew |
| Especialista → FAQ | Mudanca de background (black → gray-950), sem divisor |
| FAQ → Atendimento | Mudanca de background (gray-950 → black), sem divisor |
| Atendimento → Footer | Mudanca de background (black → black), border-top sutil |
