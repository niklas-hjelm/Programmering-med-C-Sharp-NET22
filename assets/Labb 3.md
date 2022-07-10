# Lab3 – Quiz game!

Du har fått i uppgift att skapa ett grafiskt quiz-spel.</br>
Man ska kunna spela, editera befintligt eller skapa nytt quiz.</br>
Att editera, spela och skapa skall vara separata vyer (UserControls).</br>
Ett quiz skall innehålla flera flervalsfrågor med 3 svarsalternativ till varje fråga. Och sparas som XML, JSON eller CSV. Quiz-filerna skall sparas i appdata/local/"appens namn" 

Det skall finnas en klass för **Question** som har följande properties:
```cs
public string Statement { get; }
public string[] Answers { get; }
public readonly int CorrectAnswer { get; }
```
Det skall finnas en klass för **Quiz** som har följande properties:
```cs
public ICollection Questions { get; }
public string Title { get; }
```
Och följande metoder:

```cs
public Question GetRandomQuestion()
```
```cs
public void AddQuestion(string statement, params string[] answers, int correctAnser)
```
```cs
public void RemoveQuestion(int index)
```

När man spelar spelet skall frågorna slumpas fram och man ska kunna se totala andelen och antalet korrekta svar efter varje fråga.

När man skapar en ny quiz ska man kunna ange titel och skapa frågor tills man är nöjd. När man skapar en fråga ska man kunna lägga till minst 3 svarsalternativ och markera vilket av dessa som är korrekt. Sedan kunna spara till csv/json eller xml.

När man editerar ett quiz så skall man få en överblick av samtliga frågor och välja en av dessa för att kunna ändra dess statement och/eller svarsalternativ.

## Redovisning
Uppgiften ska lösas individuellt.

## Betygskriterier 
### För godkänt:
* Man skall lämna in en planering med tillhörande klassdiagram för arbetet.
* Koden ska fungera enligt ovan beskrivning.
* Programmet skall fungera utan krasch.
* Både att spara och läsa fil skall ske asynkront.
* Både Quiz och Question skall ha lämpliga konstruktorer.
### För väl godkänt krävs även:
* Koden ska vara väl strukturerad och lätt att förstå
* Lösningen ska inte innehålla massa onödig kod.
* Det ska vara skalbart och enkelt att utöka.
* Man ska även implementera extrauppgiften enligt nedan. 

## OBS! Extra uppgift som krävs för VG! 

Som extra uppgift vill kunden gärna ha följande extra funktionalitet:

* Frågor ska kunna ha bilder kopplade till sig.
* Quiz skall sparas i JSON-format.
* Frågorna skall vara ordnade efter ämne så att man kan välja att visa slumpade frågor från antingen ett eller flera ämnen.

# Inlämning sker före deadline.

## Tips och Hjälp

Environment.GetFolderPath(Environment.SpecialFolder.LocalApplicationData)
returnerar sökvägen till användarens ‘/appdata/local’ mapp
För hantering av filer och mappar, kolla upp följande klasser:<br>
**Path, Directory, StreamWriter, StreamReader**<br>
Tänk på att göra både user input och lagrad data till lower case innan du jämför
dem om du vill att ditt program ska vara case insensitive.

**ListView** kan användas för att visa ordlistorna och **Open-/Save-Dialog** kan användas för att öppna/spara filer. 

Kolla upp Asynkron programmering [här](https://docs.microsoft.com/en-us/dotnet/api/system.action-1?view=net-5.0) för mer info kring hur du skapar ett asynkront anrop.

Färdiga frågor: [35 Quiz questions](https://www.welovequizzes.com/multiple-choice-quiz-questions-and-answers/)

JSON: [MS Docs Json](https://docs.microsoft.com/en-us/dotnet/standard/serialization/system-text-json-how-to?pivots=dotnet-5-0)

XML: [MS Docs XML in .net](https://docs.microsoft.com/en-us/dotnet/api/system.xml.xmldocument?view=net-5.0)

[draw.io](https://app.diagrams.net/)

Använd valfritt grafiskt ramverk, det måste inte vara WPF
