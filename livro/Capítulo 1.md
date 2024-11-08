<style>
    body {
        font-family: "Courier New", Courier, monospace;
    }
</style>

# Capítulo 1 - A linguagem Kotlin

Koltin é uma linguagem de programação pragmática que combina os **Paradigmas OO** e **Programação Funcional**.

Devs:
- Interoperabilidade
- Segurança
- Clareza
- Suporte a ferramentas

Equipe do Android:
- Expressiva
- Concisa
- Poderosa

Criada pela JetBrains (criou o Android Studio)

- Alteranativa para Java
- Linguagem moderna de alta produtividade

### História:
- 2011: Anúncio de uma nova linguagem tipada para a JVM
    - produtiva e de simples aprendizado
- 2016: Versão 1.0

Linguagem que roda na JVM (onde funciona JAVA, funciona Kotlin)

- 2017: Linguagem oficial para desenvolvimento Android

Todo o ecossistema Android é compatível com Kotlin

Principais pontos da linguagem: interoperabilidade, concisão e proteção contra nulos.

### Interoperabilidade

Capacidade de uma linguagem se comunicar com outra
- Total interoperabilidade com JAVA
    - Aproveita qualquer biblioteca ou classe escrita em JAVA 

### Linguagem Concisa

Precisamos escrever menos código para fazer a mesma coisa que uma outra linguagem

No Android é comum definirmos IDs de elementos como letrar minúsculas separadas por `underline` ( _ )

### Referências Nulas

Erro de referência nula (`NullPointerException`)

Quando tenta acessar um objeto que ainda não possui um espaço alocado na memória

Kotlin possui `null safety` (proteção contra nulos)

Em Kotlin nenhuma variável ou objeto pode ter um valor nulo

Operador `?` após o tipo da variável, deixa explícito que a variável pode receber um valor nulo

```kotlin
var nomeUsuario :String? = null
```

Operador `?` ignora a chamada se a variável for nula

```kotlin
var nomeUsuario :String? = null
println( nomeUsuario?.legth )
```