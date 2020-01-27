# Files Search
<img align = "right" src = "https://t00.deviantart.net/9IdCsNFyehXAeUgfS9PsBatjy6k=/fit-in/700x350/filters:fixed_height(100,100):origin()/pre00/5bc8/th/pre/f/ 2017/107 / c / 6 / kevin_is_bored_by_sbolton123-daydh6a.png ">
Kevin and Nazz were admitted to the Faculty of Automation and Computers. Nazz has found an entourage of smart people with
which discusses advanced topics that Kevin has no idea about. He wants to integrate (and conquer Nazz) so it was
read scientific articles. In a regular conversation he hears snippets of words but doesn't even remember articles to get into the word. He will ask you to make a program that receives all the articles read by Kevin because
then he would introduce word fragments and be offered suggestions on words he could speak with
the articles they come from.
As Kevin's articles are technical, they also contain many compound words. He wants to receive
suggestions and if you enter the beginning of a word inside a compound word. We consider a word composed any string
separated by a hyphen.

## Kevin's requirements
  * He does not want his words to be suggested but only the first 5 of the lexicographic sorting of all valid options.
  * He wants to be suggested also the compound words that contain the introduced fragment.
  * He will always enter the first letters of the beginning of a word.
  * Consider word composed any set of alphabet letters separated by a hyphen.
  * He wants the articles of the suggested words to be displayed in the order they are entered.
  * Capital letters should not change their suggestions and should have the same chance of appearing as lowercase words.
  * If there are no suggestions for that word, it wants to be notified by the text `No suggestions ...`

## Input data
  * The names of the files from which the articles will be read will be given as the command line parameters.
  * All files contain ASCII text.
  ``
  ./kevin file1.txt file2.jpg file3.in
  ``
  * The beginning of some words will be read from `stdin`.
  * If you read from `stdin` / exit` the program will end.
  
## Output data
  * After reading each word, the suggested words followed by the string (`:`) and then the order numbers of the articles from which the suggested words come from will be displayed in a line on each line.
  * If the word is not recognized, the phrase `No suggestions ... 'will be displayed in` stdout`
  
## Example
### __ML.txt__:
Machine-learning algorithms are used in a wide variety of applications, such as email-filtering, network-intruders detection, and computer-vision, where it is infeasible to develop an algorithm of specific instructions for performing the task.

### __quicksort.paint__:
Like Merge-Sort, Quick-Sort is a Divide-and-Conquer algorithm. It picks an element as a pivot and partitions the given array around the picked pivot. There are many different versions of quick-Sort that pick pivot in different ways.

### __youtube.database__:
Pew-Die-Pie
Algum-Coise
Universal-Pictures
SORTEDfood
Algorithm

### __randomwords.org.4d__:
different
algorithm
goodsort
quick-algebra
sorting

### `./kevin ML.txt quicksort.paint youtube.database randomwords.org.4d`
### __Studio input__:
apron
ALG
di
pi
food
/ exit

### __Output `stdout`__:
merge - ** sort **: 2
quick - ** sort **: 2
** sort ** edfood: 3
** sort ** ing: 4

** alg ** orithm: 1 2 3 4
** alg ** orithms: 1
** alg ** uma-coisa: 3
quick - ** alg ** ivra: 4

** di ** fferent: 2 4
** di ** vide-and-conquer: 2
pew - ** di ** e-pie: 3
  
pew-die - ** pi ** e: 3
** pi ** ck: 2
** pi ** cked: 2
** pi ** cks: 2
** pi ** vote: 2
  
No suggestions ...

## Run checker
To run the checker, a MAKEFILE file with build, clean and run rules must be created.
  
  ** ATTENTION: ** The run rule must execute the program with the command line parameters,
  by means of the variable ** $ (var) **. An example of a MAKEFILE file for an implemented solution
  in C ++ it is in the archive.
