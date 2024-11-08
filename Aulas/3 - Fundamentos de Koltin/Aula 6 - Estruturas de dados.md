# Fundamentos de Kotlin

## Aula 6 - Estruturas de dados

jeito de representar a informação salva no computador

lists, maps, arrays

A escolha da estrutura de dados facilita a solução

### Array
coleção de intes
do mesmo tipo
tamanho fixo

Array<int> == IntArray
para os tipos primitivos o Kotlin ja tem tipo especializados

```kotlin
fun main() {
    var array  : Array<Int> = Array(5) {0}
    // 5 posições e iniciar com 0
    var array2 : IntArray = IntArray(3)
    // 3 posições, por padrão inicia com 0s
}
```
operações
'get e set' ou []
sempre inicia com índice 0
um array de 3 posições, os indexes são 0,1,2

```kotlin
array[2] = 2            // salva o valor no index 2 
array.set(3,4)          // salva o valor 4 no index 3

println(array[0])       // pega o valor no index 0
println(array.get(1))   // pega o valor no index 1
```

### Listas

similar ao aarray
lista não tem tamanho definido
se sabe o tamanho do tamanho , usa array, senão lista


```kotlin
fun main() {
    var mutableList : MutableList<Int> = multableListOf()
    var list : List<Int> = listOf(1)    // imutável de único valor 1

    mutableList.add(1)      // adiciona o valor no final da lista
    mutableList.add(0,4)    // adiciona o valor 4 na posição 0
    mutableList.sort()      // ordena a lista de forma crescente
    mutableList.remove(0)   // remove o elemento na posição 0
    mutableList.set(0,5)    // salva o valor 5 na posição 0
    mutableList[0] = 5      // salva o valor 5 na posição 0
    mutableList.get(1)      // pega valor da posição 1
    mutableList[1]          // pega valor na posição 1
}
```

### Map

chave-valor
lista de contato
'Mateus': 123

```kotlin
var mutableMap : MutableMap<String, String> = mutableMapOf()    // map vazio
var map : Map<Int, String> = mapOf(Pair(1,"teste"))             // mapa com 1 valor

mutableMap.put("chave1","valor1")       // adiciona a chave1 no map
mutableMap["chave1"] = "valor2"         // atribuindo nova valor a "chave1"
mutableMap.set("chave1,"valor3")        // "chave1" recebendo o "valor3"
mutableMap["chave1"]                    // lendo "chave1"
mutableMap.get("chave1")                // lendo "chave1"
mutableMap.contains("chave1")           // se já exsite "chave1"
mutableMap.containsValue("valor1")      // se ja tem o "valor1"
mutableMap.keys                         // lista de todas as chaves
mutableMap.values                       // lista de todos os valores
```