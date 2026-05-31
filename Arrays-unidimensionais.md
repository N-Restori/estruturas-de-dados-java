***Estruturas básicas de Array unidimensional []***
Quando precisamos armazenar um conjunto de informaçoes de tamanho definido usando um mesmo identificador, utilizamos os arrays.
Cada posiçao de memoria do array representa uma variável.

ex. Array: int[] notaFinal = new int[10]| Leitura: Tudo que estiver dentro deste array int[] é uma posiçao de memória de numero inteiro. Temos 10 posiçoes disponíveis alocadas sob o nome notaFinal
[1] [2] [3] [4] [5] [6] [7] [8] [9] [10]

ex. Array: char[] notaLetra = new char[6] | Leitura: Tudo o que estiver dentro deste array char[] é uma posiçao de memoria de caractere único. Temos 6 posiçoes disponíveis alocadas sob o nome notaLetra
[A] [B] [C] [D] [E] [F]

ex. Array: String[] pessoa = new String[7] | Leitura: Tudo o que estiver dentro deste array String[] é uma posiçao de memória de texto. Temos 7 posiçoes disponíveis alocadas sob o nome pessoa
[Ana] [Pedro] [Paulo] [Artur] [Marcelo] [Cassio] [Amanda]

Aqui temos posiçoes de memória para armazenar as informaçoes de int notaFinal, char notaLetra, String pessoa. Quando juntamos essas informaçoes sobre um mesmo identificador em um bloco de memória, chamamos de posiçoes de memória contigua.
Cada item do Array chamamos de elemento.
O Array precisa ser instanciado com a palavra reservada new, caso nao seja, nao estará apontando para um objeto na memoria -> null, sob o erro null pointer exception (exceçao de ponteiro nullo)
Leitura: Está tentando acessar um valor de um objeto que nao foi instaciado.

Instanciando o Array:
    int[] notaFinal = new int[10] | Essa é a estrutura para todos os tipos de array

Quando o array é criado, suas posiçoes sao inicializadas com valores pré-determinados pelo Java.
    ex. array de inteiros: int[10] = [0] [0] [0] [0] [0] [0] [0] [0] [0] [0]
    ex. array de boolean: boolean[10] = [false] [false] [false] [false] [false] [false] [false] [false] [false] [false]
    ex. array de texto: String[10] = [null] [null] [null] [null] [null] [null] [null] [null] [null] [null]
    ex. array de objetos: Pessoa[10] = [null] [null] [null] [null] [null] [null] [null] [null] [null] [null]
    ex. array de char: char[10] = [\u0000] [\u0000] [\u0000] [\u0000] [\u0000] [\u0000] [\u0000] [\u0000] [\u0000] [\u0000]

Acessando os elementos: 
Sempre começa na posiçao 0
    Ex. Array de 10 posiçoes notaAluno: [0]  [1]  [2]  [3]  [4]  [5]  [6]  [7]  [8]  [9]
    notaAluno[5] -> estamos acessando o numero alocado na posiçao 5 da memoria dentro do array

Atribuindo valor a uma posiçao do array:
    ex. notaAluno[5] = 89 | Leitura: A posiçao de memoria 5 do array de inteiros notaAluno recebe 89
    ex. notaAluno[7] = 60
    ex. notaAluno[0] = 99
Até receber um valor, o restante das posiçoes continua padrao, ficaria assim: [99] [0] [0] [0] [0] [89] [0] [60] [0] [0]

Quando criamos um array, automaticamente o Java cria o atributo length, que guarda o tamanho total do array.
Se temos um array com 10 posições, o length vale 10. Como o 0 representa o primeiro espaço, o último índice é o 9. Então, para acessar o último elemento usando o tamanho, fazemos sempre length-1.

Imprimindo as informaçoes do array: 
    Pessoa[] p = new Pessoa[10]; | Leitura: A variável p do array Pessoa[] instancia o array com 10 posições do tipo objeto, inicializadas automaticamente com valor padrão null.
    for(int i=0; i<p.length; i++){ | Leitura: O laço de repetição for inicializa a variável de controle i na posição 0, define que a repetição continuará enquanto i for menor que o tamanho total do array (p.length), e incrementa i em 1 unidade a cada rodada.
        p[i] = new Pessoa("Pessoa"+i); | Leitura: A posição de memória p[i] do array instancia um novo objeto da classe Pessoa,ou seja, cada 'p[i]' representa uma Pessoa, substituindo o valor null anterior e passando o texto "Pessoa" somado ao número do índice atual como argumento.
        Rodada 1: p[0]
        Rodada 2: p[1]
        Rodada 3: p[2]...

        System.out.println(p[i]); | O comando de saída acessa a posição de memória p[i] do array e imprime uma a uma a informação do objeto alocado naquela posição.
        Impressao na tela:
        Pessoa 0 
        Pessoa 1
        Pessoa 2...
    }


