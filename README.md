# Actuar — Brand Kit

Ativos de marca da Actuar: logo completo, wordmark e folha de impressão, em SVG, PNG e PDF vetorial.

---

## Conceito de cor

O símbolo carrega a cor; o wordmark carrega o nome. O nome recua em um neutro escuro para o símbolo colorido ser o protagonista — ele é o ativo distintivo da marca.

O neutro não é preto puro (`#000000` é duro e barato em marca): é um **quase-preto azulado** `#0A1130`, ainda dentro da família estrutura/azul do sistema. Neutro com sotaque, não genérico.

| Papel | Cor | Significado |
|---|---|---|
| Laranja | `#FB5423` | energia & ação — o humano |
| Azul | `#1B2FEB` | confiança & estrutura — o core |
| Ciano | `#1FEFFF` | movimento & recorrência — o fluxo |
| Wordmark | `#0A1130` | quase-preto azulado — a base |
| Branco | `#FFFFFF` | reverso / reserva |

---

## Estrutura

```
actuar-brand-kit/
├── logo/        Lockup completo (símbolo + wordmark)
├── wordmark/    Só o nome, sem símbolo
└── print/       PDF multipágina pronto para a gráfica
```

### logo/ — lockup completo

| Arquivo | Uso |
|---|---|
| `actuar-logo-cor-fundo-claro` | Colorido + nome `#0A1130`, sobre fundo claro/branco. **Uso padrão.** |
| `actuar-logo-cor-fundo-escuro` | Colorido + nome branco, sobre fundo azul/escuro ou foto. |
| `actuar-logo-mono-escura` | Tudo `#0A1130` (1 tinta), sobre fundo claro. Carimbo, fax, 1 cor. |
| `actuar-logo-mono-branca` | Tudo branco (1 tinta), sobre fundo escuro. |

### wordmark/ — só o nome

| Arquivo | Cor | Uso |
|---|---|---|
| `actuar-wordmark-claro` | `#0A1130` | Primário, sobre fundo claro. Contraste 18.5:1. |
| `actuar-wordmark-branca` | `#FFFFFF` | Reverso, sobre fundo escuro/azul. |
| `actuar-wordmark-vibrante` | `#1B2FEB` | Opcional, peças de marketing. Contraste 7.92:1. |

> **Nunca** o wordmark em laranja ou ciano. Laranja diria "ação/impulso"; ciano diria "movimento/recorrência" (e some no branco, 1.41:1). O símbolo é a energia; o wordmark é a base.

---

## Formatos

- **SVG** — vetorial, para web e telas. Fundo transparente.
- **PNG** — raster com transparência, para uso rápido (slides, docs).
- **PDF** — vetorial em curvas, para gráfica/impressão.

## Impressão

`print/actuar-folha-de-impressao.pdf` traz as 8 artes em curvas + a tabela de equivalência Pantone / CMYK.

| Cor | HEX | Pantone (C) | CMYK |
|---|---|---|---|
| Laranja | `#FB5423` | 165 C | 0 · 75 · 90 · 0 |
| Azul | `#1B2FEB` | 2727 C | 85 · 70 · 0 · 0 |
| Ciano | `#1FEFFF` | 306 C | 55 · 0 · 5 · 0 |
| Wordmark | `#0A1130` | 2767 C | 100 · 90 · 40 · 50 |
| Branco | `#FFFFFF` | — | reserva do papel |

> Valores aproximados, em RGB nos arquivos. Atribuir perfil ICC e fechar PDF/X na gráfica; confirmar Pantone em leque físico antes da tiragem.

---

## Tokens (CSS)

```css
:root {
  /* Marca */
  --brand-orange: #FB5423;   /* energia & ação — o humano */
  --brand-blue:   #1B2FEB;   /* confiança & estrutura — o core */
  --brand-cyan:   #1FEFFF;   /* movimento & recorrência — o fluxo */
  --brand-white:  #FFFFFF;

  /* Wordmark */
  --brand-wordmark:         #0A1130;   /* primário — quase-preto azulado */
  --brand-wordmark-reverse: #FFFFFF;   /* reverso sobre escuro/azul */
  --brand-wordmark-vibrant: #1B2FEB;   /* opcional — versão colorida (marketing) */

  /* Display P3 (telas modernas) */
  --brand-orange-p3: color(display-p3 0.9110 0.3776 0.2157);
  --brand-blue-p3:   color(display-p3 0.1235 0.1823 0.8852);
  --brand-cyan-p3:   color(display-p3 0.4424 0.9236 0.9880);
}
```
