# Introdução ao TypeScript

## Veremos o TypeScript, um superset da linguagem JavaScript criado pela Microsoft para permitir a escrita de scripts com a utilização de tipagem estática, orientação a objetos, e facilitando a escrita de código com uma sintaxe de fácil compreensão

- https://www.devmedia.com.br/revista-net-magazine-128/36726)

Por que eu devo ler este artigo:Nos últimos anos, o JavaScript teve seu alcance expandido para além do front-end web e hoje pode ser utilizado no desenvolvimento de outros tipos de projetos, como mobile, IoT e no ¬back-end de aplicações.

Suporte ao alunoAnotarMarcar como concluídoCódigo fonte

[Artigos](https://www.devmedia.com.br/artigos/)[.NET](https://www.devmedia.com.br/artigos/dotnet)Introdução ao TypeScript

**A linguagem TypeScript surge como um superset do JavaScript, adicionando a este funcionalidades que nativamente não estão disponíveis ou requerem grande esforço para utilização, como tipagem de dados e Orientação a Objetos**. Conhecer essa nova opção de desenvolvimento é útil para aqueles que utilizam JavaScript intensamente em seus projetos e desejam construir códigos com melhor [arquitetura](https://www.devmedia.com.br/guias/arquitetura), aplicando padrões de projeto e práticas comumente encontradas em outras linguagens [orientadas a objetos](https://www.devmedia.com.br/os-4-pilares-da-programacao-orientada-a-objetos/9264).

------

##### Guia do artigo:

- [O que é o TypeScript?](https://www.devmedia.com.br/introducao-ao-typescript/36729#TypeScript)
- [ECMAScript 6](https://www.devmedia.com.br/introducao-ao-typescript/36729#ECMAScript)
- [Orientação a Objetos](https://www.devmedia.com.br/introducao-ao-typescript/36729#OO)
- [Encapsulamento](https://www.devmedia.com.br/introducao-ao-typescript/36729#Encapsulamento)
- [Herança](https://www.devmedia.com.br/introducao-ao-typescript/36729#Heranca)
- [Abstração](https://www.devmedia.com.br/introducao-ao-typescript/36729#Abstracao)
- [Polimorfismo](https://www.devmedia.com.br/introducao-ao-typescript/36729#Polimorfismo)
- [Trabalhando com o TypeScript](https://www.devmedia.com.br/introducao-ao-typescript/36729#anchor)
- [Tipos de dado: Any](https://www.devmedia.com.br/introducao-ao-typescript/36729#Any)
- [Let, Var e Const](https://www.devmedia.com.br/introducao-ao-typescript/36729#Let)
- [Generics](https://www.devmedia.com.br/introducao-ao-typescript/36729#Generics)
- [Modules](https://www.devmedia.com.br/introducao-ao-typescript/36729#Modules)
- [Interfaces](https://www.devmedia.com.br/introducao-ao-typescript/36729#Interfaces)
- [TypeScript Playground](https://www.devmedia.com.br/introducao-ao-typescript/36729#Playground)
- [Cross-browser](https://www.devmedia.com.br/introducao-ao-typescript/36729#browser)
- [TypeScript no Visual Studio](https://www.devmedia.com.br/introducao-ao-typescript/36729#Studio)
- [Utilizando tipagem estática](https://www.devmedia.com.br/introducao-ao-typescript/36729#tipagem)
- [TypeScript com AngularJS](https://www.devmedia.com.br/introducao-ao-typescript/36729#Projeto)
- [Criando a Interface](https://www.devmedia.com.br/introducao-ao-typescript/36729#Interface)

------

Ao longo da nossa trajetória como desenvolvedores de sistemas web, nos deparamos com a necessidade de utilizarmos a linguagem de programação JavaScript em várias das nossas aplicações. Considerada uma das linguagens mais populares do mercado, ela ainda não possui, mesmo com tanto tempo no mercado, alguns recursos e características normalmente necessárias no [desenvolvimento de software](https://www.devmedia.com.br/atividades-basicas-ao-processo-de-desenvolvimento-de-software/5413) de grande escala.

Diferentemente do que ocorria alguns anos atrás, onde JavaScript era utilizada apenas no lado cliente das aplicações, atuando na validação de formulários e composição de elementos da interface, atualmente temos iniciativas que levam essa linguagem a representar a parte principal de aplicações mobile (em frameworks de desenvolvimento híbrido como Apache Cordova) e web (no lado servidor com Node.js). Nestes cenários, os projetos não se resumem mais a pequenos arquivos com algumas linhas de código, muitas vezes apenas utilizando outros frameworks front-end. Agora, passa a ser necessária a possibilidade de construir arquiteturas mais sólidas, onde se possa organizar adequadamente o código e aplicar as melhores práticas e técnicas de programação, como a Orientação a Objetos e, dentro desta, o uso de interfaces.

### O que é o TypeScript?

**Criada pela Microsoft, TypeScript está provando ser uma escolha comum entre os desenvolvedores ASP.NET**. Não se trata, na verdade, de uma linguagem completamente nova, mas sim um superset (ou superconjunto) do JavaScript.

<iframe width="560" height="315" src="https://www.youtube.com/embed/b9LfsL_-E3k" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen="" style="outline: none; -webkit-tap-highlight-color: transparent; max-width: 100%; margin: auto; height: 455.062px; width: 809px;"></iframe>

Saiba mais: [O que é TypeScript?](https://www.devmedia.com.br/curso/o-que-e-typescript/1920)

Com **TypeScript** dispomos de recursos que melhor suportam o uso da Programação Orientada a Objetos, que tem como base quatro princípios fundamentais: encapsulamento, herança, abstração e polimorfismo, os quais veremos de forma mais detalhada a seguir. A POO sempre foi um problema ao ser aplicada em JavaScript, devido a sua sintaxe não permitir escrever classes, por exemplo, de forma tão clara, além da fraca tipagem de dados. **O TypeScript oferece então uma forma de corrigir ou contornar esses problemas**, adicionando funcionalidades que quando compiladas resultarão em código JavaScript novamente. Porém, agora o desenvolvedor lidará diretamente com uma sintaxe simplificada, mais clara e amplamente suportada por editores de código modernos.

O TypeScript, que no momento da publicação deste artigo encontrava-se em sua versão 1.8, teve como seu principal desenvolvedor o mesmo criador da linguagem C#, Anders Hejlsberg, e sua equipe na Microsoft. Visando aproveitar o máximo da linguagem e contar com a adesão e colaboração da comunidade técnica, o projeto é open source e baseia-se nos padrões ES6 (ECMAScript), que podem ser compilados para JavaScript.

Por ser um superconjunto do JavaScript, qualquer código dessa linguagem pode ser colocado em um arquivo **TypeScript**, que possui a sua extensão .ts, e utilizado diretamente. Este é um ponto bastante positivo, pois podemos utilizar códigos JavaScript já existentes, sem a necessidade de realizarmos grandes conversões. Uma vez que tenhamos um arquivo TypeScript salvo, podemos compilá-lo para JavaScript utilizando a ferramenta de compilação tsc.exe, ou mesmo utilizando task runners (**BOX 1**) como o Grunt ou mesmo o Gulp.

**BOX 1**: Task Runner

Muitas vezes, durante o desenvolvimento de softwares, é preciso executar tarefas que se repetem com certa frequência, como concatenação, minificação de arquivos, e testes. Os Task Runners são ferramentas utilizadas para automatizar esse tipo de tarefa. O Grunt e o Gulp são exemplos desse tipo de ferramenta para JavaScript, havendo vários no mercado para outras linguagens que, baseados em arquivos de configuração onde as tarefas são definidas, as executam em determinado momento durante o desenvolvimento, como no build da aplicação.

### ECMAScript 6

ECMAScript é uma especificação de linguagens de script com marca registrada padronizada pela Ecma International nos padrões ECMA-262 e ISO/IEC 16262. Algumas das implementações que conhecemos desta padronização estão no JavaScript, JScript e também no ActionScript, os quais são bastante utilizados em aplicações web no client-side. Com a evolução da Web e o alto uso de scripts, novas metas foram definidas pelo ECMAScript 2015 (também chamado ES6), as quais incluem o fornecimento de um melhor suporte para grandes aplicações, criação de bibliotecas, além do uso de ECMAScript em outras linguagens. Algumas de suas principais melhorias incluem módulos, declarações de classe, promises para programação assíncrona, dentre outras. A biblioteca do ECMAScript foi expandida para suportar abstrações de dados adicionais, incluindo mapas, conjuntos e matrizes de valores numéricos, bem como suporte adicional para caracteres Unicode em strings e expressões regulares.

Baseado nas especificações do ES 6, o TypeScript é capaz de oferecer recursos como interfaces e generics, características já presentes em outras linguagens de programação orientadas a objetos, como C# e Java.

### Princípios básicos da Orientação a Objetos

Para que possamos compreender melhor as diferenças de escrita de código entre TypeScript e JavaScript “puro”, é importante que tenhamos conhecimento dos princípios básicos do paradigma da Orientação a Objetos. A seguir, veremos o conceito e exemplos de como aplicar cada princípio em TypeScript.

### Encapsulamento

O conceito de encapsulamento define uma forma de estruturar o código para que um determinado bloco tenha pontos de acesso específicos para o ambiente externo, o que garante a visibilidade e acessibilidade controladas dos elementos internos da classe.

Por meio do encapsulamento pode-se definir quais atributos da classe serão visíveis para utilizadores externos, e a forma como serão expostos ao uso por meio da interface pública do componente. No .NET Framework, por exemplo, quem trabalha com C# está acostumado a declarar atributos privados nas classes e suas respectivas propriedades públicas que os encapsulam. O exemplo a seguir mostra o equivalente a essa prática em TypeScript:

```
private _saldo: number;
get Saldo(): number { return this._saldo; }
```

Observe que já neste trecho podemos ver a tipagem de dados e modificadores de acesso.

### Herança

Segundo o princípio da herança, uma classe (filha) pode herdar de outra (pai) características e comportamentos já definidas nessa segunda, sem necessidade de redefinição. A sintaxe em TypeScript para implementar esse conceito é semelhante à da linguagem Java, onde se usa a palavra reservada extends após o nome da classe filha, seguida do nome da classe pai, como podemos ver na **Listagem 1**.

```
module Banco {
  class Conta { ...código aqui.. }
  class ContaCorrente extends Conta { ...código aqui.. }
  class Poupanca extends Conta { ...código aqui.. }
}
```

**Listagem 1**. Utilização de herança no TypeScript

Diferente do JavaScript tradicional, que normalmente é extenso e as classes definidas por meio da palavra reservada function, temos um código muito mais simples e compreensível quando utilizamos o TypeScript. Aqui podemos perceber de forma clara a utilização da herança. Para nós é mais fácil escrever códigos com o TypeScript e deixar que ele se encarregue de gerar o código JavaScript que nos custaria mais tempo para escrita e compreensão posterior.

### Abstração

No contexto da Orientação a Objetos, a abstração é a capacidade de destacar as características dos elementos do mundo real que serão úteis para o sistema. Essas características são reunidas na forma de classes, que representam as “coisas” reais a serem utilizadas no domínio do problema.

Dentro do conceito de classes, temos ainda as classes abstratas, que até a versão 1.8 do TypeScript, utilizada neste artigo, ainda eram suportadas diretamente, no entanto, podemos utilizar interfaces para implementar esse princípio, como podemos ver na **Listagem 2**.

```
export module BancoDevmedia
{
   export interface Taxa { MudarTaxa(valor: number); }
   export class ContaCorrente implements Taxa {
       MudarTaxa(valor: number) { }
   }
}
```

**Listagem 2**. Abstração com TypeScript por meio de interfaces

### Polimorfismo

Polimorfismo é um conceito a partir do qual objetos podem assumir formas diferentes em determinadas situações, mas mantendo uma relação com sua definição inicial de nível mais alto. Aliado ao conceito de herança, o polimorfismo indica que um objeto do tipo de uma classe pai pode assumir a forma de qualquer uma de suas classes filhas, mas não o inverso.

O Typescript permite a utilização de polimorfismo através de métodos, como mostra a **Listagem 3**, onde podemos realizar operações bancárias em classes derivadas de uma classe base. O método TrocarTaxa foi originalmente definido na classe Conta, no entanto, foi sobrescrito na classe filha ContaCorrente para apresentar um comportamento específico quando acionado.

```
class ContaCorrente extends Conta
{
   TrocaTaxa(valor: number)
   {
       if (this.Saldo > 50000) { valor = 0; }
       else { valor += 10.00; }
       this.Saldo =+ valor;
   }
}
```

**Listagem 3**. Utilizando o Polimorfismo

Após essa pequena abordagem sobre a Orientação a Objetos, passaremos a ver as características básicas do TypeScript.

### Trabalhando com o TypeScript

Assim como nas demais linguagens de programação, os tipos básicos de dados encontram-se também no TypeScript, como o Boolean, String, Array, number, dentre outros.

O tipo mais básico encontrado aqui é o Boolean, cujo valor pode ser true ou false. Além dele, como no JavaScript, todos os valores numéricos no TypeScript são de ponto flutuante, os quais recebem o tipo number. Além dos tipos hexadecimal e decimal, o TypeScript também suporta binários e octais, que foram introduzidos no ES6. Os arrays no TypeScript podem ser inseridos de duas maneiras diferentes: com a utilização dos colchetes ou por meio de um array genérico.

Na **Listagem 4** podemos ver vários exemplos de declaração e atribuição de valores a variáveis de diversos tipos.

```
01 let estaAtivo: boolean = false;
02 let qtdSorvete: number = 10;
03 let nomeCompleto: string = “Edson Dionisio”;
04 let numerosPares: number[] = [2, 4, 6, 8]; //conjunto de inteiros utilizando colchetes.
05 let numerosImpar: Array<number> = [1, 3, 5, 7, 9];
//conjunto de inteiros utilizando array genérico.
```

**Listagem 4**. Definição dos tipos básicos no TypeScript

Além dos tipos básicos apresentados, temos ainda o tipo Enum, que assim como no C#, é utilizado para atribuirmos nomes amigáveis para conjuntos de valores numéricos. Por padrão, os enums são numerados a partir do 0, podendo ser modificada essa configuração de forma manual, se necessário. Também podemos obter o nome de um determinado valor a partir da sua numeração, como podemos ver na **Listagem 5**.

```
// Definição do Enum
enum Color {Red, Green, Blue};
let c: Color = Color.Green;
// Iniciando o Enum com um valor diferente de 0
enum Color {Red = 1, Green, Blue};
let c: Color = Color.Green;
// Pegando o valor a partir da numeração
let colorName: string = Color[2];
```

**Listagem 5**. Utilização de Enums no TypeScript

### Tipos de dado “Any”

Em determinadas situações pode haver dúvida sobre qual tipo de dados utilizar para representar um certo valor. Essa questão é comum quando trabalhamos com aplicações de terceiros, onde devemos obter um determinado resultado, mas não sabemos qual foi o padrão utilizado para a disposição das informações. Para isso, temos à nossa disposição o tipo de dados Any, que permite a passagem dos dados sem que haja a verificação do tipo. Esse tipo é bastante útil e poderoso quando precisamos trabalhar com códigos JavaScript já existentes, permitindo que possamos otimizar o código da melhor forma, gradualmente, sem a necessidade de verificar o tipo de dados no momento da compilação. O trecho de código a seguir exemplifica o uso do Any:

```
let tipoDado: any = 10;
tipoDado = "Teste do tipo de dado Any.. ";
tipoDado = false;
```

### Let, Var e Const

Nos exemplos apresentados até o momento foi utilizada a palavra reservada let para definirmos as variáveis, ao invés de utilizarmos a palavra var. Ambas são bastante parecidas, tendo como diferença a definição do seu escopo. Enquanto o let mantém seus resultados dentro do bloco onde a variável foi especificada, o var define uma variável como global ou local para uma função inteira, independente do escopo no qual tenhamos definido o bloco.

Temos ainda a palavra reservada const, que é um complemento para o let e previne a atribuição de valor a uma variável já declarada (constante).

Observe na **Listagem 6** exemplos de uso de let e var. Note que como as variáveis declaradas por let têm como escopo o bloco no qual são definidas, elas não podem ser acessadas externamente. Inclusive é possível ter variáveis com o mesmo nome, mas em escopos diferentes. Essa, no entanto, pode não ser uma boa prática.

```
var a = 6;
var b = 15;
if (a === 6) {
  let a = 5;  // este mantém o resultado interno ao bloco
  var b = 3; //  Em contrapartida, este declara o valor para função, saindo do bloco.
  console.log(a);  // resultado final = 4
  console.log(b);  // resultado final = 3
}
console.log(a); // resultado final = 6
console.log(b); // resultado final = 3
```

**Listagem 6**. Utilização das palavras reservadas let e var

No exemplo dessa listagem, ao utilizarmos o let dentro de um bloco condicional, o resultado da variável utilizada, presente na linha 4, é limitado apenas para esse bloco. Definimos que a variável a tem o valor 5 e está presente dentro do bloco condicional. Já o resultado para a variável definida como var b recebe o valor dentro do bloco e define ele externamente, saindo assim do escopo do bloco condicional.

### Generics

Uma das principais funcionalidades esperadas de componentes de software é a possibilidade de serem reutilizados. Linguagens de programação como C# têm em seu conjunto de ferramentas os tipos genéricos, que são flexíveis para a utilização com qualquer tipo de dado, mas também bem definidos.

Na **Listagem 7** vemos duas formas de definir uma função. Na primeira declaração a função está pronta para trabalhar apenas com dados do tipo number. Se quisermos trabalhar com qualquer tipo de dado, podemos optar inicialmente por utilizar a segunda forma, onde o argumento any pode receber qualquer valor.

```
// função 1 sem generics
function Validar(arg: number): number {
   return arg;
}
// Função 1 alterada para suportar dados genéricos
function Validar(arg: any): any {
   return arg;
}
```

**Listagem 7**. Utilizando Generics

Apesar da função definida na linha 6 estar pronta para receber qualquer parâmetro, neste ponto não temos informações sobre o real tipo de dados como qual estamos lidando, pois a única informação que teremos de retorno será o any. Precisamos então de uma maneira pela qual seja possível capturar o argumento e ainda assim deixá-lo genérico. No TypeScript, semelhante ao que ocorre em C#, podemos utilizar os chamados generics, cuja declaração utiliza os sinais < e > e dentro deles um nome genérico para o tipo, como vemos a seguir.

```
function Validar<T>(arg: T): T {
    return arg;
}
```

Dessa maneira, temos definida uma variável do tipo T para a função Validar. O T permite que tenhamos controle sobre o tipo de dado fornecido pela função, de forma a podermos utilizar essa informação.

A definição dos generics não se aplica apenas a funções, mas também a classes, interfaces, dentre outros, como no exemplo a seguir:

```
class ClasseGenerica<T> {
    atributo: T;
    funcao: (x: T, y: T) => T;
}
```

### Modules

Como uma das novas definições do ECMAScript 2015, temos introduzido o conceito de módulos para o JavaScript, e, por conseguinte, para o TypeScript. Estes módulos são executados dentro do próprio escopo, não sendo possível o seu uso de forma global. Isto quer dizer que variáveis, funções, classes ou qualquer outra definição, serão visíveis apenas no módulo onde foram declarados. Em C#, o conceito equivalente é implementado na forma de namespaces.

Um módulo pode ser utilizado em outro por meio de declarações explicitas de exportação e importação, declaradas com as palavras reservadas exports e imports entre os arquivos, respectivamente. Na **Listagem 8** temos um exemplo onde criamos um módulo para validações. Esse módulo contém uma classe que recebe o CEP de um endereço e verifica se o mesmo é válido

```
module Validacoes {
 class ValidacaoCEP {
     ehValido(s: string) {
         return s.length === 8 && numberRegexp.test(s);
     }
 }
}
export { ValidacaoCEP };
```

**Listagem 8**. Utilização de Módulos

Para utilizar essa a ValidacaoCEP em outras classes, basta realizar a importação, da seguinte forma:

```
import { ValidacaoCEP } from "./ValidacaoCEP";
  let validaCEP = new ValidacaoCEP();
```

### Interfaces

Outro ponto importante que merece destaque no Typescript é a possibilidade de criarmos interfaces personalizadas, que nos ajudam no momento em que precisamos ter consistência entre os conjuntos de objetos, garantindo assim que os tipos adequados sejam utilizados. Podemos ver um exemplo simples de sua utilização na **Listagem 9**, onde apresentamos uma interface chamada IPessoa e uma classe que implementa esta interface, chamada PessoaFisica.

```
interface IPessoa {
    Nome: string;
    Sobrenome: string;
}

class PessoaFisica implements IPessoa {
   Nome : string;
   Sobrenome : string;
   constructor(public nome, public sobrenome) {
       this.Nome = nome
        this.Sobrenome = sobrenome;
   }
}

class ContaCorrente {
    adicionarCorrentista(pessoa: IPessoa){
        alert(pessoa.Nome);
    }
}

let cliente = new PessoaFisica("Edson", "Dionisio");
let conta = new ContaCorrente();
conta.adicionarCorrentista(cliente);
```

**Listagem 9**. Criação de uma interface com TypeScript

Entre as linhas 1 e 4 definimos a interface IPessoa, que tem apenas duas propriedades. Em seguida, entre as linhas 6 e 13 criamos a classe PessoaFisica, que implementa essa interface e define o construtor recebendo valores para os atributos. Já a classe ContaCorrente, criada entre as linhas 15 e 19 espera, em seu método adicionarCorrentista, um objeto de tipo compatível com IPessoa. Esse objeto, declarado na linha 21, por ser do tipo PessoaFisica, pode ser passado como argumento normalmente na linha 23, uma vez que essa classe implementa a interface esperada.

### TypeScript Playground

Na página oficial do projeto há uma seção chamada Playground onde é possível testar código TypeScript e ver seu equivalente em JavaScript, como ilustra a **Figura 1**. Ao editar o bloco do lado esquerdo, automaticamente o outro lado é automatizado e, após concluir as alterações, basta clicar no botão Run para ver o exemplo em funcionamento.

![Visualização do código de uma classe gerada](https://arquivo.devmedia.com.br/revistas/net/imagens/128/1/image001.jpg)**Figura 1**. Visualização do código de uma classe gerada

Na caixa de seleção que pode ser vista na **Figura 2** podemos escolher entre uma série de exemplos predefinidos para visualizar os principais recursos do TypeScript em funcionamento.

![Exemplos pré-definidos](https://arquivo.devmedia.com.br/revistas/net/imagens/128/1/image002.jpg)**Figura 2**. Exemplos pré-definidos

Nas **Listagens 10** e **11** podemos ver exemplos de código referentes a criação de uma classe simples em TypeScript e seu equivalente em JavaScript, respectivamente. Um exemplo semelhante pode ser obtido ao selecionar a opção Using classes no select da **Figura 2**.

```
class Saudacoes {
   saudacao: string;
   constructor (mensagem: string) {
      this.saudacao = mensagem;
   }
   Saudacoes() {
       return "Olá, " + this.saudacao;
   }
}
```

**Listagem 10**. Classe criada com TypeScript

Enquanto no TypeScript utilizamos termos como class e constructor, que deixam claro, já à primeira vista, do que se trata aquele bloco de código, o equivalente em JavaScript utiliza basicamente funcions para definir todos os elementos. Além disso, para aplicar os conceitos de orientação a objetos no JavaScript, também é necessário utilizar prototypes, como se vê na linha 5 da **Listagem 11**.

```
var Saudacoes = (function () {
    function Saudacoes(mensagem) {
        this.saudacao = mensagem;
    }
    Saudacoes.prototype.Saudacoes = function () {
        return "Olá, " + this.saudacao;
    };
    return Saudacoes;
}());
```

**Listagem 11**. Classe criada com JavaScript

### Cross-browser

Com a grande diversidade de browsers presentes no mercado, temos muitas vezes dificuldades na interpretação correta dos arquivos JavaScript, o que torna necessária a escrita de códigos para Chrome, Firefox, Edge, etc., contendo uma mesma funcionalidade.

<iframe width="560" height="315" src="https://www.youtube.com/embed/KmKZfUqNGOA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen="" style="outline: none; -webkit-tap-highlight-color: transparent; max-width: 100%; margin: auto; height: 455.062px; width: 809px;"></iframe>

Saiba mais: [Curso de TypeScript](https://www.devmedia.com.br/curso/curso-de-typescript/422)

Também neste ponto o TypeScript nos auxilia, pois o código que é escrito para uma determinada funcionalidade é convertido automaticamente para o ECMAScript 3, 5, ou para o commonjs, garantindo a compatibilidade do JavaScript com todos os browsers que implementem esses padrões. Assim, ganhamos em produtividade e reduzimos a necessidade de repetição de código.

### TypeScript no Visual Studio

O principal ambiente de desenvolvimento da Microsoft oferece amplo suporte ao TypeScript, com validação de sintaxe automática em tempo de escrita. De forma semelhante, o editor mais recentemente lançado Visual Studio Code também suporta o desenvolvimento com TypeScript, dispondo inclusive do recurso de IntelliSense e code snippets, através dos quais trechos de código são sugeridos durante a digitação.

A **Figura 3** mostra um exemplo do IntelliSense em ação no Visual Studio Code. Observe, no canto inferior direito, que está selecionada a opção TypeScript, para que o editor possa oferecer as opções mais indicadas para essa sintaxe.

![Edição de código TypeScript no VSCode](https://arquivo.devmedia.com.br/revistas/net/imagens/128/1/image003.png)**Figura 3**. Edição de código TypeScript no VSCode

Como neste artigo utilizaremos o Visual Studio 2015, veremos a seguir alguns recursos que esse IDE nos oferece para trabalhar com TypeScript. Para isso, criaremos um projeto ASP.NET Web Application com o template MVC, o qual chamaremos de DevmediaTypeScript. Com o projeto criado, clicaremos com o botão direito do mouse sobre ele no Solution Explorer e buscaremos a opção Add > TypeScript File, como mostra a **Figura 4**. Ao nosso arquivo, daremos o nome de TesteDevmedia.

![Adicionando um novo arquivo TypeScript](https://arquivo.devmedia.com.br/revistas/net/imagens/128/1/image004.jpg)**Figura 4**. Adicionando um novo arquivo TypeScript

Caso esta opção não esteja sendo apresentada, podemos utilizar as teclas de atalho Ctrl+Shift+A, para adicionar um novo item, e em Web > Scripts encontraremos os arquivos necessários, como mostra a **Figura 5**.

![Adicionando um novo item](https://arquivo.devmedia.com.br/revistas/net/imagens/128/1/image005.jpg)**Figura 5**. Adicionando um novo item

Com o arquivo criado, perceba que ele já está com a extensão .ts, assim terá acesso a todos os recursos oferecidos pelo TypeScript.

Começaremos com um exemplo simples, onde teremos apenas uma função para a soma de dois valores, como pode ser visto na **Figura 6**.

![Função de soma com TypeScript](https://arquivo.devmedia.com.br/revistas/net/imagens/128/1/image006.png)**Figura 6**. Função de soma com TypeScript

Com este tipo de arquivo podemos trabalhar com diversas funcionalidades, de igual forma a outras linguagens de alto nível como o C#, onde podemos ir para as definições das funções criadas, buscar por referências, etc. Além disso, o IDE nos avisa sobre erros de codificação ou parâmetros incorretos, como podemos ver na **Figura 7**. Outro ponto positivo é que o IDE é capaz de “julgar” os tipos de variáveis, inclusive quando não especificamos os tipos de dados que iremos utilizar.

![Aviso de erro com IntelliSense](https://arquivo.devmedia.com.br/revistas/net/imagens/128/1/image007.png)**Figura 7**. Aviso de erro com IntelliSense

### Utilizando tipagem estática

Um dos recursos no JavaScript que sentimos falta é a tipagem estática, que apesar de para alguns cenários ser um ponto positivo dessa linguagem, em outros acaba se tornando negativo, devido ao fato de deixar a linguagem mais propensa a erros. Para aplicarmos esse conceito na prática, podemos modificar a função adiciona e modificar em sua assinatura o tipo dos argumentos esperados, da seguinte forma:

```
function adicionar(x:number, y:number) {
    return x + y;
}
```

Temos no nosso exemplo a solicitação de dois valores numéricos. Caso não houvesse a tipagem estática, poderíamos tranquilamente passar para essa função dois valores textuais, por exemplo. Em execução, teríamos como retorno a concatenação dos valores, o que não é o comportamento esperado neste caso. Graças a esse recurso do TypeScript e seu suporte no Visual Studio, podemos verificar, em tempo de escrita, que um erro está ocorrendo ao chamar o método adiciona com argumentos de tipos diferentes dos esperados, como mostra a **Figura 8**.

![Verificação estática de tipos](https://arquivo.devmedia.com.br/revistas/net/imagens/128/1/image008.png)**Figura 8**. Verificação estática de tipos

Assim como foi visto na **Figura 3**, no VSCode, o IntelliSense do Visual Studio também nos oferece diversas sugestões de palavras reservadas durante a digitação ou quando pressionamos Ctrl+Espaço (**Figura 9**).

![Tipos de dados apresentados com o IntelliSense](https://arquivo.devmedia.com.br/revistas/net/imagens/128/1/image009.png)**Figura 9**. Tipos de dados apresentados com o IntelliSense

Outro ponto positivo que temos a nosso favor ao trabalhar com TypeScript é que para os tipos de dados mais usados no HTML, ele implementa as interfaces, permitindo que acessemos diretamente os tipos de elementos HTML, como pode ser visto na **Figura 10**.

![Tipos de elementos HTML](https://arquivo.devmedia.com.br/revistas/net/imagens/128/1/image010.png)**Figura 10**. Tipos de elementos HTML

Esse recurso também nos auxilia quando precisamos acessar as propriedades de uma classe ou interface, listando todos os membros disponíveis, como na **Figura 11**. Note também que diferentes símbolos são utilizados para representar os diferentes elementos, como classes, interfaces, métodos e propriedades.

![IntelliSense para membros da classe](https://arquivo.devmedia.com.br/revistas/net/imagens/128/1/image011.png)**Figura 11**. IntelliSense para membros da classe

Agora que conhecemos os conceitos principais sobre o TypeScript e sua utilização no Visual Studio, criaremos uma aplicação de exemplo onde o aplicaremos em conjunto com o AngularJS para montar uma listagem de funcionários.

### Projeto TypeScript com AngularJS

Para este exemplo criaremos um projeto do tipo ASP.NET Web Application com o template Empty, e em seguida devemos excluir o arquivo web.config, pois não precisaremos dele. Na sequência, utilizaremos o gerenciador de pacotes NuGet para adicionar as bibliotecas necessárias ao nosso exemplo, que são a AngularJS.Core, AngularJS.Route e a angularjs.TypeScript.DefinitelyTyped, na qual estão as definições do AngularJS para o TypeScript. Os pacotes instalados podem ser vistos na **Figura 12**.

![Pacotes para trabalhar com AngularJS](https://arquivo.devmedia.com.br/revistas/net/imagens/128/1/image012.jpg)**Figura 12**. Pacotes para trabalhar com AngularJS

Saiba mais: [Primeiros passos no Angular](https://www.devmedia.com.br/angular/)

Após a adição dos pacotes, podemos ver que um novo diretório Scripts foi adicionado ao projeto e, dentro dele, temos todos os arquivos do AngularJS com a extensão “.ts” necessários ao nosso projeto, como pode ser visto na **Figura 13**.

![Arquivos no diretório scripts](https://arquivo.devmedia.com.br/revistas/net/imagens/128/1/image013.jpg)**Figura 13**. Arquivos no diretório scripts

### Criando a Interface

Com as bibliotecas instaladas, seguiremos com a criação da interface. Primeiramente criaremos um novo diretório na raiz do projeto, que chamaremos de app, onde adicionaremos todo o código da aplicação no decorrer do desenvolvimento. Nesta aplicação, utilizaremos os serviços do [Angular](https://www.devmedia.com.br/guia/angular/38245) que irão se comunicar com a API REST do back-end, com o intuito de obter os funcionários registrados. Para começar, definiremos as interfaces em um diretório separado da lógica de negócio da aplicação. Para isso, criaremos dentro do diretório app, um novo diretório chamado interfaces. Feito isso, adicionaremos um novo arquivo TypeScript, chamado interfaces.ts, no qual deveremos adicionar o código da **Listagem 12**.

```
module AngularTypeScriptDevmedia.Interfaces {
   export interface IFuncionariosService {
       getFuncionarios: () => Array<IDadosFuncionario>;
   }
   export interface IDadosFuncionario {
       NomeCompleto: string;
       Email: string;
       Telefone: string;
       Setor: string;
       Funcao: string;
       Salario: number;
   }
}
```

**Listagem 12**. Criação do arquivo interfaces.ts

Neste primeiro momento, criamos um módulo chamado AngularTypeScriptDevmedia.Interfaces com duas interfaces: IFuncionariosService, na qual temos o método getFuncionarios(), que não recebe parâmetros e deve retornar todos os funcionários cadastrados; e IDadosFuncionario, que recebe todas as informações básicas dos funcionários. Ao utilizarmos as interfaces, garantimos que não serão passados objetos aleatórios na nossa aplicação, que podem causar erros inesperados no código.

Precisaremos agora criar um novo arquivo no qual implementaremos a interface de serviços. Para isso, adicionaremos um novo diretório que chamaremos de services, onde adicionaremos um novo arquivo TypeScript chamado FuncionarioService, cujo código encontra-se na **Listagem 13**.

```
/// <reference path="../interfaces/interfaces.ts" />
module AngularTypeScriptDevmedia.Services {
   export class FuncionariosService implements
   AngularTypeScriptDevmedia.Interfaces.IFuncionariosService {
       httpService: ng.IHttpService
       static $inject = ["$http"];
       constructor($http: ng.IHttpService) {
           this.httpService = $http;
       }
       getFuncionarios = () => {
        var listaFuncionarios: Array<AngularTypeScriptDevmedia.Interfaces
        .IDadosFuncionario> = [
        { NomeCompleto: "Edson Dionisio", Email: "edson.dionisio@gmail.com",
        Telefone: "81997402800", Setor:
        "Desenvolvimento de sistemas", Funcao: "Desenvolvedor Júnior",
        Salario: 2000 },
        { NomeCompleto: "Marília Késsia", Email: "mkessia@gmail.com",
        Telefone: "81997402800", Setor:
        "Educação", Funcao: "Professora", Salario: 3000 },
        { NomeCompleto: "Caroline França", Email: "carol.dionisio@gmail.com",
        Telefone: "81997400000",
        Setor: "Estética e cosméticos", Funcao: "Esteticista", Salario: 5000 },
        { NomeCompleto: "Renato Nascimento",
        Email: "renato.nascimento@gmail.com", Telefone:
        "81996609900", Setor: "Desenvolvimento de sistemas",
        Funcao: "Desenvolvedor sênior", Salario: 1500 },
        { NomeCompleto: "Mayara", Email: "mayara@gmail.com",
        Telefone: "81999999800", Setor:
        "Desenvolvimento de sistemas", Funcao: "Tester", Salario: 2500 },
        { NomeCompleto: "Benilton Lopes", Email: "benilton@gmail.com",
        Telefone: "81999999999",
        Setor: "Engenharia", Funcao: "Engenheiro elétrico", Salario: 10000 },
        { NomeCompleto: "Artur Oliveira", Email: "arturoliveira@gmail.com",
        Telefone: "81888888888",
        Setor: "Desenvolvimento de sistemas",
        Funcao: "Coordenador de equipe", Salario: 4800 },
        { NomeCompleto: "Alberto", Email: "alberto@gmail.com",
        Telefone: "81999999999",
        Setor: "Desenvolvimento de sistemas",
        Funcao: "Gerente de negócios", Salario: 8100 },
        { NomeCompleto: "Marcelo", Email: "marcelo@gmail.com",
        Telefone: "81999999999",
        Setor: "Financeiro", Funcao: "Gestor financeiro",
        Salario: 7500 },
        { NomeCompleto: "Mariana", Email: "mariana@gmail.com",
        Telefone: "81999999999",
        Setor: "Recursos Humanos", Funcao: "estagiária",
        Salario: 1200 }
          ];
          return listaFuncionarios;
        }
   }
angular.module("AngularTypeScriptDevmedia").service("AngularTypeScriptDevmedia
.Services.FuncionariosService", FuncionariosService);
 }
```

**Listagem 13**. Arquivo FuncionarioService

Nessa listagem estamos encapsulando o serviço criado anteriormente em um novo módulo que chamamos de AngularTypeScriptDevmedia.Services. Além disso, utilizamos a palavra-chave export para garantir que o nosso serviço estará disponível para ser chamado a partir desse módulo. Em seguida, para utilizarmos o serviço, criamos uma nova classe que implementa a interface IDadosFuncionario e nela adicionamos alguns dados fictícios para efeito de testes.

No AngularJS existem cinco maneiras diferentes de criarmos um serviço: service (utilizado no exemplo), factory, provider, value e constant. Cada um dos tipos apresentados possui seus prós e contras para a criação dos serviços, mas neste exemplo utilizaremos apenas o primeiro modelo.

Dando prosseguimento, o nosso serviço precisa se comunicar com as APIs de back-end, devido a isso, utilizamos o $http, um serviço do AngularJS que ao ser adicionado nas dependências do construtor, irá agir em tempo de execução para realizar a comunicação. O $inject, apresentado na linha 5, é uma propriedade especial que o AngularJS irá consumir. É preciso ter certeza de que o $inject tenha sido definido como static, pois o seu valor é um array de strings e cada um dos arrays é identificado para um serviço em particular, além de também definir a ordem na qual as strings serão adicionadas ao vetor. O AngularJS realiza a verificação em tempo de execução para determinar quais são os serviços que precisam ser injetados. Na linha 25 temos adicionado o código padrão que é encarregado de acrescentar a nossa classe para o módulo como um serviço.

Finalizada esta etapa, deveremos clicar com a direita no diretório app e em seguida adicionar o arquivo TypeScript chamado app.module, onde definiremos o módulo do AngularJS que controlará as rotas da aplicação. Seu código pode ser visto na **Listagem 14**.

```
/// <reference path="../scripts/typings/angularjs/angular.d.ts" />
((): void => {
   var app = angular.module("AngularTypeScriptDevmedia", [''ngRoute'']);
   app.config(AngularTypeScriptDevmedia.Routes.configureRoutes);
})()
```

**Listagem 14**. Criando o app.module

Na linha 1 dessa listagem referenciamos o arquivo com as definições do AngularJS e na linha 3 adicionamos a dependência do módulo ngRoute. Na linha seguinte temos a definição das configurações de rota fornecidas por uma função de referência contida no namespace AngularTypeScriptDevmedia.Routes, a qual será um novo arquivo TypeScript cujo código pode ser visto na **Listagem 15**, ao qual chamaremos de app.routes.ts.

```
/// <reference path="../scripts/typings/angularjs/angular.d.ts" />
/// <reference path="../scripts/typings/angularjs/angular-route.d.ts" />
module AngularTypeScriptDevmedia {
  export class Routes {
    static $inject = ["$routeProvider"];
    static configureRoutes($routeProvider: ng.route.IRouteProvider) {
        $routeProvider.when("/home",
           {
               controller: "AngularTypeScriptDevmedia.controllers.FuncionarioController",
               templateUrl: "/app/views/funcionarios.html",
               controllerAs: "funcionario"
            });
        $routeProvider.otherwise({ redirectTo: "/home" });
  }
  }
}
```

**Listagem 15**. Criando a estrutura de roteamento

Nessa listagem estamos configurando uma rota /home que ao ser acessada repassará o controle para o FuncionarioController e utilizará a view funcionários.html, contida na pasta /app/views. Já na linha 13 definimos que qualquer outro URL acessado deve ser redirecionado para a rota padrão /home.

Devemos agora criar a classe FuncionarioController, de acordo com a **Listagem 16**.

```
/// <reference path="../services/FuncionariosService.ts" />
/// <reference path="../interfaces/interfaces.ts" />
/// <reference path="../../scripts/typings/angularjs/angular.d.ts" />
module AngularTypeScriptDevmedia.controllers {
   export class FuncionarioController {
       FuncionariosService: AngularTypeScriptDevmedia.Interfaces.IFuncionariosService;
       static $inject = ["AngularTypeScriptDevmedia.Services.FuncionariosService"];
          constructor(FuncionariosService: AngularTypeScriptDevmedia.Interfaces
          .IFuncionariosService) {
           this.FuncionariosService = FuncionariosService;
       }
          listaFuncionarios: Array<AngularTypeScriptDevmedia.Interfaces
          .IDadosFuncionario>;
       getFuncionariosDestaque = () => {
              this.listaFuncionarios = this.FuncionariosService.getFuncionarios();
       }
   }
   angular.module("AngularTypeScriptDevmedia").
controller("AngularTypeScriptDevmedia.controllers.FuncionarioController",
FuncionarioController);
}
```

**Listagem 16**. Criação do controller de funcionários

Nesta última etapa, criamos o controller e especificamos o serviço como dependência no construtor, como mostra a linha 8. No controller definimos uma propriedade que chamamos de listaFuncionarios, presente na linha 11, utilizada para vincular os dados à nossa view. Além disso, definimos uma função lambda, na linha 12, que será utilizada para preenchermos a propriedade listaFuncionarios com os resultados da chamada do serviço.

Por fim, criaremos a nossa view, que será responsável por apresentar as informações dos funcionários. A view que criaremos será chamada de funcionarios.html e seu código ficará como na **Listagem 17**.

```
<div class="jumbotron">
    <ul class="list-group">
        <li ng-show="Funcionario.listaFuncionarios" class="list-group-item"
         ng-repeat="devFunc in Funcionario.listaFuncionarios">
            {{ devFunc.NomeCompleto}}
            {{ devFunc.Email}}
            {{ devFunc.Telefone}}
            {{ devFunc.Setor}}
            {{ devFunc.Funcao}}
            {{ devFunc.Salario}}
        </li>
    </ul>
    <button class="btn btn-block" ng-click="Funcionario.getFuncionariosDestaque()"
 >Mostra todos os funcionários</button>
</div>
```

**Listagem 17**. View de listagem de funcionários

Essa view basicamente utiliza a diretiva ng-repeat para iterar sobre a lista de funcionários do controller (linha 3) e para cada objeto adicionamos um item na lista (linhas 4 a 9). Na linha 12 o botão faz uma chamada ao método getFuncionariosDestaque do controller, atualizando a lista e a view.

Com toda esta etapa finalizada, partiremos para o último ponto que é a criação do arquivo Index.html, o qual é definido na raiz do projeto com o código que vemos na **Listagem 18**. Mas para que essa página tenha o resultado esperado, precisamos antes instalar o pacote do Bootstrap pelo NuGet, assim como foi feito com os pacotes do AngularJS. Ao instalá-lo, será criado o diretório Content com várias folhas de estilo, e o fonts, com os arquivos de fonte utilizados pelo Bootstrap.

```
<!DOCTYPE html>
<html ng-app="AngularTypeScriptDevmedia">
<head>
   <title>Trabalhando com TypeScript e ASP.NET</title>
   <link href="content/bootstrap.min.css" rel="stylesheet" />
</head>
<body>
  <div class="container">
       <div class="page-header">Clique no botão para ver os funcionários cadastrados.</div>
       <div class="row">
           <div class="col-md-4 col-md-offset-4">
               <div ng-view=""></div>
           </div>
       </div>
   </div>
   <script src="scripts/angular.js"></script>
   <script src="scripts/angular-route.js"></script>
   <script src="app/app.routes.js"></script>
   <script src="app/app.module.js"></script>
   <script src="app/services/FuncionariosService.js"></script>
   <script src="app/controllers/FuncionarioController.js"></script>
</body>
</html>
```

**Listagem 18**. Criação do arquivo Index.html

Nessa página apenas referenciamos os arquivos CSS e JavaScript necessários para montar a interface com os recursos do AngularJS. Na linha 12 a div marcada com ng-view carregará a view funcionários.html quando for necessário, trazendo já os dados do controller. Note que nas últimas linhas estamos referenciando os arquivos com extensão “.js” e não “.ts”. Isso ocorre porque, como vimos no início do artigo, o código TypeScript é compilado para JavaScript, gerando arquivos equivalentes com mesmo nome. Esses arquivos resultantes são os que serão utilizados pelo browser em tempo de execução.

A utilização de TypeScript em aplicações onde se tem intenso uso de JavaScript permite que o código seja melhor estruturado, e que as melhores práticas e técnicas de programação sejam utilizadas. Com o apoio do Visual Studio, é possível aproveitar com maior facilidade todos os recursos desse superset da linguagem JavaScript, cujo suporte nesse IDE também tem evoluído a cada versão. Contando também com o suporte a Node.js, por exemplo, é possível desenvolver aplicações completas, desde o back-end até o front-end utilizado apenas JavaScript como linguagem principal. Ou, caso seja mais adequado para o projeto, pode-se aliar os recursos do TypeScript a projetos que já utilizem outra linguagem no lado servidor, como em Single Page Applications usando Web API e AngularJS. As possibilidades são muitas e para a maioria delas o Visual Studio poderá suportar o desenvolvimento.

**Links**:

- [TypeScript](http://www.typescriptlang.org/)
- [AngularJS](https://angularjs.org/)

Tecnologias:

- [.NET](https://www.devmedia.com.br/net/) 
- AngularJS 
- [JavaScript](https://www.devmedia.com.br/javascript/) 
- Microsoft 
- [TypeScript](https://www.devmedia.com.br/typescript/)