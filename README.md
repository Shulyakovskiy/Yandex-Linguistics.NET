#Yandex Linguistics API .NET

* Based on RestSharp (http://restsharp.org) to deserealize xml response into .NET objects.
* NUnit (http://www.nunit.org/) using for testing.

###Currently implemented API's
* [Yandex.Predictor](http://api.yandex.ru/predictor/)
* [Yandex.Dictionary](http://api.yandex.ru/dictionary/)
* [Yandex.Translate](http://api.yandex.ru/translate/)
* [Yandex.Speller](http://api.yandex.ru/speller/)
* [Yandex.Inflector](http://export.yandex.ru/inflect.xml)

###Using
```csharp

// Create service object (predictor, dictionary, translator or speller) with app key
var translator = new Translator("xxx");

// Using api call
var translation = translator.Translate("Семь раз отмерь, один раз отрежь",
  new LangPair(Lang.None, Lang.En), null, true);

// Obtained results:
// translation.LangPair = LangPair.RuEn
// translation.Detected.Lang = Lang.Ru
// translation.Text = "Seven times, cut once"

```

One can use these apies with default app keys or get them on this page: http://api.yandex.ru/key/form.xml

All API's coveraged with tests in YandexLinguistics.NET.Tests

###GUI
WinForms GUI app is available for testing.

<img src="http://habrastorage.org/storage3/3a3/65f/e27/3a365fe27b53aeb2878021bc89dc9984.png" alt="GUI sample screen"/>

###License

Yandex-Linguistics.NET is licensed under the Apache 2.0 License.
