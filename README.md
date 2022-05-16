# JavaScript Page Size Cost

The `@esmj/size` show you javascript cost for your defined packages. The packages is bundled with Webpack. Then show the bundle size and downloaded time for javascript bundle.

## Requirements

- Node 14+

## Install

```shell
npm install -g @esmj/size
esmj-size @merkur/core
// or
npx @esmj/size @merkur/core
```

## Usage

You can display all available commands with following command.

```shell
esmj-size react,react-dom
# ┌────────────────────────────────────────┬────────────────────┬────────────────────┬────────────────────┐
# │ Package                                │ Minify             │ Minify+Gzip        │ Minify+Brotli      │
# ├────────────────────────────────────────┼────────────────────┼────────────────────┼────────────────────┤
# │ react,react-dom                        │ 136.27 KB          │ 41.52 KB           │ 35.96 KB           │
# └────────────────────────────────────────┴────────────────────┴────────────────────┴────────────────────┘
# ┌────────────────────┬────────────────────┬────────────────────┬────────────────────┬────────────────────┐
# │ Bundle             │ 2g                 │ 3g                 │ 4g                 │ 5g                 │
# ├────────────────────┼────────────────────┼────────────────────┼────────────────────┼────────────────────┤
# │ minify             │ 11.63 s            │ 2.79 s             │ 159.47 ms          │ 62.02 ms           │
# ├────────────────────┼────────────────────┼────────────────────┼────────────────────┼────────────────────┤
# │ gzip               │ 3.54 s             │ 850.38 ms          │ 48.59 ms           │ 18.9 ms            │
# ├────────────────────┼────────────────────┼────────────────────┼────────────────────┼────────────────────┤
# │ brotli             │ 3.07 s             │ 736.4 ms           │ 42.08 ms           │ 16.36 ms           │
# └────────────────────┴────────────────────┴────────────────────┴────────────────────┴────────────────────┘

esmj-size easy-uid --json
# {
#   minify: {
#     size: 297,
#     speed: { '2g': 24.75, '3g': 5.94, '4g': 0.3394285714285714, '5g': 0.132 }
#   },
#   gzip: {
#     size: 212,
#     speed: {
#       '2g': 17.666666666666668,
#       '3g': 4.24,
#       '4g': 0.2422857142857143,
#       '5g': 0.09422222222222222
#     }
#   },
#   brotli: {
#     size: 177,
#     speed: {
#       '2g': 14.75,
#       '3g': 3.54,
#       '4g': 0.2022857142857143,
#       '5g': 0.07866666666666666
#     }
#   }
# }
```

You can display all available commands and settings with following command.
```shell
esmj-size --help
```

