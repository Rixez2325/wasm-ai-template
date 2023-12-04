<div align="center">

  <h1><code>wasm-ai-template</code></h1>

<strong>Un template de projet utilisant <a href="https://github.com/rustwasm/wasm-pack">wasm-pack</a>.</strong>


  <h3>
    <a href="https://rustwasm.github.io/docs/wasm-pack/tutorials/npm-browser-packages/index.html">Tutorial source</a>
  </h3>
</div>

[//]: # (This template is designed for compiling Rust libraries into WebAssembly and publishing the resulting package to NPM.)
## Utilisation

### Utiliser `cargo generate` pour cloner le template suivant

```
cargo generate --git https://github.com/Rixez2325/wasm-ai-template --name my-project
cd my-project
```

### Construire avec `wasm-pack build`
Afin de lancer la compilation il faudra ajouter dans votre fichier 'Cargo.toml' la ligne suivante:
```toml
[lib]
crate-type = ["cdylib", "rlib"]
```
Cette dernière permettra de compiler le code en tant que librairie statique et dynamique.
```bash
wasm-pack build
```

### Tester dans les navigateurs avec `wasm-pack test`
Afin de pouvoir il faudra ajouter dans votre fichier 'Cargo.toml' la ligne suivante:
```toml
[dev-dependencies]
wasm-bindgen-test = "0.3.39"
```

```bash
wasm-pack test
```

### Libraries utilisées
* [`wasm-bindgen`](https://github.com/rustwasm/wasm-bindgen) pour la communication entre le code Rust (wasm) et le code JavaScript.
* [`console_error_panic_hook`](https://github.com/rustwasm/console_error_panic_hook) permettra d'utiliser le DOM pour afficher les erreurs de Rust.
* `LICENSE-APACHE` and `LICENSE-MIT`: Licence Apache et MIT pour les projets Rust, donc inclus dans le template.