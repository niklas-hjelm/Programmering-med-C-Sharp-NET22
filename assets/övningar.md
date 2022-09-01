1.	Skriv ett program som frågar efter användarens namn och skriver ut en hälsning på konsolen. Om namnet är "David" ska det skriva ut "Hej David!"

2.	Skriv ett program som frågar användaren efter ett lösenord. Hitta på ett hemligt lösenord och spara det i en variabel. När användaren har skrivit in ett lösenord ska programmet jämföra med det sparade lösenordet och skriva ut om det var rätt eller inte. Använd en if-sats.

3.	Skriv ett program som frågar användaren efter ett tal. Det ska skriva ut om talet är mindre än 100, lika med 100 eller större.

4.	Uppdatera programmet i uppgift 1 så att det även frågar efter ett tal. Skriv hälsningen så många gånger som användaren anger.

5.	Skriv ett program som upprepade gånger frågar användaren efter ett tal ända till man skriver något som inte är ett tal (t.ex bara trycker enter). Efter varje inmatning ska summan av alla tal som matats in skrivas ut, innan nästa inmatning efterfrågas. Innan programmet avslutas ska man även skriva ut medelvärde av de inmatade talen. Hint: TryParse()

6.	Skriv ett program som först frågar efter ett tal, sedan frågar efter ett av följande tecken: +, -, * eller /. Därefter ska ytterligare ett tal efterfrågas. Programmet ska fungera som en simpel miniräknare. Om man t.ex matat in först 3, sedan *, och sist 5, så ska programmet skriva ut “3 * 5 = 15”.

7.	Skriv ett program som ber användaren skriva in en månad. Programmet ska göra om månaden till månadens siffervärde. T.ex. ska januari bli 1 och december 12. Använd switch.
Alternativ: Prova även att lösa uppgiften med array och/eller enum.

    **Extra utmaning:** Be användaren om två månader och räkna sedan ut hur många månader som skiljer mellan dem. Tänk på att ett månaderna upprepas till nästa år. Skriver man mars och maj bör man få 2. Likaså om man skriver november och januari.

8.	Skapa ett program som skriver ut 1 på första raden, 2 på nästa, sedan 4, o.s.v (dubbelt så hög siffra för varje rad). Fortsätt till du skrivit ut 16 rader.

9.	Skriv ett program som frågar användaren efter ett tal mellan 1 och 100. Programmet ska ha ett hemligt tal lagrat i en variabel. Det ska fortsätta fråga användaren till dess att användaren gissar det hemliga talet. Om man gissade för högt eller för lågt så ska det skrivas ut, så att användaren har en rimlig chans att klara det.
Exempel: programmet har det hemliga talet 27. Användaren gissar på 50. Programmet skriver ut att användaren gissade för högt. Användaren gissar på 20. Programmet skriver ut att det var för lågt. Användaren gissar på 27. Programmet skriver ut att det var rätt och avslutas.

    **Extra utmaning:** slumpa det hemliga talet med hjälp av Random (kolla upp på google hur det fungerar). Spara antalet gissningar i en variabel och skriv ut det när användaren gissat rätt.

    **Extra utmaning 2:** skriv ett sten-sax-påse spel. Användaren skriver in “sten”, “sax” eller “påse”. Dators val slumpas med Random. Skriv sedan ut vad datorn valde, och vem som vann omgången. Lägg det hela i en loop så spelet fortsätter tills man matar in en tom sträng (trycker enter utan att skriva något). Skriv även ut poäng.
    
10.	Be användaren mata in en sträng. Skriv ut varje tecken i strängen på en egen rad.
Ex: Hej =>
H
e
j

11.	Skapa ett program med en array som innehåller strängarna “noll”, “ett”, “två”, “tre”, “fyra”, “fem”, “sex”, “sju”, “åtta”, “nio”. Be sedan användaren att mata in en siffra. Använd arrayen för att skriva ut siffrans ord. Ex. Inmatning “3” => “tre”.

    **Extra utmaning:** Användaren kan mata in en sträng med fritt antal siffror, om man skriver in t.ex 432 så svarar programmet: “fyra-tre-två”.

12.	Fråga användaren hur många tal den vill mata in. Fråga sedan efter talen i tur och ordning (“Ange tal 1:” osv). När alla tal är inmatade skriv ut dem i omvänd ordning.

13.	Be användaren mata in en text. Skriv sedan ut texten baklänges.

14.	Be användaren mata in en text. Skriv ut texten med alla vokaler ersatta med *

    **Extra utmaning:** Skriv ut texten översatt till rövarspråket.

15.	Ett palindrom är ett ord som blir samma framlänges som baklänges. Be användaren skriva in ett ord och ange sedan om det är ett palindrom eller inte.

16.	Gör om uppgift 6 så man kan mata in allt på en rad (första talet, operator, andra talet). Ignorera inmatade mellanslag i strängen. Om man t.ex. matar in strängen 
“34 - 14”, så ska programmet skriva ut “= 20”.
