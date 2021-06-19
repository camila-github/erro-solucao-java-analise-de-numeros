## Exercicio (Java): Análise de Números

O exercicio publicado é referente ao treinamento do Bootcamp Java - Aritméticos em Java 
(https://digitalinnovation.one)


#### Descrição do Desafio:

Você deve fazer a leitura de 5 valores inteiros. Em seguida mostre quantos valores informados são pares, quantos valores informados são ímpares, quantos valores informados são positivos e quantos valores informados são negativos.

#### Entrada: 

Você receberá 5 valores inteiros.

#### Saída: 

Exiba a mensagem conforme o exemplo de saída abaixo, sendo uma mensagem por linha e não esquecendo o final de linha após cada uma.

Exemplos de Entrada  | Exemplos de Saída
------------- | -------------
-5 | 3 valor(es) par(es)
0 | 2 valor(es) impar(es)
-3 | 1 valor(es) positivo(s)
-4 | 3 valor(es) negativo(s)
12 | 
 


#### Java　

```java
//SOLUCAO 1

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class AnaliseDeNumeros {
    public static void main(String[] args) throws IOException {

      BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
      StringTokenizer st;
      
      int numeroEntrada, contNumPar = 0, contNumImpar = 0, contNumPostitivo = 0, contNumNegativo = 0;
      
      for (int  i = 0; i < 5; i++) {
        
        st = new StringTokenizer(br.readLine());
        numeroEntrada = Integer.parseInt(st.nextToken());
        
        if (numeroEntrada % 2 == 0) contNumPar++;  // valida numeros pares
        if (Math.abs(numeroEntrada % 2) == 1) contNumImpar++; // valida numeros impares
        if (numeroEntrada > 0) contNumPostitivo++; // valida numeros positivos
        if (numeroEntrada < 0) contNumNegativo++; // valida numeros negativos
        
      }
  
      System.out.println(
        contNumPar + " valor(es) par(es)" + "\n" +
        contNumImpar + " valor(es) impar(es)" + "\n" +
        contNumPostitivo + " valor(es) positivo(s)" + "\n" +
        contNumNegativo + " valor(es) negativo(s)"
      );
      
      br.close();
  }
}
```

