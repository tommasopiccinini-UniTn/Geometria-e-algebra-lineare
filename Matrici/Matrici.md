# Capitolo 3 — Matrici

**Riferimento:** Elisa Postinghel, *Geometria e Algebra Lineare*, Capitolo 3, pp. 62–85 della dispensa (pp. 63–86 del PDF).  
**Obiettivo:** saper operare con le matrici, riconoscere quelle invertibili, calcolarne l'inversa e descrivere le soluzioni dei sistemi lineari.  
**Prerequisito:** [Capitolo 2 — Sistemi lineari](../Sistemi%20lineari/Sistemi%20lineari.md).  
**Collegamento:** [Capitolo 4 — Spazi vettoriali](../Spazi%20vettoriali/Spazi%20vettoriali.md).

> Il file segue le sezioni 3.1–3.4 della dispensa. I paragrafi di approfondimento esplicitano i calcoli e collegano i risultati agli esercizi. Alcuni refusi tipografici della dispensa sono segnalati quando cambiano il risultato matematico.

## Indice

- [3.1 — Matrici e operazioni (pp. 62–67)](#indice-cap3-1)
  - [3.1.1 — Notazione e tipi di matrici](#indice-cap3-2)
  - [3.1.2 — Somma, opposto e prodotto per uno scalare (pp. 64–65)](#indice-cap3-3)
  - [3.1.3 — Prodotto righe per colonne (pp. 65–67)](#indice-cap3-4)
    - [Procedura operativa](#indice-cap3-5)
    - [Proprietà del prodotto di matrici](#indice-cap3-6)
    - [Il prodotto non è commutativo](#indice-cap3-7)
    - [Un prodotto nullo non significa un fattore nullo](#indice-cap3-8)
- [3.2 — Invertibilità delle matrici quadrate (pp. 68–75)](#indice-cap3-9)
  - [3.2.1 — Diagonale, inverse, esempi (pp. 68–70)](#indice-cap3-10)
  - [3.2.2 — Matrici delle operazioni elementari (pp. 70–72)](#indice-cap3-11)
  - [3.2.3 — Teorema: rango e invertibilità (pp. 72–73)](#indice-cap3-12)
  - [3.2.4 — Calcolo dell'inversa con Gauss–Jordan (pp. 73–75)](#indice-cap3-13)
    - [Esempio 40 della dispensa — Inversa di una 2×2 (pp. 73–74)](#indice-cap3-14)
    - [Esempio 41 della dispensa — Una 3×3 (p. 74)](#indice-cap3-15)
    - [Esempio 42 della dispensa — Matrice non invertibile (p. 75)](#indice-cap3-16)
- [3.3 — Sistemi lineari e invertibilità (pp. 75–79)](#indice-cap3-17)
  - [3.3.1 — Scrittura matriciale di un sistema](#indice-cap3-18)
  - [3.3.2 — Sistemi omogenei, nucleo e nullità (pp. 76–77)](#indice-cap3-19)
  - [3.3.3 — Soluzioni di un sistema compatibile non omogeneo (pp. 77–79)](#indice-cap3-20)
    - [Esempio 43 della dispensa (p. 78)](#indice-cap3-21)
  - [3.3.4 — Sistema quadrato con matrice invertibile (p. 79)](#indice-cap3-22)
    - [Esempio 44 della dispensa (p. 79)](#indice-cap3-23)
- [3.4 — Esercizi ricapitolativi (pp. 80–85)](#indice-cap3-24)
  - [Esercizio 11 della dispensa — Matrice dipendente da k (pp. 80–83)](#indice-cap3-25)
  - [Esercizio 12 della dispensa — Invertibilità, inversa e sistema (pp. 80–84)](#indice-cap3-26)
  - [Esercizio aggiuntivo — Una matrice quadrata senza inversa](#indice-cap3-27)
  - [Domande di teoria per l'esame (p. 85)](#indice-cap3-28)
- [Schema finale per gli esercizi](#indice-cap3-29)
- [Formulario essenziale](#indice-cap3-30)

---

<a name="indice-cap3-1"></a>

## 3.1 — Matrici e operazioni (pp. 62–67)

<a name="indice-cap3-2"></a>

### 3.1.1 — Notazione e tipi di matrici

**Definizione 23 — Matrice.** Una matrice reale di ordine $m\times n$ è una tabella rettangolare di $m$ **righe** e $n$ **colonne**:

$$
A=(a_{ij})=
\begin{pmatrix}
a_{11}&a_{12}&\cdots&a_{1n}\\
a_{21}&a_{22}&\cdots&a_{2n}\\
\vdots&\vdots&\ddots&\vdots\\
a_{m1}&a_{m2}&\cdots&a_{mn}
\end{pmatrix}.
$$

Scriviamo $A\in M_{m\times n}(\mathbb R)$: l'elemento $a_{ij}$ occupa la **riga $i$** e la **colonna $j$**.

**Esempio:**

$$
A=\begin{pmatrix}
1&2&-1\\
0&3&4
\end{pmatrix}\in M_{2\times3}(\mathbb R),
$$

perché ha due righe e tre colonne; $a_{23}=4$.

**Definizione 24 — Tipi particolari:**

- **Matrice quadrata:** $m=n$, quindi $A\in M_n(\mathbb R)$.
- **Matrice riga:** una sola riga, ordine $1\times n$.
- **Matrice colonna:** una sola colonna, ordine $m\times1$.

**Nota:** nel testo della definizione 24 della dispensa (pp. 62–63) le condizioni per «matrice riga» e «matrice colonna» risultano scambiate: la forma scritta delle matrici chiarisce che l'orientamento corretto è quello riportato qui.

**Definizione 25 — Matrice nulla:** $O_{m\times n}$ ha tutti i coefficienti uguali a $0$.

**Definizione 26 — Matrice identità:** $I_n$ è quadrata, con $1$ sulla diagonale principale e $0$ altrove:

$$
I_3=\begin{pmatrix}1&0&0\\0&1&0\\0&0&1\end{pmatrix}.
$$

**Definizione 27 — Trasposta.** La trasposta $A^T$ si ottiene scambiando righe e colonne:

$$
\boxed{(A^T)_{ij}=a_{ji}}.
$$

Se $A$ è $m\times n$, allora $A^T$ è $n\times m$.

**Esempio:**

$$
A=\begin{pmatrix}1&2&3\\4&5&6\end{pmatrix}
\quad\Longrightarrow\quad
A^T=\begin{pmatrix}1&4\\2&5\\3&6\end{pmatrix}.
$$

Una matrice quadrata è **simmetrica** quando $A=A^T$.

**Esempio 26 della dispensa (p. 63):**

$$
\begin{pmatrix}1&2\\2&4\end{pmatrix}
$$

è simmetrica, mentre $\begin{pmatrix}1&2\\3&4\end{pmatrix}$ non lo è.

**Approfondimento — Proprietà della trasposta:**

$$
(A^T)^T=A,\qquad(A+B)^T=A^T+B^T,\qquad
(\lambda A)^T=\lambda A^T.
$$

Se il prodotto è definito, vale inoltre

$$
\boxed{(AB)^T=B^TA^T}.
$$

**Attenzione all'ordine:** nella trasposta di un prodotto, l'ordine dei fattori si **inverte**.

<a name="indice-cap3-3"></a>

### 3.1.2 — Somma, opposto e prodotto per uno scalare (pp. 64–65)

**Definizione 28 — Somma.** Due matrici si possono sommare **solo se hanno lo stesso ordine**:

$$
(A+B)_{ij}=a_{ij}+b_{ij}.
$$

**Esempio 27 della dispensa (p. 64):**

$$
\begin{pmatrix}1&2&3\\3&4&5\end{pmatrix}
+
\begin{pmatrix}1&-2&0\\2&4&-1\end{pmatrix}
=
\boxed{\begin{pmatrix}2&0&3\\5&8&4\end{pmatrix}}.
$$

**Definizione 29 — Opposto.** La matrice $-A$ si ottiene cambiando di segno **ogni coefficiente**:

$$
(-A)_{ij}=-a_{ij},\qquad A+(-A)=O.
$$

**Definizione 30 — Prodotto per uno scalare.** Per $\lambda\in\mathbb R$:

$$
(\lambda A)_{ij}=\lambda a_{ij}.
$$

Per esempio:

$$
3\begin{pmatrix}1&-2\\0&4\end{pmatrix}
=\begin{pmatrix}3&-6\\0&12\end{pmatrix}.
$$

Le operazioni godono delle proprietà:

$$
A+B=B+A,\qquad (A+B)+C=A+(B+C),
$$

$$
A+O=A,\qquad A+(-A)=O,
$$

$$
\lambda(\mu A)=(\lambda\mu)A,\qquad 1A=A,
$$

$$
(\lambda+\mu)A=\lambda A+\mu A,\qquad
\lambda(A+B)=\lambda A+\lambda B.
$$

**Definizione 31 — Combinazione lineare di matrici.** Se $A$ e $B$ hanno lo stesso ordine e $\lambda,\mu\in\mathbb R$, allora $\lambda A+\mu B$ è una combinazione lineare.

**Collegamento al Capitolo 4:** l'insieme delle matrici $M_{m\times n}(\mathbb R)$ è uno **spazio vettoriale** proprio perché somma e prodotto per scalari soddisfano gli assiomi richiesti.

<a name="indice-cap3-4"></a>

### 3.1.3 — Prodotto righe per colonne (pp. 65–67)

**Definizione 32 — Conformabilità.** Si può calcolare $AB$ solo quando il numero di **colonne di $A$** è uguale al numero di **righe di $B$**:

$$
\underbrace{A}_{m\times n}\;
\underbrace{B}_{n\times q}
=\underbrace{AB}_{m\times q}.
$$

**Regola fondamentale:** coincidono le **dimensioni interne**; il risultato ha le **dimensioni esterne**.

**Definizione 33 — Elementi del prodotto.** Se $C=AB$, allora

$$
\boxed{c_{ik}=\sum_{j=1}^{n}a_{ij}b_{jk}}.
$$

L'elemento $(i,k)$ è il prodotto scalare della **riga $i$** della prima matrice con la **colonna $k$** della seconda.

<a name="indice-cap3-5"></a>

#### Procedura operativa

1. Controllare le dimensioni prima di calcolare.
2. Selezionare una riga di $A$.
3. Selezionare una colonna di $B$.
4. Moltiplicare gli elementi corrispondenti e sommare.
5. Ripetere per tutte le posizioni della matrice risultato.

**Esempio 30 della dispensa (p. 66, con calcolo verificato).**

$$
A=\begin{pmatrix}1&2\\2&4\end{pmatrix},\qquad
B=\begin{pmatrix}1&-2&0\\2&4&-1\end{pmatrix}.
$$

$A$ è $2\times2$ e $B$ è $2\times3$: $AB$ è definito e sarà $2\times3$.

Calcoliamo i sei elementi:

$$
AB=\begin{pmatrix}
1\cdot1+2\cdot2 & 1\cdot(-2)+2\cdot4 & 1\cdot0+2\cdot(-1)\\
2\cdot1+4\cdot2 & 2\cdot(-2)+4\cdot4 & 2\cdot0+4\cdot(-1)
\end{pmatrix}.
$$

$$
\boxed{AB=\begin{pmatrix}5&6&-2\\10&12&-4\end{pmatrix}}.
$$

**Nota sul testo:** nell'Esempio 30 stampato sono riportati, in alcuni passaggi, coefficienti incompatibili con le matrici iniziali. Qui il prodotto è stato ricalcolato usando esattamente $A$ e $B$ come mostrate. Il prodotto $BA$ **non è definito**: le dimensioni interne sarebbero $3$ e $2$.

<a name="indice-cap3-6"></a>

#### Proprietà del prodotto di matrici

Quando le dimensioni lo permettono:

$$
(AB)C=A(BC)\qquad\text{(associatività)},
$$

$$
(A+B)C=AC+BC,\qquad C(A+B)=CA+CB
\qquad\text{(distributività)},
$$

$$
\lambda(AB)=(\lambda A)B=A(\lambda B).
$$

Se $A$ è $m\times n$:

$$
\boxed{I_mA=A=AI_n}.
$$

**Attenzione:** l'identità a sinistra è di ordine $m$, quella a destra è di ordine $n$.

<a name="indice-cap3-7"></a>

#### Il prodotto non è commutativo

**Osservazione 7.** In generale

$$
\boxed{AB\ne BA}.
$$

Anche se entrambi i prodotti esistono, possono essere diversi.

**Esempio 31 della dispensa (p. 67):**

$$
A=\begin{pmatrix}1&2\\-1&3\end{pmatrix},\qquad
B=\begin{pmatrix}2&1\\0&0\end{pmatrix}.
$$

$$
AB=\begin{pmatrix}2&1\\-2&-1\end{pmatrix},\qquad
BA=\begin{pmatrix}1&7\\0&0\end{pmatrix}.
$$

<a name="indice-cap3-8"></a>

#### Un prodotto nullo non significa un fattore nullo

**Osservazione 8.** È possibile che $AB=O$ con $A\ne O$ e $B\ne O$.

**Esempio 33 della dispensa (p. 67):**

$$
A=\begin{pmatrix}0&1\\0&1\end{pmatrix},\qquad
B=\begin{pmatrix}1&1\\0&0\end{pmatrix},
\qquad AB=O_{2\times2}.
$$

**Errore frequente:** non si può applicare alle matrici la regola numerica «$ab=0$ implica $a=0$ oppure $b=0$».

<a name="indice-cap3-9"></a>

## 3.2 — Invertibilità delle matrici quadrate (pp. 68–75)

<a name="indice-cap3-10"></a>

### 3.2.1 — Diagonale, inverse, esempi (pp. 68–70)

**Definizione 34 — Diagonale principale.** In una matrice quadrata $A\in M_n(\mathbb R)$, la diagonale principale è costituita dagli elementi $a_{11},a_{22},\ldots,a_{nn}$.

Una matrice è **diagonale** se tutti gli elementi *fuori* dalla diagonale sono nulli:

$$
D=\begin{pmatrix}
d_1&0&0\\
0&d_2&0\\
0&0&d_3
\end{pmatrix}.
$$

**Definizione 35 — Matrice invertibile.** Una matrice quadrata $A\in M_n(\mathbb R)$ è invertibile se esiste una matrice $A^{-1}$ tale che

$$
\boxed{AA^{-1}=A^{-1}A=I_n}.
$$

La matrice $A^{-1}$ è l'**inversa** di $A$.

**Osservazione 9.** L'inversa, se esiste, è **unica**. Infatti, se $B$ e $C$ fossero entrambe inverse di $A$, allora

$$
B=BI_n=B(AC)=(BA)C=I_nC=C.
$$

**Esempio elementare:** $I_n^{-1}=I_n$.

**Matrice diagonale:** è invertibile **se e solo se** tutti gli elementi diagonali sono diversi da zero:

$$
D=\operatorname{diag}(d_1,\ldots,d_n),
\quad d_i\ne0
\ \Longrightarrow\
D^{-1}=\operatorname{diag}\left(\frac1{d_1},\ldots,\frac1{d_n}\right).
$$

**Precisazione:** nella frase introduttiva dell'Esempio 36 (p. 69) si legge «Ogni matrice diagonale è invertibile». È necessario aggiungere la condizione **$d_i\ne0$ per tutti gli indici**: la matrice diagonale con uno zero sulla diagonale non è invertibile.

**Osservazione 10.** Una matrice quadrata con una **riga nulla** o una **colonna nulla** non può essere invertibile.

**Osservazione 11 — Inversa del prodotto.** Se $A$ e $B$ sono matrici quadrate invertibili dello stesso ordine, allora

$$
\boxed{(AB)^{-1}=B^{-1}A^{-1}}.
$$

**Approfondimento — Perché si inverte l'ordine?**

$$
(AB)(B^{-1}A^{-1})
=A(BB^{-1})A^{-1}
=AI_nA^{-1}=I_n.
$$

Non scrivere $(AB)^{-1}=A^{-1}B^{-1}$: in generale è falso perché le matrici **non commutano**.

<a name="indice-cap3-11"></a>

### 3.2.2 — Matrici delle operazioni elementari (pp. 70–72)

Le tre operazioni elementari sulle righe possono essere viste come **moltiplicazioni a sinistra** per particolari matrici quadrate.

Si parte dall'identità $I_m$ e si applica l'operazione desiderata.

- $S_{ij}$: scambia le righe $i$ e $j$.
- $D_i(\lambda)$: moltiplica la riga $i$ per $\lambda\ne0$.
- $E_{ij}(\mu)$: sostituisce $R_i$ con $R_i+\mu R_j$.

**Esempi $3\times3$ (domanda di teoria 3.4.4.3, p. 85):**

$$
S_{13}=\begin{pmatrix}
0&0&1\\
0&1&0\\
1&0&0
\end{pmatrix},
\qquad
D_2(5)=\begin{pmatrix}
1&0&0\\
0&5&0\\
0&0&1
\end{pmatrix},
$$

$$
E_{32}(-2)=\begin{pmatrix}
1&0&0\\
0&1&0\\
0&-2&1
\end{pmatrix}.
$$

**Perché $E_{32}(-2)$ funziona?** Moltiplicando $E_{32}(-2)A$, la nuova terza riga diventa $R_3-2R_2$; le altre restano invariate.

**Proposizione 6.** Esiste una matrice quadrata $P$, prodotto di matrici elementari, tale che

$$
\boxed{PA=\operatorname{rref}(A)}.
$$

**Proposizione 7.** Le matrici elementari sono invertibili. Le operazioni inverse sono:

$$
S_{ij}^{-1}=S_{ij},\qquad
D_i(\lambda)^{-1}=D_i\left(\frac1\lambda\right),\qquad
E_{ij}(\mu)^{-1}=E_{ij}(-\mu).
$$

**Collegamento concettuale:** Gauss non «cambia arbitrariamente» la matrice: a ogni passo moltiplica a sinistra per una matrice invertibile. Per questo il rango non cambia.

<a name="indice-cap3-12"></a>

### 3.2.3 — Teorema: rango e invertibilità (pp. 72–73)

**Teorema 3.2.3.1.** Una matrice quadrata $A\in M_n(\mathbb R)$ è invertibile **se e solo se** ha rango massimo $n$:

$$
\boxed{A\text{ invertibile}\iff\operatorname{rg}(A)=n}.
$$

In modo equivalente:

$$
\boxed{A\text{ invertibile}\iff\operatorname{rref}(A)=I_n}.
$$

**Interpretazione con i pivot:** una matrice $n\times n$ è invertibile se la riduzione per righe produce **$n$ pivot**, uno per ciascuna colonna e riga.

**Perché?** Dalla proposizione 6, $\operatorname{rref}(A)=PA$ con $P$ invertibile. Se la forma ridotta è $I_n$, allora $PA=I_n$, dunque $A=P^{-1}$. Viceversa il prodotto di matrici invertibili è invertibile, e una matrice ridotta per righe invertibile deve coincidere con $I_n$.

**Conseguenze utili:**

- Una matrice $n\times n$ di rango minore di $n$ **non ha inversa**.
- Una matrice con due righe uguali, proporzionali oppure una riga nulla **non può avere rango $n$**.
- Non è necessario calcolare tutta l'inversa per decidere se esiste: è sufficiente verificare i pivot.

<a name="indice-cap3-13"></a>

### 3.2.4 — Calcolo dell'inversa con Gauss–Jordan (pp. 73–75)

Il metodo della dispensa consiste nel costruire la matrice aumentata

$$
\boxed{(A\mid I_n)}.
$$

Poi si applicano **le stesse operazioni elementari a entrambe le metà**.

- Se si arriva a $(I_n\mid B)$, allora $A$ è invertibile e $\boxed{B=A^{-1}}$.
- Se la metà sinistra non si può ridurre a $I_n$, la matrice non è invertibile.

**Perché il metodo funziona?** Le operazioni applicate equivalgono alla moltiplicazione a sinistra per $P$. Quando $PA=I_n$, si ha $P=A^{-1}$; applicando le stesse operazioni a $I_n$, la metà destra diventa appunto $PI_n=P$.

<a name="indice-cap3-14"></a>

#### Esempio 40 della dispensa — Inversa di una $2\times2$ (pp. 73–74)

$$
A=\begin{pmatrix}1&2\\3&5\end{pmatrix}.
$$

Partiamo da:

$$
\left(\begin{array}{cc|cc}
1&2&1&0\\
3&5&0&1
\end{array}\right).
$$

Prima eliminazione:

$$
\xrightarrow{R_2\leftarrow R_2-3R_1}
\left(\begin{array}{cc|cc}
1&2&1&0\\
0&-1&-3&1
\end{array}\right).
$$

Normalizziamo il secondo pivot:

$$
\xrightarrow{R_2\leftarrow-R_2}
\left(\begin{array}{cc|cc}
1&2&1&0\\
0&1&3&-1
\end{array}\right).
$$

Eliminiamo sopra il secondo pivot:

$$
\xrightarrow{R_1\leftarrow R_1-2R_2}
\boxed{\left(\begin{array}{cc|cc}
1&0&-5&2\\
0&1&3&-1
\end{array}\right)}.
$$

La metà sinistra è $I_2$, quindi

$$
\boxed{A^{-1}=\begin{pmatrix}-5&2\\3&-1\end{pmatrix}}.
$$

**Verifica mediante il prodotto:**

$$
AA^{-1}
=\begin{pmatrix}1&2\\3&5\end{pmatrix}
\begin{pmatrix}-5&2\\3&-1\end{pmatrix}
=\begin{pmatrix}1&0\\0&1\end{pmatrix}.
$$

<a name="indice-cap3-15"></a>

#### Esempio 41 della dispensa — Una $3\times3$ (p. 74)

Per

$$
A=\begin{pmatrix}
1&2&0\\
0&1&-1\\
-1&1&2
\end{pmatrix},
$$

riducendo $(A\mid I_3)$ si ottiene

$$
\boxed{
A^{-1}=\frac15
\begin{pmatrix}
3&-4&-2\\
1&2&1\\
1&-3&1
\end{pmatrix}}.
$$

**Controllo consigliato:** moltiplicare la prima riga di $A$ per le tre colonne di $A^{-1}$: si ottiene $(1,0,0)$.

<a name="indice-cap3-16"></a>

#### Esempio 42 della dispensa — Matrice non invertibile (p. 75)

$$
A=\begin{pmatrix}
1&1&0\\
2&3&-1\\
0&-1&1
\end{pmatrix}.
$$

Nella riduzione la terza riga della parte $A$ diventa nulla; restano quindi **due pivot**, perciò $\operatorname{rg}(A)=2<3$. La matrice non è invertibile e il metodo non può produrre $(I_3\mid A^{-1})$.

<a name="indice-cap3-17"></a>

## 3.3 — Sistemi lineari e invertibilità (pp. 75–79)

<a name="indice-cap3-18"></a>

### 3.3.1 — Scrittura matriciale di un sistema

Dato $A\in M_{m\times n}(\mathbb R)$, un vettore delle incognite $\mathbf x\in\mathbb R^n$ e un vettore dei termini noti $\mathbf b\in\mathbb R^m$, il sistema si scrive

$$
\boxed{A\mathbf x=\mathbf b}.
$$

L'uguaglianza è equivalente alle $m$ equazioni lineari originarie, perché ogni riga di $A$ moltiplicata per la colonna $\mathbf x$ genera il membro sinistro di una equazione.

**Esempio:**

$$
\begin{pmatrix}
1&2&-1\\
2&0&3
\end{pmatrix}
\begin{pmatrix}x\\y\\z\end{pmatrix}
=
\begin{pmatrix}4\\5\end{pmatrix}
$$

corrisponde a

$$
\begin{cases}
x+2y-z=4,\\
2x+3z=5.
\end{cases}
$$

**Non confondere:** $A$ è la matrice dei coefficienti, $\mathbf x$ è la colonna delle incognite e $\mathbf b$ è la colonna dei termini noti.

<a name="indice-cap3-19"></a>

### 3.3.2 — Sistemi omogenei, nucleo e nullità (pp. 76–77)

Un sistema è **omogeneo** quando

$$
A\mathbf x=\mathbf0.
$$

**Proposizione 8.** L'insieme delle sue soluzioni è **chiuso** rispetto a somma e prodotto per scalare. Infatti, se $A\mathbf v=\mathbf0$ e $A\mathbf w=\mathbf0$:

$$
A(\mathbf v+\mathbf w)=A\mathbf v+A\mathbf w=\mathbf0,
$$

$$
A(\lambda\mathbf v)=\lambda A\mathbf v=\mathbf0.
$$

Dunque ogni combinazione lineare di soluzioni dell'omogeneo è ancora una soluzione.

**Definizione 36 — Nucleo.** L'insieme delle soluzioni del sistema omogeneo associato ad $A$ è il **nucleo** della matrice:

$$
\boxed{N(A)=\{\mathbf x\in\mathbb R^n:A\mathbf x=\mathbf0\}}.
$$

**Nullità:** il numero $\operatorname{null}(A)$ è il numero di colonne **senza pivot** nella forma ridotta per righe di $A$, ossia il numero di variabili libere del sistema omogeneo.

**Proposizione 9 — Relazione rango–nullità:**

$$
\boxed{\operatorname{null}(A)+\operatorname{rg}(A)=n},
$$

dove $n$ è il **numero di colonne di $A$**.

**Approfondimento — Significato:** su $n$ colonne, $\operatorname{rg}(A)$ sono colonne pivot e le restanti $n-\operatorname{rg}(A)$ corrispondono alle variabili libere. Questo risultato sarà generalizzato nel capitolo sulle funzioni lineari.

**Esempio:** se $A$ ha $4$ colonne e rango $2$, allora $\operatorname{null}(A)=4-2=2$: il sistema omogeneo ha due parametri liberi.

<a name="indice-cap3-20"></a>

### 3.3.3 — Soluzioni di un sistema compatibile non omogeneo (pp. 77–79)

Sia $A\mathbf x=\mathbf b$ compatibile e sia $\mathbf x_0$ una **soluzione particolare**, cioè $A\mathbf x_0=\mathbf b$.

Se $\mathbf v\in N(A)$, allora

$$
A(\mathbf x_0+\mathbf v)
=A\mathbf x_0+A\mathbf v
=\mathbf b+\mathbf0=\mathbf b.
$$

Viceversa, se $\mathbf x$ risolve il sistema completo, allora

$$
A(\mathbf x-\mathbf x_0)=\mathbf b-\mathbf b=\mathbf0,
$$

perciò $\mathbf x-\mathbf x_0\in N(A)$.

**Proposizione 10 — Tutte le soluzioni:**

$$
\boxed{\mathbf x=\mathbf x_0+\mathbf v,\qquad \mathbf v\in N(A)}.
$$

In notazione insiemistica, l'insieme delle soluzioni è

$$
\boxed{\mathbf x_0+N(A)}.
$$

**Da ricordare:** per un sistema non omogeneo compatibile, le soluzioni sono **una soluzione particolare più tutte le soluzioni dell'omogeneo associato**. Non è in generale un sottospazio, perché non contiene necessariamente lo zero.

<a name="indice-cap3-21"></a>

#### Esempio 43 della dispensa (p. 78)

Consideriamo

$$
\begin{cases}
x+z-w=5,\\
-y+z-2w=4,\\
2x+4y-2z+6w=-6.
\end{cases}
$$

La riduzione della matrice completa porta a rango $2$. Le variabili libere sono $z$ e $w$. Ponendo $z=s$ e $w=t$ si trova

$$
\begin{cases}
x=5-s+t,\\
y=-4+s-2t,\\
z=s,\\
w=t.
\end{cases}
$$

Separando la parte costante e i due parametri:

$$
\boxed{
\begin{pmatrix}x\\y\\z\\w\end{pmatrix}
=
\begin{pmatrix}5\\-4\\0\\0\end{pmatrix}
+s\begin{pmatrix}-1\\1\\1\\0\end{pmatrix}
+t\begin{pmatrix}1\\-2\\0\\1\end{pmatrix}}.
$$

**Interpretazione:**

- $(5,-4,0,0)$ è una soluzione particolare di $A\mathbf x=\mathbf b$.
- $(-1,1,1,0)$ e $(1,-2,0,1)$ sono soluzioni di $A\mathbf v=\mathbf0$.
- Variando $s,t$ si ottengono **tutte** le soluzioni del sistema.

**Collegamento con lo Span (Capitolo 4):**

$$
N(A)=\operatorname{Span}\bigl(
(-1,1,1,0),\ (1,-2,0,1)
\bigr).
$$

<a name="indice-cap3-22"></a>

### 3.3.4 — Sistema quadrato con matrice invertibile (p. 79)

**Proposizione 11.** Se $A\in M_n(\mathbb R)$ è invertibile, allora **per ogni** $\mathbf b\in\mathbb R^n$ il sistema

$$
A\mathbf x=\mathbf b
$$

ha una **sola soluzione**, data da

$$
\boxed{\mathbf x=A^{-1}\mathbf b}.
$$

**Dimostrazione:** moltiplicando a sinistra per $A^{-1}$:

$$
A^{-1}A\mathbf x=A^{-1}\mathbf b
\quad\Longrightarrow\quad
I_n\mathbf x=A^{-1}\mathbf b.
$$

**Attenzione:** il prodotto è $A^{-1}\mathbf b$ e **non** $\mathbf bA^{-1}$; quest'ultimo non è normalmente neppure definito per le dimensioni.

<a name="indice-cap3-23"></a>

#### Esempio 44 della dispensa (p. 79)

Il sistema è

$$
\begin{cases}
x+2y=1,\\
y-z=2,\\
-x+y+2z=2.
\end{cases}
$$

Poniamo

$$
A=\begin{pmatrix}1&2&0\\0&1&-1\\-1&1&2\end{pmatrix},
\qquad
\mathbf b=\begin{pmatrix}1\\2\\2\end{pmatrix}.
$$

Dall'Esempio 41 abbiamo

$$
A^{-1}=\frac15\begin{pmatrix}3&-4&-2\\1&2&1\\1&-3&1\end{pmatrix}.
$$

Moltiplichiamo **righe per colonna**:

$$
\mathbf x=A^{-1}\mathbf b
=\frac15\begin{pmatrix}
3-8-4\\
1+4+2\\
1-6+2
\end{pmatrix}
=
\boxed{\begin{pmatrix}-9/5\\7/5\\-3/5\end{pmatrix}}.
$$

**Verifica:** $-9/5+2(7/5)=1$; $7/5-(-3/5)=2$; $9/5+7/5-6/5=2$.

**Approfondimento — Equivalenze per una matrice quadrata:**

$$
\boxed{
\begin{aligned}
A\text{ invertibile}
&\iff\operatorname{rg}(A)=n\\
&\iff\operatorname{rref}(A)=I_n\\
&\iff A\mathbf x=\mathbf0\text{ ha solo }\mathbf x=\mathbf0\\
&\iff A\mathbf x=\mathbf b\text{ ha un'unica soluzione per ogni }\mathbf b.
\end{aligned}}
$$

Sono modi diversi di riconoscere la medesima proprietà.

<a name="indice-cap3-24"></a>

## 3.4 — Esercizi ricapitolativi (pp. 80–85)

<a name="indice-cap3-25"></a>

### Esercizio 11 della dispensa — Matrice dipendente da $k$ (pp. 80–83)

$$
A_k=\begin{pmatrix}
1&2&-3\\
-1&-2k&3\\
\frac14&\frac12&k
\end{pmatrix},\qquad k\in\mathbb R.
$$

**Punto 1 — Quando è invertibile?** Applichiamo le operazioni

$$
R_2\leftarrow R_2+R_1,\qquad
R_3\leftarrow R_3-\frac14R_1.
$$

Otteniamo

$$
A_k\ \longrightarrow\
\begin{pmatrix}
1&2&-3\\
0&2(1-k)&0\\
0&0&k+\frac34
\end{pmatrix}.
$$

Il primo pivot vale $1$. Gli altri due sono non nulli precisamente quando

$$
2(1-k)\ne0
\quad\text{e}\quad
k+\frac34\ne0.
$$

Quindi

$$
\boxed{A_k\text{ invertibile}\iff k\ne1,\quad k\ne-\frac34}.
$$

**Punto 2 — Calcolare $A_0^{-1}$.** Poiché $k=0$ soddisfa entrambe le condizioni, $A_0$ è invertibile. Con la riduzione di $(A_0\mid I_3)$ (svolta nella dispensa a pp. 82–83) si trova

$$
\boxed{
A_0^{-1}=
\begin{pmatrix}
-1&-1&4\\
\frac12&\frac12&0\\
-\frac13&0&\frac43
\end{pmatrix}}.
$$

**Controllo:** il prodotto $A_0A_0^{-1}$ restituisce $I_3$.

**Che cosa insegna l'esercizio:** se una matrice dipende da $k$, prima si studia il **rango al variare di $k$**, poi si calcola l'inversa solo per i valori ammessi.

<a name="indice-cap3-26"></a>

### Esercizio 12 della dispensa — Invertibilità, inversa e sistema (pp. 80–84)

$$
A_k=\begin{pmatrix}
1&1&k\\
2&3&k-1\\
1&4&1
\end{pmatrix}.
$$

**Punto 1 — Rango al variare di $k$.** Con

$$
R_2\leftarrow R_2-2R_1,\qquad
R_3\leftarrow R_3-R_1,
$$

si ottiene

$$
\begin{pmatrix}
1&1&k\\
0&1&-k-1\\
0&3&1-k
\end{pmatrix}.
$$

Poi $R_3\leftarrow R_3-3R_2$ dà

$$
\begin{pmatrix}
1&1&k\\
0&1&-k-1\\
0&0&2k+4
\end{pmatrix}.
$$

Pertanto

$$
\operatorname{rg}(A_k)=
\begin{cases}
2,&k=-2,\\
3,&k\ne-2.
\end{cases}
$$

e

$$
\boxed{A_k\text{ invertibile}\iff k\ne-2}.
$$

**Punto 2 — Inversa per $k=1$.** La matrice è

$$
A=A_1=\begin{pmatrix}1&1&1\\2&3&0\\1&4&1\end{pmatrix},
$$

con inversa

$$
\boxed{A^{-1}=\frac16
\begin{pmatrix}
3&3&-3\\
-2&0&2\\
5&-3&1
\end{pmatrix}}.
$$

**Punto 3 — Risolvere $A\mathbf x=\mathbf b$ con $\mathbf b=(1,-1,-2)^T$.** Basta usare il prodotto:

$$
\mathbf x=A^{-1}\mathbf b
=\frac16
\begin{pmatrix}
3-3+6\\
-2-4\\
5+3-2
\end{pmatrix}
=\boxed{\begin{pmatrix}1\\-1\\1\end{pmatrix}}.
$$

**Controllo:** $1-1+1=1$; $2-3=-1$; $1-4+1=-2$.

<a name="indice-cap3-27"></a>

### Esercizio aggiuntivo — Una matrice quadrata senza inversa

Consideriamo

$$
A=\begin{pmatrix}
1&2&3\\
2&4&6\\
0&1&1
\end{pmatrix}.
$$

La seconda riga è il doppio della prima, quindi con $R_2\leftarrow R_2-2R_1$ compare una riga nulla. Al massimo ci sono due pivot:

$$
\operatorname{rg}(A)<3
\quad\Longrightarrow\quad
\boxed{A\text{ non invertibile}}.
$$

**Non serve proseguire** con la ricerca di $A^{-1}$: il criterio del rango ha già risolto la domanda.

<a name="indice-cap3-28"></a>

### Domande di teoria per l'esame (p. 85)

1. Come è definito il prodotto di matrici? Quando due matrici sono conformabili?
2. Perché il prodotto di matrici, in generale, non è commutativo?
3. Che cosa sono matrice trasposta, identità e matrice simmetrica?
4. Che cosa significa che una matrice è invertibile?
5. Qual è la relazione tra invertibilità, rango e $\operatorname{rref}(A)$?
6. Come si costruisce la matrice associata a un'operazione elementare?
7. Come si calcola un'inversa usando $(A\mid I_n)$?
8. Come si descrive il nucleo $N(A)$?
9. Qual è la relazione tra rango e nullità?
10. Come si descrivono tutte le soluzioni di un sistema compatibile non omogeneo?

<a name="indice-cap3-29"></a>

## Schema finale per gli esercizi

| Richiesta | Controllo fondamentale | Metodo |
|---|---|---|
| Somma di matrici | Stesso numero di righe e colonne | Elemento per elemento |
| Prodotto $AB$ | Colonne di $A$ = righe di $B$ | Righe per colonne |
| Verificare $A$ invertibile | $A$ deve essere quadrata | $\operatorname{rg}(A)=n$ |
| Calcolare $A^{-1}$ | Devono esserci $n$ pivot | Ridurre $(A\mid I_n)$ |
| Studiare $A_k$ | Individuare i pivot dipendenti da $k$ | Separare i valori che li annullano |
| Risolvere $A\mathbf x=\mathbf b$ | Compatibilità; se $A$ invertibile, soluzione unica | Gauss oppure $A^{-1}\mathbf b$ |
| Descrivere tutte le soluzioni | Trovare una soluzione particolare e il nucleo | $\mathbf x_0+N(A)$ |

<a name="indice-cap3-30"></a>

## Formulario essenziale

$$
\begin{aligned}
(AB)_{ik}&=\sum_{j=1}^{n}a_{ij}b_{jk},\\
I_mA&=A=AI_n\quad(A\in M_{m\times n}),\\
AA^{-1}&=A^{-1}A=I_n,\\
(AB)^{-1}&=B^{-1}A^{-1},\\
A\text{ invertibile}&\iff\operatorname{rg}(A)=n
\iff\operatorname{rref}(A)=I_n,\\
N(A)&=\{\mathbf x:A\mathbf x=\mathbf0\},\\
\operatorname{null}(A)+\operatorname{rg}(A)&=n,\\
\{\mathbf x:A\mathbf x=\mathbf b\}&=\mathbf x_0+N(A)
\quad(\text{se compatibile}),\\
\mathbf x&=A^{-1}\mathbf b\quad(\text{se }A\text{ invertibile}).
\end{aligned}
$$

**Collegamento al Capitolo 4:** le matrici costituiscono uno spazio vettoriale, i sistemi omogenei descrivono sottospazi e il rango permette di studiare generatori e indipendenza lineare.
