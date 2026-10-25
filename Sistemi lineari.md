# Capitolo 2 — Sistemi lineari

**Riferimento:** Elisa Postinghel, *Geometria e Algebra Lineare*, Capitolo 2, pp. 42–61 della dispensa (pp. 43–62 del PDF).  
**Obiettivo:** comprendere le soluzioni dei sistemi lineari, imparare l'eliminazione di Gauss–Jordan e usare correttamente il teorema di Rouché–Capelli.  
**Prerequisito utile:** [Capitolo 1 — Geometria nello spazio tridimensionale](Geometria%20nello%20spazio%20tridimensionale.md).  
**Capitolo successivo:** [Capitolo 3 — Matrici](Matrici.md).

> Struttura e numerazione seguono la dispensa. Le spiegazioni «Approfondimento», le verifiche e gli schemi sono aggiunti per rendere espliciti i passaggi che negli esercizi si sottintendono.

## 2.1 — Sistemi lineari (pp. 42–46)

### 2.1.1 — Equazioni, sistemi e soluzioni

**Definizione 15 — Equazione lineare.** Date $n$ incognite reali $x_1,\ldots,x_n$, un'equazione lineare è della forma

$$
\boxed{a_1x_1+a_2x_2+\cdots+a_nx_n=b},
$$

dove $a_1,\ldots,a_n$ sono i **coefficienti** e $b$ è il **termine noto**.

Una **soluzione** è un'ennupla $(t_1,\ldots,t_n)$ che, sostituita al posto delle incognite, soddisfa l'uguaglianza. Se $b=0$, l'equazione è **omogenea**.

**Definizione 16 — Sistema lineare.** Un insieme di $m$ equazioni lineari nelle stesse $n$ incognite:

$$
\begin{cases}
a_{11}x_1+a_{12}x_2+\cdots+a_{1n}x_n=b_1,\\
a_{21}x_1+a_{22}x_2+\cdots+a_{2n}x_n=b_2,\\
\vdots\\
a_{m1}x_1+a_{m2}x_2+\cdots+a_{mn}x_n=b_m.
\end{cases}
$$

Una soluzione del sistema deve soddisfare **tutte le equazioni contemporaneamente**.

- **Compatibile:** possiede almeno una soluzione.
- **Incompatibile:** non possiede soluzioni.
- **Omogeneo:** tutti i termini noti sono zero, cioè $b_1=\cdots=b_m=0$.

**Osservazione 4.** Ogni sistema omogeneo è compatibile: $(0,\ldots,0)$ è sempre una soluzione.

**Esempio 12 della dispensa (p. 43).** Il sistema

$$
\begin{cases}x_1+x_2=2,\\x_1-x_2=0\end{cases}
$$

ha soluzione unica $(x_1,x_2)=(1,1)$. Al contrario,

$$
\begin{cases}x_1+x_2=2,\\x_1+x_2=0\end{cases}
$$

è incompatibile: la stessa espressione non può essere contemporaneamente uguale a $2$ e a $0$.

**Definizione 17 — Sistemi equivalenti.** Due sistemi nelle stesse incognite sono equivalenti se hanno **esattamente lo stesso insieme delle soluzioni**.

**Approfondimento — Equivalenti non significa identici.** Le equazioni possono avere coefficienti diversi, ma descrivere le stesse soluzioni. Per esempio $x+y=2$ e $2x+2y=4$ sono equivalenti come singole equazioni.

### 2.1.2 — Le matrici associate a un sistema (pp. 43–44)

Consideriamo un sistema con $m$ equazioni e $n$ incognite. A esso associamo:

1. **Matrice dei coefficienti** $A$, di ordine $m\times n$.
2. **Vettore dei termini noti** $\mathbf b$, di ordine $m\times1$.
3. **Matrice completa** (o *aumentata*) $(A\mid\mathbf b)$, di ordine $m\times(n+1)$.

$$
A=
\begin{pmatrix}
a_{11}&\cdots&a_{1n}\\
\vdots&\ddots&\vdots\\
a_{m1}&\cdots&a_{mn}
\end{pmatrix},
\qquad
\mathbf b=
\begin{pmatrix}b_1\\\vdots\\b_m\end{pmatrix}.
$$

$$
(A\mid\mathbf b)=
\left(
\begin{array}{ccc|c}
a_{11}&\cdots&a_{1n}&b_1\\
\vdots&\ddots&\vdots&\vdots\\
a_{m1}&\cdots&a_{mn}&b_m
\end{array}
\right).
$$

**Esempio 13 della dispensa (p. 44).** Per

$$
\begin{cases}
x_1+x_2=2,\\x_1-x_2=0,
\end{cases}
$$

le matrici sono

$$
A=\begin{pmatrix}1&1\\1&-1\end{pmatrix},
\qquad
\mathbf b=\begin{pmatrix}2\\0\end{pmatrix},
\qquad
(A\mid\mathbf b)=
\left(\begin{array}{cc|c}1&1&2\\1&-1&0\end{array}\right).
$$

**Da ricordare:** nella matrice completa la colonna finale contiene i **termini noti**, non nuove incognite. Se hai $3$ incognite, $A$ ha $3$ colonne anche se $(A\mid\mathbf b)$ ne ha $4$.

### 2.1.3 — Operazioni elementari (pp. 44–46)

Le tre operazioni sulle righe di una matrice che preservano le soluzioni del sistema associato sono:

1. **Scambio:** $R_i\leftrightarrow R_j$.
2. **Moltiplicazione per uno scalare non nullo:** $R_i\leftarrow\lambda R_i$, con $\lambda\ne0$.
3. **Somma di una riga a un multiplo di un'altra:** $R_i\leftarrow R_i+\mu R_j$, con $i\ne j$.

Nella notazione della dispensa si usano rispettivamente $S_{ij}$, $D_i(\lambda)$ ed $E_{ij}(\mu)$.

**Perché è vietato moltiplicare una riga per zero?** Perderemmo informazioni. L'equazione $x=1$, moltiplicata per $0$, diventerebbe $0=0$, che non impone più $x=1$.

**Perché la terza operazione conserva le soluzioni?** È reversibile: per tornare indietro basta aggiungere $-\mu$ volte la stessa riga. Per questo il sistema prima e dopo l'operazione è equivalente.

**Esempio 14–15 della dispensa (pp. 45–46).**

$$
\left(\begin{array}{cc|c}
1&1&2\\
1&-1&0
\end{array}\right)
\xrightarrow{R_2\leftarrow R_2+R_1}
\left(\begin{array}{cc|c}
1&1&2\\
2&0&2
\end{array}\right).
$$

$$
\xrightarrow{R_2\leftarrow\frac12R_2}
\left(\begin{array}{cc|c}
1&1&2\\
1&0&1
\end{array}\right)
\xrightarrow{R_1\leftarrow R_1-R_2}
\left(\begin{array}{cc|c}
0&1&1\\
1&0&1
\end{array}\right).
$$

Scambiando infine le due righe:

$$
\left(\begin{array}{cc|c}
1&0&1\\0&1&1
\end{array}\right),
$$

da cui $x_1=1$ e $x_2=1$.

**Definizione 18.** Se una matrice si ottiene da un'altra con un numero finito di operazioni elementari, si parla di **modificazione per righe**.

## 2.2 — Matrici a scalini e algoritmo di Gauss–Jordan (pp. 47–50)

### 2.2.1 — Forma a scalini, pivot e rango

**Definizione 19 — Matrice a scalini.** Una matrice è *a scalini* se:

- tutte le righe nulle, se presenti, sono in fondo;
- il primo elemento non nullo di una riga si trova **più a destra** del primo elemento non nullo della riga precedente.

Il primo elemento non nullo di ogni riga non nulla in una matrice a scalini è un **pivot** (o *elemento pivot*).

**Esempio:**

$$
\begin{pmatrix}
2&1&-1&0\\
0&0&3&5\\
0&0&0&7\\
0&0&0&0
\end{pmatrix}
$$

è a scalini, con pivot nelle posizioni $(1,1)$, $(2,3)$, $(3,4)$.

**Definizione 20 — Rango.** Il rango è il **numero di pivot** in una qualsiasi forma a scalini della matrice:

$$
\boxed{\operatorname{rg}(A)=\text{numero di pivot}}.
$$

**Osservazione 5.** Una matrice può essere ridotta a forme a scalini diverse, ma il numero di pivot è sempre lo stesso; il rango quindi è ben definito.

Per $A$ di ordine $m\times n$:

$$
0\le\operatorname{rg}(A)\le\min(m,n).
$$

**Approfondimento — Pivot e variabili.** Se stiamo riducendo $(A\mid\mathbf b)$, i pivot **nelle prime $n$ colonne** individuano le incognite principali. Le colonne di $A$ senza pivot corrispondono a variabili libere, purché il sistema sia compatibile. Un pivot nella colonna dei termini noti segnala incompatibilità.

### 2.2.2 — Eliminazione in avanti (p. 48)

La procedura indicata nella dispensa come **algoritmo di Gauss–Jordan** si sviluppa in due momenti: riduzione a scalini e successiva riduzione all'indietro.

Per la **riduzione in avanti**:

1. Cercare la prima colonna non nulla.
2. Se necessario, **scambiare righe** per portare un elemento non nullo nella posizione del primo pivot.
3. **Annullare i coefficienti sotto il pivot** con somme di righe.
4. Ripetere sulle righe successive, spostandosi verso destra.

Se un pivot è $p$ e sotto di esso, nella stessa colonna, c'è il valore $a$, la mossa tipica è

$$
R_j\longleftarrow R_j-\frac ap R_i.
$$

Questo azzera il coefficiente $a$, perché $a-(a/p)p=0$.

**Esempio guidato:** riduciamo

$$
A=\begin{pmatrix}1&2&1\\2&5&3\\3&8&5\end{pmatrix}.
$$

Prima colonna:

$$
\begin{pmatrix}1&2&1\\2&5&3\\3&8&5\end{pmatrix}
\xrightarrow{\substack{R_2\leftarrow R_2-2R_1\\R_3\leftarrow R_3-3R_1}}
\begin{pmatrix}1&2&1\\0&1&1\\0&2&2\end{pmatrix}.
$$

Seconda colonna:

$$
\xrightarrow{R_3\leftarrow R_3-2R_2}
\begin{pmatrix}1&2&1\\0&1&1\\0&0&0\end{pmatrix}.
$$

Quindi $\boxed{\operatorname{rg}(A)=2}$, perché ci sono due righe non nulle e due pivot.

### 2.2.3 — Forma ridotta per righe e riduzione all'indietro

**Definizione 21.** Una matrice a scalini è **ridotta per righe** se:

1. ciascun pivot è uguale a $1$;
2. in ogni colonna pivot, **tutti gli altri elementi sono zero**.

**Definizione 22.** La forma a scalini ridotta per righe si chiama $\operatorname{rref}(A)$ (*reduced row echelon form*).

**Osservazione 6.** La forma $\operatorname{rref}(A)$ è **unica**, a differenza delle possibili forme a scalini non ridotte.

**Come si procede:** partire dall'ultimo pivot; rendere il pivot uguale a $1$ moltiplicando la riga per il suo reciproco; eliminare i coefficienti **sopra** quel pivot; risalire di una riga e ripetere.

Riprendiamo la matrice precedente:

$$
\begin{pmatrix}1&2&1\\0&1&1\\0&0&0\end{pmatrix}
\xrightarrow{R_1\leftarrow R_1-2R_2}
\boxed{\begin{pmatrix}1&0&-1\\0&1&1\\0&0&0\end{pmatrix}}.
$$

I pivot sono entrambi $1$ e unici non nulli nelle rispettive colonne.

**Distinzione fondamentale:**

- **Forma a scalini:** zeri sotto i pivot, utili per leggere il rango e applicare la sostituzione all'indietro.
- **Forma a scalini ridotta:** zeri anche sopra i pivot, utile per leggere direttamente le soluzioni.

### 2.2.4 — Come evitare errori con Gauss

- Scrivere accanto a ogni freccia la riga modificata: ad esempio $R_3\leftarrow R_3-2R_1$.
- Eseguire la stessa operazione su **tutta la riga**, incluso il termine noto.
- Non contare come pivot un semplice coefficiente non nullo in posizione arbitraria: prima bisogna arrivare a una forma a scalini.
- Non confondere il **rango di $A$** con il **rango di $(A\mid\mathbf b)$**: la colonna finale può introdurre un pivot aggiuntivo.
- Quando compare una riga $[0\ 0\ \cdots\ 0\mid c]$ con $c\ne0$, non serve continuare: il sistema è incompatibile.

## 2.3 — Teorema di Rouché–Capelli e risoluzione (pp. 50–55)

### 2.3.1 — Enunciato e significato del teorema

**Teorema 2.3.1.1 — Rouché–Capelli.** Sia un sistema di $n$ incognite con matrice dei coefficienti $A$ e matrice completa $(A\mid\mathbf b)$.

**Condizione di compatibilità:**

$$
\boxed{\text{sistema compatibile}\iff
\operatorname{rg}(A)=\operatorname{rg}(A\mid\mathbf b)}.
$$

Se i ranghi sono diversi, il sistema è **incompatibile**.

Se i ranghi sono uguali, poniamo $r=\operatorname{rg}(A)$:

- Se $r=n$, c'è **un'unica soluzione**.
- Se $r<n$, ci sono **infinite soluzioni** dipendenti da $n-r$ **variabili libere**.

$$
\boxed{\text{numero di variabili libere}=n-\operatorname{rg}(A)}
$$

quando il sistema è compatibile.

| Situazione | Esito | Cosa compare in Gauss |
|---|---|---|
| $\operatorname{rg}(A)<\operatorname{rg}(A\mid\mathbf b)$ | Nessuna soluzione | Una contraddizione $0=c$ con $c\ne0$ |
| $\operatorname{rg}(A)=\operatorname{rg}(A\mid\mathbf b)=n$ | Una soluzione | Pivot per ciascuna incognita |
| $\operatorname{rg}(A)=\operatorname{rg}(A\mid\mathbf b)=r<n$ | Infinite soluzioni | $n-r$ incognite senza pivot |

**Approfondimento — Perché la colonna finale conta.** La matrice $A$ dice quali combinazioni delle incognite sono possibili. La matrice completa richiede anche di raggiungere gli specifici termini noti. Se la colonna $\mathbf b$ aggiunge un pivot, si ottiene una richiesta impossibile del tipo $0=1$.

**Attenzione:** la sola condizione $\operatorname{rg}(A)<n$ **non** garantisce infinite soluzioni: bisogna prima verificare la **compatibilità**.

### 2.3.2 — Esempio 21: sistema con soluzione unica (pp. 51–52)

La dispensa considera

$$
\begin{cases}
x-3y-z=-1,\\
x-2y+z=3,\\
x+2y-4z=6.
\end{cases}
$$

La matrice completa è

$$
\left(\begin{array}{ccc|c}
1&-3&-1&-1\\
1&-2&1&3\\
1&2&-4&6
\end{array}\right).
$$

**Eliminazione sotto il primo pivot:**

$$
\xrightarrow{\substack{R_2\leftarrow R_2-R_1\\R_3\leftarrow R_3-R_1}}
\left(\begin{array}{ccc|c}
1&-3&-1&-1\\
0&1&2&4\\
0&5&-3&7
\end{array}\right).
$$

**Eliminazione sotto il secondo pivot:**

$$
\xrightarrow{R_3\leftarrow R_3-5R_2}
\left(\begin{array}{ccc|c}
1&-3&-1&-1\\
0&1&2&4\\
0&0&-13&-13
\end{array}\right).
$$

I ranghi sono entrambi $3$, che coincide con il numero delle incognite: dunque **soluzione unica**.

Dalla terza riga $z=1$; dalla seconda $y+2z=4$, quindi $y=2$; dalla prima $x=6$.

$$
\boxed{(x,y,z)=(6,2,1)}.
$$

**Verifica diretta:** $6-3(2)-1=-1$, $6-2(2)+1=3$, $6+2(2)-4=6$.

**Approfondimento — Riduzione completa:**

$$
\left(\begin{array}{ccc|c}
1&-3&-1&-1\\0&1&2&4\\0&0&-13&-13
\end{array}\right)
\ \longrightarrow\
\boxed{\left(\begin{array}{ccc|c}
1&0&0&6\\0&1&0&2\\0&0&1&1
\end{array}\right)}.
$$

È la stessa soluzione ottenuta senza scrivere il sistema a ogni passaggio.

### 2.3.3 — Esempio 22: infinite soluzioni e parametri (pp. 53–54)

Il sistema è

$$
\begin{cases}
x-2y+2z-w=1,\\
2x-4y+3z+w=3,\\
3x-6y+5z=4.
\end{cases}
$$

Matrice completa:

$$
\left(\begin{array}{cccc|c}
1&-2&2&-1&1\\
2&-4&3&1&3\\
3&-6&5&0&4
\end{array}\right).
$$

Con $R_2\leftarrow R_2-2R_1$ e $R_3\leftarrow R_3-3R_1$ si ottiene:

$$
\left(\begin{array}{cccc|c}
1&-2&2&-1&1\\
0&0&-1&3&1\\
0&0&-1&3&1
\end{array}\right)
\xrightarrow{R_3\leftarrow R_3-R_2}
\left(\begin{array}{cccc|c}
1&-2&2&-1&1\\
0&0&-1&3&1\\
0&0&0&0&0
\end{array}\right).
$$

Abbiamo $\operatorname{rg}(A)=\operatorname{rg}(A\mid\mathbf b)=2$ e $n=4$, quindi **due variabili libere**. I pivot sono nelle colonne di $x$ e $z$, dunque scegliamo $y=s$ e $w=t$.

Dalla seconda riga:

$$
-z+3w=1\quad\Longrightarrow\quad z=3t-1.
$$

Dalla prima:

$$
x-2s+2(3t-1)-t=1
\quad\Longrightarrow\quad x=2s-5t+3.
$$

L'insieme delle soluzioni è

$$
\boxed{
\begin{cases}
x=2s-5t+3,\\
y=s,\\
z=3t-1,\\
w=t,
\end{cases}
\qquad s,t\in\mathbb R}.
$$

**Nota di verifica:** nell'ultimo passaggio dell'esempio stampato compare anche $x=2y-5w+1$, ma sostituendo nel **sistema originale** il termine corretto è **$+3$**. Infatti, scegliendo $s=t=0$ si ottiene $(3,0,-1,0)$ e la prima equazione vale $3+2(-1)=1$.

**Approfondimento — Forma vettoriale:** il risultato precedente equivale a

$$
\begin{pmatrix}x\\y\\z\\w\end{pmatrix}
=
\begin{pmatrix}3\\0\\-1\\0\end{pmatrix}
+s\begin{pmatrix}2\\1\\0\\0\end{pmatrix}
+t\begin{pmatrix}-5\\0\\3\\1\end{pmatrix}.
$$

Questo anticipa il Capitolo 4: una soluzione particolare più combinazioni lineari di soluzioni dell'omogeneo associato.

### 2.3.4 — Esempio 23: sistema incompatibile (pp. 53–54)

Si consideri

$$
\begin{cases}
2x-y=1,\\
y+2z=0,\\
x+z=2.
\end{cases}
$$

$$
\left(\begin{array}{ccc|c}
2&-1&0&1\\
0&1&2&0\\
1&0&1&2
\end{array}\right)
\xrightarrow{R_3\leftarrow R_3-\frac12R_1}
\left(\begin{array}{ccc|c}
2&-1&0&1\\
0&1&2&0\\
0&\frac12&1&\frac32
\end{array}\right).
$$

$$
\xrightarrow{R_3\leftarrow R_3-\frac12R_2}
\left(\begin{array}{ccc|c}
2&-1&0&1\\
0&1&2&0\\
0&0&0&\frac32
\end{array}\right).
$$

L'ultima riga significa $0=3/2$, impossibile. Perciò

$$
\operatorname{rg}(A)=2,\qquad
\operatorname{rg}(A\mid\mathbf b)=3
\quad\Longrightarrow\quad
\boxed{\text{nessuna soluzione}}.
$$

**Errore frequente:** non ignorare le righe con tutti zeri **a sinistra**. Se il termine noto di quella riga è diverso da zero, la riga contiene proprio l'informazione decisiva.

### 2.3.5 — Scegliere e scrivere le variabili libere

Quando i ranghi coincidono ma sono inferiori a $n$:

1. Identificare le **colonne pivot nella parte $A$**.
2. Assegnare un parametro a ciascuna incognita **senza pivot**.
3. Risolvere le equazioni residue per le incognite principali.
4. Scrivere tutte le soluzioni al variare libero dei parametri reali.

**Esempio semplice:**

$$
\begin{cases}
x+2y-z=4,\\
2x+4y-2z=8.
\end{cases}
$$

La seconda equazione è il doppio della prima: $r=1$, $n=3$, dunque **due variabili libere**. Ponendo $y=s$ e $z=t$:

$$
\boxed{(x,y,z)=(4-2s+t,\ s,\ t)},\qquad s,t\in\mathbb R.
$$

**Non c'è obbligo** di chiamare i parametri $s,t$: conta che siano indipendenti e che tutte le soluzioni siano rappresentate.

### 2.3.6 — Sistemi omogenei: un caso speciale

Un sistema omogeneo si scrive $A\mathbf x=\mathbf0$.

- È **sempre compatibile**.
- Se $\operatorname{rg}(A)=n$, ha **solo la soluzione nulla**.
- Se $\operatorname{rg}(A)<n$, ha **infinitamente molte soluzioni**, incluse quella nulla e altre non nulle.

**Perché?** La colonna aggiunta è nulla e non può creare un pivot che rende il sistema incompatibile.

**Conseguenza utile:** in un sistema omogeneo con **più incognite che equazioni**, cioè $n>m$, si ha necessariamente $\operatorname{rg}(A)\le m<n$. Quindi ci sono infinite soluzioni.

### 2.3.7 — Applicazione alla geometria (pp. 54–55)

Le equazioni cartesiane di una retta nello spazio sono un sistema di due equazioni in $x,y,z$. Se i due piani sono distinti e incidenti, il sistema ha rango $2$ e quindi **una variabile libera**: essa diventa il parametro della retta.

**Esempio 25 della dispensa (p. 55):**

$$
r:\begin{cases}
x+y-z=1,\\
2x+2y-z=2.
\end{cases}
$$

Sottraendo il doppio della prima equazione alla seconda troviamo $z=0$. Resta $x+y=1$. Scegliamo $y=t$:

$$
\boxed{
\begin{cases}
x=1-t,\\
y=t,\\
z=0,
\end{cases}
\qquad t\in\mathbb R}.
$$

**Approfondimento — Verifica:** sostituendo, la prima equazione dà $(1-t)+t-0=1$; la seconda dà $2(1-t)+2t=2$. La forma parametrica descrive quindi la stessa retta delle equazioni cartesiane.

**Piani:** una singola equazione cartesiana non banale in tre incognite ha normalmente $2$ variabili libere, e da esse si ricava la forma parametrica del piano.

## 2.4 — Esercizi ricapitolativi (pp. 56–61)

La sezione 2.4 della dispensa contiene esercizi con sistemi lineari, le relative soluzioni e una serie di domande teoriche.

### Esercizio guidato — Sistema dipendente da un parametro

Consideriamo, come esercizio aggiuntivo, il sistema

$$
\begin{cases}
x+y=1,\\
2x+ky=2.
\end{cases}
$$

La matrice completa è

$$
\left(\begin{array}{cc|c}
1&1&1\\
2&k&2
\end{array}\right)
\xrightarrow{R_2\leftarrow R_2-2R_1}
\left(\begin{array}{cc|c}
1&1&1\\
0&k-2&0
\end{array}\right).
$$

**Caso $k\ne2$:** il secondo pivot $k-2$ è non nullo, quindi rango $2$ e soluzione unica $(x,y)=(1,0)$.

**Caso $k=2$:** la seconda riga diventa $0=0$, quindi rango $1$; le soluzioni sono infinite:

$$
\boxed{(x,y)=(1-t,t)},\qquad t\in\mathbb R.
$$

**Lezione generale:** con parametri, non si deve mai dividere per un'espressione come $k-2$ senza aver prima separato il caso in cui essa è uguale a zero.

### Esercizio guidato — Verifica di compatibilità immediata

Per

$$
\begin{cases}
x+y+z=1,\\
2x+2y+2z=3,
\end{cases}
$$

sottraendo due volte la prima equazione dalla seconda si ottiene $0=1$: **nessuna soluzione**, qualunque sia il numero di variabili.

### Procedura completa da usare agli esercizi

1. Scrivere $(A\mid\mathbf b)$ senza perdere nessun coefficiente o termine noto.
2. Eseguire Gauss per arrivare a una forma a scalini.
3. Calcolare **separatamente** $\operatorname{rg}(A)$ e $\operatorname{rg}(A\mid\mathbf b)$.
4. Applicare Rouché–Capelli per classificare il sistema.
5. Se compatibile, identificare le colonne senza pivot, introdurre i parametri e risolvere.
6. Sostituire almeno una volta il risultato nelle equazioni iniziali per controllare errori aritmetici.

### Domande di ripasso per la teoria (p. 61)

1. Qual è la differenza tra un sistema omogeneo e uno non omogeneo?
2. Quando due sistemi lineari sono equivalenti?
3. Quali operazioni elementari preservano l'insieme delle soluzioni?
4. Che cosa sono un pivot e il rango di una matrice?
5. Che cosa distingue una forma a scalini da una forma ridotta per righe?
6. La forma ridotta $\operatorname{rref}(A)$ è unica?
7. Come si riconosce una contraddizione nella matrice completa?
8. Come si enuncia il teorema di Rouché–Capelli?
9. Da che cosa dipende il numero di variabili libere?
10. Perché un sistema omogeneo è sempre compatibile?

## Formulario e collegamenti

$$
\begin{aligned}
\text{Compatibilità}&:\quad\operatorname{rg}(A)=\operatorname{rg}(A\mid\mathbf b),\\
\text{Soluzione unica}&:\quad \operatorname{rg}(A)=\operatorname{rg}(A\mid\mathbf b)=n,\\
\text{Infinite soluzioni}&:\quad\operatorname{rg}(A)=\operatorname{rg}(A\mid\mathbf b)<n,\\
\text{Variabili libere}&:\quad n-\operatorname{rg}(A).
\end{aligned}
$$

**Collegamento al Capitolo 3:** studieremo il prodotto tra matrici, le matrici invertibili e la forma compatta $A\mathbf x=\mathbf b$.  
**Collegamento al Capitolo 4:** l'insieme delle soluzioni del sistema omogeneo diventerà un esempio fondamentale di **sottospazio vettoriale**.
