# Exemplos-Java
Mostrando alguns exemplos em Java
<p align="center"><img src="https://github.com/onezer00/Exemplos-Java/blob/master/java.png"> <img /> </p>

**Aprendendo Java com exemplos práticos**
---
**Herança**

Este é um mecanismo da Orientação a Objetos que nos permite criar novas classes a partir de classes já existentes, aproveitando-se das caractersticas na classe a ser estendida atravs do ``extends``. Este é um mecanismo muito interessante, pois promove um grande reuso e reaproveitamento de códigos existentes. Com herança podemos criar classes derivadas e subclasses, a partir de classes bases, também conhecidas como superclasses. As subclasses são mais especializadas do que as suas superclasses, que tendem a ser mais genéricas. Pois as subclasses herdam todas as caractersticas de suas superclasses, com suas variáveis e métodos. A linguagem Java permite o uso de herança simples, mas não nos permite a implementação de herança múltipla. Para superar essa limitação, o Java faz o uso de interfaces, o qual pode ser visto com uma "promessa" que certos métodos com caractersticas previamente estabelecidas serão implementados, usando inclusive a palavra reservada ``implements`` para garantir esta implementação. As interfaces possuem sintaxes similares as classes, no entanto apresentam apenas a especificação das funcionalidades que uma classe deve conter, sem determinar como essa funcionalidade deve ser implementada. Apresentam apenas protótipos dos métodos.

Por exemplo, Imagine que dentro da organização de sua empresa, o sistema de RH tenha que trabalhar com os diferentes níveis de hierarquia, desde o funcionamento de baixo escalão até o presidente. Todos sãof uncionários da empresa, porém cada um com um cargo diferente. Mesmo a secretária, o pessoal da limpeza, o diretor e o presidente possuem um número de identificação, além de salário e outras características em comum. Essas características em comum podem ser resumidas em um tipo de classe em comum, e cada nível de hierarquia ser tratado como um novo tipo, mas aproveitando-se dos tipos já criados, atravs da herança. Os subtipos, além de herdarem todas as características de seus supertipos, também podem adicionar mais características, seja na forma de variáveis e/ou métodos adicionais, bem como reescrever métodos já existentes na superclasse, o que chamamos de polimorfismo (Abordaremos em outro documento). A herança permite vários níveis na hierarquia de classes, podendo criar tantos subtipos quanto necessário, até se chegar ao nível de especialização desejado. Podemos tratar subtipos como se fossem seus supertipos, por exemplo, o sistema de RH pode tratar uma instância de Presidente como se fosse um objeto do tipo Funcionário, em determinada funcionalidade. Porém não é possível tratar um supertipo como se fosse um subtipo, a não ser que o objeto em questão seja realmente do subtipo desejado e a linguagem suporte este tipo de tratamento, seja por meio de conversão de tipos ou outro mecanismo. Algumas linguagens de programação permitem herança múltipla, ou seja, uma classe pode estender características de várias classes ao mesmo tempo. É o caso do C++. Outras linguagens não permitem herança múltipla, por se tratar de algo perigo se não usada corretamente. É o caso do Java. Na Orientação a Objetos as palavras classe base, supertipo, superclasse, classe pai e classe mãe são sinônimos, bem como as palavras classe derivada, subtipo, subclasse e classe filha também são sinônimos.

O que um aluno, um professor e um funcionário possuem em comum? Todos eles são pessoas e, portanto, compartilham alguns dados comuns. Todos têm nome, idade, endereço, etc. E, o que diferencia um aluno de outra pessoa qualquer? Um aluno possui uma matrícula; Um funcionário possui um código de funcionário, data de admissão, salário, etc.; Um professor possui um código de professor e informações relacionadas à sua formação. 

É aqui que a herança se torna uma ferramenta de grande utilidade. Podemos criar uma classe Pessoa, que possui todos os atributos e métodos comuns a todas as pessoas e herdar estes atributos e métodos em classes mais específicas, ou seja, a herança parte do geral para o mais específico. Vamos começar criando uma classe Pessoa, Pessoa.java, como mostrado no código a abaixo:

```java
public class Pessoa{
	public String nome;   
	public int idade;
}
```
Esta classe possui os atributos nome e idade. Estes atributos são comuns a todas as pessoas.
Veja agora como podemos criar uma classe Aluno que herda estes atributos da classe Pessoa, e incluir seu próprio atributo, a saber, seu número de matrícula.

_Eis o código:_

```java
public class Aluno extends Pessoa{
  public String matricula;
}
```
Observe que, em Java, a palavra-chave usada para dizer que estamos herdando  ``extends``. A classe Aluno agora possui trs atributos: ``nome, idade e matricula``.

_Exemplo:_
```java
public class Estudos {
  public static void main(Strings args[]) {
    Aluno aluno = new Aluno();
    aluno.nome = "Exemplo de Aluno";
    aluno.idade = 19;
    aluno.matricula = "XXXZZZX58829";
    
    System.out.println("Nome: " + aluno.nome + "\n" + "Idade: " + aluno.idade + "\n" + "Matricula: " + aluno.matricula);
  }
}
```
A herança nos fornece um grande benefício. Ao concentrarmos características que são comuns em uma classe e derivar as classes mais específicas a partir desta, ns estamos preparados para a adição de novas funcionalidades ao sistema. Se mais adiante uma nova propriedade comum tiver que ser adicionada, não precisaremos efetuar alteraçes em todas as classes. Basta alterar a superclasse e pronto. As classes derivadas serãoa automaticamente atualizadas.

_Veja o exemplo abaixo:_
```java
public abstract class Animal {
	public abstract void fazerBarulho();
}

public class Cachorro extends Animal {
	public void fazerBarulho() {
		System.out.println("AuAu!");
	}
}

public class Gato extends Animal {
	public void fazerBarulho() {
		System.out.println("Miau!");
	}
}

class Veiculo {
	public Veiculo() {
		System.out.print("Veiculo ");
	}
	
	public void checkList() {
		System.out.println("Veiculo.checkList");
	}
	
	public void adjust() {
		System.out.println("Veiculo.adjust");
	}
	
	public void cleanup() {
		System.out.println("Veiculo.cleanup");
	}
}
class Automovel extends Veiculo {
	public Automovel() {
		System.out.println("Automovel");
	}
	
	public void checkList() {
		System.out.println("Automovel.checkList");
	}
	
	public void adjust() {
		System.out.println("Automovel.adjust");
	}
	
	public void cleanup() {
		System.out.println("Automovel.cleanup");
	}
}   

class Bicicleta extends Veiculo {
	public Bicicleta() {
		System.out.println("Bicicleta");
	}
	
	public void checkList() {
		System.out.println("Bicicleta.checkList");
	}
	
	public void adjust() {
		System.out.println("Bicicleta.adjust");
	}
	
	public void cleanup() {
		System.out.println("Bicicleta.cleanup");
	}
}
```
