![Tela de um computador exibindo códigos em typescript.](https://blog-geek-midia.s3.amazonaws.com/wp-content/uploads/2021/01/25102746/typescript-820x547.jpg)

- [Front-end](https://blog.geekhunter.com.br/category/front-end/)

# Introdução a Typescript: o que é e como começar?

- maio 14, 2021
- [2 Comments](https://blog.geekhunter.com.br/introducao-a-typescript/#disqus_thread)

Sabendo das limitações que o Javascript possui, Anders Hejlsberg, que também participou da criação do C#, do Delphi, do Turbo Pascale da plataforma .NET, resolveu criar o Typescript.

O objetivo era elevar o nível de código do JS, que era usado apenas do lado cliente e em códigos pequenos.

Hoje, o cenário é outro, pois a possibilidade de aplicar uma arquitetura mais sólida e melhores práticas de programação mudaram essa realidade.

O Javascript suporta o paradigma de Programação Orientada a Objetos graças ao Typescript, podendo usar variáveis com tipos definidos, criar classes…

Hoje você vai entender como funciona o Typescript, suas diferenças e vantagens perante o Javascript e porque você deveria usá-lo.

**Conteúdo** [ocultar](https://blog.geekhunter.com.br/introducao-a-typescript/#) 

[1 O que é TypeScript](https://blog.geekhunter.com.br/introducao-a-typescript/#O_que_e_TypeScript)

[2 Qual a diferença entre TypeScript e JavaScript](https://blog.geekhunter.com.br/introducao-a-typescript/#Qual_a_diferenca_entre_TypeScript_e_JavaScript)

[3 Vantagens do Typescript](https://blog.geekhunter.com.br/introducao-a-typescript/#Vantagens_do_Typescript)

[4 TypeScript: tipagem estática](https://blog.geekhunter.com.br/introducao-a-typescript/#TypeScript_tipagem_estatica)

[4.1 Os tipos mais utilizados no TypeScript são:](https://blog.geekhunter.com.br/introducao-a-typescript/#Os_tipos_mais_utilizados_no_TypeScript_sao)

[5 TypeScript e a orientação a objetos](https://blog.geekhunter.com.br/introducao-a-typescript/#TypeScript_e_a_orientacao_a_objetos)

[5.1 Classes](https://blog.geekhunter.com.br/introducao-a-typescript/#Classes)

[5.2 Herança](https://blog.geekhunter.com.br/introducao-a-typescript/#Heranca)

[5.3 Encapsulamento](https://blog.geekhunter.com.br/introducao-a-typescript/#Encapsulamento)

[5.4 Classes abstratas](https://blog.geekhunter.com.br/introducao-a-typescript/#Classes_abstratas)

[5.5 Interfaces](https://blog.geekhunter.com.br/introducao-a-typescript/#Interfaces)

[6 Instalação do Typescript](https://blog.geekhunter.com.br/introducao-a-typescript/#Instalacao_do_Typescript)

[6.1 Verificando instalação](https://blog.geekhunter.com.br/introducao-a-typescript/#Verificando_instalacao)

[6.2 Começando a utilização](https://blog.geekhunter.com.br/introducao-a-typescript/#Comecando_a_utilizacao)

[7 React TypeScript](https://blog.geekhunter.com.br/introducao-a-typescript/#React_TypeScript)

[8 Angular TypeScript](https://blog.geekhunter.com.br/introducao-a-typescript/#Angular_TypeScript)

[8.1 Instalação](https://blog.geekhunter.com.br/introducao-a-typescript/#Instalacao)

[9 Conclusão](https://blog.geekhunter.com.br/introducao-a-typescript/#Conclusao)

## O que é TypeScript

![O que é Typescript](https://blog-geek-midia.s3.amazonaws.com/wp-content/uploads/2021/05/14102116/o-que-e-typescript-1024x536.jpeg)Representação do superset Typescript

Typescript é uma linguagem de código aberto desenvolvida pela Microsoft que foi construída em cima do Javascript, que é muito difundido atualmente. Então esse “superset” foi criado para adicionar recursos de tipagem estáticas à linguagem original.

Em outras palavras, temos todas as funcionalidades do Javascript no Typescript acrescidas de várias outras funcionalidades que caracterizam o Typescript.

Embora Typescript seja um superset do Javascript, na hora de compilar o código, todo Typescript é convertido/transpilado para Javascript.

A pessoa desenvolvedora que estiver escrevendo códigos em Typescript lidará com uma sintaxe simplificada, mais clara e suportada por vários TaskRunners ou IDES, mas o seu código voltará a ser JS após transpilado.

Isso se dá pelo browser não entender a sintaxe de outra linguagem de programação que não seja Javascript.

## Qual a diferença entre TypeScript e JavaScript

![Typescript superset de Javascript](https://blog-geek-midia.s3.amazonaws.com/wp-content/uploads/2021/05/14102139/typescript-1024x919.jpg)Relação entre supeset Typescript e Javascript

Bom, já que TS nasceu de JS e veio para suprir algumas limitações, vou apresentar algumas diferenças básicas entre os dois:

| **Características do Typescript**                            | **Características do Javascript** |
| ------------------------------------------------------------ | --------------------------------- |
| Tipagem estática                                             | Tipagem dinâmica                  |
| [Orientação a objetos](https://blog.geekhunter.com.br/introducao-ao-javascript-numeros-e-objetos/) | Programação estruturada           |
| Genéricos                                                    | Funções                           |
| Namespaces                                                   | Prototypes                        |
| Decorators                                                   | Funções contrutoras               |

Nesse sentido, dizer que TypeScript é outra linguagem de programação diferente do JavaScript não é verdade, pois tudo que o JavaScript oferece você pode ser usado dentro de um código TypeScript e, na prática, a sintaxe JS é utilizada também.

Porém, o contrário não é verdade, se optar por JavaScript, as funcionalidades inerentes ao TypeScript não poderão ser utilizadas, como a tipagem forte, por exemplo.

**Essa é uma das grandes vantagens da utilização do TypeScript:**

Os tipos nos fornecem uma maneira de descrever um objeto não só mais precisamente, gerando uma documentação mais concisa, mas também uma validação do código em tempo de compilação.

## Vantagens do Typescript

A principal caraterística do TypeScript é sua tipagem forte, razão pela qual leva no seu nome: *type* quer dizer tipo. Mas também há outro aspecto, a **Orientação a Objetos**.

O JavaScript, na maior parte do seu projeto de linguagem, não é tipado e a inferência de tipo só vai até certo ponto. Daí uma necessidade maior de utilizar o TypeScript caso queira suprir essas deficiências.

## TypeScript: tipagem estática

No TypeScript, os tipos são inferidos de forma implícita, mas também podemos explicitar o tipo. Por exemplo, no código abaixo explicitamos que o tipo da variável *numeroQualquer* é do tipo *number*.

```
let numeroQualquer: number;
valor = 10.5;
```

Devido a tipagem estática, se tentarmos atribuir um valor do tipo string ao atributo numeroQualquer, receberemos um erro.

```
let valor: number;
valor = ‘frase qualquer’; // não é válido
```

Vale ressaltar que o TypeScript não diferencia valores ponto flutuante (decimal) de valores inteiros. Todos são tratados como sendo do tipo *number*.

No exemplo acima, a tipagem é explícita. Mas o TypeScript realiza a inferência de tipo. Por exemplo, no código abaixo, quando atribuímos a string ‘Carpe Diem’ à variável *fraseLegal*, implicitamente definimos que essa variável é do tipo string e, portanto, a linha de código logo em seguida gerará um erro de compilação.

```
let fraseLegal = ‘Carpe Diem’;
fraseLegal = 98.5; // não é válido a atribuição do tipo number para um tipo string.
```

> Tutorial: linting em [TypeScript com ESLint](https://blog.geekhunter.com.br/eslint-typescript-tutorial/)

#### Os tipos mais utilizados no TypeScript são:

- **Number**

É para todo e qualquer tipo de número, seja ele ponto flutuante ou inteiro.

- **String**

Representa uma string costumeiramente conhecida em outras linguagens de programação.

- **Boolean**

Representa um valor booleano: true ou false.

- **Any**

A tradução de Any é qualquer e, como sua tradução sugere, é um tipo que pode ser modificado para qualquer outro tipo presente na linguagem, seja string, number, boolean ou qualquer outra coisa.

Geralmente esse tipo de informação vem de uma API ou diretamente do usuário.

- **Array**

Representa o tipo Array dentro da linguagem. É válido informar que podemos criar arrays de duas formas dentro do TypeScript.

A primeira:

```
let list: number[ ] = [2, 3, 5, 7];
```

A segunda:

```
var list: Array<number> = [2, 3, 5, 7, 11]
```

Uma peculiaridade muito legal, porém não recomenda é fato de podermos definir um array com tipos diferentes:

```
let array: [string, number];
x = [“Hello”, 10];  // Inicialização
```

Esse também é um tipo, chamado **Tupla**.

Existem outros tipos como:

- **Tuple**

Como visto anteriormente, os tipos de tupla permitem expressar um array com um número fixo de elementos cujos tipos são conhecidos, mas não precisam ser os mesmos.

- **Enum**

Assim como em outras linguagens, enum é um tipo que permite declarar um conjunto valores nomeados e constantes pré-definidos.

```
enum Cor {

	VERMELHO,
	VERDE,
	AZUL,
}

let cor: Cor = Cor.Azul;
```

- **Unknown**

Às vezes, precisamos de um tipo de variável que não sabemos quando estamos escrevendo um código. Esses valores podem vir de conteúdo dinâmico. Nesses casos, é conveniente fornecer definir ao compilador e até outros programadores que tal variável pode ser qualquer coisa.

```
let valorDesconhecido: unknown;

valorDesconhecido = true;
valorDesconhecido = 100.0;
valorDesconhecido = 5;
valorDesconhecido = “Alô Mundo!”;
valorDesconhecido = null;
valorDesconhecido = undefined;
```

- **Null and Undefined**

Nada mais são do que seus próprios nomes dizem.

```
let u: undefined = undefined;
let n: null = null;
```

- **Void**

O tipo void é visto como um tipo de retorno de funções que não retornam valor nenhum, geralmente chamadas de procedimentos.

```
function minhaFuncao(): void {
	console.log(“Minha Função”);
	}
```

A documentação desses tipos, bem como exemplo, você pode encontrar nesse [link](https://www.typescriptlang.org/docs/handbook/basic-types.html).

[![Banner com link para ser uma Pessoa desenvolvera que as empresas procuram](data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20720%20200'%3E%3C/svg%3E)](https://bit.ly/3qKv5Za)

## TypeScript e a orientação a objetos

A utilização do paradigma de orientação a objetos no JavaScript pode gerar algumas dúvidas. Com TypeScript, tudo pode ficar muito fácil.

Ele oferece a possibilidade de utilizarmos classes, interfaces, encapsulamento, herança, e outras coisinhas a mais. É muito incrível.

### Classes

A declaração de classes no TypeScript é simples, semelhante a outras linguagens de programação.

```
class Exemplo { 

	// atributos
	// construtor
	// getter e setters
	// outros métodos
}
```

### Herança

Assim como no Java, por exemplo, para herdar uma classe utilizamos o comando *extends*. Um detalhe importante é que se um método da classe base for subscrito na classe herdeira, podemos chamar o método da classe base utilizando o comando *super*.

```
class ClasseBase {
	nome: string;
	
	constructor(nome: string) {
		this.nome = nome;
	}
	
	print(msg: string = ‘Classe Base’) {
		console.log(msg)
	}
}

class ClasseHerdeira extends ClasseBase {
	
	constructor(nome: string) {
	 	super(nome)
	}
	
	print(msg: string = ‘Classe Herdeira’) {
		super.print(msg);
	}

}
```

Observe a utilização do comando super na classe *ClasseHerdeira* para chamar o método print da classe base *ClasseBase*.

### Encapsulamento

O TypeScript faz uso do conceito de encapsulamento, presente em outras linguagens orientadas a objetos, através de getters e setters para acesso aos atributos protegidos de uma classe.

```
class ClasseExemplo {
	private _nome: string
	
	get nome(): string {
		return this._nome;
		}

	set nome(nome:string): void {
		this._nome = nome;
		}
}
```

### Classes abstratas

As classes abstratas servem como base para construção de outras classes, dando-lhes a estrutura padrão de métodos e atributos.

```
abstract class ClasseAbstrata {
	
	constructor(public nome: string){
		}


printNome(): void {

	console.log(‘Nome’ + this.nome)
}

abstract otherPrint(): void; // deverá ser implementado nas classes filhas

abstract class ClasseAbstrata {
	
	constructor(public nome: string){
		}


printNome(): void {

	console.log(‘Nome’ + this.nome)
}

abstract otherPrint(): void; // deverá ser implementado nas classes filhas

}

class ClasseFilhaAbs extends ClasseAbstrata {

	constructor() {
		super(‘Classe Filha Abs’);
	}

	printNome(): void {
		console.log(‘Classe Filha Abs’);
	}

	otherPrint(): void {
		console.log(‘Other print method’);
	}

}
```

### Interfaces

Assim como as classes abstratas, as interfaces também definem a estrutura das classes que “assinam o contrato” com elas.

A diferença fundamental é que todos os métodos e atributos da interface devem ser implementados nas classes filhas. No entanto, você pode definir atributos como opcional também.

```
interface ClasseInterface {
	atributo1: string;
	atriburo2?: number
	
	print();
}

class ClasseFilha implements ClasseInterface {
	atributo1: string = ‘Classe Filha’;
	atriburo2?: number = 1;
	
	print() {
	console.log(this.atributo1);
	}
}
```

Agora que tratamos dos aspectos principais, como criar um projeto utilizando TypeScript? É isso que vamos ver agora! Vamos começar com a instalação.

Mas antes de continuarmos, se você quiser testar a sintaxe do TypeScript tentando construir códigos com a linguagem, existe uma ferramenta online disponível para isso: o [Playground](https://www.typescriptlang.org/play?#code/JYWwDg9gTgLgBAKjgQwM5wEoFNkGN4BmUEIcA5FDvmQNwCwAUKJLHAN5wCuqWAyjMhhYANFx4BRAgSz44AXzhES5Snhi1GjLAA8W8XBAB2qeAGEInQ0KjjtycABsscALxwAFAEpXAPnaM4OANjeABtA0sYUR4Yc0iAXVcxPgEhdwAGT3oGAOTJaXx3L19-BkDAgBMIXE4QLCsAOhhgGCckgAMATQsgh2BcAGssCrgAEjYIqwVmutR27MC5LM0yuEoYTihDD1zAgB4K4AA3H13yvbAfbs5e-qGRiYspuBmsVD2Aekuz-YAjThgMCMcCMpj6gxcbGKLj8MTiVnck3gAGo4ABGTxyU6rcrlMF3OB1H5wT7-QFGbG4z6HE65ZYMOSMIA).

## Instalação do Typescript

Para instalação e utilização do TypeScript, você precisará do NodeJs instalado e seu gerenciador de pacotes padrão: NPM.

Pelo menos para sistemas operacionais Windows, o NPM já vem com Node.js quando o instalamos.

Abra o cmd e execute o comando abaixo:

```
npm i -g typescript
```

O comando acima instala o TypeScript globalmente na sua máquina.

### Verificando instalação

Execute o comando abaixo. Se o TypeScript estiver instalado, a versão aparecerá no console.

```
tsc -v
```

### Começando a utilização

Antes de começar a utilização, vamos precisar de um arquivo de configurações para o compilador do TypeScript. Dentro de um diretório, abra seu terminal e execute o comando abaixo:

```
tsc --init
```

O comando acima, criará o arquivo tsconfig.json de forma automática. Depois disso, é só criar um arquivo com extensão .ts e começar a utilizar.

A forma manual de realizar a execução pode ser da seguinte forma:

```
tsc <<nome_do_seu_arquivo>>
```

Esse comando irá criar um arquivo JavaScript com o mesmo nome do arquivo TypeScript. É o código transpilado para a sintaxe do JavaScript.

Como tinha dito antes, quando a compilação for realizada, todo o código TS se tornará um código JS.

Existe uma maneira mais simples de executar um arquivo TypeScript através de plugin instalado no Visual Studio Code: *Coder Runner*. Com esse plugin instalado, teremos que instalar outra dependência: *ts-node*. Para isso execute o comando abaixo:

```
npm i -g ts-node
```

Agora, quando quiser executar um arquivo TypeScript, use o atalho do Windows:

*Ctrl + Alt + N*.

Alguns frameworks front-end para construção de aplicações Web SPA, como React e Angular, também trabalham com TypeScript. Então vamos falar um pouco sobre isso. Vamos lá?

## React TypeScript

![Integração do Typescript com o React](data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%201024%20569'%3E%3C/svg%3E)Integração do Typescript com o React

[ReactJs](https://blog.geekhunter.com.br/como-aprender-react/) é uma biblioteca JavaScript com cara de framework desenvolvida pelo Facebook para construção de interfaces de usuário (IU), bastante popular na comunidade dev.

O template padrão que o React usa é com o JavaScript, mas pode ser alterado para o TypeScript facilmente.

No React com Javascript, os arquivos têm extensões .js ou .jsx. Com o template TypeScript, as extensões são .ts ou .tsx.

De qualquer forma, para ambos os templates, a essência da sintaxe do JSX continua a mesma. Basicamente, todas as caraterísticas do TypeScript que já falamos estarão disponíveis para serem utilizadas.

Para um projeto React com TypeScript, execute o comando abaixo:

```
npx create-react-app <<nome_do_seu_projeto>> --template Typescript
```

Esse comando acima cria um projeto pronto para ser utilizado com TypeScript. Se você já tiver um projeto criado, pode adicionar o TypeScript ao projeto através do comando abaixo:

```
npm install --save-dev typescript
```

Nesse último caso, precisamos modificar a seção scripts no arquivo package.json. Uma vez que temos o acesso ao comando tsc, fazemos da seguinte forma:

```
{	
       “scripts”: {
  “build”: “tsc”,
	 },
}
```

E então, para executar o projeto, rode o comando seguinte:

```
npm run buildx
```

Existem outras questões pertinentes e importantes em relação ao React com TypeScript, mas não é do escopo deste artigo falar sobre isso, mas fica a ciência que existem.

## Angular TypeScript

![Angular e Typescript](https://blog-geek-midia.s3.amazonaws.com/wp-content/uploads/2021/05/14102108/angular-typescript.png)Representação da relação entre Angular e Typescript

[Angular](https://blog.geekhunter.com.br/um-overview-sobre-o-framework-angular/) é um framework moderno criado pelo Google construído inteiramente com TypeScript para aplicações Web SPA baseada em componentes.

A documentação do Angular não apenas oferece suporte ao TypeScript como, sendo a sua linguagem primeira, oferece uma referência mais atualizada.

Na utilização do Angular, assim como outros frameworks, é comum a utilização do seu CLI (Command Line Interface). É por ele que iremos criar um projeto Angular.

### Instalação

Para instalar o command line interface do Angular, execute o comando abaixo:

```
npm i -g @angular/cli
```

Para criar um projeto Angular, execute o comando abaixo definindo o nome do seu projeto.

```
ng new <<nome_do_seu_projeto>>
```

Como o Angular é construído com TypeScript, não é preciso de uma configuração prévia e, portanto, já podemos sair programando com o superset no projeto.

## Conclusão

Essa foi uma introdução ao Typescript, você pode conhecer algumas funcionalidades, os motivos de utilizá-lo em determinados momentos e algumas instalações com Angular e React.

Em resumo, o Typescript é uma linguagem que possui uma forte tipagem, fornecendo maior performance e produtividade na hora de se rodar uma aplicação.

Outro ponto é a utilização da orientação à objetos em Javascript, que pode gerar dúvidas e confusão. Com o Typescript isso não ocorre, visto suas propriedades que são mais direcionadas e facilitadas para a programação orientada à objetos!

Espero que tenham gostado e bons estudos! 😀