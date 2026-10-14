# Appunti di Geometria e Algebra Lineare

**Dispensa:** *Geometria e Algebra Lineare*, Elisa Postinghel  
**Capitolo iniziale:** 4 — Spazi vettoriali (pp. 86–107 del PDF, numerazione stampata)

> Documento incrementale. Qui aggiungeremo spiegazioni, esempi e chiarimenti su richiesta, mantenendo sempre lo stesso nome.

## 4.1 — Spazi vettoriali reali (p. 86)

**Definizione:** Uno spazio vettoriale è un insieme dotato delle operazioni di somma e di prodotto di un elemento per uno scalare.

In uno **spazio vettoriale reale** gli scalari sono numeri reali. Le operazioni devono soddisfare le otto proprietà della Definizione 37 (commutatività e associatività della somma, vettore nullo, opposto, proprietà del prodotto per uno scalare e distributività).

Esempi della dispensa: vettori geometrici, $\mathbb R^n$, matrici $M_{m\times n}(\mathbb R)$, polinomi.

### Che cosa si intende per «vettore»?

Il termine **vettore**, nel suo significato più generale, indica **un elemento di uno spazio vettoriale**. Non va confuso con alcuni suoi casi particolari:

- **Vettore geometrico:** una classe di equivalenza di segmenti orientati.
- **Vettore riga:** una matrice formata da una sola riga.
- **Vettore colonna:** una matrice formata da una sola colonna.

**Attenzione:** questi oggetti non sono sinonimi. La nozione più generale è quella di *vettore come elemento di uno spazio vettoriale*; gli altri sono esempi particolari.

In particolare:

- L'insieme $V^3$ dei **vettori geometrici**, introdotto nel Capitolo 1, è uno spazio vettoriale.
- L'insieme $M_{m\times n}(\mathbb R)$ delle **matrici $m\times n$ a coefficienti reali** è anch'esso uno spazio vettoriale.


## 4.2 — Combinazioni lineari (p. 88)

Una **combinazione lineare** dei vettori $v_1,\ldots,v_k$ è

$
v=\lambda_1v_1+\cdots+\lambda_kv_k.
$

I numeri $\lambda_i$ sono i **coefficienti** o **scalari** (informalmente, i «pesi»).

### 4.2.1 — Forma matriciale (p. 89)

Disponiamo i vettori **nelle colonne** di una matrice:

$
A=[v_1\mid v_2\mid\cdots\mid v_k].
$

Raccogliamo i coefficienti nel **vettore colonna**:

$
\underline{\lambda}=
\begin{pmatrix}
\lambda_1\\
\lambda_2\\
\vdots\\
\lambda_k
\end{pmatrix}.
$

In questo modo, la combinazione lineare diventa $A\underline{\lambda}=v$.

**Chiarimento discusso:** $\underline{\lambda}$ non contiene i vettori originali: contiene soltanto i pesi. Se $A$ ha quattro colonne, $\underline{\lambda}$ ha quattro coefficienti.

## 4.3 — Sottospazi vettoriali e generatori (p. 89)

### 4.3.1 — Sottospazi vettoriali

Un sottoinsieme non vuoto $U\subseteq V$ è un **sottospazio vettoriale** se è chiuso per somma e prodotto per scalare. In modo equivalente, per ogni $u_1,u_2\in U$ e $\lambda_1,\lambda_2\in\mathbb R$,

$
\lambda_1u_1+\lambda_2u_2\in U.
$

Ogni sottospazio deve contenere il **vettore nullo**.

### 4.3.2 — Generatori (p. 92)

Lo **spazio generato** da $v_1,\ldots,v_k$ contiene tutte le loro combinazioni lineari:

$
\operatorname{Span}(v_1,\ldots,v_k)=
\{\lambda_1v_1+\cdots+\lambda_kv_k:\lambda_i\in\mathbb R\}.
$

Un insieme è un **sistema di generatori** di $V$ se il suo span coincide con $V$.

Per vettori in $\mathbb R^n$, scritti nelle colonne di $A$:

- $v$ appartiene allo spazio generato se il sistema $A\underline{\lambda}=v$ è **compatibile**.
- I vettori generano **tutto $\mathbb R^n$** se e solo se $\operatorname{rg}(A)=n$, dove $n$ è il numero delle **righe**.

## 4.4 — Insiemi linearmente dipendenti e indipendenti (p. 95)

Consideriamo la combinazione lineare che dà il **vettore nullo**:

$
\lambda_1v_1+\cdots+\lambda_kv_k=0
\qquad\Longleftrightarrow\qquad
A\underline{\lambda}=0.
$

- **Linearmente indipendenti:** l'unica soluzione è $\lambda_1=\cdots=\lambda_k=0$.
- **Linearmente dipendenti:** esiste una soluzione con coefficienti **non tutti nulli**.

**Chiarimento discusso:** scegliendo tutti i pesi uguali a zero si ottiene sempre il vettore nullo. Questo non prova la dipendenza. La dipendenza esiste quando si può ottenere zero con *almeno un coefficiente non nullo*.

Se un insieme è dipendente, almeno uno dei suoi vettori è combinazione lineare degli altri e può essere eliminato senza modificare lo spazio generato.

**Esempio:**

$
v_1=(1,0),\quad v_2=(0,1),\quad v_3=(1,1).
$

Siccome $v_1+v_2-v_3=0$, con pesi $1,1,-1$ non tutti nulli, i tre vettori sono **dipendenti**.

### 4.4.1 — Indipendenza lineare e rango (pp. 97–98)

Se $A$ ha come colonne i **$k$ vettori** che stiamo studiando, allora

$
\boxed{\text{vettori indipendenti}\iff\operatorname{rg}(A)=k}.
$

Se il rango è minore del numero delle colonne, i vettori sono dipendenti.

**Non confondere i due confronti:**

- **Indipendenza:** rango uguale al **numero di colonne**.
- **Generatori di tutto $\mathbb R^n$:** rango uguale al **numero di righe**.

**Colonne con pivot:** quando riduciamo $A$ con Gauss, le posizioni dei pivot ci indicano quali colonne della **matrice originale** formano un insieme indipendente. Una colonna senza pivot corrisponde a un vettore che si può ricavare come combinazione lineare dei vettori nelle colonne con pivot.

**Esempio 61–62 della dispensa:**

$
v_1=(1,2,-1,0),\quad
v_2=(0,1,1,3),\quad
v_3=(-1,0,3,6).
$

La matrice ha rango 2, inferiore alle 3 colonne. I vettori sono dipendenti e

$
v_3=-v_1+2v_2.
$

## 4.5 — Basi (p. 99)

Una **base** di uno spazio vettoriale è un insieme di vettori che:

1. **genera** lo spazio;
2. è **linearmente indipendente**.

Una base permette dunque di generare tutto lo spazio **senza vettori ridondanti**.

### 4.5.1 — Basi di $\mathbb R^n$

Per essere una base di $\mathbb R^n$, un insieme deve avere $n$ vettori e la matrice corrispondente deve avere rango $n$.

La **base canonica** è formata dai vettori con un solo 1 e tutte le altre componenti uguali a 0.

Ogni vettore dello spazio si esprime **in maniera unica** come combinazione lineare dei vettori di una base.

## 4.6 — Esercizi ricapitolativi (p. 101)

*Spazio riservato agli esercizi e alle correzioni che decideremo di aggiungere.*

---

## Appunti personali e chiarimenti successivi

*Questa sezione verrà aggiornata di volta in volta, senza creare nuovi file.*
