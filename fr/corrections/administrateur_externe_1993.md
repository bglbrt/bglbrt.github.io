---
layout: default
description: Annale 1993 - Concours externe d'administrateur de l'Insee
title: Benjamin GILBERT - Corrections
lang: "fr"
katex: True
---

<h1 style="margin-bottom: 0">Annale de l'épreuve de mathématiques - 1993</h1>
<h3 style="font-weight: normal; margin-top: 10px">Concours externe d'administrateur de l'Insee</h3>

<p style="border: solid 2px; border-radius: 10px; background-color:rgba(121, 28, 248, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px 0px;">
Ces propositions de corrections n'engagent que leur auteur.
</p>

---

## Problème 1

Dans tout le problème $$x$$ désigne un réel _strictement positif_, et $$n$$ un entier naturel.

### Partie 1

<ol type="1">
    <li>
        <ol type="a">
            <li> Calculer l'intégrale \(\int_{0}^{+\infty} e^{-t} \mathrm{d}t\). </li>

<p style="border: solid 2px; border-radius: 10px; background-color:rgba(121, 28, 248, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; margin: 15px 0 15px -60px;">

En évaluant l'intégrale, on a :
$$
\begin{aligned}
    \int_{0}^{+\infty} e^{-t} \mathrm{d} t & = \lim_{b \rightarrow +\infty} \int_{0}^{b} e^{-t} \mathrm{d}t \\
    & = \lim_{b \rightarrow +\infty} \left[ -e^{-t} \right]_{0}^{b} \\
    & = \lim_{b \rightarrow +\infty} -e^{-b} - \left( -e^{-0} \right) \\
    & = 1
\end{aligned}
$$
</p>

            <li> 
            On pose :
            $$ F_n(x) = \int_{x}^{+\infty} \frac{e^{-t}}{t^{n+1}} \mathrm{d}t$$
            Montrer que \(F_n(x)\) converge pour tout \( n\in\mathbb{N} \) et \( x>0 \) et vérifie :
            $$0 < F_n(x) < \frac{e^{-x}}{x^{n+1}}$$
            </li>

<p style="border: solid 2px; border-radius: 10px; background-color:rgba(121, 28, 248, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; margin: 15px 0 15px -60px;">

On commence par montrer par majoration que \(F_n(x)\) converge pour tout \( n\in\mathbb{N} \) et \( x>0 \).\n

On note que pour tout \(n \in \mathbb{N}\), on a :
$$
\begin{aligned}
    F_n(x) & = \int_{x}^{+\infty} \frac{e^{-t}}{t^{n+1}} \mathrm{d}t \\
    & \leq \int_{x}^{+\infty} \frac{e^{-t}}{x^{n+1}} \mathrm{d}t \\
    & = \frac{1}{x^{n+1}} \int_{x}^{+\infty} e^{-t} \mathrm{d}t \\
    & = \frac{e^{-x}}{x^{n+1}} \\
    @ < +\infty
\end{aligned}
$$

On montre ensuite que pour tout \( n\in\mathbb{N} \) et \( x>0 \) on a \(0 < F_n(x) < \frac{e^{-x}}{x^{n+1}}\).

</p>

        </ol>
    </li>
</ol> 

---

## Problème 2

### Partie 1
