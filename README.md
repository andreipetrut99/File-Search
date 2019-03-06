# Replici de agatat
<img align="right" src="https://t00.deviantart.net/9IdCsNFyehXAeUgfS9PsBatjy6k=/fit-in/700x350/filters:fixed_height(100,100):origin()/pre00/5bc8/th/pre/f/2017/107/c/6/kevin_is_bored_by_sbolton123-daydh6a.png">
Kevin si Nazz au fost admisi la Facultatea de Automatica si Calculatoare. Nazz si-a gasit un anturaj de oameni inteligenti cu
care discuta subiecte avansate de care Kevin nu are habar. El doreste sa se integreze (si sa o cucereasca pe Nazz) asa ca s-a
pus pe citit articole stiintifice. Intr-o conversatie uzuala el aude fragmente din cuvinte dar nu isi aminteste si articole pentru a se baga in vorba. El va roaga pe voi sa faceti un program care primeste toate articolele citite de Kevin pentru ca
apoi el sa introduca fragmente de cuvinte si sa i se ofere sugestii despre cuvintele despre care ar putea vorbi impreuna cu
articolele din care provin.
Cum articolele pe care le-a citit Kevin sunt tehnice, acestea contin si foarte multe cuvinte compuse. El vrea sa primeasca
sugestii si daca introduce inceputul unui cuvant din interiorul unui cuvant compus. Consideram un cuvant compus orice sir de caractere
despartit prin cratima.

## Cerintele lui Kevin
  * Nu doreste sa ii fie sugerate toate cuvintele ci doar primele 5 din sortarea lexicografica a tuturor optiunilor valide.
  * Vrea sa ii fie sugerate si cuvintele compuse ce contin fragmentul introdus.
  * El va introduce mereu primele litere de la inceputul unui cuvant.
  * Considera cuvant compus orice set de litere din alfabet despartite prin cratima.
  * Vrea ca articolele cuvintelor sugerate sa fie afisate in ordinea in care sunt introduse.
  * Cuvintele cu majuscule nu ar trebui sa ii schimbe sugestiile si trebuie sa aiba aceeasi sansa de a aparea ca si cuvintele scrise cu litera mica.
  * Daca nu exista sugestii pentru cuvantul respectiv, vrea sa fie notificat prin textul `No suggestions…`

## Date de intrare
  * Numele fisierelor din care se vor citi articolele se vor da ca parametrii liniei de comanda.
  * Toate fisierele contin text ASCII.
  ```
  ./kevin file1.txt file2.jpg file3.in
  ```
  * Se vor citi de la `stdin` inceputurile unor cuvinte.
  * Daca se citeste de la `stdin` `/exit` programul se va termina.
  
## Date de iesire
  * Dupa citirea fiecarui cuvant se va afisa la `stdout` pe cate o linie cuvantele sugerate urmate de stringul (` : `) si apoi de numerele de ordine ale articolelor din care provin cuvintele sugerate.
  * Daca cuvantul nu este recunoscut, se va afisa la `stdout` sintagma `No suggestions...`
  
## Exemplu
### __ML.txt__ :
Machine-learning algorithms are used in a wide variety of applications, such as email-filtering, detection of network-intruders, and computer-vision, where it is infeasible to develop an algorithm of specific instructions for performing the task.

### __Language.paint__ : 
The European **la**nguages are members of the **sa**me family. Their separate existence is a myth. For science, music, sport, etc, Europe uses the **sa**me vocabulary. The **la**nguages only differ in their grammar, their pronunciation and their most common words.

### __youtube.database__ :
S-**lang**
**La**mborghini
Work-around
**La**dy-bird  
**La**dy-**bu**g  
**La**ke-side  
**Sa**feboat  
Minor-**sa**fe  
**La**ke-bed  
**sa**me  
**bu**tter-fly  
**bu**tter-milk  

### __analemma.4d__ :
**Sa**feguard  
**Sa**feboat  
**sa**me  
**La**ke-bed  
man-**lang**os-pig  

### `./kevin Language.paint youtube.database analemma.4d`
### __Input `stdio`__ :
sa  
bu  
la  
Lang  
bo  
/exit  

### __Output `stdout`__ :
minor-**sa**fe : 2  
**sa**feboat : 2 3  
**sa**feguard : 3  
**sa**me : 1 2 3  
  
**bu**tter-fly : 2  
**bu**tter-milk : 2  
lady-**bu**g : 2  
  
**la**dy-bird : 2  
**la**dy-bug : 2  
**la**ke-bed : 3 2  
**la**ke-side : 2  
**la**mborghini : 2  
  
**lang**uages : 1  
man-**lang**os-pig : 3  
s-**lang** : 2  
  
No suggestions...





