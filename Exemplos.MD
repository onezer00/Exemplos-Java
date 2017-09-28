# Exemplos-Java
Mostrando alguns exemplos em Java
<p align="center"><img src="https://github.com/onezer00/Exemplos-Java/blob/master/java.png"> <img /> </p>

**Aprendendo Java com exemplos práticos**
---
Aqui apresentaremos alguns modelos conceituais e práticos da tecnologia Java para desenvolvimento de programas orientados a objetos, ou seja, POO(Programação orientada a objetos), que já falamos por aqui.

Para começar, descreveremos e daremos alguns exemplos sobre como funciona uma linguagem Orientada a Objetos.
Aqui trabalharemos com classes abstratas, que nada mais é do que uma estrutura que abstrai um conjunto de objetos com métodos e os estados possíveis deste objeto atravs de atributos. Em outros termos uma classe descreve básicamente os serviços providos por seus objetos e quais informaçes eles podem armazenar. Classes não são diretamente suportadas em todas as linguagens, e são necessárias para que uma linguagem seja orientada a objetos. A programação orientada a objetos tem três pilares:

* [**ENCAPSULAMENTO**]()
* [**HERANÇA**](https://github.com/onezer00/Exemplos-Java/blob/master/HERAN%C3%87A.MD)
* [**POLIMORFISMO**]()

**Agora que sabemos um pouco sobre o assunto, vamos ver alguns exemplos práticos:**

---

**Formatação de texto - Bold, Italic e Italic+Bold**
---
Em nosso primeiro exemplo, criaremos uma janela com 3 ``JRadioButton`` que irá alterar nosso texto conforme nossa seleção ``BOLD, ITALIC e BOLD + ITALIC``.

_Ficará como o exemplo abaixo:_
<p align="center"><img src="https://github.com/onezer00/Exemplos-Java/blob/master/exemploRadioButton.png"> <img /> </p>

Aqui está nosso código para o exemplo acima: [Exemplo JRadioButton - Git](https://github.com/onezer00/Exemplos-Java/blob/master/JRadioButton)

---
**Formataço de texto - Fontes**
---
Já que estamos falando de formatação de texto, iremos nos aprofundar um pouco mais, vendo um exemplo de como ter acesso a lista de fontes. Para isso utilizaremos o método ``GraphicsEnvironment.getLocalGraphicsEnvironment().getAvailableFontFamilyNames();``, e criaremos um laço para percorrer a todas as fontes disponíveis.

_Deverá ficar como no exemplo:_
<p align="center"><img src="https://github.com/onezer00/Exemplos-Java/blob/master/fontlist.png"> <img /> </p>

Veja o código do nosso exemplo: [Exemplo Font - Git](https://github.com/onezer00/Exemplos-Java/blob/master/Font)

---
**Bordas**
---
Aqui veremos dois exemplos de bordas, primeiro vamos ver como estilizar nossos trabalhos com vários tipos de bordas simples, coloridas e em diversos formatos. Que poderemos utilizar em no dia a dia, em várias ocasiões:

_Segue o primeiro exemplo:_
<p align="center"><img src="https://github.com/onezer00/Exemplos-Java/blob/master/Bordas.png"> <img /> </p>

Veja o código de nosso primeiro exemplo sobre bordas: [Exemplo Bordas](https://github.com/onezer00/Exemplos-Java/blob/master/Bordas)

Em nosso segundo exemplo, veremos como aplicar o efeito de bordas em um JButton, e ainda como estilizar combinando vários efeitos ao mesmo botão.

_Veja no segundo exemplo:_
<p align="center"><img src="https://github.com/onezer00/Exemplos-Java/blob/master/bordasButtons.png"> <img /> </p>

Aqui o código de nosso segundo exemplo sobre bordas coloridas em um JButton: [Exemplo de bordas coloridas](https://github.com/onezer00/Exemplos-Java/blob/master/Bordas%20Coloridas)

---
**Cores**
---
Podemos definir e manipular as cores em Java através da classe ``Color``. Esta classe encapsula as cores do sistema RGB (Red, Green and Blue).
O sistema RGB pode ser entendido como objetos que emitem luz, como monitores, televisão ou o sol, sobrepondo ou somando os comprimentos de onda.
A escala de cor varia de 0 até 255, sendo que 0 o canhão está desligado e com 255 ligado no máximo. Quando temos os três canhões desligados, teremos o preto, que indica ausência de luz, enquanto que quando ligamos todos os canhões no máximo, teremos o branco.

**Cores de Fontes:**
Para definirmos as cores das fontes componentes, basta definir a propriedade do ``Foreground`` com a cor desejada. É possível utilizar cores predefinidas ou definir na hora.

_Veja no exemplo:_
```java
JLabel6.setForeground(Color.blue);
Color vermelhoEscuro = new Color(235, 50, 50);
JLabel5.setForeground(vermelhoEscuro);
```

**Cores de Fontes:**
Para definirmos as cores de fundo, utilizamos a propriedade ``Background``. O detalhe é que esta propriedade só funciona para componentes que sejam opacos. Então, é necessário definir opacidade como verdadeiro.

_Veja no exemplo:_
```java
JLabel7.setOpaque(true);
JLabel7.setBackground(Color.green);
```

_Para ilustrar nosso trabalho, faremos o exemplo a seguir:_
<p align="center"><img src="https://github.com/onezer00/Exemplos-Java/blob/master/Cores.png"> <img /> </p>

Segue nosso código para o exemplo: [Exemplo Color - Git](https://github.com/onezer00/Exemplos-Java/blob/master/Color)

---
**Tratamento de Eventos em Java**
---
Quase todos os componentes propagam eventos. Estes eventos devem ser tratados em algum ponto do código da aplicação. Os eventos nunca são tratados no próprio componente.
Para ligar o código de tratamento de eventos ao componente existem, no Java, um conjunto de interfaces chamadas listeners. Um listener é uma interface que especifica os métodos que uma aplicação deve ter para ser notificada da concorrência de um determinado evento. Os componentes que geram eventos permitem que sejam adicionados ou removidos listeners em qualquer altura.

**Funcionamento do tratamento de eventos**
---
* O componente que produz eventos possui métodos especiais do tipo addXXListener(XXListener) que permite adicionar ou remover listeners. Onde XX representa o nome do evento.
O método addXXListener recebe por parâmetro o objeto que implementa a interface XXListener.

* A implementação do método addXXListener no componente apenas adiciona o objeto passado por um parâmetro a uma lista interna. Sempre que ocorrer um evento (ex. botão pressionado), o componente percorre a lista e invoca, para cada elemento, o método definido na interface XXListener.

**Eventos prontos**

|Ação do Usuário 			              | Evento disparado | Listener       |
|-----------------------------------------------------|------------------|----------------|
|Clicar em um boão - JButton 		              | ActionEvent      | ActionListener |
|Abrir, minimizar ou fechar uma janela - JFrame       | WindowEvent      | WindowListener |
|Clicar em um componente - JComponent                 | Mouse Event      | MouseListener  |
|Alteração de texto em um campo de texto - JTextField | TextEvent        | TextListener   |
|Digitar uma tecla 				      | KeyEvent         | KeyListener    |
|Clicar em um item de escolha - Checkbox              | ItemEvent        | ItemListener   |

Inicialmente, falaremos apenas sobre o ``ActionListener``. Mas você pode testar os outros "Listeners" seguindo o exemplo de implementação do método ``ActionListener``.

**Vamos implementar**

* Vamos implementar um programa simples para incrementar um texto a um ``JTextBox``. Quando apertamos o botão "Clique-me", irá aparecer o texto "Botão foi clicado", apertar em "Limpar", o texto será retirado.
* Para isso, precisaremos de um JFrame, dentro dele teremos dois JButton e um JTextBox.

<p align="center"><img src="https://github.com/onezer00/Exemplos-Java/blob/master/actionListener.png"> <img />

Aqui está o código de nosso exemplo: [Exemplo Listener - Git](https://github.com/onezer00/Exemplos-Java/blob/master/Listener)
