---
title: "Probabilidade e Estatística"
subtitle: "Variáveis Aleatórias"
author: "Prof. Dr. Alessandro JQ Sarnaglia"
lang: "pt"
format:
  revealjs:
    width: 1280
    height: 720
    min-scale: 0.05
    fig-width: 5.5
    fig-height: 5.5
    theme: [custom.scss]
    css: [fonts.css, style.css]
    callout-icon: false
    toc: true
    toc-depth: 3
    toc-expand: 3
    number-sections: true
    number-depth: 3
    footer: "[Voltar 🔙](../index.html)"
    menu:
      useTextContentForMissingTitles: false
editor: source
filters:
  - parse-latex
---



# Definição

## 1 Definição {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 1:** Uma amostra de $n$ componentes é submetida a testes para verificar os defeituosos e os não defeituosos. Nesse experimento, podemos definir o espaço amostral
$$
\newcommand{\invisible}[1]{\color{white}{#1}}
\Omega = \{\omega = (z_1, \ldots, z_n) : z_i \in \{S,F\} \},
$$
em que $S =$ "componente defeituoso" e $F =$ "componente não defeituoso".

::: 

::: {.callout-caution}
## Observação

Como visto acima, o espaço amostral pode assumir formas bem abstratas. No entanto, em muitos casos, é de interesse associar um valor numérico a cada resultado de $\Omega$.
:::

## 1 Definição {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 1 (cont.):** No exemplo anterior, suponha $n=3$, então
$$
\Omega = \{(FFF),(SFF),(FSF),(FFS),(SSF),(SFS),(FSS),(SSS)\}.
$$
Pode ser interesse registrar apenas o número de componentes defeituosos e não as falhas individuais (se $n$ grande por exemplo). Assim, teríamos $X(\omega) =$ "número de componentes defeituosos em $\omega$" e:

::: incremental

-   $X(FFF) = 0$;
-   $X(SFF) = X(FSF) = X(FFS) = 1$;
-   $X(SSF) = X(SFS) = X(FSS) = 2$; e
-   $X(SSS) = 3$.

:::

:::

::: fragment

::: {.callout-caution}
## Observação

O tipo de situação acima nos leva a definição de [**variáveis aleatórias**]{style="color:red;"}.
:::

:::

## 1 Definição {.unnumbered .unlisted}

::: {.callout-note}
## Definição - Variáveis Aleatórias

Seja $\Omega$ espaço amostral de um experimento aleatório. Uma **variável aleatória** (va) é qualquer regra que associe um valor numérico real a cada resultado de $\Omega$.
:::

::: {.callout-caution}
## Observações

Da definição de va, podemos fazer os seguintes apontamentos:

1.    Variáveis aleatórias normalmente são denotadas por letras maiúsculas do final do alfabeto, tais como $X$, $Y$, $Z$, entre outras;
2.    Matematicamente, podemos definir $X$ como va se $X : \Omega \to \mathbb{R}$;
3.    Podemos também escrever $X(\omega) = x$ para dizer que $x$ é o valor atribuído a $\omega$ pela va $X$.
:::

## 1 Definição {.unnumbered .unlisted}

::: columns

::: {.column #vcenter width=55%}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 1 (cont.):**

<figure>
  <img src="figs/ilustracao_variavel_aleatoria0.png" style="display: block;margin-left: auto;margin-right: auto;width: 80%;">
</figure>

:::

:::

::: {.column #vcenter width=45%}

:::

:::

## 1 Definição {.unnumbered .unlisted}

::: columns

::: {.column #vcenter width=55%}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 1 (cont.):**

<figure>
  <img src="figs/ilustracao_variavel_aleatoria1.png" style="display: block;margin-left: auto;margin-right: auto;width: 80%;">
</figure>

:::

:::

::: {.column #vcenter width=45%}

:::

:::

## 1 Definição {.unnumbered .unlisted}

::: columns

::: {.column #vcenter width=55%}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 1 (cont.):**

<figure>
  <img src="figs/ilustracao_variavel_aleatoria2.png" style="display: block;margin-left: auto;margin-right: auto;width: 80%;">
</figure>

:::

:::

::: {.column #vcenter width=45%}

:::

:::

## 1 Definição {.unnumbered .unlisted}

::: columns

::: {.column #vcenter width=55%}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 1 (cont.):**

<figure>
  <img src="figs/ilustracao_variavel_aleatoria3.png" style="display: block;margin-left: auto;margin-right: auto;width: 80%;">
</figure>

:::

:::

::: {.column #vcenter width=45%}

:::

:::

## 1 Definição {.unnumbered .unlisted}

::: columns

::: {.column #vcenter width=55%}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 1 (cont.):**

<figure>
  <img src="figs/ilustracao_variavel_aleatoria4.png" style="display: block;margin-left: auto;margin-right: auto;width: 80%;">
</figure>

:::

:::

::: {.column #vcenter width=45%}

:::

:::

## 1 Definição {.unnumbered .unlisted}

::: columns

::: {.column #vcenter width=55%}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 1 (cont.):**

<figure>
  <img src="figs/ilustracao_variavel_aleatoria5.png" style="display: block;margin-left: auto;margin-right: auto;width: 80%;">
</figure>

:::

:::

::: {.column #vcenter width=45%}
::: {.callout-caution}
## Observação

Os valores de $\text{Im}(X)$ induzem uma partição de $\Omega$. No exemplo, vimos:

-   $[X=0] = \{(FFF)\}$;
-   $[X=1] = \{(FFS), (FSF), (SFF)\}$;
-   $[X=2] = \{(FSS), (SFS), (SSF)\}$; e
-   $[X=3] = \{(SSS)\}$.

:::
:::

:::



## 1 Definição {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

A qualquer va $X$, podemos associar um contradomínio (normalmente o conjunto $\mathbb{R}$) e uma [**imagem**]{style="color:red;"}, que denotaremos por $\text{Im}(X)$.

:::

::: {.callout-note}
## Definição

O conjunto de todos possíveis valores que uma va $X$ pode assumir é denominado **imagem** de $X$ e é denotado por $\text{Im}(X)$.

:::

::: {.callout-caution}
## Observação

No exemplo anterior, temos que $\text{Im}(X) = \{0,1,2,3\}$.
:::

## 1 Definição {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

Similarmente a estatística descritiva, podemos classificar as va's de acordo com o seu conjunto imagem.

:::

::: {.callout-note}
## Definição

Dada uma va $X$, dizemos que:

-   $X$ é va **discreta** (vad) se $\text{Im}(X)$ for conjunto finito ou infinito enumerável;
-   $X$ é va **contínua** (vac) se $\text{Im}(X)$ for conjunto não enumerável.

:::

::: {.callout-caution}
## Observação

Agora, fica claro que a va $X$ do exemplo anterior se trata de uma **vad**.

:::

## 1 Definição {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 2:** Uma linha de produção é observada até a produção da primeira peça defeituosa. Seja $S =$ "Peça defeituosa" e $F =$ "Peça normal". Então temos que
$$
\Omega = \{(S), (FS), (FFS), (FFFS), \ldots\}.
$$

::: columns

::: {.column #vcenter width=60%}

A este experimento, podemos associar a va $X =$ "Número de peças produzidas". Nesse caso, teríamos
$$
\text{Im}(X) = \{1, 2, 3, \ldots\}.
$$

:::

::: {.column #vcenter width=40%}

<figure>
  <img src="figs/ilustracao_variavel_aleatoria_discreta.png" style="display: block;margin-left: auto;margin-right: auto;width: 90%;">
</figure>

:::

:::

:::

::: {.callout-caution}
## Observação

Embora $\text{Im}(X)$ seja infinito, ele é um conjunto enumerável, de modo que $X$ é **vad**.

:::

## 1 Definição {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

::: columns

::: {.column #vcenter width=60%}

**Exemplo 3:** Um ponto de uma região circular de raio unitário é sorteado. Nesse caso, podemos definir $\Omega = \{\omega = (z_1,z_2) : z_1^2 + z_2^2 \leq 1\}$.

[Nesse espaço amostral, um evento $A$, é uma [**região**]{style="color:red;"} de pontos, $A\subset\Omega$.]{style="visibility:hidden;"}

[A este experimento, poderíamos associar a variável aleatória $X =$ "Distância de $\omega$ à origem". Isto é $X(\omega) = (z_1^2 - z_2^2)^{1/2}$. Note que, nesse caso $\text{Im}(X) = [0,1]$.]{style="visibility:hidden;"}

:::

::: {.column #vcenter width=40%}

<figure>
  <img src="figs/ilustracao_variavel_aleatoria_continua0.svg" style="display: block;margin-left: auto;margin-right: auto;width: 95%;">
</figure>

:::

:::

:::

::: {style="visibility:hidden"}

::: {.callout-caution}
## Observação

Como $\text{Im}(X)$ é conjunto não enumerável, classificamos $X$ como uma **vac**.

:::

:::

## 1 Definição {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

::: columns

::: {.column #vcenter width=60%}

**Exemplo 3:** Um ponto de uma região circular de raio unitário é sorteado. Nesse caso, podemos definir $\Omega = \{\omega = (z_1,z_2) : z_1^2 + z_2^2 \leq 1\}$.

Nesse espaço amostral, um evento $A$, é uma [**região**]{style="color:red;"} de pontos, $A\subset\Omega$.

[A este experimento, poderíamos associar a variável aleatória $X =$ "Distância de $\omega$ à origem". Isto é $X(\omega) = (z_1^2 - z_2^2)^{1/2}$. Note que, nesse caso $\text{Im}(X) = [0,1]$.]{style="visibility:hidden;"}

:::

::: {.column #vcenter width=40%}

<figure>
  <img src="figs/ilustracao_variavel_aleatoria_continua1.svg" style="display: block;margin-left: auto;margin-right: auto;width: 95%;">
</figure>

:::

:::

:::

::: {style="visibility:hidden"}

::: {.callout-caution}
## Observação

Como $\text{Im}(X)$ é conjunto não enumerável, classificamos $X$ como uma **vac**.

:::

:::

## 1 Definição {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

::: columns

::: {.column #vcenter width=60%}

**Exemplo 3:** Um ponto de uma região circular de raio unitário é sorteado. Nesse caso, podemos definir $\Omega = \{\omega = (z_1,z_2) : z_1^2 + z_2^2 \leq 1\}$.

Nesse espaço amostral, um evento $A$, é uma [**região**]{style="color:red;"} de pontos, $A\subset\Omega$.

A este experimento, poderíamos associar a variável aleatória $X =$ "Distância de $\omega$ à origem". Isto é $X(\omega) = (z_1^2 + z_2^2)^{1/2}$. Note que, nesse caso $\text{Im}(X) = [0,1]$.

:::

::: {.column #vcenter width=40%}

<figure>
  <img src="figs/ilustracao_variavel_aleatoria_continua2.svg" style="display: block;margin-left: auto;margin-right: auto;width: 95%;">
</figure>

:::

:::

:::

::: fragment

::: {.callout-caution}
## Observação

Como $\text{Im}(X)$ é conjunto não enumerável, classificamos $X$ como uma **vac**.

:::

:::

## Função de distribuição acumulada

::: {.callout-caution}
## Observação

Um evento aleatório muito importante para modelagem de va's é $[X \leq x]$. A probabilidade deste evento nos diz o quanto de probabilidade a va $X$ acumula até o valor $x$.

:::

::: {.callout-note}
## Definição

A **função de distribuição acumulada** (fda) é definida por $F_X(x) = P(X \leq x)$
:::

::: {.callout-caution}
## Observação

Ao se partir de uma medida de probabilidade definida em $\Omega$, para o calcular $F_X(x)$, devemos encontrar a probabilidade (em $\Omega$) do evento $A_x = \{\omega \in \Omega: X(\omega) \leq x\}$. Isto é, $F_X(x) = P(X \leq x) = P(A_x)$.

:::

## {.unnumbered .unlisted .smaller}

### Exemplo 1 (cont.) {.unnumbered .unlisted}

Se supomos que $\Omega$ é equiprovável. Teremos que

$$
F_X(x) = \begin{cases}
0, & x < 0;\\
P(X=0) = \frac{1}{8}, & 0 \leq x < 1;\\
P(X=0) + P(X=1) = \frac{1}{8} + \frac{3}{8} = \frac{4}{8}, & 1 \leq x < 2;\\
P(X=0) + P(X=1) + P(X=2) = \frac{1}{8} + \frac{3}{8} + \frac{3}{8} = \frac{7}{8}, & 2 \leq x < 3;\\
P(X=0) + P(X=1) + P(X=2) + P(X=3) = \frac{1}{8} + \frac{3}{8} + \frac{3}{8} + \frac{1}{8} = 1, & x \geq 3;\\
\end{cases}
$$

## {.unnumbered .unlisted}

### Exemplo 1 (cont.) {.unnumbered .unlisted}

<figure>
  <img src="figs/ilustracao_fda0.png" style="display: block;margin-left: auto;margin-right: auto;width: 65%;">
</figure>

## {.unnumbered .unlisted}

### Exemplo 1 (cont.) {.unnumbered .unlisted}

<figure>
  <img src="figs/ilustracao_fda1.png" style="display: block;margin-left: auto;margin-right: auto;width: 65%;">
</figure>

## {.unnumbered .unlisted}

### Exemplo 1 (cont.) {.unnumbered .unlisted}

<figure>
  <img src="figs/ilustracao_fda2.png" style="display: block;margin-left: auto;margin-right: auto;width: 65%;">
</figure>

## {.unnumbered .unlisted}

### Exemplo 1 (cont.) {.unnumbered .unlisted}

<figure>
  <img src="figs/ilustracao_fda3.png" style="display: block;margin-left: auto;margin-right: auto;width: 65%;">
</figure>

## {.unnumbered .unlisted}

### Exemplo 1 (cont.) {.unnumbered .unlisted}

<figure>
  <img src="figs/ilustracao_fda4.png" style="display: block;margin-left: auto;margin-right: auto;width: 65%;">
</figure>


## {.unnumbered .unlisted}

### Exemplo 1 (cont.) {.unnumbered .unlisted}

<figure>
  <img src="figs/ilustracao_fda5.png" style="display: block;margin-left: auto;margin-right: auto;width: 65%;">
</figure>

::: {.callout-caution}
## Observação

No caso discreto, os tamanhos dos saltos de $F_X(x)$ nos dá os valores de $P(X=x)$.
:::

## 1.1 Função de distribuição acumulada {.unnumbered .unlisted}

::: {.callout-note}
## Definição

Se $X$ é vad, a função $p_X(x) = P(X=x)$, $x \in \text{Im}(X)$, é chamada [**função massa de probabilidade**]{style="color:red;"} (fmp).
:::

::: fragment

::: {.callout-warning}
## Propriedades

A fmp $p_X(x)$ de um uma vad $X$ satisfaz:

::: incremental

1.    $p_X(x) \geq 0$;
2.    $\textstyle \sum_{x} p_X(x) = 1$.

:::

:::

:::

::: fragment

::: {.callout-caution}
## Observação

Assim, vemos que, para variáveis aleatórias discretas, a fda $F_X(x)$ nos fornece a fmp $p_X(x)$ e vice-versa.
:::

:::

## 1.1 Função de distribuição acumulada {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

A fmp é um modelo teórico para as **frequências relativas** vistas em estatística descritiva.
:::

::: fragment


<figure>
  <img src="figs/ilustracao_frequencia_fmp.png" style="display: block;margin-left: auto;margin-right: auto;width: 75%;">
</figure>


:::

## {.unnumbered .unlisted .smaller}

### Exemplo 3 (cont.) {.unnumbered .unlisted}

Supondo que nenhum ponto de $\Omega$ é privilegiado, podemos definir a medida de probabilidade de $A$ como
$$\textstyle P(A) = \frac{\text{Área}(A)}{\text{Área}(\Omega)} = \frac{\text{Área}(A)}{\pi}.$$
Nesse caso, as probabilidades de dois eventos de mesma área serão as mesmas (equiprobabilidade).  

::: columns

::: {.column #vcenter width=65%}

[Usando essa medida de probabilidade, para calcular a fda de $X$, precisamos encontrar a área da região $[X \leq x]$. Veja na ilustração ao lado.]{style="visibility:hidden;"}

[Logo, a fda de $X$ é dada por
$$
\textstyle F_X(x) = P(X \leq x) = \begin{cases}
0, & x < 0;\\
\frac{\text{Área}(X \leq x)}{\pi} = \frac{\pi x^2}{\pi} = x^2, & 0\leq x < 1;\\
1, & x \geq 1.
\end{cases}
$$
]{style="visibility:hidden;"}

:::

::: {.column #vcenter width=35%}

<figure>
  <img src="figs/ilustracao_fda_vac0.png" style="display: block;margin-left: auto;margin-right: auto;width: 70%;">
</figure>

:::

:::

## {.unnumbered .unlisted .smaller}

### Exemplo 3 (cont.) {.unnumbered .unlisted}

Supondo que nenhum ponto de $\Omega$ é privilegiado, podemos definir a medida de probabilidade de $A$ como
$$\textstyle P(A) = \frac{\text{Área}(A)}{\text{Área}(\Omega)} = \frac{\text{Área}(A)}{\pi}.$$
Nesse caso, as probabilidades de dois eventos de mesma área serão as mesmas (equiprobabilidade).  

::: columns

::: {.column #vcenter width=65%}

Usando essa medida de probabilidade, para calcular a fda de $X$, precisamos encontrar a área da região $[X \leq x]$. Veja na ilustração ao lado.

[Logo, a fda de $X$ é dada por
$$
\textstyle F_X(x) = P(X \leq x) = \begin{cases}
0, & x < 0;\\
\frac{\text{Área}(X \leq x)}{\pi} = \frac{\pi x^2}{\pi} = x^2, & 0\leq x < 1;\\
1, & x \geq 1.
\end{cases}
$$
]{style="visibility:hidden;"}

:::

::: {.column #vcenter width=35%}

<figure>
  <img src="figs/ilustracao_fda_vac0.png" style="display: block;margin-left: auto;margin-right: auto;width: 70%;">
</figure>


:::

:::



## {.unnumbered .unlisted .smaller}

### Exemplo 3 (cont.) {.unnumbered .unlisted}

Supondo que nenhum ponto de $\Omega$ é privilegiado, podemos definir a medida de probabilidade de $A$ como
$$\textstyle P(A) = \frac{\text{Área}(A)}{\text{Área}(\Omega)} = \frac{\text{Área}(A)}{\pi}.$$
Nesse caso, as probabilidades de dois eventos de mesma área serão as mesmas (equiprobabilidade).  

::: columns

::: {.column #vcenter width=65%}

Usando essa medida de probabilidade, para calcular a fda de $X$, precisamos encontrar a área da região $[X \leq x]$. Veja na ilustração ao lado.

[Logo, a fda de $X$ é dada por
$$
\textstyle F_X(x) = P(X \leq x) = \begin{cases}
0, & x < 0;\\
\frac{\text{Área}(X \leq x)}{\pi} = \frac{\pi x^2}{\pi} = x^2, & 0\leq x < 1;\\
1, & x \geq 1.
\end{cases}
$$
]{style="visibility:hidden;"}

:::

::: {.column #vcenter width=35%}

<figure>
  <img src="figs/ilustracao_fda_vac1.png" style="display: block;margin-left: auto;margin-right: auto;width: 70%;">
</figure>


:::

:::


## {.unnumbered .unlisted .smaller}

### Exemplo 3 (cont.) {.unnumbered .unlisted}

Supondo que nenhum ponto de $\Omega$ é privilegiado, podemos definir a medida de probabilidade de $A$ como
$$\textstyle P(A) = \frac{\text{Área}(A)}{\text{Área}(\Omega)} = \frac{\text{Área}(A)}{\pi}.$$
Nesse caso, as probabilidades de dois eventos de mesma área serão as mesmas (equiprobabilidade).  

::: columns

::: {.column #vcenter width=65%}

Usando essa medida de probabilidade, para calcular a fda de $X$, precisamos encontrar a área da região $[X \leq x]$. Veja na ilustração ao lado.

[Logo, a fda de $X$ é dada por
$$
\textstyle F_X(x) = P(X \leq x) = \begin{cases}
0, & x < 0;\\
\frac{\text{Área}(X \leq x)}{\pi} = \frac{\pi x^2}{\pi} = x^2, & 0\leq x < 1;\\
1, & x \geq 1.
\end{cases}
$$
]{style="visibility:hidden;"}

:::

::: {.column #vcenter width=35%}

<figure>
  <img src="figs/ilustracao_fda_vac2.png" style="display: block;margin-left: auto;margin-right: auto;width: 70%;">
</figure>


:::

:::

## {.unnumbered .unlisted .smaller}

### Exemplo 3 (cont.) {.unnumbered .unlisted}

Supondo que nenhum ponto de $\Omega$ é privilegiado, podemos definir a medida de probabilidade de $A$ como
$$\textstyle P(A) = \frac{\text{Área}(A)}{\text{Área}(\Omega)} = \frac{\text{Área}(A)}{\pi}.$$
Nesse caso, as probabilidades de dois eventos de mesma área serão as mesmas (equiprobabilidade).  

::: columns

::: {.column #vcenter width=65%}

Usando essa medida de probabilidade, para calcular a fda de $X$, precisamos encontrar a área da região $[X \leq x]$. Veja na ilustração ao lado.

[Logo, a fda de $X$ é dada por
$$
\textstyle F_X(x) = P(X \leq x) = \begin{cases}
0, & x < 0;\\
\frac{\text{Área}(X \leq x)}{\pi} = \frac{\pi x^2}{\pi} = x^2, & 0\leq x < 1;\\
1, & x \geq 1.
\end{cases}
$$
]{style="visibility:hidden;"}

:::

::: {.column #vcenter width=35%}

<figure>
  <img src="figs/ilustracao_fda_vac3.png" style="display: block;margin-left: auto;margin-right: auto;width: 70%;">
</figure>


:::

:::

## {.unnumbered .unlisted .smaller}

### Exemplo 3 (cont.) {.unnumbered .unlisted}

Supondo que nenhum ponto de $\Omega$ é privilegiado, podemos definir a medida de probabilidade de $A$ como
$$\textstyle P(A) = \frac{\text{Área}(A)}{\text{Área}(\Omega)} = \frac{\text{Área}(A)}{\pi}.$$
Nesse caso, as probabilidades de dois eventos de mesma área serão as mesmas (equiprobabilidade).  

::: columns

::: {.column #vcenter width=65%}

Usando essa medida de probabilidade, para calcular a fda de $X$, precisamos encontrar a área da região $[X \leq x]$. Veja na ilustração ao lado.

Logo, a fda de $X$ é dada por
$$
\textstyle F_X(x) = P(X \leq x) = \begin{cases}
0, & x < 0;\\
\frac{\text{Área}(X \leq x)}{\pi} = \frac{\pi x^2}{\pi} = x^2, & 0\leq x < 1;\\
1, & x \geq 1.
\end{cases}
$$

:::

::: {.column #vcenter width=35%}

<figure>
  <img src="figs/ilustracao_fda_vac3.png" style="display: block;margin-left: auto;margin-right: auto;width: 70%;">
</figure>


:::

:::

## {.unnumbered .unlisted}

### Exemplo 3 (cont.) {.unnumbered .unlisted}

<figure>
  <img src="figs/ilustracao_fda_vac_grafico0.png" style="display: block;margin-left: auto;margin-right: auto;width: 50%;">
</figure>


## {.unnumbered .unlisted}

### Exemplo 3 (cont.) {.unnumbered .unlisted}

<figure>
  <img src="figs/ilustracao_fda_vac_grafico1.png" style="display: block;margin-left: auto;margin-right: auto;width: 50%;">
</figure>


## {.unnumbered .unlisted}

### Exemplo 3 (cont.) {.unnumbered .unlisted}

<figure>
  <img src="figs/ilustracao_fda_vac_grafico2.png" style="display: block;margin-left: auto;margin-right: auto;width: 50%;">
</figure>



::: {.callout-caution}
## Observação

Observe que não há pontos de descontinuidade para a fda de uma va contínua. Portanto, a fda de uma vac não fornece probabilidades diretamente.
:::

## 1.1 Função de distribuição acumulada {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

Tomando a derivada da fda de uma vac, obtemos a chamada [**função densidade de probabilidade**]{style="color:red;"}.
:::

::: fragment

::: {.callout-note}
## Definição

Se $X$ é vac com fda $F_X(x)$, a sua **função densidade de probabilidade** (fdp) é definida por $f_X(x) = \frac{dF_X(x)}{dx}$.
:::

:::

::: fragment

::: {.callout-warning}
## Propriedades

A fdp $f_X(x)$ de uma vac $X$ satisfaz:

::: incremental

1.    $f_X(x) \geq 0$, $x\in \mathbb{R}$;
2.    $\int_{-\infty}^\infty f_X(x)dx = 1$.

:::

:::

:::

## 1.1 Função de distribuição acumulada {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

A fdp é um modelo teórico para as **densidades** de faixas vistas em estatística descritiva.
:::

::: fragment

<figure>
  <img src="figs/ilustracao_densidade_fdp.png" style="display: block;margin-left: auto;margin-right: auto;width: 75%;">
</figure>

:::

## 1.1 Função de distribuição acumulada {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

Note que o tratamento probabilístico para obter a fda, bem como o seu comportamento, dependem do tipo de va em questão.
:::

::: fragment

::: {.callout-warning}
## Propriedades

Seja $F_X(x)$ fda de uma va $X$, então

::: incremental

1.    $\lim_{x\to-\infty} F_X(x) = 0$ e $\lim_{x\to\infty} F_X(x) = 1$;
2.    $x < x' \Rightarrow F_X(x) \leq F_X(x')$, isto é, $F_X(\cdot)$ é não decrescente; e
3.    se $X$ é vad, $P(X=x) = F_X(x) - \lim_{x'\uparrow x} F_X(x')$, isto é, a fmp $p_X(x)$ é o tamanho do salto de $F_X(\cdot)$ em $x$.
4.    se $X$ é vac, $f_X(x) = \frac{dF_X(x)}{dx}$, isto é, a fdp $f_X(x)$ é a derivada de $F_X(\cdot)$ em $x$.

:::

:::

:::

# Variáveis aleatórias discretas

## 2 Variáveis aleatórias discretas {.unnumbered .unlisted}

::: {.callout-caution}
## Observações

::: incremental

1. Vimos que, se o modelo probabilístico é concebido sobre um espaço amostral $\Omega$ abstrato e $X : \Omega \to \mathbb{R}$, então a fmp pode ser obtida por
$$p_X(x) = P(X = x) = P(A_x),$$
em que $A_x = \{\omega \in \Omega : X(\omega) = x\}$. Isto é, a fmp de $X$ é **induzida** pela medida de probabilidade em $\Omega$;
2. Muito frequentemente, a construção de um modelo probabilístico em $\Omega$ é muito complicada, o que dificultaria a determinação da fmp induzida.
3. Para contornar esse problema, levando em consideração o comportamento da vad em estudo, podemos especificar diretamente uma fmp para a vad, desde que atenda as propriedades já vistas:
    + $p_X(x) \geq 0$;
    + $\sum_{x\in\text{Im}(X)} p_X(x) = 1$.

:::

:::

## {.unnumbered .unlisted .smaller}

### Exemplo 4 {.unnumbered .unlisted}

Suponha que em um estoque existem seis lotes de um produto: três com $0$ itens defeituosos; dois com $1$ defeituoso; e um com $2$ defeituosos. Um lote será sorteado entre os seis e será enviado a um cliente. Seja $X=$ "número de itens defeituosos no lote recebido pelo cliente". [Nesse caso, podemos especificar]{.fragment fragment-index=1}

::: {.fragment fragment-index=1}

::: columns

::: {.column #vcenter width=45%}

<div style="text-align: center;">
<table>
  <tr style="border-top:solid;">
    <td style="border-right:solid 1pt;">$x$</td>
    <td style="text-align: center;">$0$</td>
    <td style="text-align: center;">$1$</td>
    <td style="text-align: center;">$2$</td>
    <td style="text-align: center;border-left:solid 1pt;">Total</td>
  </tr>
  <tr style="border-top:solid 1pt;border-bottom:solid;">
    <td style="border-right:solid 1pt;">$p_X(x)$ </td>
    <td style="text-align: center;">$\frac{3}{6}$</td>
    <td style="text-align: center;">$\frac{2}{6}$</td>
    <td style="text-align: center;">$\frac{1}{6}$</td>
    <td style="text-align: center;border-left:solid 1pt;">$1$</td>
  </tr>
</table>
</div>

:::

::: {.column #vcenter width=10%}

<p style="text-align:center;">
ou ainda
</p>

:::

::: {.column #vcenter width=45%}

<div style="text-align: center;">
<table>
  <tr style="border-top:solid;">
    <td style="border-right:solid 1pt;">$x$</td>
    <td style="text-align: center;">$0$</td>
    <td style="text-align: center;">$1$</td>
    <td style="text-align: center;">$2$</td>
    <td style="text-align: center;border-left:solid 1pt;">Total</td>
  </tr>
  <tr style="border-top:solid 1pt;border-bottom:solid;">
    <td style="border-right:solid 1pt;">$p_X(x)$ </td>
    <td style="text-align: center;">$\frac{1}{2}$</td>
    <td style="text-align: center;">$\frac{1}{3}$</td>
    <td style="text-align: center;">$\frac{1}{6}$</td>
    <td style="text-align: center;border-left:solid 1pt;">$1$</td>
  </tr>
</table>
</div>

:::

:::

:::

::: {.fragment fragment-index=2}

Se não sabemos a quantidade de lotes em estoque, a especificação acima não é praticável, pois não sabemos o comportamento probabilístico do experimento ($\Omega$ é equiprovável, mas desconhecido).

:::

::: {.fragment fragment-index=3}

Nesse caso, se ainda assumirmos que os lotes tem no máximo 2 itens defeituosos, podemos especificar uma fmp arbitrária para a vad $X$, como, por exemplo

<div style="text-align: center;">
<table>
  <tr style="border-top:solid;">
    <td style="border-right:solid 1pt;">$x$</td>
    <td style="text-align: center;">$0$</td>
    <td style="text-align: center;">$1$</td>
    <td style="text-align: center;">$2$</td>
    <td style="text-align: center;border-left:solid 1pt;">Total</td>
  </tr>
  <tr style="border-top:solid 1pt;border-bottom:solid;">
    <td style="border-right:solid 1pt;">$p_X(x)$ </td>
    <td style="text-align: center;">$0.7$</td>
    <td style="text-align: center;">$0.2$</td>
    <td style="text-align: center;">$0.1$</td>
    <td style="text-align: center;border-left:solid 1pt;">$1$</td>
  </tr>
</table>
</div>

:::

::: {.fragment fragment-index=4}

Note que $p_X(0), p_X(1), p_X(2) \geq 0$ e que $\sum_{x=0}^2 p_X(x) = 1$, de modo que $p_X(x)$ é uma fmp válida.

:::

## 2 Variáveis aleatórias discretas {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

No exemplo anterior, especificamos de maneira arbitrária uma fmp $p_X(x)$ para a vad $X$. No entanto, podemos ser mais flexíveis e propor uma [**família**]{style="color:red;"} de fmp's que dependa de [**parâmetros**]{style="color:red;"}.

:::

::: {.fragment fragment-index=1 style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 4 (cont.):** 

Para flexibilizar o nosso modelo probabilístico, podemos especificar a seguinte [**forma**]{style="color:red;"} para a fmp:

::: columns

::: {.column #vcenter width=30%}

<div style="text-align: center;">
<table>
  <tr style="border-top:solid;">
    <td style="border-right:solid 1pt;">$x$</td>
    <td style="text-align: center;">$0$</td>
    <td style="text-align: center;">$1$</td>
    <td style="text-align: center;">$2$</td>
    <td style="text-align: center;border-left:solid 1pt;">Total</td>
  </tr>
  <tr style="border-top:solid 1pt;border-bottom:solid;">
    <td style="border-right:solid 1pt;">$p_X(x)$ </td>
    <td style="text-align: center;">$\alpha$</td>
    <td style="text-align: center;">$\beta$</td>
    <td style="text-align: center;">$\gamma$</td>
    <td style="text-align: center;border-left:solid 1pt;">$1$</td>
  </tr>
</table>
</div>

:::

::: {.column #vcenter width=70%}

::: {.fragment fragment-index=2}

Para $p_X(x)$ ser uma fmp, precisamos impor as seguintes restrições:

::: incremental
- $0 \leq \alpha \leq 1$;
- $0 \leq \beta \leq 1-\alpha$; e
- $\gamma = 1-\alpha-\beta$ (isto é, $\gamma$ é fixo).
:::

:::

:::

:::

::: fragment

Nesse caso, dizemos que $\alpha$ e $\beta$ são **parâmetros** (livres) da família de fmp's $p_X(x)$.

:::

::: 

## 2 Variáveis aleatórias discretas {.unnumbered .unlisted}

::: {.callout-note}
## Definição

Se a forma de $p_X(x)$ depende de um valor (ou vetor de valores) $\theta$, dizemos que $\theta$ é um **parâmetro** (ou vetor paramétrico) da família $p_X(x)$.
:::

::: fragment

::: {.callout-caution}
## Observação

Nesse caso, podemos escrever $p_X(x; \theta)$ para enfatizar que se trata de uma família de fmp's e que sua forma só é completamente conhecida se soubermos o valor do parâmetro $\theta$ que indexa a família.

:::

:::

::: {.fragment style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 4 (cont.):** Nesse exemplo, podemos agrupar os parâmetros no vetor $\theta = (\alpha, \beta)$. Note que, a fmp induzida pela medida equiprovável em $\Omega$ e a fmp arbitrariamente especificada posteriormente são membros particulares dessa família, em que $\theta = (\frac{1}{2}, \frac{1}{3})$ e $\theta = (0.7, 0.2)$, respectivamente.

:::

## 2 Variáveis aleatórias discretas {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

Como já visto anteriormente, a fda pode ser obtida acumulando as probabilidades da fmp.
:::

::: {.fragment style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

::: columns

::: {.column #vcenter width=50%}

**Exemplo 4 (cont.):** A fda para a família de fmp's neste caso é
$$
F_X(x) = F_X(x; \theta) = \begin{cases}
0, & x < 0;\\
\alpha, & 0\leq x < 1;\\
\alpha + \beta, & 1\leq x < 2;\\
1, & x \geq 2;\\
\end{cases}
$$

:::

::: {.column #vcenter width=50%}

<figure>
  <img src="figs/ilustracao_fda_exemplo4.png" style="display: block;margin-left: auto;margin-right: auto;width: 90%;">
</figure>

:::

:::

:::

## 2 Variáveis aleatórias discretas {.unnumbered .unlisted}

::: {.callout-tip}
## Exercício

Considere a seguinte função de $x$ que depende de um vetor de parâmetros $\theta = (\theta_1, \theta_2, \theta_3, \theta_4)$:
$$
p_X(x;\theta) = \begin{cases}
\theta_1, & x=0;\\
\theta_2, & x=1;\\
\theta_3, & x=2;\\
\theta_4, & x=3.
\end{cases}
$$

Pede-se:

1. Quais restrições necessitamos impor sobre $\theta = (\theta_1, \theta_2, \theta_3, \theta_4)$ para garantir que $p_X(x;\theta)$ seja de fato família de fmp's?
2. Qual a condição adicional sobre $\theta$ para que $p_X(x;\theta)$ seja simétrica? Qual é o ponto de simetria?
3. Determine e esboce a fda associada a família $p_X(x;\theta)$.
:::


## Esperança e variância de vad's

::: {.callout-caution}
## Observação

Vimos que a fmp é um modelo teórico para as frequências relativas vistas em estatística descritiva. Assim, fazendo uso da fmp, é natural calcularmos valores teóricos para a média e a variância de uma vad $X$.
:::

::: {.callout-note}
## Definição

Seja $X$ vad com imagem $\text{Im}(X)$ e fmp $p_X(x;\theta)$, sua **média**, também chamada de **esperança** ou **valor esperado**, é definida por 
$$\mu = \mu_X = E(X) = \sum_{x\in\text{Im}(X)} x\cdot p_X(x;\theta).$$
:::

## 2.1 Esperança e variância de vad's {.unnumbered .unlisted}

::: {.callout-caution}
## Observações

::: incremental

1. A fórmula para o cálculo de $\mu$ é muito similar àquela vista em estatística descritiva, no entanto, agora a fmp $p_X(x;\theta)$ toma o lugar da frequência relativa que teria sido efetivamente observada;
2. De maneira similar a estatística descritiva, $\mu$ é calculada como uma média **ponderada** com pesos dados por $p_X(x;\theta)$;
3. Naturalmente, para famílias de fmp's, pelo fato de $p_X(x;\theta)$ ser indexada por $\theta$, a sua esperança também será função de $\theta$.

:::

:::

::: {.fragment style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 4 (cont.):** Utilizando a fórmula de esperança, obtemos
$$\mu_X = 0p_X(0;\theta) + 1p_X(1;\theta) + 2p_X(2;\theta) = \beta + 2(1-\alpha-\beta) = 2-2\alpha - \beta.$$

Se $\alpha = \frac{1-\beta}{2}$, vemos que a fmp é simétrica em torno de $1$ e $\mu_X = 1$.

:::

## 2.1 Esperança e variância de vad's {.unnumbered .unlisted}

::: {.callout-caution}
## Observações

::: incremental

1. Quando está claro a que va $X$ a esperança se refere, usaremos $\mu$ em vez de $\mu_X$;
2. No Exemplo 4, se hipotetizarmos uma população em que a vad $X$ com valores $0, 1$ e $2$ associados as frequências relativas $\alpha$, $\beta$, $1-\alpha-\beta$, respectivamente, então $\mu = 2-2\alpha - \beta$ será a média populacional. Por isso podemos nos referir a $\mu$ por média populacional ou teórica;
3. No Exemplo 4, tomando $\theta = (\frac{1}{2}, \frac{1}{3})$, obtemos $\mu = 2-2\frac{1}{2} - \frac{1}{3} = \frac{2}{3} \approx 0.67$, que não é um valor possível de $X$. A palavra esperado deve ser interpretada com cautela porque uma pessoa não espera ver um valor de $X = 0.67$ quando um único estoque é selecionado.

:::

:::


## 2.1 Esperança e variância de vad's {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 5:** Seja $X$ o número de entrevistas que um estudante faz para conseguir um emprego e suponha que a sua seja $p_X(x) = \frac{k}{x^2}$, $x = 1, 2, 3, \ldots$, e $p_X(x) = 0$ caso contrário. A constante $k$ deve ser tal que $k^{-1} = \sum_{x=1}^\infty\frac{1}{x^2}$. É possível mostrar que $\sum_{x=1}^\infty\frac{1}{x^2} < +\infty$, portanto $p_X(x)$ é de fato uma fmp.

::: {.fragment fragment-index=1}

Agora, o seu valor esperado é
$$
\textstyle \mu = \sum_{x=1}^\infty x \cdot p_X(x) = \sum_{x=1}^\infty x\cdot\frac{k}{x^2} = k\sum_{x=1}^\infty \frac{1}{x}.
$$
O último termo é a soma harmônica, que diverge, isto é, $\mu = +\infty$.

:::

:::

::: {.fragment fragment-index=2}

::: {.callout-caution}
## Observação

Dizemos que $p_X(x)$ tem **caudas longas** (as probabilidades da cauda decrescem muito lentamente). Ao selecionar uma amostra dessa variável, a média amostras tenderá a crescer indefinidamente com o tamanho da amostra.

:::

:::

## 2.1 Esperança e variância de vad's {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

Frequentemente, temos interesse na esperança de $Y = h(X)$, em vez de $X$. Pela definição poderíamos obter $\mu_Y = \sum_y y \cdot p_Y(y)$, necessitando da fmp de $Y$. No entanto, existe uma maneira mais direta.
:::

::: {.fragment fragment-index=1 style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 6:** Seja $X$ vad e $Y = X^2$. [Por exemplo: ]{.fragment fragment-index=2}

::: columns

::: {.column #vcenter width=50%}

::: {.fragment fragment-index=2}
<div style="text-align: center;">
Se a fmp de $X$ for:
<table>
  <tr style="border-top:solid;">
    <td style="border-right:solid 1pt;">$x$</td>
    <td style="text-align: center;">$-2$</td>
    <td style="text-align: center;">$0$</td>
    <td style="text-align: center;">$2$</td>
    <td style="text-align: center;border-left:solid 1pt;">Total</td>
  </tr>
  <tr style="border-top:solid 1pt;border-bottom:solid;">
    <td style="border-right:solid 1pt;">$p_X(x)$ </td>
    <td style="text-align: center;">$p_{-2}$</td>
    <td style="text-align: center;">$p_{0}$</td>
    <td style="text-align: center;">$p_{2}$</td>
    <td style="text-align: center;border-left:solid 1pt;">$1$</td>
  </tr>
</table>
</div>

:::

:::

::: {.column #vcenter width=50%}

::: {.fragment fragment-index=3}

<div style="text-align: center;">
A fmp de $Y$ será:
<table>
  <tr style="border-top:solid;">
    <td style="border-right:solid 1pt;">$x$</td>
    <td style="text-align: center;">$0$</td>
    <td style="text-align: center;">$4$</td>
    <td style="text-align: center;border-left:solid 1pt;">Total</td>
  </tr>
  <tr style="border-top:solid 1pt;border-bottom:solid;">
    <td style="border-right:solid 1pt;">$p_Y(y)$ </td>
    <td style="text-align: center;">$p_{0}$</td>
    <td style="text-align: center;">$p_{-2}+p_{2}$</td>
    <td style="text-align: center;border-left:solid 1pt;">$1$</td>
  </tr>
</table>
</div>

:::

:::

:::

[Logo,
$$\textstyle \mu_Y = \sum_y y\cdot p_Y(y) = 0p_0 + 4(p_{-2} + p_2) = (-2)^2p_{-2} + 0^2p_{0} + 2^2p_{2} = \sum_x h(x)\cdot p_X(x) = E[h(X)].$$
]{.fragment fragment-index=4}

:::

## 2.1 Esperança e variância de vad's {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

Assim, se $X$ for vad com fmp $p_X(x)$ e $Y = h(X)$, então a esperança de $Y$ é
$$\mu_Y = E[h(X)] = \sum_x h(x)\cdot p_X(x).$$
Isto é, substituímos os $x$ pelos $h(x)$ no cálculo.

:::

::: fragment

::: {.callout-warning}
## Propriedade

Seja $X$ vad com esperança $\mu_X$ e $Y = aX+b$, com $a, b$ constantes, então
$$\mu_{Y} = \mu_{aX+b} = E(aX + b) = a E(X) + b = a\mu_X + b.$$
:::

:::

## 2.1 Esperança e variância de vad's {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

É verdade que $E(aX + b) = a E(X) + b$. Mas, não necessariamente vale que  $E[h(X)] = h[E(X)]$.

:::

::: {.fragment style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 6 (cont.):** Sejam $p_{-2} = p_2 = \frac{1}{4}$ e $p_0 = \frac{1}{2}$. [Então, temos
$$\textstyle E(X) = -2\frac{1}{4} + 0\frac{1}{2} + 2\frac{1}{4} = 0$$]{.fragment}
[e
$$\textstyle E(X^2) = (-2)^2\frac{1}{4} + 0^2\frac{1}{2} + 2^2\frac{1}{4} = 2.$$]{.fragment}

::: fragment

Assim, $E(X^2) = 2 \neq [E(X)]^2 = 0$.

:::

:::


## 2.1 Esperança e variância de vad's {.unnumbered .unlisted}

::: {.callout-note}
## Definição

Seja $X$ vad com fmp $p_X(x)$ e esperança $\mu$. A variância de $X$, denotada por $V(X)$, é definida por
$$\textstyle V(X) = \sum_{x}(x - \mu)^2\cdot p_X(x) = E[(X - \mu)^2].$$
O desvio padrão (DP) de $X$ é definido por $DP(X) = \sqrt{V(X)}.$ A variância pode ser denotada por $\sigma^2_X$, ou apenas $\sigma^2$, e o DP por $\sigma_X$, ou apenas $\sigma$.

:::

::: fragment

::: {.callout-caution}
## Observação

Note que a variância é definida como a esperança de $h(X) = (X-\mu)^2$. Isto é, quanto **esperamos** que a variável $X$ se desvie de sua esperança $\mu$.
:::

:::

## 2.1 Esperança e variância de vad's {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 6 (cont.):** Suponha agora que $p_2 = \frac{\alpha}{2}$, $p_{-2} = \frac{1-\alpha}{2}$ e $p_0 = \frac{1}{2}$, com $0 < \alpha < 1$. [Então,
$$\textstyle E(X) = \mu = -2\frac{1-\alpha}{2} + 2\frac{\alpha}{2} = 2\alpha - 1.$$]{.fragment}
[Então, a variância é dada por
$$\textstyle V(X) = \sigma^2 = \sum_{x}(x - \mu)^2\cdot p_X(x) = \sum_{x}[x-(2\alpha - 1)]^2 p_X(x).$$]{.fragment}
[Depois de algumas álgebras obtemos $\sigma^2_X = 1+4\alpha(1-\alpha)$.]{.fragment}

:::

::: fragment

::: {.callout-caution}
## Observação

O cálculo dos desvios quadráticos $(x-\mu)^2$ para obter $\sigma^2$ pode ser tedioso. Felizmente, temos uma fórmula que pode simplificar a sua determinação.

:::

:::

## 2.1 Esperança e variância de vad's {.unnumbered .unlisted}

::: fragment

::: {.callout-warning}
## Propriedades

::: incremental

1. Seja $X$ vad com fmp $p_X(x)$ e esperança $\mu$. Então
$$\begin{align*}
\sigma^2 &= \textstyle \sum_{x}(x - \mu)^2\cdot p_X(x) = \sum_{x}(x^2 - 2\mu x + \mu^2)\cdot p_X(x)\\
&= \textstyle \sum_{x}x^2p_X(x) - 2\mu \sum_{x}x p_X(x) + \mu^2 \sum_{x}p_X(x) = E(X^2) - 2\mu\mu + \mu^2 = E(X^2) - \mu^2.
\end{align*}$$
2. Seja $X$ vad com esperança $\mu_X$ e $Y = aX+b$, com $a, b$ constantes, então
$$\sigma_{Y}^2 = \sigma_{aX+b}^2 = a^2 \sigma_X^2.$$
:::

:::

:::

::: fragment

::: {.callout-caution}
## Observações

::: incremental
- A Propriedade 1 pode ser utilizada para facilmente se chegar a variância do exemplo anterior;
- A Propriedade 2 mostra que a variância só é afetada por mudanças em $a$ (escala), e não em $b$ (locação).
:::

:::

:::

## 2.1 Esperança e variância de vad's {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 7:** Seja $X$ o número obtido no arremesso de um dado honesto. Um jogo consiste de você pagar $Y = \frac{1}{X}$ e receber um prêmio de $\frac{1}{\mu_X}$ independente do resultado do dado. [Será que o jogo é vantajoso para o jogador?]{.fragment fragment-index=1}

[Note que $\mu_X = (1+2+\cdots+6)\frac{1}{6} = 3.5$, de onde vem que o prêmio é sempre $\frac{1}{3.5} \approx 0.2857$.]{.fragment fragment-index=2}

[Por outro lado, temos
$$\textstyle \mu_Y = E(Y) = E(\frac{1}{X}) = (1+\frac{1}{2}+\cdots+\frac{1}{6})\frac{1}{6} = \frac{1}{6}\frac{(60+30+20+15+12+10)}{60} = \frac{147}{360} = 0.4083.$$]{.fragment fragment-index=3}

[Assim, isso significa, em média, pagar $0.4083$ para jogar um jogo que oferece prêmio fixo de $0.2857$.]{.fragment fragment-index=4}

:::

::: fragment

::: {.callout-tip}
## Exercícios

Qual seria a variância do valor pago?
:::

:::

## {.unnumbered .unlisted .smaller}

### Exemplo 8 {.unnumbered .unlisted}

Uma loja de computadores comprou 3 computadores de certo tipo a R\$ $1000$ cada. Eles serão vendidos a R\$
$1500$ cada. Após um período, o fabricante aceita os não vendidos por R\$ 400 cada. Seja $X$ o número de computadores vendidos e suponha que $p_X(0) = 0.1$, $p_X(1) = 0.2$, $p_X(2)=0.3$ e $p_X(3) = 0.4$. [Note que
$$\mu_X = 0\cdot0.1 + 1\cdot0.2 + 2\cdot0.3 + 3\cdot0.4 = 2$$
e
$$\sigma^2_X = 0^2\cdot0.1 + 1^2\cdot0.2 + 2^2\cdot0.3 + 3^2\cdot0.4 - 2^2 = 0.2 + 4\cdot0.3 + 9\cdot0.4 - 4 = 5 - 4 = 1.$$]{.fragment}

[Por sua vez, o lucro no período seria de
$$L = h(X) = 1500X - 3000 + 400(3-X) = 1100X - 1800.$$]{.fragment}

[Logo, o lucro esperado será $\mu_L = 1100\mu_x-1800 = 1100\cdot 2 - 1800 = 400$ e a variância do lucro será de $\sigma_L = 1100^2\sigma^2_X = 1100^2\cdot 1 = 1100^2$. O desvio-padrão do lucro é de $\sigma_L = \sqrt{1100^2} = 1100$.]{.fragment}

## Modelos probabilísticos discretos

::: {.callout-caution}
## Observação

Em muitas situações, lidamos com experimentos cujo resultado é dicotômico (possui apenas dois resultados) ou pode ser dicotomizado.
:::

::: {.fragment style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 9:** Um exercício possui 5 alternativas de resposta. Um estudante decide responder o exercício aleatoriamente. Duas possíveis formas de escrever o espaço amostral são:

<table>
<tr class=fragment><td>$\Omega = \{a, b, c, d, e\}$</td> <td>(do ponto de vista de todas alternativas possíveis)</td></tr>
<tr class=fragment style="border-bottom:none;"><td>$\Omega = \{s,f\}$</td> <td>(do ponto de vista de se a alternativa está correta ($s$) ou errada $f$)</td></tr>
</table>

[Note que o segundo espaço amostral é escrita de maneira dicotomizada.]{.fragment}
:::

## 2.2 Modelos probabilísticos discretos {.unnumbered .unlisted}

::: {.callout-note}
## Definição

Dizemos que um experimento aleatório é um experimento de Bernoulli se seu espaço amostral é dicotômico e pode ser escrito como $\Omega = \{s,f\}$, em que costumamos denominar $s =$ sucesso e $f =$ fracasso. Normalmente, denotamos a probabilidade de sucesso por $P(\{s\}) = p$, $0\leq p\leq 1$.
:::

::: fragment

::: {.callout-note}
## Definição

Num experimento de Bernoulli com $P(\{s\}) = p$, podemos definir a vad
$$X = \begin{cases}
1, & \text{ se } \ \ s;\\
0, & \text{ se } \ \ f.
\end{cases}$$
Nesse caso, dizemos que $X$ tem distribuição **Bernoulli** com probabilidade de sucesso $p$ e usamos a notação $X \sim \text{Ber}(p)$.
:::

:::

## 2.2 Modelos probabilísticos discretos {.unnumbered .unlisted}

::: {.callout-warning}
## Propriedade

Se $X \sim \text{Ber}(p)$, então

<table>
  <tr style="border-bottom:none;text-align:center;">
    <td>$\mu = E(X) = p$</td> <td>e</td> <td>$\sigma^2 = V(X) = p(1-p).$</td>
  </tr>
</table>

:::

::: {.fragment style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 9 (cont.):** Defina a vad $X$ como $X = 1$, se a alternativa está correta, e $X = 0$, se a alternativa está errada. Então $X \sim \text{Ber}(p)$, com $p = \frac{1}{5}$.

:::

::: fragment

::: {.callout-caution}
## Observações

::: incremental

1. No Exemplo 9, definimos como sucesso o aluno acertar a questão, mas esse não precisa ser o caso. A classificação do que será entendido como **sucesso** dependerá do problema em questão.
2. O experimento de Bernoulli pode ser utilizado para construção de vad's mais complexas.

:::

:::

:::

## {.unnumbered .unlisted .smaller}

### Exemplo 9 (cont.) {.unnumbered .unlisted}

Se o estudante responde aleatoriamente uma prova com 4 exercícios de 5 alternativas cada, tratam-se de 4 realizações **independentes** de um experimento de Bernoulli com $P(\{s\}) = p = \frac{1}{5}$. 

::: {.fragment fragment-index=1}

Defina $X =$ "número de exercícios respondidos corretamente". Note que $\text{Im}(X) = \{0,1,2,3,4\}$. A fmp de $X$ é dada por

<table>
  <tr>
    <td style="border-top:solid;border-bottom:solid;">$\omega$</td>
    <td style="text-align:center;border-top:solid;border-bottom:solid">$X(\omega)$</td>
    <td style="text-align:center;border-top:solid;border-bottom:solid">$P(\{\omega\})$</td>
    <td style="text-align:center;border-top:none;border-bottom:none;visibility:hidden;">$P(X = x)$</td>
  </tr>
  <tr>
    <td>[$(ffff)$]{.fragment fragment-index=2}</td>
    <td style="text-align:center;">[$0$]{.fragment fragment-index=2}</td>
    <td style="text-align:center;">[$p^0(1-p)^4$]{.fragment fragment-index=2}</td>
    <td style="text-align:center;visibility:hidden;">$p^0(1-p)^4$</td>
  </tr>
  <tr>
    <td>[$(sfff)$, $(fsff)$, $(ffsf)$, $(fffs)$]{.fragment fragment-index=3}</td>
    <td style="text-align:center;">[$1$]{.fragment fragment-index=3}</td>
    <td style="text-align:center;">[$p^1(1-p)^3$]{.fragment fragment-index=3}</td>
    <td style="text-align:center;visibility:hidden;">$4p^1(1-p)^3$</td>
  </tr>
  <tr>
    <td>[$(ssff)$, $(sfsf)$, $(sffs)$, $(fssf)$, $(fsfs)$, $(ffss)$]{.fragment fragment-index=4}</td>
    <td style="text-align:center;">[$2$]{.fragment fragment-index=4}</td>
    <td style="text-align:center;">[$p^2(1-p)^2$]{.fragment fragment-index=4}</td>
    <td style="text-align:center;visibility:hidden;">$6p^2(1-p)^2$</td>
  </tr>
  <tr>
    <td>[$(sssf)$, $(ssfs)$, $(sfss)$, $(fsss)$]{.fragment fragment-index=5}</td>
    <td style="text-align:center;">[$3$]{.fragment fragment-index=5}</td>
    <td style="text-align:center;">[$p^3(1-p)^1$]{.fragment fragment-index=5}</td>
    <td style="text-align:center;visibility:hidden;">$4p^3(1-p)^1$</td>
  </tr>
  <tr style="border-bottom:none">
    <td style="border-bottom:solid">[$(ssss)$]{.fragment fragment-index=6}</td>
    <td style="text-align:center;border-bottom:solid">[$4$]{.fragment fragment-index=6}</td>
    <td style="text-align:center;border-bottom:solid">[$p^4(1-p)^0$]{.fragment fragment-index=6}</td>
    <td style="text-align:center;border-bottom:none;visibility:hidden;">$p^4(1-p)^0$</td>
  </tr>
</table>

:::

[Nesse caso, dizemos que $X$ tem distribuição **Binomial** com $4$ repetições e probabilidade de sucesso $\frac{1}{5}$.]{style="visibility:hidden"}

## {.unnumbered .unlisted .smaller}

### Exemplo 9 (cont.) {.unnumbered .unlisted}

Se o estudante responde aleatoriamente uma prova com 4 exercícios de 5 alternativas cada, tratam-se de 4 realizações **independentes** de um experimento de Bernoulli com $P(\{s\}) = p = \frac{1}{5}$. 

Defina $X =$ "número de exercícios respondidos corretamente". Note que $\text{Im}(X) = \{0,1,2,3,4\}$. A fmp de $X$ é dada por

<table>
  <tr>
    <td style="border-top:solid;border-bottom:solid;">$\omega$</td>
    <td style="text-align:center;border-top:solid;border-bottom:solid">$X(\omega)$</td>
    <td style="text-align:center;border-top:solid;border-bottom:solid">$P(\{\omega\})$</td>
    <td style="text-align:center;border-top:solid;border-bottom:solid;background-color:lightgray;">$P(X = x)$</td>
  </tr>
  <tr>
    <td>$(ffff)$</td>
    <td style="text-align:center;">$0$</td>
    <td style="text-align:center;">$p^0(1-p)^4$</td>
    <td style="text-align:center;background-color:lightgray;">$p^0(1-p)^4$</td>
  </tr>
  <tr>
    <td>$(sfff)$, $(fsff)$, $(ffsf)$, $(fffs)$</td>
    <td style="text-align:center;">$1$</td>
    <td style="text-align:center;">$p^1(1-p)^3$</td>
    <td style="text-align:center;background-color:lightgray;">$4p^1(1-p)^3$</td>
  </tr>
  <tr>
    <td>$(ssff)$, $(sfsf)$, $(sffs)$, $(fssf)$, $(fsfs)$, $(ffss)$</td>
    <td style="text-align:center;">$2$</td>
    <td style="text-align:center;">$p^2(1-p)^2$</td>
    <td style="text-align:center;background-color:lightgray;">$6p^2(1-p)^2$</td>
  </tr>
  <tr>
    <td>$(sssf)$, $(ssfs)$, $(sfss)$, $(fsss)$</td>
    <td style="text-align:center;">$3$</td>
    <td style="text-align:center;">$p^3(1-p)^1$</td>
    <td style="text-align:center;background-color:lightgray;">$4p^3(1-p)^1$</td>
  </tr>
  <tr style="border-bottom:none">
    <td style="border-bottom:solid">$(ssss)$</td>
    <td style="text-align:center;border-bottom:solid">$4$</td>
    <td style="text-align:center;border-bottom:solid">$p^4(1-p)^0$</td>
    <td style="text-align:center;border-bottom:solid;background-color:lightgray;">$p^4(1-p)^0$</td>
  </tr>
</table>

::: fragment

Nesse caso, dizemos que $X$ tem distribuição **Binomial** com $4$ repetições e probabilidade de sucesso $\frac{1}{5}$.

:::

## 2.2 Modelos probabilísticos discretos {.unnumbered .unlisted}

::: {.callout-note}
## Definição

Considere $n$ repetições independentes de um experimento de Bernoulli com probabilidade de sucesso $p$ e seja $X =$ "número de sucessos nas $n$ repetições". Dizemos que $X$ tem distribuição **Binomial** com $n$ repetições e probabilidade de sucesso $p$, denotada por $X \sim \text{Bin}(n,p)$. A fmp de $X$ é
$$p_X(x) = P(X = x) = {n \choose x} p^x (1-p)^{n-x}, \ \ x=0,1,2,\ldots,n.$$
:::

::: {.callout-caution}
## Observação

Note que, se $X_i \sim \text{Ber}(p)$ é a va Bernoulli associada à $i$-ésima repetição, então podemos escrever $X = \sum_{i=1}^nX_i$. Isto é, a va Binomial pode ser vista como soma de $n$ va's Bernoulli indendentes com a mesma probabilidade de sucesso.
:::

## 2.2 Modelos probabilísticos discretos {.unnumbered .unlisted}

::: {.callout-warning}
## Propriedade

Se $X \sim \text{Bin}(n,p)$, então

<table>
  <tr style="border-bottom:none;text-align:center;">
    <td>$\mu = E(X) = np$</td> <td>e</td> <td>$\sigma^2 = V(X) = np(1-p).$</td>
  </tr>
</table>

:::

::: {.fragment style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 9 (cont.):** Como a prova tem $n=4$ questões, cada uma com $5$ alternativas ($p=\frac{1}{5}$), temos que $\mu = E(X) = np = 4 \cdot \frac{1}{5} = 0.8$ e $\sigma^2 = V(X) = np(1-p) = 4 \cdot \frac{1}{5} \cdot \frac{4}{5} = 0.64$. Logo, $\sigma = 0.8$. Portanto, em média, o estudante acerta menos do que 1 das 4 questões.

::: fragment

A probabilidade de ele acertar mais da metade da prova é
$$\textstyle P(X > 2) = P(X = 3) + P(X = 4) = {4 \choose 3} (\frac{1}{5})^3 (\frac{4}{5})^{1} + {4 \choose 4} (\frac{1}{5})^4 (\frac{4}{5})^{0} = 0.0256 + 0.0016 = 0.0272.$$

:::

:::

## 2.2 Modelos probabilísticos discretos {.unnumbered .unlisted}


::: {.cell layout-align="center"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-1-1.png){fig-align='center' width=960}
:::
:::



## 2.2 Modelos probabilísticos discretos {.unnumbered .unlisted}


::: {.cell layout-align="center"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-2-1.png){fig-align='center' width=960}
:::
:::


## 2.2 Modelos probabilísticos discretos {.unnumbered .unlisted}


::: {.cell layout-align="center"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-3-1.png){fig-align='center' width=960}
:::
:::



## 2.2 Modelos probabilísticos discretos {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 10:** Um lote contém 10 peças, sendo 3 defeituosas. Serão sorteadas para inspeção 4 peças do lote. Seja $X =$ "número de peças defeituosas na amostra". Se a amostra resulta em no máximo 1 peça defeituosa, o lote é classificado como conforme.

Se a seleção é feita [**com reposição**]{style='color:red;'}, então estamos contando o número de sucessos (peças defeituosas) em 4 repetições independentes de um experimento de Bernoulli. Assim, $X \sim \text{Bin}(n=4, p=\frac{3}{10})$. Logo, a probabilidade do lote ser conforme é
$$\textstyle P(X \leq 1) = P(X = 0) + P(X = 1) = {4 \choose 0}(\frac{7}{10})^4 + {4 \choose 1}(\frac{3}{10})(\frac{7}{10})^3 = 0.2401 + 0.4116 = 0.6517.$$

:::

::: fragment

::: {.callout-caution}
## Observação

No Exemplo 10, a distribuição Binomial só foi apropriada para a variável $X$ pelo fato da seleção ser **com reposição**. Como veremos a seguir, $X$ terá outra distribuição quando a seleção é **sem reposição**.
:::

:::

## {.unnumbered .unlisted .smaller}

### Exemplo 11 {.unnumbered .unlisted}

Uma urna contém $M$ objetos do Tipo 1 e $N-M$ do Tipo 2. Desses, serão selecionados $n$ [**sem reposição**]{style="color:red;"}. Seja $X =$ "objetos do Tipo 1 nos $n$ selecionados". [Vamos determinar $p_X(x) = P(X=x)$.]{.fragment fragment-index=1} [Abaixo são apresentadas a quantidade de maneiras que observamos $x$ objetos do Tipo 1 e $n-x$ do Tipo 2:]{.fragment fragment-index=2}

::: {.fragment fragment-index=2}

<table>
  <tr style='border-top:solid;border-bottom:solid'>
    <td style='border-right:solid 1pt'>Objeto</td>
    <td style='border-right:solid 1pt;text-align:center' colspan=4>Tipo 1</td>
    <td style='text-align:center' colspan=4>Tipo 2</td>
  </tr>
  <tr>
    <td style='border-right:solid 1pt'>Retirada</td>
    <td style='border-right:dotted 1pt;text-align:center'>$1$</td>
    <td style='border-right:dotted 1pt;text-align:center'>$2$</td>
    <td style='border-right:dotted 1pt;text-align:center'>$\cdots$</td>
    <td style='border-right:solid 1pt;text-align:center'>$x$</td>
    <td style='border-right:dotted 1pt;text-align:center'>$x+1$</td>
    <td style='border-right:dotted 1pt;text-align:center'>$x+2$</td>
    <td style='border-right:dotted 1pt;text-align:center'>$\cdots$</td>
    <td style='text-align:center'>$n$</td>
  </tr>
  <tr style='border-top:solid 1pt;border-bottom:solid'>
    <td style='border-right:solid 1pt'>Maneiras</td>
    <td style='border-right:dotted 1pt;text-align:center'>$M$</td>
    <td style='border-right:dotted 1pt;text-align:center'>$M-1$</td>
    <td style='border-right:dotted 1pt;text-align:center'>$\cdots$</td>
    <td style='border-right:solid 1pt;text-align:center'>$M-x+1$</td>
    <td style='border-right:dotted 1pt;text-align:center'>$N-M$</td>
    <td style='border-right:dotted 1pt;text-align:center'>$N-M-1$</td>
    <td style='border-right:dotted 1pt;text-align:center'>$\cdots$</td>
    <td style='text-align:center'>$N-M-n+x+1$</td>
  </tr>
</table>

:::

[Da regra do produto, temos $\frac{M!}{(M-x)!}\frac{(N-M)!}{(N-M-(n-x))!}$.]{.fragment fragment-index=3} [Como a ordem em que os objetos são selecionados não importa, precisamos dividir esse valor pelas $x!$ permutações dos objetos do Tipo 1 e pelas $(n-x)!$ do Tipo 2, resultando em ${M \choose x} {N-M \choose n-x}$ maneiras favoráveis a $\{X = x\}$.]{.fragment fragment-index=4} [Sem nenhuma restrição, obtemos $N(N-1)\cdots(N-n+1) = \frac{N!}{(N-n)!}$.]{.fragment fragment-index=5} [Descontando as $n!$ permutações, há ${N \choose n}$ elementos em $\Omega$.]{.fragment fragment-index=6} [Assim,
$$p_X(x) = P(X = x) = \frac{ {M \choose x} {M-M \choose n-x} }{ {N \choose n} }, \ \ \max\{0, n-(N-M)\} \leq x \leq \min\{n,M\}.$$]{.fragment fragment-index=7}

## 2.2 Modelos probabilísticos discretos {.unnumbered .unlisted}

::: {.callout-note}
## Definição

Sejam $N$ itens, $M$ do Tipo 1 e $N-M$ do Tipo 2, dos quais $n$ são selecionados **sem reposição**. Seja $X =$ "itens do Tipo 1 na amostra". Dizemos que $X$ tem distribuição hipergeométrica com parâmetros $N$ (total), $M$ (itens do Tipo 1) e $n$ (tamanho da amostra) e denotamos por $X \sim \text{Hip}(N,M,n)$. A fmp de $X$ é
$$p_X(x) = \frac{ {M \choose x} {N-M \choose n-x} }{ {N \choose n} }, \ \ \max\{0, n-(N-M)\} \leq x \leq \min\{n,M\}.$$
:::

::: fragment

::: {.callout-warning}
## Propriedade

Se $X \sim \text{Hip}(N,M,n)$ e $p = \frac{M}{N}$ é a proporção de itens do Tipo 1, então

<table>
  <tr style="border-bottom:none;text-align:center;">
    <td>$\mu = E(X) = np$</td> <td>e</td> <td>$\sigma^2 = V(X) = np(1-p)(\frac{N-n}{N-1}).$</td>
  </tr>
</table>

:::

:::

## 2.2 Modelos probabilísticos discretos {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 10 (cont.):** Se a seleção fosse realizada [**sem reposição**]{style="color:red;"}, então $X \sim \text{Hip}(N=10, M=3, n=4)$, logo a probabilidade do lote ser conforme é
$$P(X \leq 1) = P(X=0) + P(X=1) = \frac{ {3 \choose 0} {7 \choose 4} }{ {10 \choose 4} } + \frac{ {3 \choose 1} {7 \choose 3} }{ {10 \choose 4} } = 0.1667 + 0.5 = 0.6667.$$

:::

::: fragment

::: {.callout-caution}
## Observação

Note o efeito do tipo de seleção em algumas características da vad $X$:

<table style="margin-bottom: 12pt !important;">
  <tr style='border-top:solid;border-bottom:solid'>
    <td style='border-right:solid 1pt;'>Seleção</td>
    <td>$P(X \leq 1)$</td>
    <td>$E(X)$</td>
    <td>$V(X)$</td>
  </tr>
  <tr>
    <td style='border-right:solid 1pt;'>Com reposição</td>
    <td>$0.6517$</td>
    <td>$1.2\ \ [np]$</td>
    <td>$0.84\ \ [np(1-p)]$</td>
  </tr>
  <tr style='border-bottom:solid;'>
    <td style='border-right:solid 1pt;'>Sem reposição</td>
    <td>$0.6667$</td>
    <td>$1.2 \ \ [np]$</td>
    <td>$0.56 \ \ [np(1-p)(\frac{N-n}{N-1})]$</td>
  </tr>
</table>

:::

:::

## 2.2 Modelos probabilísticos discretos {.unnumbered .unlisted}



::: {.cell layout-ncol="2" layout-align="center" fig.ncol='2'}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-4-1.png){fig-align='center' width=576}
:::

::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-4-2.png){fig-align='center' width=576}
:::
:::


## {.unnumbered .unlisted .smaller}

### Exemplo 12 {.unnumbered .unlisted}

Um sistema de transações **independentes** possui 3 computadores que operam de modo redundante:

- se o 1º apresenta falha de transação (com probabilidade $p$), o 2º entra em operação;
- se o 2º apresenta falha de transação (com probabilidade $p$), o 3º entra em operação;
- se o 3º apresenta falha de transação (com probabilidade $p$), o sistema é interrompido;

[Tratam-se de repetições independentes de um experimento de Bernoulli com $P(\{s\}) = p$ até obter o 3º sucesso.]{.fragment fragment-index=1} [Seja $X =$ "número de transações realizadas". Note que $\text{Im}(X) = \{3,4,\ldots\}$.]{.fragment fragment-index=2} [Veja a seguinte tabela:]{.fragment fragment-index=3}

::: {.fragment fragment-index=3}

<table>
  <tr style="border-top:solid;border-bottom:solid">
    <td style="text-align:left;border-right:solid 1pt;">$\omega$</td>
    <td style="text-align:center;border-right:solid 1pt;">$x$</td>
    <td style="text-align:center;border-right:solid 1pt;">$P(\{\omega\})$</td>
    <td style="text-align:center;">$P(X=x)$</td>
  </tr>
  <tr>
    <td style="text-align:left;border-right:solid 1pt;">$(sss)$</td>
    <td style="text-align:center;border-right:solid 1pt;">$3$</td>
    <td style="text-align:center;border-right:solid 1pt;">$p^3$</td>
    <td style="text-align:center;">$p^3$</td>
  </tr>
  <tr>
    <td style="text-align:left;border-right:solid 1pt;">$(ssfs)$, $(sfss)$, $(fsss)$</td>
    <td style="text-align:center;border-right:solid 1pt;">$4$</td>
    <td style="text-align:center;border-right:solid 1pt;">$(1-p)p^3$</td>
    <td style="text-align:center;">$3(1-p)p^3$</td>
  </tr>
  <tr>
    <td style="text-align:left;border-right:solid 1pt;">$(ssffs)$, $(sfsfs)$, $(fssfs)$, $(sffss)$, $(fsfss)$, $(ffsss)$</td>
    <td style="text-align:center;border-right:solid 1pt;">$5$</td>
    <td style="text-align:center;border-right:solid 1pt;">$(1-p)^2p^3$</td>
    <td style="text-align:center;">$6(1-p)^2p^3$</td>
  </tr>
  <tr style="border-bottom:solid">
    <td style="text-align:left;border-right:solid 1pt;">$\vdots$</td>
    <td style="text-align:center;border-right:solid 1pt;">$\vdots$</td>
    <td style="text-align:center;border-right:solid 1pt;">$\vdots$</td>
    <td style="text-align:center;">$\vdots$</td>
  </tr>
</table>

:::

## {.unnumbered .unlisted .smaller}

### Exemplo 12 (cont.) {.unnumbered .unlisted}

Assim, notando que a última repetição tem que ser $s$, um exemplo de $\omega$ favorável a $[X = x]$ é
$$\omega = (\underbrace{ssff\ldots f}_{x-1}s),$$
cuja probabilidade é $P(\{\omega\}) = (1-p)^{x-3}p^3$. [Os outros resultados favoráveis a $[X=x]$ têm a mesma probabilidade e são contados verificando de quantas formas podemos posicionar os dois sucessos dentre as primeiras $x-1$ repetições.]{.fragment fragment-index=1} [Para o 1º $s$, temos $x-1$ posições e, para o 2º $s$, temos $x-2$ posições.]{.fragment fragment-index=2}

[Pela regra da multiplicação teríamos $(x-1)(x-2) = \frac{(x-1)!}{(x-3)!}$ maneiras possíveis.]{.fragment fragment-index=3} [Como a ordem que escolhemos a posição não importa (escolher 1 e 2 é o mesmo que 2 e 1, por exemplo), precisamos descontar as $2!$ permutações possíveis entre as duas, o que resulta em $\frac{(x-1)!}{2!(x-3)!} = { x-1 \choose 2 }$ maneiras possíveis.]{.fragment fragment-index=4} [Assim
$$P(X = x) = { x-1 \choose 2 } (1-p)^{x-3} p^x, \ \ \ x = 3, 4, 5, \ldots.$$]{.fragment fragment-index=5}

## 2.2 Modelos probabilísticos discretos {.unnumbered .unlisted}

::: {.callout-note}
## Definição

Um experimento de Bernoulli com $P(\{s\}) = p$ é repetido **independentemente** até a ocorrência do $k$-ésimo sucesso. Seja $X =$ "número de repetições realizadas". Dizemos que $X$ tem distribuição Binomial Negativa com $k$ sucessos e probabilidade de sucesso $p$, denotada por $X \sim \text{BN}(k,p)$. A fmp de $X$ é
$$p_X(x) = P(X = x) = { x-1 \choose k-1 } (1-p)^{x-k} p^k, \ \ \ x = k, k+1, k+2, \ldots.$$
:::

::: fragment

::: {.callout-warning}
## Propriedades

Se $X \sim \text{BN}(k,p)$, então

<table>
  <tr style="border-bottom:none;text-align:center;">
    <td>$\mu = E(X) = \frac{k}{p}$</td> <td>e</td> <td>$\sigma^2 = V(X) = k\frac{(1-p)}{p^2}.$</td>
  </tr>
</table>
:::

:::

## 2.2 Modelos probabilísticos discretos {.unnumbered .unlisted}

::: {.callout-caution}
## Observações

::: incremental

1. No Exemplo 12, temos que $X \sim \text{BN}(k=3, p)$. Se $p = 0.01$, por exemplo, teríamos $\mu = E(X) = \frac{3}{0.01} = 300$, $\sigma^2 = V(X) = 3\frac{0.99}{0.01^2} = 29700$ e $\sigma \approx 172.34$. Em média, são realizadas $300$ transações até a terceira falha com DP de $172.34$. Além disso, $P(X > \mu) = P(X > 300) \approx 0.4221$;
2. A distribuição BN também pode ser definida como a distribuição do número de fracassos (em vez de repetições) até o $k$-ésimo sucesso. Nesse caso, sua fmp é
$$\textstyle p_X(x) = { x + k -1 \choose k-1 } (1-p)^{x} p^k, \ \ \ x = 0, 1, 2, \ldots,$$
e sua esperança e variância são, respectivamente, $\mu = k\frac{(1-p)}{p}$ e $\sigma^2 = k\frac{(1-p)}{p^2}$;
3. Se $X \sim \text{BN}(k = 1, p)$, dizemos que $X$ tem distribuição geométrica, cuja notação é $X \sim \text{Geo}(p)$;
4. Se $X \sim \text{BN}(k, p)$, então $X = \sum_{j=1}^k X_j$, em que $X_1,\ldots,X_k \sim \text{Geo}(p)$ independentes.
5. Bin: repetições fixas e sucessos aleatórios; BN: sucessos fixos e repetições aleatórias.

:::

:::

# Variáveis aleatórias contínuas

## 3 Variáveis aleatórias contínuas {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

Anteriormente, definimos uma vac $X$ como sendo aquelas cuja imagem $\text{Im}(X)$ é não enumerável. De agora em diante, as vac's serão restringidas àquelas em que a fda é [**absolutamente contínua**]{style="color:red"}.
:::

::: {.callout-note}
## Definição

Diremos que $X$ é va **contínua** (vac) se sua imagem $\text{Im}(X)$ é não enumerável e se sua fda $F_X(x) = P(X \leq x)$ é **absolutamente contínua**. Neste caso, podemos escrever
$$F_X(x) = \int_{-\infty}^x f_X(t)dt,$$
em que $f_X(\cdot)$ é denominada **função densidade de probabilidade** (fdp).
:::

## 3 Variáveis aleatórias contínuas {.unnumbered .unlisted}

::: {.callout-warning}
## Propriedades
Seja $X$ vac com fda $F_X(\cdot)$ e fdp $f_X(\cdot)$, então:

::: incremental

1. sua fdp satisfaz:
    + $f_X(\cdot) \geq 0$;
    + $\int_{-\infty}^\infty f_X(x)dx = 1$.
2. a probabilidade do intervalo $(a,b]$, $a<b$, é dada por
$$\textstyle P(a < X \leq b) = F_X(b) - F_X(a) = \int_a^b f_X(x) dx;$$
3. a probabilidade de um ponto $x$ é $P(X=x) = 0$;
4. valem as igualdades $P(a < X \leq b) = P(a \leq X \leq b) = P(a \leq X < b) = P(a < X < b)$, sendo que o mesmo não é válido no caso discreto.

:::

:::

## {.unnumbered .unlisted .smaller}

### Exemplo 13 {.unnumbered .unlisted}

Tempo de avanço é a diferença entre o instante em que um carro termina de passar por um ponto e o instante em que o próximo carro começa a passar por esse ponto. Seja $X =$ "tempo de avanço para dois carros escolhidos ao acaso". O artigo "*The Statistical Properties of Freeway Traffic*" sugeriu a fdp
$$f_X(x) = 0.15e^{-0.15(x-0.5)} \mathbb{I}(x \geq 0.5) = \begin{cases}
0.15e^{-0.15(x-0.5)}, & x \geq 0.5;\\
0, & x < 0.5,
\end{cases}$$
em que $\mathbb{I}(A) = 1$, se a condição $A$ é válida, e $\mathbb{I}(A) = 0$, caso contrário.

::: fragment

Note que $f_X(x) \geq 0$ e que $\int_{-\infty}^\infty f_X(x)dx = 1$. Vamos encontrar $P(X > 5)$. Note que
$$P(X > 5) = \int_{5}^\infty f_X(x) dx = \int_{5}^\infty 0.15e^{-0.15(x-0.5)} dx = \left[\left.-e^{-0.15(x-0.5)}\right|_5^\infty\right] = e^{-0.675} \approx 0.5092.$$

:::

## {.unnumbered .unlisted .smaller}

### Exemplo 13 (cont.) {.unnumbered .unlisted}

Veja abaixo a representação da fdp e a da probabilidade $P(X > 5)$:


::: {.cell layout-align="center"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-5-1.png){fig-align='center' width=768}
:::
:::


## 3 Variáveis aleatórias contínuas {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

É importante reforçar que podemos obter a fdp $f_X(\cdot)$ da fda $F_X(\cdot)$ e vice-versa, por meio de
$$\textstyle f_X(x) = \frac{d}{dx}F_X(x)\ \ \ \ \text{e} \ \ \ \ F_X(x) = \int_{-\infty}^x f_X(t)dt.$$
:::

::: {.fragment style="border-style: solid; border-width: 3px; padding-bottom: 12px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 13 (cont.):** No caso, dada a fdp, podemos obter a fda como a antiderivada de $f_X(x)$
[$$\textstyle F_X(x) = \int_{-\infty}^{0.5}0dt + \int_{0.5}^x 0.15e^{-0.15(t-0.5)}dt = 0 + \left[\left.-e^{-0.15(t-0.5)}\right|_{0.5}^x\right] = 1-e^{-0.15(x-0.5)}.$$]{.fragment}
[Agora, a fda pode ser utilizada para obter a probabilidade anterior:
$$\textstyle P(X > 5) = 1- P(X \leq 5) = 1- F_X(5) = 1-[1-e^{-0.15(5-0.5)}] = e^{-0.675} \approx 0.5092.$$]{.fragment}
:::

## 3 Variáveis aleatórias contínuas {.unnumbered .unlisted}


::: {.callout-caution}
## Observação

A inversa de $F_X(x)$ pode ser utilizada para encontrar os quantis.
:::

::: {.fragment style="border-style: solid; border-width: 3px; padding-bottom: 12px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 13 (cont.):** Vimos que $F_X(x) = 1-e^{-0.15(x-0.5)}$. Vamos determinar a mediana de $X$, denotada por $\tilde{\mu}_X$. Para $\tilde{\mu}_X$ ser a mediana, devemos ter $F_X(\tilde{\mu}_X) = 0.5$. [Logo
$$1-e^{-0.15(\tilde{\mu}_X-0.5)} = 0.5 \Rightarrow e^{-0.15(\tilde{\mu}_X-0.5)} = 0.5 \Rightarrow \tilde{\mu}_X = 0.5 -\frac{20}{3}\log(0.5) \approx 5.121.$$]{.fragment}
:::

::: fragment

::: {.callout-tip}
## Exercício

Encontre o quantil de ordem $p$, denotado por $Q_p$, isto é, o valor tal que $F_X(Q_p) = p$.
:::

:::

## Esperança e variância de vac's

::: {.callout-caution}
## Observação

Em Estatística Descritiva, ao tratar de distribuições intervalares, uma aproximação para a média era
$$\textstyle \bar{x} \approx \sum_{i}x_i^{(m)} f_i = \sum_{i}x_i^{(m)} d_i h_i,$$
em que $x_i^{(m)}$, $f_i$, $d_i$ e $h_i$ são, respectivamente, o ponto médio, a frequência relativa, a [**densidade**]{style="color:red"} e o [**comprimento**]{style="color:red"} do intervalo $i$. Como a fdp $f_X(x)$ é um modelo teórico para as densidades $d_i$ no intervalo de comprimento infinitesimal $dx$ em torno de $x$, isso motiva a seguinte definição de esperança.
:::

::: fragment

::: {.callout-note}
## Definição

Seja $X$ vac com fdp $f_X(x)$, então a sua esperança é definida por
$$\textstyle \mu = \mu_X = E(X) = \int_{-\infty}^\infty xf_X(x)dx.$$
:::

:::

## 3.1 Esperança e variância de vac's {.unnumbered .unlisted}

::: {.callout-warning}
## Propriedade

Da mesma forma que no caso discreto, se $X$ é vac e $Y = h(X)$, então
$$\textstyle \mu_Y = E(Y) = E[h(X)] = \int_{-\infty}^\infty h(x) f_X(x) dx.$$
:::

::: fragment

::: {.callout-caution}
## Observação

A propriedade acima contorna a necessidade de obter $f_Y(y)$ para calcular $\mu_Y$ via $\mu_Y = \int_{-\infty}^\infty y f_Y(y)dy$.
:::

:::

::: fragment

::: {.callout-note}
## Definição

Seja $X$ vac com fdp $f_X(x)$, então a sua variância é definida por
$$\textstyle \sigma^2 = \sigma^2_X = V(X) = E[(X-\mu)^2] = \int_{-\infty}^\infty (x-\mu)^2f_X(x)dx.$$
:::

:::

## 3.1 Esperança e variância de vac's {.unnumbered .unlisted}

::: {.callout-warning}
## Propriedade

Da mesma forma que no caso discreto, se $X$ é vac, temos a seguinte forma alternativa para a variância:
$$\textstyle \sigma^2 = E(X^2) - \mu^2, \ \ \ \ \  E(X^2) = \int_{-\infty}^\infty x^2 f_X(x) dx.$$
:::

:::fragment

::: {.callout-warning}
## Propriedades

Da mesma forma que no caso discreto, se $X$ é vac e $a$ e $b$ são constantes, então:

::: incremental

1. $\mu_{aX+b} = E(aX + b) = aE(X) + b = a\mu_X + b$;
2. $\sigma_{aX+b}^2 = V(aX + b) = a^2V(X) = a^2\sigma_X^2$;
3. $\sigma_{aX+b} = DP(aX + b) = aDP(X) = a\sigma_X$.

:::

:::

:::

## 3.1 Esperança e variância de vac's {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 12px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 13 (cont.):**

Vamos calcular $\mu$. [Tomando $s = 0.15(x - 0.5)$, então $0.15x = s+0.15\cdot0.5$ e $ds = 0.15dx$.]{style='color:white'} [Portanto,]{style='color:white'}
$$\begin{align*}
\color{white}{\mu} &\color{white}{=}{\textstyle \color{white}{\int_{-\infty}^{0.5} x\cdot 0 dx + \int_{0.5}^{\infty} x\cdot 0.15e^{-0.15(x-0.5)} dx}\color{white}{=\int_{0}^\infty (s+0.15\cdot0.5)e^{-s}\frac{ds}{0.15}}}\\
&\color{white}{=}{\textstyle \color{white}{\frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5\int_{0}^\infty e^{-s}ds}\color{white}{= \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5.}}\\
\end{align*}$$

[Na integral após a última igualdade, fazendo $u = s$ e $dv = e^{-s}ds$, vem que $du=ds$ e $v = -e^{-s}$.]{style='color:white;'} [Logo,]{style='color:white;'}
$${\textstyle\color{white}{\mu = 0.5 + \frac{1}{0.15}\{[-\frac{s}{e^s}|_0^\infty] + \int_0^{\infty}e^{-s}ds\}}\color{white}{= 0.5 + \frac{20}{3}[0 + 1]}\color{white}{= \frac{3 + 40}{6} = \frac{43}{6} \approx 7.1667.}}$$

[Note que obtivemos $\mu = 7.1667 > \tilde\mu = 5.121$, o que reflete a assimetria à direita da fdp.]{style='color:white;'}

:::

::: {style='visibility:hidden;'}

::: {.callout-tip}
## Exercícios

Calcule $\sigma^2$ para a vac $X$ do Exemplo 13.
:::

:::


## 3.1 Esperança e variância de vac's {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 12px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 13 (cont.):**

Vamos calcular $\mu$. Tomando $s = 0.15(x - 0.5)$, então $0.15x = s+0.15\cdot0.5$ e $ds = 0.15dx$. [Portanto,]{style='color:white'}
$$\begin{align*}
\color{white}{\mu} &\color{white}{=}{\textstyle \color{white}{\int_{-\infty}^{0.5} x\cdot 0 dx + \int_{0.5}^{\infty} x\cdot 0.15e^{-0.15(x-0.5)} dx}\color{white}{=\int_{0}^\infty (s+0.15\cdot0.5)e^{-s}\frac{ds}{0.15}}}\\
&\color{white}{=}{\textstyle \color{white}{\frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5\int_{0}^\infty e^{-s}ds}\color{white}{= \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5.}}\\
\end{align*}$$

[Na integral após a última igualdade, fazendo $u = s$ e $dv = e^{-s}ds$, vem que $du=ds$ e $v = -e^{-s}$.]{style='color:white;'} [Logo,]{style='color:white;'}
$${\textstyle\color{white}{\mu = 0.5 + \frac{1}{0.15}\{[-\frac{s}{e^s}|_0^\infty] + \int_0^{\infty}e^{-s}ds\}}\color{white}{= 0.5 + \frac{20}{3}[0 + 1]}\color{white}{= \frac{3 + 40}{6} = \frac{43}{6} \approx 7.1667.}}$$

[Note que obtivemos $\mu = 7.1667 > \tilde\mu = 5.121$, o que reflete a assimetria à direita da fdp.]{style='color:white;'}

:::

::: {style='visibility:hidden;'}

::: {.callout-tip}
## Exercícios

Calcule $\sigma^2$ para a vac $X$ do Exemplo 13.
:::

:::



## 3.1 Esperança e variância de vac's {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 12px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 13 (cont.):**

Vamos calcular $\mu$. Tomando $s = 0.15(x - 0.5)$, então $0.15x = s+0.15\cdot0.5$ e $ds = 0.15dx$. Portanto, 
$$\begin{align*}
\mu &={\textstyle \int_{-\infty}^{0.5} x\cdot 0 dx + \int_{0.5}^{\infty} x\cdot 0.15e^{-0.15(x-0.5)} dx\color{white}{=\int_{0}^\infty (s+0.15\cdot0.5)e^{-s}\frac{ds}{0.15}}}\\
&\color{white}{=}{\textstyle \color{white}{\frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5\int_{0}^\infty e^{-s}ds}\color{white}{= \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5.}}\\
\end{align*}$$

[Na integral após a última igualdade, fazendo $u = s$ e $dv = e^{-s}ds$, vem que $du=ds$ e $v = -e^{-s}$.]{style='color:white;'} [Logo,]{style='color:white;'}
$${\textstyle\color{white}{\mu = 0.5 + \frac{1}{0.15}\{[-\frac{s}{e^s}|_0^\infty] + \int_0^{\infty}e^{-s}ds\}}\color{white}{= 0.5 + \frac{20}{3}[0 + 1]}\color{white}{= \frac{3 + 40}{6} = \frac{43}{6} \approx 7.1667.}}$$

[Note que obtivemos $\mu = 7.1667 > \tilde\mu = 5.121$, o que reflete a assimetria à direita da fdp.]{style='color:white;'}

:::

::: {style='visibility:hidden;'}

::: {.callout-tip}
## Exercícios

Calcule $\sigma^2$ para a vac $X$ do Exemplo 13.
:::

:::




## 3.1 Esperança e variância de vac's {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 12px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 13 (cont.):**

Vamos calcular $\mu$. Tomando $s = 0.15(x - 0.5)$, então $0.15x = s+0.15\cdot0.5$ e $ds = 0.15dx$. Portanto, 
$$\begin{align*}
\mu &={\textstyle \int_{-\infty}^{0.5} x\cdot 0 dx + \int_{0.5}^{\infty} x\cdot 0.15e^{-0.15(x-0.5)} dx = \int_{0}^\infty (s+0.15\cdot0.5)e^{-s}\frac{ds}{0.15}}\\
&\color{white}{=}{\textstyle \color{white}{\frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5\int_{0}^\infty e^{-s}ds}\color{white}{= \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5.}}\\
\end{align*}$$

[Na integral após a última igualdade, fazendo $u = s$ e $dv = e^{-s}ds$, vem que $du=ds$ e $v = -e^{-s}$.]{style='color:white;'} [Logo,]{style='color:white;'}
$${\textstyle\color{white}{\mu = 0.5 + \frac{1}{0.15}\{[-\frac{s}{e^s}|_0^\infty] + \int_0^{\infty}e^{-s}ds\}}\color{white}{= 0.5 + \frac{20}{3}[0 + 1]}\color{white}{= \frac{3 + 40}{6} = \frac{43}{6} \approx 7.1667.}}$$

[Note que obtivemos $\mu = 7.1667 > \tilde\mu = 5.121$, o que reflete a assimetria à direita da fdp.]{style='color:white;'}

:::

::: {style='visibility:hidden;'}

::: {.callout-tip}
## Exercícios

Calcule $\sigma^2$ para a vac $X$ do Exemplo 13.
:::

:::



## 3.1 Esperança e variância de vac's {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 12px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 13 (cont.):**

Vamos calcular $\mu$. Tomando $s = 0.15(x - 0.5)$, então $0.15x = s+0.15\cdot0.5$ e $ds = 0.15dx$. Portanto, 
$$\begin{align*}
\mu &={\textstyle \int_{-\infty}^{0.5} x\cdot 0 dx + \int_{0.5}^{\infty} x\cdot 0.15e^{-0.15(x-0.5)} dx = \int_{0}^\infty (s+0.15\cdot0.5)e^{-s}\frac{ds}{0.15}}\\
&={\textstyle \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5\int_{0}^\infty e^{-s}ds\color{white}{= \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5.}}\\
\end{align*}$$

[Na integral após a última igualdade, fazendo $u = s$ e $dv = e^{-s}ds$, vem que $du=ds$ e $v = -e^{-s}$.]{style='color:white;'} [Logo,]{style='color:white;'}
$${\textstyle\color{white}{\mu = 0.5 + \frac{1}{0.15}\{[-\frac{s}{e^s}|_0^\infty] + \int_0^{\infty}e^{-s}ds\}}\color{white}{= 0.5 + \frac{20}{3}[0 + 1]}\color{white}{= \frac{3 + 40}{6} = \frac{43}{6} \approx 7.1667.}}$$

[Note que obtivemos $\mu = 7.1667 > \tilde\mu = 5.121$, o que reflete a assimetria à direita da fdp.]{style='color:white;'}

:::

::: {style='visibility:hidden;'}

::: {.callout-tip}
## Exercícios

Calcule $\sigma^2$ para a vac $X$ do Exemplo 13.
:::

:::



## 3.1 Esperança e variância de vac's {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 12px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 13 (cont.):**

Vamos calcular $\mu$. Tomando $s = 0.15(x - 0.5)$, então $0.15x = s+0.15\cdot0.5$ e $ds = 0.15dx$. Portanto, 
$$\begin{align*}
\mu &={\textstyle \int_{-\infty}^{0.5} x\cdot 0 dx + \int_{0.5}^{\infty} x\cdot 0.15e^{-0.15(x-0.5)} dx = \int_{0}^\infty (s+0.15\cdot0.5)e^{-s}\frac{ds}{0.15}}\\
&={\textstyle \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5\int_{0}^\infty e^{-s}ds = \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5.}\\
\end{align*}$$

[Na integral após a última igualdade, fazendo $u = s$ e $dv = e^{-s}ds$, vem que $du=ds$ e $v = -e^{-s}$.]{style='color:white;'} [Logo,]{style='color:white;'}
$${\textstyle\color{white}{\mu = 0.5 + \frac{1}{0.15}\{[-\frac{s}{e^s}|_0^\infty] + \int_0^{\infty}e^{-s}ds\}}\color{white}{= 0.5 + \frac{20}{3}[0 + 1]}\color{white}{= \frac{3 + 40}{6} = \frac{43}{6} \approx 7.1667.}}$$

[Note que obtivemos $\mu = 7.1667 > \tilde\mu = 5.121$, o que reflete a assimetria à direita da fdp.]{style='color:white;'}

:::

::: {style='visibility:hidden;'}

::: {.callout-tip}
## Exercícios

Calcule $\sigma^2$ para a vac $X$ do Exemplo 13.
:::

:::



## 3.1 Esperança e variância de vac's {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 12px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 13 (cont.):**

Vamos calcular $\mu$. Tomando $s = 0.15(x - 0.5)$, então $0.15x = s+0.15\cdot0.5$ e $ds = 0.15dx$. Portanto, 
$$\begin{align*}
\mu &={\textstyle \int_{-\infty}^{0.5} x\cdot 0 dx + \int_{0.5}^{\infty} x\cdot 0.15e^{-0.15(x-0.5)} dx = \int_{0}^\infty (s+0.15\cdot0.5)e^{-s}\frac{ds}{0.15}}\\
&={\textstyle \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5\int_{0}^\infty e^{-s}ds = \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5.}\\
\end{align*}$$

Na integral após a última igualdade, fazendo $u = s$ e $dv = e^{-s}ds$, vem que $du=ds$ e $v = -e^{-s}$. [Logo,]{style='color:white;'}
$${\textstyle\color{white}{\mu = 0.5 + \frac{1}{0.15}\{[-\frac{s}{e^s}|_0^\infty] + \int_0^{\infty}e^{-s}ds\}}\color{white}{= 0.5 + \frac{20}{3}[0 + 1]}\color{white}{= \frac{3 + 40}{6} = \frac{43}{6} \approx 7.1667.}}$$

[Note que obtivemos $\mu = 7.1667 > \tilde\mu = 5.121$, o que reflete a assimetria à direita da fdp.]{style='color:white;'}

:::

::: {style='visibility:hidden;'}

::: {.callout-tip}
## Exercícios

Calcule $\sigma^2$ para a vac $X$ do Exemplo 13.
:::

:::


## 3.1 Esperança e variância de vac's {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 12px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 13 (cont.):**

Vamos calcular $\mu$. Tomando $s = 0.15(x - 0.5)$, então $0.15x = s+0.15\cdot0.5$ e $ds = 0.15dx$. Portanto, 
$$\begin{align*}
\mu &={\textstyle \int_{-\infty}^{0.5} x\cdot 0 dx + \int_{0.5}^{\infty} x\cdot 0.15e^{-0.15(x-0.5)} dx = \int_{0}^\infty (s+0.15\cdot0.5)e^{-s}\frac{ds}{0.15}}\\
&={\textstyle \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5\int_{0}^\infty e^{-s}ds = \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5.}\\
\end{align*}$$

Na integral após a última igualdade, fazendo $u = s$ e $dv = e^{-s}ds$, vem que $du=ds$ e $v = -e^{-s}$. Logo
$${\textstyle \mu = 0.5 + \frac{1}{0.15}\{[-\frac{s}{e^s}|_0^\infty] + \int_0^{\infty}e^{-s}ds\}\color{white}{= 0.5 + \frac{20}{3}[0 + 1]}\color{white}{=\frac{3 + 40}{6} = \frac{43}{6} \approx 7.1667.}}$$

[Note que obtivemos $\mu = 7.1667 > \tilde\mu = 5.121$, o que reflete a assimetria à direita da fdp.]{style='color:white;'}

:::

::: {style='visibility:hidden;'}

::: {.callout-tip}
## Exercícios

Calcule $\sigma^2$ para a vac $X$ do Exemplo 13.
:::

:::



## 3.1 Esperança e variância de vac's {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 12px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 13 (cont.):**

Vamos calcular $\mu$. Tomando $s = 0.15(x - 0.5)$, então $0.15x = s+0.15\cdot0.5$ e $ds = 0.15dx$. Portanto, 
$$\begin{align*}
\mu &={\textstyle \int_{-\infty}^{0.5} x\cdot 0 dx + \int_{0.5}^{\infty} x\cdot 0.15e^{-0.15(x-0.5)} dx = \int_{0}^\infty (s+0.15\cdot0.5)e^{-s}\frac{ds}{0.15}}\\
&={\textstyle \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5\int_{0}^\infty e^{-s}ds = \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5.}\\
\end{align*}$$

Na integral após a última igualdade, fazendo $u = s$ e $dv = e^{-s}ds$, vem que $du=ds$ e $v = -e^{-s}$. Logo
$${\textstyle \mu = 0.5 + \frac{1}{0.15}\{[-\frac{s}{e^s}|_0^\infty] + \int_0^{\infty}e^{-s}ds\} = 0.5 + \frac{20}{3}[0 + 1]\color{white}{=\frac{3 + 40}{6} = \frac{43}{6} \approx 7.1667.}}$$

[Note que obtivemos $\mu = 7.1667 > \tilde\mu = 5.121$, o que reflete a assimetria à direita da fdp.]{style='color:white;'}

:::

::: {style='visibility:hidden;'}

::: {.callout-tip}
## Exercícios

Calcule $\sigma^2$ para a vac $X$ do Exemplo 13.
:::

:::


## 3.1 Esperança e variância de vac's {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 12px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 13 (cont.):**

Vamos calcular $\mu$. Tomando $s = 0.15(x - 0.5)$, então $0.15x = s+0.15\cdot0.5$ e $ds = 0.15dx$. Portanto, 
$$\begin{align*}
\mu &={\textstyle \int_{-\infty}^{0.5} x\cdot 0 dx + \int_{0.5}^{\infty} x\cdot 0.15e^{-0.15(x-0.5)} dx = \int_{0}^\infty (s+0.15\cdot0.5)e^{-s}\frac{ds}{0.15}}\\
&={\textstyle \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5\int_{0}^\infty e^{-s}ds = \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5.}\\
\end{align*}$$

Na integral após a última igualdade, fazendo $u = s$ e $dv = e^{-s}ds$, vem que $du=ds$ e $v = -e^{-s}$. Logo
$${\textstyle \mu = 0.5 + \frac{1}{0.15}\{[-\frac{s}{e^s}|_0^\infty] + \int_0^{\infty}e^{-s}ds\} = 0.5 + \frac{20}{3}[0 + 1] = \frac{3 + 40}{6} = \frac{43}{6} \approx 7.1667.}$$

[Note que obtivemos $\mu = 7.1667 > \tilde\mu = 5.121$, o que reflete a assimetria à direita da fdp.]{style='color:white;'}

:::

::: {style='visibility:hidden;'}

::: {.callout-tip}
## Exercícios

Calcule $\sigma^2$ para a vac $X$ do Exemplo 13.
:::

:::


## 3.1 Esperança e variância de vac's {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 12px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 13 (cont.):**

Vamos calcular $\mu$. Tomando $s = 0.15(x - 0.5)$, então $0.15x = s+0.15\cdot0.5$ e $ds = 0.15dx$. Portanto, 
$$\begin{align*}
\mu &={\textstyle \int_{-\infty}^{0.5} x\cdot 0 dx + \int_{0.5}^{\infty} x\cdot 0.15e^{-0.15(x-0.5)} dx = \int_{0}^\infty (s+0.15\cdot0.5)e^{-s}\frac{ds}{0.15}}\\
&={\textstyle \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5\int_{0}^\infty e^{-s}ds = \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5.}\\
\end{align*}$$

Na integral após a última igualdade, fazendo $u = s$ e $dv = e^{-s}ds$, vem que $du=ds$ e $v = -e^{-s}$. Logo
$${\textstyle \mu = 0.5 + \frac{1}{0.15}\{[-\frac{s}{e^s}|_0^\infty] + \int_0^{\infty}e^{-s}ds\} = 0.5 + \frac{20}{3}[0 + 1] = \frac{3 + 40}{6} = \frac{43}{6} \approx 7.1667.}$$

Note que obtivemos $\mu = 7.1667 > \tilde\mu = 5.121$, o que reflete a assimetria à direita da fdp.

:::

::: {style='visibility:hidden;'}

::: {.callout-tip}
## Exercícios

Calcule $\sigma^2$ para a vac $X$ do Exemplo 13.
:::

:::


## 3.1 Esperança e variância de vac's {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 12px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 13 (cont.):**

Vamos calcular $\mu$. Tomando $s = 0.15(x - 0.5)$, então $0.15x = s+0.15\cdot0.5$ e $ds = 0.15dx$. Portanto, 
$$\begin{align*}
\mu &={\textstyle \int_{-\infty}^{0.5} x\cdot 0 dx + \int_{0.5}^{\infty} x\cdot 0.15e^{-0.15(x-0.5)} dx = \int_{0}^\infty (s+0.15\cdot0.5)e^{-s}\frac{ds}{0.15}}\\
&={\textstyle \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5\int_{0}^\infty e^{-s}ds = \frac{1}{0.15}\int_{0}^\infty se^{-s}ds + 0.5.}\\
\end{align*}$$

Na integral após a última igualdade, fazendo $u = s$ e $dv = e^{-s}ds$, vem que $du=ds$ e $v = -e^{-s}$. Logo
$${\textstyle \mu = 0.5 + \frac{1}{0.15}\{[-\frac{s}{e^s}|_0^\infty] + \int_0^{\infty}e^{-s}ds\} = 0.5 + \frac{20}{3}[0 + 1] = \frac{3 + 40}{6} = \frac{43}{6} \approx 7.1667.}$$

Note que obtivemos $\mu = 7.1667 > \tilde\mu = 5.121$, o que reflete a assimetria à direita da fdp.

:::

::: {.callout-tip}
## Exercícios

Calcule $\sigma^2$ para a vac $X$ do Exemplo 13.
:::

## Modelos probabilísticos contínuos

::: {.callout-caution}
## Observação

Sem dúvidas, em termos práticos, o modelo probabilístico mais importante para variáveis aleatórias é o n normal. Algumas de suas características serão discutidas mais adiante.
:::

::: {.callout-note}
## Definição

Seja $X$ vac. Dizemos que $X$ tem distribuição normal com média $\mu$ e variância $\sigma^2$ e escrevemos $X \sim \text{N}(\mu,\sigma^2)$ se sua fdp for dada por
$$f_X(x) = f_X(x; \mu,\sigma) = \frac{1}{\sqrt{2\pi\sigma^2}}e^{-\frac{(x-\mu)^2}{2\sigma^2}}, \ \ \ \ \ \ -\infty <x < \infty, \ \ -\infty < \mu < \infty, \ \ \sigma^2 > 0.$$
:::


## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}


::: {.cell layout-align="center"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-6-1.png){fig-align='center' width=768}
:::
:::


## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

::: {.callout-warning}
## Propriedades

Se $X \sim \text{N}(\mu, \sigma^2)$, então
<table>
  <tr style="border-bottom:none;text-align:center;">
    <td>$E(X) = \mu$</td> <td>e</td> <td>$V(X) = \sigma^2.$</td>
  </tr>
</table>
:::

::: fragment

::: {.callout-caution}
## Observações
Se $X \sim \text{N}(\mu, \sigma^2)$, então:

::: incremental

1. a sua fdp é completamente especificada por sua média $\mu$ e sua variância $\sigma$;
2. é óbvio que, $f_X(x) \geq 0$, mas a demonstração que $\int_{-\infty}^\infty f_X(x)dx = 1$ requer técnicas de integração via coordenadas polares;
3. a operação definida por $Z = \frac{X - \mu}{\sigma}$ é denominada [**padronização**]{style='color:red;'} de $X$ e podemos mostrar que $Z \sim \text{N}(0,1)$, caso em que dizemos que $Z$ tem distribuição [**normal padrão**]{style='color:red;'}.

:::

:::

:::


## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

::: {.callout-caution}
## Observações

Se $X \sim \text{N}(\mu, \sigma^2)$, então:

::: incremental

1. a probabilidade intervalar $P(a < X \leq b)$ deveria ser obtida por
$${\textstyle P(a < X \leq b) = \int_a^b \frac{1}{\sqrt{2\pi\sigma^2}}e^{-\frac{(x-\mu)^2}{2\sigma^2}} dx},$$
que não possui solução analítica, exceto se $a = -\infty$ e $b = \infty$;
2. poderíamos, a princípio, utilizar métodos numéricos para obtê-la, mas para cada $\mu$ e $\sigma^2$ diferentes precisaríamos executar o código novamente;
3. podemos utilizar a **padronização** para constatar que
$${\textstyle P(a < X \leq b) = P(\frac{a-\mu}{\sigma} < \frac{X-\mu}{\sigma} \leq \frac{b-\mu}{\sigma}) = P(\frac{a-\mu}{\sigma} < Z \leq \frac{b-\mu}{\sigma})}.$$

:::

:::

## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 14:** Seja $X =$ "tempo de reação de um motorista às luzes de freio do carro a frente". Um artigo na *Ergonomics* (1993, p. 391-395) sugere que $X \sim \text{N}(1.25, 0.46^2)$. [Determinemos $P(1 \leq X \leq 1.75)$:
$$
\begin{align*}
P(1 \leq X \leq 1.75) &= {\textstyle P(\frac{1-\mu}{\sigma} \leq \frac{X-\mu}{\sigma} \leq \frac{1.75-\mu}{\sigma}) = P(\frac{1-1.25}{0.46} \leq Z \leq \frac{1.75-1.25}{0.46})}\\
&= {\textstyle P(\frac{1-1.25}{0.46} \leq Z \leq \frac{1.75-1.25}{0.46}) = P(-0.54 \leq Z \leq 1.09)}\\
&= {\textstyle P(Z \leq 1.09) - P(Z \leq -0.54) = \Phi(1.09) - \Phi(-0.54),}
\end{align*}
$$
em que $\Phi(z) = P(Z \leq z)$ é uma notação especial para representar a fda da normal padrão $Z$.]{.fragment}
::: 

::: fragment

::: {.callout-caution}
## Observações

::: incremental

1. Note que passamos de um problema de calcular as probabilidades com respeito a $X \sim \text{N}(\mu, \sigma^2)$, com $\mu$ e $\sigma^2$ quaisquer, para as probabilidades de uma **normal padrão** $Z \sim \text{N}(0,1)$;
2. As probabilidades para $Z \sim \text{N}(0,1)$ também não tem solução analítica, mas métodos numéricos foram utilizados para computar e tabelar $\Phi(z)$ para diversos valores de $z$.

:::

:::

:::

## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}


::: {.cell layout-align="center"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-7-1.png){fig-align='center' width=768}
:::
:::


## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

<figure>
  <img src="figs/fig_normal_padrao1.png" style="display: block;margin-left: auto;margin-right: auto;width: 70%;">
</figure>

## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

<figure>
  <img src="figs/fig_normal_padrao2.png" style="display: block;margin-left: auto;margin-right: auto;width: 70%;">
</figure>


## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

<figure>
  <img src="figs/fig_normal_padrao3.png" style="display: block;margin-left: auto;margin-right: auto;width: 70%;">
</figure>

## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}


::: {.cell layout-align="center"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-8-1.png){fig-align='center' width=768}
:::
:::


## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

<figure>
  <img src="figs/fig_normal_padrao2_1.png" style="display: block;margin-left: auto;margin-right: auto;width: 70%;">
</figure>

## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

<figure>
  <img src="figs/fig_normal_padrao2_2.png" style="display: block;margin-left: auto;margin-right: auto;width: 70%;">
</figure>


## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

<figure>
  <img src="figs/fig_normal_padrao2_3.png" style="display: block;margin-left: auto;margin-right: auto;width: 70%;">
</figure>

## {.unnumbered .unlisted .smaller}

### Exemplo 14 (cont.) {.unnumbered .unlisted}

Vimos que $P(1 \leq X \leq 1.75) = P(-0.54 \leq Z \leq 1.09) = \Phi(1.09) - \Phi(-0.54)$. [Consultando a tabela da normal padrão, temos]{.fragment fragment-intex=1}

::: columns

::: {.column #vcenter width=50%}

::: {.fragment fragment-intex=2}

<figure>
  <img src="figs/figura_normal_padrao_ex14_1.png" style="display: block;margin-left: auto;margin-right: auto;width: 95%;">
  <figcaption style='text-align:center'>$\Phi(-0.54) = 0.2946$</figcaption>
</figure>

:::

:::

::: {.column #vcenter width=50%}

::: {.fragment fragment-intex=3}

<figure>
  <img src="figs/figura_normal_padrao_ex14_2.png" style="display: block;margin-left: auto;margin-right: auto;width: 95%;">
  <figcaption style='text-align:center'>$\Phi(1.09) = 0.8621$</figcaption>
</figure>

:::

:::

:::

[Assim,
$$P(1 \leq X \leq 1.75) = P(-0.54 \leq Z \leq 1.09) = \Phi(1.09) - \Phi(-0.54) = 0.8621 - 0.2946 = 0.5675.$$]{.fragment fragment-intex=4}


## {.unnumbered .unlisted .smaller}

### Exemplo 14 (cont.) {.unnumbered .unlisted}

Suponha que desejamos $P(X > 1.75)$. [Utilizando a padronização, temos
$${\textstyle P(X > 1.75) = P(\frac{X-\mu}{\sigma} > \frac{1.75-1.25}{0.46}) = P(Z > 1.09) = 1 - P(Z \leq 1.09) = 1 - \Phi(1.09).}$$]{.fragment fragment-intex=1}

::: columns

::: {.column #vcenter width=60%}

::: {.fragment fragment-intex=2}

Consultando a tabela da normal padrão, temos

<figure>
  <img src="figs/figura_normal_padrao_ex14_2.png" style="display: block;margin-left: auto;margin-right: auto;width: 99%;">
  <figcaption style='text-align:center'>$\Phi(1.09) = 0.8621$</figcaption>
</figure>

:::

:::

::: {.column #vcenter width=40%}

::: {.fragment fragment-intex=3}

Logo,
$$\begin{align*}
P(X > 1.75) &= 1 - \Phi(1.09)\\
&= 1 - 0.8621\\
&= 0.1379.
\end{align*}$$

:::

:::

:::

## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

Muitas vezes, é necessário determinar o quantil de ordem $p$ da va $X$, denotado por $Q_{X,p}$, cuja definição é $P(X \leq Q_{X,p}) = p$. Vejas as Figuras abaixo.
:::

::: {style='visibility:hidden'}


::: {.cell layout-align="center"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-9-1.png){fig-align='center' width=768}
:::
:::


:::

## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

Muitas vezes, é necessário determinar o quantil de ordem $p$ da va $X$, denotado por $Q_{X,p}$, cuja definição é $P(X \leq Q_{X,p}) = p$. Vejas as Figuras abaixo.
:::



::: {.cell layout-align="center"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-10-1.png){fig-align='center' width=768}
:::
:::


## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

Muitas vezes, é necessário determinar o quantil de ordem $p$ da va $X$, denotado por $Q_{X,p}$, cuja definição é $P(X \leq Q_{X,p}) = p$. Vejas as Figuras abaixo.
:::



::: {.cell layout-align="center"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-11-1.png){fig-align='center' width=768}
:::
:::



## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

Muitas vezes, é necessário determinar o quantil de ordem $p$ da va $X$, denotado por $Q_{X,p}$, cuja definição é $P(X \leq Q_{X,p}) = p$. Vejas as Figuras abaixo.
:::



::: {.cell layout-align="center"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-12-1.png){fig-align='center' width=768}
:::
:::


## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 14 (cont.):** Suponha que desejamos encontrar o valor que corresponde ao tempo de reação dos $70\%$ motoristas que reagem mais rapidamente. Na verdade, estamos interessados no quantil de ordem $p=0.7$, isto é, $Q_{X,0.7}$. Para encontrarmos, note que
$${\textstyle 0.7 = P(X \leq Q_{X,0.7}) = P(\frac{X - \mu}{\sigma} \leq \frac{Q_{X,0.7} - \mu}{\sigma})} = P(Z \leq Q_{Z,0.7}),$$
em que $Q_{Z,0.7} = \frac{Q_{X,0.7} - \mu}{\sigma} = \frac{Q_{X,0.7} - 1.25}{0.46}$, ou ainda, $Q_{X,0.7} = 1.25 + 0.46 Q_{Z,0.7}$.

:::

::: {.callout-caution}
## Observação

Note que, novamente, o problema passa do quantil de uma normal qualquer para o quantil de uma normal padrão. Para encontrar $Q_{Z,0.7}$, necessitamos consultar a tabela normal padrão de maneira inversa.

:::

## {.unnumbered .unlisted .smaller}

### Exemplo 14 (cont.) {.unnumbered .unlisted}

<figure>
  <img src="figs/figura_normal_padrao_ex14_2_1.png" style="display: block;margin-left: auto;margin-right: auto;width: 80%;">
</figure>

## {.unnumbered .unlisted .smaller}

### Exemplo 14 (cont.) {.unnumbered .unlisted}

<figure>
  <img src="figs/figura_normal_padrao_ex14_2_2.png" style="display: block;margin-left: auto;margin-right: auto;width: 80%;">
</figure>

## {.unnumbered .unlisted .smaller}

### Exemplo 14 (cont.) {.unnumbered .unlisted}

<figure>
  <img src="figs/figura_normal_padrao_ex14_2_3.png" style="display: block;margin-left: auto;margin-right: auto;width: 80%;">
</figure>

[Assim, concluímos que $0.52 < Q_{Z,0.7} < 0.53$. Podemos usar interpolação para aproximar $Q_{Z, 0.7}$.]{.fragment fragment-index=1} [Note que $Q_{Z,0.6985} = 0.52$ e $Q_{Z,0.7019} = 0.53$]{.fragment fragment-index=2}. [Agora, admitindo que $Q_{Z,p}$ tem uma relação aproximadamente linear para $0.6985 \leq p \leq 0.7019$, temos que $Q_{Z,p} = a+bp$, com as restrições]{.fragment fragment-index=3}

:::{.fragment fragment-index=3}

<table>
  <tr style="border-bottom:none;text-align:center;">
    <td>$0.52 = a+0.6985b$</td> <td>([**Eq. 1**]{style='color:red;'})</td> <td></td> <td></td> <td>e</td> <td></td> <td></td> <td>$0.53 = a+0.7019b$.</td> <td>([**Eq. 2**]{style='color:red;'})</td>
  </tr>
</table>

:::

[Pela 1ª equação, $a = 0.52 - 0.6985b$.]{.fragment fragment-index=4} [Substituindo na 2ª equação, vem $b = \frac{0.53 - 0.52}{0.7019 - 0.6985} \approx 2.9412$.]{.fragment fragment-index=5} [Retornando na 1ª equação, temos $a = 0.52 - 0.6985\cdot 2.9412 \approx -1.5344$.]{.fragment fragment-index=6} [Finalmente, temos
$$Q_{Z,0.7} = a+0.7b = -1.5344 + 0.7 \cdot 2.9412 \approx 0.5244 \color{white}{\Rightarrow Q_{X,0.7} = 1.25 + 0.46 Q_{Z,0.7} = 1.4912.}$$]{.fragment fragment-index=7}


## {.unnumbered .unlisted .smaller}

### Exemplo 14 (cont.) {.unnumbered .unlisted}

<figure>
  <img src="figs/figura_normal_padrao_ex14_2_3.png" style="display: block;margin-left: auto;margin-right: auto;width: 80%;">
</figure>

Assim, concluímos que $0.52 < Q_{Z,0.7} < 0.53$. Podemos usar interpolação para aproximar $Q_{Z, 0.7}$. Note que $Q_{Z,0.6985} = 0.52$ e $Q_{Z,0.7019} = 0.53$. Agora, admitindo que $Q_{Z,p}$ tem uma relação aproximadamente linear para $0.6985 \leq p \leq 0.7019$, temos que $Q_{Z,p} = a+bp$, com as restrições

<table>
  <tr style="border-bottom:none;text-align:center;">
    <td>$0.52 = a+0.6985b$</td> <td>([**Eq. 1**]{style='color:red;'})</td> <td></td> <td></td> <td>e</td> <td></td> <td></td> <td>$0.53 = a+0.7019b$.</td> <td>([**Eq. 2**]{style='color:red;'})</td>
  </tr>
</table>

Pela 1ª equação, $a = 0.52 - 0.6985b$. Substituindo na 2ª equação, vem $b = \frac{0.53 - 0.52}{0.7019 - 0.6985} \approx 2.9412$. Retornando na 1ª equação, temos $a = 0.52 - 0.6985\cdot 2.9412 \approx -1.5344$. Finalmente, temos
$$Q_{Z,0.7} = a+0.7b = -1.5344 + 0.7 \cdot 2.9412 \approx 0.5244 \color{red}{\Rightarrow Q_{X,0.7} = 1.25 + 0.46 Q_{Z,0.7} = 1.4912.}$$ 
**Conclusão:** 70% dos motoristas apresentam tempo de reação inferior a 1,4912 seg.


## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

::: {.callout-warning}
## Propriedades

De modo geral, podemos encontrar o quantil $Q_{Z,p}$ de uma normal padrão por interpolação da seguinte forma. Sejam $p_L$ e $p_U$, respectivamente, a maior e a menor probabilidades tabeladas tais que $p_L < p < p_U$ e $Q_{Z,p_L}$ e $Q_{Z,p_U}$ os respectivos quantis, então
$$Q_{Z,p} \approx a + bp,$$
em que
<table>
  <tr style="border-bottom:none;text-align:center;">
    <td>$b = \frac{p_U - p_L}{Q_{Z,p_U} - Q_{Z,p_L}}$</td> <td>e</td> <td>$a = p_L - bQ_{Z,p_L}$.</td>
  </tr>
</table>

:::

::: fragment

::: {.callout-caution}
## Observação

No Exemplo 14, obtivemos $P_L = 0.52$, $P_U = 0.7019$, $Q_{Z,p_L} = 0.6985$ e $Q_{Z,p_U} = 0.7019$.
:::

:::

## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

::: {.callout-caution}
## Observações

::: incremental

1. Em inferência, veremos um dos teoremas mais importantes para utilização em aplicações, o **Teorema Central do Limite** (TCL). Basicamente, o TCL afirma que, em grandes amostras, a média amostral tem distribuição aproximadamente normal.
2. Como a média amostral é soma de va's dividida pelo tamanho da amostra, é natural, imaginar que, se uma va $X$ pode ser enxergada como soma de várias va's, então a sua distribuição também será bem aproximada por uma normal. Esse é o caso da distribuição Binomial (soma de Bernoulli's), por exemplo.

:::

:::

::: fragment

::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo 15:** Dos motoristas de um estado, 25% não têm seguro. Seja $X =$ "quantidade sem seguro numa amostra de tamanho 50". [Se $s =$ "motorista não ter seguro", então $X \sim \text{Bin}(n = 50, p = 0.25)$.]{.fragment} [Vamos determinar a probabilidade de 20% ou menos da amostra não ter seguro:]{.fragment} [
$$\textstyle P(\frac{X}{n} \leq 0.2) = P(X \leq 10) = \sum_{x=0}^{10} p_X(x) = \sum_{x=0}^{10} {50 \choose x} 0.25^x0.75^{50-x} \approx 0.2622.$$]{.fragment}

:::

:::

## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

::: {.callout-caution}
## Observações

::: incremental

1. Note que, no Exemplo 15, o cálculo do valor exato de $P(X \leq 10)$ envolveu o cálculo de 11 probabilidades da distribuição binomial, o que pode ser exaustivo se realizado sem auxílio computacional;
2. A alternativa que surge é utilizar $Y \sim \text{N}(\mu, \sigma^2)$ como aproximação para $X \sim \text{Bin}(n,p)$;
3. Os parâmetros $\mu$ e $\sigma^2$ da distribuição de $Y$ utilizada para a aproximação são $\mu = \mu_X = np$ e $\sigma^2 = np(1-p)$, que são a média e a variância da $X \sim \text{Bin}(n,p)$;
4. Tendo em vista que $X$ pode ser representada como soma de $n$ va's $\text{Ber}(p)$, o TCL garante que a aproximação do Item 2 fica melhor a medida que $n$ aumenta;
5. Para ilustração, os gráficos a seguir mostram a fmp de $X \sim \text{Bin}(n,p)$ com a fdp de $Y \sim \text{N}(\mu = np, \sigma^2 = np(1-p))$, para $p=0.05$ e $0.25$, e $n = 5, 10, 50$ e $100$.

:::

:::

## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}



::: {.cell layout-ncol="2"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-13-1.png){width=100%}
:::

::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-13-2.png){width=100%}
:::
:::


## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}


::: {.cell layout-ncol="2"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-14-1.png){width=100%}
:::

::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-14-2.png){width=100%}
:::
:::



## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}


::: {.cell layout-ncol="2"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-15-1.png){width=100%}
:::

::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-15-2.png){width=100%}
:::
:::


## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}


::: {.cell layout-ncol="2"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-16-1.png){width=100%}
:::

::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-16-2.png){width=100%}
:::
:::




## {.unnumbered .unlisted .smaller}

### Exemplo 15 (cont.) {.unnumbered .unlisted}

Nesse caso, temos $\mu_X = np = 50 \cdot 0.25 = 12.5$ e $\sigma_X^2 = np(1-p) = 50 \cdot 0.25 \cdot 0.75 = 9.375$. Vamos ilustrar a aproximação de $P(X \leq 10)$ por meio de $Y \sim \text{N}(12.5, 9.375)$. Veja a figura abaixo.


## {.unnumbered .unlisted .smaller}

### Exemplo 15 (cont.) {.unnumbered .unlisted}

Nesse caso, temos $\mu_X = np = 50 \cdot 0.25 = 12.5$ e $\sigma_X^2 = np(1-p) = 50 \cdot 0.25 \cdot 0.75 = 9.375$. Vamos ilustrar a aproximação de $P(X \leq 10)$ por meio de $Y \sim \text{N}(12.5, 9.375)$. Veja a figura abaixo.


::: {.cell layout-align="center"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-17-1.png){fig-align='center' width=1056}
:::
:::



## {.unnumbered .unlisted .smaller}

### Exemplo 15 (cont.) {.unnumbered .unlisted}

Nesse caso, temos $\mu_X = np = 50 \cdot 0.25 = 12.5$ e $\sigma_X^2 = np(1-p) = 50 \cdot 0.25 \cdot 0.75 = 9.375$. Vamos ilustrar a aproximação de $P(X \leq 10)$ por meio de $Y \sim \text{N}(12.5, 9.375)$. Veja a figura abaixo.


::: {.cell layout-align="center"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-18-1.png){fig-align='center' width=1056}
:::
:::


## {.unnumbered .unlisted .smaller}

### Exemplo 15 (cont.) {.unnumbered .unlisted}

Nesse caso, temos $\mu_X = np = 50 \cdot 0.25 = 12.5$ e $\sigma_X^2 = np(1-p) = 50 \cdot 0.25 \cdot 0.75 = 9.375$. Vamos ilustrar a aproximação de $P(X \leq 10)$ por meio de $Y \sim \text{N}(12.5, 9.375)$. Veja a figura abaixo.


::: {.cell layout-align="center"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-19-1.png){fig-align='center' width=1056}
:::
:::


## {.unnumbered .unlisted .smaller}

### Exemplo 15 (cont.) {.unnumbered .unlisted}

Assim, a ideia é realizar a aproximação
$$\textstyle P(X \leq 10) \approx P(Y \leq 10.5) = P(Z \leq \frac{10.5 - 12.5}{\sqrt{9.375}}) = P(Z \leq -0.65) = 0.2578.$$

<figure>
  <img src="figs/figura_normal_padrao_ex15_3.png" style="display: block;margin-left: auto;margin-right: auto;width: 80%;">
</figure>

## {.unnumbered .unlisted .smaller}

### Exemplo 15 (cont.) {.unnumbered .unlisted}

Nesse caso, temos $\mu_X = np = 50 \cdot 0.25 = 12.5$ e $\sigma_X^2 = np(1-p) = 50 \cdot 0.25 \cdot 0.75 = 9.375$. Vamos ilustrar a aproximação de $P(X \leq 10)$ por meio de $Y \sim \text{N}(12.5, 9.375)$. Veja a figura abaixo.


::: {.cell layout-align="center"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-20-1.png){fig-align='center' width=1056}
:::
:::


## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

::: {.callout-tip}
## Exercícios

Considerando as condições do Exemplo 15 e utilizando $Y \sim \text{N}(12.5, 9.375)$, aproxime as seguintes probabilidades:

1. $P(X < 10)$;
2. $P(X = 10)$;
3. $P(X > 10)$;
4. $P(X \geq 10)$.
:::

::: {.callout-caution}
## Observações

1. É possível notar que a va normal tem fdp simétrica em torno de $mu$ com formato de sino (a fdp $f_X(x)$ decresce conforme $x$ se afasta de $\mu$).
2. Em muitas situações práticas, a vac é positiva e possui assimetria. Uma família de fdp com essas características é a família **gama**.
:::

## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

::: {.callout-note}
## Definição

Dizemos que $X$ tem distribuição Gama com parâmetros $\alpha$ e $\beta$, se sua fdp é dada por
$$\textstyle f_X(x) = \frac{1}{\beta^\alpha\Gamma(\alpha)}x^{\alpha - 1}e^{-x/\beta}, \ \ \ \ x > 0, \ \ \ \ \alpha,\beta > 0,$$
em que $\Gamma(\alpha) = \int_0^\infty z^{\alpha-1}e^{-z}dz$ é a função gama. Nesse caso, utilizamos a notação $X \sim \text{Gama}(\alpha, \beta)$.
:::

::: fragment

::: {.callout-warning}
## Propriedades

A função gama possui as seguintes propriedades:

::: incremental

1. Para qualquer $\alpha > 1$, $\Gamma(\alpha) = (\alpha - 1)\Gamma(\alpha - 1)$;
2. Se $n \in \mathbb{N}$, então $\Gamma(n) = (n-1)!$;
3. $\Gamma(\frac{1}{2}) = \pi$.

:::

:::

:::

## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}


::: {.cell layout-align="center"}
::: {.cell-output-display}
![](variaveis-aleatorias_files/figure-revealjs/unnamed-chunk-21-1.png){fig-align='center' width=768}
:::
:::



## 3.2 Modelos probabilísticos contínuos {.unnumbered .unlisted}

::: {.callout-warning}
## Propriedades

Se $X \sim \text{Gama}(\alpha, \beta)$, então
<table>
  <tr style="border-bottom:none;text-align:center;">
    <td>$E(X) = \alpha\beta$</td> <td>e</td> <td>$V(X) = \alpha\beta^2.$</td>
  </tr>
</table>

:::

# Vetores Aleatórios Bidimensionais

## Covariância e Correlação

# Funções de Variáveis Aleatórias

# FIM {.unnumbered .unlisted}

# APAGAR DPS 1 {.unnumbered .unlisted}

::: {.callout-caution}
## Observação

:::

::: {.callout-note}
## Definição

:::

::: {.callout-warning}
## Propriedades

:::

::: {.callout-tip}
## Exercícios

:::

::: {.callout-important}
## Problema

:::


::: {style="border-style: solid; border-width: 3px; padding-bottom: 0px; padding-right: 12px; padding-left: 12px; font-size:70%;"}

**Exemplo:** 

::: 

# APAGAR DPS 2 {.unnumbered .unlisted}

::: columns

::: {.column #vcenter width=45%}
1
:::

::: {.column #vcenter width=55%}
2

3

4
:::

:::




```{=latex}
\begin{align*}
\Omega &= \{(1,1), (1,2), \ldots, (4,4)\}\\
       &= \{(x,y) : x,y = 1,\ldots,4\}.
\end{align*}
```



# FIM {.unnumbered .unlisted}

