# Domande di teoria degli esami passati — fino al determinante

> **Ambito di studio:** capitoli **1–5** del dispensario *Geometria e Algebra Lineare* di Elisa Postinghel, fino alla fine del capitolo **5 — Il determinante** (p. 125).  
> **Fonti:** PDF nella cartella [Esami anni precedenti](./) e dispensario del corso.  
> **Uso:** raccolta ragionata delle domande, risposte essenziali, esempi svolti e priorità di ripasso. Le formulazioni delle domande sono talvolta normalizzate per correggere i caratteri illeggibili dell'estrazione dai PDF.

## Indice

1. [Come leggere le frequenze](#1-come-leggere-le-frequenze)
2. [Graduatoria degli argomenti ricorrenti](#2-graduatoria-degli-argomenti-ricorrenti)
3. [Capitolo 1 — Vettori geometrici e geometria nello spazio](#3-capitolo-1--vettori-geometrici-e-geometria-nello-spazio)
4. [Capitolo 2 — Sistemi lineari](#4-capitolo-2--sistemi-lineari)
5. [Capitolo 3 — Matrici](#5-capitolo-3--matrici)
6. [Capitolo 4 — Spazi vettoriali](#6-capitolo-4--spazi-vettoriali)
7. [Capitolo 5 — Il determinante](#7-capitolo-5--il-determinante)
8. [Tracce per appello](#8-tracce-per-appello)
9. [Domande incontrate ma **oltre** il capitolo 5](#9-domande-incontrate-ma-oltre-il-capitolo-5)
10. [Piano di ripasso e simulazione](#10-piano-di-ripasso-e-simulazione)

---

## 1. Come leggere le frequenze

L'analisi quantitativa principale riguarda **18 appelli GAL** del periodo **2023 – giugno 2026**, includendo le *provette* disponibili: 6 del 2023, 6 del 2024, 5 del 2025 e 1 del 2026. Si considera la **presenza di almeno una domanda sull'argomento per appello**, non il numero di versioni A/B/C/D che ripetono il quesito. Uno stesso appello può comparire in più categorie.

Le prove del **2021–2022**, spesso **a crocette**, e i PDF storici **2016–2018** vengono usati come conferma qualitativa delle tipologie, **senza mescolarli al denominatore di 18**. Le soluzioni contrassegnate *sol* o *corr* non valgono come ulteriori appelli.

**Attenzione:** i conteggi sono una classificazione per famiglie di argomenti, non una probabilità matematica che la prossima prova contenga un quesito. La forma dell'esame cambia da anno ad anno. Non sono state considerate domande che richiedono esclusivamente i capitoli 6–9.

## 2. Graduatoria degli argomenti ricorrenti

| Famiglia di domande | Appelli GAL 2023–giugno 2026 | Priorità di studio |
|---|---:|---|
| Dipendenza e indipendenza lineare, con esempi | **12/18** | **Molto alta** |
| Vettori geometrici: prodotto scalare, proiezioni, normalizzazione | **10/18** | **Molto alta** |
| Basi e sistemi di generatori | **8/18** | **Alta** |
| Sottospazi vettoriali | **6/18** | **Alta** |
| Teorema di Rouché-Capelli ed esempi di sistemi | **6/18** | **Alta** |
| Matrici: scalini, prodotto, invertibilità e rango | **6/18** | **Alta** |
| Determinante come domanda esplicita: Binet, rango, invertibilità | **2/18** | **Da conoscere comunque** |

Le categorie possono sovrapporsi e le cifre vanno lette come **frequenze storiche approssimate per argomento**. Un tema poco chiesto autonomamente, come Laplace o Cramer, può essere indispensabile per gli **esercizi**.

### Domande da padroneggiare per prime

- Dare la **definizione di sottospazio** e due esempi in $\mathbb{R}^3$.
- Dare la **definizione di dipendenza/indipendenza lineare** con esempi.
- Distinguere un **insieme indipendente**, un **sistema di generatori** e una **base**.
- **Enunciare Rouché-Capelli** e costruire un sistema compatibile/incompatibile.
- Definire la **proiezione ortogonale** e saper usare la formula sulle componenti.
- Definire una **matrice invertibile**, collegandola al rango e poi al determinante.
- Enunciare **Binet** e dedurre il determinante dell'inversa.

---

## 3. Capitolo 1 — Vettori geometrici e geometria nello spazio

**Riferimento al dispensario:** capitolo 1, pp. 5–41.

### D1. Che cos'è un vettore geometrico? Quali sono le proprietà della somma?

**Tracce:** [provetta 2022](./GALprovetta22.pdf), [settembre 2023](./GALset23.pdf) (quest'ultima per il prodotto scalare).

**Risposta:** un vettore geometrico è una **classe di equivalenza di segmenti orientati** aventi stessa direzione, stesso verso e stesso modulo. Un vettore non dipende dal punto di applicazione del rappresentante.

La somma di vettori geometrici soddisfa:

- commutatività: $\mathbf{v}+\mathbf{w}=\mathbf{w}+\mathbf{v}$;
- associatività: $(\mathbf{u}+\mathbf{v})+\mathbf{w}=\mathbf{u}+(\mathbf{v}+\mathbf{w})$;
- esistenza del vettore nullo: $\mathbf{v}+\mathbf{0}=\mathbf{v}$;
- esistenza dell'opposto: $\mathbf{v}+(-\mathbf{v})=\mathbf{0}$.

**Esempio:** in coordinate, $(1,2,0)+(3,-1,2)=(4,1,2)$.

### D2. Definizione e proprietà del prodotto scalare di vettori geometrici

**Tracce:** [settembre 2023](./GALset23.pdf), [luglio 2024](./GALlug24.pdf), [settembre 2025](./GALset25.pdf).

Per vettori non nulli, con angolo $\theta$ fra loro:

$$
\mathbf{v}\cdot\mathbf{w}
=|\mathbf{v}|\cdot|\mathbf{w}|\cdot\cos\theta.
$$

In una base cartesiana ortonormale, se $\mathbf{v}=(v_1,v_2,v_3)$ e $\mathbf{w}=(w_1,w_2,w_3)$:

$$
\mathbf{v}\cdot\mathbf{w}=v_1w_1+v_2w_2+v_3w_3.
$$

**Proprietà da ricordare:** simmetria, linearità rispetto a ciascun argomento e $\mathbf{v}\cdot\mathbf{v}=|\mathbf{v}|^2\geq 0$, con uguaglianza se e solo se $\mathbf{v}=\mathbf{0}$. Due vettori non nulli sono ortogonali se e solo se il loro prodotto scalare è zero.

**Verifica frequentemente richiesta:** dimostrare per componenti la distributività

$$
\mathbf{v}\cdot(\mathbf{u}+\mathbf{w})
=\mathbf{v}\cdot\mathbf{u}+\mathbf{v}\cdot\mathbf{w}.
$$

**Dimostrazione breve:** scrivendo $\mathbf{v}=(v_i)$, $\mathbf{u}=(u_i)$ e $\mathbf{w}=(w_i)$, si ha $\sum_i v_i(u_i+w_i)=\sum_i v_iu_i+\sum_i v_iw_i$.

### D3. Come si calcola la proiezione ortogonale su un versore o su un vettore qualsiasi?

**Tracce:** [febbraio 2023](./GALfeb23.pdf), [gennaio 2024](./GALgen24.pdf), [gennaio 2025](./GALgen25.pdf), [luglio 2025](./GALlug25.pdf).

Su un versore $\mathbf{e}$, cioè $|\mathbf{e}|=1$:

$$
\mathrm{proj}_{\mathbf{e}}(\mathbf{v})
=(\mathbf{v}\cdot\mathbf{e})\mathbf{e}.
$$

Su un vettore **non nullo** $\mathbf{w}$:

$$
\mathrm{proj}_{\mathbf{w}}(\mathbf{v})
=\frac{\mathbf{v}\cdot\mathbf{w}}{\mathbf{w}\cdot\mathbf{w}}\cdot\mathbf{w}.
$$

**Esempio:** $\mathbf{v}=(3,4,0)$ e $\mathbf{w}=(1,0,0)$; la proiezione è $(3,0,0)$.

**Attenzione all'esame:** una cosa è la *componente scalare* lungo un versore, $\mathbf{v}\cdot\mathbf{e}$; altra cosa è il *vettore proiezione*, $(\mathbf{v}\cdot\mathbf{e})\mathbf{e}$.

### D4. Che cos'è la normalizzazione di un vettore?

**Tracce:** [giugno 2024](./GALgiu24.pdf), [settembre 2024](./GALset24.pdf).

Per un vettore geometrico non nullo $\mathbf{v}$, il **versore** avente la stessa direzione e lo stesso verso è

$$
\widehat{\mathbf{v}}=\frac{\mathbf{v}}{|\mathbf{v}|}.
$$

Se $\mathbf{v}=(3,4,0)$, allora $|\mathbf{v}|=5$ e $\widehat{\mathbf{v}}=(3/5,4/5,0)$. Il vettore nullo non si può normalizzare.

### D5. Rette, piani e distanze: quale teoria ripassare?

Nelle **crocette 2021–2022** ricorrono affermazioni su rette parallele, incidenti, sghembe e complanari; negli esercizi degli appelli recenti sono comuni rette, piani e distanze.

- Il piano con normale $\mathbf{n}=(a,b,c)\neq\mathbf{0}$ ha equazione $ax+by+cz+d=0$.
- Una retta può essere descritta in forma parametrica come $(x,y,z)=P+t\mathbf{v}$, con $\mathbf{v}\neq\mathbf{0}$.
- Distanza di $P=(x_0,y_0,z_0)$ dal piano $ax+by+cz+d=0$:

$$
d(P,\pi)=\frac{|ax_0+by_0+cz_0+d|}{\sqrt{a^2+b^2+c^2}}.
$$

**Errore da evitare:** due rette nello spazio non sono automaticamente complanari; possono essere **sghembe**.

---

## 4. Capitolo 2 — Sistemi lineari

**Riferimento al dispensario:** capitolo 2, pp. 42–61.

### D6. Enunciare e spiegare il teorema di Rouché-Capelli

**Enunciato del teorema di Rouché-Capelli.** Un sistema lineare $A\mathbf{x}=\mathbf{b}$ è **compatibile**, cioè ammette almeno una soluzione, **se e solo se** il rango della matrice dei coefficienti $A$ è uguale al rango della matrice completa $[A\mid\mathbf{b}]$.

$$
\boxed{
A\mathbf{x}=\mathbf{b}\ \text{è compatibile}
\iff \mathrm{rg}(A)=\mathrm{rg}([A\mid\mathbf{b}]).
}
$$

**Tracce:** [gennaio 2023](./GALgen23.pdf), [luglio 2023](./GALlug23.pdf), [provetta 2023](./GALprovetta23.pdf), [febbraio 2024](./GALfeb24.pdf), [settembre 2024](./GALset24.pdf), [provetta 2024](./GALprovetta24.pdf).

#### 1. Quali matrici confrontiamo?

Consideriamo un sistema lineare di **$m$ equazioni in $n$ incognite**:

$$
A\mathbf{x}=\mathbf{b}.
$$

- **$A$ (matrice dei coefficienti):** contiene solo i coefficienti delle incognite e ha $m$ righe e $n$ colonne.
- **$[A\mid\mathbf{b}]$ (matrice completa):** è la matrice $A$ a cui aggiungiamo **un'ultima colonna**, quella dei termini noti $\mathbf{b}$. Ha quindi $m$ righe e $n+1$ colonne.
- **$\mathrm{rg}(A)$:** è il numero di colonne linearmente indipendenti di $A$ (equivalentemente, il numero di pivot dopo Gauss).
- **$\mathrm{rg}([A\mid\mathbf{b}])$:** è il rango dopo aver aggiunto la colonna dei termini noti.

**Il punto fondamentale:** chiedere che esista una soluzione equivale a chiedere che $\mathbf{b}$ si possa ottenere come **combinazione lineare delle colonne di $A$**. In simboli, scrivendo $A=[\mathbf{a}_1\ \cdots\ \mathbf{a}_n]$:

$$
x_1\mathbf{a}_1+\cdots+x_n\mathbf{a}_n=\mathbf{b}.
$$

Se $\mathbf{b}$ è già nello spazio generato dalle colonne di $A$, aggiungerla **non aumenta il rango** e il sistema è compatibile. Se non lo è, il rango della matrice completa **aumenta di 1** e il sistema è impossibile.

#### 2. Teorema di Rouché-Capelli: prima la compatibilità

$$
\boxed{
A\mathbf{x}=\mathbf{b}\ \text{è compatibile}
\iff
\mathrm{rg}(A)=\mathrm{rg}([A\mid\mathbf{b}]).
}
$$

Questa è la condizione **necessaria e sufficiente** affinché il sistema ammetta *almeno una soluzione*.

- Se $\mathrm{rg}(A)\neq\mathrm{rg}([A\mid\mathbf{b}])$, il sistema è **incompatibile**: **nessuna soluzione**.
- Se $\mathrm{rg}(A)=\mathrm{rg}([A\mid\mathbf{b}])$, il sistema è **compatibile**: **almeno una soluzione**. Solo ora passiamo al secondo confronto.

**Attenzione:** in questo primo passaggio confrontiamo **due ranghi**. Non stiamo ancora confrontando il rango con il numero delle incognite.

#### 3. Solo dopo: una soluzione oppure infinite?

Supponiamo che i due ranghi siano **uguali** e poniamo $r=\mathrm{rg}(A)$ e $n=$ numero delle incognite (numero delle colonne di $A$):

- Se **$r=n$**, il sistema ha **un'unica soluzione**.
- Se **$r<n$**, il sistema ha **infinite soluzioni**, con **$n-r$ parametri liberi**.

| Confronto fra i ranghi | Confronto con $n$ | Conclusione |
|---|---|---|
| $\mathrm{rg}(A)\neq\mathrm{rg}([A\mid\mathbf{b}])$ | Non serve | **Nessuna soluzione** |
| $\mathrm{rg}(A)=\mathrm{rg}([A\mid\mathbf{b}])=n$ | Rango uguale a $n$ | **Una soluzione unica** |
| $\mathrm{rg}(A)=\mathrm{rg}([A\mid\mathbf{b}])<n$ | Rango minore di $n$ | **Infinite soluzioni** |

**Errore da evitare:** la condizione $\mathrm{rg}(A)<n$ **da sola non dice** se un sistema sia compatibile. Prima bisogna controllare il rango della matrice completa.

#### 4. Esempio A — Incompatibile: i due ranghi sono diversi

Sistema di **2 equazioni e 3 incognite**:

$$
\begin{cases}
x+y+z=1,\\
2x+2y+2z=3.
\end{cases}
$$

Le matrici sono:

$$
A=
\begin{pmatrix}
1&1&1\\
2&2&2
\end{pmatrix},
\qquad
[A\mid\mathbf{b}]=
\begin{pmatrix}
1&1&1&1\\
2&2&2&3
\end{pmatrix}.
$$

- In $A$ la seconda riga è il doppio della prima: **$\mathrm{rg}(A)=1$**.
- Nella matrice completa la seconda riga **non** è il doppio della prima, perché $3\neq2\cdot1$: **$\mathrm{rg}([A\mid\mathbf{b}])=2$**.

Quindi il sistema è **incompatibile**. Infatti la prima equazione, moltiplicata per 2, darebbe $2x+2y+2z=2$, in contraddizione con la seconda.

Qui $n=3$ e $\mathrm{rg}(A)=1<3$, **ma non ci sono infinite soluzioni**: il sistema è impossibile perché **i due ranghi non coincidono**.

#### 5. Esempio B — Compatibile con un'unica soluzione

Sistema di **3 equazioni e 2 incognite**:

$$
\begin{cases}
x+y=1,\\
x-y=0,\\
2x=1.
\end{cases}
$$

$$
A=
\begin{pmatrix}
1&1\\
1&-1\\
2&0
\end{pmatrix},
\qquad
[A\mid\mathbf{b}]=
\begin{pmatrix}
1&1&1\\
1&-1&0\\
2&0&1
\end{pmatrix}.
$$

Le prime due righe di $A$ sono indipendenti e la terza equazione è la somma delle prime due. Si ha quindi

$$
\mathrm{rg}(A)=\mathrm{rg}([A\mid\mathbf{b}])=2=n.
$$

Il sistema è **compatibile** e ha **un'unica soluzione**:

$$
(x,y)=\left(\frac12,\frac12\right).
$$

#### 6. Esempio C — Compatibile con infinite soluzioni

Sistema di **2 equazioni e 2 incognite**:

$$
\begin{cases}
x+y=3,\\
2x+2y=6.
\end{cases}
$$

$$
A=
\begin{pmatrix}
1&1\\
2&2
\end{pmatrix},
\qquad
[A\mid\mathbf{b}]=
\begin{pmatrix}
1&1&3\\
2&2&6
\end{pmatrix}.
$$

La seconda riga è il doppio della prima **in entrambe le matrici**; quindi

$$
\mathrm{rg}(A)=\mathrm{rg}([A\mid\mathbf{b}])=1<2=n.
$$

Il sistema è **compatibile** ma ha **infinite soluzioni**. C'è $n-r=2-1=1$ parametro libero; per esempio:

$$
(x,y)=(t,3-t),\qquad t\in\mathbb{R}.
$$

#### 7. Schema da ricordare all'esame

**Prima domanda: esistono soluzioni?** Confronta $\mathrm{rg}(A)$ con $\mathrm{rg}([A\mid\mathbf{b}])$.

**Seconda domanda (solo se esistono): quante soluzioni?** Confronta il rango comune con il numero di incognite $n$.

**Perché è importante:** nelle provette chiedono spesso **enunciato + esempio** di sistema compatibile o incompatibile, non soltanto la definizione.

### D7. Che cos'è una matrice a scalini? E una matrice a scalini ridotta per righe?

**Enunciato del metodo di Gauss (eliminazione per righe).** Ogni matrice può essere trasformata, mediante un **numero finito di operazioni elementari sulle righe**, in una **matrice a scalini**. Il numero di pivot ottenuti è il **rango della matrice** e non dipende dalla particolare sequenza di operazioni utilizzate.

Se applichiamo queste operazioni alla **matrice completa di un sistema lineare** $[A\mid\mathbf{b}]$, otteniamo un sistema **equivalente a quello iniziale**, cioè con **lo stesso insieme delle soluzioni**.

Le operazioni elementari ammesse sono:

1. **Scambiare** due righe.
2. **Moltiplicare** una riga per uno scalare **non nullo**.
3. **Sommare** a una riga un multiplo di un'altra riga.

**Distinzione:** l'eliminazione di **Gauss** porta la matrice in **forma a scalini**; proseguendo con la normalizzazione dei pivot e l'eliminazione anche **sopra** di essi, si ottiene la **forma a scalini ridotta per righe** (procedimento di **Gauss-Jordan**). Nel dispensario questo argomento è presentato come *algoritmo di Gauss-Jordan*, non come un teorema autonomo.

**Tracce:** [febbraio 2023](./GALfeb23.pdf), [febbraio 2025](./GALfeb25.pdf).

Una matrice è **a scalini per righe** se le righe nulle sono in fondo e i pivot delle righe non nulle si spostano strettamente verso destra scendendo di riga, con zeri sotto ogni pivot.

Una matrice è **a scalini ridotta per righe** se, inoltre, ogni pivot è 1 e nella sua colonna tutti gli altri elementi sono zero.

**Esempio a scalini (non ridotta):**

$$
\begin{pmatrix}
1&2&3\\
0&1&4\\
0&0&0
\end{pmatrix}.
$$

**Esempio a scalini ridotta per righe:**

$$
\begin{pmatrix}
1&0&-5\\
0&1&4\\
0&0&0
\end{pmatrix}.
$$

Il **rango** è il numero di pivot di una forma a scalini. Per calcolare le soluzioni si usa l'eliminazione di Gauss o Gauss-Jordan.

### D8. Perché l'insieme delle soluzioni di $A\mathbf{x}=\mathbf{0}$ è un sottospazio?

**Collegamenti:** sistemi lineari, matrici e sottospazi; rilevante anche nelle crocette 2021–2022.

Indichiamo con $U=\lbrace\mathbf{x}:A\mathbf{x}=\mathbf{0}\rbrace$. Se $\mathbf{x},\mathbf{y}\in U$ e $\lambda,\mu\in\mathbb{R}$, allora

$$
A(\lambda\mathbf{x}+\mu\mathbf{y})
=\lambda A\mathbf{x}+\mu A\mathbf{y}
=\mathbf{0}.
$$

Quindi $U$ è chiuso rispetto alle combinazioni lineari e contiene il vettore nullo.

**Confronto importante:** l'insieme delle soluzioni di $A\mathbf{x}=\mathbf{b}$ con $\mathbf{b}\neq\mathbf{0}$, se non vuoto, **non** è un sottospazio perché non contiene $\mathbf{0}$.

---

## 5. Capitolo 3 — Matrici

**Riferimento al dispensario:** capitolo 3, pp. 62–85.

### D9. Quando si può definire il prodotto righe per colonne e come si calcola?

**Traccia:** [febbraio 2025](./GALfeb25.pdf).

Se $A$ ha dimensioni $m\times n$ e $B$ ha dimensioni $n\times p$, il prodotto $AB$ è definito e ha dimensioni $m\times p$. L'elemento in posizione $(i,j)$ vale

$$
(AB)_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}.
$$

**Esempio:** siano

$$
A =
\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix},
\qquad
B =
\begin{pmatrix}
2 & 0 \\
1 & 3
\end{pmatrix}.
$$

Calcoliamo gli elementi del prodotto, moltiplicando ogni riga di $A$ per ogni colonna di $B$:

$$
AB =
\begin{pmatrix}
1\cdot 2 + 2\cdot 1 & 1\cdot 0 + 2\cdot 3 \\
0\cdot 2 + 1\cdot 1 & 0\cdot 0 + 1\cdot 3
\end{pmatrix}
=
\begin{pmatrix}
4 & 6 \\
1 & 3
\end{pmatrix}.
$$

**Attenzione:** in generale $AB\neq BA$; il prodotto non è commutativo.

### D10. Definire una matrice quadrata invertibile e dare esempi

**Tracce:** [gennaio 2023](./GALgen23.pdf), [gennaio 2024](./GALgen24.pdf), [provetta 2024](./GALprovetta24.pdf), [luglio 2025](./GALlug25.pdf).

Una matrice quadrata $A\in M_n(\mathbb{R})$ è **invertibile** se esiste $B\in M_n(\mathbb{R})$ tale che

$$
AB=BA=I_n.
$$

Tale matrice è unica ed è indicata con $A^{-1}$.

**Esempi:**

$$
A=\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix},
\qquad
A^{-1}=\begin{pmatrix}
1 & -2 \\
0 & 1
\end{pmatrix}.
$$

$$
C=\begin{pmatrix}
1 & 2 \\
2 & 4
\end{pmatrix}
$$

non è invertibile: la seconda riga è multipla della prima, quindi il rango è 1 invece di 2.

### D11. Qual è il legame tra rango e invertibilità?

**Tracce:** [febbraio 2023](./GALfeb23.pdf), [febbraio 2025](./GALfeb25.pdf). Il criterio con il determinante è approfondito nel capitolo 5.

Per $A\in M_n(\mathbb{R})$, **$n$ è l'ordine della matrice**: poiché $A$ è quadrata, ha **$n$ righe e $n$ colonne**. Quindi $\mathrm{rg}(A)=n$ significa che la matrice ha **rango massimo**, pari sia al numero di righe sia al numero di colonne. Il criterio di invertibilità qui vale per **matrici quadrate**:

$$
A\text{ invertibile}\iff\mathrm{rg}(A)=n.
$$

Dopo il capitolo 5 il criterio equivalente diventa:

$$
A\text{ invertibile}
\iff \mathrm{rg}(A)=n
\iff \det(A)\neq 0.
$$

**Come calcolare l'inversa con Gauss-Jordan:** si costruisce la matrice aumentata $[A\mid I_n]$ e si applicano operazioni elementari alle righe fino a ottenere $[I_n\mid A^{-1}]$, se possibile. Se $A$ non ha rango massimo, non esiste l'inversa.

---

## 6. Capitolo 4 — Spazi vettoriali

**Riferimento al dispensario:** capitolo 4, pp. 86–107. Il capitolo 4 introduce già **generatori, indipendenza e basi**; la teoria generale della **dimensione** viene sviluppata nel capitolo 6.

### D12. Dare la definizione di sottospazio vettoriale ed esempi di rette/piani in $\mathbb{R}^3$

**Tracce:** [giugno 2023](./GALgiu23.pdf), [gennaio 2024](./GALgen24.pdf), [gennaio 2025](./GALgen25.pdf), [giugno 2026](./GALgiu26.pdf).

Sia $V$ uno spazio vettoriale reale. Un sottoinsieme **non vuoto** $U\subseteq V$ è un sottospazio se è chiuso rispetto a somma e prodotto per scalari; equivalentemente:

$$
\forall\;\mathbf{u},\mathbf{v}\in U,\ \forall\;\lambda,\mu\in\mathbb{R},
\quad \lambda\mathbf{u}+\mu\mathbf{v}\in U.
$$

**Esempi di sottospazi di $\mathbb{R}^3$:**

- Retta passante per l'origine: $U=\lbrace(t,0,0):t\in\mathbb{R}\rbrace$.
- Piano passante per l'origine: $W=\lbrace(s,t,0):s,t\in\mathbb{R}\rbrace$.

**Controesempio:** $Z=\lbrace(x,y,z)\in\mathbb{R}^3:x+y+z=1\rbrace$ non è un sottospazio, perché $(0,0,0)\notin Z$.

**Controllo rapido:** prima verifica se $\mathbf{0}$ appartiene all'insieme, poi la chiusura rispetto a $\lambda\mathbf{u}+\mu\mathbf{v}$. È un test necessario e sufficiente, se l'insieme non è vuoto.

### D13. Che cos'è una combinazione lineare? Che cos'è un sistema di generatori?

**Tracce:** [gennaio 2023](./GALgen23.pdf), [gennaio 2025](./GALgen25.pdf); anche [intermedia novembre 2018](./GeoTLC_intermedia_novembre_2018.pdf).

**Definizione.** Dati i vettori $\mathbf{v}_1,\ldots,\mathbf{v}_k\in V$, una **combinazione lineare di questi vettori** è **un vettore ottenuto sommando multipli scalari dei vettori assegnati**. Scelti gli scalari $\lambda_1,\ldots,\lambda_k\in\mathbb{R}$, il vettore risultante è

$$
\mathbf{v}=\lambda_1\mathbf{v}_1+\lambda_2\mathbf{v}_2+\cdots+\lambda_k\mathbf{v}_k.
$$

**Attenzione:** non basta dire che una combinazione lineare «è un vettore»: bisogna specificare **come si ottiene e da quali vettori**.

Il **sottospazio generato** dai vettori è l'insieme di tutte le loro combinazioni lineari:

$$
\mathrm{Span}(\mathbf{v}_1,\ldots,\mathbf{v}_k)
=\lbrace\sum_{i=1}^{k}\lambda_i\mathbf{v}_i:
\lambda_i\in\mathbb{R}\rbrace.
$$

Un insieme di vettori è un **sistema di generatori di $V$** se il suo Span coincide con $V$.

**Esempio:** $\lbrace(1,0),(0,1)\rbrace$ genera $\mathbb{R}^2$, perché ogni $(x,y)$ si scrive $x(1,0)+y(0,1)$.

**Criterio operativo in $\mathbb{R}^n$:** affiancare i vettori come **colonne** in una matrice $A$; generano $\mathbb{R}^n$ se e solo se $\mathrm{rg}(A)=n$.

### D14. Definizione di insieme linearmente dipendente e indipendente, con esempi

**Tracce:** [gennaio 2023](./GALgen23.pdf), [luglio 2023](./GALlug23.pdf), [provetta 2023](./GALprovetta23.pdf), [gennaio 2025](./GALgen25.pdf), [febbraio 2025](./GALfeb25.pdf), [giugno 2025](./GALgiu25.pdf), [settembre 2025](./GALset25.pdf), [giugno 2026](./GALgiu26.pdf).

#### Che cosa significa «linearmente indipendenti»?

Dei vettori sono **linearmente indipendenti** quando **nessuno di essi può essere ottenuto facendo una combinazione lineare degli altri**. In altre parole, nessun vettore è ricavabile dagli altri.

La definizione precisa è questa: se moltiplichiamo ciascun vettore per un numero e sommiamo i risultati, **l'unico modo per ottenere il vettore nullo è usare tutti coefficienti uguali a zero**.

**Esempio:** in $\mathbb{R}^2$ consideriamo i vettori

$$
v_1=(1,0),\qquad v_2=(0,1).
$$

Se scriviamo una combinazione lineare uguale al vettore nullo,

$$
a(1,0)+b(0,1)=(0,0),
$$

otteniamo $(a,b)=(0,0)$. Quindi **entrambi i coefficienti devono essere zero** e i due vettori sono **linearmente indipendenti**.

#### Che cosa significa «linearmente dipendenti»?

Dei vettori sono **linearmente dipendenti** quando **almeno uno di essi può essere ottenuto come combinazione lineare degli altri**.

In modo equivalente, possiamo ottenere il **vettore nullo anche usando coefficienti che non sono tutti zero**.

**Esempio:** in $\mathbb{R}^2$ prendiamo

$$
v_1=(1,0),\qquad v_2=(0,1),\qquad v_3=(1,1).
$$

Il terzo vettore è la somma dei primi due: $v_3=v_1+v_2$. Perciò possiamo scrivere

$$
1\cdot v_1+1\cdot v_2-1\cdot v_3=(0,0).
$$

Abbiamo ottenuto il vettore nullo **senza usare tutti coefficienti zero**: i tre vettori sono quindi **linearmente dipendenti**.

#### Come riconoscerli con una matrice?

Se abbiamo **$k$ vettori di $\mathbb{R}^n$**, li disponiamo come **colonne** di una matrice $A$. La matrice avrà **$n$ righe** (una per ogni componente dei vettori) e **$k$ colonne** (una per ogni vettore).

- Se il **rango di $A$ è uguale a $k$**, tutti i $k$ vettori sono **linearmente indipendenti**.
- Se il **rango di $A$ è minore di $k$**, i vettori sono **linearmente dipendenti**.

Il rango indica il **numero massimo di colonne linearmente indipendenti** della matrice.

#### Casi da riconoscere subito

- Se tra i vettori compare il **vettore nullo**, l'insieme è linearmente dipendente.
- Se **un vettore è multiplo di un altro**, l'insieme è linearmente dipendente.
- Se abbiamo **più vettori che componenti** (per esempio, tre vettori di $\mathbb{R}^2$), sono necessariamente linearmente dipendenti.

**Da ricordare:** *indipendenti* significa che nessun vettore si ricava dagli altri; *dipendenti* significa che almeno uno si ricava dagli altri.

### D15. Dare la definizione di base e distinguere base, indipendenza e generatori

**Tracce:** [giugno 2023](./GALgiu23.pdf), [gennaio 2024](./GALgen24.pdf), [giugno 2024](./GALgiu24.pdf), [luglio 2024](./GALlug24.pdf), [gennaio 2025](./GALgen25.pdf), [giugno 2026](./GALgiu26.pdf).

Una **base** di $V$ è un insieme di vettori che è **contemporaneamente**:

1. linearmente indipendente;
2. un sistema di generatori di $V$.

**Esempio di insieme indipendente di $\mathbb{R}^3$ che non è una base:**

$$
\lbrace(1,0,0),(0,1,0)\rbrace.
$$

Non genera i vettori con terza coordinata non nulla.

**Esempio di sistema di generatori di $\mathbb{R}^3$ che non è una base:**

$$
\lbrace(1,0,0),(0,1,0),(0,0,1),(1,1,0)\rbrace.
$$

Genera tutto lo spazio, ma è dipendente.

**Base dello spazio delle matrici $2\times 2$:**

$$
\lbrace
\begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix},
\begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix},
\begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix},
\begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix}
\rbrace.
$$

Ogni matrice $2\times2$ è una combinazione lineare **unica** di queste quattro matrici.

**Differenza da memorizzare:** *indipendente* non implica *generatore* e *generatore* non implica *indipendente*. Una *base* soddisfa entrambe le condizioni.

---

## 7. Capitolo 5 — Il determinante

**Riferimento al dispensario:** capitolo 5, pp. 108–125.

Le due domande autonome effettivamente emerse con maggior chiarezza negli appelli recenti sono quella su **Binet** ([febbraio 2024](./GALfeb24.pdf)) e quella sul **legame determinante–rango–invertibilità** ([febbraio 2025](./GALfeb25.pdf), versione B). Le altre voci qui sotto sono **approfondimenti del programma e della sezione «Domande di teoria» del dispensario**, non domande dichiarate frequenti negli appelli recenti.

### D16. Che cos'è il determinante? Come si calcola per matrici $2\times2$ e $3\times3$?

Il determinante è uno **scalare** associato a una matrice **quadrata**. Per

$$
A=\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$

si ha

$$
\det(A)=ad-bc.
$$

Per le matrici $3\times3$ si può usare lo sviluppo di Laplace. Ad esempio:

$$
B=\begin{pmatrix}
1&2&0\\
0&3&0\\
2&1&4
\end{pmatrix}.
$$

Sviluppando lungo la terza colonna, che contiene due zeri:

$$
\det(B)=4\det\begin{pmatrix}
1 & 2 \\
0 & 3
\end{pmatrix}
=4\cdot3=12.
$$

Per una matrice triangolare il determinante è il prodotto degli elementi della diagonale principale.

### D17. Enunciare il teorema di Laplace

**Approfondimento di programma:** §5.1.1 del dispensario.

Per qualsiasi riga fissata $i$:

$$
\det(A)=\sum_{j=1}^{n}(-1)^{i+j}a_{ij}\det(A_{ij}),
$$

dove $A_{ij}$ si ottiene eliminando la riga $i$ e la colonna $j$. Una formula equivalente vale sviluppando lungo una qualunque colonna.

**Da saper spiegare:** il fattore $(-1)^{i+j}$ stabilisce il segno del cofattore; conviene scegliere righe o colonne con molti zeri.

### D18. Enunciare il teorema di Binet e dedurre la formula per l'inversa

**Traccia:** [febbraio 2024](./GALfeb24.pdf). **Domanda corrispondente anche nel dispensario**, §5.4.4.

Se $A,B\in M_n(\mathbb{R})$, allora

$$
\boxed{\det(AB)=\det(A)\det(B).}
$$

Se $A$ è invertibile, $AA^{-1}=I_n$; quindi

$$
1=\det(I_n)=\det(A)\det(A^{-1}),
$$

e dunque

$$
\boxed{\det(A^{-1})=\frac{1}{\det(A)}.}
$$

**Mini esempio:**

$$
A=\begin{pmatrix}
1 & 1 \\
0 & 2
\end{pmatrix},
\qquad
B=\begin{pmatrix}
3 & 0 \\
1 & 1
\end{pmatrix}.
$$

Qui $\det(A)=2$, $\det(B)=3$ e

$$
AB=\begin{pmatrix}
4 & 1 \\
2 & 2
\end{pmatrix},
\qquad
\det(AB)=8-2=6=2\cdot3.
$$

### D19. Come cambiano i determinanti con le operazioni elementari sulle righe?

**Approfondimento di programma:** §5.1.3 del dispensario.

| Operazione elementare | Effetto sul determinante |
|---|---|
| Scambio di due righe | Cambia segno |
| Moltiplicazione di una riga per $\lambda$ | Viene moltiplicato per $\lambda$ |
| Somma a una riga di un multiplo di un'altra | Rimane invariato |

Per la seconda operazione, se $\lambda=0$, il nuovo determinante è zero e l'operazione non è invertibile.

**Applicazione:** porta una matrice quadrata in forma triangolare con Gauss, registra eventuali scambi o fattori moltiplicativi e usa il prodotto degli elementi diagonali.

### D20. Qual è il rapporto tra determinante, rango e invertibilità?

**Traccia:** [febbraio 2025](./GALfeb25.pdf), versione B. **Domanda corrispondente anche nel dispensario**, §5.4.4.

Per una matrice $A$ **quadrata di ordine $n$**:

$$
\boxed{
\det(A)\neq0
\iff \mathrm{rg}(A)=n
\iff A\text{ è invertibile}.
}
$$

Le negazioni sono equivalenti: $\det(A)=0$ se e solo se $\mathrm{rg}(A)<n$ se e solo se $A$ non è invertibile.

**Applicazione ai sistemi:** se $\det(A)\neq0$, il sistema quadrato $A\mathbf{x}=\mathbf{b}$ ha **un'unica soluzione per ogni** $\mathbf{b}$.

**Applicazione alle basi:** $n$ vettori di $\mathbb{R}^n$ sono una base se e solo se il determinante della matrice che li ha come colonne è non nullo.

### D21. Enunciare il teorema di Cramer e fare un esempio

**Approfondimento di programma:** §5.3.1 del dispensario, anche nella lista delle domande di teoria §5.4.4.

Se $A$ è una matrice $n\times n$ con $\det(A)\neq0$, il sistema $A\mathbf{x}=\mathbf{b}$ ha soluzione unica e

$$
x_j=\frac{\det(A_j(\mathbf{b}))}{\det(A)},
$$

dove $A_j(\mathbf{b})$ si ottiene sostituendo la colonna $j$ di $A$ con $\mathbf{b}$.

**Esempio:**

$$
\begin{cases}
x+y=3,\\
x-y=1.
\end{cases}
$$

$$
A=\begin{pmatrix}
1 & 1 \\
1 & -1
\end{pmatrix},
\quad \det(A)=-2.
$$

Sostituendo le colonne si ottiene $\det(A_1(\mathbf{b}))=-4$ e $\det(A_2(\mathbf{b}))=-2$; quindi $x=2$, $y=1$.

**Limite:** Cramer richiede una matrice quadrata con determinante non nullo; non si applica direttamente a un sistema rettangolare o singolare.

### D22. Come si trova l'inversa tramite i cofattori?

**Approfondimento di programma:** §5.3.2 del dispensario.

Il cofattore dell'elemento $a_{ij}$ è

$$
C_{ij}=(-1)^{i+j}\det(A_{ij}).
$$

Se $A$ è invertibile, la formula è

$$
A^{-1}=\frac{1}{\det(A)}\cdot C^{T},
$$

dove $C$ è la matrice dei cofattori (la trasposta $C^T$ è detta anche **aggiunta classica**).

Per una matrice

$$
A=
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$

con $ad-bc\neq0$:

$$
A^{-1}=\frac{1}{ad-bc}
\begin{pmatrix}
d & -b \\
-c & a
\end{pmatrix}.
$$

### D23. Definire prodotto vettoriale e prodotto misto, con aree e volumi

**Approfondimento di programma:** §5.3.3 e domande finali del capitolo 5.

Il **prodotto vettoriale** $\mathbf{v}\times\mathbf{w}$ è ortogonale a entrambi i vettori; il verso è determinato dalla regola della mano destra e il modulo è

$$
|\mathbf{v}\times\mathbf{w}|=|\mathbf{v}|\cdot|\mathbf{w}|\cdot\sin\theta.
$$

L'area del **parallelogramma** è $|\mathbf{v}\times\mathbf{w}|$; quella del **triangolo** è la metà.

**Esempio:** $\mathbf{v}=(1,0,0)$, $\mathbf{w}=(0,2,0)$:

$$
\mathbf{v}\times\mathbf{w}=(0,0,2).
$$

L'area del parallelogramma è $2$; quella del triangolo è $1$.

Il **prodotto misto** è $\mathbf{u}\cdot(\mathbf{v}\times\mathbf{w})$ ed equivale al determinante della matrice avente i tre vettori per righe (o per colonne, mantenendo lo stesso ordine). Il suo valore assoluto è il **volume del parallelepipedo** individuato dai tre vettori.

---

## 8. Tracce per appello

Di seguito la **mappa degli argomenti entro il capitolo 5** riscontrati nelle sezioni teoriche. La data nel nome del PDF identifica l'appello; più versioni dello stesso appello possono contenere domande diverse.

| Appello | Domande / argomenti nel programma 1–5 |
|---|---|
| [Gennaio 2023](./GALgen23.pdf) | Rouché-Capelli; indipendenza lineare; generatori; matrice invertibile |
| [Febbraio 2023](./GALfeb23.pdf) | Proiezione ortogonale; matrici a scalini; sottospazi; rango e invertibilità |
| [Giugno 2023](./GALgiu23.pdf) | Sottospazi di $\mathbb{R}^3$; indipendenza, generatori e basi |
| [Luglio 2023](./GALlug23.pdf) | Rouché-Capelli; dipendenza lineare |
| [Settembre 2023](./GALset23.pdf) | Vettori geometrici e prodotto scalare; basi di matrici |
| [Provetta 2023](./GALprovetta23.pdf) | Rouché-Capelli con esempi; indipendenza/dipendenza |
| [Gennaio 2024](./GALgen24.pdf) | Sottospazi; matrice invertibile; proiezione; indipendenza e generatori |
| [Febbraio 2024](./GALfeb24.pdf) | Rouché-Capelli; sistemi compatibili/incompatibili; **Binet** |
| [Giugno 2024](./GALgiu24.pdf) | Normalizzazione; definizione di base e base delle matrici $2\times2$ |
| [Luglio 2024](./GALlug24.pdf) | Prodotto scalare; indipendenza e sistemi di generatori |
| [Settembre 2024](./GALset24.pdf) | Normalizzazione; Rouché-Capelli |
| [Provetta 2024](./GALprovetta24.pdf) | Rouché-Capelli con esempi; dipendenza; matrice invertibile |
| [Gennaio 2025](./GALgen25.pdf) | Sottospazi; base di matrici; indipendenza e generatori; proiezione |
| [Febbraio 2025](./GALfeb25.pdf) | Distributività prodotto scalare; prodotto tra matrici; matrici a scalini; indipendenza; **determinante, rango e invertibilità** |
| [Giugno 2025](./GALgiu25.pdf) | Indipendenza lineare di matrici |
| [Luglio 2025](./GALlug25.pdf) | Proiezione ortogonale; matrici invertibili |
| [Settembre 2025](./GALset25.pdf) | Distributività del prodotto scalare; dipendenza lineare |
| [Giugno 2026](./GALgiu26.pdf) | Sottospazi; indipendenza e sistemi di generatori |

### Conferme dalle prove storiche

- [Provetta 2021](./GALprovetta21.pdf) e [appelli 2022](./GALgen22.pdf): frequenti **crocette** su sottospazi, generatori, rango/dimensione, sistemi lineari e geometria dello spazio.
- [Provetta 2017](./GAprovetta17.pdf): sottospazi, Rouché-Capelli, invertibilità, prodotto scalare e definizioni.
- [Intermedia novembre 2018](./GeoTLC_intermedia_novembre_2018.pdf): Rouché-Capelli con esempi, generatori, indipendenza, sottospazi e proiezione.
- [Settembre 2018](./GAset2018.pdf): Rouché-Capelli con esempi.
- [Febbraio 2017](./GAfeb17.pdf): sottospazi e basi con esempi.

**Nota sulla confrontabilità:** alcuni esami storici appartengono a formati e insegnamenti indicati diversamente nei file; sono utili per allenarsi, ma non entrano nelle frequenze 2023–2026.

---

## 9. Domande incontrate ma **oltre** il capitolo 5

Queste compaiono realmente in varie prove, **ma non appartengono alla parte da studiare fino al capitolo 5** del dispensario. Sono riportate per non confonderle con le domande prioritarie.

| Domanda / argomento | Capitolo del dispensario |
|---|---|
| Definizione di **dimensione** di uno spazio vettoriale e dimensione di $M_{m,n}(\mathbb{R})$ o $\mathbb{R}_d[x]$ | **6** (dimensione; §6.2) |
| Completamento di una base e estrazione di basi | **6** |
| Definizione di **funzione lineare**, nucleo, immagine e **teorema nullità più rango** | **7** |
| Distanza, norma e complemento ortogonale in uno **spazio vettoriale euclideo astratto** | **8** |
| Matrici ortogonali e loro determinante $\pm1$ | **8** |
| Autovalori, autovettori, diagonalizzabilità e teorema spettrale | **9** |

**Distinzione importante:** il *modulo e la proiezione di vettori geometrici* rientrano già nel **capitolo 1**; la trattazione degli *spazi euclidei astratti* è nel capitolo **8**. Analogamente, **la definizione di base** è già nel **capitolo 4**, mentre **la teoria generale della dimensione** è nel **capitolo 6**.

**Se il programma effettivo dell'esame è più ampio dei capitoli 1–5**, aggiungere anche questi argomenti e verificarne il peso negli appelli: non vanno ignorati in un esame completo.

---

## 10. Piano di ripasso e simulazione

### Priorità consigliata

1. **Prima fascia:** indipendenza/dipendenza, sottospazi, generatori, basi, Rouché-Capelli.
2. **Seconda fascia:** prodotto scalare, proiezioni, normalizzazione, matrici a scalini, invertibilità e rango.
3. **Terza fascia (obbligatoria perché è nel programma):** definizione di determinante, Laplace, Binet, operazioni elementari, equivalenza determinante–rango–invertibilità, Cramer, cofattori, prodotto vettoriale e misto.
4. **Ripasso di geometria:** rette, piani e distanze, soprattutto se la prova contiene anche quesiti a crocette o esercizi geometrici.

### Mini simulazione di teoria (soltanto capitoli 1–5)

1. Enunciare **Rouché-Capelli** e costruire un sistema incompatibile di due equazioni in tre incognite.
2. Definire **sottospazio vettoriale** e proporre una retta e un piano passanti per l'origine come esempi in $\mathbb{R}^3$.
3. Definire **indipendenza lineare** e fornire due insiemi di tre vettori, uno dipendente e uno indipendente.
4. Distinguere **base**, **sistema di generatori** e **insieme indipendente** con esempi.
5. Derivare la **formula della proiezione ortogonale** su un vettore non nullo e applicarla.
6. Dare la definizione di **matrice invertibile** e spiegare il rapporto con rango e determinante.
7. Enunciare **Binet** e dedurre $\det(A^{-1})=1/\det(A)$.
8. Spiegare come il determinante cambia sotto le **tre operazioni elementari** sulle righe.
9. Enunciare il **teorema di Cramer** con un sistema $2\times2$.
10. Definire **prodotto vettoriale e misto** e spiegare come ricavare area e volume.

### Metodo per rispondere bene

Per ogni domanda aperta prepara una risposta di **tre passaggi**:

1. **Definizione o enunciato preciso**, comprese le ipotesi (ad esempio $A$ quadrata, $\det(A)\neq0$, $\mathbf{w}\neq\mathbf{0}$).
2. **Spiegazione o dimostrazione breve**, quando richiesta.
3. **Esempio numerico verificato**, preferibilmente con coordinate, vettori o matrici di ordine 2–3.

---

**Conclusione:** sulla base delle domande osservate, i temi più ricorrenti **entro il capitolo 5** sono indipendenza lineare, sottospazi, generatori e basi, Rouché-Capelli, prodotto scalare/proiezioni e matrici invertibili. **Binet e il criterio determinante–rango–invertibilità** sono le richieste specifiche sul determinante rilevate negli appelli recenti. I teoremi di Laplace e Cramer e le altre applicazioni del capitolo 5 sono inclusi qui come **preparazione completa**, non perché risultino tra le domande autonome più frequenti.
