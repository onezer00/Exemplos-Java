# Exemplos-Java
Mostrando alguns exemplos em Java
<p align="center"><img src="https://github.com/onezer00/Exemplos-Java/blob/master/java.png"> <img /> </p>

**Aprendendo Java com exemplos práticos**

**Java - Como devo começar?**
Se nunca se deparou com Java antes, sugiro que comece lendo a documentação da própria Sun, que é a desenvolvedora da plataforma Java em [What Is the Java Platform](http://www.oracle.com/technetwork/java/index.html). Se já ouviu um pouco sobre, mas ainda não está totalmente por dentro, sugiro que leia assim mesmo a documentação. Isso te dará informações valiosas sobre os objetivos básicos da técnologia Java e como dúvidas gerais. Outra forma de começar, é ler livros como [Getting Started With Java Technology](http://www.oracle.com/technetwork/java/index.html).

Outra coisa que você precisa saber, é que Java é uma tecnologia especialmente criada para se trabalhar com programação orientada a objetos. Se nunca ouviu falar sobre isto, ou se não conhece a termologia básica de orientação a objetos, é importante se aprofundar sobre o assunto para que não surjam dúvidas básicas e que não abordaremos aqui. Uma opção é ler a [FAQ sobre OO](http://www.cyberdyne-object-sys.com/), escolha o item "Basics" para ver as termologias mais comuns. Mas não se limite a apenas os exemplos citados aqui, busque conhecimento em outras fontes e comece a fazer pesquisas sobre o assunto para se aprofundar ainda mais, pois lembre-se que, ``"Numa sociedade com base no conhecimento, por definição é necessário que você seja estudante a vida toda". - Tom Peters``.

**Java - O que preciso para começar?**

Agora que já sabemos um pouco sobre o que é a tecnologia Java, vamos nos preparar de fato. Portanto, você precisará de ferramentas, documentação e mais algumas coisinhas.
Se prepare para perder algum tempo na internet baixando as ferramentas necessárias para inciar sua jornada na plataforma Java. Abaixo algumas das ferramentas mais utilizadas para o desenvolvimento Java:

* **_Java 2 SDK, Standard Edition_** - SDK (software development kit) contém todas as ferramentas para você começar o seu desenvolvimento em Java. Você pode encontrar todas as versões e pacotes do SDK na página http://java.sun.com/jdk/, e sempre é bom você conhecer essa página e o que você pode baixar a partir dela. Para quem tem dificuldades com o inglês, ou não sabe exatamente o que baixar, vá direto para a página do SDK para Solaris ou para Windows[95/98/NT](http://java.sun.com/products/jdk/1.2/download-solaris.html). Nos dois casos, as instruções para o download são os grandes números em vermelho. Não se esqueca de seguir o link para as instruções de instalação. Se você quiser, você pode dar uma olhada também na [página de outras plataformas](http://java.sun.com/cgi-bin/java-ports.cgi). Observe que nas listas de discussão quase todo mundo trata o SDK como JDK (Java development kit), que era como o SDK era chamado até a versão anterior. [uma palavrinha sobre as versões de Java](http://www.javaman.com.br/artigos/versoesJava.html).

* **_Java 2 Standard Edition API Documentation_** - essa é a documentação completa do SDK e de todas as APIs básicas do Java. Apesar de você poder [acessar via web](http://java.sun.com/products/jdk/1.2/docs/index.html), eu recomendo que você [baixe e instale localmente](http://java.sun.com/products/jdk/1.2/download-docs.html), já que você usará isso o tempo todo.

* **_Java Tutorial_** - esse é o tutorial que você vai utilizar para aprender Java, e também pode [ser utilizado direto da web](http://java.sun.com/tutorial) o que é recomendado, já que você não precisa de tudo de uma só vez. Mas se você quiser, pode [baixa-lo também](http://java.sun.com/docs/books/tutorial/information/download.html).

* **_NetBeans_** - A fins didáticos, usaremos o NetBeans, essa é uma poderosa ferramenta de desenvolvimento, que você irá utilizar mais pra frente, depois de ter aprendido o básico. Portanto, também pode deixar para baixar depois (mas não deixe de fazê-lo!). O NetBeans é uma ferramenta da Sun, ela própria escrita em Java, e é disponibilizada gratuitamente. Pode ser baixada a partir do site http://www.netbeans.com(http://www.netbeans.com).

(Obs: O NetBeans não é a única ferramenta para desenvolvimento de aplicações em Java, existem outras ferramentas tão poderosas quanto. Mas como estamos iniciando, adotaremos o uso do NetBeans, e conforme avançarmos, cada desenvolvedor poderá optar pela ferramenta que melhor agradar.)

Depois de baixar tudo, instale o SDK, a documentação, e se você tiver baixado, o Java Tutorial. Ao instalar as ferramentas anteriores, estaremos aptos a instalar o NetBeans, mas caso ainda não esteja se sentindo preparado para colocar a mão na massa, sugiro que leia um pouco mais da documentação e tutoriais das ferramentas mais rudimentares para avançar ao próximo nível.

**Meu caro novato, te apresento o Java Tutorial!** 

Um dos modos mais bacanas para você que está começando (e mesmo para os mais experiêntes) é o [Java Tutorial](http://java.sun.com/tutorial). Nele você encontra quase tudo que precisa para aprender Java, e mais tarde, para aprender cada uma das dezenas de tecnologias envolvidas.

O Java tutorial é dividido em trails ``caminhos``, e cada um deles, vai te levar através de uma série de lições que vão cobrir diversos aspectos do assunto abordado.
Toda vez que estiver procurando por algum aspecto da tecnologia Java, o primeiro lugar em que deve olhar sempre é o Java Tutorial.

Portanto, sugiro que seu próximo passo na busca pelo conhecimento seja seguir os trails que estão na seção ``Trails Covering the Basics``. Vão ser um total de 20 a 30 pequenas lições, que vão cobrir desde os primeiros passos na criação e compilação de uma aplicação Java, conceitos básicos de orientação a objetos, as classes mais importantes de Java, e que vai chegar até a criação de aplicações e uma visão geral das funcionalidades existentes.

Lembre-se que tentaremos abordar todas essas lições e daremos alguns exemplos aqui, mas que aconselhamos procurar novos conhecimentos, principalmente na documentação do próprio fabricante.

**Mas só linhas de comando?**

Muita gente que vem do mundo de desenvolvimento visual acaba se assustando com as ferramentas básicas que fazem parte do Java Development Kit (JDK). É extremamente importante que você aprenda essas ferramentas, pois elas te obrigam a entender algumas coisas que as ferramentas visuais acabam por esconder.

Mas para o desenvolvimento em Java existem dezenas de ferramentas, e entre elas existem ferramentas tão e até mais sofisticadas do que as ferramentas existentes para outras linguagens. Portanto, aconselhamos que como parte do seu aprendizado, você conheça pelo menos uma dessas ferramentas, sugiro  que faça download do [NetBeans](http://www.netbeans.com/), que é uma ferramenta de desenvolvimento Java, visual, ela própria é escrita em Java (assim você inclusive tem uma idéia de que aplicações muito sofisticadas podem ser desenvolvidas inteiramente em Java), e é totalmente gratuita.

**Agora que temos uma noção do que é Java, e por onde começar, que tal colocarmos a mão na massa?**

**JFrame e JPanel - Criando uma aplicação gráfica em Java**

---
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

_Em nosso caso, usaremos o método mencionado com um incremento como parâmetro, veja o exemplo abaixo_:

```java
import javax.swing.JFrame;

public class framesPanels {
  public static void main(String[] args) {
    JFrame janela = new JFrame("Hello World");
    janela.setPreferredSize(new Dimensions(300, 200));
    janela.setVisible(true);
  }
}
```

Você pode consultar mais sobre as funcionalidades da classe JFrame em na [Documentação sobre JFrame](http://docs.oracle.com/javase/6/docs/api/javax/swing/JFrame.html)

---
