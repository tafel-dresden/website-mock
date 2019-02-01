# Content Manage System (CMS) Evaluierung
CMS Wahl könnte stärkere Auswirkungen darauf haben welche Möglichkeiten wir im Frontend haben.

## Anforderungen / gewünschte Features

// TODO add user stories as github issues?

- Finanzen, Übersicht, Tortendiagramm
- Fakten aus Tätigkeitsbericht und Weitere darstellen
- Verweis auf Projekte (ZurTonne), Kooperationen 
- Nächste Veranstaltungen
- Tafelkunde werden mit Assistent
- Mitarbeiten Assistent
- Sozialstunden leisten -> suchmaschinenrelevant
- Bundesfreiwilligendienst leisten - suchmaschinenrelevant
- für Benachrichtigungen registrieren (auswählen: facebook, twitter, instagram, whatsapp, telegram, signal, slack)

e. V. -> Satzung, Vereinsmitglied werden, Fördermitglied werden, Selbstverständnis

Nice to have:
- Barrierefreiheit
- Mehrsprachigkeit, beginnend mit Englisch


## Kanditan
__PHP__
* https://www.concrete5.org/
* https://de.wordpress.org/
* https://www.drupal.de/
* https://octobercms.com/
* https://bolt.cm/
* https://getgrav.org/
* https://www.neos.io
* https://contao.org/de/

__JS__
* https://www.endurojs.com/docs/what-is-enduro
* https://keystonejs.com/
* https://strapi.io/
* https://apostrophecms.org/

__Java__
Java CMS sind tot... oder zu "enterprise"

## Welche Programmiersprache?

__PHP?__
+ persönliche Erfahrung: ~4 Jahre 
- eingerostet (~3 Jahre her)
- andere Entwickler mögen anscheinend kein PHP =(
+ Native Objekt Orientierung

__JS?__
+ persönliche Erfahrung: ~2 Jahre
- eingerostet (~5 Jahre her)
- persönlich wenig Erfahrung mit NodeJS und die NodeJS-Welt
+ es gibt gefühlt mehr Leute die NodeJS entwickeln
+ Erfahrugen mit NodeJS bringen persönlichen Mehrwert
+ Frontend ist auch in JavaScript...

### Battle!

```
PHP     JS
+--+ vs +--+++
-1      2
```

## Welches CMS?

### Kriterien

* Dokumentation Dev / Src
* Offene github Issues
* Stackoverflow Fragen
* Verfügbare Plugins
* Update Frequenz / Stabilität
* Geile Features o.O
* Benötigte Features (ein ! bedeutet wichtig)
  * !Content Pflege (... standard für CMS)
  * !Multilanguage
  * !Templating
  * !Rechte System
  * !User Verwaltung
  * Datenbank Anbindung / Persistence
  * API
  * Analytics
  * PayPal + evtl. weitere Payment Anbindungen
  * Social Media Anbindung

### Battle!

### https://www.concrete5.org/

#### Dokumentation Dev / Src
https://documentation.concrete5.org/developers  
https://github.com/concrete5/concrete5  
* Die __Entwickler Doku__ sieht ganz brauchbar aus. Könnte aber einiges mehr an Beispiele vertragen und allgemein bessere Veranschaulichungen.
* Der __Quellcode__ ist so gut wie gar nicht dokumentiert... eijeijei

6  / 2  

#### Offene github Issues
https://github.com/concrete5/concrete5/issues  
669  

#### Stackoverflow Fragen
https://stackoverflow.com/questions/tagged/concrete5  
562  

#### Verfügbare Plugins
https://www.concrete5.org/marketplace/addons  
~511  
nicht alle gratis  

https://www.concrete5.org/marketplace/addons/ez-paypal :heavy_check_mark:  

#### Update Frequenz / Stabilität
https://github.com/concrete5/concrete5/pulse/monthly  

```
Excluding merges, 11 authors have pushed 97 commits to develop and 98 commits to all branches. On develop, 371 files have changed and there have been 12,947 additions and 5,761 deletions.
```

Merged PR: 17  
Proposed PR: 6  
Closed Issues: 2  
New Issues: 6  

https://www.concrete5.org/developers/bugs  
(bug tracker ist bugged)... alle Bugs stehen in der Übersicht auf "New", auch wenn sie "beantwortet / gelöst" worden -___-  
  
https://travis-ci.org/concrete5/concrete5/jobs/485987798  
Tests: 1818, Assertions: 5514, Skipped: 7, Incomplete: 6.  

#### Geile Features o.O  
https://www.concrete5.org/about/feature-index  



### https://de.wordpress.org/

#### Dokumentation Dev / Src
https://codex.wordpress.org/  
https://github.com/WordPress/WordPress  
* Die __Entwickler Doku__ ist sehr umfassend, sieht aber ziemlich "historisch gewachsen" aus. Viel Text, mittelmäßig viele Beispiele. Bräuchte mal ne Überholung :x
* Owww man, der __Code__... oldskool PHP. Aber ziemlich gut dokumentiert, sogar mit Beispielen. Leider fehlt mir ein wenig das "warum die Sachen hier sind und wofür sie gut sind". Es ist oft nur die "Funktion der Funktion" erklärt. Also der Code nochmal in Prosa wiedergegeben. Wenn Code selbst gut geschrieben / strukturiert ist, brauch er eigentlich keine weitere Erklärung, da man den Code selbst lesen kann. Da sind "warum die Sachen hier sind und wofür sie gut sind" Kommentare wertvoller :P

7 / 7

#### Offene github Issues
k.A.

#### Stackoverflow Fragen
https://stackoverflow.com/questions/tagged/wordpress  
152092  

#### Verfügbare Plugins
https://de.wordpress.org/plugins/  
~227  
alle gratis  

https://de.wordpress.org/plugins/paypal-donations/ :heavy_check_mark:  


#### Update Frequenz / Stabilität
https://github.com/WordPress/WordPress/pulse/monthly  
keine PR / Issues Statistiken  

```
Excluding merges, 19 authors have pushed 308 commits to master and 341 commits to all branches. On master, 594 files have changed and there have been 40,668 additions and 245,142 deletions.
```

https://core.trac.wordpress.org/search?q=error  
11648 Ergebnisse  
einige geschlossen / einige offen  

#### Geile Features o.O
https://de.wordpress.org/about/features/  



### https://www.drupal.de/

#### Dokumentation Dev / Src
https://api.drupal.org/api/drupal  
https://www.drupal.org/documentation  
https://github.com/drupal/drupal
* Die __Entwickler Doku__ sieht sehr nice aus. Man merkt, dass Drupal ein sehr "customisierbares" CMS ist - wenn man die Entwicklingszeit investiert. Es gibt eine online Entwickler Doku, ein Cookbook und eine Code API Doku mit Beispielen. 
* Der __Quellcode__ ist seeehr "standard" dokumentiert. Das sieht schon fast generiert aus. Hier ein Beispiel:

```php
  protected function getForumStatistics($tid) {
```

Die Funktion heißt ```getForumStatistics```. Spoiler: Die wird wahrscheinlich irgendwelche Forum Statistiken zurück geben. Und übergeben bekommt sie eine ```$tid```, was höchstwahrscheinlich irgend ein Identifikator ist (```$tId```, würde das noch klarer machen). Jetzt die Dokumentation dazu:

```php
  /**
   * Provides statistics for a forum.
   *
   * @param int $tid
   *   The forum tid.
   *
   * @return \stdClass|null
   *   Statistics for the given forum if statistics exist, else NULL.
   */
   protected function getForumStatistics($tid) {
```

(－‸ლ) Der einzige Mehrwert sind die @param und @return Annotationen, der Rest ist sinnlos... Mehr?!

```php
/**
 * Provides forum manager service.
 */
class ForumManager implements ForumManagerInterface {
```

Super! Die Klasse ```ForumManager``` stellt den "forum manager service" zur Verfügung. Würde die Klasse ```ForumManagerService``` heißen, dann wäre das sowieso schon nichtssagende Kommentar: nichtsstagend². Und wofür ist der Service gut und welche Rolle spielt er für das (in dem Fall) Forum Modul? -_______-
  
// END OF RANT  

Der __Code__ ist aber nicht überall so dokumentiert, dennoch macht diese Art der Doku den größten Anteil aus.
Inline Kommentare sind recht wenig vorhanden, der Code ist aber gut strukturiert und leicht lesbar. Manchmal schachteln die if-Blöcke schon ziemlich hart an der Schachtelgrenze, aber das ist eher die Ausnahme.

8 / 5  


#### Offene github Issues
k.A.

#### Stackoverflow Fragen
https://stackoverflow.com/questions/tagged/drupal  
19075  

#### Verfügbare Plugins
https://www.drupal.org/project/project_module  
~42397  

https://www.drupal.org/project/paypal_donations :heavy_check_mark:  


#### Update Frequenz / Stabilität
https://github.com/drupal/drupal/pulse/monthly  
keine PR / Issues Statistiken  

```
Excluding merges, 11 authors have pushed 52 commits to 8.6.x and 175 commits to all branches. On 8.6.x, 107 files have changed and there have been 2,352 additions and 543 deletions. 
```

#### Geile Features o.O
https://www.drupal.org/about  



### https://octobercms.com/
#### Dokumentation Dev / Src
#### Offene github Issues
#### Stackoverflow Fragen
#### Verfügbare Plugins
#### Update Frequenz / Stabilität
#### Geile Features o.O

### https://bolt.cm/
#### Dokumentation Dev / Src
#### Offene github Issues
#### Stackoverflow Fragen
#### Verfügbare Plugins
#### Update Frequenz / Stabilität
#### Geile Features o.O

### https://getgrav.org/
#### Dokumentation Dev / Src
#### Offene github Issues
#### Stackoverflow Fragen
#### Verfügbare Plugins
#### Update Frequenz / Stabilität
#### Geile Features o.O

### https://www.neos.io
#### Dokumentation Dev / Src
#### Offene github Issues
#### Stackoverflow Fragen
#### Verfügbare Plugins
#### Update Frequenz / Stabilität
#### Geile Features o.O

### https://www.endurojs.com/
#### Dokumentation Dev / Src
#### Offene github Issues
#### Stackoverflow Fragen
#### Verfügbare Plugins
#### Update Frequenz / Stabilität
#### Geile Features o.O

### https://keystonejs.com/
#### Dokumentation Dev / Src
#### Offene github Issues
#### Stackoverflow Fragen
#### Verfügbare Plugins
#### Update Frequenz / Stabilität
#### Geile Features o.O

### https://strapi.io/
#### Dokumentation Dev / Src
#### Offene github Issues
#### Stackoverflow Fragen
#### Verfügbare Plugins
#### Update Frequenz / Stabilität
#### Geile Features o.O

### https://apostrophecms.org/
#### Dokumentation Dev / Src
#### Offene github Issues
#### Stackoverflow Fragen
#### Verfügbare Plugins
#### Update Frequenz / Stabilität
#### Geile Features o.O

### https://contao.org/de/
#### Dokumentation Dev / Src
#### Offene github Issues
#### Stackoverflow Fragen
#### Verfügbare Plugins
#### Update Frequenz / Stabilität
#### Geile Features o.O

