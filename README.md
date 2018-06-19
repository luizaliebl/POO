# QUESTIONÁRIO POO


**Construtor**

O método construtor determina que ações devem ser executadas quando da criação de um objeto. Em Java, o construtor é definido como um método cujo nome deve ser o mesmo nome da classe e sem indicação do tipo de retorno. O construtor é unicamente invocado no momento da criação do objeto através do operador new.

```java
class Cliente
{
  int codigo;
  string nome;
  
  //Construtor
  public Cliente(int cod, string nom){
    codigo = cod;
    nome = nom;
  }
}
```



**Instanciação**

A instanciação é um processo por meio do qual se realiza a cópia de um objeto (classe) existente. Uma classe, a qual tem a função de determinar um tipo de dado, deve ser instanciada para que possamos utilizá-la.


```java
public class Pessoa
  {
    public char sexo;
    public string nome;
    public int idade;
  }
public class Funcionario
  {
    static void Main()
      {
         Pessoa objPessoa = new Pessoa();
         objPessoa.sexo = 'm';
         objPessoa.nome = "Wellington";
         objPessoa.idade = 21;

         Console.WriteLine(objPessoa.nome);
      }          
   }
```



**Palavra reservada new**

Usada para instânciar um novo objeto. 

```java
Point p = new Point();
```



**Palavra reservada instanciof**

É um operador. Compara o tipo de uma variável a uma classe.

```java
class Point   { int x, y; }
class Element { int atomicNumber; }
class Test {
    public static void main(String[] args) {
        Point   p = new Point();
        Element e = new Element();
        if (e instanceof Point) {  // compile-time error
            System.out.println("I get your point!");
            p = (Point)e;  // compile-time error
        }
    }
}
```


**Encapsulamento**

É o empacotamento (encapsulamento) de variáveis e métodos, ocultando a implementação do usuário. Representa reutilização, segurança e facilidade de manutenção.



**Palavra reservada this**

Variável de referência que diz respeito a instancia atual de um objeto;

```java
class Cliente
{
  int codigo;
  string nome;
  
  //Construtor
  public Cliente(int codigo, string nome){
    this.codigo = codigo;
    this.nome = nome;
  }
}
```



**Getters/Setters**

_Getters:_ Métodos que retornam o valor de uma variável da classe. 

_Setters:_ Métodos que modificam o valor de uma variável da classe. 

```java
public class Ponto {
    private double x;
    private double y;

    public Ponto(double x, double y) {
        this.x = x;
        this.y = y;
    }
 
    public double getX() { return x; }
 
    public double getY() { return y; }
 
    public void setX(double x) { this.x = x; }
 
    public void setY(double y) { this.y = y; }
 
}
```



**Palavra reservada public/private**

_Public:_ Faz com que uma classe, método ou variável possa ser acessado a partir de qualquer outra classe.

_Private:_ Faz com que um método ou variável possa ser acessado somente de dentro da própria classe;








**Assinatura de método**

É o nome do método, sua visibilidade, retorno e parâmetros. 

```java
//Visibilidade + retorno + nome + parâmetros.
public void Ponto(double x, double y) {
    this.x = x;
    this.y = y;
}
```



**Sobrecarga de método**

Permite a existência de vários métodos de mesmo nome, porém com assinaturas levemente diferentes ou seja variando no número , tipo de argumentos , no valor de retorno e até variáveis diferentes.

```java
public void Ponto(double x, double y) {
}

public boolean Ponto(double x) {
}

public String Ponto(double x, int y) {
}
```



**Escopo de classe**

Escopo refere-se à vida e acessibilidade. Quão grande é o alcance depende de onde é declarada. Existem _quatro_:

1. Variáveis estáticas vivem pelo mesmo tempo da classe.

1. Variáveis de instância vivem pelo mesmo tempo do objeto.

1. Variáveis locais vivem pelo mesmo tempo que os seus métodos na pilha, se o método chamar outro método, estas ficam temporariamente indisponíveis.

1. As variáveis de bloco (for, if...) vivem até a conclusão do bloco.


```java
public class MinhaClasse {// início do escopo
	private int inteiro;
	boolean ativado;
} // fim do escopo
```


**Escopo de objeto**

O escopo de um objeto é sua visibilidade de outras partes do programa, o que implica não apenas quanto tempo existe a variável, como também quando foi criada e quando se tornou disponível. Um objeto definido dentro de uma função tem escopo local, e se é definido fora de qualquer função tem escopo global.

```java
public static void main(String args[]){
	Pessoa pessoa1;
	pessoa1 = new Pessoa(“Fulano”, 25, ’M’);
}
```



**Palavra reservada final**

Torna impossível estender uma classe, sobrepor um método ou reiniciar uma variável;

A palavra _final_ pode ser usada em vários lugares:

Se for utilizada numa classe, isso indica que ela não poderá ser estendida:

```java
public final class MyClass {}

// Isso não é permitido
public class MyOtherClass extends MyClass {}
```

Se utilizamos em um método, indica que o método não poderá ser sobrescrito:

```java
public class MyClass {
    public final void foo() {}
}
 
public class MyOtherClass extends MyClass {
    public void foo() {} // Não é permitido sobrescrever o método
}
```

Se a palavra for usada em uma variável, indica que tal variável será uma constante, pois não será permitido que modifique o valor dela uma vez que um valor seja atribuído:

```java
public class MyClass {
 
    public void foo() {
        final int teste = 0;
        teste++; // Não é permitido
    }
}
```



**Relacionamento de dependência**

Classe A não consegue ser executado e compilada sem a Classe B. Uma classe utiliza o serviço de outra. Método da Classe. UML símbolo = seta tracejada



**Relacinamento de Agregação**

Parte existe sem o todo. Aluno pode existir sem uma disciplina Relação Todo-Parte. Atributo da Classe. UML símbolo = linha com losango na ponta.




**Relacionamento de Composição**

Parte não existe sem o todo. Ser vivo não pode existir sem o coração. Relação Todo-Parte. Atributo da Classe. UML símbolo = linha com losango preto na ponta.


