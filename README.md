ModifiedWarUML
==============

Modified War Card Game UML and Problem Domain
The problem domain is comprised of: Card1, Card2, Deck, and Class (rank only). The function assesses the value by rank only.
The problem domain is the randomly chosen value of Card1 compared to that of Card2, per hand.
The UML diagram was saved to the Wiki. https://www.draw.io/#LModifiedWarUML 

<!DOCTYPE html>
<!--[if lt IE 7]>      <html class="no-js lt-ie9 lt-ie8 lt-ie7"> <![endif]-->
<!--[if IE 7]>         <html class="no-js lt-ie9 lt-ie8"> <![endif]-->
<!--[if IE 8]>         <html class="no-js lt-ie9"> <![endif]-->
<!--[if gt IE 8]><!--> <html class="no-js"> <!--<![endif]-->
    <head>
        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <title></title>
        <meta name="description" content="">
        <meta name="viewport" content="width=device-width, initial-scale=1">

        <!-- Place favicon.ico and apple-touch-icon.png in the root directory -->

        <link rel="stylesheet" href="css/normalize.css">
        <link rel="stylesheet" href="css/main.css">
        <script src="js/vendor/modernizr-2.6.2.min.js"></script>
		<script>
//Modified War Card Game, where each card number is comprised of rank.
//Ranks are a string from the 0 to 13.
//First, does the rank equal Joker? You lose, because you got 0.
//Second, does the rank equal Ace? You win, because you got 13.
//Third, is the rank less than Ace, but less than the other card? You lose.
//Fourth, is the rank less than Ace, but higher than the other card? You win.
//The two classes of objects are deck and card, but the suit is irrelevant in this game, because card value is the rank and determines outcome.
function Deck() {
this.cards = [];
this.count = function() {
return this.cards.length;
}
this.init = function() {
//for (s = 1; s <= 4; s++) {
for (r = 1; r <= 13; r++) {
this.cards.push(new Card(r, s));
//}
}
}
}
//First, does the card number equal Joker? You lose, because you got 0.
function Card(rank, == Joker) {
this.rank = rank;
//this.suit = suit;
this.show = function() {
console.log(this.rank + " loses. Oh, no!");
//Second, does the card number equal Ace? You win, because you got 13.
function Card(rank, == Ace) {
this.rank = rank;
this.show = function() {
console.log(this.rank + " wins. Congratulations!");
//Third, is the card number less than Ace? You could win if the other card is less than yours.
function Card(rank > Joker && < Ace && < card1) {
this.rank = rank;
this.show = function() {
console.log(this.rank + "loses to the other card. Try again!");
//This is where the other card wins.
function Card(rank > Joker && < Ace && > card1) {
this.rank = rank;
this.show = function() {
console.log(this.rank + "wins. Great job!");
}
}
d = new Deck();
d.init();
</script>
    </head>
    <body>
        <!--[if lt IE 7]>
            <p class="browsehappy">You are using an <strong>outdated</strong> browser. Please <a href="http://browsehappy.com/">upgrade your browser</a> to improve your experience.</p>
        <![endif]-->

        <!-- Add your site or application content here -->
        <p>Hello world! This is HTML5 Boilerplate.</p>

        <script src="//ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
        <script>window.jQuery || document.write('<script src="js/vendor/jquery-1.10.2.min.js"><\/script>')</script>
        <script src="js/plugins.js"></script>
        <script src="js/main.js"></script>

        <!-- Google Analytics: change UA-XXXXX-X to be your site's ID. -->
        <script>
            (function(b,o,i,l,e,r){b.GoogleAnalyticsObject=l;b[l]||(b[l]=
            function(){(b[l].q=b[l].q||[]).push(arguments)});b[l].l=+new Date;
            e=o.createElement(i);r=o.getElementsByTagName(i)[0];
            e.src='//www.google-analytics.com/analytics.js';
            r.parentNode.insertBefore(e,r)}(window,document,'script','ga'));
            ga('create','UA-XXXXX-X');ga('send','pageview');
        </script>
    </body>
</html>
