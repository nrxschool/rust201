# Rust 201 – Beyond the Basics

## 1. Recapitulando o Básico

* Revisão rápida: Variables, Shadowing, Control Flow
* Functions & Pattern Matching avançado (guards, `@`, `_`)
* Ownership & Borrowing em profundidade (regras implícitas e pegadinhas comuns)
* Enums e Data Modeling idiomático

> Mini-projeto: CLI simples que usa enums para parsing de comandos

---

## 2. Generics e Traits

* Revisão de Generics
* **Monomorfização** (o que realmente acontece no binário)
* Traits essenciais: `Debug`, `Clone`, `Eq`, `PartialOrd`, `Iterator`
* Trait Objects (`dyn Trait`) vs. Generics (`impl Trait`)
* Blanket implementations e trait bounds avançados (`where`, `Sized`, `?Sized`)

> Mini-projeto: construir uma mini-lib genérica de coleções customizadas

---

## 3. Módulos e Manipulação de Erros

* Organização de projeto: Módulos, Crates, `pub`, `pub(crate)`
* Cargo workspaces & crates externos
* `panic!` vs. `Result<T, E>` vs. `Option<T>`
* Definindo erros customizados com `thiserror`
* Propagação de erros com `?`

> Mini-projeto: cliente HTTP que trata erros de rede graciosamente

---

## 4. Lifetimes e Borrow Checker Avançado

* Lifetimes explícitos em funções e structs
* Lifetime elision rules (quando o compilador infere por você)
* `'static`, generics e traits com lifetimes
* Subtyping e lifetime bounds (`'a: 'b`)
* Casos práticos: APIs assíncronas, iteradores customizados

> Mini-projeto: construir um parser que retorna slices com lifetimes corretos

---

## 5. Smart Pointers e Interior Mutability

* Revisão: stack vs heap
* `Box<T>` e uso em recursividade
* `Rc<T>` e `Arc<T>` – contagem de referências
* `Cell<T>` e `RefCell<T>` – mutabilidade interior e runtime borrow checking
* `Weak<T>` e ciclo de referências
* Comparando com GC e RAII em outras linguagens

> Mini-projeto: implementar uma árvore de diretórios usando `Rc<RefCell<T>>`

---

## 6. Concorrência em Rust

* Threads nativas (`std::thread`)
* `Send` e `Sync` em profundidade
* Channels (`mpsc`)
* `Arc<Mutex<T>>`, `RwLock<T>`
* Introdução ao async/await
* `tokio` e `async-std` (quando usar cada)

> Mini-projeto: servidor TCP concorrente simples

---

## 7. Unsafe Rust

* O que o `unsafe` realmente significa
* Regras que o compilador não garante em `unsafe`
* `raw pointers`, `unsafe fn`, `extern`
* Criação de abstrações seguras a partir de código inseguro
* FFI (Foreign Function Interface) básico

> Mini-projeto: escrever uma função `unsafe` encapsulada em API segura

---

## 8. Macros

* `macro_rules!` – declarative macros
* Procedural macros: `derive`, `attribute`, `function-like`
* Casos práticos (`serde`, `wasm_bindgen`, `clap`)
* Tradeoffs entre macros e traits genéricos

> Mini-projeto: criar uma macro de logging customizada

