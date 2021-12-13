

![Como usar TypeScript com Node.js](https://www.luiztools.com.br/wp-content/uploads/2020/10/typescript.jpeg)

#### NODE.JS

# Como usar TypeScript com Node.js

![Luiz Duarte](https://www.gravatar.com/avatar/93a9abccc4d85eefdb90b62bd810342e?d=mm&s=128)

Escrito por [**Luiz Duarte**](https://www.luiztools.com.br/post/author/luiztools/)em 14/10/2020



***Este tutorial tem versão em videoaula no meu [curso Web FullStack JS](https://www.luiztools.com.br/curso-fullstack?utm_source=google&utm_medium=cpc&utm_campaign=12231680300&utm_content=115851466463&utm_term=como usar typescript&gclid=CjwKCAiA-9uNBhBTEiwAN3IlNMci-JMX5gd-zinK4il10jyxhNQNBZ2mQw8s6c-fy1cYZyVB0yrApRoC_5YQAvD_BwE)!***

No tutorial de hoje eu quero lhe ensinar o básico de TypeScript.

TypeScript cresceu muito nos últimos anos e cada vez mais empresas têm adotado ele como um padrão para uso com JavaScript em escala corporativa pelos benefícios que ele traz em termos de organização e padronização de código, além de segurança e qualidade.

Embora seja uma tecnologia polêmica, uma vez que tira parte da produtividade e liberdade fornecida pela tipagem dinâmica, é certo que para grandes projetos e/ou grandes times os seus benefícios no médio e longo prazo superam o drawback no curto prazo.

Mas afinal, o que é TypeScript?

Se preferir, ao invés de ler este artigo, assista a esse vídeo. Ao final do artigo, tem outros para você se aprofundar.

<iframe loading="lazy" id="_ytid_34545" width="480" height="360" data-origwidth="480" data-origheight="360" src="https://www.youtube.com/embed/g0hkeyMb45U?enablejsapi=1&amp;autoplay=0&amp;cc_load_policy=0&amp;cc_lang_pref=&amp;iv_load_policy=1&amp;loop=0&amp;modestbranding=0&amp;rel=0&amp;fs=1&amp;playsinline=0&amp;autohide=2&amp;theme=dark&amp;color=red&amp;controls=1&amp;" class="__youtube_prefs__  epyt-is-override  no-lazyload" title="YouTube player" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen="" data-no-lazy="1" data-skipgform_ajax_framebjll="" data-gtm-yt-inspected-1_19="true" style="box-sizing: border-box; margin: 0px; padding: 0px; border: 0px; font: inherit; vertical-align: baseline; outline: 0px; text-decoration: none; position: absolute; left: 0px; top: 0px; width: 700px; height: 406px;"></iframe>





































### O que é TypeScript?

TypeScript é um superset para JavaScript, ou um conjunto adicional de instruções, keywords e estruturas, criado pela Microsoft.

Ou seja, você ainda estará programando JavaScript, mas com “super poderes”.

E que super poderes são essas?

O primeiro, mais direto e mais simples é a tipagem estática, muito comum em linguagens como Java, C e derivados, mas algo que passa longe do JavaScript geralmente.

Mas TypeScript vai muito além disso, adicionando várias outras validações, oferecendo suporte a Generics, interfaces e muito mais, além de estender enormemente as possibilidades do uso de [classes em JS](https://www.luiztools.com.br/post/como-criar-classes-em-javascript-es6-e-node-js/).

Note que todos estes benefícios são em tempo de codificação, pois em produção, você terá o bom e velho JS sendo transpilado a partir do TypeScript novamente.

### #1- Instalando e testando TypeScript

O primeiro passo é você instalar o compilador do TypeScript na sua máquina. Claro, aqui considerando que você já tem o Node.js instalado.

Você pode fazer isso facilmente instalando a dependência do mesmo de maneira global via NPM (não esqueça que você precisa ter permissões de administrador).

| 1    | **npm** install -g typescript |
| ---- | ----------------------------- |
|      |                               |

Para verificar se foi instalado corretamente, você pode criar um arquivo qualquer com a extensão .ts (de TypeScript) e tentar compilá-lo usando o utilitário tsc, como abaixo:

| 1    | **tsc** app.ts |
| ---- | -------------- |
|      |                |

Como resultado, deve aparecer um arquivo de mesmo nome na mesma pasta, mas com a extensão .js. Você irá executar esta compilação sempre que mexer em seu código TS e queira gerar a sua contraparte JS, para poder testar.

Além de fazer esta tradução (chamada transpilação na verdade), o uso de TS vai lhe ajudar com code-complete em ferramentas como VS Code.

No arquivo com extensão .TS você pode utilizar o superset para definir tipagem do seu código JS. Os tipos disponíveis nativamente no JavaScript são:

- number: números inteiros e decimais, positivos e negativos;
- string: textos;
- boolean: true ou false;
- array: conjuntos de elementos;
- object: tipos complexos, que podem ter propriedades personalizadas;

E é com esse último tipo que o TypeScript mostra todo o seu poder.

[![img](https://www.luiztools.com.br/wp-content/uploads/2021/05/banner-curso-bot.jpg)](https://www.luiztools.com.br/curso-beholder?utm_source=google&utm_medium=cpc&utm_campaign=12231680300&utm_content=115851466463&utm_term=como usar typescript&gclid=CjwKCAiA-9uNBhBTEiwAN3IlNMci-JMX5gd-zinK4il10jyxhNQNBZ2mQw8s6c-fy1cYZyVB0yrApRoC_5YQAvD_BwE)

### #2 – Usando tipagem em parâmetros

Para começarmos a usar TypeScript, vamos fazer alguns exemplos práticos bem simples.

Primeiro, crie um arquivo app.ts e insira um código JS como abaixo:

| 1234567 | //app.ts**function** somar(num1, num2){  **return** num1 + num2;} console.log(somar(1,2));console.log(somar('1','2')); |
| ------- | ------------------------------------------------------------ |
|         |                                                              |

Note que este é um código JavaScript perfeitamente normal e que o uso errôneo da função somar com strings funciona em JS, embora o resultado seja completamente diferente da soma tradicional.

Não esqueça de compilar com o tsc antes de testar com o Node.js no terminal.

Agora, vamos colocar a tipagem nos parâmetros desta função somar. Para adicionar tipagem a um parâmetro é bem simples, basta usar :tipo depois do nome da variável, como abaixo.

| 1234567 | //app.ts**function** somar(num1: number, num2: number){  **return** num1 + num2;} console.log(somar(1,2));console.log(somar('1','2')); |
| ------- | ------------------------------------------------------------ |
|         |                                                              |

No momento que você fizer isso, a sua ferramenta de editor de código já vai reclamar do uso errado na segunda chamada do somar. E, se mesmo assim, você quiser tentar compilar, vai dar erro no console.

![Erro TS](https://www.luiztools.com.br/wp-content/uploads/2020/10/erro-ts-720x174.png)

Ou seja, o TS vai nos ajudar a evitar erro de tipagem em tempo de codificação, o que é muito melhor do que descobrir esses usos errados de funções em produção, não é mesmo?

Mas agora, se você remover a chamada errada da função somar, mandar compilar com o tsc e depois olhar o JS gerado, verá que não há nada demais, que o código JS é exatamente o que você faria sem tipagem.

Ou seja, na prática, o resultado final não é nada diferente do que você faria sem o TypeScript, sendo os maiores ganhos durante o desenvolvimento mesmo, principalmente em grandes projetos e/ou com várias pessoas, onde a falta de tipagem pode virar bagunça.

<iframe class="mailmunch-embedded-iframe mailmunch-embedded-iframe-17db433f21f547c" title="Typescript" frameborder="0" scrolling="no" allowtransparency="true" data-gtm-yt-inspected-1_19="true" style="box-sizing: border-box; margin: 0px; padding: 0px; border: 0px; font: inherit; vertical-align: baseline; outline: 0px; text-decoration: none; opacity: 1 !important; visibility: visible !important; background: transparent; width: 1349px; height: 0px; max-height: 0px;"></iframe>

Um truque que vale a pena mencionar aqui é para conversão de strings para numbers nos parâmetros de função. Basta usar o sinal de ‘+’ antes da variável string para transformá-la em number, como abaixo.

| 123  | **const** var1 = "2";**const** var2 = "3";somar(+var1, +var2); |
| ---- | ------------------------------------------------------------ |
|      |                                                              |

Legal, né?

[![Curso Node.js e MongoDB](https://www.luiztools.com.br/wp-content/uploads/2020/08/curso-nodejs-e1618510190832.png)](https://www.luiztools.com.br/curso-nodejs?utm_source=google&utm_medium=cpc&utm_campaign=12231680300&utm_content=115851466463&utm_term=como usar typescript&gclid=CjwKCAiA-9uNBhBTEiwAN3IlNMci-JMX5gd-zinK4il10jyxhNQNBZ2mQw8s6c-fy1cYZyVB0yrApRoC_5YQAvD_BwE)

### #3 – Retornos e inferência de tipos

Além dos parâmetros, você pode usar tipagem no retorno de funções, sendo tão simples quanto no primeiro exemplo, bastando adicionar :tipo ao final da assinatura da função e antes de abrir chaves.

| 123  | **function** dividir(num1: number, num2: number): number{  **return** num1 / num2;} |
| ---- | ------------------------------------------------------------ |
|      |                                                              |

No exemplo acima, além dos parâmetros terem de ser numéricos, o retorno também o será.

Experimente tentar colocar uma concatenação com string no return e você verá que tanto o VS Code quanto o tsc vão te xingar que você não pode retornar uma string, que deve ser um number.

Esse conceito de tipagem de retorno é importante para entender outro conceito que é o de inferência de tipos.

Inferência de tipos é quando o compilador define o tipo de uma variável a partir da atribuição de valor realizado sobre ela. Isso já é feito no JS normal, afinal ele até faz isso várias vezes mesmo com tipos diferentes e somente no caso de const que ele não deixa ficar mudando o tipo. Na verdade ele não deixa mudar o valor né, e a restrição no tipo acaba sendo um bônus.

Mas no TS esse poder sobe um nível.

Com TypeScript, quando uma função possui um tipo explícito, a inferência de tipos fica ainda mais poderosa uma vez que estamos falando de uma linguagem tipada.

Assim sendo, no código abaixo, a variável resultado é do tipo number, com certeza e o VS Code sabe disso antes mesmo da execução deste programa.

| 12345 | **function** dividir(num1: number, num2: number): number{  **return** num1 / num2;} **const** resultado = dividir(4,2); |
| ----- | ------------------------------------------------------------ |
|       |                                                              |

![Inferência](https://www.luiztools.com.br/wp-content/uploads/2020/10/inferencia-de-tipo-720x183.png)

Normalmente, o interpretador JS só saberia o tipo desta const em produção, durante a execução daquela linha de código. Aqui temos esta inferência em tempo de código.

Outro ponto legal a respeito da inferência de tipos com TS é que ele possui suporte nativo a muitos elementos nativos do JS, incluindo as APIs de DOM, facilitando muito a codificação de front-end também.

[![img](https://www.luiztools.com.br/wp-content/uploads/2021/06/banner-ebooks-node.jpg)](https://www.luiztools.com.br/mongodb-ou-mysql/)

### #4 – Typecasting e configuração

Em alguns casos a inferência de tipos não vai lhe ajudar.

Seja porque o tipo retornado por uma função é muito genérico, seja porque a função não tem tipo de retorno definido.

Em ambos os casos, se você sabe o que será retornado, você pode usar typecasting ou conversão de tipo.

Para fazer isso, você usa o operador ‘as’ logo depois da chamada da function, citando o tipo a ser convertido logo a sequência.

| 12345 | **function** multiplicar(num1, num2){  **return** num1 * num2;} **const** resultado2 = multiplicar(2,3) **as** number; |
| ----- | ------------------------------------------------------------ |
|       |                                                              |

Isso garantirá que resultado2, será um number. Claro, se a conversão for possível, caso contrário dará erro, então tome cuidado com esse recurso.

Falando em conversões e falhas, e no caso de null? Como que o TS nos ajuda com referências de objetos que podem ser nulas?

Para acionarmos mais alguns poderes do TS temos de adicionar um arquivo de configuração em nosso projeto. Você faz isso usando o comando abaixo na pasta do projeto:

| 1    | **tsc** --init |
| ---- | -------------- |
|      |                |

Com isso, será criado um arquivo tsconfig.json, como abaixo.

| 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869 | { "compilerOptions": {  /* Visit https://aka.ms/tsconfig.json to read more about this file */   /* Basic Options */  // "incremental": true,          /* Enable incremental compilation */  "target": "es5",             /* Specify ECMAScript target version: 'ES3' (default), 'ES5', 'ES2015', 'ES2016', 'ES2017', 'ES2018', 'ES2019', 'ES2020', or 'ESNEXT'. */  "module": "commonjs",           /* Specify module code generation: 'none', 'commonjs', 'amd', 'system', 'umd', 'es2015', 'es2020', or 'ESNext'. */  // "lib": [],               /* Specify library files to be included in the compilation. */  // "allowJs": true,            /* Allow javascript files to be compiled. */  // "checkJs": true,            /* Report errors in .js files. */  // "jsx": "preserve",           /* Specify JSX code generation: 'preserve', 'react-native', or 'react'. */  // "declaration": true,          /* Generates corresponding '.d.ts' file. */  // "declarationMap": true,        /* Generates a sourcemap for each corresponding '.d.ts' file. */  // "sourceMap": true,           /* Generates corresponding '.map' file. */  // "outFile": "./",            /* Concatenate and emit output to single file. */  // "outDir": "./",            /* Redirect output structure to the directory. */  // "rootDir": "./",            /* Specify the root directory of input files. Use to control the output directory structure with --outDir. */  // "composite": true,           /* Enable project compilation */  // "tsBuildInfoFile": "./",        /* Specify file to store incremental compilation information */  // "removeComments": true,        /* Do not emit comments to output. */  // "noEmit": true,            /* Do not emit outputs. */  // "importHelpers": true,         /* Import emit helpers from 'tslib'. */  // "downlevelIteration": true,      /* Provide full support for iterables in 'for-of', spread, and destructuring when targeting 'ES5' or 'ES3'. */  // "isolatedModules": true,        /* Transpile each file as a separate module (similar to 'ts.transpileModule'). */   /* Strict Type-Checking Options */  "strict": **true**,              /* Enable all strict type-checking options. */  // "noImplicitAny": true,         /* Raise error on expressions and declarations with an implied 'any' type. */  // "strictNullChecks": true,       /* Enable strict null checks. */  // "strictFunctionTypes": true,      /* Enable strict checking of function types. */  // "strictBindCallApply": true,      /* Enable strict 'bind', 'call', and 'apply' methods on functions. */  // "strictPropertyInitialization": true, /* Enable strict checking of property initialization in classes. */  // "noImplicitThis": true,        /* Raise error on 'this' expressions with an implied 'any' type. */  // "alwaysStrict": true,         /* Parse in strict mode and emit "use strict" for each source file. */   /* Additional Checks */  // "noUnusedLocals": true,        /* Report errors on unused locals. */  // "noUnusedParameters": true,      /* Report errors on unused parameters. */  // "noImplicitReturns": true,       /* Report error when not all code paths in function return a value. */  // "noFallthroughCasesInSwitch": true,  /* Report errors for fallthrough cases in switch statement. */   /* Module Resolution Options */  // "moduleResolution": "node",      /* Specify module resolution strategy: 'node' (Node.js) or 'classic' (TypeScript pre-1.6). */  // "baseUrl": "./",            /* Base directory to resolve non-absolute module names. */  // "paths": {},              /* A series of entries which re-map imports to lookup locations relative to the 'baseUrl'. */  // "rootDirs": [],            /* List of root folders whose combined content represents the structure of the project at runtime. */  // "typeRoots": [],            /* List of folders to include type definitions from. */  // "types": [],              /* Type declaration files to be included in compilation. */  // "allowSyntheticDefaultImports": true, /* Allow default imports from modules with no default export. This does not affect code emit, just typechecking. */  "esModuleInterop": **true**,         /* Enables emit interoperability between CommonJS and ES Modules via creation of namespace objects for all imports. Implies 'allowSyntheticDefaultImports'. */  // "preserveSymlinks": true,       /* Do not resolve the real path of symlinks. */  // "allowUmdGlobalAccess": true,     /* Allow accessing UMD globals from modules. */   /* Source Map Options */  // "sourceRoot": "",           /* Specify the location where debugger should locate TypeScript files instead of source locations. */  // "mapRoot": "",             /* Specify the location where debugger should locate map files instead of generated locations. */  // "inlineSourceMap": true,        /* Emit a single file with source maps instead of having a separate file. */  // "inlineSources": true,         /* Emit the source alongside the sourcemaps within a single file; requires '--inlineSourceMap' or '--sourceMap' to be set. */   /* Experimental Options */  // "experimentalDecorators": true,    /* Enables experimental support for ES7 decorators. */  // "emitDecoratorMetadata": true,     /* Enables experimental support for emitting type metadata for decorators. */   /* Advanced Options */  "skipLibCheck": **true**,           /* Skip type checking of declaration files. */  "forceConsistentCasingInFileNames": **true** /* Disallow inconsistently-cased references to the same file. */ }} |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |

Eu não vou explicar aqui cada uma das configurações, até porque a maioria delas está documentada nos comentários do próprio arquivo.

Mas uma que eu gostaria de frisar aqui é a “strict”: true, que é altamente recomendada que seja deixada assim, mas que ao mesmo tempo é a mais xarope de todas, isso porque ela reforça regras de segurança no código, como o cuidado a variáveis nulas e a tipos não especificados.

Se você tiver algum trecho de código que possa retornar null e com isso estourar uma exceção em produção, o compilador do TS não vai deixar você avançar antes de implementar um teste para ver se o valor não é null primeiro.

Outra situação em que o strict mode vai te incomodar é com a declaração de tipos que deixará de ser opcional e passará a ser obrigatória. Caso você, por algum motivo, ainda queira que uma variável, parâmetro ou retorno de função tenha tipagem dinâmica, você pode usar o tipo ‘any’ para ele.

E por hoje é só. A parte 2 você encontra [neste link](https://www.luiztools.com.br/post/como-usar-typescript-com-node-js-2/).