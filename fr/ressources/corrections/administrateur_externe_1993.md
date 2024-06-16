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

<p>
Dans tout le problème \( x \) désigne un réel <i>strictement positif</i>, et \( n \) un entier naturel.
</p>

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
                    On utilise une intégration par parties.
                    <br><br>
                    Pour ce faire, on s'appuie sur le résultat de convergence montré dans les questions précédentes et on note que :
                    <br><br>
                    • &nbsp; la fonction \( t \mapsto e^{-t} \) est de classe \( \mathcal{C}^1 \) sur \( \mathbb{R}_{+}^{*} \)
                    <br><br>
                    • &nbsp; pour tout \( n \in \mathbb{N} \), la fonction \( t \mapsto \frac{1}{t^{n+1}} \) est de classe \( \mathcal{C}^1 \) sur \( \mathbb{R}_{+}^{*} \)
                    <br><br>
                    • &nbsp; \( \lim_{t \rightarrow +\infty} \frac{e^{-t}}{t^{n+1}} = 0 \)
                    <br><br>
                    On obtient ainsi pour tout \( n \in \mathbb{N} \) :
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
                    \lvert \varphi(x)-f_{n}(x) \rvert \leq \frac{9!}{10^{10}} 
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
                    On rappelle que, par la formule du binôme de Newton, pour tout \( n \in \mathbb{N}, x>0 \) et \( t \geq x \) on a :
                    $$
                    (t-x)^{n} = \sum_{k=0}^{n} \binom{n}{k} t^{k} (-x)^{n-k}
                    $$
                    <br>
                    Avec un changement de variables, on peut alons écrire pour tout \( n \in \mathbb{N}, x>0 \) :
                    $$
                    \begin{aligned}
                        G_{n}(x) & = n! \int_{x}^{+\infty} \sum_{k=0}^{n} \binom{n}{k} t^{k} (-x)^{n-k} \frac{e^{-t}}{t^{n+1}} \mathrm{d}t \\
                        & = n! \sum_{k=0}^{n} \binom{n}{k} (-x)^{n-k} \int_{x}^{+\infty} \frac{e^{-t}}{t^{n+1-k}} \mathrm{d}t \\
                        & = n! \sum_{k=0}^{n} \binom{n}{k} (-x)^{n-k} F_{n-k}(x) \\
                        & = \sum_{p=0}^{n} \left[ n! \binom{n}{p} (-1)^{p} \right] x^{p} F_{p}(x)
                    \end{aligned}
                    $$
                    <br>
                    On en déduit que \( G_n \) peut s'écrire comme une combinaison linéaire des fonctions \( x \mapsto x^p F_p(x) \).
                </p>
            </li>
            <li>
                Établir que la fonction \( G_n(x) \) est deux fois dérivable sur \( \left] 0, +\infty \right[ \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    En s'appuyant sur les résultats de la partie précédente, la fonction \( G_n(x) \) est deux fois dérivables sur \( \left] 0, +\infty \right[ \) pour tout \( n\in \mathbb{N} \) en tant que combinaison linéaire de fonctions elles-mêmes deux fois dérivables sur \( \left] 0, +\infty \right[ \).
                </p>
            </li>
            <li>
                Justifier que pour \( n\geq 1 \), on a \( \sum_{p=0}^n (-1)^p \binom{n, p} = 0 \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    Par la formule du binôme de Newton, on a :
                    $$
                    \sum_{p=0}^{n} (-1)^{p} C_{n}^{p} = \sum_{p=0}^{n} \binom{n}{p} (-1)^{p} (1)^{n-p} = (-1+1)^{n} = 0
                    $$
                </p>
            </li>
            <li>
                Pour \( n\geq 1 \) et \( x > 0 \), montrer que :
                $$
                G_n'(x) = -n n! \int_{x}^{+\infty} \frac{e^{-t}(t-x)^{n-1}}{t^{n+1}} \mathrm{d}t.
                $$
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    En utilisant les résultats de la partie précédente, on a :
                    $$
                    \begin{aligned}
                        G_{n}'(x) & = n! \sum_{p=0}^{n} \binom{n}{p} (-1)^{p} \left( p x^{p-1} F_{p}(x) - x^{p} F_{p}'(x) \right) \\
                        & = n! \sum_{p=0}^{n} p \binom{n}{p} (-1)^{p} x^{p-1} F_{p}(x) + n! \frac{e^{-x}}{x} \sum_{p=0}^{n} \binom{n}{p} (-1)^{p} \\
                        & = n! \sum_{p=0}^{n} p \binom{n}{p} (-1)^{p} x^{p-1} \int_{x}^{+\infty} \frac{e^{-t}}{t^{p+1}} \mathrm{d}t + 0 \\
                        & = n! \int_{x}^{+\infty} e^{-t} \sum_{p=0}^{n} p\binom{n}{p} (-1)^{p} x^{p-1} t^{p-1} \mathrm{d}t \\
                        & = -n n! \int_{x}^{+\infty} \frac{e^{-t} \sum_{p=1}^{n} \binom{n-1}{p-1} (-x)^{p-1} t^{(n-1)-(p-1)}}{t^{n+1}} \mathrm{d}t \\
                        & = -n n! \int_{x}^{+\infty} \frac{e^{-t}(t-x)^{n-1}}{t^{n+1}} d t
                    \end{aligned}
                    $$
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
                    En utilisant les résultats précédents, on a pour tout \( n \geq 1 \) et pour tout \( x > 0 \) :
                    $$
                    \begin{aligned}
                        x G_n'(x) & = -x n n! \int_{x}^{+\infty} \frac{e^{-t}(t-x)^{n-1}}{t^{n+1}} \mathrm{d}t \\
                        & = n \left( n! \int_{x}^{+\infty} \frac{e^{-t}(t-x)^{n-1}(t-x-t)}{t^{n+1}} \mathrm{d}t \right) \\
                        & = n n! \left( \int_{x}^{+\infty} \frac{e^{-t}(t-x)^{n}}{t^{n+1}} \mathrm{d}t - \int_{x}^{+\infty} \frac{e^{-t}(t-x)^{n-1}}{t^{n}} \mathrm{d}t \right) \\
                        & = n n! \left( G_{n}(x) - n G_{n-1}(x) \right) \\
                        & = n G_{n}(x)-n^{2} G_{n-1}(x)
                    \end{aligned}
                    $$
                </p>
            </li>
            <li>
                À l'aide d'une intégration par partie — qu'on justifiera — de \( \int_{x}^{+\infty} \frac{e^{-t (t-x)^{n-1}}}{t^n} \mathrm{d}t \), montrer que pour \( n \geq 1 \) et \( x > 0 \) on a :
                $$
                G_n'(x) = n G_{n-1}(x) + n G_{n-1}'(x).
                $$
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    On utilise une intégration par parties.
                    <br><br>
                    Pour ce faire, on note que :
                    <br><br>
                    • &nbsp; la fonction \( t \mapsto e^{-t} \) est de classe \( \mathcal{C}^1 \) sur \( \mathbb{R}_{+}^{*} \)
                    <br><br>
                    • &nbsp; pour tout \( n \geq 1 \) et tout \( x > 0 \), la fonction \( t \mapsto \frac{(t-x)^{n-1}}{t^{n+1}} \) est de classe \( \mathcal{C}^1 \) sur \( \mathbb{R}_{+}^{*} \)
                    <br><br>
                    • &nbsp; \( \lim_{t \rightarrow +\infty } \frac{e^{-t}(t-x)^{n-1}}{t^{n+1}} = 0 \)
                    <br><br>
                    On obtient ainsi pour tout \( n \geq 1 \) et \( x > 0 \) :
                    $$
                    \begin{aligned}
                        \frac{G_{n-1}(x)}{(n-1)!} & = \lim_{b\rightarrow +\infty} \int_{x}^{b} \frac{e^{-t}(t-x)^{n-1}}{t^{n}} \mathrm{d}t \\
                        & = \lim_{b\rightarrow +\infty} \left( \left[-\frac{e^{-t}(t-x)^{n-1}}{t^{n}}\right]_{x}^{b} + \int_{x}^{b} e^{-t}\frac{\partial}{\partial t} \left( \frac{(t-x)^{n-1}}{t^{n}} \right) \right) \\
                        & = \lim_{b\rightarrow +\infty} \int_{x}^{b} e^{-t}\left(\frac{(n-1)(t-x)^{n-2}}{t^{n}}-\frac{n(t-x)^{n-1}}{t^{n+1}}\right) \mathrm{d}t \\
                        & = (n-1) \int_{x}^{+\infty} \frac{e^{-t}(t-x)^{n-2}}{t^{n}} \mathrm{d}t - n \int_{x}^{+\infty} \frac{e^{-t}(t-x)^{n-1}}{t^{n+1}} \mathrm{d}t
                    \end{aligned}
                    $$
                    On en déduit alors en multipliant par \( (n-1)! \) :
                    $$
                    G_{n-1}(x) = -G_{n-1}'(x) + \frac{1}{n} G_n'(x)
                    $$
                    En réarrangeant les termes de l'équation, on obtient :
                    $$
                    G_n'(x) = n G_{n-1}(x) + n G_{n-1}'(x)
                    $$
                </p>
            </li>
            <li>
                En utilisant les résultats précédents, établir que pour \( n\geq 1 \) et \( x > 0 \) :
                $$
                G_{n+1}(x) = (x+2n+1) G_n(x) - n^2 G_{n-1}(x).
                $$
                 <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    En utilisant les résultats précédents, on a pour \( n\geq 1 \) et \( x > 0 \) :
                    $$
                    x G_{n+1}'(x) = x (n+1) G_{n}(x) + x(n+1) G_{n}'(x)
                    $$
                    Or, on a aussi pour \( n\geq 1 \) et \( x > 0 \) :
                    $$
                    x G_{n+1}'(x) = (n+1) G_{n+1}(x) - (n+1)^{2} G_{n}(x)
                    $$
                    En combinant ces deux égalités, on obtient :
                    $$
                    x (n+1) G_{n}(x) + x(n+1) G_{n}'(x) = (n+1) G_{n+1}(x) - (n+1)^{2} G_{n}(x)
                    $$
                    En réarrangeant les termes, on obtient :
                    $$
                    G_{n+1}(x) = x G_{n}(x) + x G_{n}'(x) + (n+1) G_{n}(x)
                    $$
                    En substituant la relation mise en évidence à la question <b>2. a.</b> dans l'équation, on obtient :
                    $$
                    G_{n+1}(x) = x G_{n}(x) + \left( n G_n(x) - n^2 G_{n-1}(x) \right) + (n+1) G_{n}(x)
                    $$
                    En réarrangeant les termes, on obtient finalement :
                    $$
                    G_{n+1}(x) = (x+2n+1) G_n(x) - n^2 G_{n-1}(x)
                    $$
                </p>
            </li>
            <li>
                En utilisant les résultats précédents, montrer que pour \( n\geq 1 \) et \( x > 0 \) on a :
                $$
                x G_n''(x) + (x+1) G_n'(x) - nG_n(x) = 0.
                $$
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    On note d'abord qu'on a pour tout \( n\geq 1 \) et \( x > 0 \), en combinant les résultats précédents :
                    $$
                    n G_{n}(x) = x G_n'(x) + n^{2} G_{n-1}(x) = x G_n'(x) + n \left( G_n'(x) - n G_{n-1}'(x)\right)
                    $$
                    Puis, en dérivant la relation mise en évidence à la question <b>2. a.</b>, on a pour tout \( n\geq 1 \) et \( x > 0 \) :
                    $$
                    G_{n}'(x) + x G_{n}^{\prime\prime}(x) = n G_n'(x) - n^2 G_{n-1}'(x)
                    $$
                    En insérant la deuxième équation dans la première, on obtient :
                    $$
                    n G_{n}(x) = x G_n'(x) + G_n'(x) + xG_n''(x)
                    $$
                    En réarrangeant les termes, on obtient :
                    $$
                    x G_n''(x) + (x+1) G_n'(x) - nG_n(x) = 0
                    $$
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
                Étant donné l'entier \( n\geq 1 \), on cherche à déterminer les réels \( \alpha_{n,0}, \alpha_{n,1}, ..., \alpha_{n,n-1},  \) pour que le polynôme \( P_n \) :
                $$
                P_n(x) = x^n + \alpha_{n,n-1} x^{n-1} + ... + \alpha_{n, 1}x + \alpha_{n,0}
                $$
                vérifie l'équation (dite <i>équation différentielle</i>) pour tout \( x>0 \) :
                $$
                P_n^{\prime\prime}(x) + (x+1) P_n'(x) - nP_n(x) = 0.
                $$
                <br>
                Montrer que pour \( p \in \{ 0, 1, ..., n-1 \} \) les \( \alpha_{n,p} \) doivent vérifier la relation de récurrence :
                $$
                (p+1)^2 \alpha_{n, p+1} = (n-p)\alpha_{n, p}
                $$
                où l'on a posé \( \alpha_{n, n} = 1 \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    En dérivant, on note qu'on a pour tout \(n \geq 1 \) et \( x > 0 \) :
                    $$
                    P_{n}'(x) = \sum_{p=1}^{n} \alpha_{n, p} p x^{p-1}
                    $$ 
                    De la même manière, on calcule la dérivée seconde : 
                    $$
                    P_{n}^{\prime\prime}(x) = \sum_{p=2}^{n} \alpha_{n, p} p (p-1) x^{p^{-2}}
                    $$
                    L'équation différentielle est donc vérifiée si et seulement si :
                    $$
                    \sum_{p=0}^{n} \alpha_{n, p} \left[x p(p-1) x^{p-2}+(x-1) p x^{p-1}-n x^{p}\right] = 0
                    $$
                    En développant et réarrangeant les termes de l'équation, on obtient :
                    $$
                    \sum_{p=0}^{n} \alpha_{n, p}p^{2} x^{p-1} + \sum_{p=0}^{n} \alpha_{n, p}(p-n) x^{p}=0
                    $$
                    Par un changement de variable dans la somme de gauche, on obtient :
                    $$
                    \sum_{q=0}^{n-1} \alpha_{n, q+1}(q+1)^{2} x^{q} + \sum_{p=0}^{n} \alpha_{n, p}(p-n) x^{p}=0
                    $$
                    On en déduit en rassemblant les termes :
                    $$
                    \sum_{p=0}^{n-1} \left( \alpha_{n, p+1}(p-1)^{2} + \alpha_{n, p}(p-n) \right) x^{p} = 0
                    $$
                    Or, on sait que les polynômes unitaires \( x^{0}, x, x^{1}, \ldots, x^{n} \) constituent une famille libre dans l'espace des polynômes de degré \( n \) \( \mathbb{R}_{n}[x] \). On en déduit que \(P_n\) vérifie l'équation différentielle si et seulement si :
                    $$
                    \forall p \in \{0, \ldots, n-1 \} : (p+1)^{2} \alpha_{n, p+1} = (n-p) \alpha_{n, p}
                    $$
                </p>
            </li>
            <li>
                En déduire que \( \alpha_{n, p} = \frac{n!}{p!} \binom{n}{p} \) puis que \( \alpha_{n, p} \) est entier.
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    En utilisant le résulat précédent, on peut écrire pour tout \( p \in \{ 0, ..., n-1\} \) :
                    $$
                    \alpha_{n, p} = \frac{(p+1)^{2}}{(n-p)} \alpha_{n, p+1}
                    $$
                    Par récurrence immédiate sur \( p \), en notant que \( \alpha_{n, n} = 1 \), on obtient :
                    $$
                    \alpha_{n, p} =\prod_{k=p}^{n} \frac{(k-1)^{2}}{(n-k)} =\frac{\left(\frac{n!}{p!}\right)^{2}}{(n-p)!} = \frac{n!}{p!} \frac{n!}{p!(n-p)!} = \frac{n!}{p!}\binom{n}{p}
                    $$
                    <br>
                    Puis, pour montrer que pour tout \( p \in \{ 0, ..., n\} \), \( \alpha_{n, p} \) est un entier naturel, on note que :
                    <br><br>
                    • &nbsp; pour tout \( n \geq 1, p \in \{ 0, ..., n\} \) : \( \frac{n!}{p!} \in \mathbb{N} \) comme produit de \( n - p \) entiers naturels ;
                    <br><br>
                    • &nbsp; pour tout \( n \geq 1, p \in \{ 0, ..., n \} \) : \( \binom{n}{p} \in \mathbb{N} \) par récurrence immédiate en utilisation le fait que \( \binom{0}{0} = 1 \) et \( \binom{1}{0} = 1 \) ainsi que la propriété du triangle de Pascal, donnée par :
                    $$ 
                    \binom{n}{p} = \binom{n-1}{p-1} + \binom{n-1}{p}
                    $$
                    On en déduit que \( \alpha_{n, p} \) est un produit naturel comme produit d'entiers naturels.
                </p>
            </li>
            <li>
                Expliciter les polynômes \( P_1, P_2 \) et \( P_3 \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    On obtient les polynômes suivants :
                    <br><br>
                    • &nbsp; pour tout \( x > 0 \) : \( P_{1}(x)=x+1 \)
                    <br><br>
                    • &nbsp; pour tout \( x > 0 \) : \( P_{2}(x)=x^{2}+4 x+2 \)
                    <br><br>
                    • &nbsp; pour tout \( x > 0 \) : \( P_{3}(x)=x^{3}+9 x^{2}+18 x+6 \)
                </p>
            </li>
        </ol>
    </li>
    <li>
        <ol type="a" start="1">
            <li>
                En utilisant les questions précédentes, montrer que pour \( n\in \mathbb{N}^\star \), il existe un unique polynôme \( Q_n \) tel que pour tout \( x > 0 \) on ait :
                $$
                G_n(x) = P_n(x) F_0(x) - Q_n(x) e^{-x}
                $$
                <br>
                Vérifier que \( Q_n(x) = \sum_{p=0}^n \alpha_{n, p} x^p f_p(x) \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    On sait par les questions précédentes que pour tout \( n \in \mathbb{N} \) et \( x>0 \) on a :
                    $$
                    e^{x} F_{0}(x) = f_{n}(x) + (-1)^{n} n! e^{x} F_{n}(x)
                    $$
                    On en déduit que :
                    $$
                    \begin{aligned}
                        G_{n}(x) & = n! \sum_{p=0}^{n} \binom{n}{p} (-1)^{p} x^{p} F_{p}(x) \\
                        & = n! \sum_{p=0}^{n} \binom{n}{p} (-1)^{p} x^{p}  \frac{e^{x} F_{0}(x)-f_{p}(x)}{(-1)^p p!} \\
                        & = \sum_{p=0}^{n} \alpha_{n, p} x^{p} \left( F_{0} - e^{-x} f_{p}(x) \right) \\
                        & = P_{n}(x) F_{0}(x) - e^{-x} Q_{n}(x)
                    \end{aligned}
                    $$
                </p>
            </li>
            <li>
                Expliciter les polynômes \( Q_1, Q_2 \) et \( Q_3 \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    On obtient les polynômes suivants :
                    <br><br>
                    • &nbsp; pour tout \( x > 0 \) : 
                    $$
                    \begin{aligned} Q_1(x) & = x f_{1}(x) + f_{0}(x)=1
                    \end{aligned}
                    $$
                    <br><br>
                    • &nbsp; pour tout \( x > 0 \) :
                    $$
                    \begin{aligned} Q_2(x) & = x^{2} f_{2}(x)+4 x f_{1}(x)+2 f_{0}(x) \\ & =x^{2}\left(\frac{1}{x}-\frac{1}{x^{2}}\right)+4 \\ & =x+3
                    \end{aligned}
                    $$
                    <br><br>
                    • &nbsp; pour tout \( x > 0 \) :
                    $$
                    \begin{aligned}
                    Q_3(x) & = x^{3} f_{3}(x)+9 x^{2} f_{2}(x)+18 x f_{1}(x)+6 f_{0}(x) \\ & =x^{3}\left(\frac{1}{x}-\frac{1}{x^{2}}+\frac{2}{x^{3}}\right)+9 x^{2}\left(\frac{1}{x}-\frac{1}{x^{2}}\right)+18 \\ & =x^{2}+8 x+11
                    \end{aligned}
                    $$
                </p>
            </li>
        </ol>
    </li>
    <li>
        <ol type="a" start="1">
            <li>
                Établir pour \( n\in \mathbb{N} \) et \( x > 0 \) l'inégalité :
                $$
                0 < G_n(x) < \frac{n! e^{-x}}{x}.
                $$
                <br><br>
                Puis, établir pour \( n\in \mathbb{N} \) et \( x > 0 \) l'inégalité :
                $$
                P_n(x) > n! n x.
                $$
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                Montrer que pour \( x > 0 \) fixé, on a \( \lim_{n \rightarrow +\infty} \frac{G_n(x)}{P_n(x)}e^x = 0 \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                En déduire pour \( x > 0 \) fixé \( \varphi(x) = \lim_{n \rightarrow +\infty} \frac{Q_n(x)}{P_n(x)} \).
                <br><br>
                Puis, calculer \( \frac{Q_3(10)}{P_3(10)} \) et en dédurie une valeur approchée de \( \varphi(10) \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
        </ol>
    </li>
</ol> 

---

## Problème 2

<p>
Dans tout le problème, \( n \) désigne un entier naturel, et \( \mathcal{M}_3(\mathbb{R}) \) l'espace vectoriel réel des matrices carrées d'ordre \( 3 \) à coefficients réels.
<br><br>
On note \( I \) la matrice de l'identité de \( \mathbb{R}_3 \) et \( M \) la matrice :
$$
M = \begin{pmatrix} -7 & 0 & -8 \\ 4 & 1 & 4 \\ 4 & 0 & 5 \end{pmatrix}.
$$
</p>

<ol type="1" start="1">
    <li>
        <ol type="a" start="1">
            <li>
                Calculer \( A = \frac{1}{4}(M - I) \) puis \( A^2 \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                Démontrer qu'il existe une suite \( (u_n)_{n\in\mathbb{N}} \) de nombres réels tels que :
                $$
                \forall n \in \mathbb{N} : M^n = I + u_n A
                $$
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                Calculer \( u_n \) en fonction de \( n \) et en déduire l'expression de \( M^n \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
        </ol>
    </li>
    <li>
        Soit \( J \) la matrice :
        $$
        J = \begin{pmatrix} -1 & 0 & -2 \\ 1 & 1 & 1 \\ 1 & 0 & 2 \end{pmatrix}.
        $$
        Calculer \( J^2 \) puis \( J^n \) et montrer que \( J \) n'est pas inversible.
        <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -30px;">
            ...
        </p>
    </li>
    <li>
        <p>
        On considère l'ensemble \( E = \{ aI + bJ, (a, b) \in \mathbb{R}^2 \} \subset \mathcal{M}_3(\mathbb{R}) \).
        </p>
        <ol type="a" start="1">
            <li>
                Montrer que \( E \) est stable par le produit de matrices. Montrer aussi que \( E \) est un espace vectoriel réel, en donner une base et préciser sa dimension.
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                Déterminer quels sont les éléments de \( E \) admettant un inverse dans \( E \), et préciser celui-ci.
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                Résoudre dans \( E \) les équations d'inconnue \( X \) suivantes :
                <br><br>
                • &nbsp; \( X^2 = I \),
                <br><br>
                • &nbsp; \( X^2 = X \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
        </ol>
    </li>
    <li>
        <ol type="a" start="1">
            <li>
                Montrer que \( M \in E \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                En déduire que \( M^n = [1 - (-3)^n]J + (-3)^n I \) et comparer avec le résultat obtenu à la première question.
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
        </ol>
    </li>
    <li>
        <p>
        Soit \(j\) l'endomorphisme de \(\mathbb{R}^3\) associé à \(J\) dans la base canonique de \(\mathbb{R}^3\).
        </p>
        <ol type="a" start="1">
            <li>
                Pour quelles valeurs de \(X\) le noyau de l'endomorphisme \(j - X I_{d}\) n'est-il pas réduit au vecteur nul ?
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                En déduire une base \(\mathcal{B}\) de \(\mathbb{R}^3\) dans laquelle la matrice de \(j\) soit égale à :
                $$
                J' = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{pmatrix}.
                $$
                <br>
                Déterminer la matrice de passage \(P\) de la base canonique à \(\mathcal{B}\).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                Donner dans la base \(\mathcal{B}\) la matrice \(N\) de l'endomorphisme \(f\) de matrice \(M\) dans la base canonique.
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                Déterminer la matrice de \(f^n = f \circ ... \circ f\) dans cette base.
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                Retrouver à nouveau l'expression de \( M^n \).
                <p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
        </ol>
    </li>
</ol> 

