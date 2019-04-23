# Trumpas įvadas į programavimą

Paprašyti visų parsisiųsti kol kalbėsiu:
1. Chrome naršyklę https://www.google.com/chrome/ .
2. Git for windows https://git-scm.com/download/win .
3. Visual Studio Code https://code.visualstudio.com/download .


## Kas išvis tas programavimas?
Programavimas tai instrukcijų nustatymas kompiuteriui. Kadangi kompiuteriai,
priešingai nei žmonės nėra protingi ir negali patys sugalvoti, kaip jiems
išspręsti užduotis, jiems reikia tiksliai tą nurodyti. Gerai tik tai, kad jie
sugeba atkartoti instrukcijas duotas jiems tobulai. Tobulai reiškia, kad jas
atlieka reikiamu eiliškumu ir be matematinių ar kitokių klaidų.
Kaip pavyzdį duosiu omleto pagaminimą. Instrukcijos kurias duoda mama tau
kai reikia pagaminti omletą:
1. Pakepink daržoves keptuvėj.
2. Išplak kiaušinius.
3. Supilk išplaktus kiaušinius į keptuvę ant daržovių.
4. SUPLAUK INDUS, NES PRAEITĄ KART BETVARKĘ PALIKAI, TINGINY.

Kadangi mes, žmonės, suprantam, kaip interpretuoti šias instrukcijas, ir
elgiamės adekvačiai priklausomai nuo konteksto lengvai pasidarysim valgyt pagal
tokias instrukcijas. Na žinant mano gaminimo sugebėjimus tikriausiai teks pirkt
naują keptuvę, bet pavalgęs būčiau.
Tuo tarpu kompiuteriui neišeitų padaryti nei pirmos užduoties, nei antros, nei
trečios, nei ketvirtos. Kad jis sugebėtų padaryti kiaušinienę jį turėtų
ištreniruoti daryti viską smulkiausiomis detalėmis. Na, šiuo atveju tai jau būtų
robotas, o ne kompiuteris, nes kompiuteris neatlieka mechaninių veiksmų.
Pavyzdys kaip tos pačios instrukcijas reiktų nustatyti kompiuteriui:
1. Pakepink daržoves keptuvėj:
    1. Atsidaryk spintelę ir paimk:
        1. Papriką.
        2. Pomidorą.
        3. ...
    2. Atsidaryk stalčių ir paimk:
        1. Peilį.
        2. Pjaustymo lentelę
        3. ...
    3. ...
2. ...

Visko nerašiau, nes bučiau visą sekmadienį užtrukęs. Ir tai vistiek nebūtų
tikslu, nes vien "atsidaryti spintelę" turėtų būti aprašyta smulkiais veiksmais
kaip rankos kėlimu, traukimu ir panašiai. Užsiknisimas.
Gelbsti tai, kad jei kiti programuotojai jau yra suprogramavę kaip padaryti
"atsidaryk spintelę ir paimk" veiksmą, galima panaudoti jų instrukcijas vietoj
rašymo to paties per tą patį.  Prisiminkit šitą, kai mokysimės apie funkcijas.

## Bet kaip metalo gabalas atlieka matematinius veiksmus?

Parodysiu ant lentos.


## JavaScript pagrindai

### Apie JavaScript
JavaScript yra programavimo kalba, kuria naudojantis sukurta didžioji dalis
internetinių puslapių. Taip pat galima sakyti kad ji yra populiariausia
programavimo kalba pasaulyje. Ją naudoja tokios kompanijos kaip:
1. Apple
2. Microsoft
3. Amazon
4. Google
5. Facebook
6. Bloomberg (čia dirbu aš)
7. Airbnb

Ir tikriausiai bet kuri interetinė bendrovė kurią žinote.
Tuo tarpu brangiausios pasaulio kompanijos yra:

1. Apple
2. Microsoft
3. Amazon
4. Alphabet (Google)

Ką tas reiškia? Tai reiškia, kad pinigų mokant JavaScript tikrai uždirbti
galima.

Tęsiant kalbą apie patį JavaScript, jums gali kilti klausimas, ką jis daro
pačiam internetiniam puslapyje. Bet, kadangi patys tuoj jį sukursite, greit
suprasite.

### Hello World!
Pati pirma pamoka kaip naudoti programavimo kalbą yra vadinama "Hello World!",
nes taip prieš keturiasdešimt metų pirmą C programavimo kalbos pamoką pavadino
jos kūrėjai.
Važiuojam.
Atsidarykite "Chrome". Ir spauskite: <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>J</kbd> (Windows),
<kbd>Cmd</kbd>+<kbd>Alt</kbd>+<kbd>J</kbd> (OsX). Atsidarys console ir tiesiog
parašykite:
```javascript
console.log("Hello World!");
```
Spauskite <kbd>Enter</kbd> ir BAAAAM!!! Kątik parašėt savo pirmąją JavaScript programą. Atrodo kietai? Žinau, kad ne. Bet tęsiam.

### Kintamieji
Kadangi jau esate gimnazijos amžiaus, tikriausiai žinote kas yra kintamasis ir
dažniausiai jį regite pažymėtą kaip ***X***. JavaScript analogija būtų:
```javascript
let x;
```
"let" iš anglų kalbos išvertus reiškia "tebūnie". Tai tiesiog kompiuteriui
pasako, kad *x* šiuo atveju yra kintamasis.
Kaip žinote iš matematikos, kintamiesiems galima priskirti vertes ir tai labai
paprasta JavaScript'e (ir kitose programavimo kalbose).
```javascript
x = 100;
```
Galima šitą užrašyti ir viena eilute:
```javascript
let x = 100;
```

Grįžkime prie pirmojo pavyzdžio ir pabandome:
```javascript
console.log(100); // <--- naudojama 100
let x = 100;
console.log(x);   // <--- naudojama x, kurio verte 100
```
Kaip matote console'je *100* buvo parašyta du kartus. Taip yra dėl to kad
pirmoje eilutėje tiesiog sakoma "atspausdink 100", o trečioje sakoma atspausdink
*x*. Kadangi x nėra kabutėse, tai JavaScript'e reiškia, jog kalbama apie
kintamąjį ir kompiuteris bandys įstatyti jo vertę.
Dabar darome refresh <kbd>Ctrl</kbd>+<kbd>R</kbd> pabandykime:
```javascript
let x;
console.log(x);   // <--- undefined, reiskia kad verte niekada nebuvo priskirta
```
<kbd>Ctrl</kbd>+<kbd>R</kbd> Ir:
```javascript
console.log(x);   // <--- ReferenceError, KAS TAS X???
                  // Turetu but kintamasis bet niekur nepasakyta.
```

### Aritmetika
Kompiuteris yra skaičiuotuvas, tik kietesnis. Žmonės jo labai ta paskirtimi
nenaudoja, o galėtų. Pradedam aritmetiką.
<kbd>Ctrl</kbd>+<kbd>R</kbd>
```javascript
let x = 5;
let y = 3;
let k = x + y; // <-- suma
console.log(k);
k = x - y      // <-- skirtumas
console.log(k);
k = x * y      // <-- sandauga
console.log(k);
k = x / y      // <-- dalyba
console.log(k);
k = x % y      // <-- liekana
console.log(k);
```
Padarome užduotį:
1. *Į kintamąjį **s_kvadrato** priskirkime kvadrato mkurio sienos ilgis 6, plotą.*
2. *Į kintamąjį **s_skritulio** priskirkime skritulio, kurio skersmuo 6, plotą.*
3. *Į kintamąjį **s_atlieka** priskirkime plotą, kuris atlieka įbrėžus skritulį iš **2** į kvadratą iš **1**.*

Iliustracija: ![circle_in_square](./circle_in_square.gif)

### Funkcijos
Žiūrint į kątik išspręstas formules matome, kad tiesiog pritaikoma formulė. Kadangi iš esmės veiksmas yra tas
pats, keičiasi tik kintamasis norėtųsi, kad kompiuteris pats pritaikytų formulę. Gerai, kad tai įmanoma ir tam
yra funkcijos.

***Funkcija*** yra veiksmų seka kuri įvykdoma jai pateikus (arba nepateikus) argumentus.
Funkcija užrašoma taip:
```javascript
function pavadinimas(pirmasArgumentas, antrasArgumentas) {
    pirmasVeiksmas;
    antrasVeiksmas;
    return 5; // Vertė kurią grąžina funkcija
}
```
Viršuje užrašyta funkcija, kurios vardas yra `pavadinimas`, argumentai `pirmasArgumentas` ir `antrasArgumentas`.
Argumentų galėtų būti ir daugiau. Funkcijos *kūnas* apgaubiamas `{}`. `pirmasVeiksmas` ir `antrasVeiksmas` tai tiesiog kodo eilutės kur gali būti bet kas. Atkreipkite dėmesį į `return` raktažodį. Po `return` raktažodžio sekanti vertė tai ta, kurią funkcija grąžina (kuriai tampa lygi).

Funkcijos naudojamos jas šaukiant taip:
```javascript
let sugrazintaVerte = pavadinimas(5, 4);
```
Šiuo atveju naudojama funkcija `pavadinimas`, nes jo uždėti skliausteliai. `pirmasArgumentas` yra 5 ir `antrasArgumentas` yra 4. Taip yra, nes 5 yra pirmas skliaustelyje, o 4 antras. `sugrazintaVerte` bus 5,
nes `pavadinimas` turi `return 5;` gale (visada gražina 5).

Parodysiu labiau praktišką pavyzdį. Prieš tai darytoje užduotyje reikėjo rasti kvadrato plotą. Tai galima užrašyti formule `a*a`, kur `a` tai kvadrato kraštinė. Analogiška funkcija:
```javascript
function kvadratoPlotas(krastinesIlgis) {
    let plotas = krastinesIlgis * krastinesIlgis;
    return plotas;
}
```
Ši funkcija grąžins kvadrato plotą jai pateikus kraštinės ilgį. Kaip matote galima daryti veiksmus funkcijos viduje ir vėliau grąžinti vertę. Ši funkcija būtų naudojama taip:

```javascript
let kvadrato6Plotas = kvadratoPlotas(6);
console.log("Kvadrato, kurio krastine 6 plotas:");
console.log(kvadrato6Plotas);

let kvadrato10Plotas = kvadratoPlotas(10);
console.log("Kvadrato, kurio krastine 10 plotas:");
console.log(kvadrato10Plotas);
```

Funkcija nebūtinai turi grąžinti vertę. Kartais ji reikalinga dėl šalutinių efektų kaip vertės atspausdinimas ekrane. Pavyzdžiui:
```javascript
function graziaiAtspausdinti(vardas, pavarde, profesija) {
    console.log("Pilietis pavarde " + pavarde + ", vardu " + vardas + ", yra " + profesija);
}
```
Ji būtų naudojama taip:
```javascript
graziaiAtspausdinti("Vardenis", "Pavardenis", "Stalius");
graziaiAtspausdinti("Ignas", "Zilinskas", "Noliferis");
```
Panaudojus matome, kad gražiai atspausdinama ir žymiai patogiau užrašyti nei tą ilgą eilutę, kuri yra funkcijoje.

### Logika
Logika programavime sukuriama naudojantis "jeigu" ir "antraip" komandomis. Anglų kalboje tai būtų `if` ir `else`.
Kad logika veiktų reikia tam tikros sąlygos, kuri yra tiesa arba ne. Sąlygų pavyzdžiai
```javascript
5 < 10; // tiesa, verte 'true'
5 > 10; // ne tiesa, verte 'false'

5 <= 10; // tiesa, verte 'true'
5 >= 10; // ne tiesa, verte 'false'

5 == 10;    // palyginimas ar lygu be tipu. Tipai vienodi, bet vertes ne. Gaunasi 'false'.
'5' == 10;  // palyginimas ar lygu be tipu. Tipai ir vertes skirtingi. Gaunasi 'false'.
10 == 10;   // palyginimas ar lygu be tipu. Tipai vienodi ir vertes vienodos. Gaunasi 'true'.
'10' == 10; // palyginimas ar lygu be tipu. Tipai skirtingi, o vertes vienodos. Gaunasi 'true'.

5 === 10;    // palyginimas ar lygu su tipais. Tipai vienodi, bet vertes ne. Gaunasi 'false'.
'5' === 10;  // palyginimas ar lygu su tipais. Tipai skirtingi, vertes irgi. Gaunasi 'false'.
10 === 10;   // palyginimas ar lygu su tipais. Tipai vienodi, vertes irgi. Gaunasi 'true'.
'10' === 10; // palyginimas ar lygu su tipais. Tipai skirtingi, vertes vienodos. Gaunasi 'false'
```
Visada naudokite `===` ir `==` nebent jei reikia kritiniu atveju! Jei norite testuoti ar *nelygu* tada reikia naudoti `!==`.
Dabar panaudokime `if` ir `else` tai labai paprasta:
```javascript
if (5 < 10) {
    console.log("5 maziau uz 10");
}
else {
    console.log("5 daugiau arba lygu 10");
}
```
Kadangi 5 yra mažiau už 10, kodo eilutės esančios `{}` už `if` bus paleistos, o tos kurios yra `{}` už `else` bus praleistos.
```javascript
let a = 5;
let b = 10;
if (a === b) {
    console.log("a lygu b");
}
else {
    console.log("a nelygu b");
}
```
Jei nereikia `else` galima jį tiesiog praleisti:
```javascript
let k = 10;
let l = 10;
if (k === l) {
    console.log("k lygus l!");
}
```

Padarome užduotis:
1. *Naudojantis* `console.log()` *,* `if` *ir* `else` *parašyti funkciją, kuri atspausdina "didesnis", jei funkcijos argumentas didesnis nei 100, ir "ne didesnis" kitu atveju.*
2. *Parašyti funkciją, kuri atspausdina "didesnis", jei funkcijos argumentasdidesnis nei 100, "vienodas" jei skaičius yra 100 ir "mazesnis" jei argumentas mažesnis.*
3. *Parašyti funkciją* `atspekVarda(vardas)`*, kuri grąžina* `true`*, jei funkcijos argumentas jūsų vardas, ir `false` kitu atveju.*

## Ciklai
Dažnai programuojant reikia atlikti tą pačią instrukcijų kombinaciją daug kartų. Tam naudojami ciklai.
JavaScript `for` ciklas, kuris paleis instrukcijas su `i` vertėmis nuo 0 iki 9:
```javascript
for (let i = 0; i < 10; i = i + 1) {
    console.log(i);
}
```
Sintaksės esminis elementas yra `;`. Prieš pirmąjį kabliataškį esanti instrukcija bus įvykdyta vieną kart prieš pradedant ciklą. Po apačia esantis ciklas yra analogiškas ciklui, kuris yra viršuje, nes prieš pirmąjį kabliataškį buvusi instrukcija parašyta prieš pat ciklą.
```javascript
let i = 0;
for (;i < 10; i = i + 1) {
    console.log(i);
}
```
Instrukcija esanti po antrojo kabliataškio paleidžiama prieš pat pradedant naują pakartojimą. Šiuo atveju prie esančios `i` vertės pridedame 1. Analogiškas ciklas:
```javascript
let i = 0;
for (;i < 10;) {
    console.log(i);
    i = i + 1;
}
```
Instrukcija esanti tarp `;` yra tikrinimo instrukcija ir jei tai nėra tiesa, ciklas nebekartojamas. Analogiškas ciklas:
```javascript
let i = 0;
for (;;) {
    if (i >= 10) {
        break; // break baigia cikla
    }
    console.log(i);
    i = i + 1;
}
```
Šiuo atveju buvo panaudota `break` instrukcija, kuri nutraukia ciklą.

Užduotys:
1. Parašykite ciklą, kuris atspausdins visus skaičius nuo 0 iki 99.
2. Parašykite ciklą, kuris atspausdins visus lyginius skaičius nuo 0 iki 98.
3. Parašykite ciklą, kuris atspausdins visų skaičių nuo 0 iki 99 kvadratus.
4. Parašykite ciklą, kuris atspausdins visų skaičių nuo 0 iki 1000 sumą.

## Arrays

```javascript
let k = [];
for (let i = 0; i < 100; ++i) {
    k.push(i);
}
console.log(k);
```