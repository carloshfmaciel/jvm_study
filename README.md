# JVM Compilers e Code Cache

## Jit(Just In Time) Compilation

#### Saber quais métodos são Nativos
```java
-XX:+PrintCompilation
```

![image](https://github.com/carloshfmaciel/jvm_study/blob/master/001.PNG)

| Coluna |  |
| -------- | -------- |
| Coluna 1 | Tempo em ms desde que a JVM iniciou |
| Coluna 2 | A ordem em que o método foi compilado
| Coluna 3 | O Level de compilação do método |
|    n     | Indica que o método foi compilado para o modo nativo
|    s     | Indica que o método é sicronizado |
|    %     | Indica que o método está no Code Cache

![image](https://github.com/carloshfmaciel/jvm_study/blob/master/002.PNG)

Quanto mais acessado um método, maior será o level de compilação

Logar o compile em arquivo
-XX:+UnlockDiagnosticVMOptions -XX:+LogCompilation

Code Cache
Área da memória em que um método pode ser acessado mais rápido
Método pode ser movido para dentro e para fora do Code Cache, de acordo com o acesso

Acessar o tamanho do Code Cache
-XX:+PrintCodeCache

![image](https://github.com/carloshfmaciel/jvm_study/blob/master/003.PNG)

- Java 8 ou posterior - Tamanho Maximo Code Cache - 240Mb
-XX:+InitialCodeCacheSize (Tamanho inicial)
-XX:+ReservedCodeCacheSize (Tamanho máximo)
-XX:+CodeCacheExpansionSize (Quão rapido ele pode crescer, Quanto espaço extra adicionamos a cada time que crescemos)
- Valores podem ser em bytes(k), kbytes(kb) ou mbytes(mb)

Monitorando Code Cache - Remote Server - JConsole

1 – Acessar o diretório do seu user abaixo:
