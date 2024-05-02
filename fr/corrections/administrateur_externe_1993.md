---
layout: default
description: Annale 1993 - Concours externe d'administrateur de l'Insee
title: Benjamin GILBERT - Corrections
lang: "fr"
katex: True
---

<h2 style="font-weight: normal; margin-bottom: 10px"><em>Concours externe d'administrateur de l'Insee</em></h2>
<h1 style="margin-top: 0">Annale de l'épreuve de mathématiques — 1993</h1>

---

<p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px 0px;">
Les propositions de corrections présentées ci-dessous n'engagent que l'auteur de ce site.
</p>

---

## Problème 1

Dans tout le problème $$x$$ désigne un réel _strictement positif_, et $$n$$ un entier naturel.

### Partie 1

<ol type="1" start="1">
    <li>
        <ol type="a" start="1">
            <li>
                Calculer l'intégrale \(\int_{0}^{+\infty} e^{-t} \mathrm{d}t\).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    En évaluant directement l'intégrale, on a :
                    $$
                    \int_{0}^{+\infty} e^{-t} \mathrm{d} t = \lim_{b \rightarrow +\infty} \int_{0}^{b} e^{-t} \mathrm{d}t = \lim_{b \rightarrow +\infty} \left[ -e^{-t} \right]_{0}^{b} = \lim_{b \rightarrow +\infty} -e^{-b} - \left( -e^{-0} \right) = 1.
                    $$
                </p>
            </li>
            <li> 
                On pose :
                $$
                F_n(x) = \int_{x}^{+\infty} \frac{e^{-t}}{t^{n+1}} \mathrm{d}t
                $$
                Montrer que \(F_n(x)\) converge pour tout \( n\in\mathbb{N} \) et \( x>0 \) et vérifie :
                $$
                0 < F_n(x) < \frac{e^{-x}}{x^{n+1}}
                $$
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    On commence par montrer par majoration que \(F_n(x)\) converge pour tout \( n\in\mathbb{N} \) et \( x>0 \).
                    <br><br>
                    On note que pour tout \(n \in \mathbb{N}\), on a :
                    $$
                    F_n(x) = \int_{x}^{+\infty} \frac{e^{-t}}{t^{n+1}} \mathrm{d}t \leq \int_{x}^{+\infty} \frac{e^{-t}}{x^{n+1}} \mathrm{d}t = \frac{e^{-x}}{x^{n+1}} < +\infty.
                    $$
                    <br><br>
                    On montre ensuite que pour tout \( n\in\mathbb{N} \) et \( x>0 \) on a bien : \(0 < F_n(x) < \frac{e^{-x}}{x^{n+1}}\).
                    fcghjklmù
                 </p>
            </li>
        </ol>
    </li>
</ol> 

---

## Problème 2

### Partie 1
