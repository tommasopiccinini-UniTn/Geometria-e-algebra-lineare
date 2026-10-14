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

$$v=\lambda_1v_1+\cdots+\lambda_kv_k.$$

I numeri $\lambda_i$ sono i **coefficienti** o **scalari** (informalmente, i «pesi»).

### 4.2.1 — Forma matriciale (p. 89)

Disponiamo i vettori **nelle colonne** di una matrice:

$$A=[v_1\mid v_2\mid\cdots\mid v_k].$$

Raccogliamo i coefficienti nel **vettore colonna**:

$$\underline{\lambda}= \begin{pmatrix} \lambda_1\\ \lambda_2\\ \vdots\\ \lambda_k \end{pmatrix}.$$

In questo modo, la combinazione lineare diventa $A\underline{\lambda}=v$.

**Chiarimento discusso:** $\underline{\lambda}$ non contiene i vettori originali: contiene soltanto i pesi. Se $A$ ha quattro colonne, $\underline{\lambda}$ ha quattro coefficienti.

## 4.3 — Sottospazi vettoriali e generatori (p. 89)

### 4.3.1 — Sottospazi vettoriali

Un sottoinsieme non vuoto $U\subseteq V$ è un **sottospazio vettoriale** se è chiuso per somma e prodotto per scalare. In modo equivalente, per ogni $u_1,u_2\in U$ e $\lambda_1,\lambda_2\in\mathbb R$,

$$\lambda_1u_1+\lambda_2u_2\in U.$$

Ogni sottospazio deve contenere il **vettore nullo** di $V$, indicato con $0_V$. Questo vale per ogni sottospazio $U\subseteq V$, ma **non** per un sottoinsieme qualsiasi di $V$.

**Test del vettore nullo (condizione necessaria).** Se $U\subseteq\mathbb{R}^n$ **non contiene il vettore nullo**, allora **non è un sottospazio vettoriale**. Infatti, se $U$ è un sottospazio e $v\in U$, per la chiusura rispetto al prodotto per uno scalare deve valere

$$0\cdot v=\mathbf{0}\in U.$$

**Attenzione:** contenere il vettore nullo è **necessario, ma non sufficiente** per essere un sottospazio. Se $\mathbf{0}\in U$, bisogna comunque verificare anche la **chiusura rispetto alla somma** e la **chiusura rispetto al prodotto per uno scalare**.


**Numero di elementi di un sottospazio vettoriale reale.** Un sottospazio $U$ può avere:

- **Un solo elemento:** in questo caso è necessariamente il vettore nullo, quindi $U=\{0_V\}$. Questo insieme è detto **sottospazio nullo**.
- **Infiniti elementi:** se $U$ contiene almeno un vettore non nullo $v$, per la chiusura rispetto al prodotto per uno scalare contiene anche tutti i vettori $\lambda v$, al variare di $\lambda\in\mathbb{R}$; essi sono infiniti e distinti.

**Conclusione:** un sottospazio vettoriale reale ha **un solo elemento (lo zero) oppure infiniti elementi**. Non può avere un numero finito di elementi maggiore di uno.

### 4.3.2 — Generatori (p. 92)

Lo **spazio generato** da $v_1,\ldots,v_k$ contiene tutte le loro combinazioni lineari:

$$\mathrm{Span}(v_1,\ldots,v_k)= \{\lambda_1v_1+\cdots+\lambda_kv_k:\lambda_i\in\mathbb R\}.$$

Un insieme è un **sistema di generatori** di $V$ se il suo span coincide con $V$.

### Significato dello Span

**Span** significa **spazio generato**: è l'insieme di **tutti** i vettori ottenibili facendo combinazioni lineari dei vettori di partenza, non soltanto l'insieme dei vettori iniziali.

Per esempio, dati due vettori $v_1$ e $v_2$:

$$\mathrm{Span}(v_1,v_2) =\{\lambda_1v_1+\lambda_2v_2\mid \lambda_1,\lambda_2\in\mathbb{R}\}.$$

I coefficienti $\lambda_1$ e $\lambda_2$ possono assumere **qualsiasi valore reale**.

**Esempio in $\mathbb{R}^2$.** Prendiamo $v_1=(1,0)$ e $v_2=(0,1)$. Ogni combinazione lineare è

$$\lambda_1(1,0)+\lambda_2(0,1) =(\lambda_1,\lambda_2).$$

Poiché $\lambda_1$ e $\lambda_2$ possono essere qualsiasi numero reale, si ottiene ogni vettore del piano:

$$\boxed{\mathrm{Span}(v_1,v_2)=\mathbb{R}^2}.$$

### Interpretazione geometrica

**1. Un solo vettore non nullo:** il suo Span è la **retta passante per l'origine** nella direzione del vettore.

![Schema: lo Span di un vettore non nullo è una retta passante per l'origine](immagini/span_retta.svg)

**2. Due vettori linearmente indipendenti in $\mathbb{R}^2$:** il loro Span è **l'intero piano $\mathbb{R}^2$**.

![Schema: due vettori indipendenti generano tutto il piano](immagini/span_piano.svg)

**Collegamento con le matrici.** Se $A$ ha per colonne i vettori $v_1,\ldots,v_k$, allora

$$v\in\mathrm{Span}(v_1,\ldots,v_k) \quad\Longleftrightarrow\quad A\underline{\lambda}=v \ \text{ammette almeno una soluzione}.$$

I coefficienti cercati sono le componenti del vettore colonna $\underline{\lambda}$.


Per vettori in $\mathbb R^n$, scritti nelle colonne di $A$:

- $v$ appartiene allo spazio generato se il sistema $A\underline{\lambda}=v$ è **compatibile**.
- I vettori generano **tutto $\mathbb R^n$** se e solo se $\mathrm{rg}(A)=n$, dove $n$ è il numero delle **righe**.

## 4.4 — Insiemi linearmente dipendenti e indipendenti (p. 95)

Consideriamo la combinazione lineare che dà il **vettore nullo**:

$$\lambda_1v_1+\cdots+\lambda_kv_k=0 \qquad\Longleftrightarrow\qquad A\underline{\lambda}=0.$$

- **Linearmente indipendenti:** l'unica soluzione è $\lambda_1=\cdots=\lambda_k=0$.
- **Linearmente dipendenti:** esiste una soluzione con coefficienti **non tutti nulli**.

**Chiarimento discusso:** scegliendo tutti i pesi uguali a zero si ottiene sempre il vettore nullo. Questo non prova la dipendenza. La dipendenza esiste quando si può ottenere zero con *almeno un coefficiente non nullo*.

Se un insieme è dipendente, almeno uno dei suoi vettori è combinazione lineare degli altri e può essere eliminato senza modificare lo spazio generato.

**Proprietà — Insiemi che contengono il vettore nullo.** L'insieme formato dal solo vettore nullo, $\{\mathbf{0}\}\subseteq V$, è **linearmente dipendente**. Infatti, $1\cdot\mathbf{0}=\mathbf{0}$: otteniamo il vettore nullo con un coefficiente **non nullo** (uguale a $1$).

Più in generale, **qualsiasi insieme di vettori che contiene il vettore nullo è linearmente dipendente**: basta scegliere coefficiente $1$ per il vettore nullo e coefficiente $0$ per tutti gli altri vettori.

**Attenzione:** il fatto che $\{\mathbf{0}\}$ sia un **sottospazio vettoriale** non significa che sia un insieme linearmente indipendente. Sono proprietà diverse.


**Esempio:**

$$v_1=(1,0),\quad v_2=(0,1),\quad v_3=(1,1).$$

Siccome $v_1+v_2-v_3=0$, con pesi $1,1,-1$ non tutti nulli, i tre vettori sono **dipendenti**.

### Esempio 60 — Indipendenza lineare di matrici (dispensa, p. 96)

**Obiettivo:** verificare, usando la definizione di indipendenza lineare, che le seguenti tre matrici di $M_2(\mathbb{R})$ (matrici $2\times 2$ a coefficienti reali) sono **linearmente indipendenti**:

$$A_1=\begin{pmatrix} 1 & 1\\ 0 & 0 \end{pmatrix}, \qquad A_2=\begin{pmatrix} 0 & 1\\ -1 & 2 \end{pmatrix}, \qquad A_3=\begin{pmatrix} 3 & 0\\ 1 & 0 \end{pmatrix}.$$

**1. Impostiamo la combinazione lineare uguale alla matrice nulla.**

$$\lambda_1 A_1+\lambda_2 A_2+\lambda_3 A_3= \begin{pmatrix} 0 & 0\\ 0 & 0 \end{pmatrix}.$$

Sostituiamo le tre matrici:

$$\lambda_1\begin{pmatrix} 1 & 1\\ 0 & 0 \end{pmatrix} + \lambda_2\begin{pmatrix} 0 & 1\\ -1 & 2 \end{pmatrix} + \lambda_3\begin{pmatrix} 3 & 0\\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 0 & 0\\ 0 & 0 \end{pmatrix}.$$

**2. Moltiplichiamo ogni matrice per il suo coefficiente e sommiamo posizione per posizione.**

$$\begin{pmatrix} \lambda_1 & \lambda_1\\ 0 & 0 \end{pmatrix} + \begin{pmatrix} 0 & \lambda_2\\ -\lambda_2 & 2\lambda_2 \end{pmatrix} + \begin{pmatrix} 3\lambda_3 & 0\\ \lambda_3 & 0 \end{pmatrix} = \begin{pmatrix} 0 & 0\\ 0 & 0 \end{pmatrix}.$$

Quindi:

$$\begin{pmatrix} \lambda_1+3\lambda_3 & \lambda_1+\lambda_2\\ -\lambda_2+\lambda_3 & 2\lambda_2 \end{pmatrix} = \begin{pmatrix} 0 & 0\\ 0 & 0 \end{pmatrix}.$$

**3. Uguagliamo gli elementi che occupano la stessa posizione.** Otteniamo il sistema omogeneo:

$$\begin{cases} \lambda_1+3\lambda_3=0\\ \lambda_1+\lambda_2=0\\ -\lambda_2+\lambda_3=0\\ 2\lambda_2=0 \end{cases}$$

**4. Risolviamo il sistema.** Dall'ultima equazione si ottiene $\lambda_2=0$. Sostituendolo nella seconda e nella terza:

$$\lambda_1=0,\qquad \lambda_3=0.$$

Anche la prima equazione è quindi verificata.

**Conclusione:** l'unica combinazione lineare che produce la matrice nulla ha **tutti i coefficienti uguali a zero**:

$$\boxed{\lambda_1=\lambda_2=\lambda_3=0}.$$

Perciò **$A_1$, $A_2$ e $A_3$ sono linearmente indipendenti**.

**Da ricordare:** per verificare l'indipendenza di matrici si usa lo stesso procedimento usato per i vettori: si impone una combinazione lineare uguale allo **zero dello spazio** (qui la matrice nulla) e si cercano i coefficienti.

### 4.4.1 — Indipendenza lineare e rango (pp. 97–98)

Se $A$ ha come colonne i **$k$ vettori** che stiamo studiando, allora

$$\boxed{\text{vettori indipendenti}\iff\mathrm{rg}(A)=k}.$$

Se il rango è minore del numero delle colonne, i vettori sono dipendenti.

**Non confondere i due confronti:**

- **Indipendenza:** rango uguale al **numero di colonne**.
- **Generatori di tutto $\mathbb R^n$:** rango uguale al **numero di righe**.

**Colonne con pivot:** quando riduciamo $A$ con Gauss, le posizioni dei pivot ci indicano quali colonne della **matrice originale** formano un insieme indipendente. Una colonna senza pivot corrisponde a un vettore che si può ricavare come combinazione lineare dei vettori nelle colonne con pivot.

#### Esempio 61 — Dipendenza lineare e rango (p. 98)

Consideriamo i vettori di $\mathbb{R}^4$:

$$
v_1=(1,2,-1,0),\quad v_2=(0,1,1,3),\quad v_3=(-1,0,3,6).
$$

Per verificare l'indipendenza, disponiamo i vettori **nelle colonne** della matrice:

$$
A=\begin{pmatrix}
1&0&-1\\
2&1&0\\
-1&1&3\\
0&3&6
\end{pmatrix}.
$$

Applicando le operazioni $E_{21}(-2)$ ed $E_{31}(1)$ indicate nella dispensa:

$$
\begin{pmatrix}
1&0&-1\\
0&1&2\\
0&1&2\\
0&3&6
\end{pmatrix}.
$$

Dopo le operazioni indicate $E_{32}(1)$ ed $E_{42}(-3)$, **la dispensa riporta** la matrice a scalini:

$$
\begin{pmatrix}
1&0&-1\\
0&-1&2\\
0&0&0\\
0&0&0
\end{pmatrix}.
$$

**Conclusione:** $\mathrm{rg}(A)=2<3$, quindi i tre vettori sono **linearmente dipendenti**. La terza colonna è priva di pivot: $v_3$ è combinazione lineare di $v_1$ e $v_2$.

#### Esempio 62 — Ricavare la relazione tra i vettori (pp. 98–99)

L'Esempio 62 prosegue la riduzione dell'Esempio 61. La **matrice iniziale riportata nella dispensa** è:

$$
\begin{pmatrix}
1&0&-1\\
0&-1&-2\\
0&0&0\\
0&0&0
\end{pmatrix}.
$$

Con $D_2(-1)$, ossia moltiplicando la seconda riga per $-1$, si ottiene:

$$
\begin{pmatrix}
1&0&-1\\
0&1&2\\
0&0&0\\
0&0&0
\end{pmatrix}.
$$

**Conclusione:** dalla terza colonna della forma ridotta si leggono i coefficienti $-1$ e $2$:

$$
\boxed{v_3=-v_1+2v_2}.
$$

**Nota sui segni della dispensa.** Tra le matrici a scalini stampate negli Esempi 61 e 62 ci sono **refusi nella seconda riga**. Le matrici qui sopra sono state **trascritte come nell'originale**, senza correggerle. Effettuando correttamente Gauss, la seconda riga è $(0,1,2)$; la conclusione $v_3=-v_1+2v_2$ resta corretta.

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
