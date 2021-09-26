# Typescript: o que é, principais conceitos e porquê usar!

- por[Cairo Noleto](https://blog.betrybe.com/author/cairo-noleto/) - 1 de maio de 2020 - 5 minutos de leitura

Caso você esteja estudando programação web, já deve ter ouvido de Javascript (JS) não é mesmo? Você sabia que existe um superset que busca melhorar ainda mais a produtividade de quem trabalha com o JS? É o **Typescript**.

Criado pela Microsoft em busca de um melhor aproveitamento de características da linguagem, como a tipagem dinâmica do Javascript, essa modificação, conjunto de ferramentas como classes e interfaces a mais, caiu no gosto de [profissionais](https://blog.betrybe.com/carreira/profissional-do-futuro/) de programação, **melhorando o trabalho de descobrir falhas e bugs**.

Neste post, vamos mostrar um pouco mais para você sobre **o que é o Typescript**, quais são os conceitos dessa ferramenta e quais as vantagens que o seu uso pode trazer para pessoas da área de programação. Não perca!

## O que significa Typescript?

Quem desenvolve para a web sabe que é necessário utilizar o Javascript, [HTML](https://blog.betrybe.com/desenvolvimento-web/tudo-que-voce-precisa-saber-sobre-html/) e CSS em seus projetos. Isso pode ser um pouco limitado quando falamos em software de larga escala, uma vez que essa linguagem não provê determinados recursos e características.

Alia-se essa questão ao fato de hoje o Javascript não ser mais uma linguagem exclusiva de cliente. Ela pode ser utilizada no servidor com bastante eficácia, com a aplicação de Node.js, por exemplo, e até mesmo para o desenvolvimento mobile.

Ou seja, nesse novo contexto, o Javascript deixou de ser utilizado em poucas linhas de código no front-end para ser o cerne de muitas [aplicações](https://blog.betrybe.com/carreira/desenvolvedor-de-aplicativos/), utilizando-se paradigmas de programação como a orientação a objetos. Isso exige uma ferramenta que possibilidade um ajuste na linguagem.

É dentro desse cenário que surge o Typescript. Mesmo que algumas pessoas digam que se trata de uma linguagem, isso não é verdade. **Podemos conceituar o Typescript como um superset de Javascript.**

### Relação do Typescript e o Javascript

Ao aplicarmos esse superconjunto, podemos melhorar o suporte a programação orientada a objetos, já que turbinamos o Javascript com várias possibilidades que a linguagem pura não dispõe.

Em sua forma simples, o JS não nos permite a utilização de interfaces de forma clara, por exemplo, além de apresentar uma tipagem fraca, o que prejudica o desenvolvimento em escala de aplicações.

O Typescript visa contornar esses problemas adicionando uma série de funcionalidades, que se perderão, uma vez que o código final se torna Javascript quando transpilado posteriormente.

Porém, durante o desenvolvimento, aquele que programa poderá contar com maiores possibilidades e uma sintaxe mais simples, clara e suportada por todos os editores de códigos modernos.

Como o Typescript é um modificação do JS, **qualquer arquivo que tenha sido escrito com essa extensão, .js, pode ser utilizado dentro do TS diretamente**, uma vez que ele aceita códigos JS por padrão. Isso é muito positivo, pois possibilita a atualização de sistemas construídos em Javascript.

Newsletter da Trybe

Junte-se a mais de 100.000 pessoas da nossa tribo que recebem conteúdos gratuitos e exclusivos em nossa newsletter semanal!

## Quais são os seus principais conceitos?

Ao utilizarmos o Typescript, temos a possibilidade de aplicar aplicar a tipagem estática à [programação](https://blog.betrybe.com/carreira/erros-no-estudo-de-programacao/) juntamente com interfaces em um sistema construído unicamente com Javascript; ou seja, podemos turbinar as nossas aplicações. Entre esses conceitos estão os que listamos abaixo.

### Encapsulamento

O conceito de encapsulamento pode ser entendido como uma forma de estruturação de código para que determinados blocos tenham acesso a pontos específicos para o ambiente externo. Assim, **há visibilidade e acessibilidade dos elementos internos de uma classe**.

Ao aplicarmos o encapsulamento, podemos definir quais são os atributos de uma casse que poderão ser visíveis aos usuários externos ou que estarão expostos para uma interface pública do sistema.

Quem trabalha com linguagens como Java, PHP e C# já está acostumado a declarar atributos privados dentro de suas classes, garantindo esse controle. Vamos a um exemplo em Typescript:

```typescript
private _saldo: number;
```

### Herança

O princípio da herança também é muito conhecido e, com base nele, **uma classe filha pode herdar, ou não, os comportamentos e características de uma classe pai**, sem que seja necessário redefinir todas as funções novamente.

A palavra reservada utilizada para realizar a herança em Typscript é “*extends*” assim como na linguagem Java. É preciso declarar a nova função estendendo-a de outra, conforme o exemplo abaixo:

```typescript
module Escola {
  class Pessoa { ...código aqui.. }
  class Aluno extends Pessoa { ...código aqui.. }
  class Professor extends Pessoa { ...código aqui.. }
}
```

No exemplo acima, temos um módulo escola, no qual todos são pessoas e compartilham determinados atributos, como o CPF. Contudo, existem características específicas, que são únicas de alunos e de professores. **O TS facilita a escrita desse código baseado em herança**, que será compilado posteriormente em JS puro.

### Abstração

A abstração pode ser considerada **a capacidade de destacar apenas algumas características de elementos do mundo real,** e é algo muito utilizado na programação orientada a objetos.

Essas características são agrupadas nas chamadas classes, que representam partes de um elemento e seus atributos para a solução de um determinado problema.

Temos ainda as chamadas “classes abstratas”, que não têm uma representação no mundo real, mas realizam determinadas funções necessárias ao sistema. São as chamadas interfaces.

```typescript
export module Escola
{
   export interface Nota { AlterarNota(nota: number); }
   export class Aluno implements Nota {
       AlterarNota(nota: number) { }
   }
}
```

### Polimorfismo

Por fim, temos o polimorfismo, que permite que sejam utilizados objetos dentro da programação de formas diferenciadas, de acordo com a situação. Ou seja, em um sentido reverso à herança, podemos assumir que uma classe pai possa usar atributos de qualquer de suas classes filhas.

## Quais as vantagens de utilizar Typescript?

São várias as vantagens de adotar o Typescript como uma [ferramenta](https://blog.betrybe.com/ferramentas/tutorial-slack/) de desenvolvimento para quem já trabalha com JS. **Uma das maiores é descobrir erros durante a sua implementação**, uma vez que é possível utilizar o Intellisense da IDE, permitindo visualizar pontos de melhoria e problemas de compilação.

O principal foco do Typescript é trazer a tipagem estática para o Javascript, juntando também alguns features para facilitar a aplicação dos conceitos de OOP também. Porém, é por meio da tipagem que podemos construir aplicações muito mais seguras e manuteníveis, melhorando a [produtividade](https://blog.betrybe.com/carreira/gestao-do-tempo-dicas-essencias/).

**Podemos considerar o Typescript como um potencializador da linguagem Javascript**. Ele permite que grandes sistemas complexos sejam construídos com essa linguagem sem nenhum empecilho e sem que ela deixe a desejar diante de outras linguagens de back-end, como PHP ou Java.

Está começando no mundo da programação e quer saber quanto ganha esse profissional? Temos o post perfeito para você. Saiba em nosso artigo [quanto ganha um profissional de programação](https://blog.betrybe.com/carreira/quanto-ganha-um-programador/)!