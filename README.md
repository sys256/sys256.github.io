# sys256.github.io

**This is a ✨special✨ repository for my GitHub Pages.**

## Description

Ez a git repository a <https://sys256.github.io> _GitHub Pages_ honlap
forrásfájljait és az aktuális build-et tartalmazza. A build helye a _Vite_
frontend build tool által alapértelmezetten használt `dist` könyvtár.

> **🛠️ FIGYELEM!**\
> A _main branch_-beli `dist` alkönyvtár változásai automatikusan elindítják a
> `.github/workflows/static.yml`-ben előírt műveleteket. Mivel a könyvtárba
> — ellentétben a _Jekyll_-alapú GitHub Pages oldalakkal, — már a kész build
> kerül, a feldolgozás mindössze a fájlok változtatás nélküli live webroot-ba
> másolásából áll.

## Cloning and initialization

A fejlesztői gépre klónozott repository nem tartalmazza a dev futtatáshoz és a
build létrehozásához szükséges _Node.js_ vendor csomagokat (`node_modules`
mappát). Telepítésük:

```console
cd sys256.github.io
npm install
```

## Developer commands

Command           | Description
------------------|------------
`npm run dev`     | Vite dev server futtatása
`npm run build`   | Vite build
`npm run preview` | A build megtekintése a fejlesztői szerverrel
