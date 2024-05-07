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
                    Dans la suite, on définit \( f : t \mapsto \frac{e^{-t}}{t^{n+1}} \). Il est clair qu'on a pour tout \( n\in\mathbb{N} \) et \( t>x \) :
                    $$
                    0 < f(t) < \frac{e^{-t}}{x^{n+1}}
                    $$
                    On en déduit qu'on a pour tout \( n\in\mathbb{N} \) et \( x>0 \) :
                    $$
                    0 < \int_{x}^{+\infty} f(t) \mathrm{d}t < \int_{x}^{+\infty} \frac{e^{-t}}{x^{n+1}} = \frac{1}{x^{n+1}} \int_{x}^{+\infty} e^{-t} \mathrm{d}t = \frac{e^{-x}}{x^{n+1}}
                    $$
                    Il s'ensuit que pour tout \( n\in\mathbb{N} \) et \( x>0 \) on a bien : \( 0 < F_n(x) < \frac{e^{-x}}{x^{n+1}} \).
                    <br><br>
                    Par encadrement, on en déduit que pour tout \( n\in\mathbb{N} \) et \( x>0 \) : \(F_n(x)\) converge.
                 </p>
            </li>
            <li>
                Montrer que pour tout \(n \in \mathbb{N} \), la fonction \( F_n \) est deux fois dérivable sur \( \left] 0, +\infty \right[ \) et calculer sa dérivée \( F'_n \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    Par le théorème fondamental de l'analyse, en utilisant le résultat de convergence montré précédemment, on a pour tout \(n \in \mathbb{N} \) et pour tout \( x \in \left] 0, +\infty \right[ \) :
                    $$
                    F'_n(x) = \frac{\partial F_n(x)}{\partial x} = \frac{\partial}{\partial x} \int_{x}^{+\infty} f(t) \mathrm{d}t = - f(x) = - \frac{e^{-x}}{x^{n+1}}
                    $$
                    <br><br>
                    On en déduit que \( F_n \) est deux fois dérivable sur \( \left] 0, +\infty \right[ \) car \( F'_n \) est la composée de fonctions dériavles sur cet intervalle.
                </p>
            </li>
        </li>
        <li>
            <li>
                ...
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                ...
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    En s'appuyant sur la convergence de \( F_n(x) \), on note qu'en utilisant une intégration par parties on a :
                    $$
                    \int_{x}^{+\infty} \frac{e^{-t}}{t^{n+1}} \mathrm{d}t = \lim_{b \rightarrow +\infty} \left[-\frac{e^{-t}}{t^{n+1}}\right]_{x}^{b}-\int_{x}^{b} \frac{(n+1) e^{-t}}{t^{n+2}} \mathrm{d}t
                     =\frac{e^{-x}}{x^{n+1}} - (n+1) \int_{x}^{+\infty} \frac{e^{-t}}{t^{n+2}} d t
                    $$
                </p>
            </li>
            <li>
                ...
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                ...
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
        </ol>
    </li>
</ol> 

---

## Problème 2

### Partie 1
