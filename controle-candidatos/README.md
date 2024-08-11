## Criando Um Pequeno Sistema Para Validação de Processo Seletivo

Crie o projeto controle-candidatos.

Dentro do projeto, crie a classe ProcessoSeletivo.java para realizar toda a codificação do nosso programa.

### Case 1
Vamos imaginar que em um processo seletivo existe o valor base salarial de R$ 2.000,00 e o salário pretendido pelo candidato. Vamos elaborar um controle de fluxo onde:

- Se o valor salário base for maior que valor salário pretendido, imprima: LIGA PARA O CANDIDATO;

- Senão se o valor salário base for igual ao valor salário pretendido, imprima: LIGAR PARA O CANDIDATO COM A CONTRA PROPOSTA;

- Senão imprima: AGUARDANDO RESULTADO DEMAiS CANDIDATOS.


### Case 2
Foi solicitado que nosso sistema garanta que diante das inúmeras candidaturas sejam selecionados apenas no máximo 5 candidatos para a entrevista onde o salário pretendido seja menor ou igual salário base.

// Array com a lista de candidatos

String [] candidatos = {"FELIPE", "MARCIA", "JULIA", "PAULO", "AUGUSTO", "MONICA", "FABRICIO", "NIRELA", "DANIELA", "JORGE"};

 // Método que simula o valor pretendido

 import java.util.concurrent.ThreadLocalRandom;
 static double valorPretendido() {
   return ThreadLocalRandom.current().nextDouble(1800, 2200);
 }

### Case 3
Agora é hora de imprimir a lista de candidatos selecionados para dispoonibilizar para o rh entrar em contato.

### Case 4
O RH deverá realizar um ligação com no máximo 03 tentativas para cada candidato selecionado e caso o candidato atenta, deve-se imprimir.

- "CONSEGUIMOS CONTATO COM [CANDIDATO] APÓS [TENTATIVAS] TENTATIVAS"
- Do contrário imprima: "NÃO CONSEGUIMOS CONTATO COM O [CANDIDATO]"

public class ProcessoSeletivo {
    public static void main(String[] args) throws Exception {
        
        String [] candidatos = {"FELIPE", "MARCIA", "JULIA", "PAULO", "AUGUSTO"};
        //Primeiro um for para selecionar os candidatos       
    } 
}

static void case4(String candidato){
    int tentativasRealizadas = 1;
    boolean continuarTentando = true;
    boolean atendeu = false;
    do {
        atendeu = atender();
        continuarTentando = !atendeu;
        if (continuarTentando){
            tentativasRealizadas++;
        }else{
            System.out.println("CONTATO REALIZADO COM SUCESSO")
        }
    }while(continuarTentando && tentativasRealizadas < 3);
    if(atendeu){
        System.out.println("CONSEGUIMOS CONTATO COM [CANDIDATO] NA [TENTATIVASREALIZADAS] TENTATIVAS")
    }
    else{
        System.out.println("NÃO CONSEGUIMOS CONTATO COM O [CANDIDATO], NÚMERO MÁXIMO TENTATIVAS [TENTATIVASREALIZADAS] REALIZADAS")
    }

    // Método auxiliar
    static boolean atender(){
    return new Random().nextInt(3) == 1;
    }
}

// Método auxiliar
static boolean atender(){
    return new Random().nextInt(3) == 1;
}