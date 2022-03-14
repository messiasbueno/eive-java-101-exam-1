# eive-java-101-exam-1

1. Qual comando possibilita a visualização de forma resumida dos commits realizados em um repositório?
   1. :white_square_button:`git log --short`
   2. :white_check_mark:`git log --oneline`
   3. :white_square_button:`git show --all`
   4. :white_square_button:`git commits --summary`
   5. :white_square_button:`git log --summary`

2. Quais os comandos para configurar sua identidade no Git? (desconsidere o uso de flags)
   1. :white_square_button:`git config username "John Doe"`, `git config email "john.doe@db1.com.br"`
   2. :white_square_button:`git config user.name "John Doe"`, `git config email "john.doe@db1.com.br"`
   3. :white_square_button:`git config user.name "John Doe"`, `git config user.mail "john.doe@db1.com.br"`
   4. :white_check_mark:`git config user.name "John Doe"`, `git config user.email "john.doe@db1.com.br" `
   5. :white_square_button:`git config user.username "John Doe"`, `git config user.email "john.doe@db1.com.br"`

3. Qual(is) a(s) diferença(s) entre os comandos `git merge` e `git rebase`?
   * `git merge` Mantém o histórico de alteração gerando um novo commit com as alterações.
   * `git rebase` Realoca os commit's alterando seu ponto de origem.

4. No Git, é possível salvar o estado atual de seu trabalho e voltar ao estado do último commit da branch. Nesse caso, qual comando devemos utilizar? E para recuperar o trabalho posteriormente, qual é o comando?
   * `git stash` é o comando utilizado para salvar o estado do seu trabalho
      ```git
      git stash save 'Inclusão da rotina x'
      ```
   * `git stash pop` é utilizado para recuperar o trabalho salvo anteriormentes
      * Recuperar o ultimo trabalho salvo em stash 
         ```git
         git stash pop
         ```   
      * Recuperar um trabalho especifico passando o seu identificador
         ```git
         git stash pop stash@{2}
         ```

5. No contexto do Git, o que são, para que servem e em quais casos devemos criar `issues`?
   * São solicitações de alterações como, melhoria, correções e etc.
   * Ajudam a manter o controle das pendencias e compartilhar com a equipe.
   * Devemos criar para registrar as possíveis modificações a serem realizadas.

6. O que é e para que serve o `cherry-pick`?
   * É o comando utilizado para copiar commit's especificos para o branch selecionado.

7. No cotidiano de um desenvolvedor, é comum que conflitos apareçam, e é de responsabilidade do mesmo resolvê-los. Qual o processo mostrado em curso para a resolução de um conflito?
   * Resolvemos o conflitos com o merge

8. Existe uma estratégia de branching chamada Git Flow, muito comumente aplicada no desenvolvimento de software. Qual das opções abaixo representam as branches presentes nessa estratégia, de acordo com o conteúdo?
   1. :white_square_button:`master`, `develop`, `feat`, `hotfix` e `release`
   2. :white_square_button:`master`, `develop`, `feature`, `fix` e `release`
   3. :white_check_mark:`master`, `develop`, `feature`, `hotfix` e `release`
   4. :white_square_button:`master`, `develop`, `feat`, `fix` e `release`
   5. :white_square_button:`master`, `develop`, `feat`, `fix` e `rc`

9. Qual(is) a(s) diferença(s) entre JRE e JDK?
   * `JRE` Java Runtime Environment é a camada utilizada para executar os softwares da linguagem Java.
   * `JDK` Java development kit é a camada utilizada para criação de softwares da linguagem java.

10. O que é um workspace, no contexto do Eclipse?
    * É nosso diretório de trabalho, onde os projetos ficam organizados.

11. Em Java, o operador `+` possui duas funções básicas. Quais são elas? Dê um exemplo em código de cada uma delas.
    * Podemos utilizar o operador `+` para concater strings ou somar numéricos.
       ```java
       String ladoEsquerdo = "Inicio do texto";
       String ladoDireito = "Fim do texto";
       System.out.println(ladoEsquerdo + ladoDireito);
       //Resultado final `Inicio do textoFim do texto`
       ```
       ```java
       int ladoEsquerdo = 10;
       int ladoDireito = 5;
       System.out.println(ladoEsquerdo + ladoDireito);
       //Resultado final `15`
       ```

12. Ao realizar a operação abaixo, qual será o resultado mostrado no console?
    ```java
    class App {
        public static void main(String... args) {
            double divisionResult = 5 / 2;
            System.out.println(divisionResult);
        }
    }
    ```

    1. :white_square_button:`2`
    2. :white_square_button:`3.0`
    3. :white_square_button:`3`
    4. :white_square_button:`2.5`
    5. :white_check_mark:`2.0`

13. Por que o type casting "implícito" do Java não é possível no caso abaixo?
    ```java
    class App {
        public static void main(String... args) {
            float pi = 3.14;
        }
    }
    ```
    * Por padrão o java entende que o valor 3.14 é um double, assim float que possui um tamanho menor não pode receber a informação.

14. Observe o código abaixo. Ele compilará? Qual a diferença entre as variáveis `firstValue` e `secondValue`?
    ```java
    class App {
        public static void main(String... args) {
            char firstValue = 'a';
            char secondValue = 97;
        }
    }
    ```
    * O sistema compilará.
    * a representação final de ambas as variáveis será `a`
       * Devido o código 97 na tabelas ASCII ser a letra `a`

15. Observe os códigos abaixo. Ao serem compilados e executados, o que é exibido no terminal?
    ```java
    // código 1
    class App {
        boolean hasValue;
        public static void main(String... args) {
            System.out.println(hasValue);
        }
    }
    ```
    * Este código não é compilavel, a variável `hasValue` está em um contexto onde deveria ser static para poder ser utilizada desta forma.
    
    ```java
    // código 2
    class App {
        public static void main(String... args) {
            boolean hasValue;
            System.out.println(hasValue);
        }
    }
    ```
    * Este código não é compilavel, a variável `hasValue` deve ser inicializada.

16. Para que serve e quando utilizar o comando `break`?
    * Serve para interromper uma execução
    * Utilizamos para sair de loop's ou switch's

17. Quais as diferenças entre classe, objeto e referência?
    * `classe` é um modelo, onde informamos quais são suas propriedades e atribuições.
    * `objeto` é onde manipulamos as informações de uma classe.
    * `referência` é o espaço na memória que armazena a informação do objeto.

18. O que é exibido no terminal ao executar o código abaixo, considerando que ClasseExemplo não sobreescreveu o método `toString()`? Explique cada parte da estrutura do que é mostrado.
    ```java
    class App {
        public static void main(String... args) {
            ClasseExemplo exemplo = new ClasseExemplo();
            System.out.println(exemplo);
        }
    }
    ```
    ```
    Será impresso o identificador da referencia de memória da variavel
    ```
19. O que é exibido no terminal ao executar o código abaixo?
    ```java
    class Pessoa {
        Endereco endereco;
    }
    
    class Endereco {
        String cep;
    }
    
    class App {
        public static void main(String... args) {
            Pessoa aluno = new Pessoa();
            System.out.println(aluno.endereco.cep);
        }
    }
    ```
    ```
    Considerando que existe um construtor na classe da pessoa e do endereço será exibido a referencia da mémoria do objeto cep.
    Se não houver esta estrutura será apresentado um erro, pois a classe endereco não foi instanciada
    ```

20. Em Java, existem atributos e métodos de classe. Explique como declará-los e qual(is) a(s) diferença(s) entre eles e os atributos e métodos de instância.
    * Atributos são como caracteristicas de uma classe, informações que podemos preencher quando geramos objetos.
       ```java
       public class Funcionario {
           private String nome;
           private String cpf;
           private double salario;
       }
       ```
    * Métodos são como ações que a classe pode executar.
       ```java
       public class Funcionario {
           private String nome;
           private String cpf;
           private double salario;
           
           public double getBonificacao() {
               return this.salario * 0.1;
           }
       }
       ```
    * Classes e Métodos de instância precisam ser instanciados para utilização.
       ```java
       
       class Funcionario {
           String nome;
       }
       
       public class Main {
           public static void main(String[] args) {
               Funcionario messias = new Funcionario();
           }
       }
       ```
    * Classes e Métodos de classes podem ser utilizados sem serem instanciados.
       ```java
       
       class Funcionario {
           String nome;
	        static double contador;
	
	         public static double getContador() {
		          return contador;
	         }
       }
       
       public class Main {
           public static void main(String[] args) {
               Funcionario messias = new Funcionario();
           }
       }
       ```

21. Os códigos mostrados até agora não respeitam os pilares da Programação Orientada a Objetos. Descreva cada um deles e explique seus benefícios e aplicações.
    * `Abstração` O conceito de abstração consiste em esconder os detalhes de algo, no caso, os detalhes desnecessários.
    * `Encapsulamento` O conceito de encapsulamento é proteger os dados, limitando o acesso as informações por meios de classes e métodos.
    * `Herança` O conceito de herança é reaproveitar código.
    * `Polimorfismo` O conceito de polimorfismo é que classes derivadas possam invocar os métodos que apresentam a mesma assinatura, permitindo um comportamento exclusivo por classe.

22. Em Java, conseguimos aplicar a herança entre classes com a _keyword_ `extends`. Explique quais os benefícios de utilizar esse conceito no código.
    * Este conceito permite muito reaproveitamento de código, permitindo sobrescrita, sobrecarga entre outras possíveis reutilizações.

23. Explique a(s) diferença(s) entre as *keywords* `this` e `super`. No caso da `super`, ela pode ser utilizada tanto no formato `super.` quanto `super()`, porém com aplicações diferentes - explique essas duas aplicações e dê exemplos de quando utilizar cada uma.
    * `this` Utilizado para acessar informações da propria classe.
    * `super` Utilizado para acessar informações da classe pai.
    * `super()` Utilizado para invocar o construtor da classe pai.
    ``` java
    public class Pessoa {
        private String nome;
        private String documento;
        private String tipoDocumento;

        public Pessoa(String nome, String documento, String tipoDocumento) {
            this.nome = nome;
            this.documento = documento;
            this.tipoDocumento = tipoDocumento;
        }
        
        {getter and Setter}
    }
      
    public class PessoaFisica extends Pessoa{
          
          public PessoaFisica(String nome, String documento,) {
              super(nome, documento, "F");
          }
          
          public String getCPF () {
              UtilCPF utilCPF = new() UtilCPF();
              return utilCPF.formatar(super.getDocumento());
          }
      }
      ```

24. No exemplo abaixo, a classe `Cachorro` é herdada de `Mamifero`. Por que o código não compila, como seria possível ajustá-lo para que compilasse e, após ajustado, o que ele exibirá quando for executado?
    ```java
    class Mamifero {
        public void fazerSom() {
            System.out.println("...");
        }
    }
    
    class Cachorro extends Mamifero {
        public void fazerSom() {
            this.latir(); 
        }

        private void latir() {
            System.out.println("Woof woof");
        }
    }
    
    class App {
        public static void main(String... args) {
            Cachorro beethoven = new Mamifero(); 
            beethoven.fazerSom();
        }
    }
    ```
    * Cachorro é um mamifero, mas mamifero não é um cachorro.
    * Podemos resolver fazendo um cast, mas não é uma boa solução.
    * Para este cenário Mamifero seria melhor ser uma classe abstrata.
    * Para que seja impresso o `Woof woof` o código deveria ser modificado para:
    ```java
    class App {
        public static void main(String... args) {
            Mamifero beethoven = new Cachorro(); 
            beethoven.fazerSom();
        }
    }
    ```

25. Sobre construtores, qual(is) das alternativas abaixo está(ão) correta(s)?
    1. :white_check_mark:O construtor `default` do Java deixa de existir assim que algum outro é declarado;
    2. :white_square_button:O construtor `default` do Java possui como parâmetros todos os atributos da classe;
    3. :white_check_mark:É obrigatória a criação de construtores explícitos quando a classe é herdada em algum local;
    4. :white_square_button:Os construtores sempre precisam ter o modificador de acesso `public`. Caso contrário, o código não compila;
    5. :white_check_mark:O construtor `super()` precisa sempre ser chamado de forma explícita, em todos os casos de herança.

26. Qual a utilidade de classes abstratas em Java? E de métodos abstratos?
    * `classe abstrata` Quando queremos compartilhar código entre classes porem queremos indicar que o pai não pode ser criado como objeto, para tal é necessário instanciar um filho.
    * `método abstrato` Quando queremos que as classes filhos implementem o metódo abstrato sem criamos código lixo na classe pai.

27. Qual a utilidade de interfaces em Java?
    * `interfaces` São contratos preestabelecidos entre as classes que a implementam e as rotinas que a utilizam.

28. Como funciona a composição em Java?
    * Quando implementamos classes dentro de classes.
    ```java
      public class Pedido {
          private int codigo;
          private Item item;
          private FormaPagamento formaPagamento;
      }
      ```

29. Quando devemos utilizar classes abstratas (herança) e quando devemos utilizar interfaces? Qual o principal problema que o uso da segunda opção pode gerar, se não for feito da forma correta?
    * `classes abstratas (herança)` Utilizar quando queremos reutilizar código e reescrever informações.
    * `intarfaces` Utilizar quando queromos impor um contrato para execução de uma rotina.
    * Interfaces devem ser utilizadas para generalizar processos, se utilizado de forma indevida teremos problemas com criação de contratos que obrigam informar dados não utilizados.
