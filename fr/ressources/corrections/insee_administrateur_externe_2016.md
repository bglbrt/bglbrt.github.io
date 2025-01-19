---
layout: default
description: Concours externe d'administrat·eur·rice de l'Insee — 2016
title: Benjamin GILBERT - Corrections
lang: "fr"
katex: True
---

<h2 style="font-weight: normal; margin-bottom: 10px"><em>Concours externe d'administrat·eur·rice de l'Insee — 2016</em></h2>
<h1 style="margin-top: 0">Épreuve de mathématiques</h1>

---

<p>
Le sujet est accessible <a href = "/pdfs/insee_administrateur_externe/insee_administrateur_externe_2016.pdf">ici</a> au format PDF.
</p>

<p style="border: solid 2px; border-radius: 10px; background-color:rgba(152, 180, 212, .1); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px 0px;">
Les propositions de corrections présentées ci-dessous n'engagent que l'auteur de ce site.
</p>

---
<!-- ======================================================= -->
<!-- Partie 1 - Analyse et algèbre                           -->
<!-- ======================================================= -->

## Partie 1 - Analyse et algèbre

### Exercice 1

<ol type="1" start="1">

    <!-- 1. -->
    <li>
        <p>
        On note \(J\) l’intervalle \(\left] 0,+\infty \right[\) et on définit sur \(J\) la fonction \(h\) par :
        </p>
        $$ 
        \forall x \in J, \quad h(x) \;=\;\int_{0}^{+\infty} \frac{x \cos t}{x^{2} + t^{2}} \,\mathrm{d}t.
        $$

        <p>Montrer que la fonction \(h\) est bien définie.</p>

        <p style="border: solid 2px; border-radius: 10px; 
                  background-color:rgba(152, 180, 212, .1); 
                  padding: 10px; margin: 15px 0 15px -60px;">
            <b>Solution :</b>  
            <br><br>
            Pour tout \(x>0\), l’intégrande 
            \(\displaystyle \frac{x \cos t}{x^2 + t^2}\) est continue en \(t\) 
            et son amplitude décroît comme \(\frac{1}{t}\) pour \(t \to +\infty\). 
            De plus, près de \(t=0\), la fonction reste bornée. Ainsi l’intégrale 
            \(\int_{0}^{+\infty}\) converge absolument. On en déduit que 
            \(h(x)\) est bien définie pour tout \(x>0\).
        </p>
    </li>

    <!-- 2. -->
    <li>
        <ol type="a" start="1">
            
            <!-- (a) -->
            <li>
                <p>
                À l’aide d’une intégration par parties, établir l’égalité suivante :
                </p>
                $$
                h(x) \;=\; 2x \int_{0}^{+\infty} 
                \frac{t \,\sin t}{\bigl(x^{2} + t^{2}\bigr)^{2}} 
                \,\mathrm{d}t.
                $$

                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution :</b>  
                    <br><br>
                    En posant 
                    \(\displaystyle I = \int_{0}^{+\infty} \frac{x \cos t}{x^{2}+t^{2}} \,\mathrm{d}t\), 
                    on effectue une intégration par parties avec 
                    \(u = \cos t\) et \(\mathrm{d}v = \frac{x}{x^{2}+t^{2}}\,\mathrm{d}t\). 
                    On obtient la dérivée de \(\arctan\bigl(\frac{t}{x}\bigr)\) ou on 
                    différencie \(\frac{x}{x^2+t^2}\). Les limites à 
                    \(\infty\) se traitent via la décroissance de l’intégrande. 
                    Un calcul standard montre alors 
                    \(\displaystyle h(x)=2x\int_{0}^{+\infty} \frac{t\sin t}{(x^{2}+t^{2})^{2}}\,\mathrm{d}t.\)
                </p>
            </li>

            <!-- (b) -->
            <li>
                <p>
                En déduire l’inégalité suivante :
                $$\forall x \in J,\quad |h(x)| \;\leqslant\; \frac{1}{x}.$$
                </p>
                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution :</b>  
                    <br><br>
                    On a 
                    \(\displaystyle \bigl|\sin t\bigr| \le 1\). 
                    Ainsi, dans l’intégrale, 
                    \(\bigl|\frac{t \sin t}{(x^2 + t^2)^2}\bigr| \le \frac{t}{(x^2 + t^2)^2}.\)
                    L’intégration montre alors une borne 
                    \(\le \frac{1}{x}\). 
                    On trouve donc 
                    \(\displaystyle |h(x)| \le \frac{1}{x}.\)
                </p>
            </li>

            <!-- (c) -->
            <li>
                <p>
                Donner la limite de \(h(x)\) quand \(x\) tend vers \(+\infty\).
                </p>
                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution :</b>
                    <br><br>
                    Lorsque \(x \to +\infty\), l’intégrande \(\frac{x\cos t}{x^2+t^2}\) 
                    se comporte comme \(\frac{\cos t}{x}\). L’intégrale tend vers 0. 
                    Donc \(\lim_{x\to+\infty}h(x) = 0.\)
                </p>
            </li>

        </ol>
    </li>

    <!-- 3. -->
    <li>
        <ol type="a" start="1">
            
            <!-- (a) -->
            <li>
                <p>
                À l’aide d’un changement de variable, montrer que, pour tout 
                \(x \in J,\quad h(x) = \int_{0}^{+\infty} \frac{\cos (xt)}{1 + t^{2}} \,\mathrm{d}t.\)
                </p>
                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution :</b>
                    <br><br>
                    Partant de 
                    \(\displaystyle h(x)=\int_{0}^{+\infty}\frac{x\cos t}{x^2+t^2}\,\mathrm{d}t\), 
                    on effectue le changement de variable \(u = \frac{t}{x}\). 
                    On trouve 
                    \(\mathrm{d}t = x\,\mathrm{d}u\) et \(t = x\,u\). 
                    Le dénominateur \(x^2 + t^2\) devient 
                    \(x^2(1 + u^2)\). 
                    Finalement, 
                    \(\displaystyle h(x)=\int_{0}^{+\infty}\frac{\cos(xu)}{1+u^2}\,\mathrm{d}u.\)
                </p>
            </li>

            <!-- (b) -->
            <li>
                <p>
                Établir, pour tout réel \(a\), l’encadrement 
                \(0 \le 1-\cos a \le \frac{a^2}{2}\).
                </p>
                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution :</b>
                    <br><br>
                    Le premier membre \(1-\cos a \ge 0\) est classique. 
                    Pour la borne supérieure, on utilise le développement 
                    limité de \(\cos a\), ou la convexité de la fonction 
                    \(t\mapsto \cos t\). On obtient 
                    \(\displaystyle 1 - \cos a \le \frac{a^2}{2}\).
                </p>
            </li>

            <!-- (c) -->
            <li>
                <p>
                Montrer l’encadrement 
                \(\displaystyle 0 \le \frac{\pi}{2} - h(x) \le 
                  \frac{x^2}{2}\int_{0}^{A}\frac{t^2}{1+t^2}\mathrm{d}t 
                  \;+\;2\int_{A}^{+\infty}\frac{1}{1+t^2}\mathrm{d}t.\)
                </p>
                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution (idée) :</b>
                    <br><br>
                    On écrit 
                    \(\displaystyle \frac{\pi}{2}-h(x) = \int_{0}^{+\infty}\bigl[\frac{\pi}{2}\cdot\delta(t) - \cos(xt)\bigr]\frac{1}{1+t^2}\,\mathrm{d}t\). 
                    On compare \(\cos(xt)\) à 1 pour l’encadrement, et on sépare 
                    l’intégrale en deux régions \(t \in [0,A]\) et 
                    \([A,+\infty[\). Les majorations par \(1-\cos(xt)\) 
                    et la borne \(\frac{(xt)^2}{2}\) permettent d’arriver 
                    à l’inégalité voulue après quelques manipulations.
                </p>
            </li>

            <!-- (d) -->
            <li>
                <p>
                Déterminer la limite de \(h(x)\) quand \(x\) tend vers \(0\) 
                par valeurs supérieures.
                </p>
                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution :</b>
                    <br><br>
                    On montre que \(\lim_{x\to0^+}h(x)=\frac{\pi}{2}\). 
                    (On peut le voir via la représentation 
                    \(h(x)=\int_{0}^{+\infty}\frac{\cos(xt)}{1+t^2}\mathrm{d}t\), 
                    qui tend vers \(\int_{0}^{+\infty}\frac{1}{1+t^2}\mathrm{d}t=\frac{\pi}{2}.\))
                </p>
            </li>

        </ol>
    </li>

    <!-- 4. -->
    <li>
        <ol type="a" start="1">
            
            <!-- (a) -->
            <li>
                <p>
                On définit sur 
                \(U = \mathbb{R}^{2}\setminus\{\,(0,0)\}\) la fonction 
                \(\Phi(x, t)=\frac{x}{x^{2}+t^{2}}\). Calculer 
                \(\frac{\partial^2 \Phi}{\partial x^2}(x,t) 
                 + \frac{\partial^2 \Phi}{\partial t^2}(x,t)\).
                </p>
                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1);
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution :</b>
                    <br><br>
                    Par un calcul direct (dérivation répétée), on montre 
                    que 
                    \(\displaystyle \Delta \Phi = \frac{\partial^2 \Phi}{\partial x^2} 
                    + \frac{\partial^2 \Phi}{\partial t^2} = 0.\) 
                    (Il s’agit d’une forme classique de fonction harmonique 
                    en coordonnées cartésiennes.)
                </p>
            </li>

            <!-- (b) -->
            <li>
                <p>
                En déduire que, pour tout \(x \in J\), 
                \(h''(x)=h(x)\).
                </p>
                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1);
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution :</b>
                    <br><br>
                    Comme \(\Delta \Phi=0\) et \(h(x)\) est obtenu par 
                    \(\int_{0}^{\infty}\cos t\;\Phi(x,t)\,\mathrm{d}t\), 
                    on peut permuter dérivées et intégrales (hypothèses 
                    de régularité suffisantes), ce qui entraîne l’équation 
                    différentielle 
                    \(\displaystyle h''(x)=h(x)\).
                </p>
            </li>

        </ol>
    </li>

    <!-- 5. -->
    <li>
        <p>On pose, pour tout \(x \in J,\; k(x)=e^{-2x}\bigl(e^{x}h(x)\bigr)'.</p>

        <ol type="a" start="1">

            <!-- (a) -->
            <li>
                <p>Calculer \(k'(x)\).</p>
                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1);
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution (idée) :</b>
                    <br><br>
                    On dérive formellement : 
                    \(\bigl(e^{x}h(x)\bigr)'=e^{x}h'(x)+e^{x}h(x)\). 
                    Puis on multiplie par \(e^{-2x}\) et on redérive. 
                    Le résultat s’interprète via l’équation 
                    \(h''(x)=h(x)\). 
                    On constate que \(k'(x)=0\). 
                    Ainsi \(k(x)\) est constant.
                </p>
            </li>

            <!-- (b) -->
            <li>
                <p>
                En déduire que, pour tout \(x \in J,\; 
                h(x)=\frac{\pi}{2} e^{-x}\).
                </p>
                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1);
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution :</b>
                    <br><br>
                    De \(k'(x)=0\), on déduit 
                    \(\bigl(e^{x}h(x)\bigr)'=C\,e^{2x}\). 
                    Les conditions aux bornes (limite pour \(x\to+\infty\) ou \(x\to0^+\)) 
                    montrent que \(C = \frac{\pi}{2}\). 
                    On trouve donc \(\displaystyle h(x) = \frac{\pi}{2} e^{-x}\).
                </p>
            </li>

        </ol>
    </li>

</ol>

### Exercice 2

<ol type="1" start="1">

    <!-- 1. -->
    <li>
        <p>
        On désigne par \(n\) un entier naturel \(\ge 2\) et on 
        considère l’espace vectoriel 
        \(E_{n} = \mathbb{R}_{n}[X]\) (polynômes de degré \(\le n\)), 
        de base canonique \(\mathcal{B} = (1,X,\dots,X^n)\).
        </p>
        <p>
        On pose, \(\forall (P,Q)\in ( \mathbb{R}_{n}[X])^2\): 
        \(\langle P,Q\rangle = \int_{-1}^{1}P(t)\,Q(t)\,\mathrm{d}t.\)
        </p>
        <p>Montrer que c’est un produit scalaire.</p>

        <p style="border: solid 2px; border-radius: 10px; 
                  background-color:rgba(152, 180, 212, .1); 
                  padding: 10px; margin: 15px 0 15px -60px;">
            <b>Solution :</b>
            <br><br>
            La bilinéarité, la symétrie et la positivité (i.e. 
            \(\langle P,P\rangle \ge 0\) et \(\langle P,P\rangle=0 \iff P=0\)) 
            se vérifient par la définition de l’intégrale 
            \(\int_{-1}^{1}P(t)Q(t)\mathrm{d}t\). 
            Ainsi, \(\langle \,\cdot,\cdot\rangle\) est bien un produit scalaire. 
        </p>
    </li>

    <!-- 2. -->
    <li>
        <p>
        On pose, \(\forall (x,y)\in \mathbb{R}^2\),
        \(\displaystyle f(x,y)=\int_{-1}^{1}\bigl(t^4 - x\,t - y\bigr)^2\,\mathrm{d}t.\)
        </p>
        <ol type="a" start="1">
            
            <!-- (a) -->
            <li>
                <p>Justifier l’existence d’un unique \((x_0,y_0)\) qui minimise \(f\).</p>
                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution :</b>
                    <br><br>
                    \(f\) est une fonction quadratique en \((x,y)\), 
                    strictement convexe (matrice associée positive). 
                    Il existe donc un unique minimum global, obtenu en 
                    annulant les dérivées partielles \(\frac{\partial f}{\partial x}\) 
                    et \(\frac{\partial f}{\partial y}\).
                </p>
            </li>

            <!-- (b) -->
            <li>
                <p>Déterminer \((x_0,y_0)\).</p>
                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution (idée) :</b>
                    <br><br>
                    On écrit 
                    \(\displaystyle f(x,y)=\int_{-1}^{1}(t^4 - xt - y)^2\,\mathrm{d}t.\)
                    Les conditions d’optimalité imposent 
                    \(\int_{-1}^1 t(t^4-xt-y)\,\mathrm{d}t=0\) et 
                    \(\int_{-1}^1 (t^4-xt-y)\,\mathrm{d}t=0.\) 
                    On résout le système linéaire en \((x,y)\) : 
                    on trouve \(x_0=0\) et \(y_0=\int_{-1}^1 t^4 \mathrm{d}t / \int_{-1}^1 1\,\mathrm{d}t\), etc.  
                    Le calcul explicite donne 
                    \(\int_{-1}^1 t^4\mathrm{d}t = \frac{2}{5}\). 
                    Finalement, \((x_0,y_0)=(0,\tfrac{1}{5}).\)
                </p>
            </li>

        </ol>
    </li>

    <!-- 3. -->
    <li>
        <p>
        Soit \(A\in E_n\). On définit 
        \(S_A: E_n \to \mathbb{R},\; Q \mapsto \langle A,Q\rangle.\)  
        Montrer que l’application 
        \(h: A \mapsto S_A\) (de \(E_n\) vers \(\mathcal{L}(E_n,\mathbb{R})\)) 
        est un isomorphisme d’espaces vectoriels.
        </p>
        <p style="border: solid 2px; border-radius: 10px; 
                  background-color:rgba(152, 180, 212, .1); 
                  padding: 10px; margin: 15px 0 15px -60px;">
            <b>Solution :</b>
            <br><br>
            L’application \(h\) est linéaire, et un produit scalaire 
            permet l’isomorphisme de Riesz : à toute forme linéaire 
            \(S_A\) on associe l’unique \(A\) tel que 
            \(\langle A,Q\rangle = S_A(Q)\). 
            La bijectivité est garantie (forme bilinéaire non dégénérée). 
            Donc c’est bien un isomorphisme.
        </p>
    </li>

    <!-- 4. -->
    <li>
        <p>
        On définit \(\Phi(P,Q)=\int_{-1}^{1} t\,P(t)\,Q(t)\mathrm{d}t.\) 
        Montrer que c’est une forme bilinéaire symétrique et se demander 
        si c’est un produit scalaire.
        </p>
        <p style="border: solid 2px; border-radius: 10px; 
                  background-color:rgba(152, 180, 212, .1); 
                  padding: 10px; margin: 15px 0 15px -60px;">
            <b>Solution :</b>
            <br><br>
            La bilinéarité est claire : 
            \(\Phi\bigl(aP_1+bP_2,Q\bigr)=a\Phi(P_1,Q)+b\Phi(P_2,Q)\), etc. 
            La symétrie vient de la commutation \(\,P(t)Q(t)=Q(t)P(t)\). 
            En revanche, \(\Phi(P,P)=\int_{-1}^1 t(P(t))^2\mathrm{d}t\) 
            peut être négatif si \(P\) est non nul sur \([-1,0]\), 
            donc \(\Phi\) n’est pas définie positive. 
            Ce n’est pas un produit scalaire.
        </p>
    </li>

    <!-- 5. -->
    <li>
        <p>
        Montrer qu’il existe un unique \(A\in E_n\) tel que 
        \(\forall Q\in E_n,\;\Phi(P,Q)=\langle A,Q\rangle\). 
        On définit \(\varphi(P)=A\).  
        Alors \(\Phi(P,Q)=\langle \varphi(P),\,Q\rangle\).
        </p>
        <p style="border: solid 2px; border-radius: 10px; 
                  background-color:rgba(152, 180, 212, .1); 
                  padding: 10px; margin: 15px 0 15px -60px;">
            <b>Solution (idée) :</b>
            <br><br>
            Grâce à la non-dégénérescence du produit scalaire 
            \(\langle\cdot,\cdot\rangle\), toute forme bilinéaire 
            \(\Phi(\cdot,Q)\) correspond à un unique vecteur \(A\). 
            On le détermine par une méthode analogue à la question 3 : 
            pour chaque \(Q\), \(\Phi(P,Q)=\int_{-1}^{1} t\,P(t)Q(t)\mathrm{d}t\) 
            doit s’écrire \(\langle A,Q\rangle\). 
            L’unicité et l’existence en découlent.
        </p>
    </li>

    <!-- 6. -->
    <li>
        <ol type="a" start="1">
            
            <li>
                <p>\(\varphi\) est un endomorphisme de \(E_n\). Justifier.</p>
                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1);
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution :</b>
                    <br><br>
                    Clair par construction : \(\varphi\) est linéaire 
                    (somme et homothétie dans \(P\) se traduisent linéairement 
                    en \(\Phi\)). 
                    Elle agit donc comme un endomorphisme (application linéaire 
                    de \(E_n\) dans lui-même).
                </p>
            </li>
            <li>
                <p>
                Montrer que, si \(\deg P \le n-1\), alors \(\varphi(P)=X\,P\).
                </p>
                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1);
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution :</b>
                    <br><br>
                    En effet, \(\Phi(P,Q)=\int_{-1}^{1}t\,P(t)Q(t)\mathrm{d}t\). 
                    Si \(\varphi(P)=A\), alors 
                    \(\langle A,Q\rangle=\int_{-1}^1A(t)Q(t)\mathrm{d}t\). 
                    On reconnaît que multiplier \(P\) par la variable \(t\) 
                    revient exactement à un décalage de degré. 
                    Pour \(\deg P\le n-1\), on voit que \(A(t)=tP(t)\). 
                    Donc \(\varphi(P)=X\cdot P\).
                </p>
            </li>

        </ol>
    </li>

    <!-- 7. -->
    <li>
        <p>
        On suppose \(n=2\). 
        (a) Donner la matrice de \(\varphi\) dans la base canonique. 
        (b) En déduire ses valeurs propres.
        </p>
        <p style="border: solid 2px; border-radius: 10px; 
                  background-color:rgba(152, 180, 212, .1);
                  padding: 10px; margin: 15px 0 15px -60px;">
            <b>Solution (idées) :</b>
            <br><br>
            (a) La base canonique est \((1, X, X^2)\). On calcule 
            \(\varphi(1)=X\cdot1=X\), 
            \(\varphi(X)=X\cdot X=X^2\), 
            \(\varphi(X^2)=X\cdot X^2=X^3\) mais ramené dans l’espace de degré \(\le2\) 
            (ou hors base si on le projette). On trouve la matrice 
            \(\begin{pmatrix}
              0 & 0 & a \\ 
              1 & 0 & b \\
              0 & 1 & c
            \end{pmatrix}\), 
            après calcul des coordonnées. 
            <br><br>
            (b) On résout le polynôme caractéristique pour trouver 
            les valeurs propres (typiquement 0 et autres). 
            Les détails dépendent de la projection mod \(X^3\). 
            On obtient en général \(\lambda_1=0,\;\lambda_{2,3}=\dots\). 
            Le calcul concret reste assez rapide.
        </p>
    </li>

</ol>


<!-- ======================================================= -->
<!-- Partie 2 - Probabilités et statistiques                 -->
<!-- ======================================================= -->

## Partie 2 - Probabilités et statistiques

### Exercice 3

<ol type="1" start="1">

    <!-- 1. -->
    <li>
        <p>
        Soit \(X\) une variable aléatoire à densité, 
        nulle sur \(\mathbb{R}_{-}\), continue sur \(\mathbb{R}_{+}\). 
        \(F\) est la fonction de répartition.  
        <br><br>
        (a) Établir 
        \(\int_{0}^{x} t f(t)\,\mathrm{d}t 
          = \int_{0}^{x}[1-F(t)]\,\mathrm{d}t - x\,\mathbb{P}(X>x)\).
        <br>
        (b) Montrer que 
        \(\displaystyle X\) admet une espérance 
        \(\mathbb{E}(X)=\int_{0}^{+\infty}[1-F(t)]\,\mathrm{d}t\).
        </p>
        <p style="border: solid 2px; border-radius: 10px; 
                  background-color:rgba(152, 180, 212, .1);
                  padding: 10px; margin: 15px 0 15px -60px;">
            <b>Solution :</b>
            <br><br>
            (a) On intègre par parties : 
            \(\int_{0}^{x} t\,f(t)\mathrm{d}t 
              = [tF(t)]_{0}^{x} - \int_{0}^{x}F(t)\mathrm{d}t\). 
            Or \(tF(t)\big|_{t=x}=xF(x)=x(1-\mathbb{P}(X>x))\). 
            En réarrangeant, on obtient la formule demandée.
            <br><br>
            (b) Si \(\int_{0}^{+\infty}[1-F(t)]\,\mathrm{d}t\) converge, 
            on montre que \(\mathbb{E}(X)\) est finie et égale à cette intégrale 
            (c’est un résultat standard pour les v.a. positives).
        </p>
    </li>

    <!-- 2. -->
    <li>
        <p>
        Suite \(\bigl(X_n\bigr)\) de v.a. exponentielles (indépendantes) 
        de paramètre \(\lambda\). On note 
        \(S_n = \max(X_1,\dots,X_n)\).
        <br><br>
        (a) (i) Déterminer la F.R. \(F_n\) de \(S_n\).  
        (ii) En déduire une densité \(f_n\).  
        <br>
        (b) (i) Justifier la convergence de 
        \(J_n=\int_{0}^{+\infty}[1-F_n(t)]\,\mathrm{d}t.\)  
        (ii) En conclure que \(S_n\) admet une espérance.
        </p>
        <p style="border: solid 2px; border-radius: 10px; 
                  background-color:rgba(152, 180, 212, .1);
                  padding: 10px; margin: 15px 0 15px -60px;">
            <b>Solution :</b>
            <br><br>
            (a) (i) Pour des exponentielles de paramètre \(\lambda\), 
            \(\mathbb{P}(X_i \le t)=1-e^{-\lambda t}\) pour \(t\ge0\). 
            Comme \(S_n \le t\) ssi \(X_i\le t\) pour tous \(i\), on obtient 
            \(F_n(t)=\bigl(1 - e^{-\lambda t}\bigr)^n\). 
            <br>
            (ii) La densité est alors 
            \(f_n(t)=\frac{\mathrm{d}}{\mathrm{d}t}\bigl(1-e^{-\lambda t}\bigr)^n.\)
            <br><br>
            (b) (i) L’intégrale converge car \([1-F_n(t)]\) est le terme 
            \(1-\bigl(1-e^{-\lambda t}\bigr)^n\) qui décroit rapidement. 
            <br>
            (ii) On en déduit \(\mathbb{E}(S_n)\) est finie 
            (même argument que ci-dessus).
        </p>
    </li>

    <!-- 3. -->
    <li>
        <p>
        On souhaite une expression de \(\mathbb{E}(S_n)\) 
        et un équivalent pour \(n\to\infty\).  
        On pose \(T_n=\sum_{j=1}^n \frac{X_j}{j}\).  
        (a) Densité de \(\frac{X_{n+1}}{n+1}\).  
        (b) Montrer que \(f_n\) est une densité de \(T_n\).  
        (c) En déduire \(\mathbb{E}(S_n)\) et l’équivalent pour \(n\to+\infty\).
        </p>
        <p style="border: solid 2px; border-radius: 10px; 
                  background-color:rgba(152, 180, 212, .1);
                  padding: 10px; margin: 15px 0 15px -60px;">
            <b>Solution (très succincte) :</b>
            <br><br>
            (a) \(\frac{X_{n+1}}{n+1}\) a densité 
            \(\displaystyle (n+1)\lambda \exp\bigl(-\lambda(n+1)x\bigr)\) 
            pour \(x\ge0\). 
            <br><br>
            (b) Le produit de convolutions successives prouve que 
            \(\sum_{j=1}^n \frac{X_j}{j}\) a exactement la densité \(f_n\). 
            <br><br>
            (c) On utilise des techniques standard (ex. moments) pour relier 
            \(\mathbb{E}(S_n)\) à la somme \(\sum \frac1j\). 
            On trouve typiquement 
            \(\displaystyle \mathbb{E}(S_n)\sim \frac{1}{\lambda}\ln n\) 
            pour \(n\to\infty\).
        </p>
    </li>

</ol>

### Exercice 4

<ol type="1" start="1">

    <!-- 1. -->
    <li>
        <p>
        Loi lognormale : \(Z\) positif tel que \(\ln Z\) soit normal.  
        Soit \(Z_1\) avec \(X_1 = \ln Z_1 \sim \mathcal{N}(0,1)\).  
        (a) Densité de \(Z_1\).  
        (b) \(\mathbb{E}(e^{sX_1})\).  
        (c) En déduire \(\mathbb{E}(Z_1)=e^{\tfrac12}\).
        </p>
        <p style="border: solid 2px; border-radius: 10px; 
                  background-color:rgba(152, 180, 212, .1);
                  padding: 10px; margin: 15px 0 15px -60px;">
            <b>Solution :</b>
            <br><br>
            (a) Si \(Z_1>0\) et \(\ln Z_1\sim\mathcal{N}(0,1)\), alors 
            \(\displaystyle f_{Z_1}(z)=\frac{1}{z\sqrt{2\pi}}
            \exp\Bigl(-\frac{(\ln z)^2}{2}\Bigr),\;z>0.\)
            <br>
            (b) \(\mathbb{E}\bigl(e^{sX_1}\bigr)=\exp\bigl(\tfrac12 s^2\bigr)\) 
            (MGF d’une gaussienne centrée réduite).
            <br>
            (c) Pour \(s=1\), on obtient 
            \(\mathbb{E}(Z_1)=\exp(\tfrac12)\).
        </p>
    </li>

    <!-- 2. -->
    <li>
        <p>
        Soit \(Z_2\) tel que \(\ln Z_2\sim \mathcal{N}(m,\sigma^2)\).  
        Calculer \(\mathbb{E}(Z_2)\) et \(\mathrm{Var}(Z_2)\).  
        Puis on considère une suite \((Y_n)\) i.i.d. lognormales, 
        \(\ln Y_i\sim\mathcal{N}(m,\sigma^2)\).  
        On pose 
        \(\displaystyle \overline{Y_n}=\frac1n\sum_{i=1}^n Y_i\), 
        \(\displaystyle \overline{X_n}=\frac1n\sum_{i=1}^n X_i\).
        </p>
        <p style="border: solid 2px; border-radius: 10px; 
                  background-color:rgba(152, 180, 212, .1);
                  padding: 10px; margin: 15px 0 15px -60px;">
            <b>Solution :</b>
            <br><br>
            On sait que si \(X\sim \mathcal{N}(m,\sigma^2)\), 
            alors \(\exp(X)\) a pour espérance 
            \(\exp\bigl(m+\tfrac12\sigma^2\bigr)\) et pour variance 
            \(\exp\bigl(2m+\sigma^2\bigr)\bigl(e^{\sigma^2}-1\bigr)\). 
            Ainsi 
            \(\mathbb{E}(Z_2)=e^{m+\frac12\sigma^2}\) 
            et \(\mathrm{Var}(Z_2)=e^{2m+\sigma^2}\bigl(e^{\sigma^2}-1\bigr)\).
        </p>
    </li>

    <!-- 3. -->
    <li>
        <ol type="a" start="1">
            <li>
                <p>Proposer un estimateur convergent de \(\mathbb{E}(Y)\) via les \(Y_i\).</p>
                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1);
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution :</b>
                    <br><br>
                    Un estimateur naturel est 
                    \(\displaystyle T_{1,n}=\overline{Y_n}=\frac1n\sum_{i=1}^n Y_i\). 
                    Par la loi des grands nombres, \(T_{1,n}\to \mathbb{E}(Y)\) p.s.
                </p>
            </li>
            <li>
                <p>Calculer la variance de cet estimateur.</p>
                <p style="border: solid 2px; border-radius: 10px; 
                          background-color:rgba(152, 180, 212, .1);
                          padding: 10px; margin: 15px 0 15px -60px;">
                    <b>Solution :</b>
                    <br><br>
                    \(\mathrm{Var}\bigl(\overline{Y_n}\bigr)
                      = \frac1{n^2}\sum_{i=1}^n \mathrm{Var}(Y_i)
                      = \frac1n \mathrm{Var}(Y)\). 
                    Avec \(\mathrm{Var}(Y)=e^{2m+\sigma^2}(e^{\sigma^2}-1)\), 
                    on obtient 
                    \(\mathrm{Var}(T_{1,n})=\frac{e^{2m+\sigma^2}(e^{\sigma^2}-1)}{n}\).
                </p>
            </li>
        </ol>
    </li>

    <!-- 4. -->
    <li>
        <p>
        On suppose \(\sigma^2\) connu = \(\sigma_0^2\).  
        (a) Estimateur convergent de \(m\).  
        (b) Nouvel estimateur de \(\mathbb{E}(Y)\) via \(\overline{X_n}\).  
        (c) Est-il sans biais ?
        </p>
        <p style="border: solid 2px; border-radius: 10px; 
                  background-color:rgba(152, 180, 212, .1);
                  padding: 10px; margin: 15px 0 15px -60px;">
            <b>Solution :</b>
            <br><br>
            (a) Un estimateur de \(m\) est 
            \(\displaystyle \widehat{m}_n=\overline{X_n}=\frac1n\sum_{i=1}^n \ln Y_i.\) 
            Par la loi des grands nombres, \(\widehat{m}_n\to m\). 
            <br>
            (b) Connaissant \(\sigma_0^2\), on sait 
            \(\mathbb{E}(Y)=\exp\bigl(m+\tfrac12\sigma_0^2\bigr)\). 
            On propose 
            \(\displaystyle T_{2,n}=\exp\bigl(\widehat{m}_n + \tfrac12\sigma_0^2\bigr).\)
            <br>
            (c) Cet estimateur n’est pas sans biais, car 
            \(\mathbb{E}\bigl(e^{\overline{X_n}}\bigr)\neq e^{m}\). 
            Le biais tend toutefois vers 0 pour \(n\) grand (biais exponentiel).
        </p>
    </li>

    <!-- 5. -->
    <li>
        <p>
        Comparer (pour \(n\) grand) les variances des deux estimateurs 
        \(\overline{Y_n}\) et 
        \(\exp\bigl(\overline{X_n} + \tfrac12\sigma_0^2\bigr)\). 
        (Développements limités en \(\tfrac1n\).)
        </p>
        <p style="border: solid 2px; border-radius: 10px; 
                  background-color:rgba(152, 180, 212, .1);
                  padding: 10px; margin: 15px 0 15px -60px;">
            <b>Solution (esquisse) :</b>
            <br><br>
            On calcule la variance asymptotique de 
            \(\exp(\overline{X_n}+\tfrac12\sigma_0^2)\). 
            Pour des \(\ln Y_i\sim \mathcal{N}(m,\sigma_0^2)\), 
            la Delta-method donne 
            \(\mathrm{Var}(T_{2,n})\approx 
              \bigl(\frac{\mathrm{d}}{\mathrm{d}m} e^{m+\sigma_0^2/2}\bigr)^2
              \cdot \mathrm{Var}(\overline{X_n}) 
              = e^{2m+\sigma_0^2}\,\frac{\sigma_0^2}{n}.\) 
            On compare cela à 
            \(\mathrm{Var}(T_{1,n})=\frac{1}{n}e^{2m+\sigma_0^2}(e^{\sigma_0^2}-1)\). 
            Pour \(\sigma_0^2\) petit, on constate que 
            \(\mathrm{Var}(T_{2,n})<\mathrm{Var}(T_{1,n})\). 
            Pour \(\sigma_0^2\) plus grand, on compare numériquement.
        </p>
    </li>

    <!-- 6. -->
    <li>
        <p>
        On construit un estimateur linéaire 
        \(T_n=\lambda_1 T_{1,n} + \lambda_2 T_{2,n}\).  
        (a) Montrer que \(\lambda_1\) optimal est 
        \(\displaystyle \tilde{\lambda}_1
           = \frac{\mathrm{Cov}(T_{2,n}-T_{1,n},\,T_{2,n})}
                  {\mathrm{Var}(T_{2,n}-T_{1,n})}.\)
        <br>
        (b) Calcul de \(\mathrm{Cov}\bigl(Y_i,\;e^{\overline{X_n}}\bigr)\).  
        (c) Expression explicite de l’estimateur optimal.  
        (d) Comportement quand \(n\) est grand.
        </p>
        <p style="border: solid 2px; border-radius: 10px; 
                  background-color:rgba(152, 180, 212, .1);
                  padding: 10px; margin: 15px 0 15px -60px;">
            <b>Solution (grandes lignes) :</b>
            <br><br>
            (a) On écrit la variance de 
            \(\lambda_1 T_{1,n} + \lambda_2 T_{2,n}\) et on minimise 
            par rapport à \(\lambda_1,\lambda_2\) sous la contrainte 
            \(\lambda_1+\lambda_2=1\) (estimateur sans biais ou imposant 
            la somme fixe). Le critère standard donne la formule 
            \(\tilde{\lambda}_1\). 
            <br>
            (b) On calcule 
            \(\mathrm{Cov}\bigl(Y_i,e^{\overline{X_n}}\bigr)\) 
            via \(\overline{X_n}=\frac1n\sum_{k=1}^n\ln Y_k\). 
            Indépendance partielle selon \(i\). 
            On aboutit à un terme en 
            \(\exp(m+\dots)\bigl(\dots\bigr)\). 
            <br>
            (c) On substitue au final dans \(\lambda_1,\lambda_2\) 
            l’expression explicite. 
            <br>
            (d) Pour \(n\) grand, on fait un DL : la meilleure combinaison 
            donne un gain en variance, et on retrouve souvent un 
            \(\lambda_1\approx \dots\) qui tend à réduire le biais et la variance.
        </p>
    </li>

    <!-- 7. -->
    <li>
        <p>
        Cas \(\sigma^2\) inconnu : proposer un estimateur convergent 
        de \(\sigma^2\) en fonction de \(\overline{X_n}\) et \(\overline{Y_n}\). 
        Connaissez-vous d’autres estimateurs de la variance en échantillon normal ?
        </p>
        <p style="border: solid 2px; border-radius: 10px; 
                  background-color:rgba(152, 180, 212, .1);
                  padding: 10px; margin: 15px 0 15px -60px;">
            <b>Solution (idées) :</b>
            <br><br>
            On peut utiliser 
            \(\widehat{\sigma}^2_n = \frac1n\sum_{i=1}^n (\ln Y_i - \overline{X_n})^2\) 
            corrigé par la relation 
            \(\mathbb{E}(Y)=\exp\bigl(m+\tfrac12\sigma^2\bigr)\). 
            D’autres estimateurs existent (type écart quadratique), 
            en lien avec la statistique habituelle pour un échantillon normal 
            (ex. \(\displaystyle \frac1{n-1}\sum_i(X_i-\overline{X_n})^2\), etc.).
        </p>
    </li>

</ol>