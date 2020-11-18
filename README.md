# Snowpack Symlink Repro

## Repro

```
yarn
yarn build
tree build/_dist_
```

### Actual

```
build/_dist_
├── in-src.js
├── link
│   └── in-link.js
└── no-link
    ├── in-link.js
    └── subdir
        └── in-subdir.js
```

### Expected

```
build/_dist_
├── in-src.js
├── link
│   ├── in-link.js
│   └── subdir
│       └── in-subdir.js
└── no-link
    ├── in-link.js
    └── subdir
        └── in-subdir.js
```
