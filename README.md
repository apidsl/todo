
# [todo.apidsl.com](https://todo.apidsl.com/)



## TODO [<span style='font-size:20px;'>&#x270D;</span>](https://github.com/apidsl/todo/edit/main/MD/TODO.md)

### CSV

APIDSL działa domyślnie w oparciu o tekst przesyłany w strumieniu jako wejście.
Brakuje możliwości używania wielu zmiennych jednocześnie w linii
można wykorzystać format CSV do pobierania zmiennych lub JSON.

### Inne formaty strumieniowanych danych
+ JSON
+ yaml

Nowa komenda zamiast domyślnej "echo"

    echo file.json | komenda.sh
    

    echox file.json | komenda.sh


Format JSON/Yaml jest bardziej wymagający i może wymagać translacji do CSV

Docs

https://docs.spring.io/spring-framework/docs/3.2.x/spring-framework-reference/html/expressions.html

// evaluates to true
boolean trueValue = parser.parseExpression("2 == 2").getValue(Boolean.class);

// evaluates to false
boolean falseValue = parser.parseExpression("2 < -5.0").getValue(Boolean.class);

// evaluates to true
boolean trueValue = parser.parseExpression("'black' < 'block'").getValue(Boolean.class);

Logical operators

The logical operators that are supported are and, or, and not. Their use is demonstrated below.

// -- AND --

// evaluates to false
boolean falseValue = parser.parseExpression("true and false").getValue(Boolean.class);

// evaluates to true
String expression =  "isMember('Nikola Tesla') and isMember('Mihajlo Pupin')";
boolean trueValue = parser.parseExpression(expression).getValue(societyContext, Boolean.class);

// -- OR --

// evaluates to true
boolean trueValue = parser.parseExpression("true or false").getValue(Boolean.class);

// evaluates to true
String expression =  "isMember('Nikola Tesla') or isMember('Albert Einstein')";
boolean trueValue = parser.parseExpression(expression).getValue(societyContext, Boolean.class);

// -- NOT --

// evaluates to false
boolean falseValue = parser.parseExpression("!true").getValue(Boolean.class);


// -- AND and NOT --
String expression =  "isMember('Nikola Tesla') and !isMember('Mihajlo Pupin')";
boolean falseValue = parser.parseExpression(expression).getValue(societyContext, Boolean.class);


## Types

The special 'T' operator can be used to specify an instance of java.lang.Class (the 'type'). Static methods are invoked using this operator as well. The StandardEvaluationContext uses a TypeLocator to find types and the StandardTypeLocator (which can be replaced) is built with an understanding of the java.lang package. This means T() references to types within java.lang do not need to be fully qualified, but all other type references must be.

Class dateClass = parser.parseExpression("T(java.util.Date)").getValue(Class.class);

Class stringClass = parser.parseExpression("T(String)").getValue(Class.class);

boolean trueValue =
parser.parseExpression("T(java.math.RoundingMode).CEILING < T(java.math.RoundingMode).FLOOR")
.getValue(Boolean.class);


## Mathematical operators

The addition operator can be used on numbers, strings and dates. Subtraction can be used on numbers and dates. Multiplication and division can be used only on numbers. Other mathematical operators supported are modulus (%) and exponential power (^). Standard operator precedence is enforced. These operators are demonstrated below.

// Addition
int two = parser.parseExpression("1 + 1").getValue(Integer.class); // 2

String testString =
parser.parseExpression("'test' + ' ' + 'string'").getValue(String.class);  // 'test string'

// Subtraction
int four =  parser.parseExpression("1 - -3").getValue(Integer.class); // 4

double d = parser.parseExpression("1000.00 - 1e4").getValue(Double.class); // -9000

// Multiplication
int six =  parser.parseExpression("-2 * -3").getValue(Integer.class); // 6

double twentyFour = parser.parseExpression("2.0 * 3e0 * 4").getValue(Double.class); // 24.0

// Division
int minusTwo =  parser.parseExpression("6 / -3").getValue(Integer.class); // -2

double one = parser.parseExpression("8.0 / 4e0 / 2").getValue(Double.class); // 1.0

// Modulus
int three =  parser.parseExpression("7 % 4").getValue(Integer.class); // 3

int one = parser.parseExpression("8 / 5 % 2").getValue(Integer.class); // 1

// Operator precedence
int minusTwentyOne = parser.parseExpression("1+2-3*8").getValue(Integer.class); // -21


### Mapowanie

skrypty zapisywać w folderze głównym

zamiast w folderach, kazdy skrypt z kropkami
jeśli piszemy 

letwhois.ns()
plik:
letwhois.ns.sh

kazda funkcja jest przepisywana żeby mieć do niej dostęp z jednego poziomu bez przechodzenia po folderach

uproszcenie zarządzania i wyswietlanie listy plików

każda funkcja i tak musi działać autopnimicznie

skrypt instalujący kopiuje wszystkie skrypty bezposrednio

https://github.com/letwhois/bash apidsl/apidsl/bash letwhois

apidsl/apidsl/bash/letwhois/reverseIp.sh 

repozytiorium
https://github.com/letwhois/bash

mapa funkcji
apidsl/apidsl/bash/letwhois/reverseIp.sh reverseIp

1. pobiera cale repo
https://github.com/letwhois/bash

2. wyodrebnia poprzez mapowanie
domainIp.sh domainIp
domainIp.sh letwhois.domainIp






#### mapowanie funkcji z linuxa:
curl().grep("ri",)

#### mapowanie funckji uslug w linux

#### mapowanie API
+ Skąd pobierać dane autoryzacyjne?
 


### Praktyczne przykłady
+ Example with plainedit
+ more loop options
+ many loop in one sentence

install
https://github.com/apidsl/ultimate-nmap-parser


### Inframonit

skanuje hosty
git clone https://github.com/desecsecurity/parsing_html_bash
./parsing_html.sh www.google.com


+ skrypty do detekcji
+ skrypty do naprawy
+ schematy naprawy / template w zalezności od sytuacji



http.get("https://web.com")

$('#cliente').click(function(){$('#container').load('/clienti/cliente.html');});

js.
get("https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js")
.get("https://web.com")
.xpath("title")
.print()


js.
console.log("clone")
jquery.get("simpleargs")
.nano("filename.txt","content")
.git("commit","-m","nowy plik")
.git("push");




### Preprocessing

Każdy z tych jest w fodlerze ze skryptami, gdzie kolejno podaje sie wartosci
+ values
+ context - before, next command

