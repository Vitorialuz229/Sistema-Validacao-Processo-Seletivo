# Criando um pequeno Sistema para validação de Processo Seletivo

## Case 1:
Vamos imaginar que em um processo seletivo existe o valor base salarial de R$2.000,00 e o salário pretendido pelo candidato.
Vamos elaborar um controle de fluxo onde:

* Se o valor salário base for maior que o valor pretendido, imprima: *LIGAR PARA O CANDIDATO*;
* Se o valor do salário base for igual ao valor salário pretendido, imprima: *LIGAR PARA O CANDIDATO COM CONTRA PROPOSTA*;
* Senão imprima: *AGUARDADO RESULTADO DEMAIS CANDIDATOS*

## Case 2: 
Foi solicitado que nosso sistema garanta que diante das inúmeras candidaturas sejam selecionadas apenas no máximo 
5 candidados para entrevista onde o salário pretendido seja menor ou igual ao salário base.

```java
// Array com a lista de candidados 
String [] candidados = {"FELIPE", "MARCIA", "JULIA", "PAULO", "AUGUSTO", "MONICA", "FABRICIO", "MIRELA", "DANIELA", "JORGE"}

//Método que simula o valor pretendido
import java.util.concurrent.ThreadLocalRandom;
static double valorPretendido() { 
    return ThreadLocalRandom.current().nextDouble(1800, 2200);
}
```
## Case 3: 
Agora é hora imprimir a lista dos candidatos selecionados para disponibilizar para o RH entrar em contato.

## Case 4: 
O RH deverá realizar uma ligação com no máximo 03 tentativas para cada candidato selecionado e caso o candidato atenda, deve-se imprimir: 

* *"CONSEGUIMOS CONTATO COM [CANDIDATO] APÓS [TENTATIVA] TENTATIVAS"*
* do contrario imprima: "NÃO CONSEGUIMOS CONTATO COM [CANDIDATO]"

```java 
import java.util.Random; 

//método auxiliar 
static boolean atender() { 
    return new Random().nextInt(3) == 1;
}
```