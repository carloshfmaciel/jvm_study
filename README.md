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
