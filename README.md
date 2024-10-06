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
git submodule update --init --recursive
npm install
```

### Update
Ich hab es noch nicht ausprobiert, weil ich das nur auf einen System am laufen haben aber die Schritte sollten wie folgt sein:
```
git pull --recurse-submodules
npm install
```

### Starten
Noch nicht implementiert

### Commits
Ich hab mir dafuer commitizen installiert.
``` (Ich glaube den zweiten Schritt muss man je Repo machen)
npm install -g commitizen
commitizen init cz-conventional-changelog --save-dev --save-exact 
```
oder
```
npm install -g commitizen
npm install -g cz-conventional-changelog echo '{ "path": "cz-conventional-changelog" }' > ~/.czrc
```

Und dann:
```
git add .
cz
```

### Erweitern um neue Application/Packages/Libary
Mit der Aufteilung bin ich mir noch nicht ganz sicher. Ich wuerde sagen, in `apps` kommen die Anwendungen die nachher starten muessen. In `libs` kommen die sachen, die grundlegende funktionalitaeten fuer alle Anwendungen bereit stellen und in `packages` kommen die Sachen die irgendwie von den apps benoetigt werden?

