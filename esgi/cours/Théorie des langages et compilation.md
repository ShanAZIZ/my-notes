# ThΓ©orie des langages et compilation

## 07/09/2021 

### Expression RΓ©guliΓ¨res (REGEX) 
 
![regex](../.././attachments/regex.png)

### Langages et Grammaires 

 

#### Exercice 1  

πΏ1 = { ππ , π β₯ 0}  

a* 

RΓ¨gles de production π β πS | π  

πΏ2 = { ππ , π > 0}  

a+ 

RΓ¨gle de production π β πS | a 

πΏ3 = πππ  πππ‘π  π π’π π, π ππ’π πππππππ‘πππ‘ π’π π ππ’π π ππ’ πππ₯πππ’π = {π€ β π, π β , π€ π < 2} 

b*a?b* 

RΓ¨gle de production  

 π β bS | aA | π  

 A β bA | π  


S β BAB 

B β bB | π 

A β a | π  


πΏ4 = {π π π π , π, π β₯ 0 } 

a*b* 

S  β AB 

B β bB | π 

A β aA | π 

πΏ5 = πππ  πππ‘π  π π’π π ππ‘ π πΓΉ π ππ π‘ πππΓ©ππππ‘πππππ‘ π π’ππ£π π β²π’π a 

a*ba* 

S  β AB 

A β aA | B 

B β baA | π 


S β baS | aS | π 


πΏ6 = πππ  πππ‘π  ππππππ Γ©π  ππ βΆ  

- un a,suivi de 

- (une sΓ©rie non vide de b sΓ©parΓ©s par des c )ou un d, suivi de  

- une sΓ©rie (possiblement vide) de f  

 

a ( (bc)*b| d ) f* 

S  β aBF | adF 

B β bcB | b 

F β fF | c 

 

TODO : Finir l'exercice + Exercice 2 sur les Regex 

 

## 09/09/2021 

 

04/11 CC1 -> Regex, langages, gramm+aire (dΓ©rivation, arbre de dΓ©rivation, ambiguitΓ© 

### EXERCICE REGEX : 

1. Ecrire la regex des noms de variables (un mo composΓ© d'une suite de chiffre, lettre ou "_", ne commenΓ§ant pas par un chiffre) 

[a-zA-Z-][a-zA-Z-0-9]* 

2. Ecrire la regex des numΓ©ro de tΓ©lΓ©phone portable  

0[67][0-9]{8} 

3. Ecrire la regex des nombre entiers sans 0 inutile (10 mais pas 010)  

[1-9][0-9]* | 0 

4. Ecrire la regex des nombre dΓ©cimaux sans 0 inutile (10.2 mais pas 010.2 ni 10.20, 2.0 ou 0.2 mais pas 2. ni .2)  

([1-9][0-9]*|)0\.(0|[0-9]*[1-9] 

5. Ecrire la regex des adresse email  

Cfc3696 -->  

6. Ecrire la regex des expressions additives d'entiers a. V1 : 12+6+3+44 mais aussi 12 b. V2 sans les expressions sans opΓ©rateur (sans le 12) 

 

### EXERCICE 2 GRAMMAIRE : 

 

L1 = { anbn, n>= 0} 

Pas de regex simple pour L1 

S -> aSb|π 

 

L2  = {πππππππππππ  π π’π β = π, π } 

S -> aSa | bSb | a | b | aa | bb 

 


((b*a){3})*b* 

 

S -> BaBaBaBaS | B 

B -> bB| π 

 


S -> aSBc 

S -> aSBc -> a2SBaBc  -> a2 SBBcc 

cB -> Bc 

SB -> b 

bB -> b 

 

 

 

### Grammaires engendrΓ©s  

S aSbb I c 

### Exercice 5 :  


C -> 0 | 1 | β¦ |9 (Seul cas oΓΉ l'on peut mettre des β¦.)

N -> nombre ? 
+ 
- 

012 / 0 

1+ 

(12) 

(1+2)(3+4) 

 

-1 + 2 

1+2+3 

(-(-2)) 

(1+2)*3 

 

(-1 + 2 ) 

 
### Grammaire : 

 

C -> 0 | 1 | β¦ |9 

N -> CN | C 

O -> + | - | / | * 

P -> ( | ) 

 

S -> SOS | (S) | N |(-N)  

 

### Exercice 6  

 

+ 

- 

void toto (int toto) 

void toto (char [] a) 

void toto (char [] a []) 

private Etudiant toto (char int) 

 

 

P -> private |public | protected | π  

 

S -> static | π 

R -> Int | String | Char | Boolean |Float  | void 

T -> [] |π 

V -> CL 

 

S ->  PSRTT(RTTV) | π 

 

Parametres -> Type var | Param, Type var  

Var -> Var L | Min | _ 

TypeR ->Type | void 

Type -> TypePrim | Cslasse |  Type [] 

Classe -> Classe L | Maj 

Quality ->static | e 

TypePrim -> Int | Float | String| Boolean 

 

- langage - regex - grammaire (dΓ©rivation, arbre de dΓ©rivation, ambiguΓ―tΓ©) 

 

###Β PREPARATION DS 

####Β REGEX 

"(0|(\\+33)|(0033))[1-9][0-9]{8}",β― 

NumΓ©ro de tΓ©lΓ©phone exemple 

 

04/11/2021 

 

####Β REVISION Grammaire 

 

L = a*b( (ac)+ | b) 

aabac 

Aabb 

Bacac 

 

Vt = {a, b, c} 

Vn = AB 

 

S ->  AB 

A -> aA | b 

B -> ac | acB | b 

 

Ou 

 

S -> AbC 

A -> aA | rien 

C -> D | b 

D-> acD | ac 

 

#### DΓ©rivation  

 

S -> AbC 

S -> aAbC 

S -> aabC 

S -> aabb 



 

#### Exercice : analyse par dΓ©calage-rΓ©duction 

 

S -> S+S | S*S | N  

N -> NC | C 

C-> 1 | 2 | 3 | 4 

 

W = 12 + 3 * 4  

Pile 

EntrΓ©e 

Actions 

$ 

12 + 3 * 4 $ 

DΓ©calage 

1 

2 + 3 * 4 $ 

RΓ©duire C-> 1 

C 

 2 + 3 * 4 $ 

DΓ©calage  

C2 

 + 3 * 4 $ 

RΓ©duire C -> 2 

CC 

 + 3 * 4 $ 

RΓ©duire C - > N 

CN  

 + 3 * 4 $ 

RΓ©duire N -> CN 

N  

 + 3 * 4 $ 

RΓ©duire S -> N 

S 

  + 3 * 4 $ 

DΓ©calage + 

S + 

3 * 4 $ 

DΓ©calage 3 

S + 3   

  * 4 $ 

RΓ©duction C -> 3 

S + C  

* 4 $ 

RΓ©duction N-> C 

S + N  

* 4 $ 

RΓ©duction S -> N 

S + S  

* 4 $ 

RΓ©duction S -> S + S 

S 

*4 $ 

DΓ©calage * 

S *  

4 $ 

DΓ©calage 4 

S * 4 

$ 

RΓ©duction C -> 4 

S * C 

$ 

RΓ©duction N -> C 

S * N  

$ 

RΓ©duction S -> N 

S* S 

$ 

RΓ©duction S -> S*S 

S 

$ 

 
 ## 02/12/2021 


E -> E + E  | E *E | N  

Pile 

EntrΓ©e  

Action 


N + N * N 

dΓ©calage 

N  

+ N * N 

Red E -> N 

p(0)   p(1) 

E 

+ N * N 

dΓ©calage 

E + N  

   *  N 

Red E ->N 

E + E    

   * N 

Red E -> E + E  

 

 
