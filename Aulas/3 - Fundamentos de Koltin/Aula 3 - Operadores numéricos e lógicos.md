# Fundamentos de Kotlin

## Aula 3 - Operadores numéricos e lógicos

### Operadores básicos:

| Operação         | Símbolo |
|------------------|---------|
| Soma             | `+`       |
| Subtração        | `-`      |
| Multiplicação    | `*`       |
| Divisão          | `/`       |
| Resto da divisão | `%`       |


### Conversão

- Cast
- Todos os tipos numéricos oferecem operadores de conversão:
    - `toByte()`
    - `toShort()`
    - `toInt()`
    - `toLong()`
    - `toFloat()`
    - `toDouble()`
    - `toChar()`
    - `toString()`
- Conversão texto para numérico:
    - `toInt()`
    - `toDouble()`
    - `toLong()`
    - `toShort()`
    - `toByte()`
    - `toFloat()`

"String que não é número, não pode ser convertido, vai dar uma exceção"

```kotlin
package com.mateusauler.variaveis

fun main() {
    // conversão
    val a: Int = 1
    var b: Double

    // errado
    b = a

    // certo
    b = a.toDouble()

}
```


```kotlin
Double = Int * 1.0

var resultado = Int / Int
// resultado = Int

var resultado = Double / Int
// resultado = ponto flutuante
```

### Operadores lógicos

| Operação       | Símbolo |
|----------------|---------|
| Operador OU    | `\|\|`    |
| Operador E     | `&&`      |
| Negação        | `!`       |


### Concatenação e Template de strings

- Concatenação
    - Juntar duas coisas

```kotlin
var texto = "Hello" + " world!"
```

- Template
    - Substituir variável pelo conteúdo

```kotlin
val name = "Mateus"
val template = "my name is $name"
// resultado: "my  name is Mateus"
```

![Imagem 3](/imagens/3.png)

- Ponto (.)
    - Lista todas as funções para a variável `test`

"No Android Studio, quando uma variável está cinza, ela não está sendo usada."


