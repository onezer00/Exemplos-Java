# Exemplos-Java
Mostrando alguns exemplos em Java
<p align="center"><img src="https://github.com/onezer00/Exemplos-Java/blob/master/java.png"> <img /> </p>

**Aprendendo Java com exemplos práticos**

Neste repositório, você encontrará exemplos práticos em Java para ajudá-lo a aprender e entender os conceitos básicos da linguagem. Vamos começar com alguns exemplos simples.

## Como começar com Java?

### Instalação do Java

Para começar a programar em Java, você precisa do Kit de Desenvolvimento Java (JDK). Você pode baixar o JDK mais recente no site oficial da Oracle ou usar uma distribuição OpenJDK. Siga as instruções de instalação para o seu sistema operacional.

### Configuração do ambiente de desenvolvimento

Você pode usar uma variedade de IDEs (Ambiente de Desenvolvimento Integrado) para programar em Java. Algumas opções populares incluem:

- [IntelliJ IDEA](https://www.jetbrains.com/idea/) (Comunidade ou Ultimate Edition)
- [Eclipse](https://www.eclipse.org/)
- [NetBeans](https://netbeans.apache.org/)

Escolha a que melhor se adapta às suas necessidades e instale-a. Ela facilitará o desenvolvimento de aplicativos Java.
***
**Agora que temos uma noção do que é Java, e por onde começar, que tal colocarmos a mão na massa?**

---
**JFrame e JPanel - Criando uma aplicação gráfica em Java**

**_JFrame: Criando janelas em java_**

JFrame é uma classe como outra qualquer, ela é responsável por criar a tela em que iremos desenhar, colocar os botões, menus, caixas de texto e tudo mais que existem nas janelas de aplicativos.

Para fazer uso do JFrame, temos que importar essa classe do pacote swing, que contém diversas funcionalidades para programação gráfica:

Fazemos isso digitando: ``import.javax.swing.JFrame;`` No início de nosso código.

Cada objeto que criamos é um frame, ou janela, diferente. Um único programa criado pode conter dezenas ou centenas de frames.

Nessa seção iremos criar alguns objetos da classe JFrame passando uma String como argumento para o construtor padrão, essa string será o título de nossa aplicação.

Esses JFrames, possuem dezenas de funcionalidades e opçes, iremos usar as funcionalidades: O que ocorre quando clicamos no `x` de close, adicionar panels, definir o tamanho do frame e se ele será visível ou não, são exemplos disso.

Como disse, o JFrame é uma Classe. E para criar uma classe que pode ser definida como um objeto.
Assim, nossa janela será um objeto chamado "janela".
Vamos passar a string para o construtor dessa classe, que servirá como título de nosso "frame/janela".

Porém, para ver o frame que acabamos de criar, precisaremos definir uma funcionalidade "Que ele seja visível!".
Pode parecer óbvio, mas um programa pode ter muitos frames, e obviamente não podemos exibir todos, senão nossa tela ficaria uma bagunça.

Assim, para exibir o frame que acabamos de criar, usaremos o método setVisible, que recebe ``true ou false``.
Portanto, um simples prgorama em Java que cria e exibe um frame ficará da seguinte forma:

```java
import javax.swing.JFrame;

public class framesPanels {
  public static void main(String[] args) {
    JFrame janela = new JFrame ("Hello World");
    janela.setVisible(true);
  }
}
```
Note que com o exemplo acima, teremos criado uma janela que provavelmente nem será notada. Isso porque não fornecemos o tamanho da janela, então ela foi criada com 0 px de largura e 0 px de altura.

Vamos usar o método ``SetVisible``, que recebe um tipo _boolean_. Como o que queremos é que a janela fique visível, colocamos _true_.

Caso queira definir um tamanho pré-definido, use o método ``setSize()``, que recebe dois parâmetros com os pixels da janela (horizontal e vertical):

_Em nosso caso, usaremos o método mencionado ``setSize`` para definir o tamanho de nossa janela, veja o exemplo abaixo_:

```java
import javax.swing.JFrame;

public class framesPanels {
  public static void main(String[] args) {
    JFrame janela = new JFrame("Hello World");
    janela.setSize(300, 200);
    janela.setVisible(true);
  }
}
```

Você pode consultar mais sobre as funcionalidades da classe JFrame na [Documentação sobre JFrame](http://docs.oracle.com/javase/6/docs/api/javax/swing/JFrame.html)

**_JPanel: Inserindo elementos em um JFrame_**

Como vimos, nosso frame está vazio. Apenas definimos o tamanho da 'moldura' e o título.
Vamos adicionar alguns elementos ao nosso frame, e faremos isso inserindo um JPanel, onde nele podemos colocar uma infinidade de elementos, chamados JComponents:



Para usar o JPanel, importamos essa classe da package swing, usando ``import.javax.swing.JPanel;``.

Vamos criar uma classe que será nosso painel, vamos chamar de "Painel".
Para isso, basta fazer com que ela **_Extends_** a _JPanel_, como aprendemos em [Herança](https://github.com/onezer00/Exemplos-Java/blob/master/HERAN%C3%87A.MD), para herdarmos todas as propriedades do JPanel.

```java
import javax.swing.JPanel;

public class Painel extends JPanel {

}
```
Na nossa classe principal, vamos criar um objeto do tipo "Painel" e chamar de "meuPainel".
Adicionaremos nosso JPanel em nosso JFrame, usando o método **_add_** que recebe como argumento um JPanel:

```java
Painel meuPainel = new Painel();
janela.add(meuPainel);
```
Embora tenhamos adicionado o Panel ao nosso Frame, ainda não conseguiremos visualiza-lo quando executarmos, pois não adicionamos nenhum elemento ao Panel.

Para dar um exemplo bacana, criaremos o seguinte código com base no que aprendemos até agora, para termos uma idéia do que vem pela frente:

<p align="center"><img src="https://github.com/onezer00/Exemplos-Java/blob/master/primeiro%20frame%20java.png"> <img /> </p>

**_FramesPanels.java_**
```java
//Esta é a classe java que criará nosso Frame
import javax.swing.JFrame;

public class framesPanels {

  public static void main(String[] args) {
    JFrame janela = new JFrame("Meu primeiro Frame");
    Painel meuPainel = new Painel();

    janela.setDefaultCloseOperation( JFrame.EXIT_ON_CLOSE );
    janela.add(meuPainel);
    janela.setSize(600, 400);
    janela.setVisible(true);
  }
}
```
**_Painel.java_**
```java
import java.awt.Graphics;
import javax.swing.JPanel;

public class Painel extends JPanel{
	public void paintComponent( Graphics g ){
	    super.paintComponent( g );
	    int pixel=0;
	    
	    for(pixel=0 ; pixel <= getHeight() ; pixel += 10){
	        g.drawLine(0, pixel, pixel, getHeight());
	        }

	    for(pixel=getHeight() ; pixel >=0 ; pixel -= 10){
	        g.drawLine(0, pixel, getHeight() - pixel, 0);
	    }
	    
	    for(pixel=0 ; pixel <= getHeight() ; pixel +=10){
	        g.drawLine(getWidth(), pixel, getWidth() - pixel, getHeight());
	    }
	    
	    for(pixel=getHeight() ; pixel >=0 ; pixel -= 10){
	        g.drawLine(getWidth(), pixel, getWidth() - (getHeight() - pixel), 0);
	    }
	    
	}
}
```
Para Mais detalhes sobre os métodos e outras funcionalidades do JPanel, você pode acessar a [Documentação do JPanel](http://docs.oracle.com/javase/1.4.2/docs/api/javax/swing/JPanel.html)

A partir daqui, veremos exemplos práticos usados no dia a dia. E para não se tornar um arquivo muito grande criaremos um arquivo para listar [todos os nossos exemplos](https://github.com/onezer00/Exemplos-Java/blob/master/Exemplos.MD)

[Clique aqui para ir para a página de exemplos](https://github.com/onezer00/Exemplos-Java/blob/master/Exemplos.MD)

---
