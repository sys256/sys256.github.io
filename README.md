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

### Warnings about deprecated packages

**TODO**\
Ezeket a figyelmeztetéseket a jelenlegi hivatalos _Vuetify_ okozza. Az érintett
csomagok nem jelentenek működésbeli problémát, de később el kell majd végezni a
szükséges frissítéseket.

- **inflight@1.0.6**: This module is not supported, and leaks memory.
  Do not use it. Check out lru-cache if you want a good and tested way to
  coalesce async requests by a key value, which is much more comprehensive and
  powerful.

- **@humanwhocodes/config-array@0.11.14**: Use `@eslint/config-array` instead.

- **rimraf@3.0.2**: Rimraf versions prior to v4 are no longer supported.

- **glob@7.2.3**: Glob versions prior to v9 are no longer supported.

- **@humanwhocodes/object-schema@2.0.3**: Use `@eslint/object-schema` instead.

- **babel-eslint@10.1.0**: babel-eslint is now `@babel/eslint-parser`. This
  package will no longer receive updates.

## Developer commands

Command           | Description                                  | Comments
------------------|----------------------------------------------|---------
`npm run dev`     | Vite dev server futtatása                    | &nbsp;
`npm run build`   | Vite build                                   | Inkrementálja az NPM version patch értékét
`npm run preview` | A build megtekintése a fejlesztői szerverrel | &nbsp;
