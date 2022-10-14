# Lab2 – Skapa en simpel butik

Skapa en konsollaplikation som skall agera som en enkel affär.
När programmet körs så ska man få se någon form av **meny** där man ska kunna välja att **registrera ny kund** eller **logga in**. Därefter ska ytterligare en **meny** visas där man ska kunna välja att **handla**, **se kundvagn** eller **gå till kassan**. 

Om man väljer att handla ska man få upp **minst 3 olika** **produkter** att köpa (t.ex. Korv, Dricka och Äpple). Man ska se **pris** för varje **produkt** och kunna lägga till vara i **kundvagn**. 

Kundvagnen ska visa alla produkter man lagt i den, styckpriset, antalet och totalpriset samt totala kostnaden för hela kundvagnen.
Kundvagnen skall sparas i kund och finnas tillgänglig när man loggar in.

När man ska Registrera en ny kund ska man ange Namn och lösenord. Dessa ska sparas och namnet ska inte gå att ändra.

Väljer man Logga In så ska man skriva in namn och lösenord. Om användaren inte finns registrerad ska programmet skriva ut att kunden inte finns och fråga ifall man vill registrera ny kund. Om lösenordet inte stämmer så ska programmet skriva ut att lösenordet är fel och låta användaren försöka igen.

Både kund och produkt ska vara separata klasser med **Properties** för information och metoder för att räkna ut totalpris och verifiera lösenord.

I klassen Kund skall det finnas en ToString() som skriver ut Namn, lösenord och kundvagnen på ett snyggt sätt.

Exempel:
```cs
    public class Customer 
    {
        public string Name { get; private set; }

        private string Password { get; private set }

        private List<Product> _cart;
        public List<Product> Cart { get { return _cart; } }

        public Customer(string name, string password)
        {
            Name = name;
            Password = password;
            _cart = new List<Product>();
        }
    }
```

## Redovisning
Uppgiften ska lösas individuellt eller i par. </br>
OBS! Väljer man att jobba i par skall man arbeta i samma repository.
Det skall vara tydligt vem som gjort vad.
Lämna in uppgiften på ithsdistans med en kommentar med github-länken. </br>

## Betygskriterier 
### För godkänt:
* Koden ska fungera enligt ovan beskrivning.
* Man ska kunna få ut korrekt totalpris och antal i kundvagnen. 
* ToString() ska vara implementerad.
* Programmet skall fungera utan krasch.
* Det skall gå att skapa ny kund, lägga till föremål i kundvagnen, titta i sin kundvagn och sedan fortsätta handla.
* Log in ska fungera för minst 3 fördefinierade kunder.
  * Kund1: Namn="Knatte", Password="123"
  * Kund2: Namn="Fnatte", Password="321"
  * Kund3: Namn="Tjatte", Password="213"
* Det skall gå att logga ut och in men inget krav på att skapade kunder skall finnas kvar emellan körningar.
### För väl godkänt krävs även:
* Koden ska vara väl strukturerad och lätt att förstå
* Lösningen ska inte innehålla massa onödig kod.
* Det ska vara skalbart och enkelt att utöka.
* Man ska även implementera extrauppgiften enligt nedan. 

## OBS! Extra uppgift som krävs för VG! 

Som Extra uppgift ska man på något sätt implementera 3 nivåer av kund (Gold, Silver och Bronze), dessa ska ha olika mycket rabatt. 

* Gold: 15% rabatt på hela köpet
* Silver: 10% rabatt på hela köpet
* Bronze: 5% rabatt på hela köpet

Nivåerna skall implementeras med hjälp av arv av basklassen Kund.

Programmet ska också spara alla registrerade kunder så att de går att använda emellan körningar. (OBS! Kundvagnar behöver ej sparas) Tips: textfil.

Man ska också kunna välja att se priser i minst 3 olika valutor (två ytterligare förutom SEK).


# Inlämning sker före deadline.