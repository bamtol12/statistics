##Espérance de la note

Nous allons calculer l'espérance de la note du test si on choisit toutes les réponses aléatoirement.

La condition du test est suivante :
- Le test contient 8 questions dont 3 questions possèdent deux réponses et 5 questions possèdent une seule réponse.
- Si on choisit bonne réponse, on obtient 1 point
- Si on choisit mauvaise réponse, chaque mauvaise réponse donne -0,5 point.


Calculons d’abord l'espérance de la note pour une question avec une seule réponse.

-----------------------------------

####Question avec 1 reponse

|$X$|$-1,5$|$-1$|$-0,5$|$0$|$0,5$|$1$|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|$P(X)$|${1 \over 16}$|${3 \over 16}$|${4 \over 16}$|${4 \over 16}$|${3 \over 16}$|${1 \over 16}$|

La possibilite de la combinaison des reponses est:  
$\displaystyle \sum_{k=0}^4 \binom{4}{k} = 16$ .

$X=-1,5$  
On aura la note minimum -1,5 si on ne choisit que 3 mauvaises réponses. On choisit 3 mauvaises réponses parmi 3 et 0 bonne réponse parmi 1. Donc $\binom{3}{3} \cdot \binom{1}{0}$

$X=-1$  
On aura -1 si on choisit 2 mauvaises réponses parmi 3 et 0 bonne réponse parmi 1. Donc $\binom{3}{2} \cdot \binom{1}{0}$

$X=-0,5$  
On aura -0,5 si on choisit 3 mauvaises réponses parmi 3 et 1 bonne réponse parmi 1, ou 1 mauvaise réponse parmi 3 et 0 bonne réponses parmi 1. Donc $\binom{3}{3} \cdot \binom{1}{1} + \binom{3}{1} \cdot \binom{1}{0}$

$X=0$  
On aura 0 si on choisit aucune reponse parmi 4, ou 2 mauvaises réponses parmi 3 et 1 bonne réponses parmi 1. Donc $\binom{4}{0} + \binom{3}{2} \cdot \binom{1}{1}$

$X=0,5$  
On aura 0,5 si on choisit 1 mauvaise réponse parmi 3 et 1 bonne réponse parmi 1. Donc $\binom{3}{1} \cdot \binom{1}{1}$

$X=1$  
On aura la note maximum 1 si on choisit 0 mauvaise réponse parmi 3 et 1 bonne réponse parmi 1. Donc $\binom{3}{0} \cdot \binom{1}{1}$

Alors, l'espérance de note pour une question avec une réponse sera :  
${{(-1,5) \cdot 1 + (-1) \cdot 3 + (-0,5) \cdot 4 + 0 \cdot 4 + 0,5 \cdot 3 + 1\cdot 1} \over 16} = -0,25$ 


Calculons ensuite l'espérance de la note pour une question avec deux réponses.

####Question avec 2 reponses

|$X$|$-1$|$-0,5$|$0$|$0,5$|$1$|$1,5$|$2$|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|$P(X)$|${1 \over 16}$|${2 \over 16}$|${3 \over 16}$|${4 \over 16}$|${3 \over 16}$|${2 \over 16}$|${1 \over 16}$|

$X=-1$  
On aura la note minimum -1 si on ne choisit que 2 mauvaises réponses. On choisit 2 mauvaises réponses parmi 2 et 0 bonne réponse parmi 2. Donc $\binom{2}{2} \cdot \binom{2}{0}$

$X=-0,5$  
On aura -0,5 si on choisit 1 mauvaise réponse parmi 2 et 0 bonne réponse parmi 2. Donc $\binom{2}{1} \cdot \binom{2}{0}$

$X=0$  
On aura 0 si on choisit aucune reponse parmi 4, ou 2 mauvaises réponses parmi 2 et 1 bonne réponses parmi 2. Donc $\binom{4}{0} + \binom{2}{2} \cdot \binom{2}{1}$

$X=0,5$  
On aura 0,5 on choisit 1 mauvaise réponse parmi 2 et 1 bonne réponse parmi 2. Donc $\binom{2}{1} \cdot \binom{2}{1}$

$X=1$  
On aura 1 si on choisit 0 mauvaise réponse parmi 2 et 1 bonne réponse parmi 2 ou 2 mauvaises réponses parmi 2 et 2 bonnes réponses parmi 2 . Donc $\binom{2}{0} \cdot \binom{2}{1} + \binom{2}{2} \cdot \binom{2}{2}$

$X=1,5$  
On aura 1,5 si on choisit 1 mauvaise réponse parmi 2 et 2 bonnes réponses parmi 2. Donc $\binom{2}{1} \cdot \binom{2}{2}$

$X=2$  
On aura la note maximum 2 si on choisit 0 mauvaise réponse parmi 2 et 2 bonnes réponse parmi 2. Donc $\binom{2}{0} \cdot \binom{2}{2}$

Alors, l'espérance de note pour une question avec deux réponses sera :  
${{(-1) \cdot 1 + (-0,5) \cdot 2 + 0 \cdot 3 + 0,5 \cdot 4 + 1 \cdot 3 + 1,5 \cdot 2 + 2 \cdot 1} \over 16} = 0,5$ 

-----------------

D'apres la linéarité d'ésperance, l'ésperance de la note du test est:  
$\sum E(\text{note pour une question avec une réponse}) + \sum E(\text{note pour une question avec deux réponses}) \\
= -0,25 \cdot 5 + 0,5 \cdot 3 \\
= 0,25 $
