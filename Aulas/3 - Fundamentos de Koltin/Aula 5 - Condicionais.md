# Fundamentos de Kotlin

## Aula 5 - Condicionais

"Comandos de condicionais são os mais utilizados no dia-a-dia."

- Fazer testes
- Checar condições
- Alterar o fluxo do código
- Comparar as coisas

"Baseado em uma condição, se toma uma decisão"

| Símbolo | Significado       |
| ------- | ------------------ |
| `>`     | Maior             |
| `<`     | Menor             |
| `>=`    | Maior ou igual     |
| `<=`    | Menor ou igual     |
| `==`    | Igual             |
| `!=`    | Diferente         |


- 1 sinal de igual (`=`)
    - Atribui
    - Recebe alguma coisa

- 2 sinais de igual (`==`)
    - Igualdade
    - Comparando dois valores se são ou não iguais

- `if, else`
    - Verificar uma única condição

- `else if`
    - Testes encadeados

"O programa testa as condições na ordem em que estão escritas."

```kotlin
if(numero < 4){
    println("menor que 4")
}else if(numero == 4){
    println("igual a 4")
}else{
    println("maior que 4")
}
```

**Atribuição com if's**

- em Kotlin o `if` é uma expressão, ou seja, ela retorna um valor

```kotlin
var parImpar: String
var numero = 4

parImpar = if(numero % 2 == 0) "par" else "impar"
```

**When**

- Jeito idiomático/elegante
- Múltiplas condições
- Semelhante ao `Switch`
- Também é uma expressão

```kotlin
when{
    numero < 4 -> println("menor que 4")
    numero == 4 -> println("igual a 4")
    else -> println("maior que 4")
}
```
```kotlin
// Atribuição com when
fun main() {
    var numero = 5
    var parImpar: String

    parImpar = when{
        numero % 2 == 0 -> "par"
        else -> "impar"
    }
}
```
