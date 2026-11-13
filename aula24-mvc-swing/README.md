# Aula 24 — MVC com Swing (StarLog Logistics)

Kit do professor com a tela pronta. Foram completados o fail-fast e o `calcularSeguro()` da `Carga` (2% do valor + R$ 150 se perigosa ou acima de 100 kg) e o `cadastrarCarga` do `CargaController`, que converte os textos e trata `NumberFormatException` e `IllegalArgumentException`.

## Como rodar

Abra o terminal na pasta do projeto (onde está este README). É preciso ter o JDK 17 ou superior.

**macOS / Linux**

```bash
javac -encoding UTF-8 -cp "lib/*" -sourcepath src -d bin src/br/com/starlog/main/MainApp.java
java -cp "bin" br.com.starlog.main.MainApp
```

**Windows**

```bat
javac -encoding UTF-8 -cp "lib/*" -sourcepath src -d bin src\br\com\starlog\main\MainApp.java
java -cp "bin" br.com.starlog.main.MainApp
```

## Testes (JUnit 5)

**macOS / Linux**

```bash
javac -encoding UTF-8 -cp "bin:lib/*" -d bin test/br/com/starlog/test/CargaMvcTest.java
java -jar lib/junit-platform-console-standalone-1.10.2.jar -cp bin --select-class br.com.starlog.test.CargaMvcTest
```

**Windows**

```bat
javac -encoding UTF-8 -cp "bin;lib/*" -d bin test\br\com\starlog\test\CargaMvcTest.java
java -jar lib/junit-platform-console-standalone-1.10.2.jar -cp bin --select-class br.com.starlog.test.CargaMvcTest
```

## Resultado esperado

Os 6 testes JUnit do kit passam. Na tela: peso `abc` mostra erro de formato, valor `-50` mostra a regra violada, e cargas válidas aparecem no relatório.
