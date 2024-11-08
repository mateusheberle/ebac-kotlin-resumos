# Fundamentos de Kotlin

## Aula 2 - Variáveis

"Conhecimento nunca faz mal."

    Variáveis servem para guardar informação para usar no futuro
    Estruturas para armazenar informação

### Tipos
- Estaticamente tipada
- Declaro tem que dizer o tipo
- O tipo não pode mudar depois de definido
- Tipos de informação que quer salvar

**Numéricos inteiros**
- Números inteiros positivos e negativos
- Depende da informação que quer armazenar
- Normal é usar o int (pouco mais de 2 milhões)
- 4 tipos:
    - `byte` - menos memória
    - `short`
    - `int`
    - `long`

**Numéricos com ponto flutuante**
- Representa um numero com virgula
- Parte não inteira
- 2 tipos:
    - `float`
    - `double`

**Textos, strings e caracteres**
- 2 tipos:
    - `char`
        - caractere
        - uma única letra
    - `string`
        - texto
        - vários caracteres
        - depende do tamanho da memória

**Booleano**
- Recebe apenas um valor
- Ou um, ou outro
    - `true`
    - `false`


### Mutáveis e Imutáveis
- Mutável
    - pode mudar
    - valor muda
    - **var**
- Imutável
    - nunca muda
    - imutável atribuir valor uma única vez
    - nunca muda
    - **val**

"Sempre que possível usar variáveis imutáveis"
- código otimizado
- menos erros

### Declaração

```kotlin
mutável/imutável + nomeVariavel + : + tipos
```

- exemplos:

```kotlin
var resultado : Int
val teste : String
```

#### Nome da variável
- Precisa ser algo que faz sentido pro código
- Que dá pra ler
- Código bem escrito facilita a leitura
- Quase como ler um texto

**Não precisa dizer o tipo**, explicitamente
- exemplo:

```kotlin
var resultado = 1
// computador atribui como inteiro
```

```kotlin
var teste = 1.0
// computador entende que é double, não inteiro
```


Não confundir com tipagem dinâmica
- Se baseia na atribuição
- Depois que decidiu o tipo, não dá pra mudar o tipo


### Plataforma para testes 
- [Kotlin Playground](https://play.kotlinlang.org/)
    - Mais prático
    - Roda a partir do navegador
    - Testar e validar

- Android Studio
    - "New Project"
    - "No Activity"
    - "File" > "New" > "Kotlin Class/File"
    - nome
        - Variables
        - class


### Função `main`
- Função principal
- Vai começar a rodar o código a partir dele

- Palavras reservadas aparecem de outra cor
- Se atribuir um valor, kotlin vai inferir o tipo

- Classe
    - começa com letra maiúscula
    - `Variable.kt`
- Variáveis
    - começa com letra minúscula
    - `resultadoSoma`
    - CamelCase


`string` - sempre entre aspas

### Código

```kotlin
package com.mateusauler.variaveis

class Variables {
}

fun main() {
    // variável mutável
    var resultadoSoma: Int
    var inteiro = 1

    // variável imutável
    val outroInteiro = 1

}
```