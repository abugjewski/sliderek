# Sliderek
Mała biblioteka do zamieszczenia slidera na Twojej stronie.
*Opis dostępny również w języku [angielskim](https://github.com/abugjewski/sliderek/blob/master/README-EN.md)*
- - -
##Spis treści
* [Wprowadzenie](#wprowadzenie)
* [Technologie](#technologie)
* [Instalacja](#instalacja)
* [Sposób użycia](#sposób-użycia)
* [Inspiracja](#inspiracja)
* [Kontakt](#kontakt)
- - -
##Wprowadzenie
Sliderek pozwala użytkownikowi na zamieszenie prostego slidera ze zdjęciami i ich opisem (jeżeli trzeba) na swojej stronie. Z założenia projekt miał być po prostu tym - sliderem. Został jednak zmodyfikowany, by możliwe było jego łatwe zawarcie na (przynajmniej w teorii) dowolnej stronie. Definitywnie wymaga dodatkowych szlifów, jednak powinien zapewnić bazowe funkcjonalności.
- - -
##Technologie
* HTML
* CSS
* Javascript
- - -
##Instalacja
Po pobraniu biblioteki należy zamieścić ją na stronie przez zawarcie plików *sliderek.css* oraz *sliderek.js*, najlepiej w znaczniku \<head>. Przykładowy sposób przedstawia wycinek kodu HTML poniżej:
```html
<head>
    <link rel="stylesheet" href="sliderek/sliderek.css">
    <script src="sliderek/sliderek.js" defer>
</head>
```
- - -
##Sposób użycia
Po zawarciu biblioteki na stronie, we własnym skrypcie javascript należy zawrzeć funkcję *createSliderek()*. Przykładowo:
```javascript
createSliderek(".box", slides);
```
Pierwszy argument odnosi się do elementu na stronie, w którym chcemy zawrzeć slider. Można to zrobić przy pomocy podania klasy lub id elementu. Argument ten powinien być typu *String*.
Drugi argument odnosi się do tablicy obiektów, które zawierają informacje o poszczególnych slajdach. Każdy taki obiekt może posiadać następujący zestaw właściwości:
* **img** - *typ String*. Jest to odnośnik do zdjęcia slajdu.
* **title** - *typ String*. Nagłówek na slajdzie.
* **content** - *typ String*. Opis na slajdzie.
* **slideFrom** - *typ String*. Określa stronę, z której slajd "wjedzie". Może przyjąć wartości *top*, *bottom*, *left* lub *right* (co kolejno oznacza wejście z góry, z dołu, od lewej lub od prawej strony). Domyślna wartość to *top*.
* **contentFrom** - *typ String*. Określa stronę, z której nagłówek i/lub opis slajdu "wjedzie". Może przyjąć wartości identyczne do właściwości *slideFrom*. Domyślna wartość to *top*.
* **contentDelay** - *typ Number*. Określa opóźnienie (w sekundach) pojawienia się nagłówka i/lub opisu slajdu po pojawieniu się jego zdjęcia.

Pełny przykład kodu, w którym użyto dwa slajdy (przy pierwszym nadano wartości wszystkim właściwościom, przy drugim tylko dwóm), prezentowałby się następująco:
```javascript
slides = [
    {
        img: "img/slide1.png",
        title: "Nagłówek1",
        content: "lorem ipsum",
        slideFrom: "left",
        contentFrom: "right",
        contentDelay: 1
    },
    {
        img: "img/slide2.png",
        content: "lorem ipsum",
    }
];

createSliderek(".box", slides);
```
Przykład działania Sliderka można zobaczyć pod [tym linkiem](https://abugjewski.github.io/sliderektest).
- - -

##Inspiracja
Baza dla slidera powstała na podstawie tutoriala youtube, do którego prowadzi ten [link](https://www.youtube.com/watch?v=PDVr7qNytTg).
- - -
##Kontakt
Projekt stworozny przez [Adriana Bugajewskiego](https://abugjewski.github.io/portfolio/). W razie pytań, sugestii lub innych spraw, zapraszam do kontaktu!