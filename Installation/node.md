# Installer LODEX avec Node

Pré-requis: MongoDB 3+, [Node](https://nodejs.org/) 8+

Commencez par cloner ou télécharger le dépôt GitHub, puis installez les paquets, compilez l'application, et lancez-la:

```bash
git clone https://github.com/Inist-CNRS/lodex.git
cd lodex
npm install
npm run build
npm start
```

Par défaut, l'application est accessible à l'URL: [http://localhost:3000/](http://localhost:3000/).

Si ce serveur est accessible sur le web, vous pouvez renseigner la variable d'environnement `EZMASTER-PUBLIC-URL` \(en remplaçant le tiret `-` par un souligné: `_`\) avec l'URL de base du serveur \(par exemple `https://data.istex.fr`\).



