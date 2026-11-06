# Capitolo 1 — Geometria nello spazio tridimensionale

**Riferimento:** Elisa Postinghel, *Geometria e Algebra Lineare*, Capitolo 1, pp. 5–41 della dispensa (pp. 6–42 del PDF).  
**Scopo:** definizioni, proprietà, procedure ed esempi ragionati per preparare teoria ed esercizi.  
**Collegamento:** [Capitolo 2 — Sistemi lineari](../Sistemi%20lineari/Sistemi%20lineari.md).

> Gli argomenti, la sequenza delle sezioni e gli esempi contrassegnati come «della dispensa» seguono il Capitolo 1. I paragrafi «Approfondimento» e «Da ricordare» sviluppano i passaggi per facilitare lo studio. Le formule sono scritte in Markdown matematico compatibile con GitHub.

## Indice

- [1.1 — Segmenti orientati e vettori geometrici (pp. 5–18)](#indice-cap1-1)
  - [1.1.1 — Sistema di riferimento cartesiano](#indice-cap1-2)
  - [1.1.2 — Segmenti orientati, equivalenza, vettori](#indice-cap1-3)
  - [1.1.3 — Operazioni di vettori geometrici (pp. 7–11)](#indice-cap1-4)
    - [Somma: regola punta-coda](#indice-cap1-5)
    - [Prodotto di un vettore per uno scalare](#indice-cap1-6)
    - [Prodotto scalare](#indice-cap1-7)
  - [1.1.4 — Proiezioni ortogonali (pp. 11–13)](#indice-cap1-8)
  - [1.1.5 — Vettori e operazioni in coordinate (pp. 13–18)](#indice-cap1-9)
    - [Coordinate a partire da due punti](#indice-cap1-10)
    - [Operazioni coordinate per coordinate](#indice-cap1-11)
- [1.2 — Rette e piani nello spazio (pp. 18–33)](#indice-cap1-12)
  - [1.2.1 — Equazioni di un piano](#indice-cap1-13)
    - [Forma cartesiana](#indice-cap1-14)
    - [Forma parametrica](#indice-cap1-15)
  - [1.2.2 — Equazioni di una retta (pp. 21–23)](#indice-cap1-16)
  - [1.2.3 — Fascio di piani di sostegno una retta (p. 23)](#indice-cap1-17)
  - [1.2.4 — Posizione reciproca di rette e piani (pp. 24–27)](#indice-cap1-18)
    - [Due rette nello spazio](#indice-cap1-19)
    - [Due piani](#indice-cap1-20)
    - [Retta e piano](#indice-cap1-21)
  - [1.2.5 — Distanze (pp. 27–33)](#indice-cap1-22)
    - [Distanza punto–punto](#indice-cap1-23)
    - [Distanza punto–piano](#indice-cap1-24)
    - [Distanza punto–retta](#indice-cap1-25)
    - [Distanza retta–retta](#indice-cap1-26)
- [1.3 — Esercizi ricapitolativi (pp. 33–41)](#indice-cap1-27)
  - [Schema operativo: scegliere il metodo giusto](#indice-cap1-28)
  - [Esercizio guidato aggiuntivo — Piano per una retta e un punto](#indice-cap1-29)
  - [Domande per il ripasso orale (p. 41)](#indice-cap1-30)
- [Formulario essenziale](#indice-cap1-31)

---

<a name="indice-cap1-1"></a>

## 1.1 — Segmenti orientati e vettori geometrici (pp. 5–18)

<a name="indice-cap1-2"></a>

### 1.1.1 — Sistema di riferimento cartesiano

Nello spazio tridimensionale si fissa un'origine $O=(0,0,0)$ e si scelgono tre assi perpendicolari $x,y,z$, orientati secondo la **regola della mano destra** (figura 1.1). Un punto è descritto dalle sue coordinate $P=(x_P,y_P,z_P)$.

**Attenzione:** un *punto* indica una posizione, mentre un *vettore geometrico* descrive uno spostamento (direzione, verso e modulo). Le coordinate possono sembrare le stesse, ma il significato non è identico.

<a name="indice-cap1-3"></a>

### 1.1.2 — Segmenti orientati, equivalenza, vettori

**Definizione 1 — Segmento orientato.** Il segmento $\overrightarrow{AB}$ ha estremo iniziale $A$ ed estremo finale $B$: la freccia va da $A$ verso $B$.

Due segmenti orientati sono **equivalenti** se hanno contemporaneamente:
- la stessa **direzione** (giacciono su rette parallele);
- lo stesso **verso**;
- lo stesso **modulo** (lunghezza).

**Definizione 2 — Vettore geometrico.** È una *classe di equivalenza* di segmenti orientati. Segmenti posti in punti diversi possono quindi rappresentare **lo stesso vettore**, purché siano equivalenti.

**Definizione 3 — Vettore nullo.** È il vettore rappresentato dai segmenti del tipo $\overrightarrow{AA}$: il suo modulo è zero, mentre direzione e verso sono indeterminati.

**Definizione 4 — Versore.** Un vettore geometrico di modulo $1$.

**Approfondimento — Le tre parole da distinguere.** Due vettori possono avere la stessa direzione ma verso opposto; possono inoltre avere stessa direzione e verso ma moduli differenti. Per essere uguali servono **tutte e tre** le caratteristiche.

<a name="indice-cap1-4"></a>

### 1.1.3 — Operazioni di vettori geometrici (pp. 7–11)

<a name="indice-cap1-5"></a>

#### Somma: regola punta-coda

Se $\mathbf v=\overrightarrow{AB}$ e $\mathbf w=\overrightarrow{BC}$, allora

$$
\mathbf v+\mathbf w=\overrightarrow{AC}.
$$

L'estremo finale del primo rappresentante coincide con l'inizio del secondo (figura 1.3 della dispensa). La **regola del parallelogramma** esprime la stessa somma.

**Opposto:** $-\mathbf v$ ha modulo e direzione uguali a $\mathbf v$, ma verso opposto.

Le quattro proprietà della somma sono:

1. **Commutatività:** $\mathbf v+\mathbf w=\mathbf w+\mathbf v$.
2. **Associatività:** $(\mathbf v+\mathbf w)+\mathbf u=\mathbf v+(\mathbf w+\mathbf u)$.
3. **Elemento neutro:** $\mathbf v+\mathbf 0=\mathbf v$.
4. **Opposto:** $\mathbf v+(-\mathbf v)=\mathbf 0$.

<a name="indice-cap1-6"></a>

#### Prodotto di un vettore per uno scalare

Per $\lambda\in\mathbb R$, il vettore $\lambda\mathbf v$:

- conserva la direzione di $\mathbf v$ quando $\lambda\ne0$;
- ha lo stesso verso se $\lambda>0$, verso opposto se $\lambda<0$;
- ha modulo $|\lambda\mathbf v|=|\lambda|\,|\mathbf v|$;
- è nullo se $\lambda=0$ o $\mathbf v=\mathbf 0$.

Le proprietà fondamentali sono:

$$
\lambda(\mu\mathbf v)=(\lambda\mu)\mathbf v,\qquad 1\mathbf v=\mathbf v,
$$

$$
(\lambda+\mu)\mathbf v=\lambda\mathbf v+\mu\mathbf v,\qquad
\lambda(\mathbf v+\mathbf w)=\lambda\mathbf v+\lambda\mathbf w.
$$

**Definizione 8 — Normalizzazione.** Se $\mathbf v\ne\mathbf 0$, il vettore

$$
\boxed{\frac{\mathbf v}{|\mathbf v|}}
$$

è un versore con **la stessa direzione e lo stesso verso** di $\mathbf v$.

**Perché funziona?** Il suo modulo è $|\mathbf v|/|\mathbf v|=1$. Non si può normalizzare il vettore nullo: si dividerebbe per zero.

<a name="indice-cap1-7"></a>

#### Prodotto scalare

**Definizione 9.** Se $\theta$ è l'angolo tra due vettori geometrici, allora

$$
\boxed{\mathbf v\cdot\mathbf w=|\mathbf v|\,|\mathbf w|\cos\theta}.
$$

Il prodotto scalare restituisce **un numero reale**, non un vettore.

Proprietà:

$$
\mathbf v\cdot\mathbf w=\mathbf w\cdot\mathbf v,\qquad
(\lambda\mathbf v)\cdot\mathbf w=\lambda(\mathbf v\cdot\mathbf w),
$$

$$
\mathbf v\cdot(\mathbf w+\mathbf u)
=\mathbf v\cdot\mathbf w+\mathbf v\cdot\mathbf u,\qquad
\mathbf v\cdot\mathbf v=|\mathbf v|^2.
$$

Per vettori **non nulli**:

$$
\boxed{\mathbf v\perp\mathbf w\iff\mathbf v\cdot\mathbf w=0}.
$$

**Approfondimento — Segno del prodotto scalare:** è positivo se l'angolo è acuto, zero se è retto e negativo se è ottuso. Questo consente di capire il tipo di angolo senza disegnarlo.

<a name="indice-cap1-8"></a>

### 1.1.4 — Proiezioni ortogonali (pp. 11–13)

La **proiezione ortogonale** di $\mathbf v$ su un vettore non nullo $\mathbf w$ è la componente di $\mathbf v$ nella direzione di $\mathbf w$ (figura 1.8).

**Proposizione 1.** Se $\mathbf e$ è un versore:

$$
\mathrm{proj}_{\mathbf e}(\mathbf v)=(\mathbf v\cdot\mathbf e)\mathbf e.
$$

Per un vettore generico $\mathbf w\ne\mathbf 0$:

$$
\boxed{\mathrm{proj}_{\mathbf w}(\mathbf v)
=\frac{\mathbf v\cdot\mathbf w}{|\mathbf w|^2}\mathbf w}.
$$

**Perché si divide per $|\mathbf w|^2$?** Si normalizza la direzione $\mathbf e=\mathbf w/|\mathbf w|$ e si sostituisce nella prima formula: compaiono due fattori $1/|\mathbf w|$.

**Esempio guidato:** $\mathbf v=(3,2,0)$ e $\mathbf w=(1,0,0)$. Poiché $\mathbf v\cdot\mathbf w=3$ e $|\mathbf w|^2=1$,

$$
\mathrm{proj}_{\mathbf w}(\mathbf v)=3(1,0,0)=(3,0,0).
$$

Il vettore **perpendicolare** a $\mathbf w$ che resta dopo la proiezione è $\mathbf v-\mathrm{proj}_{\mathbf w}(\mathbf v)=(0,2,0)$.

<a name="indice-cap1-9"></a>

### 1.1.5 — Vettori e operazioni in coordinate (pp. 13–18)

<a name="indice-cap1-10"></a>

#### Coordinate a partire da due punti

Se $A=(x_A,y_A,z_A)$ e $B=(x_B,y_B,z_B)$:

$$
\boxed{\overrightarrow{AB}=(x_B-x_A,\ y_B-y_A,\ z_B-z_A)}.
$$

**Regola pratica:** *punto finale meno punto iniziale*.

**Esempio:** per $A=(1,-2,3)$, $B=(4,0,-1)$ si ha $\overrightarrow{AB}=(3,2,-4)$, mentre $\overrightarrow{BA}=(-3,-2,4)$.

I tre versori degli assi sono $\mathbf i=(1,0,0)$, $\mathbf j=(0,1,0)$, $\mathbf k=(0,0,1)$. Ogni vettore si scrive

$$
\mathbf v=(v_1,v_2,v_3)=v_1\mathbf i+v_2\mathbf j+v_3\mathbf k.
$$

**Proposizione 2.** Poiché i tre versori sono ortonormali, $v_1=\mathbf v\cdot\mathbf i$, $v_2=\mathbf v\cdot\mathbf j$, $v_3=\mathbf v\cdot\mathbf k$.

<a name="indice-cap1-11"></a>

#### Operazioni coordinate per coordinate

Dati $\mathbf v=(v_1,v_2,v_3)$ e $\mathbf w=(w_1,w_2,w_3)$:

$$
\mathbf v+\mathbf w=(v_1+w_1,v_2+w_2,v_3+w_3),
$$

$$
\lambda\mathbf v=(\lambda v_1,\lambda v_2,\lambda v_3).
$$

**Proposizione 3 — Modulo:**

$$
\boxed{|\mathbf v|=\sqrt{v_1^2+v_2^2+v_3^2}}.
$$

**Proposizione 4 — Prodotto scalare in coordinate:**

$$
\boxed{\mathbf v\cdot\mathbf w=v_1w_1+v_2w_2+v_3w_3}.
$$

**Esempio completo:** $\mathbf v=(2,-1,2)$, $\mathbf w=(1,2,0)$.

$$
|\mathbf v|=\sqrt{4+1+4}=3,\qquad
\mathbf v\cdot\mathbf w=2-2+0=0.
$$

Dunque i vettori sono ortogonali e il versore nella direzione di $\mathbf v$ è

$$
\frac{\mathbf v}{|\mathbf v|}=\left(\frac23,-\frac13,\frac23\right).
$$

**Errore frequente:** il prodotto scalare non consiste nella somma delle coordinate: bisogna moltiplicare tra loro le componenti **corrispondenti**.

<a name="indice-cap1-12"></a>

## 1.2 — Rette e piani nello spazio (pp. 18–33)

<a name="indice-cap1-13"></a>

### 1.2.1 — Equazioni di un piano

<a name="indice-cap1-14"></a>

#### Forma cartesiana

Un piano $\pi$ ha equazione

$$
\boxed{\pi:\ ax+by+cz+d=0},\qquad (a,b,c)\ne(0,0,0).
$$

Il vettore $\mathbf n=(a,b,c)$ è **normale al piano**: è perpendicolare a tutte le direzioni contenute nel piano.

**Appartenenza:** $P=(x_P,y_P,z_P)$ appartiene a $\pi$ se e solo se $ax_P+by_P+cz_P+d=0$.

**Come ricavare il piano da un punto e una normale.** Dati $P$ e $\mathbf n=(a,b,c)$, imponiamo $\overrightarrow{PQ}\cdot\mathbf n=0$ per un punto generico $Q=(x,y,z)$:

$$
\boxed{a(x-x_P)+b(y-y_P)+c(z-z_P)=0}.
$$

**Esempio 2 della dispensa (p. 19–20).** Con $P=(1,-1,2)$ e $\mathbf n=(2,-3,-1)$:

$$
2(x-1)-3(y+1)-(z-2)=0
\iff\boxed{2x-3y-z-3=0}.
$$

**Non unicità:** moltiplicare tutti i coefficienti dell'equazione per uno scalare **non nullo** produce lo stesso piano. Per esempio $2x-3y-z-3=0$ e $-4x+6y+2z+6=0$ sono equivalenti.

<a name="indice-cap1-15"></a>

#### Forma parametrica

Un piano si descrive con un punto $A$ e due vettori direzionali **non proporzionali** $\mathbf v,\mathbf w$:

$$
\boxed{Q=A+t\mathbf v+s\mathbf w},\qquad t,s\in\mathbb R.
$$

In coordinate:

$$
\begin{cases}
x=x_A+tv_1+sw_1,\\
y=y_A+tv_2+sw_2,\\
z=z_A+tv_3+sw_3.
\end{cases}
$$

Tre punti $A,B,C$ **non allineati** determinano un piano: basta porre $\mathbf v=\overrightarrow{AB}$, $\mathbf w=\overrightarrow{AC}$.

**Esempio 3 della dispensa (p. 20).** $A=(2,0,1)$, $B=(1,3,3)$, $C=(-1,2,0)$, quindi

$$
\mathbf v=(-1,3,2),\qquad \mathbf w=(-3,2,-1).
$$

Le equazioni parametriche sono

$$
\begin{cases}
x=2-t-3s,\\
y=3t+2s,\\
z=1+2t-s.
\end{cases}
$$

**Approfondimento — Ricavare la cartesiana:** cerchiamo $(a,b,c)$ ortogonale a $\mathbf v$ e $\mathbf w$:

$$
\begin{cases}
-a+3b+2c=0,\\
-3a+2b-c=0.
\end{cases}
$$

Una soluzione non nulla è $(a,b,c)=(1,1,-1)$. Imporre il passaggio per $A$ dà

$$
(x-2)+y-(z-1)=0
\iff\boxed{x+y-z-1=0}.
$$

**Cartesiana $\to$ parametrica:** si risolve l'equazione del piano scegliendo **due variabili libere**. Per esempio, $2x-3y-z-3=0$ con $x=s$, $y=t$ implica

$$
\begin{cases}
x=s,\\ y=t,\\ z=2s-3t-3.
\end{cases}
$$

<a name="indice-cap1-16"></a>

### 1.2.2 — Equazioni di una retta (pp. 21–23)

Una retta può essere descritta con un punto $A$ e un vettore direzionale $\mathbf v\ne\mathbf 0$:

$$
\boxed{Q=A+t\mathbf v},\qquad t\in\mathbb R.
$$

In coordinate:

$$
\begin{cases}
x=x_A+tv_1,\\
y=y_A+tv_2,\\
z=z_A+tv_3.
\end{cases}
$$

In **forma cartesiana** la retta è l'intersezione di due piani non paralleli:

$$
\boxed{r:\begin{cases}
ax+by+cz+d=0,\\
a'x+b'y+c'z+d'=0.
\end{cases}}
$$

**Esempio 5 della dispensa (p. 22).** La retta per $A=(3,1,-2)$ e $B=(5,2,-3)$ ha direzione

$$
\overrightarrow{AB}=(2,1,-1),
$$

e pertanto

$$
\begin{cases}
x=3+2t,\\
y=1+t,\\
z=-2-t.
\end{cases}
$$

Dalla terza equazione $t=-2-z$; sostituendo nelle altre due:

$$
\boxed{\begin{cases}
x+2z+1=0,\\
y+z+1=0.
\end{cases}}
$$

**Da ricordare:** per la retta serve **un parametro** (una direzione), per il piano **due parametri** (due direzioni indipendenti).

<a name="indice-cap1-17"></a>

### 1.2.3 — Fascio di piani di sostegno una retta (p. 23)

Se $r$ è l'intersezione di $\pi_1:F(x,y,z)=0$ e $\pi_2:G(x,y,z)=0$, ogni piano del fascio che contiene $r$ è

$$
\boxed{\lambda F(x,y,z)+\mu G(x,y,z)=0},
\qquad (\lambda,\mu)\ne(0,0).
$$

**Procedura per il piano che contiene $r$ e passa per $P$:**

1. Scrivere il fascio $\lambda F+\mu G=0$.
2. Sostituire le coordinate di $P$: si trova una relazione tra $\lambda$ e $\mu$.
3. Scegliere una coppia non nulla che soddisfi la relazione.
4. Sostituirla nel fascio.

**Esempio 6 della dispensa (p. 23).** Per

$$
r:\begin{cases}x+2z+1=0,\\y+z+1=0,\end{cases}
\qquad P=(1,3,0),
$$

la condizione di passaggio è $2\lambda+4\mu=0$. Scelti $\lambda=-2,\mu=1$:

$$
-2(x+2z+1)+(y+z+1)=0
\iff\boxed{-2x+y-3z-1=0}.
$$

<a name="indice-cap1-18"></a>

### 1.2.4 — Posizione reciproca di rette e piani (pp. 24–27)

<a name="indice-cap1-19"></a>

#### Due rette nello spazio

Siano $r:A+t\mathbf v$ e $r':B+s\mathbf w$.

- **Parallele:** $\mathbf v$ e $\mathbf w$ sono proporzionali.
- **Incidenti:** esistono $t,s$ che rendono uguali tutte e tre le coordinate.
- **Sghembe:** non sono né parallele né incidenti.
- **Complanari:** giacciono nello stesso piano; per rette distinte equivale a dire che sono parallele oppure incidenti.
- **Direzioni ortogonali:** $\mathbf v\cdot\mathbf w=0$.

**Metodo di confronto (fondamentale negli esercizi):**

1. Estrarre i due vettori direzionali.
2. Controllare se sono proporzionali.
3. Se non lo sono, risolvere $A+t\mathbf v=B+s\mathbf w$ in **tre equazioni e due incognite**.
4. Se il sistema è compatibile, le rette si incontrano; altrimenti sono sghembe.

**Approfondimento importante:** due rette possono avere vettori direzionali ortogonali **senza incontrarsi**: in quel caso sono sghembe con direzioni ortogonali. Il solo prodotto scalare nullo non prova che abbiano un punto in comune (vedi Esempio 7, pp. 24–25).

<a name="indice-cap1-20"></a>

#### Due piani

Per $\pi:ax+by+cz+d=0$ e $\pi':a'x+b'y+c'z+d'=0$, siano $\mathbf n=(a,b,c)$ e $\mathbf n'=(a',b',c')$.

- **Paralleli:** $\mathbf n$ e $\mathbf n'$ proporzionali (i piani possono anche coincidere).
- **Incidenti:** normali non proporzionali; l'intersezione è una retta.
- **Ortogonali:** $\mathbf n\cdot\mathbf n'=0$.

**Esempio:** $x+y+z=1$ e $x-y=0$ hanno normali $(1,1,1)$ e $(1,-1,0)$; poiché il prodotto scalare è $0$, i piani sono ortogonali.

<a name="indice-cap1-21"></a>

#### Retta e piano

Per $r:A+t\mathbf v$ e $\pi:\mathbf n\cdot Q+d=0$:

- **Retta parallela alla direzione del piano:** $\mathbf v\cdot\mathbf n=0$. Occorre verificare separatamente se la retta è **contenuta** in $\pi$ oppure è **disgiunta**.
- **Retta incidente in un punto:** $\mathbf v\cdot\mathbf n\ne0$.
- **Retta perpendicolare al piano:** $\mathbf v$ e $\mathbf n$ sono proporzionali.

**Esempio 9 della dispensa (p. 27).** Per $\pi:x+y+z-1=0$ e

$$
r:\begin{cases}x+2y=0,\\y-z=0,\end{cases}
$$

ponendo $y=t$ si ottiene $(x,y,z)=(-2t,t,t)$. Quindi $\mathbf v=(-2,1,1)$ e $\mathbf n=(1,1,1)$: $\mathbf v\cdot\mathbf n=0$. Il punto $O=(0,0,0)$ appartiene a $r$ ma non a $\pi$, dunque **retta e piano sono paralleli e disgiunti**.

<a name="indice-cap1-22"></a>

### 1.2.5 — Distanze (pp. 27–33)

<a name="indice-cap1-23"></a>

#### Distanza punto–punto

Per $A=(x_A,y_A,z_A)$ e $B=(x_B,y_B,z_B)$:

$$
\boxed{d(A,B)=\sqrt{(x_B-x_A)^2+(y_B-y_A)^2+(z_B-z_A)^2}}.
$$

È semplicemente il modulo di $\overrightarrow{AB}$.

<a name="indice-cap1-24"></a>

#### Distanza punto–piano

**Proposizione 5.** Per $P=(x_P,y_P,z_P)$ e $\pi:ax+by+cz+d=0$:

$$
\boxed{d(P,\pi)=
\frac{|ax_P+by_P+cz_P+d|}{\sqrt{a^2+b^2+c^2}}}.
$$

**Interpretazione:** il numeratore misura lo scostamento dall'equazione del piano, il denominatore normalizza la lunghezza del vettore normale. Le barre di **valore assoluto** assicurano una distanza non negativa.

**Esempio guidato:** $P=(2,0,1)$ e $\pi:x+y+2z=0$:

$$
d(P,\pi)=\frac{|2+0+2|}{\sqrt{1+1+4}}
=\frac4{\sqrt6}=\frac{2\sqrt6}{3}.
$$

<a name="indice-cap1-25"></a>

#### Distanza punto–retta

Sia $r:A+t\mathbf v$ e sia $P$ un punto. Il punto più vicino $H$ è la **proiezione ortogonale di $P$ sulla retta**.

**Metodo 1 della dispensa:** prendere $Q(t)=A+t\mathbf v$ e imporre

$$
\boxed{(Q(t)-P)\cdot\mathbf v=0}.
$$

Trovato $t_0$, calcolare $H=Q(t_0)$ e $d(P,r)=|P-H|$.

**Metodo 2:** trovare il piano passante per $P$ e perpendicolare alla retta; il suo punto di intersezione con $r$ è $H$.

**Esempio 10 della dispensa (pp. 29–30).** $P=(1,2,2)$, $r$ passa per $R=(3,-1,3)$ con direzione $\mathbf v=(2,-1,-1)$. Un punto generico è

$$
Q(t)=(3+2t,-1-t,3-t).
$$

Imponiamo $\overrightarrow{PQ(t)}\cdot\mathbf v=0$:

$$
(2+2t,-3-t,1-t)\cdot(2,-1,-1)=6+6t=0.
$$

Quindi $t=-1$, $H=(1,0,4)$ e

$$
\boxed{d(P,r)=\sqrt{0^2+(-2)^2+2^2}=2\sqrt2}.
$$

<a name="indice-cap1-26"></a>

#### Distanza retta–retta

**Definizione.** La distanza tra due rette $r$ e $r'$ nello spazio è la **minima distanza tra un punto di $r$ e un punto di $r'$**:

$$
d(r,r')=\min_{\substack{P\in r\\Q\in r'}} d(P,Q).
$$

Prima di calcolarla bisogna riconoscere la posizione reciproca delle rette:

1. **Rette incidenti:** hanno un punto in comune, perciò $d(r,r')=0$.
2. **Rette parallele distinte:** scelto un punto qualsiasi $P\in r$, basta calcolare $d(P,r')$. Tale distanza è la stessa qualunque sia il punto scelto su $r$.
3. **Rette sghembe:** non sono parallele e non si incontrano. Occorre trovare il segmento che le unisce e ha **lunghezza minima**: questo segmento è perpendicolare a entrambe le rette.

Per le rette sghembe la dispensa (pp. 31–32) presenta **due metodi equivalenti**: quello dei due punti generici e quello del piano ausiliario.

##### Metodo 1 — Segmento perpendicolare a entrambe le rette

Siano note le equazioni parametriche:

$$
r:\begin{cases}
x=a_1+tv_1\\
y=a_2+tv_2\\
z=a_3+tv_3
\end{cases}
\qquad
r':\begin{cases}
x=b_1+sw_1\\
y=b_2+sw_2\\
z=b_3+sw_3
\end{cases}
$$

I rispettivi vettori direzionali sono $\mathbf v=(v_1,v_2,v_3)$ e $\mathbf w=(w_1,w_2,w_3)$. Indichiamo con $P(t)\in r$ e $Q(s)\in r'$ due punti generici. Usiamo **parametri diversi** ($t$ e $s$), perché i punti delle rette possono essere scelti indipendentemente.

Il vettore che li collega è $\overrightarrow{P(t)Q(s)}=Q(s)-P(t)$. Cerchiamo i parametri $t_0,s_0$ per cui il segmento è ortogonale a entrambe le direzioni. Siccome due vettori sono ortogonali quando il prodotto scalare è nullo, risolviamo:

$$
\boxed{
\begin{cases}
\overrightarrow{P(t)Q(s)}\cdot\mathbf v=0\\
\overrightarrow{P(t)Q(s)}\cdot\mathbf w=0
\end{cases}
}
$$

Ottenuti $t_0,s_0$, i punti più vicini sono $H=P(t_0)$ e $H'=Q(s_0)$; dunque:

$$
\boxed{d(r,r')=\left|\,\overrightarrow{HH'}\,\right|
=\sqrt{(x_{H'}-x_H)^2+(y_{H'}-y_H)^2+(z_{H'}-z_H)^2}.}
$$

**Interpretazione geometrica:** non basta prendere due punti qualsiasi sulle rette, perché la loro distanza non è necessariamente minima. Le due condizioni di ortogonalità individuano proprio gli estremi del segmento più corto.

##### Esempio 11 della dispensa — Svolgimento completo con il metodo 1

Consideriamo:

$$
r:\begin{cases}
x=1-t\\
y=-1+3t\\
z=-t
\end{cases}
\qquad
r':\begin{cases}
x=2+s\\
y=s\\
z=1-s
\end{cases}
$$

**1. Vettori direzionali e posizione reciproca.** Leggendo i coefficienti di $t$ e $s$:

$$
\mathbf v=(-1,3,-1),\qquad \mathbf w=(1,1,-1).
$$

Non sono proporzionali, quindi le rette non sono parallele. Per verificare che non siano incidenti, uguagliamo le coordinate:

$$
\begin{cases}
1-t=2+s\\
-1+3t=s\\
-t=1-s
\end{cases}
$$

Dalle ultime due equazioni si ricava $t=1$, $s=2$, ma questi valori **non** soddisfano la prima: $0\ne4$. Le rette sono dunque **sghembe**.

**2. Punti generici e vettore che li collega.**

$$
P(t)=(1-t,-1+3t,-t),\qquad Q(s)=(2+s,s,1-s).
$$

Sottraiamo le coordinate del punto iniziale da quelle del punto finale:

$$
\begin{aligned}
\overrightarrow{P(t)Q(s)}
&=Q(s)-P(t)\\
&=(1+s+t,\ 1+s-3t,\ 1-s+t).
\end{aligned}
$$

**3. Prima condizione di ortogonalità.** Il segmento cercato deve essere perpendicolare alla direzione $\mathbf v$ di $r$:

$$
\begin{aligned}
0&=\overrightarrow{P(t)Q(s)}\cdot(-1,3,-1)\\
&=-(1+s+t)+3(1+s-3t)-(1-s+t)\\
&=3s-11t+1.
\end{aligned}
$$

**4. Seconda condizione di ortogonalità.** Deve essere perpendicolare anche alla direzione $\mathbf w$ di $r'$:

$$
\begin{aligned}
0&=\overrightarrow{P(t)Q(s)}\cdot(1,1,-1)\\
&=(1+s+t)+(1+s-3t)-(1-s+t)\\
&=3s-3t+1.
\end{aligned}
$$

**5. Risolviamo il sistema nei parametri.**

$$
\begin{cases}
3s-11t+1=0\\
3s-3t+1=0
\end{cases}
$$

Sottraendo la seconda equazione dalla prima:

$$
-8t=0\quad\Longrightarrow\quad t_0=0.
$$

Poi $3s+1=0$, quindi $s_0=-\frac13$.

**6. Calcoliamo i due punti più vicini.**

$$
H=P(0)=(1,-1,0)
$$

$$
H'=Q\left(-\frac13\right)=\left(\frac53,-\frac13,\frac43\right).
$$

Il vettore tra i due punti è:

$$
\overrightarrow{HH'}=H'-H
=\left(\frac23,\frac23,\frac43\right).
$$

**7. Calcoliamo il suo modulo**, cioè la distanza fra le rette:

$$
\begin{aligned}
d(r,r')&=\sqrt{\left(\frac23\right)^2+
\left(\frac23\right)^2+\left(\frac43\right)^2}\\
&=\sqrt{\frac{4+4+16}{9}}\\
&=\boxed{\frac{2\sqrt6}{3}}.
\end{aligned}
$$

##### Metodo 2 — Piano ausiliario parallelo all'altra retta

In questo metodo **trasformiamo un problema retta–retta in un problema punto–piano**.

Cerchiamo un piano $\pi$ che soddisfi contemporaneamente due condizioni:

1. **Contenga tutta la prima retta $r$**: per garantirlo, scegliamo $\pi$ nel *fascio di piani di sostegno* di $r$.
2. **Sia parallelo alla seconda retta $r'$**: per garantirlo, imponiamo che il vettore normale $\mathbf n$ del piano sia ortogonale al vettore direzionale $\mathbf w$ di $r'$.

La seconda condizione si esprime con:

$$
\boxed{\mathbf n\cdot\mathbf w=0.}
$$

**Perché proprio il prodotto scalare nullo?** Il vettore normale è perpendicolare al piano. Se la direzione della seconda retta è perpendicolare alla normale, quella direzione è parallela al piano. **Non stiamo imponendo che la retta sia perpendicolare al piano:** stiamo imponendo esattamente il contrario, ossia che la sua direzione sia contenuta nelle direzioni del piano.

Poiché le rette di partenza sono sghembe, $r'$ non è contenuta in questo piano. Quindi possiamo scegliere **un punto qualsiasi $Q\in r'$** e calcolare:

$$
\boxed{d(r,r')=d(Q,\pi).}
$$

La distanza punto–piano si calcola con la formula già vista:

$$
d(Q,\pi)=\frac{|ax_Q+by_Q+cz_Q+d|}{\sqrt{a^2+b^2+c^2}},
\qquad \pi:ax+by+cz+d=0.
$$

**Perché funziona geometricamente?** Il piano passa per $r$ ed è parallelo a $r'$. La distanza perpendicolare dal piano a $r'$ misura esattamente la separazione minima fra le due rette: il segmento minimo ha una direzione perpendicolare sia a $r$ sia a $r'$.

##### Esempio 11 della dispensa — Svolgimento completo con il metodo 2

Riprendiamo:

$$
r:\begin{cases}
x=1-t\\
y=-1+3t\\
z=-t
\end{cases}
\qquad
r':\begin{cases}
x=2+s\\
y=s\\
z=1-s
\end{cases}
$$

**1. Trasformiamo $r$ in forma cartesiana.** Dalla terza equazione $z=-t$ ricaviamo $t=-z$. Sostituendo nelle altre:

$$
x=1+z\quad\Longrightarrow\quad x-z-1=0;
$$

$$
y=-1-3z\quad\Longrightarrow\quad y+3z+1=0.
$$

Quindi $r$ è l'intersezione dei due piani:

$$
r:\begin{cases}
x-z-1=0\\
y+3z+1=0.
\end{cases}
$$

**2. Costruiamo il fascio di piani che contiene $r$.** Tutti i piani del fascio hanno equazione:

$$
\lambda(x-z-1)+\mu(y+3z+1)=0,
\qquad (\lambda,\mu)\ne(0,0).
$$

Sviluppando:

$$
\lambda x+\mu y+(3\mu-\lambda)z-\lambda+\mu=0.
$$

Confrontando con $ax+by+cz+d=0$, un vettore normale è:

$$
\boxed{\mathbf n=(\lambda,\mu,3\mu-\lambda).}
$$

**3. Imponiamo il parallelismo con $r'$.** Il vettore direzionale della seconda retta si legge dalle sue equazioni parametriche:

$$
\mathbf w=(1,1,-1).
$$

Il piano è parallelo a $r'$ se $\mathbf n$ e $\mathbf w$ sono ortogonali:

$$
\begin{aligned}
0&=\mathbf n\cdot\mathbf w\\
&=\lambda+\mu-(3\mu-\lambda)\\
&=2\lambda-2\mu.
\end{aligned}
$$

Pertanto $\lambda=\mu$. Scegliamo $\lambda=\mu=1$ (sono ammessi anche altri valori uguali e non nulli).

**4. Ricaviamo l'equazione del piano cercato.**

$$
(x-z-1)+(y+3z+1)=0
$$

e dunque:

$$
\boxed{\pi:x+y+2z=0.}
$$

Abbiamo ora un piano che **contiene $r$** ed è **parallelo a $r'$**. Non potevamo prendere un piano qualsiasi del fascio: un altro piano contenente $r$ potrebbe incontrare $r'$, rendendo nulla la sua distanza da quella retta anche se $r$ e $r'$ sono sghembe.

**5. Prendiamo un punto qualsiasi sulla seconda retta.** Scegliendo $s=0$:

$$
Q=(2,0,1)\in r'.
$$

**6. Calcoliamo la distanza di $Q$ da $\pi$.** Nell'equazione $x+y+2z=0$ abbiamo $a=1$, $b=1$, $c=2$, $d=0$:

$$
\begin{aligned}
d(r,r')&=d(Q,\pi)\\
&=\frac{|1\cdot2+1\cdot0+2\cdot1+0|}{\sqrt{1^2+1^2+2^2}}\\
&=\frac4{\sqrt6}\\
&=\boxed{\frac{2\sqrt6}{3}}.
\end{aligned}
$$

Il risultato coincide con quello del metodo 1.

##### Quale metodo usare?

| Situazione | Procedimento |
|---|---|
| Rette incidenti | Distanza nulla |
| Rette parallele | Distanza punto–retta |
| Rette sghembe — metodo 1 | Due punti generici, due prodotti scalari nulli, distanza fra i punti trovati |
| Rette sghembe — metodo 2 | Fascio di piani contenente $r$, condizione $\mathbf n\cdot\mathbf w=0$, distanza punto–piano |

**Da ricordare:** nel **metodo 1** cerchiamo *due punti* che determinino un segmento perpendicolare a entrambe le rette; nel **metodo 2** cerchiamo *un piano* che contenga una retta e sia parallelo all'altra. Entrambi individuano la stessa distanza minima.

<a name="indice-cap1-27"></a>

## 1.3 — Esercizi ricapitolativi (pp. 33–41)

La dispensa propone esercizi su **posizione reciproca**, **piani per una retta**, **rette perpendicolari** e **distanze**, con soluzioni e svolgimenti alle pp. 34–40.

<a name="indice-cap1-28"></a>

### Schema operativo: scegliere il metodo giusto

| Dato / richiesta | Primo passo | Strumento finale |
|---|---|---|
| Retta per due punti | Calcolare $\overrightarrow{AB}$ | Parametrizzazione con $t$ |
| Piano per tre punti | Calcolare $\overrightarrow{AB}$ e $\overrightarrow{AC}$ | Due parametri, oppure una normale |
| Piano per punto e normale | Usare $\mathbf n\cdot(Q-P)=0$ | Equazione cartesiana |
| Piano che contiene una retta | Scrivere il fascio | Imporre il passaggio per un punto |
| Intersezione di due rette | Uguagliare coordinate con $t,s$ | Compatibilità del sistema |
| Intersezione retta–piano | Sostituire la parametrizzazione nel piano | Equazione in $t$ |
| Distanza punto–piano | Leggere la normale | Formula del valore assoluto |
| Distanza punto–retta | Cercare il piede $H$ | Ortogonalità o piano ausiliario |
| Distanza rette sghembe | Due parametri e due prodotti scalari | Segmento minimo comune |

<a name="indice-cap1-29"></a>

### Esercizio guidato aggiuntivo — Piano per una retta e un punto

Sia

$$
r:\begin{cases}x=1+t,\\y=2-t,\\z=t,\end{cases}
\qquad P=(0,0,1).
$$

La retta contiene $A=(1,2,0)$ e ha direzione $\mathbf v=(1,-1,1)$. Il vettore che collega $A$ a $P$ è $\mathbf w=(-1,-2,1)$. Cerchiamo una normale $\mathbf n=(a,b,c)$ ortogonale a entrambe:

$$
\begin{cases}
a-b+c=0,\\
-a-2b+c=0.
\end{cases}
$$

Sottraendo otteniamo $2a+b=0$, cioè $b=-2a$, e dalla prima $c=-3a$. Scegliamo $a=1$, quindi $\mathbf n=(1,-2,-3)$.

Il piano passante per $A$ è

$$
(x-1)-2(y-2)-3z=0
\iff\boxed{x-2y-3z+3=0}.
$$

**Controllo:** sostituendo $(1+t,2-t,t)$ si ottiene sempre $0$; sostituendo $P=(0,0,1)$ si ottiene $-3+3=0$.

<a name="indice-cap1-30"></a>

### Domande per il ripasso orale (p. 41)

1. Qual è la differenza fra un segmento orientato e un vettore geometrico?
2. Come si calcolano il modulo e il prodotto scalare in coordinate?
3. Che differenza c'è fra versore e vettore generico? Come si normalizza?
4. Come si passa da una forma parametrica a una cartesiana e viceversa?
5. In quali casi due rette nello spazio sono sghembe?
6. Due rette con direzioni ortogonali devono incontrarsi? Perché?
7. Che cosa rappresenta il vettore normale a un piano?
8. Come si ottiene la distanza minima da un punto a una retta?

<a name="indice-cap1-31"></a>

## Formulario essenziale

**Vettore individuato da due punti** $A$ e $B$:

$$
\overrightarrow{AB}=B-A
$$

**Modulo di un vettore** $\mathbf v=(v_1,v_2,v_3)$:

$$
|\mathbf v|=\sqrt{v_1^2+v_2^2+v_3^2}
$$

**Prodotto scalare** tra $\mathbf v=(v_1,v_2,v_3)$ e $\mathbf w=(w_1,w_2,w_3)$:

$$
\mathbf v\cdot\mathbf w=v_1w_1+v_2w_2+v_3w_3
$$

**Proiezione ortogonale** di $\mathbf v$ su $\mathbf w$, con $\mathbf w\ne\mathbf 0$:

$$
\mathrm{proj}_{\mathbf w}(\mathbf v)
=\frac{\mathbf v\cdot\mathbf w}{|\mathbf w|^2}\,\mathbf w
$$

**Equazione parametrica di una retta** passante per $A$ e con vettore direzionale $\mathbf v$:

$$
r:\quad Q=A+t\mathbf v
$$

**Equazione parametrica di un piano** passante per $A$ e con vettori direzionali non proporzionali $\mathbf v$ e $\mathbf w$:

$$
\pi:\quad Q=A+t\mathbf v+s\mathbf w
$$

**Distanza punto–piano**, per $P=(x_P,y_P,z_P)$ e $\pi:ax+by+cz+d=0$:

$$
d(P,\pi)=\frac{|ax_P+by_P+cz_P+d|}{\sqrt{a^2+b^2+c^2}}
$$

**Collegamento al Capitolo 2:** le condizioni di intersezione e il passaggio da cartesiane a parametriche diventano **sistemi lineari**; le tecniche di Gauss e il teorema di Rouché–Capelli permetteranno di risolverli in modo sistematico.
