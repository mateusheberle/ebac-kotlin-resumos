<style>
    body {
        font-family: "Courier New", Courier, monospace;
    }
</style>

# Capítulo 2 - Programando em Kotlin

## Índice

1. [Estrutura básica da linguagem](#estrutura-básica-da-linguagem)
2. [Inserindo Comentários](#inserindo-comentários)
3. [Definindo variáveis](#definindo-variáveis)
4. [Variáveis imutáveis](#variáveis-imutáveis)
5. [Tipos de dados](#tipos-de-dados)
    - [Dados numéricos](#dados-numéricos)
    - [Strings e caracteres](#strings-e-caracteres)
    - [Booleanos](#booleanos)
6. [Listas e Arrays](#listas-e-arrays)
7. [Estruturas de decisão](#estruturas-de-decisão)
8. [Estruturas de repetição](#estruturas-de-repetição)
9. [Funções](#funções)
10. [Orientação a Objetos](#orientação-a-objetos)
    - [Herança entre as classes](#herança-entre-as-classes)
    - [Classe de dados](#classe-de-dados)

### Estrutura básica da linguagem

- https://try.kotlinlang.org
- Plataforma online para executar código Kotlin

```kotlin
// Função 'main' do Kotlin
fun main(args: Array<String>)
```

A função `main` é o ponto de partida de todo programa feito em Kotlin
A função `println` recebe um texto como parâmetro, exibe no console e pula uma linha no final. `print` não pula uma linha ao final

### Inserindo Comentários

Comentários são textos inserido no código mas que serão ignorados pelo compilador e não vão interferir no funcionamento do programa
- Explicar ou o que faz algum comando

```kotlin
// Este é um comentário em Kotlin

/*
Este é um comentário em Kotlin,
com mais de uma linha
*/
```

```kotlin
/*
A função main é o ponto de partida de qualquer programa em Kotlin
Todos os códigos devem estar dentro dela, ou ser chamados a partir dela
*/

fun main(args: Array<String>){
    // o comando print exibe uma mensagem no console, mas não pula a linha
    print("Meu primeiro ")
    // o comando println exibe a mensagem no console e pula uma linha no final
    println("programa em Kotlin!")
}
```

### Definindo variáveis

Utilizamos variáveis para guardar algum valor que usaremos posteriormente

Espaço reservado na memória do computador em que eu posso guardar valores e resgatá-los através de um nome.

Palavra-chave `var`, seguido da definição de seu tipo

```kotlin
var idade:Int = 22
```

É obrigatório que a variável tenha um valor inicial
Não é obrigatório a indicação de seu tipo

```kotlin
var idade = 22
```

Tipos básicos que o Kotlin aceita

| Tipo     | Descrição                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Double   | Tipo numérico para valores de ponto flutuante, com Double é possível guardar valores com precisão bem grande pois ele ocupa 64 bits                         |
| Float    | Tipo numérico para valores de ponto flutuante, com a diferença de que tem uma precisão menor que o Double pois ele ocupa 32 bits                            |
| Long     | Usado para valores inteiros, a diferença dele para o Int é que, como ele ocupa 64 bits, você consegue representar números muito maiores                     |
| Int      | Talvez um dos tipos numéricos mais comuns, é para guardar números inteiros com uma precisão de 32 bits                                                      |
| Short    | Também guarda valores inteiros, porém com capacidade máxima de metade de um Int, pois ocupa somente 16 bits                                                  |
| Byte     | Também guarda números inteiros, porém seu número máximo é 127 pois ele ocupa somente 8 bits                                                                 |
| String   | É um tipo para guardar valores em texto, uma frase, um nome ou qualquer valor que seja um texto                                                             |
| Char     | É um tipo para guardar um único caractere, diferente da String, em que você pode guardar textos                                                             |
| Boolean  | É usado para valores booleanos, ou seja, valores que são verdadeiro (True) ou falso (False)                                                                 |

### Variáveis imutáveis

Palavra reservada `val`
Uma variável que não terá seu valor alterado posteriormente
Por via de regra defina as variáveis como `val`, e caso haja necessidade, mude para `var`

### Tipos de dados

Em kotlin, **tudo é um objeto**
Todas as variáveis e tipos que usamos possuem propriedades e métodos
Todo objeto possui características e comportamentos específicos

O tipo `int` do JAVA é um tipo primitivo
Já o tipo `Int` do Kotlin é um objeto, ele possui métodos que podem auxiliar o desenvolvimento
O `Int` do Kotlin se assemelha ao tipo `Integer` também do JAVA

Converter do tipo `Int` para Double, Float ou String:
- `toDouble()`
- `toFloat()`
- `toString()`

```kotlin
val x: Int = 10;

var y: Double = x.toDouble()
// retorna um objeto Double a partir do valor de x
var z: Float = x.toFloat()
// retorna um objeto Float a partir do valor de x
var a: String = x.toString()
// retorna um objeto String a partir do valor de x
```

#### Dados numéricos

Muito parecidos com os suportados em JAVA, com a diferença de que todos são objetos

| Tipo   | Bit |
|--------|-----|
| Double | 64  |
| Float  | 32  |
| Long   | 64  |
| Int    | 32  |
| Short  | 16  |
| Byte   | 8   |

Utilização do `underline` para facilitar a legibilidade

```kotlin
val umMilhao = 1000000
val umMilhao - 1_000_000
```

#### Strings e caracteres

Guardar conteúdo do tipo texto
Conteúdo definido entre **aspas duplas**

```kotlin
val texto = "Boa tarde, seja bem-vindo ao sistema."
```

**Templates de strings** são trechos de código inseridos diretamente em uma String e que têm seu resultado concatenado junto à String

```kotlin
fun main(args: Array<String>) {
    
    val nomeUsuario = "Mateus"
    val saudacao = "Bem-vindo, $nomeUsuario"
    
    println(saudacao)
}
```

Texto com várias linhas

```kotlin
val texto = """
    Exemplo de texto
    com mais de uma
    linha
"""
```

#### Booleanos

Definido como `Boolean`, só pode receber os valores `true` ou `false`

| Operação | Operador |
|----------|----------|
| E        | &&       |
| OU       | &#124;&#124; |
| NÃO      | !        |

Tipo booleano possui funções para essas operações

```kotlin
fun main(args: Array<String>) {

    val b1 = true
    val b2 = false

    val c1 = b1.and(b2) // retorno será false
    val c2 = b1.or(b2)  // retorno será true
    var c3 = b1.not()   // retorno será false

}
```

#### Listas e Arrays

**Array**
- Mais de um valor em uma variável
- Várias variáveis em uma única variável

- **Tamanho fixo**
- Resgatar valores através de seu índice utilizando colchetes ( [ ] )

```kotlin
// Array de inteiros de 4 posições
val arrayInt :Array<Int> = arrayOf(1, 2, 3, 4)

val x = arrayInt[2]
println(x)      // 3
```
- Todo array tem seu início na posição 0

**Listas**
- Parecidas com as estruturas de `Array`
- Tamanho não precisa saber antecipadamente
- Posso adicionar novos valores conforme a necessidade

Listas que aceita a adição de novos valores: **Mutáveis**
Listas que não aceitam novos valores: **Imutáveis**

```kotlin
// Lista mutável
val lista = multableListOf(1, 2, 3, 4)

lista.add(5)    
// adiciona um novo valor a lista

val item = lista.first()    
// a variável 'item' ficará com o valor 1

val item = lista.last()     
// a variável 'item' ficará com o valor 4

val numerosPares = lista.filter { it $ 2 == 0 }     
// a variável 'numerosPares' ficará com os valores 2 e 4

```

- `first`: retorna o primeiro elemento
- `last`: retorna o último item da lista
- `filter`: aplica um filtro específico

```kotlin
// Lista imutável
val lista = listOf(1, 2, 3, 4)
```

Todos os métodos utilizados na lista mutável funcionam em listas imutáveis (com exceção do método `add`)

### Estruturas de decisão

Quando queremos que determinado pedaço de código seja executado somente quando uma condição for satisfeita

A expressão `if` é uma estrutura de decisão, conseguimos mudar o fluxo do programa de acordo com o resultado de um `if`

```kotlin
fun main(args: Array<String>) {
    val senha = "123"

    if( senha == "123"){
        println("Acesso concedido")
    }else{
        println("Senha incorreta")
    }
}
```

Um `if` não precisa necessariamente ter um `else`

```kotlin
val a = 10
val b = 5

if( a > b) {
    println("$a é maior que $b")
}
```

```kotlin
val a = 10
val b = 5

if( a > b) {
    println("$a é maior que $b")
}else{
    println("$a é menor que $b")
}
```

```kotlin
// Armazenar o valor em uma variável
val a = 10
val b = 5

val maior = if( a > b) a else b
```

Nesse caso o `if` foi usado como uma expressão e não como um simples controle de fluxo

Estrutura `when`, quando precisamos de várias verificações em seguida
Em comparativo com JAVA o `when` seria o substituto do `switch`

```kotlin
when (x) {
    1 -> print("x == 1")
    2 -> print("x == 2")
    else -> {
        print("x possui outro valor")
    }
}
```
```kotlin
when (x) {
    0, 1 -> print("x == 0 ou x == 1")
    else -> print("x tem outro valor")
}
```
```kotlin
when (x) {
    in 1..10 -> print("x está no intervalo")
    else -> print("x está fora do intervalo")
}
```

### Estruturas de repetição

Repetir determinado trecho de código
`for` e `while`

`for` para iterar listas
Quando sabemos o número de interações que o programa precisa fazer

```kotlin
val lista = listOf(1,2,3,4)

for(i in lista) {
    println("Item: $i")
}
```
```kotlin
val lista = listOf(1,2,3,4)
for((indice, valor) in lista.withIndex()){
    println("Índice: $indice  valor: $valor")
}
```

`while`
Repte um trecho do código enquanto uma condição for verdadeira

```kotlin
// repete o 'print' enquanto a variável 'x' tiver um valor menor que 10
var x = 0
while (x < 10) {
    println(x.toString())
    x++
}
```

### Funções

Conjunto de comando agrupados em um bloco, que recebe um nome e através deste nome pode ser chamado em outras partes do código
Na prática, utilizamos funções para separar melhor nossa lógica

Utilizamos a palavra `fun`, seguida do nome da função, seus argumentos e seu retorno

```kotlin
// Exemplo de função com o nome 'somar'
// recebe 2 argumentos inteiros e retorna a soma
fun somar(n1: Int, n2: Int): Int {
    return n1 + n2
}

// para chamar a função
val resultado = somar(5, 7)
```

`return` serve para devolver o resultado
Nem todas as funções possuem retorno, para esses casos o retorno da função é `Unit` e não precisamos utilizar a palavra `return`

```kotlin
fun imprimir(texto: String): Unit{
    println(texto)
}
```

`Unit` para indicar que essa função não possui retorno
Eu posso omitir a palavra `Unit`

```kotlin
fun imprimir(texto: String){
    println(texto)
}
```

**Single-Expression Functions**
- Funções de expressão única
- Possui apenas uma linha
- Não sendo necessário o uso das chaves {}

```kotlin
fun somar(n1: Int, n2: Int) = n1 + n2

fun imprimir(texto: String) = println(texto)

// Não foi preciso usar a palavra 'return'
// nem definir o tipo de retorno
```

### Orientação a Objetos

Kotlin trabalha com:
- Paradigma de orientação a objetos
- Paradigma Funcional

POO é um modelo baseado em objetos
Um objeto é uma abstração de algo que pode ou não ser do mundo resultado
Um objeto pode ter características e executar ações
- Características são chamadas de **propriedades** 
- Ações são chamadas de **métodos** 

Para criar um objeto devemos criar uma **classe**
Em uma `classe` colocaremos a programação do objeto
Uma `classe` é como um molde para a criação do objeto
Uma `classe` pode criar `N objetos`
Palavra `class` seguida pelo nome da classe

```kotlin
class Carro{

}
```

Definir suas propriedades
Definir seus métodos

```kotlin
class Carro {

    var cor: String = ""
    var modelo: String = ""

    fun acelerar(){
        println("Acelerando")
    }

    fun frear(){
        println("Freando")
    }
}
```

Sempre que eu quiser utilizar este objeto, basta criar uma instância dele:

```kotlin
val c = Carro()
c.cor = "Azul"
c.modelo = "Nissan 350z"
c.acelerar()
```

#### Herança entre as classe

Criar subclasses de alguma outra classe
Uma classe pode herdar características e métodos de outra classe
Para fazer a herança de uma classe, devemos colocar `:` na frente do nome da classe, e em seguida, a classe pai

```kotlin
class CarroEspecial : Carro(){

    fun fazerDrift(){
        // implementação
    }
}
```

Dessa forma a classe `CarroEspecial` herda todas as propriedades e métodos da classe `Carro`
Utilizar a palavra `open` da definição da classe

```kotlin
open class Carro {

    var cor: String = ""
    var modelo: String = ""

    fun acelerar(){
        println("Acelerando")
    }

    fun frear(){
        println("Freando")
    }

}
class CarroEspecial : Carro(){

    fun fazerDrift(){
        // implementação
    }
}
```

#### Classe de dados

- "Data class"
- Nenhum método
- Somente propriedades
- classe somente para guardar informações
- `data class`

```kotlin
data class Usuario(var nome: String, var email: String, var senha: String)
```
