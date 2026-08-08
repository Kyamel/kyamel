# Rumo à Pesquisa em Linguagens de Programação

## Minha situação

- 25 anos.
- Estudante de Engenharia de Computação (UFOP), indo para o 9º período.
- Interesse em arquitetura de software, compiladores, protocolos, linguagens de programação, sistemas e infraestrutura.
- Objetivo de longo prazo: tentar criar algo realmente útil para o futuro da computação, especialmente na área de linguagens de programação e paradigmas.

---

# Uma observação importante

O objetivo **não deve ser "inventar uma linguagem"**.

O objetivo deve ser:

> Entrar na comunidade internacional que pesquisa linguagens de programação, compiladores, sistemas e métodos formais.

Linguagens importantes normalmente surgem como consequência de anos estudando um problema profundamente, e não como objetivo em si.

---

# Mercado x Academia

## Mercado

O mercado é excelente para aprender engenharia de software.

Ele ensina:

- construir sistemas grandes;
- manutenção;
- trabalho em equipe;
- desempenho;
- arquitetura;
- problemas reais.

Entretanto, empresas raramente pesquisam novos paradigmas de programação.

Algumas exceções:

- Google
- Microsoft
- Apple
- JetBrains
- Mozilla
- Meta
- empresas de compiladores e tooling

---

## Academia

A academia permite explorar ideias muito mais profundamente.

Mas existe um risco:

Criar soluções elegantes que nunca chegam a ser usadas por ninguém.

Muitos papers excelentes acabam sem impacto prático.

---

# O caminho que parece mais promissor

Um caminho híbrido.

## Curto prazo

Terminar a graduação.

Depois trabalhar alguns anos em infraestrutura ou tooling.

Exemplos:

- compiladores
- banco de dados
- cloud
- sistemas distribuídos
- IDEs
- motores gráficos
- ferramentas de build
- sistemas operacionais

Enquanto isso...

Continuar estudando linguagens de programação por conta própria.

---

# O Goatty como laboratório

É fácil pensar:

> "Estou fazendo um terminal."

Na verdade o projeto pode ser muito mais do que isso.

Ele pode servir para experimentar ideias como:

- protocolo orientado a objetos para terminais
- substituição parcial do ANSI
- arquitetura modular
- toolkit reutilizável
- APIs para extensões
- novos modelos de renderização
- novos modelos de interação

Grandes ideias frequentemente começam exatamente assim.

Exemplos:

- Git
- SQLite
- LLVM
- Lua

Nenhum deles começou tentando ser "o próximo padrão da indústria".

---

# Mestrado

Vale a pena se existir um orientador cuja pesquisa seja próxima de:

- Programming Languages
- Compilers
- Static Analysis
- DSLs
- Logic Programming
- Formal Methods
- Incremental Computation
- Constraint Solving
- Type Systems

Mais importante que a universidade é o orientador.

---

# Doutorado

Só faz sentido se a curiosidade pela área continuar enorme depois do mestrado.

O doutorado é uma maratona.

Não um título.

---

# Ler papers

Começar cedo.

Mesmo entendendo pouco.

No início talvez apenas 10%.

Depois 30%.

Depois 70%.

O importante é acostumar o cérebro com o estilo de pesquisa.

---

# Conferências para acompanhar

Mesmo sem publicar nelas.

Principalmente:

- POPL
- PLDI
- OOPSLA
- ICFP
- ASPLOS
- SOSP
- OSDI

Essas conferências praticamente definem os rumos da área.

---

# Participar da comunidade

Não depender apenas da universidade.

Participar de:

- GitHub Discussions
- Zulip
- Discords
- Mailing Lists
- IRC (alguns projetos ainda usam)

Contribuir para projetos como:

- Rust
- Zig
- LLVM
- OCaml
- GHC
- Roc
- Gleam
- Nushell
- Ghostty

É uma forma de conhecer pessoas que trabalham exatamente nos problemas que você quer estudar.

---

# Matemática importante

Não apenas cálculo.

Principalmente:

- Lógica
- Teoria da Computação
- Autômatos
- Semântica Operacional
- Sistemas de Tipos
- Constraint Solving
- SAT/SMT
- Teoria das Categorias (ao menos o básico)

---

# Continuar construindo software

Esse talvez seja o conselho mais importante.

Muitas pesquisas excelentes falham porque seus autores nunca enfrentaram problemas reais.

Projetos grandes ajudam a descobrir:

> "Isso dói."

Essas dores normalmente são o ponto de partida para pesquisas relevantes.

---

# Uma observação sobre paradigmas declarativos

Paradigmas declarativos continuam sendo pesquisados intensamente.

Principalmente em áreas como:

- Datalog
- Logic Programming
- Constraint Programming
- Relational Programming
- Program Synthesis
- Incremental Computation
- Probabilistic Programming
- Neurosymbolic Programming

O objetivo atual parece ser menos substituir linguagens imperativas e mais integrar diferentes paradigmas numa mesma linguagem.

---

# Uma possível direção futura para linguagens

Uma linguagem poderia combinar vários paradigmas de forma nativa.

Exemplo conceitual:

```text
fn download() {
    // imperativo
}

relation ancestor(A, B) {
    parent(A, B)
    or parent(A, X) && ancestor(X, B)
}

solve {
    x + y == 20
    x > y
}

query {
    users
        where reputation > 100
}
```

Cada bloco seria compilado usando um mecanismo diferente.

Por exemplo:

- código imperativo → compilador tradicional
- relation → engine Datalog
- solve → SAT/SMT solver
- query → otimizador relacional

---

# Outra oportunidade

Memory management.

Hoje existem vários modelos:

- GC
- ARC
- ORC
- Ownership
- Manual

Cada um possui vantagens e desvantagens.

Talvez exista espaço para uma linguagem onde o compilador escolha automaticamente o melhor modelo conforme o contexto.

---

# ABI universal

Hoje praticamente todas as linguagens conversam usando a ABI do C.

Uma linguagem futura poderia oferecer uma ABI estável própria e gerar automaticamente bindings para:

- C
- Go
- Rust
- Python
- Swift
- Java
- C#
- WASM

---

# IA e linguagens

Talvez a próxima geração de linguagens preserve muito mais informação semântica.

Exemplo:

```text
fn withdraw(account, amount)

requires amount > 0

requires account.balance >= amount

ensures account.balance ==
    old(account.balance) - amount
```

Essas informações permitiriam que compiladores e agentes de IA raciocinassem muito melhor sobre programas.

---

# A ideia central

Quanto menos o programador especifica **como** fazer alguma coisa, mais liberdade o compilador ganha para encontrar uma implementação melhor.

Linguagens declarativas preservam a intenção.

Linguagens imperativas frequentemente escondem essa intenção em detalhes de implementação.

---

# O conselho mais importante

Não tentar inventar "a próxima linguagem".

Tentar entender profundamente:

> Quais problemas atuais das linguagens realmente impedem pessoas de construir software melhor?

Grandes linguagens nasceram exatamente dessa pergunta.

- Go nasceu da complexidade percebida do C++.
- Rust nasceu dos problemas de segurança de memória do C++.
- Nix nasceu dos problemas de reprodutibilidade.
- Prolog nasceu da ideia de declarar fatos em vez de algoritmos.

Provavelmente a próxima linguagem importante também nascerá da tentativa de resolver uma dor real que ainda não possui uma solução satisfatória.
