# QUESTIONÁRIO POO

* Construtor

R: O método construtor determina que ações devem ser executadas quando da criação de um objeto. Em Java, o construtor é definido como um método cujo nome deve ser o mesmo nome da classe e sem indicação do tipo de retorno. O construtor é unicamente invocado no momento da criação do objeto através do operador new.

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


* Instanciação

R: A instanciação é um processo por meio do qual se realiza a cópia de um objeto (classe) existente. Uma classe, a qual tem a função de determinar um tipo de dado, deve ser instanciada para que possamos utilizá-la.


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


* Palavra reservada new

R: Usada para instânciar um novo objeto. 

```java
Point p = new Point();
```


* Palavra reservada instanciof

R: É um operador. Compara o tipo de uma variável a uma classe.

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


* Encapsulamento

R: É o empacotamento (encapsulamento) de variáveis e métodos, ocultando a implementação do usuário. Representa reutilização, segurança e facilidade de manutenção.


* Palavra reservada this

R: Variável de referência que diz respeito a instancia atual de um objeto;

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


* Getters/Setters

R:

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

* Palavra reservada public/private

R: Public: Faz com que uma classe, método ou variável possa ser acessado a partir de qualquer outra classe.
Private: Faz com que um método ou variável possa ser acessado somente de dentro da própria classe;

* Assinatura de método

R:

* Sobrecarga de método

R:

* Escopo de classe

R:

* Escopo de objeto

R:

* Palavra reservada final

R: torna impossível estender uma classe, sobrepor um método ou reiniciar uma variável;

* Relacionamento de dependência

R:

* Relacinamento de Agregação

R:

* Relacionamento de Composição

R:


```java
codigo java
```

**negrito**

_italico teste_
