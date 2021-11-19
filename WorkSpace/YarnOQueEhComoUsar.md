[Fundamentos de Programação](https://blog.cod3r.com.br/category/fundamentos-de-programacao/)

 18/03/2021 1069 [ 0](https://blog.cod3r.com.br/yarn-o-que-e-como-usar/#comments)

# Yarn – O que é? Como usar?

Todos já devem ter usado o **npm** para instalar alguma dependência em seu projeto ***[frontend](https://blog.cod3r.com.br/category/desenvolvimento-web/)***, pois ele é o gerenciador de pacotes mais popular no momento. No entanto, ele é a causa de dores de cabeça em muitos desenvolvedores, por causa do conflito de dependências, versão do **npm** desatualizada, entrave em alguma dependência entre outros problemas.

Pensando nisso, o **Yarn** é um gerenciador de pacotes mais simples e ágil, que garante um controle maior sobre o que está sendo instalado no projeto.

## O que é Yarn?

**Yarn** é uma alternativa para o gerenciador de pacotes mais clássico que temos. Mas não é só! Ele também é bem mais rápido para uma série de tarefas, pois traz algumas técnicas que não estão presentes no **npm**, como por exemplo:

- Um cache local guarda a versão exata da dependência. Ou seja, se no futuro você baixá-la novamente, utilizará a versão que está no cache, atualizando apenas se necessário. Atualmente, o **npm** tem algo semelhante, mas não é tão performático quanto o **Yarn**

- Coloca as dependências diretamente no **package.json**, dispensando uma **flag** (**-s** por exemplo) para garantir que elas serão escritas corretamente
- Ao instalar as dependências do projeto, ele sempre seguirá uma ordem determinada, fazendo com que todo processo seja bem mais rápido
- Continua utilizando a mesma estrutura já conhecida com o **package.json**, logo a adaptação é bem tranquila

Com isso em mente, vamos partir para a parte mais legal! Vamos ver na prática como funciona um projeto com **Yarn**.

## Como o Yarn funciona?

Antes de mais nada, é preciso instalar o **Yarn** na sua máquina. É bem simples, basta usar o seguinte comando:

```
npm install -g yarn
```

Agora, se quisermos realmente instalar nossas dependências, precisamos criar o **package.json** e para isso vamos usar o seguinte comando:

```
yarn init
```

Para instalar as dependências em si, use este comando:

```
yarn add [nome-pacote]
```

Finalmente, use o seguinte comando para instalar todas as dependências do projeto e criar o **node_modules**:

```
yarn install
```

Pronto! Agora você já sabe o que é o **Yarn** e como dar os primeiros passos com essa belezinha. Agora você já pode analisar qual vale mais a pena e qual vai usar em seus futuros projetos.

Bons estudos!

## Referências

[Documentação](https://yarnpkg.com/getting-started)

[Yarn: A new package manager for JavaScript](https://engineering.fb.com/2016/10/11/web/yarn-a-new-package-manager-for-javascript/)