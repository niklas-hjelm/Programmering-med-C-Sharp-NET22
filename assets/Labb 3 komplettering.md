# Lab3 – Butiksapplikation

Du har fått i uppgift att skapa WPF-applikation som representerar en butik.</br>
Applikationen ska ha 4 olika vyer (UserControls):
* Start - Här ska man kunna välja att logga in som kund eller butiksägare(admin).
  * Antingen navigeras man till ny vy för att loggas in eller så har man två loginformulär på startsidan. 
* Admin - Här ska butiksägare kunna lägga till varor i lagret samt, både nya varor och fler av redan befintliga varor. Butiksägaren ska också kunna se hela lagret med styckpriser för varor och totala summan för varje vara (alltså antaler multiplicerat med styckpriset). 
* Kundprofil - Här ska kunden kunna se sitt användarnamn och sin kundkorg. 
* Shop - Här ska användaren kunna handla, alltså lägga till varor utifrån sortimentet i sin kundvagn.
Både butikslager och användare ska sparas till fil och förändringar ska bestå om man stänger av och startar applikationen igen. Filer ska som JSON. Butiks-filerna skall sparas i appdata/local/"appens namn"/butik och kundfiler i appdata/local/"appens namn"/kunder.

Det skall finnas en klass för **Butik** som har följande properties:
```cs
public string Namn { get; set; }
//Dictionary product, int är produkten och hur många som finns i lager
public Dictionary<Product, int> Lager { get; set; }
public User Admin { get; set;}
```
Och följande metoder:
```cs
 // ska kolla om rätt admin försöker logga in och sätta property Admin om det lyckas. 
 //Returnerar false om det inte går och true om det går
public bool LogInAdmin(User user)
// Checkout ska tömma kundkorgen, anropa med await och visa en dialog när den är klar.
public async Task CheckOut(User kund)
```
Det skall finnas en klass för **Produkt** som har följande properties:
```cs
public string Namn { get; set; }
public double Price { get; set; }
```
Det skall finnas en klass för **User** som har följande properties:
```cs
public string Namn { get; set; }
//Dictionary product, int är produkten och hur många som finns i kundkorgen
public Dictionary<Product, int> Kundkorg { get; set; }
public string Password { get; set;}
```

Man ska kunna logga ut och sedan in igen, alltså kunna ta sig från alla vyer tillbaka till start.

Man ska kunna gå från **Shop** till **Kundprofil** och tillbaks för att kunna handla, se sin kundkorg och sedan fortsätta handla.

## Redovisning
Uppgiften ska lösas individuellt.

## Betygskriterier 
### För godkänt:
* Man skall lämna in en planering med tillhörande klassdiagram för arbetet **Deadline för planering och klassdiagram: 19/12-2021**.
* Koden ska fungera enligt ovan beskrivning.
* Programmet skall fungera utan krasch.
* Både att spara och läsa fil skall ske asynkront.
* Alla klasser skall ha lämpliga konstruktorer.
### För väl godkänt krävs även:
* Koden ska vara väl strukturerad och lätt att förstå
* Lösningen ska inte innehålla massa onödig kod.
* Det ska vara skalbart och enkelt att utöka.
* Man ska även implementera extrauppgiften enligt nedan. 

## OBS! Extra uppgift som krävs för VG! 

Som extra uppgift vill kunden gärna ha följande extra funktionalitet:

* Produkter ska kunna ha bilder kopplade till sig.
* Man ska kunna filtrera lagret och affären efter produkttyp.

# Inlämning sker före deadline.

## Tips och Hjälp

Environment.GetFolderPath(Environment.SpecialFolder.LocalApplicationData)
returnerar sökvägen till användarens ‘/appdata/local’ mapp
För hantering av filer och mappar, kolla upp följande klasser:<br>
**Path, Directory, StreamWriter, StreamReader**<br>
Tänk på att göra både user input och lagrad data till lower case innan du jämför
dem om du vill att ditt program ska vara case insensitive.

**ListView** kan användas för att visa produktlistor och kundkorg och **Open-/Save-Dialog** kan användas för att öppna/spara filer. 

Kolla upp Asynkron programmering [här](https://docs.microsoft.com/en-us/dotnet/api/system.action-1?view=net-5.0) för mer info kring hur du skapar ett asynkront anrop.

JSON: [MS Docs Json](https://docs.microsoft.com/en-us/dotnet/standard/serialization/system-text-json-how-to?pivots=dotnet-5-0)

[draw.io](https://app.diagrams.net/)
