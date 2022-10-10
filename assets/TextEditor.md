# TextEditor

Klona följande repo: [TextEditor](https://github.com/niklas-hjelm/TextEditorOvning)

Detta är en väldigt simpel text-editor som nyttjar kontrollen RichTextBox för att låta användaren skriva formatterad text.

I applikationen finns "Open"- och "Save"-funktionalitet som nyttjar något som heter Commands. Commands är ett sätt att hantera logik baserat på händelser, likt events men  istället för att skickas till alla som lyssnar så kör Commands en angiven metod. För Save och Open nyttjar vi inbyggda kommandon som ger oss kortkommandon "Ctrl+S" och "Ctrl+O" för att spara och öppna. Däreftre kopplas en metod på som körs efter att kommandot körts.

Ett Command har tre delar, "CanExecute" en metod som körs för att se om det går att utföra kommandot, "Execute" Själva händelsen, slutligen anropas "Executed" där vi kan utföra operationer efter att ett kommando utförts.

I vårat exempel använder vi det inbyggda Open/Save och får därigenom både "CanExecute" och "Execute" men har specificerat egna "Executed" för båda som talar om vad som ska hända efter att öppna/spara-dialogerna är färdiga.

[Commands WPF Tutorial](https://wpf-tutorial.com/commands/using-commands/)

### Mer information om fler inbyggda commands finns på dessa länkar (Obs! Detta är ej menat som utantillkunskap. Det viktiga är att känna till att de existerar och hur ni hittar dem när de behövs):
  * [Application Commands](https://docs.microsoft.com/en-us/dotnet/api/system.windows.input.applicationcommands?redirectedfrom=MSDN&view=net-6.0)
  * [Component Commands](https://docs.microsoft.com/en-us/dotnet/api/system.windows.input.componentcommands?redirectedfrom=MSDN&view=net-6.0)
  * [Navigation Commands](https://docs.microsoft.com/en-us/dotnet/api/system.windows.input.navigationcommands?view=net-6.0)

  * [EditingCommands](https://docs.microsoft.com/en-us/dotnet/api/system.windows.documents.editingcommands?view=net-6.0)

  * [MediaCommands](https://docs.microsoft.com/en-us/dotnet/api/system.windows.input.mediacommands?view=net-6.0)


## Övning

1. I ToolBar lägg till en TextBox, ComboBox eller Slider för att sätta storleken på all texten i RichTextBox.
2. Lägg till 3st Buttons eller ToggleButtons för att sätta texten till Fet/Kursiv/Understruken (Tips, det finns inbyggda commands för detta).
3. **Extra** Lägg till en ComboBox för val av typsnitt. (Tips är att skapa en Lista i xaml.cs med FontStyles och binda ItemsSource till den)

### Resurser:
* [ToolBar](https://wpf-tutorial.com/common-interface-controls/toolbar-control/)
* [RichTextBox](https://wpf-tutorial.com/rich-text-controls/introduction/)
* [ComboBox](https://wpf-tutorial.com/list-controls/combobox-control/)
* [Slider](https://wpf-tutorial.com/misc-controls/the-slider-control/)