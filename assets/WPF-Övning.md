# Övning inför Labb 3(4) 

Du får i uppdrag att utveckla ett program där man ska kunna skapa och redigera
gloslistor på olika språk, samt kunna öva på glosor från listorna man lagt in.

Varje ordlista ska sparas som en egen fil med filändelse .csv, och namnet på filen
är namnet på listan. T.ex ’mywords.csv’.</br>
Första raden i filen innehåller namn på språken, separerade med comma. Därefter följer en rad för varje glosa, med översättningarna separerade med comma. Se bifogad [exempel-fil](./Exempelfil.csv).
Alla .csv filer ska lagras i en mapp med samma namn som applikationen under
användarens appdata\local. Om mappen inte redan finns måste applikationen
skapa den.

Klasserna Word samt WordList skall implementeras enligt nedan:

Klassen Word används för att lagra ett enskilt ord och ska ha dessa tre properties:
```cs
public string[] Translations { get; }
public int FromLanguage { get; }
public int ToLanguage { get; }
```
Translations lagrar översättningarna, en för varje språk. Med FromLanguage och
ToLanguage kan man ange för övningar vilket språk som ska översättas till
respektive från. Dessa används av metoden WordList.GetWordToPractice() 
Klassen ska ha även ha konstruktor i två versioner
```cs
//initialiserar ’Translations’ med data som skickas in som ’translations’
public Word(params string[] translations)
```
```cs
//som ovan, fast sätter även FromLanguage och ToLanguage.
public Word(int fromLanguage, int toLanguage, params string[] translations)
```

Klassen WordList består av en lista av typ Word, samt tillhandahåller metoder för
att ladda in och spara listan från .csv; lägga till och ta bort ord; slumpa ord för
övningar; och andra metoder beskrivet enligt nedan:</br>
Properties:
```cs
public string Name { get; } //Namnet på listan.
public string[] Languages { get; } //Namnen på språken.
```
Metoder:
```cs
// Konstruktor. Sätter properites Name och Languages till parametrarnas värden.
public Wordlist(string name, params string[] languages)
```
```cs
//Returnerar array med namn på alla listor som finns lagrade (utan filändelsen).
public static string[] GetLists()
```
```cs
//Laddar in ordlistan (name anges utan filändelse) och returnerar som WordList.
public static Wordlist LoadList(string name)
```
```cs
//Sparar listan till en fil med samma namn som listan och filändelse .csv
public void Save()
```
```cs
//Lägger till ord i listan. Kasta ArgumentException om det är fel antal translations.
public void Add(params string[] translations)
```
```cs
// translation motsvarar index i Languages. Sök igenom språket och ta bort ordet.
public bool Remove(int translation, string word)
```
```cs
//Räknar och returnerar antal ord i listan. 
public int Count()
```
```cs
//sortByTranslation = Vilket språk listan ska sorteras på.showTranslations = Callback som anropas för varje ord i listan.
public void List(int sortByTranslation, Action<string[]> showTranslations)
```
```cs
//Returnerar slumpmässigt Word från listan, med slumpmässigt valda FromLanguage och ToLanguage (dock inte samma).
public Word GetWordToPractice()
```

WPF-applikationen skall kunna göra/visa följande saker:

* Visa en lista av alla ordlistor (filnamnen ifrån appdata/local/"mappen med .csv-filerna")
* Visa alla ord i en lista
* Skapa en ny csv-fil för två förvalda språk
* Lägga till ord i språklistan som är öppen
* Ta bort ord ur den aktiva listan
* Visa hur många ord listan innehåller
* Ha en vy för "träning" där användaren ombes översätta ett slumpat ord ur den öppnade listan. Man ska få fortsätta gissa tills man väljer att sluta. Då ska andelen rätta svar visas (i procent).


## Tips & Hjälp
Environment.GetFolderPath(Environment.SpecialFolder.LocalApplicationData)
returnerar sökvägen till användarens ‘/appdata/local’ mapp
För hantering av filer och mappar, kolla upp följande klasser:<br>
**Path, Directory, StreamWriter, StreamReader**<br>
Tänk på att göra både user input och lagrad data till lower case innan du jämför
dem om du vill att ditt program ska vara case insensitive.

**ListView** kan användas för att visa ordlistorna och **Open-/Save-Dialog** kan användas för att öppna/spara filer. 

Kolla upp **Action** [här](https://docs.microsoft.com/en-us/dotnet/api/system.action-1?view=net-5.0) för mer info kring hur du skapar ett delegate/callback.

Använd valfritt grafiskt ramverk, det måste inte vara WPF

