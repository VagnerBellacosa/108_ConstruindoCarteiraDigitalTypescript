# Quem tem medo do TypeScript?

![img](https://secure.gravatar.com/avatar/dc7c6804f4f8333b3d4b4105bb38e711?s=96&d=mm&r=g)### Por Luiz Gonçalves -  Publicado em 23 de junho de 2021 - ![img](https://blog.impulso.network/wp-content/uploads/2021/06/clock.svg)3 min de leitura

![TypeScript](https://blog.impulso.network/wp-content/uploads/2021/06/Quem-tem-medo-do-TypeScript-Blog-Impulso.jpg)

**Você usa TypeScript?** Ou faz parte do grupo de pessoas desenvolvedoras que possuem medo de utilizá-lo? Se é do segundo time, atenção: **você pode estar perdendo oportunidades incríveis** em suas atividades no dia a dia.

Trazemos aqui algumas das principais reflexões que o **William Grasel** *(desenvolvedor web, Google Developers Expert e coordenador do AngularSP)* compartilhou conosco em uma [talk incrível](https://www.youtube.com/watch?v=J9OoXt1dvm8), que tivemos aqui na Impulso, sobre TypeScript. Vamos juntos neste processo? ![🚀](https://s.w.org/images/core/emoji/13.1.0/svg/1f680.svg)

## **Por que as pessoas têm medo do TypeScript?**

![img](https://blog.impulso.network/wp-content/uploads/2021/06/por-que-temer-o-TypeScript-Blog-Impulso-1024x683.jpg)

Fato é: muitas pessoas ficam muito relutantes em incorporar TypeScript com JavaScript, criando um verdadeiro medo de seu uso. Muitos especialistas argumentam:

“Ah, mas já tentaram fazer isso no ES4 e não deu certo”.

Mas, afinal, **quem disse que foi isso o responsável pelos problemas do ECMAScript 4?** Ele também tinha uma série de problemas presentes ali que foram responsáveis pelo seu fracasso, como diversos bugs e falhas de retrocompatibilidade *– uma falha vital para projetos de JavaScript.*

Fato é que temos, desde então, **novas tentativas de tipagem**. Por exemplo:

- Google Closure Compiler + JSDocs *(tipagem na própria documentação)*;
- ECMAScript Typed Objects Proposal *(proposta para retorno da tipagem, mas ainda está em passos iniciais e lentos para este fim)*;
- Web Assembly + SIMD.js *(possui tipos de baixo nível)*;
- Microsoft TypeScript;
- Facebook Flow.

## **O que é o TypeScript?**

![O que é TypeScript](https://blog.impulso.network/wp-content/uploads/2021/06/typescript-o-que-e-Impulso-1024x472.png)

O TypeScript surgiu pela Microsoft, em formato **Open Source**. O **Typed Superset** possui algumas **especificações importantes**, tais como:

- **Todo JavaScript válido deve ser um TypeScript válido**, ou seja, não pode ter itens que conflitem diretamente com a linguagem. Ou seja, não precisa aprender uma linguagem nova;
- Ele promete ser **fiel ao futuro do ECMAScript**;
- **Todas as features extras são estritamente opcionais**, ou seja, você não é obrigado a usar nenhuma delas;
- **Funciona como Transpiler** *(transcrição de um JavaScript moderno com todas as switchers e transpila para uma versão mais antiga)* **e Bundler** *(uso de vários arquivos, unificando-os em poucos arquivos, a fim de fazer um download mais inteligente na máquina do usuário)*, como Babel;
- **Edita seu código o mínimo possível** ao transpilar;
- **Focado no ferramental e análise estatística de código**;
- **Facilita o refactor e o crescimento** de grandes bases de código.

## **Quem está usando TypeScript?**

![TypeScript quem está usando](https://blog.impulso.network/wp-content/uploads/2021/06/Google-e-TypeScript-Blog-Impulso.jpg)

Enquanto há muitas pessoas desenvolvedoras que estão relutantes no uso do Type, outros estão **investindo pesado para seu uso**. Entre eles:

- **Google** *(é uma das 5 linguagens oficiais)*;
- Empresas como **Airbnb**, **Reddit**, **Paypal** e **Lyft**, que realizaram ou estão realizando a migração de JavaScrip para TypeScript;
- Há registros de **mais de 200 mil projetos cadastrados Open Source** no Github que utilizam Type;
- **Frameworks Web**, como Angular, Ember, Vue, Aurelia, Cycle.js;
- Frameworks [**Mobile**](https://blog.impulso.network/desenvolvimento-de-app-mobile-dicas-para-entrar-nessa-area/), como Ionic, NativeScript;
- **Desktop Apps**, como VS Code, Slack.

Assim, é **uma das linguagens mais amadas** por pessoas desenvolvedoras ![🧡](https://s.w.org/images/core/emoji/13.1.0/svg/1f9e1.svg), segundo *Stack Overflow Survey*.

## **Então, como perder o medo do TypeScript?**

![img](https://blog.impulso.network/wp-content/uploads/2021/06/como-perder-o-medo-do-TypeScript-Blog-Impulso-1-1024x683.jpg)

Diante disso, o **William Grasel** propõe **5 passos** que tornarão o seu conhecimento sobre Type mais suave, **evitando processos traumáticos.** *Are you ready?*

1. **Purista:** você pode usar JavaScript/ECMAScript puro, sem tipar nada, sem usar nenhuma feature. Seu uso será semelhante ao Babel para transpilling e bundling da sua aplicação. Também não é preciso usar a extensão .ts, podendo utilizar .js, .jsx, .vue, entre outros. Com isso, você ganha em IntelliSense e inferência de tipos
2. **Introdutório:** comece a tipar algumas variáveis de entrada e saída de funções. Deixe o TypeScript te ajudar, oferecendo informações extras;
3. **Intermediário:** comece a criar e implemente interface de dados, o que permite ganhar ainda mais IntelliSense e garante proteção de grandes estruturas de dados. Importante lembrar que trata-se de **interface de dados**, e não de objetos, por isso não se assemelha a #C ou Java;
4. **Avançado:** passe a navegar por features mais avançadas. Então entenda e aproveite ao máximo os tipos “genéricos”. Conheça o conteúdo de um Array, Promisse ou um Observer antes mesmo de executarem;
5. **GodMod:** comece a ativar todas as flags de segurança disponíveis, bem como mantenha-se agindo de forma segura.

Com esses passos, você consegue fazer uma aproximação do TypeScript e perder o medo de utilizá-lo **sem receios**. **Aproveite essas dicas imperdíveis do William Grasel** e não deixe as oportunidades passarem devido a isso! 