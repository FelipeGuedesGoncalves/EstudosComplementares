## Princípios Básicos em Kotlin

comentários podem ser feitos em linhas singulares com "//" e "/* trecho de texto */

### Variáveis e Constantes
são identificadores que armazenam dados específicos reutilizáveis, podendo ser declaradas como `var` (**Variáveis** - mutáveis) ou `val` (**Constantes** - imutáveis), esta sendo utilizada quando queremos ter uma segurança a mais durante o desenvolvimento, pois a própria IDE bloqueará sua edição.

Vale citar que toda variável é composta pelo identificador de criação val ou var, seguido do nome da mesma, o sinal de atribuição "=" e o valor que será atribuído.
 
Veja abaixo um exemplo:

```kotlin
var nomeFaculdade = "FIAP"

```

Para chamar esta variável em outros trechos do código basta  evidenciá-la em trechos posteriores:

```kotlin

var nomeFaculdade = "FIAP"

println(nomeFaculdade)
```

Vale notar que a variável `nomeFaculdade` neste caso foi inicializada com um valor string, e portanto, terá este tipo de valor durante todo o seu uso. Em adição, é importante lembrar que este tipo "string" foi atribuído à variável automaticamente (inferida) pelo o uso de aspas duplas, mas ao utlizar outros tipos como int, double, long, é necessário que haja sua evidenciação no código, veja abaixo:

```kotlin
 
var idade: Byte = 19

println(idade)
```

As variáveis numéricas são aquelas que demandam mais atenção em sua tipagem, confira abaixo as principais:

|Identificador|Espaço na memória|Categoria|
|:-----------:|:---------------:|:--------:|
|Long|64|Inteiro|
|Int|32|Inteiro|
|Short|16|Inteiro|
|Byte|8|Inteiro|
|Double|64|Decimal|
|Float|32|Decimal|

O espaço na memória se dá pela equação: 2 elevado ao valor em bits, através disso obtemos a fatia de números que podemos armazenar na variável declarada, todavia, o intervalo citado abrange tanto os números negativos como positivos, portanto, um ***Byte***, por exemplo, pode guardar todos os números presentes em um intervalo de 256 valores, que vão de -128 a 127 (0 sendo considerado positivo). Sem fosse atribuído um valor de 128, por exemplo, teríamos a ocorrência de overflow.

Caso haja dúvidas no limite de tamanho, basta utilizar este trecho de código:

```kotlin

println(Byte.MAX_VALUE)

//ou

println(Byte.MIN_VALUE)

```

