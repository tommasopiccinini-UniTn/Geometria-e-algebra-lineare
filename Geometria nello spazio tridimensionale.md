# Capitolo 1 — Geometria nello spazio tridimensionale

**Riferimento:** Elisa Postinghel, *Geometria e Algebra Lineare*, Capitolo 1, pp. 5–41 della dispensa (pp. 6–42 del PDF).  
**Scopo:** definizioni, proprietà, procedure ed esempi ragionati per preparare teoria ed esercizi.  
**Collegamento:** [Capitolo 2 — Sistemi lineari](Sistemi%20lineari.md).

> Gli argomenti, la sequenza delle sezioni e gli esempi contrassegnati come «della dispensa» seguono il Capitolo 1. I paragrafi «Approfondimento» e «Da ricordare» sviluppano i passaggi per facilitare lo studio. Le formule sono scritte in Markdown matematico compatibile con GitHub.

## 1.1 — Segmenti orientati e vettori geometrici (pp. 5–18)

### 1.1.1 — Sistema di riferimento cartesiano

Nello spazio tridimensionale si fissa un'origine $O=(0,0,0)$ e si scelgono tre assi perpendicolari $x,y,z$, orientati secondo la **regola della mano destra** (figura 1.1). Un punto è descritto dalle sue coordinate $P=(x_P,y_P,z_P)$.

**Attenzione:** un *punto* indica una posizione, mentre un *vettore geometrico* descrive uno spostamento (direzione, verso e modulo). Le coordinate possono sembrare le stesse, ma il significato non è identico.

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

### 1.1.3 — Operazioni di vettori geometrici (pp. 7–11)

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

### 1.1.4 — Proiezioni ortogonali (pp. 11–13)

La **proiezione ortogonale** di $\mathbf v$ su un vettore non nullo $\mathbf w$ è la componente di $\mathbf v$ nella direzione di $\mathbf w$ (figura 1.8).

**Proposizione 1.** Se $\mathbf e$ è un versore:

$$
\operatorname{proj}_{\mathbf e}(\mathbf v)=(\mathbf v\cdot\mathbf e)\mathbf e.
$$

Per un vettore generico $\mathbf w\ne\mathbf 0$:

$$
\boxed{\operatorname{proj}_{\mathbf w}(\mathbf v)
=\frac{\mathbf v\cdot\mathbf w}{|\mathbf w|^2}\mathbf w}.
$$

**Perché si divide per $|\mathbf w|^2$?** Si normalizza la direzione $\mathbf e=\mathbf w/|\mathbf w|$ e si sostituisce nella prima formula: compaiono due fattori $1/|\mathbf w|$.

**Esempio guidato:** $\mathbf v=(3,2,0)$ e $\mathbf w=(1,0,0)$. Poiché $\mathbf v\cdot\mathbf w=3$ e $|\mathbf w|^2=1$,

$$
\operatorname{proj}_{\mathbf w}(\mathbf v)=3(1,0,0)=(3,0,0).
$$

Il vettore **perpendicolare** a $\mathbf w$ che resta dopo la proiezione è $\mathbf v-\operatorname{proj}_{\mathbf w}(\mathbf v)=(0,2,0)$.

### 1.1.5 — Vettori e operazioni in coordinate (pp. 13–18)

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

## 1.2 — Rette e piani nello spazio (pp. 18–33)

### 1.2.1 — Equazioni di un piano

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

### 1.2.4 — Posizione reciproca di rette e piani (pp. 24–27)

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

#### Due piani

Per $\pi:ax+by+cz+d=0$ e $\pi':a'x+b'y+c'z+d'=0$, siano $\mathbf n=(a,b,c)$ e $\mathbf n'=(a',b',c')$.

- **Paralleli:** $\mathbf n$ e $\mathbf n'$ proporzionali (i piani possono anche coincidere).
- **Incidenti:** normali non proporzionali; l'intersezione è una retta.
- **Ortogonali:** $\mathbf n\cdot\mathbf n'=0$.

**Esempio:** $x+y+z=1$ e $x-y=0$ hanno normali $(1,1,1)$ e $(1,-1,0)$; poiché il prodotto scalare è $0$, i piani sono ortogonali.

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

### 1.2.5 — Distanze (pp. 27–33)

#### Distanza punto–punto

Per $A=(x_A,y_A,z_A)$ e $B=(x_B,y_B,z_B)$:

$$
\boxed{d(A,B)=\sqrt{(x_B-x_A)^2+(y_B-y_A)^2+(z_B-z_A)^2}}.
$$

È semplicemente il modulo di $\overrightarrow{AB}$.

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

#### Distanza retta–retta

- Se sono **incidenti**, la distanza è $0$.
- Se sono **parallele**, basta scegliere un punto su una retta e calcolare la distanza dall'altra.
- Se sono **sghembe**, cercare la minima distanza tra punti delle due rette.

**Metodo 1 della dispensa:** parametrizzare $P(t)\in r$, $Q(s)\in r'$ e imporre

$$
\begin{cases}
(Q(s)-P(t))\cdot\mathbf v=0,\\
(Q(s)-P(t))\cdot\mathbf w=0.
\end{cases}
$$

Le due condizioni identificano il segmento perpendicolare a **entrambe** le rette: risolto il sistema in $t,s$, si calcola $|P(t)-Q(s)|$.

**Metodo 2:** cercare il piano che contiene una retta ed è parallelo all'altra, poi applicare la formula punto–piano.

**Esempio 11 della dispensa (pp. 31–32).** Per

$$
r:\begin{cases}x=1-t,\\y=-1+3t,\\z=-t,\end{cases}
\qquad
r':\begin{cases}x=2+s,\\y=s,\\z=1-s,\end{cases}
$$

le condizioni di ortogonalità danno $t=0$ e $s=-1/3$; perciò

$$
\boxed{d(r,r')=\frac{2\sqrt6}{3}}.
$$

Il metodo del piano fornisce lo stesso valore usando $x+y+2z=0$ e il punto $(2,0,1)\in r'$.

## 1.3 — Esercizi ricapitolativi (pp. 33–41)

La dispensa propone esercizi su **posizione reciproca**, **piani per una retta**, **rette perpendicolari** e **distanze**, con soluzioni e svolgimenti alle pp. 34–40.

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

### Domande per il ripasso orale (p. 41)

1. Qual è la differenza fra un segmento orientato e un vettore geometrico?
2. Come si calcolano il modulo e il prodotto scalare in coordinate?
3. Che differenza c'è fra versore e vettore generico? Come si normalizza?
4. Come si passa da una forma parametrica a una cartesiana e viceversa?
5. In quali casi due rette nello spazio sono sghembe?
6. Due rette con direzioni ortogonali devono incontrarsi? Perché?
7. Che cosa rappresenta il vettore normale a un piano?
8. Come si ottiene la distanza minima da un punto a una retta?

## Formulario essenziale

$$
\begin{aligned}
\overrightarrow{AB}&=B-A,\\
|\mathbf v|&=\sqrt{v_1^2+v_2^2+v_3^2},\\
\mathbf v\cdot\mathbf w&=v_1w_1+v_2w_2+v_3w_3,\\
\operatorname{proj}_{\mathbf w}(\mathbf v)&=
\frac{\mathbf v\cdot\mathbf w}{|\mathbf w|^2}\mathbf w\quad(\mathbf w\ne0),\\
r&:\ Q=A+t\mathbf v,\\
\pi&:\ Q=A+t\mathbf v+s\mathbf w,\\
d(P,\pi)&=\frac{|ax_P+by_P+cz_P+d|}{\sqrt{a^2+b^2+c^2}}.
\end{aligned}
$$

**Collegamento al Capitolo 2:** le condizioni di intersezione e il passaggio da cartesiane a parametriche diventano **sistemi lineari**; le tecniche di Gauss e il teorema di Rouché–Capelli permetteranno di risolverli in modo sistematico.
