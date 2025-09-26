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

<p style="border: none; border-radius: 0; background-color:rgba(152, 180, 212, .12); padding-right: 10px; padding-left: 10px; padding-top: 10px; padding-bottom: 10px; margin: 15px 0 15px 0px;">
Les propositions de corrections présentées ci-dessous n'engagent que l'auteur de ce site.
</p>

---
<!-- ========================================= -->
<!-- Partie 1 — Analyse et algèbre             -->
<!-- ========================================= -->

## Partie 1 — Analyse et algèbre

### Exercice 1

<p>
On note \(J\) l’intervalle \(\left] 0,+\infty \right[\) et on définit sur \(J\) la fonction \(h\) par :
</p>

<ol type="1" start="1">

    $$
    \forall x \in J, \quad h(x) \;=\;\int_{0}^{+\infty} \frac{x \cos t}{x^{2} + t^{2}} \,\mathrm{d}t.
    $$
    
    <!-- 1. -->
    <li>
        <p>
        Montrer que la fonction \(h\) est bien définie.
        </p>
    
        <!-- Answer placeholder -->
        <p style="border: none; border-radius: 0; 
                  background-color:rgba(152, 180, 212, .12); 
                  padding: 10px; margin: 15px 0 15px -30px;">
            Pour \(x&gt;0\), la fonction \(t\mapsto \dfrac{x\cos t}{x^{2}+t^{2}}\) est continue sur \([0,+\infty[\). <br>
            – Sur \([0,1]\), elle est bornée (en particulier \( \left|\dfrac{x\cos t}{x^{2}+t^{2}}\right| \le \dfrac{x}{x^{2}}=\dfrac1x\)), donc intégrable. <br>
            – Sur \([1,+\infty[\), on a
            \[
                \left|\frac{x\cos t}{x^{2}+t^{2}}\right| \le \frac{x}{t^{2}},
                \qquad \text{et} \quad \int_{1}^{+\infty}\frac{x}{t^{2}}\,\mathrm dt = x &lt;+\infty.
            \]
            L’intégrale impropre converge donc absolument sur \([1,+\infty[\). Par additivité, l’intégrale sur \([0,+\infty[\) existe : \(h\) est bien définie sur \(J\).
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
    
                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    Pour \(b&gt;0\), on intègre par parties sur \([0,b]\) avec
                    \[
                        u(t)=\frac{x}{x^{2}+t^{2}},\qquad v'(t)=\cos t
                        \quad\Longrightarrow\quad
                        u'(t)=-\frac{2xt}{(x^{2}+t^{2})^{2}},\; v(t)=\sin t.
                    \]
                    On obtient
                    \[
                        \int_{0}^{b}\frac{x\cos t}{x^{2}+t^{2}}\,\mathrm dt
                        =\Big[\tfrac{x\sin t}{x^{2}+t^{2}}\Big]_{0}^{b}
                        +2x\int_{0}^{b}\frac{t\sin t}{(x^{2}+t^{2})^{2}}\,\mathrm dt.
                    \]
                    Comme \(\dfrac{x\sin b}{x^{2}+b^{2}}\to 0\) quand \(b\to+\infty\) (car \(|\sin b|\le 1\) et \(\dfrac{x}{x^{2}+b^{2}}\le \dfrac{x}{b^{2}}\)), et \(\sin 0=0\), on peut passer à la limite \(b\to+\infty\) (les intégrales impropres étant convergentes par majoration) et l’égalité annoncée s’ensuit :
                    \[
                        h(x)=2x\int_{0}^{+\infty}\frac{t\sin t}{(x^{2}+t^{2})^{2}}\,\mathrm dt.
                    \]
                </p>
            </li>
    
            <!-- (b) -->
            <li>
                <p>
                En déduire l’inégalité suivante :
                </p>
                $$
                \forall x \in J,\quad |h(x)| \;\leqslant\; \frac{1}{x}.
                $$
    
                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    D’après (a),
                    \[
                        |h(x)|\le 2x\int_{0}^{+\infty}\frac{t\,|\sin t|}{(x^{2}+t^{2})^{2}}\,\mathrm dt
                        \le 2x\int_{0}^{+\infty}\frac{t}{(x^{2}+t^{2})^{2}}\,\mathrm dt.
                    \]
                    Or
                    \[
                        \int_{0}^{+\infty}\frac{t}{(x^{2}+t^{2})^{2}}\,\mathrm dt
                        =\frac1{2}\int_{0}^{+\infty}\frac{1}{(x^{2}+u)^{2}}\,\mathrm du
                        =\frac1{2}\Big[\!-\,\frac{1}{x^{2}+u}\Big]_{0}^{+\infty}
                        =\frac{1}{2x^{2}},
                    \]
                    (en posant \(u=t^{2}\)). Ainsi \(|h(x)|\le 2x\times \dfrac{1}{2x^{2}}=\dfrac{1}{x}\).
                </p>
            </li>
    
            <!-- (c) -->
            <li>
                <p>
                Donner la limite de \(h(x)\) quand \(x\) tend vers \(+\infty\).
                </p>
    
                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    D’après (b), \(|h(x)|\le \dfrac{1}{x}\) pour tout \(x&gt;0\). Par encadrement,
                    \(\displaystyle \lim_{x\to +\infty}h(x)=0\).
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
                \(x \in J\) :
                </p>
                $$
                h(x) \;=\; \int_{0}^{+\infty} \frac{\cos (xt)}{1 + t^{2}} \,\mathrm{d}t.
                $$
    
                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    Dans la définition de \(h(x)\), on pose \(t=xu\) (avec \(u\in[0,+\infty[\)), donc \(\mathrm dt=x\,\mathrm du\).
                    Alors
                    \[
                        h(x)=\int_{0}^{+\infty}\frac{x\cos(xu)}{x^{2}+x^{2}u^{2}}\,x\,\mathrm du
                        =\int_{0}^{+\infty}\frac{\cos(xu)}{1+u^{2}}\,\mathrm du,
                    \]
                    ce qui donne la formule voulue (en renommant la variable d’intégration).
                </p>
            </li>
    
            <!-- (b) -->
            <li>
                <p>
                Établir, pour tout réel \(a\), l’encadrement suivant :
                </p>
                $$
                0 \;\leqslant\; 1 - \cos a \;\leqslant\; \frac{a^{2}}{2}.
                $$
    
                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    On a \(1-\cos a=2\sin^{2}\!\bigl(\tfrac{a}{2}\bigr)\ge 0\). De plus, pour tout \(u\in\mathbb R\),
                    \(|\sin u|\le |u|\) (par inégalité des accroissements finis appliquée à \(\sin\)).
                    Ainsi
                    \[
                        1-\cos a = 2\sin^{2}\!\Big(\tfrac{a}{2}\Big) 
                        \le 2\Big(\tfrac{|a|}{2}\Big)^{2}=\frac{a^{2}}{2}.
                    \]
                </p>
            </li>
    
            <!-- (c) -->
            <li>
                <p>
                Montrer l’encadrement suivant :
                </p>
                $$
                \forall x \in J,\; \forall A>0,\quad 
                0 \;\leqslant\; \frac{\pi}{2} - h(x) \;\leqslant\; 
                \frac{x^{2}}{2} \int_{0}^{A} \frac{t^{2}}{1+t^{2}} \,\mathrm{d}t
                \;+\; 2 \int_{A}^{+\infty} \frac{1}{1 + t^{2}} \,\mathrm{d}t.
                $$
    
                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    Par (3a), 
                    \[
                        h(x)=\int_{0}^{+\infty}\frac{\cos(xt)}{1+t^{2}}\,\mathrm dt,
                        \qquad
                        \int_{0}^{+\infty}\frac{1}{1+t^{2}}\,\mathrm dt=\frac{\pi}{2}.
                    \]
                    Donc
                    \[
                        \frac{\pi}{2}-h(x)=\int_{0}^{+\infty}\frac{1-\cos(xt)}{1+t^{2}}\,\mathrm dt.
                    \]
                    Soit \(A&gt;0\). En découpant \([0,+\infty[=[0,A]\cup[A,+\infty[\) et en utilisant (3b) et \(|1-\cos(xt)|\le 2\), on obtient
                    \[
                    \begin{aligned}
                        0\le \frac{\pi}{2}-h(x)
                        &\le \int_{0}^{A}\frac{1-\cos(xt)}{1+t^{2}}\,\mathrm dt
                           +\int_{A}^{+\infty}\frac{2}{1+t^{2}}\,\mathrm dt \\
                        &\le \int_{0}^{A}\frac{x^{2}t^{2}}{2(1+t^{2})}\,\mathrm dt
                           +2\int_{A}^{+\infty}\frac{1}{1+t^{2}}\,\mathrm dt,
                    \end{aligned}
                    \]
                    ce qui donne l’encadrement requis.
                </p>
            </li>
    
            <!-- (d) -->
            <li>
                <p>
                Déterminer la limite de \(h(x)\) quand \(x\) tend vers \(0\) par valeurs supérieures.
                </p>
    
                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    À partir de (3c), pour tout \(A&gt;0\) et \(x&gt;0\),
                    \[
                        0\le \frac{\pi}{2}-h(x)\le 
                        \frac{x^{2}}{2}\int_{0}^{A}\frac{t^{2}}{1+t^{2}}\,\mathrm dt
                        +2\int_{A}^{+\infty}\frac{1}{1+t^{2}}\,\mathrm dt.
                    \]
                    En fixant \(A\) et en laissant \(x\to 0^{+}\), le premier terme du majorant tend vers \(0\).
                    Puis en choisissant \(A\) assez grand, le second terme peut être rendu arbitrairement petit.
                    Par le procédé usuel \(\varepsilon\!-\!A\), on déduit
                    \[
                        \lim_{x\to 0^{+}}h(x)=\frac{\pi}{2}.
                    \]
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
                On définit sur \(U = \mathbb{R}^{2}\setminus\{\,(0,0)\}\) la fonction 
                \(\Phi\) par
                </p>
                $$
                \Phi(x, t) \;=\; \frac{x}{x^{2} + t^{2}}.
                $$
                <p>
                Calculer, pour \((x,t)\in U,\; 
                \frac{\partial^2 \Phi}{\partial x^2}(x,t) \;+\;
                \frac{\partial^2 \Phi}{\partial t^2}(x,t).\)
                </p>
    
                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    Posons \(s=x^{2}+t^{2}\). On a
                    \[
                        \partial_{x}\Phi=\frac{s-2x^{2}}{s^{2}}=\frac{t^{2}-x^{2}}{s^{2}},
                        \qquad
                        \partial_{t}\Phi=-\frac{2xt}{s^{2}}.
                    \]
                    Puis
                    \[
                        \partial_{xx}\Phi
                        =\frac{-2x}{s^{2}}-\frac{4x(t^{2}-x^{2})}{s^{3}},
                        \qquad
                        \partial_{tt}\Phi
                        =-\frac{2x}{s^{2}}+\frac{8xt^{2}}{s^{3}}.
                    \]
                    En sommant,
                    \[
                        \partial_{xx}\Phi+\partial_{tt}\Phi
                        =-\frac{4x}{s^{2}}+\frac{4x(x^{2}+t^{2})}{s^{3}}=0.
                    \]
                    Ainsi, \(\Phi\) est harmonique sur \(U\).
                </p>
            </li>
    
            <!-- (b) -->
            <li>
                <p>
                En déduire que, pour tout \(x \in J,\; h''(x) = h(x)\).
                </p>
    
                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    On écrit
                    \[
                        h(x)=\int_{0}^{+\infty}\Phi(x,t)\,\cos t\,\mathrm dt.
                    \]
                    Pour \(x&gt;0\), les dérivées partielles \(\partial_{x}\Phi,\partial_{xx}\Phi\) existent et
                    \(|\partial_{xx}\Phi(x,t)|\le C_{x}\,(x^{2}+t^{2})^{-2}\), fonction intégrable en \(t\) sur \([0,+\infty[\).
                    On peut donc dériver sous le signe intégral (théorème de dérivation des intégrales à paramètre) et obtenir
                    \[
                        h''(x)=\int_{0}^{+\infty}\partial_{xx}\Phi(x,t)\,\cos t\,\mathrm dt.
                    \]
                    Or \(\partial_{xx}\Phi=-\partial_{tt}\Phi\) d’après (4a), d’où
                    \[
                        h''(x)=-\int_{0}^{+\infty}\partial_{tt}\Phi(x,t)\,\cos t\,\mathrm dt.
                    \]
                    En intégrant par parties deux fois par rapport à \(t\) (les termes de bord s’annulent car
                    \(\partial_{t}\Phi(x,t)=\mathcal O(1/t^{3})\) et \(\Phi(x,t)=\mathcal O(1/t^{2})\) quand \(t\to+\infty\), et \(\Phi,\partial_{t}\Phi\) sont nulles en \(t=0\)),
                    on obtient
                    \[
                        \int_{0}^{+\infty}\partial_{tt}\Phi\,\cos t\,\mathrm dt
                        = -\int_{0}^{+\infty}\Phi\,\cos t\,\mathrm dt.
                    \]
                    Ainsi \(h''(x)=h(x)\) pour tout \(x\in J\).
                </p>
            </li>
    
        </ol>
    </li>
    
    <!-- 5. -->
    <li>
        <p>
        On pose, pour tout \(x \in J,\; k(x)=e^{-2x}\bigl(e^{x}h(x)\bigr)'\). 
        </p>
        <ol type="a" start="1">
    
            <!-- (a) -->
            <li>
                <p>
                Calculer \(k'(x)\).
                </p>
    
                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    On a \((e^{x}h(x))'=e^{x}(h'(x)+h(x))\), donc
                    \[
                        k(x)=e^{-2x}\cdot e^{x}\,(h'+h)=e^{-x}(h'+h).
                    \]
                    Ainsi
                    \[
                        k'(x)=-e^{-x}(h'+h)+e^{-x}(h''+h')=e^{-x}\bigl(h''-h\bigr).
                    \]
                    Or, d’après (4b), \(h''=h\). Par conséquent \(k'(x)=0\) pour tout \(x\in J\).
                </p>
            </li>
    
            <!-- (b) -->
            <li>
                <p>
                En déduire que, pour tout \(x \in J,\; 
                h(x)=\frac{\pi}{2}\, e^{-x}\).
                </p>
    
                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    De (a), \(k'(x)=0\) donc \(k\) est constante : il existe \(C\in\mathbb R\) tel que
                    \[
                        (e^{x}h(x))'=C\,e^{2x}.
                    \]
                    En intégrant, il existe \(D\in\mathbb R\) tel que
                    \[
                        e^{x}h(x)=\frac{C}{2}e^{2x}+D
                        \quad\Longleftrightarrow\quad
                        h(x)=\frac{C}{2}e^{x}+D\,e^{-x}.
                    \]
                    D’après (2c), \(\displaystyle \lim_{x\to+\infty}h(x)=0\), donc nécessairement \(C=0\), d’où
                    \(h(x)=D\,e^{-x}\). Enfin, par (3d), \(\displaystyle \lim_{x\to 0^{+}}h(x)=\dfrac{\pi}{2}\),
                    ce qui impose \(D=\dfrac{\pi}{2}\). Par suite,
                    \[
                        \boxed{\;h(x)=\dfrac{\pi}{2}\,e^{-x}\;}\qquad (x&gt;0).
                    \]
                </p>
            </li>
    
        </ol>
    </li>
</ol>

<ol type="1" start="1">

    $$
    \forall x \in J, \quad h(x) \;=\;\int_{0}^{+\infty} \frac{x \cos t}{x^{2} + t^{2}} \,\mathrm{d}t.
    $$

    <!-- 1. -->
    <li>
        <p>
        Montrer que la fonction \(h\) est bien définie.
        </p>

        <!-- Answer placeholder -->
        <p style="border: none; border-radius: 0; 
                  background-color:rgba(152, 180, 212, .12); 
                  padding: 10px; margin: 15px 0 15px -30px;">
            ...
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

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <!-- (b) -->
            <li>
                <p>
                En déduire l’inégalité suivante :
                </p>
                $$
                \forall x \in J,\quad |h(x)| \;\leqslant\; \frac{1}{x}.
                $$

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <!-- (c) -->
            <li>
                <p>
                Donner la limite de \(h(x)\) quand \(x\) tend vers \(+\infty\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
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
                \(x \in J\) :
                </p>
                $$
                h(x) \;=\; \int_{0}^{+\infty} \frac{\cos (xt)}{1 + t^{2}} \,\mathrm{d}t.
                $$

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <!-- (b) -->
            <li>
                <p>
                Établir, pour tout réel \(a\), l’encadrement suivant :
                </p>
                $$
                0 \;\leqslant\; 1 - \cos a \;\leqslant\; \frac{a^{2}}{2}.
                $$

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <!-- (c) -->
            <li>
                <p>
                Montrer l’encadrement suivant :
                </p>
                $$
                \forall x \in J,\; \forall A>0,\quad 
                0 \;\leqslant\; \frac{\pi}{2} - h(x) \;\leqslant\; 
                \frac{x^{2}}{2} \int_{0}^{A} \frac{t^{2}}{1+t^{2}} \,\mathrm{d}t
                \;+\; 2 \int_{A}^{+\infty} \frac{1}{1 + t^{2}} \,\mathrm{d}t.
                $$

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <!-- (d) -->
            <li>
                <p>
                Déterminer la limite de \(h(x)\) quand \(x\) tend vers \(0\) par valeurs supérieures.
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
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
                On définit sur \(U = \mathbb{R}^{2}\setminus\{\,(0,0)\}\) la fonction 
                \(\Phi\) par
                </p>
                $$
                \Phi(x, t) \;=\; \frac{x}{x^{2} + t^{2}}.
                $$
                <p>
                Calculer, pour \((x,t)\in U,\; 
                \frac{\partial^2 \Phi}{\partial x^2}(x,t) \;+\;
                \frac{\partial^2 \Phi}{\partial t^2}(x,t).\)
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <!-- (b) -->
            <li>
                <p>
                En déduire que, pour tout \(x \in J,\; h''(x) = h(x)\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

        </ol>
    </li>

    <!-- 5. -->
    <li>
        <p>
        On pose, pour tout \(x \in J,\; k(x)=e^{-2x}\bigl(e^{x}h(x)\bigr)'\). 
        </p>
        <ol type="a" start="1">

            <!-- (a) -->
            <li>
                <p>
                Calculer \(k'(x)\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <!-- (b) -->
            <li>
                <p>
                En déduire que, pour tout \(x \in J,\; 
                h(x)=\frac{\pi}{2}\, e^{-x}\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
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
        On désigne par \(n\) un entier naturel supérieur ou égal à 2 et on 
        considère l’espace vectoriel 
        \(E_{n} = \mathbb{R}_{n}[X]\) des polynômes de degré 
        inférieur ou égal à \(n\), dont la base canonique est 
        \(\mathcal{B} = (1, X, \ldots, X^n)\).
        </p>
        <p>
        On pose, pour tout couple \((P,Q)\) d’éléments de 
        \(\bigl(\mathbb{R}_{n}[X]\bigr)^2\):
        </p>
        $$
        \langle P,Q\rangle \;=\;\int_{-1}^{1} P(t)\,Q(t)\,\mathrm{d}t.
        $$
        <p>
        Montrer que \(\langle \,\cdot\,,\,\cdot\,\rangle\) est 
        un produit scalaire.
        </p>

        <!-- Answer placeholder -->
        <p style="border: none; border-radius: 0; 
                  background-color:rgba(152, 180, 212, .12); 
                  padding: 10px; margin: 15px 0 15px -30px;">
            ...
        </p>
    </li>

    <!-- 2. -->
    <li>
        <p>
        On pose, pour tout couple de réels \((x,y)\):
        </p>
        $$
        f(x,y) \;=\; \int_{-1}^{1}\bigl(t^4 - x\,t - y\bigr)^2 \,\mathrm{d}t.
        $$

        <ol type="a" start="1">
            
            <!-- (a) -->
            <li>
                <p>
                Justifier l’existence d’un unique couple de réels 
                \(\bigl(x_0, y_0\bigr)\) tel que 
                \(f(x_0, y_0)=\displaystyle\inf_{(x,y)\in \mathbb{R}^2} f(x,y)\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <!-- (b) -->
            <li>
                <p>
                Déterminer \(\bigl(x_0, y_0\bigr)\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

        </ol>
    </li>

    <!-- 3. -->
    <li>
        <p>
        Soit \(A\) un élément de \(E_{n}\). On définit l’application 
        \(S_{A}\) de \(E_{n}\) dans \(\mathbb{R}\) par :
        </p>
        $$
        S_{A}: \quad E_{n} \longrightarrow \mathbb{R},\quad 
        Q \longmapsto \langle A,\, Q\rangle.
        $$
        <p>
        Montrer que l’application 
        \(h: A \longmapsto S_{A}\) 
        (de \(E_{n}\) vers \(\mathcal{L}(E_{n}, \mathbb{R})\)) 
        est un isomorphisme d’espaces vectoriels.
        </p>

        <!-- Answer placeholder -->
        <p style="border: none; border-radius: 0; 
                  background-color:rgba(152, 180, 212, .12); 
                  padding: 10px; margin: 15px 0 15px -30px;">
            ...
        </p>
    </li>

    <!-- 4. -->
    <li>
        <p>
        On définit l’application \(\Phi\) par :
        </p>
        $$
        \Phi: E_{n}\times E_{n}\;\longrightarrow\;\mathbb{R},\quad
        (P,Q)\;\longmapsto\;\int_{-1}^{1} t\,P(t)\,Q(t)\,\mathrm{d}t.
        $$
        <p>
        Montrer que \(\Phi\) est une forme bilinéaire symétrique 
        sur \(E_{n}\). Est-ce un produit scalaire sur \(E_{n}\)?
        </p>

        <!-- Answer placeholder -->
        <p style="border: none; border-radius: 0; 
                  background-color:rgba(152, 180, 212, .12); 
                  padding: 10px; margin: 15px 0 15px -30px;">
            ...
        </p>
    </li>

    <!-- 5. -->
    <li>
        <p>
        Montrer qu’il existe un unique polynôme \(A \in E_{n}\), 
        dépendant de \(P\), tel que:
        \[
          \forall Q \in E_{n},\quad \Phi(P,Q) \;=\;\langle A,\,Q\rangle.
        \]
        </p>
        <p>
        On note alors \(\varphi\) l’application de \(E_{n}\) dans lui-même, 
        définie par \(\varphi(P)=A\). On a donc 
        \(\forall(P,Q)\in E_{n}^2, \;\Phi(P,Q)=\langle\varphi(P),\,Q\rangle\).
        </p>

        <!-- Answer placeholder -->
        <p style="border: none; border-radius: 0; 
                  background-color:rgba(152, 180, 212, .12); 
                  padding: 10px; margin: 15px 0 15px -30px;">
            ...
        </p>
    </li>

    <!-- 6. -->
    <li>
        <ol type="a" start="1">
            
            <li>
                <p>
                Montrer que \(\varphi\) est un endomorphisme de \(E_{n}\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                <p>
                Montrer que, pour tout polynôme \(P\) de \(E_{n}\) 
                avec \(\deg P \leqslant n-1,\; \varphi(P)=X\,P\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

        </ol>
    </li>

    <!-- 7. -->
    <li>
        <p>
        On suppose, dans cette question, que \(n=2\).
        </p>
        <ol type="a" start="1">

            <li>
                <p>
                Donner la matrice de \(\varphi\) dans la base canonique de \(E_{2}\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                <p>
                Donner les valeurs propres de \(\varphi\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

        </ol>
    </li>

</ol>

<!-- ========================================= -->
<!-- Partie 2 — Probabilités et statistiques   -->
<!-- ========================================= -->

## Partie 2 — Probabilités et statistiques

### Exercice 3

<ol type="1" start="1">

    <!-- 1. -->
    <li>
        <p>
        Soit \(X\) une variable aléatoire à densité, dont une densité \(f\) 
        est nulle sur \(\mathbb{R}_{-}\) et continue sur \(\mathbb{R}_{+}\). 
        On note \(F\) la fonction de répartition de \(X\).
        </p>
        <ol type="a" start="1">

            <!-- (a) -->
            <li>
                <p>
                Établir, pour tout réel \(x\) positif, l’égalité suivante :
                </p>
                $$
                \int_{0}^{x} t\,f(t)\,\mathrm{d}t 
                \;=\; \int_{0}^{x}\bigl[\,1 - F(t)\bigr]\mathrm{d}t 
                      \;-\; x\,\mathbb{P}(X > x).
                $$

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <!-- (b) -->
            <li>
                <p>
                On suppose que l’intégrale 
                \(\int_{0}^{+\infty}\bigl[\,1 - F(t)\bigr]\mathrm{d}t\) 
                est convergente. Montrer que \(X\) admet une espérance 
                mathématique et établir l’égalité suivante :
                </p>
                $$
                \mathbb{E}(X) 
                \;=\;\int_{0}^{+\infty}\bigl[\,1 - F(t)\bigr]\mathrm{d}t.
                $$

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

        </ol>
    </li>

    <!-- 2. -->
    <li>
        <p>
        On considère une suite de variables aléatoires 
        \(\bigl(X_{n}\bigr)_{n \in \mathbb{N}^{*}}\), définies 
        sur le même espace probabilisé \((\Omega,\mathcal{A},\mathbb{P})\), 
        mutuellement indépendantes et suivant toutes la loi exponentielle 
        de paramètre \(\lambda\) (\(\lambda>0\)).
        </p>
        <p>
        Pour tout \(n \in \mathbb{N}^{*}\), on pose 
        \(S_{n} = \max\bigl(X_{1}, X_{2}, \ldots, X_{n}\bigr)\).
        </p>
        $$
        \forall \omega \in \Omega,\quad
        S_{n}(\omega) = \max\bigl(X_{1}(\omega), X_{2}(\omega),\ldots, X_{n}(\omega)\bigr).
        $$

        <ol type="a" start="1">
            
            <li>
                <p>
                (i) Déterminer la fonction de répartition \(F_{n}\) de \(S_{n}\).
                <br>
                (ii) En déduire que \(S_{n}\) est une variable aléatoire à densité 
                et déterminer une densité \(f_{n}\) de \(S_{n}\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <li>
                <p>
                (i) On pose, pour tout entier \(n \ge 1\):
                </p>
                $$
                J_{n} \;=\; \int_{0}^{+\infty}\bigl[\,1 - F_{n}(t)\bigr]\mathrm{d}t.
                $$

                <ol type="i" start="1">
                    <li>
                        <p>Montrer que l’intégrale \(J_{n}\) est convergente.</p>

                        <!-- Answer placeholder -->
                        <p style="border: none; border-radius: 0; 
                                  background-color:rgba(152, 180, 212, .12); 
                                  padding: 10px; margin: 15px 0 15px -60px;">
                            ...
                        </p>
                    </li>
                    <li>
                        <p>En déduire que \(S_{n}\) admet une espérance mathématique.</p>

                        <!-- Answer placeholder -->
                        <p style="border: none; border-radius: 0; 
                                  background-color:rgba(152, 180, 212, .12); 
                                  padding: 10px; margin: 15px 0 15px -60px;">
                            ...
                        </p>
                    </li>
                </ol>
            </li>

        </ol>
    </li>

    <!-- 3. -->
    <li>
        <p>
        On se propose de trouver une expression simple de 
        \(\mathbb{E}\bigl(S_{n}\bigr)\) et un équivalent de 
        \(\mathbb{E}\bigl(S_{n}\bigr)\) quand \(n \to +\infty\). 
        Pour tout \(n \ge 1\), on pose 
        \(T_{n} = \sum_{j=1}^{n} \dfrac{X_{j}}{j}\).
        </p>
        <ol type="a" start="1">

            <li>
                <p>
                Déterminer une densité de la variable aléatoire 
                \(\dfrac{X_{n+1}}{n+1}\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <li>
                <p>
                Montrer que, pour tout \(n \ge 1,\; f_{n}\) est une densité 
                de \(T_{n}\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <li>
                <p>
                En déduire l’expression de \(\mathbb{E}\bigl(S_{n}\bigr)\) et 
                un équivalent de \(\mathbb{E}\bigl(S_{n}\bigr)\) quand 
                \(n\) tend vers \(+\infty\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

        </ol>
    </li>

</ol>

### Exercice 4

<ol type="1" start="1">

    <!-- 1. -->
    <li>
        <p>
        On dit qu’une variable aléatoire \(Z\) à valeurs strictement 
        positives suit une loi lognormale si la variable aléatoire 
        \(\ln Z\) suit une loi normale.
        </p>
        <p>
        Soit \(Z_{1}\) une variable aléatoire à valeurs strictement positives, 
        telle que \(X_{1} = \ln Z_{1}\) suive la loi normale centrée réduite.
        </p>
        <ol type="a" start="1">

            <li>
                <p>
                Donner la densité de \(Z_{1}\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <li>
                <p>
                Calculer, pour tout réel \(s\), \(\mathbb{E}\bigl(e^{sX_{1}}\bigr)\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <li>
                <p>
                En déduire que \(\mathbb{E}\bigl(Z_{1}\bigr) = e^{\tfrac12}\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

        </ol>
    </li>

    <!-- 2. -->
    <li>
        <p>
        Soit \(Z_{2}\) une variable aléatoire à valeurs strictement positives 
        telle que \(X_{2}=\ln Z_{2}\) suive la loi normale \(\mathcal{N}(m,\sigma^2)\). 
        Calculer, en utilisant les résultats de la première question, 
        \(\mathbb{E}\bigl(Z_{2}\bigr)\) et \(\mathrm{Var}\bigl(Z_{2}\bigr)\).
        </p>
        <p>
        On considère dorénavant une suite de variables aléatoires 
        \(\bigl(Y_{n}\bigr)_{n\ge1}\), à valeurs strictement positives, 
        indépendantes, suivant toutes la même loi lognormale, associées aux 
        variables \(X_{i}=\ln Y_{i}\), où chaque \(X_{i}\) suit la loi 
        \(\mathcal{N}(m,\sigma^{2})\). 
        On notera génériquement \(\mathbb{E}(Y)\) et \(\mathrm{Var}(Y)\) 
        l’espérance et la variance de ces variables.
        </p>
        <p>
        On pose, pour tout \(n\ge1\):
        </p>
        $$
        \overline{Y_{n}} = \frac{1}{n}\sum_{i=1}^{n}Y_{i}
        \quad\text{et}\quad
        \overline{X_{n}} = \frac{1}{n}\sum_{i=1}^{n}X_{i}.
        $$

    </li>

    <!-- 3. -->
    <li>
        <ol type="a" start="1">
            <li>
                <p>
                Proposer un estimateur convergent de \(\mathbb{E}(Y)\), 
                obtenu à partir des \(Y_{i}\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                <p>
                Calculer la variance de cet estimateur, en fonction de 
                \(m\) et de \(\sigma^{2}\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
        </ol>
    </li>

    <!-- 4. -->
    <li>
        <p>
        On suppose, dans les questions suivantes 4, 5 et 6, que \(\sigma^2\) 
        est connu : \(\sigma^2 = \sigma_{0}^2\).
        </p>
        <ol type="a" start="1">
            <li>
                <p>
                Proposer un estimateur convergent de \(m\) obtenu à partir 
                des \(X_{i}\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                <p>
                En déduire un nouvel estimateur convergent de \(\mathbb{E}(Y)\), 
                fonction de \(\overline{X_{n}}\) et de \(\sigma_{0}^2\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
            <li>
                <p>
                Cet estimateur est-il sans biais ?
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
        </ol>
    </li>

    <!-- 5. -->
    <li>
        <p>
        Comparer, pour \(n\) grand, selon leurs variances, les deux estimateurs 
        de \(\mathbb{E}(Y)\) obtenus en 3.(a) et en 4.(b). 
        On pourra effectuer des développements limités des variances 
        considérées en puissances de \(\tfrac1n\).
        </p>

        <!-- Answer placeholder -->
        <p style="border: none; border-radius: 0; 
                  background-color:rgba(152, 180, 212, .12); 
                  padding: 10px; margin: 15px 0 15px -30px;">
            ...
        </p>
    </li>

    <!-- 6. -->
    <li>
        <p>
        On note \(T_{1,n}\) l’estimateur de \(\mathbb{E}(Y)\) obtenu en 3.(a) 
        et \(T_{2,n}\) celui obtenu en 4.(b). On cherche à construire un 
        estimateur convergent de \(\mathbb{E}(Y)\), combinaison linéaire 
        de \(T_{1,n}\) et \(T_{2,n}\) et de variance minimale. 
        Un tel estimateur sera donc de la forme :
        </p>
        $$
        T_{n} \;=\;\lambda_{1} T_{1,n} \;+\;\lambda_{2} T_{2,n}.
        $$
        <ol type="a" start="1">
            <li>
                <p>
                En raisonnant sur les moments de \(T_{1,n}\) et \(T_{2,n}\), 
                sans chercher à les expliciter à ce stade, montrer que la 
                solution optimale de ce problème conduit à prendre, 
                pour valeur de \(\lambda_{1}\), le réel \(\tilde{\lambda}_{1}\) 
                défini par :
                </p>
                $$
                \tilde{\lambda}_{1} \;=\;
                \frac{\mathrm{Cov}\bigl(T_{2,n}-T_{1,n},\,T_{2,n}\bigr)}
                     {\mathrm{Var}\bigl(T_{2,n}-T_{1,n}\bigr)}.
                $$

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <li>
                <p>
                Pour tout \(i\) fixé, calculer 
                \(\mathrm{Cov}\bigl(Y_{i},\,e^{\overline{X_{n}}}\bigr)\).
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <li>
                <p>
                En déduire l’expression explicite de l’estimateur optimal obtenu.
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>

            <li>
                <p>
                Que devient cette expression pour \(n\) assez grand ?
                <br>
                (On effectuera à nouveau des développements limités 
                 des variances considérées en puissances de \(1/n\).)
                </p>

                <!-- Answer placeholder -->
                <p style="border: none; border-radius: 0; 
                          background-color:rgba(152, 180, 212, .12); 
                          padding: 10px; margin: 15px 0 15px -60px;">
                    ...
                </p>
            </li>
        </ol>
    </li>

    <!-- 7. -->
    <li>
        <p>
        On revient au cas où \(\sigma^2\) est inconnu. Proposer un 
        estimateur convergent de \(\sigma^2\), s’exprimant comme fonction, 
        à la fois, de \(\overline{X_{n}}\) et de \(\overline{Y_{n}}\). 
        Connaissez-vous d’autres estimateurs de la variance 
        dans un échantillon normal ?
        </p>

        <!-- Answer placeholder -->
        <p style="border: none; border-radius: 0; 
                  background-color:rgba(152, 180, 212, .12); 
                  padding: 10px; margin: 15px 0 15px -30px;">
            ...
        </p>
    </li>

</ol>
