# Homepage-fuer-Kuenstler-mit-Bootstrap-und-Sass
Homepage für Template mit Bootstrap und Sass, Kontaktformular für Künstler, Photographen o.ä.

## Verwendet
- [Bootstrap](http://getbootstrap.com/)
- [Sass](http://foundation.zurb.com/sites/docs/v/5.5.3/sass.html)
- [Font Awesome](http://fontawesome.io/)
- [NodeJS](https://nodejs.org/en/) 
- [Lizenzfreie Bilder von Pexels.com](https://nodejs.org/en/) 
- [Google Fonts](https://fonts.google.com/)

## Voraussetzungen

- [NodeJS](https://nodejs.org/en/) 
- [Git](https://git-scm.com/)
- [Koala](http://koala-app.com/) "GUI application for Less, Sass, ..."
- [Atom](https://atom.io/) and life Server or XAMPP or similar


### Setup

1.Download mit Git:

```bash
git clone https://github.com/MariaHildebrandt/Homepage-mit-Bootstrap-und-Sass projectname
```
2.Ordner in command line öffnen und dependencies installieren:

```bash
cd projectname
npm install -g bower
bower install bootstrap-sass --save
```
3.Starte Koala. Öffne darin die Datei projectname/sass/app.scss

4. starte Atom Life Server
- Atom code editor: file>settings>Packages search for atom-life-server by Jes-Chen
- install and start server via Packages>atom-live-sever

### Screenshots

#### Vollansicht:
<p>
  <a href="https://postimg.org/image/anocyrygv/">Idex</a>,
  <a href="https://postimg.org/image/q38nfe4gh/">Mobile Ansicht</a>
</p>


#### Vorschau:
Bemerkung: Mobile Ansicht Gallerie noch nicht responsive daher unschön nach links verschoben
<p align="left">
  <img src="https://s27.postimg.org/nf2j5a88z/index.png"/  width="390">
  <img src="https://s8.postimg.org/nyoaeb2tx/mobile.png"/  width="80">
</p>

### How to Recreate
- 1.)download koala GUI : to compile sass files
- 2.) use bower to set up bootstrap with following command in you project folder:npm install -g bower   this will create a folder called "bower components"
- set-up will take ~ 3min
- 3.) install sass with command (still in project folder): bower install bootstrap-sass --save
- 4.) inside project folder create new folder "sass" and in new folder create new file "app.scss"
- 5.)in app.scss write:
- @import "../bower_components/bootstrap-sass/assets/stylesheets/bootstrap";
- @import "../bower_components/bootstrap-sass/assets/stylesheets/bootstrap-compass";
- 6.)open app.scss in koala aand compile - this will create e new folder named css which contains app.cssinclude this file in the header of your index.html
```bash
 <link href="../css/app.css" rel="stylesheet">
 ```

#### Integrate working Email Service: Third Party service for Mials - mailchimp (free)
- 1.)sign up for free
- 2.)create a list with website name
- 3.) deafult from emal: your email and default from name
- 4.)you can also see subsciptions to your website
- 5.) embedded forms genrator

#### Mögliche Fehler und wie sie zu beheben sind
##### Erste möglichkeit falls die scss files nicht mehr compilert werden
- _filename.scss umbennen und in mainfile.scss importieren

##### Zweite möglichkeit falls die scss files nicht mehr compilert werden
- 1.) öffne projekt ordner im bash
- 2.)$ gem install compass
- dabei musst du beachten dass SASS bzw. Ruby schon installiert ist
- 3.) sobald installier den befehl "compass clean" ausführen. Dies soll den .sass-cache folder leeren


##### Bootstrap glyphicons nicht sichtbar oder nur kleine vierecke:
- fonts folder in bower-components muss auf selver ebee wie css folder Sein
- ordner "folder" kopieren und neben folder css einfügen

##### Wenn Koala nicht startet -> koale.exe in task-manager beenden und nochmal starten

##### google fonts:
- für font-famliy importiere den link in app.scss
- like this: @import url('https://fonts.googleapis.com/css?family=Open+Sans|Pacifico|Raleway');

##### wenn tabs in bootstrap nicht funktionieren:
- neuesten jquery link einfügen und
- bootstrap runterladen und bootstrap.min.js in einem neuen ordner "js" (auf selber ebene wie "css") entpacken
- dann über dem body-schließ-tag (</body>) folgendes einsetzen:
```bash
 <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
 <script src="js/bootstrap.min.js"></script>
````
