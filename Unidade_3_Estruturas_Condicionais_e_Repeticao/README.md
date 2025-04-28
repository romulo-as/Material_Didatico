# **Abstração**
Abstração é o componente mais importante dentro da programação orientada a objetos (POO). Este é o processo de aproximar o mundo real do mundo da programação, e tem como objetivo simplificar um problema difícil. Para isso, a abstração leva em conta os aspectos mais importantes de um determinado ponto de vista e desconsidera os aspectos restantes.
Em resumo, a abstração se concentra apenas nas informações importantes para seu propósito, mantendo suas classes o mais simples possível e se concentrando no que realmente importa para uma determinada finalidade, ou seja, quando você tem algo muito grande, mas não há necessidade de cadastrar todas informações, você abstrai coisas.  
  

**Na prática:**  
Vamos supor que você está desenvolvendo um código com a classe
“ser humano”. Essa classe é composta por inúmeros atributos, como por exemplo: altura, peso, cor da pele, cor do olho, CPF, nome, endereço etc.
O objetivo do seu código é tratar o “ser humano” como cliente.
Para cada cliente é preciso obter as informações de CPF, Nome e
Endereço. As outras informações que pode obter na classe “ser
humano”, como cor da pele, cor do olho, altura, peso etc. não são
importantes para esta situação.
Portanto, podemos abstrair estas informações e considerar
somente o que importa.  

Em java podemos declarar uma classe abstrata da seguinte forma:  

    package objetos; //informa em qual pacote a classe está sendo criada, no caso pacote objetos.

    public abstract class Humano{  //Esta é a classe abstrata Humano
        public abstract void realizarPagamento(); //Este é o método abstrato realizarPagamento. Não necessita ter um corpo.
    }

Uma classe abstrata não pode ser instanciada, mas ela pode ter atributos e métodos abstratos, como no exemplo acima, criamos um método abstrato realizarPagamento, que deverá ser, obrigatóriamente, implementado pelas classes filhas dessa classe, ao contrário de algum método comum, que não precisa ser obrigatóriamente implementado. Vamos criar uma classe filha Mulher dentro do mesmo pacote, que implementa esse método.

    package objetos;

    public class Mulher extends Humano{  // extends é a palvra reservada para herança. Humano é a classe mãe.
        public void realizarPagamento(){   //Este é o método abstrato realizarPagamento impelmentado na classe filha.
        System.out.println("Pagamento realizado com sucesso!");   //Este é o corpo do método abstrato.
        }
    }

##  Estruturas Condicionais  

É uma estrutura de controle que permite definir que um certo bloco de comandos somente será executado dependendo de uma condição, se a condição for verdadeira, um bloco será executado, se for falsa outro bloco será executado.  
Temos basicamente dois tipos de estruturas condicionais, as simples e as compostas.  

<b>Simples</b>: Se a condição for verdadeira, ela executa o bloco de comandos, e se for falsa, ela pula o bloco de comandos.  
	
	if ( condição ) {
		      <comando 1>  
		      <comando 2>  
	}	

<b>Composta ou de controle</b>: Se a condição for verdadeira, executa o bloco do if, se for falsa, executa somente o bloco do else.   

	if ( condição ) {   
		<comando1>  
		<comando2>  
	}  
	
	else {  
		<comando3>  
		<comando4>  
	}  

##  Expressão Condicional Ternária  

É uma estrutura opcional ao if-else quando há o desejo de decidir um valor com base em uma condição. 
Sintaxe:   
	( condição ) ? valor_se_verdadeiro : valor_se_falso

Por exemplo:
	
	( 2 > 4 )? 51 : 81     		Resultado: 81  
	(  11 != 3 ) ? "Maria" : "William"	Resultado: "Maria"  

Na primeira expressão, como ela é falsa, o resultado dá o segundo numero após a interrogação, ou seja "81".  
Na segunda expressão, como ela é verdadeira, o resultado dá o primeiro nome após a interrogação, que é "Maria".  


# Estruturas Repetitivas  

## Estrutura repetitiva "enquanto" (while)  

A estrutura while é uma estrutura de controle que repete um bloco de comandos enquato uma condição for verdadeira.  

<b>Quando usar:</b> Utiliza-se o while quando <b>não</b> se sabe previamente a quantidade de repetições que será realizada.  

Exemplo: Escrever um programa que lê números inteiros até que um zero seja lido. Ao final mostra a soma dos números lidos.  
Enquanto não for digitado o número 0, o programa irá armazenar os números digitados e ao final entregará a soma desses números na saída. Nesse caso se sabe previamente quantos números serão digitados, por isso é interessante usar o while.  

<b>Sintaxe/Regra</b>  

    while (condição) {  
        comando 1  
        comando 2
    }  

Regra:  
    V: executa e volta
    F: pula fora  

Note que a sintaxe é igual a da estrutura if, ou seja, se a condição for verdadeira, execute o bloco de comandos, se falsa, pule fora. A diferença é que no while, quando a condição é verdadeira ele executa e volta, ou seja, executa novamente, <b>enquanto</b> a condição for verdadeira.   

## Estrutura Repetitiva "para" (for)  

A estrutura repetitiva for é uma estrutura de controle que repete um bloco de comandos para um certo intervalo de valores.  

<b>Quando usar:</b> Usa-se o "for" quando se sabe previamente a quantidade de repetições, ou o intervalo de valores.  

Exemplo: Fazer um programa que lê um valor inteiro N e depois N números inteiros. Ao final, mostra a soma dos N números lidos.  

<b>Sintaxe/regra</b>  

    for ( início ; condição ; incremento ) {      
        comando 1  
        comando 2
    }  

<b>início:</b> Executa somente na primeira vez.  
<b>condição:</b> Se verdadeira, executa e volta, como no while, se falsa, pula fora.  
<b>incremento:</b> Executa toda vez depois de voltar. Ou seja, se a condição foi verdadeira, executou o bloco de comandos, voltou a primeira vez, executa o incremento, e enquanto a condição for verdadeira, o processo será repetido.  
  
<b>Nota:</b> "i++" é a forma resumida de se escrever "i = i + 1". Utilizado para incrementos.  

## Estrutura Repetitiva "faça-enquanto"  

Essa estrutura é menos utilizada que o "while" ou "for", mas em alguns casos ela se encaixa melhor ao problema.  
A grande diferença entre o "do-while" para as outras estruturas é que o bloco de comandos será executado pelo menos uma vez, pois a condição é verificada no final, já as outras duas estruturas verificam a condição no início, e se a condição é falsa no início, aquelas estruturas não executam o código nenhuma vez.  

<b>Sintaxe/regra</b>  

    do {
        comando 1
        comando 2
    
    } while ( condição );  

Note que nessa estrutura, se a condição for verdadeira após a execução ela volta, se falsa, pula fora.   

**VAMOS PRATICAR!!**  

---

Atividades Práticas de JAVA: A Jornada do Aprendizado!
Tema: Aventura em uma Galáxia Muito Distante
Nível: Intermediário
Objetivo: Consolidar e expandir o conhecimento sobre loops for e while em JAVA
através de desafios temáticos.

---

**Atividade 1: Decifrando Mensagens Estelares com for**


Cenário: Você é um(a) criptoanalista espacial e interceptou uma série de mensagens
codificadas de diferentes planetas. Cada mensagem é uma string, e você precisa
decifrá-las para entender as intenções dos alienígenas.
Tarefa:  
1. Crie uma lista contendo pelo menos 3 mensagens codificadas. As mensagens
devem conter letras maiúsculas, minúsculas, números e símbolos.
2. Utilize um loop for para iterar sobre cada mensagem da lista.
3. Dentro do loop, para cada mensagem:
    <ul>
    <li>Crie uma nova string vazia para armazenar a mensagem decifrada.</li>  
    <li>Utilize outro loop for (aninhado) para iterar sobre cada caractere da mensagem codificada.</li>  
    <li>Dentro do loop aninhado, aplique as seguintes regras de decodificação:</li>
            <ul>
            <li>Se o caractere for uma letra minúscula, adicione-o à mensagem decifrada.</li>  
            <li>Se o caractere for uma letra maiúscula, converta-o para minúsculo e adicione-o à mensagem decifrada.</li>  
            <li>Ignore números e símbolos.</li>  
            </ul>
    <li>Imprima a mensagem codificada original e a mensagem decifrada.</li>  
    </ul>
---
**RESOLUÇÃO**  

    package espacial;

    //importação de bibliotecas necessárias para trabalhar com listas.  
    import java.util.ArrayList;  
    import java.util.List;  

    //criação da classe Mensagem.  
    public class Mensagem {  
        public static void main(String[] args) {  
        //Declarando e instanciando uma lista de mensagens.  
            List<String> mensagensCodificadas = new ArrayList<>();  
            //usando o método add para adicionar elementos na lista.  
            mensagensCodificadas.add("Cor1-i@nTH!IaNs");  
            mensagensCodificadas.add("AlErTa@M4ald1it0oo!");  
            mensagensCodificadas.add("Vie13m0%osem@P4aZ");  

            for (String mensagem : mensagensCodificadas) {  

                String decifrada = "";  
                for (char c : mensagem.toCharArray()) {  
                    if (c >= 'a' && c <= 'z') {  
                        decifrada += c;  
                    }  
                    else if (c >= 'A' && c <= 'Z') {  
                        decifrada += Character.toLowerCase(c);  
                    }  
                }  
                System.out.println("Original: " + mensagem);  
                System.out.println("Decifrada: " + decifrada);  
                System.out.println("---------------------");  
        }  
        }  
    }  

---



---


**Atividade 2: Navegação Segura em um Campo de Asteroides com while**


Cenário: Você é um(a) piloto de Millennium Falcon e precisa navegar sua nave por um campo de
asteroides perigoso. Você tem um sensor que detecta a distância do asteroide mais
próximo.  
Tarefa:
1. Defina uma distância inicial segura (um número inteiro positivo).
2. Utilize um loop while para simular a navegação. O loop deve continuar enquanto a
distância do asteroide mais próximo for menor que a distância segura.
3. Dentro do loop:  
    <ul>
    <li>Gere uma distância aleatória para o asteroide mais próximo (um número inteiro entre 1 e 10).</li>
    <li>Imprima a distância do asteroide.</li>
    <li>Se a distância for menor que 3, imprima uma mensagem de "PERIGO!" e encerre o loop usando break.</li>
    <li>Se a distância for menor que a metade da distância segura, imprima um aviso de "Aproximando-se de asteroide!".</li>
    <li>Aumente a distância segura em um valor fixo (por exemplo, 2) para simular o piloto se afastando dos asteroides.</li>
    </ul>
4. Se o loop terminar sem ser interrompido por break, imprima uma mensagem de
"Navegação concluída com segurança!".

---

**RESOLUÇÃO**  

    package espacial;

    // importação de bibliotecas necessárias para trabalhar com números aleatórios.
    import java.util.Random;

    public class CampoAsteroides {
        public static void main(String[] args) {
            // 1. definição da distancia segura
            int distanciaSegura = 5;
            Random random = new Random();
            boolean perigoEncontrado = false;

            // 2. criação de um Loop while para simular a navegação
            while (true) {
                // 3a. Geramos a distância aleatória do asteroide entre 1 e 10
                int distanciaAsteroide = random.nextInt(10) + 1;

                // verificação da condição de saída do loop
                if (distanciaAsteroide >= distanciaSegura) {
                    break;
                }

                // 3b. imprimir a distância detectada
                System.out.println("Distância do asteroide: " + distanciaAsteroide);

                // 3c. verificação das condições de Asteróides críticos
                if (distanciaAsteroide < 3) {
                    System.out.println("PERIGO! Asteroide crítico detectado!");
                    perigoEncontrado = true;
                    break;
                }
                else if (distanciaAsteroide < distanciaSegura / 2) {
                    System.out.println("Aviso: Aproximando-se de asteroide!");
                }

                // 3d. aumentar a distância segura
                distanciaSegura += 2;
            }

            // 4. verificação de conclusão de navegação segura
            if (!perigoEncontrado) {
                System.out.println("\nNavegação concluída com segurança!");
            }
        }
    }

---

Atividade 3: Batalha Espacial Intergaláctica com for e while  
Cenário: Você é um piloto de X-Wing a serviço da Resistência contra o Império e está atravessando uma galáxia com sua nave quando se depara com TIE Fighters, naves de caça da tropa Imperial, e entram em uma batalha intergaláctica. Você tem um número limitado de torpedos de prótons e precisa usá-los estrategicamente para destruir as naves inimigas.

Tarefa:   
1. Defina o número inicial de torpedos (um número inteiro positivo).  
2. Crie uma lista com os nomes de pelo menos 3 naves inimigas.   
3. Utilize um loop while para simular a batalha. O loop deve continuar enquanto você tiver munição E houver naves inimigas na lista.
4. Dentro do loop:  
    <ul>
    <li>Imprima o número de torpedos restantes e a lista de naves inimigas.</li>
    <li>Solicite ao usuário que escolha qual nave inimiga atacar (usando o índice da lista).</li>
    <li>Implemente tratamento de erros para garantir que o usuário digite um índice válido.</li>  
    <li>Se o usuário digitar um índice inválido, exiba uma mensagem de erro e continue para a próxima iteração do loop usando continue.</li>
    <li>Se o usuário digitar um índice válido:
        <ul>  
        <li>Remova a nave inimiga da lista.</li>  
        <li>Diminua o número de munição em 1.</li>
        <li>Imprima uma mensagem informando qual nave foi destruída.</li>
        </ul>  
    <li>Se o número de munição chegar a zero, imprima uma mensagem de "Sem torpedos de prótons! Retirada estratégica pelo hiperespaço!!".</li>
    <li>Se todas as naves inimigas forem destruídas, imprima uma mensagem de "Vitória! Todas as naves inimigas foram destruídas!".</li>

---

**RESOLUÇÃO**

    package espacial;  

    import java.util.ArrayList;
    import java.util.List;
    import java.util.Scanner;

    public class Batalha {
        public static void main(String[] args) {
            Scanner ler = new Scanner(System.in);
            //definindo o quantos mísseis a nave possui
            int m = 4;

            //declarando e instanciando uma nova lista.
            List<String> navesInimigas = new ArrayList<>();

            //adicionando nome das naves inimigas.
            navesInimigas.add("TIE Fighter Alpha");
            navesInimigas.add("TIE Fighter Beta");
            navesInimigas.add("TIE Fighter Charlie");

            //isEmpty() é um método que verifica se uma lista, um conjunto ou uma string está vazia.
            while (m > 0 && !navesInimigas.isEmpty()) {
                System.out.printf("\nVocê possuí %d torpedos de prótons...\n", m);
                System.out.printf("Atenção X-Wing T-65B, frota Imperial se aproximando, %d naves inimigas!!\n", navesInimigas.size());
                System.out.println("Identificando tropas...\n");
                int i; //variável inteira indice que será utilizada para percorrer o ArrayList.

                //utilizando o loop for para percorrer o ArrayList e imprimir os componentes na tela.
                for (i=0; i<navesInimigas.size(); i++) {
                    System.out.printf("Posição %d- %s\n", i, navesInimigas.get(i));
                }

                System.out.println("Qual posição deseja atacar, piloto?: ");
                String input = ler.nextLine(); //Declaração de variável tipo String para armazenar a posição escolhida.

                try {
                    int posicao = Integer.parseInt(input); //nova variável para converter a posição escolhida em um número inteiro

                    //condição caso posicao seja menor que 0 OU maior que o tamanho da lista.
                    if (posicao < 0 || posicao >= navesInimigas.size()) {
                        System.out.println("Error: Esta posicão não existe...");
                        continue; //volta para o inicio do loop
                    }
                    //Se posicao for um número inteiro dentro do range permitido, segue para cá!
                    String naveDestruida = navesInimigas.remove(posicao);
                    m = m - 1;
                    System.out.printf("Nave %s abatida!!\n\n", naveDestruida);


                } catch(NumberFormatException e) { //exceção lançada quando se tenta converter uma string para um valor numérico, mas essa string não contém um formato numérico válido
                    System.out.println("Entrada inválida. Digite um número: ");
                    continue; //Volta para o inicio do loop
                }
            }
            //condição se navesInimigas estiver vazia, informa a vitória
            if (navesInimigas.isEmpty()) {
                System.out.println("\nVitória! Todas as naves inimigas foram destruídas!");
            } else { //caso acabem as munições e ainda há naves inimigas vivas, segue aqui.
                System.out.println("Sem torpedos de prótons! Retirada estratégica pelo hiperespaço!!");
            }
            ler.close();
        }
    }
