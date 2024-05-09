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
                    Dans la suite, on définit \( f : t \mapsto \frac{e^{-t}}{t^{n+1}} \). Il est clair qu'on a pour tout \( n\in\mathbb{N} \) et \( t>x>0 \) :
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
                    Par le théorème fondamental de l'analyse, en utilisant le résultat de convergence montré à la question précédente, on a pour tout \(n \in \mathbb{N} \) et pour tout \( x \in \left] 0, +\infty \right[ \) :
                    $$
                    F'_n(x) = \frac{\partial}{\partial x} F_n(x) = \frac{\partial}{\partial x} \int_{x}^{+\infty} f(t) \mathrm{d}t = - f(x) = - \frac{e^{-x}}{x^{n+1}}
                    $$
                    On en déduit que \( F_n \) est deux fois dérivable sur \( \left] 0, +\infty \right[ \) car \( F'_n \) est une composée de fonctions dérivables sur l'intervalle \( \left] 0, +\infty \right[ \).
                </p>
            </li>
        </ol>
    </li>
    <li> On pose \( f_0(x) = 0 \) et pour \( n \in \mathbb{N}^\star \) :
    $$
    f_n(x) = \sum_{k=1}^{n} (-1)^{k-1} \frac{(k-1)!}{x^k}.
    $$
        <ol type="a" start="1">
            <li>
                Etablir pour \( x >0 \) et \( n \in \mathbb{N} \) la relation de récurrence :
                $$
                F_n(x) = \frac{e^{-x}}{x^{n+1}} - (n+1)F_{n+1}(x)
                $$
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    En s'appuyant sur le résultat de convergence montré dans les questions précédentes, on obtient pour tout \( n \in \mathbb{N} \) en utilisant une intégration par parties :
                    $$
                    \begin{aligned}
                        \lim_{b \rightarrow +\infty} \int_{x}^{b} \frac{e^{-t}}{t^{n+1}} \mathrm{d}t & = \lim_{b \rightarrow +\infty} \left( \left[-\frac{e^{-t}}{t^{n+1}}\right]_{x}^{b}-\int_{x}^{b} \frac{(n+1) e^{-t}}{t^{n+2}} \mathrm{d}t \right) \\
                        & = \frac{e^{-x}}{x^{n+1}} - (n+1) \int_{x}^{+\infty} \frac{e^{-t}}{t^{n+2}} \mathrm{d}t
                    \end{aligned}
                    $$
                    On en déduit pour \( x >0 \) et \( n \in \mathbb{N} \) la relation de récurrence :
                    $$
                    F_n(x) = \frac{e^{-x}}{x^{n+1}} - (n+1)F_{n+1}(x)
                    $$
                </p>
            </li>
            <li>
                En déduire :
                $$
                e^{x} F_0(x) = f_n(x) + (-1)^n n! e^{x} F_n(x)
                $$
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    On établit la relation par récurrence sur \( n \in \mathbb{N} \).
                    <br><br>
                    <u>Initialisation</u>
                    <br><br>
                    Pour \( n=0 \), on a bien :
                    $$
                    e^{x} F_{0}(x) = f_{0}(x)+(-1)^{0} 0! e^{x} F_{0}(x) =e^{x} F_{0}(x)
                    $$
                    <br>
                    <u>Hérédité</u>
                    <br><br>
                    On suppose la relation de récurrence vraie au rang \( n \). On a alors :
                    $$
                    \begin{aligned}
                        e^{x} F_0(x) & = f_n(x) + (-1)^n n! e^{x} F_n(x) \\
                        & = f_{n}(x) + (-1)^{n} n! e^{x} \left( \frac{e^{-x}}{x^{n+1}} - (n+1)F_{n+1}(x) \right) \\
                        & = f_{n}(x) + \frac{(-1)^{n} n!}{x^{n+1}} + (-1)^{n+1}(n+1)!e^{x} F_{n+1}(x) \\
                        & = f_{n+1}(x)+(-1)^{n+1}(n+1)!e^{x} F_{n+1}(x)
                    \end{aligned}
                    $$
                    On en déduit qu'on a bien pour \( x >0 \) et \( n \in \mathbb{N} \) :
                    $$
                    e^{x} F_0(x) = f_n(x) + (-1)^n n! e^{x} F_n(x)
                    $$
                </p>
            </li>
        </ol>
    </li>
    <li>
        <ol type="a" start="1">
            <li>
                On pose \( \varphi(x) = e^x F_0(x) \). Montrer que :
                $$
                \lvert \varphi(x) - f_n(x) \rvert \leq \frac{n!}{x^{n+1}}
                $$
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    En utilisant la majoration trouvée précédemment, on a pour \( x >0 \) et \( n \in \mathbb{N} \) :
                    $$
                    \begin{aligned}
                        \lvert \varphi(x)-f_{n}(x) \rvert & = \lvert (-1)^{n} n! e^{x} F_{n}(x) \rvert \\
                        & \leq n! \lvert e^{x} \frac{e^{-x}}{x^{n+1}} \rvert \\
                        & = \frac{n!}{x^{n+1}}
                    \end{aligned}
                    $$
                </p>
            </li>
            <li>
                Déterminer les valeurs de \( n \) pour lesquelles \( \varepsilon_n = \frac{n!}{10^{n+1}} \) est minimal, et en déduire pour ces valeurs de \( n \) un majorant numérique de l'erreur conimise en prenant \( \ln(10) \) comme valeur approchée de \( \varphi(10) \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    On note que pour tout \( n \in \mathbb{N} : \varepsilon > 0 \) et qu'on a :
                    $$
                    \frac{\varepsilon_{n+1}}{\varepsilon_{n}} = \frac{(n+1)!}{10^{n+2}} \times \frac{10^{n+1}}{n!} = \frac{n+1}{10}
                    $$
                    On en déduit que la suite \( (\varepsilon_n )_{n\in\mathbb{N}} \) est décroissante jusqu'en \( n = 9 \), égale en \( n = 9 \) et \( n = 10 \) puis croissante à partir de \( n = 10 \).
                    <br><br>
                    Elle atteint donc son minimum en \( n = 9 \) et \( n = 10 \).
                    <br><br>
                    On en déduit directement, en utilisant la question précédente :
                    $$
                    \lvert \varphi(x)-f_{n}(x) \rvert \leq \frac{10!}{10^{11}} 
                    $$
                </p>
            </li>
        </ol>
    </li>
</ol> 

### Partie 2

<ol type="1" start="1">
    <li>
        <ol type="a" start="1">
            <li>
                Montrer pour tout \( n \in \mathbb{N} \) et tout \( x>0 \), la convergence de l'intégrale :
                $$
                G_n(x) = n! \int_{x}^{+\infty} \frac{e^{-t}(t-x)^n}{t^{n+1}} \mathrm{d}t.
                $$
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    On remarque que pour tout \( n\in\mathbb{N}, x>0 \) et \( t>x \) on a :
                    $$
                    0 \leq (t-x)^n \leq t^n
                    $$
                    En utilisant le résultat de la première partie, on en déduit :
                    $$
                    G_{n}(x) = n!\int_{x}^{+\infty} \frac{e^{-t}(t-x)^{n}}{t^{n+1}} \mathrm{d}t \leq n! \int_{x}^{+\infty} \frac{e^{-t}}{t} \mathrm{d}t < +\infty
                    $$
                </p>
            </li>
            <li>
                Exprimer la fonction \( G_n \) comme combinaison linéaire des fonctions \( x \mapsto x^p F_p(x) \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                Établir que la fonction \( G_n(x) \) est deux fois dérivable sur \( \left] 0, +\infty \right[ \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                Justifier que pour \( n\geq 1 \), on a \( \sum_{p=0}^n (-1)^p C_n^p = 0 \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                Pour \( n\geq 1 \) et \( x > 0 \), montrer que :
                $$
                G_n'(x) = -n n! \int_{x}^{+\infty} \frac{e^{-t}(t-x)^{n-1}}{t^{n+1}} \mathrm{d}t.
                $$
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
        </ol>
    </li>
    <li>
        <ol type="a" start="1">
            <li>
                Montrer que pour \( n \geq 1 \) et \( x > 0 \) :
                $$
                xG_n'(x) = n G_n(x) - n^2 G_{n-1}(x).
                $$
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                À l'aide d'une intégration par partie qu'on justifiera de \( \int_{x}^{+\infty} \frac{e^{-t (t-x)^{n-1}}}{t^n} \mathrm{d}t \), montrer que pour \( n \geq 1 \) et \( x > 0 \) on a :
                $$
                G_n'(x) = n G_{n-1}(x) + n G_{n-1}'(x).
                $$
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                En utilisant les résultats précédents, établir que pour \( n\geq 1 \) et \( x > 0 \) :
                $$
                G_{n+1}(x) = (x+2n+1) G_n(x) - n^2 G_{n-1}(x).
                $$
                 <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                En utilisant les résultats précédents, montrer que pour \( n\geq 1 \) et \( x > 0 \) on a :
                $$
                x G_n''(x) + (x+1) G_n'(x) - nG_n(x) = 0.
                $$
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
        </ol>
    </li>
</ol> 

### Partie 3

<ol type="1" start="1">
    <li>
        <ol type="a" start="1">
            <li>
                ..
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                ..
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                ..
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
        </ol>
    </li>
    <li>
        <ol type="a" start="1">
            <li>
                ..
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                ..
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
        </ol>
    </li>
    <li>
        <ol type="a" start="1">
            <li>
                ..
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
