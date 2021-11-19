# Ganhando tempo, rapidez e segurança com o Yarn



### 

Anunciado em 11 de outubro de 2016 pelo Facebook, o Yarn Package Manager é uma evolução do consagrado [npm](https://www.npmjs.com/), o gerenciador de pacotes do Node. O Yarn possui o mesmo funcionamento, até as bibliotecas são as mesmas, porém, ele veio com a proposta de ser muito mais rápido, seguro e confiável que o npm. Abaixo seguem algumas das vantagens que temos ao usar o Yarn:

1. **Rapidez:** Ele realiza caches de todos os pacotes baixados para que não seja preciso baixar de novo. [Alguns benchmarks](https://www.berriart.com/blog/2016/10/npm-yarn-benchmark/) mostram que em alguns casos, ele é até 3x mais rápido!
2. **Segurança:** Usa checksums que verificam a integridade de cada pacote instalado antes que o código seja executado.
3. **Confiabilidade:** Contém um algoritmo determinístico, garantindo que as instalações funcionem igualmente em qualquer sistema.

Além disso, o Yarn possui o inusitado modo offline. Isso significa que se um pacote for instalado anteriormente é possível instalá-lo novamente sem a necessidade de ter conexão com a internet. As dependências são instaladas da mesma maneira em qualquer dispositivo, independente da ordem que forem instaladas. Por fim, ele também resolve versões incompatíveis de dependências de pacotes para uma única versão, evitando criar duplicação.

Fantástico, não acham? Vamos dar uma olhada rápida em como utilizá-lo.

## Instalando e utilizando

Há duas formas de instalação da ferramenta:

1. Pelo [site oficial](https://yarnpkg.com/en/docs/install) do Yarn
2. Por outro gerenciador de pacote, como no caso o npm

A segunda opção é a mais fácil e rápida. Basta executar o seguinte comando para a instalação global na máquina:

```bash
npm install -g yarn
```

A sua utilização é muito semelhante ao que já estamos acostumados no npm. Para inicializar o projeto e gerar o arquivo package.json, por exemplo, basta digitar:

```bash
yarn init
```

Além do package.json, é criado na pasta raíz do projeto e um arquivo yarn.lock, que lista as bibliotecas originais do projeto. Abaixo listarei os comandos para realizar as principais atividades com o Yarn:

**Instalar dependências**

```bash
yarn install
```

**Adicionar uma dependência**

```bash
yarn add (nome do pacote) 
yarn add (nome do pacote @versão)
yarn add (nome do pacote @tag)
```

**Fazer update de um pacote**

```bash
yarn upgrade (nome do pacote) 
yarn upgrade (nome do pacote @versão)
yarn upgrade (nome do pacote @tag)
```

**Remover um pacote**

```bash
yarn remove (nome do pacote) 
```

**Limpar dependências**

```bash
yarn clean
```

Esse comando vasculha as dependências verificando tudo o que não está sendo utilizado e exporta para o arquivo .yarnclean. Quando for executado o yarn install, as dependências serão instaladas de forma mais limpa.

**Atualizar o Yarn**

```bash
yarn self-update
yarn self-update [especificação da versão]
```

Estes são alguns comandos do Yarn, perceba que muitos são parecidos com os do NPM, a diferença só está no nome yarn na frente dos comandos. Portanto, fica muito mais fácil migrar para essa nova poderosa ferramenta! Eu a tenho utilizado nos projetos da empresa e tem sido bastante surpreendente.

E você? Já utilizou o Yarn? Deixa aí nos comentários!

Leia mais sobre o projeto open source Yarn [neste link](https://yarnpkg.com/pt-BR/) e aproveite para contribuir com as suas ideias no [GitHub](https://github.com/yarnpkg/yarn)!



### [BRUNA DE FREITAS ESCUDELARIO](https://imasters.com.br/perfil/brunaescudelario)

### [Executando o PM2 e o Node.js em ambientes de produção](https://imasters.com.br/back-end/executando-o-pm2-e-o-node-js-em-ambientes-de-producao)