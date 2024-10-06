# SythRpgDev

## Benoetigt:
- Node.js (https://nodejs.org/en/learn/getting-started/how-to-install-nodejs)
- NX (https://nx.dev/getting-started/installation)

## Einleitung
Dies ist ein Repo um die Entwicklung vom SimpleYTH - Bot zu erweitern.
Dieses Repo ist nur für das Managen der Submodule für das Text-RPG zustaendig, ein uebergeordnetes Repo wird noch erstellt.
Aber so koennen wir schon mal anfangen.

## How To?
### Installation
Ich hab es noch nicht ausprobiert, weil ich das nur auf einen System am laufen haben aber die Schritte sollten wie folgt sein:
```
git clone git@github.com:Istani/syth-rpg-dev.git
cd syth-rpg-dev
git submodule update --init --recursive
npm install
```

### Update
Ich hab es noch nicht ausprobiert, weil ich das nur auf einen System am laufen haben aber die Schritte sollten wie folgt sein:
```
git pull --recurse-submodules
npm install
```

### Submodule
Soweit ich weiß muss man dann bei jedem Submodul auch ```npm install``` machen!

### Starten
Noch nicht implementiert.
Achtung: 
Einige Submodule brauchen ENV Einstellungen/Config Dateien.
Die sind so natuerlich nicht oeffentlich im GitRepo, wegen Serverlogins etc...

### Entwicklung
Keine Ahnung wie das mit Forks und Pull Reqeusts funktioniert.

### Commits
Ich hab mir dafuer commitizen installiert.
``` (Ich glaube den zweiten Schritt muss man je Repo machen)
npm install -g commitizen
commitizen init cz-conventional-changelog --save-dev --save-exact 
```


Und dann:
```
git add .
cz
```

### Erweitern um neue Application/Packages/Libary
Mit der Aufteilung bin ich mir noch nicht ganz sicher. Ich wuerde sagen, in `apps` kommen die Anwendungen die nachher starten muessen. In `libs` kommen die sachen, die grundlegende funktionalitaeten fuer alle Anwendungen bereit stellen und in `packages` kommen die Sachen die irgendwie von den apps benoetigt werden?
Weil NX aber nicht direkt mit SubModulen arbeitet, muss man da ein wenig tricksen... Ich hab immer npm-packages hinzugefuegt weil ich mit node arbeite, vielleicht gibt es noch bessere fuer php oder so...

- Application:
```
nx g npm-package apps/[webserver]
(Vielleicht die Daten sichern bevor man loescht)
rm -rf apps/[webserver]
git submodule add [git@github.com:Istani/syth-webserver.git] apps/[webserver]
```

- Libary:
```
nx g npm-package libs/[database]
(Vielleicht die Daten sichern bevor man loescht)
rm -rf libs/[database]
git submodule add [git@github.com:Istani/syth-databse.git] libs/[database]
```


