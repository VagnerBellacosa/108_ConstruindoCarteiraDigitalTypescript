# Técnicas e ferramentas de depuração para ajudá-lo a escrever um código melhor

- Artigo
- 14/10/2021
- 7 minutos para o fim da leitura
- - [![img](https://github.com/Mikejo5000.png?size=32)](https://github.com/Mikejo5000)
  - [![img](https://github.com/olprod.png?size=32)](https://github.com/olprod)

Esta página é útil?

Corrigir bugs e erros em seu código pode ser demorado e, às vezes, frustrante– tarefa. Leva tempo para aprender a depurar com eficiência, mas um IDE poderoso como Visual Studio pode tornar seu trabalho muito mais fácil. Um IDE pode ajudá-lo a corrigir erros e depurar seu código mais rapidamente e não apenas isso, mas também pode ajudá-lo a escrever um código melhor com menos bugs. Nosso objetivo neste artigo é dar uma visão holística do processo de "correção de bugs", para que você saiba quando usar o analisador de código, quando usar o depurador, como corrigir exceções e como codificar para intenção. Se você já sabe que precisa usar o depurador, confira [Primeira olhada no depurador](https://docs.microsoft.com/pt-br/visualstudio/debugger/debugger-feature-tour?view=vs-2022).

Neste artigo, falamos sobre como aproveitar o IDE para tornar suas sessões de codificação mais produtivas. Tocamos em várias tarefas, como:

- Preparar seu código para depuração aproveitando o analisador de código do IDE
- Como corrigir exceções (erros em tempo de executar)
- Como minimizar bugs codificando a intenção (usando assert)
- Quando usar o depurador

Para demonstrar essas tarefas, mostramos alguns dos tipos mais comuns de erros e bugs que você encontrará ao tentar depurar seus aplicativos. Embora o código de exemplo seja C#, as informações conceituais geralmente são aplicáveis ao C++, Visual Basic, JavaScript e outras linguagens com suporte do Visual Studio (exceto quando for anotou). As capturas de tela estão em C#.

## Criar um aplicativo de exemplo com alguns bugs e erros nele

O código a seguir tem alguns bugs que você pode corrigir usando o Visual Studio IDE. O aplicativo aqui é um aplicativo simples que simula obter dados JSON de alguma operação, desserlizar os dados para um objeto e atualizar uma lista simples com os novos dados.

Para criar o aplicativo:

1. Você deve ter Visual Studio e a carga de trabalho de desenvolvimento de plataforma cruzada **do .NET Core** instalada.

   Se você ainda não tiver instalado o Visual Studio, acesse a página [Visual Studio downloads](https://visualstudio.microsoft.com/downloads/) para instalá-lo gratuitamente.

   Se você precisar instalar a carga de trabalho, mas já tiver Visual Studio, clique em **Ferramentas** > **Obter Ferramentas e Recursos**. O Instalador do Visual Studio é iniciado. Escolha a carga de trabalho desenvolvimento de plataforma cruzada do **.NET Core** e, em seguida, **escolha Modificar**.

2. Abra o Visual Studio.

   Na janela inicial, escolha **Criar um novo projeto.** Digite **console** na caixa de pesquisa e escolha Aplicativo **de Console** para .NET Core. Escolha **Próxima**. Digite um nome de projeto **como Console_Parse_JSON** clique em **Próximo** **ou Criar**, qualquer opção disponível.

   Para o .NET Core, escolha a estrutura de destino recomendada ou o .NET 6 e, em seguida, **escolha Criar**.

   Se você não vir o modelo de projeto Aplicativo de **Console** para .NET Core, acesse Ferramentas Obter Ferramentas e Recursos , que abre o > Instalador do Visual Studio. Escolha a carga de trabalho desenvolvimento de plataforma cruzada do **.NET Core** e, em seguida, **escolha Modificar**.

   O Visual Studio criará o console do projeto, que será aberto no Gerenciador de Soluções no painel direito.

3. Substitua o código padrão no arquivo *Program.cs* do projeto pelo código de exemplo abaixo.

C#Copiar

```csharp
using System;
using System.Collections.Generic;
using System.Runtime.Serialization.Json;
using System.Runtime.Serialization;
using System.IO;

namespace Console_Parse_JSON
{
    class Program
    {
        static void Main(string[] args)
        {
            var localDB = LoadRecords();
            string data = GetJsonData();

            User[] users = ReadToObject(data);

            UpdateRecords(localDB, users);

            for (int i = 0; i < users.Length; i++)
            {
                List<User> result = localDB.FindAll(delegate (User u) {
                    return u.lastname == users[i].lastname;
                    });
                foreach (var item in result)
                {
                    Console.WriteLine($"Matching Record, got name={item.firstname}, lastname={item.lastname}, age={item.totalpoints}");
                }
            }

            Console.ReadKey();
        }

        // Deserialize a JSON stream to a User object.
        public static User[] ReadToObject(string json)
        {
            User deserializedUser = new User();
            User[] users = { };
            MemoryStream ms = new MemoryStream(Encoding.UTF8.GetBytes(json));
            DataContractJsonSerializer ser = new DataContractJsonSerializer(users.GetType());

            users = ser.ReadObject(ms) as User[];

            ms.Close();
            return users;
        }

        // Simulated operation that returns JSON data.
        public static string GetJsonData()
        {
            string str = "[{ \"points\":4o,\"firstname\":\"Fred\",\"lastname\":\"Smith\"},{\"lastName\":\"Jackson\"}]";
            return str;
        }

        public static List<User> LoadRecords()
        {
            var db = new List<User> { };
            User user1 = new User();
            user1.firstname = "Joe";
            user1.lastname = "Smith";
            user1.totalpoints = 41;

            db.Add(user1);

            User user2 = new User();
            user2.firstname = "Pete";
            user2.lastname = "Peterson";
            user2.totalpoints = 30;

            db.Add(user2);

            return db;
        }
        public static void UpdateRecords(List<User> db, User[] users)
        {
            bool existingUser = false;

            for (int i = 0; i < users.Length; i++)
            {
                foreach (var item in db)
                {
                    if (item.lastname == users[i].lastname && item.firstname == users[i].firstname)
                    {
                        existingUser = true;
                        item.totalpoints += users[i].points;

                    }
                }
                if (existingUser == false)
                {
                    User user = new User();
                    user.firstname = users[i].firstname;
                    user.lastname = users[i].lastname;
                    user.totalpoints = users[i].points;

                    db.Add(user);
                }
            }
        }
    }

    [DataContract]
    internal class User
    {
        [DataMember]
        internal string firstname;

        [DataMember]
        internal string lastname;

        [DataMember]
        // internal double points;
        internal string points;

        [DataMember]
        internal int totalpoints;
    }
}
```

## Encontre os botões vermelho e verde!

Antes de tentar iniciar o aplicativo de exemplo e executar o depurador, verifique o código no editor de códigos para ver se há alternâncias em vermelho e verde. Eles representam erros e avisos identificados pelo analisador de código do IDE. Os botões vermelhos são erros de tempo de compilação, que você deve corrigir antes de executar o código. Os botões verdes são avisos. Embora você geralmente possa executar seu aplicativo sem corrigir os avisos, eles podem ser uma fonte de bugs e você geralmente economiza tempo e problemas investigando-os. Esses avisos e erros também aparecem na janela **Lista** de Erros, se você preferir uma exibição de lista.

No aplicativo de exemplo, você verá várias alternâncias vermelhas que você precisa corrigir e uma verde que você verá. Este é o primeiro erro.

![Erro mostrando como um squiggle vermelho](https://docs.microsoft.com/pt-br/visualstudio/debugger/media/write-better-code-red-squiggle.png?view=vs-2022)

Para corrigir esse erro, você verá outro recurso do IDE, representado pelo ícone de lâmpada.

## Verifique a lâmpada!

A primeira alternância vermelha representa um erro de tempo de compilação. Passe o mouse sobre ele e você verá a mensagem `The name `Encoding` does not exist in the current context` .

Observe que esse erro mostra um ícone de lâmpada no canto inferior esquerdo. Junto com o ícone de chave de fenda ícone de chave de fenda, o ícone de lâmpada ícone de lâmpada representa Ações Rápidas que podem ajudá-lo a corrigir ou ![ ](https://docs.microsoft.com/pt-br/visualstudio/ide/media/screwdriver-icon.png?view=vs-2022) ![ ](https://docs.microsoft.com/pt-br/visualstudio/ide/media/light-bulb-icon.png?view=vs-2022) refactor o código em linha. A lâmpada representa problemas que você *deve* corrigir. A chave de fenda é para problemas que você pode optar por corrigir. Use a primeira correção sugerida para resolver esse erro clicando **usando System.Text** à esquerda.

![Usar a lâmpada para corrigir o código](https://docs.microsoft.com/pt-br/visualstudio/debugger/media/write-better-code-missing-include.png?view=vs-2022)

Quando você clica nesse item, Visual Studio adiciona a instrução na parte superior do arquivo `using System.Text` *Program.cs* e a alternância vermelha desaparece. (Quando você não tem certeza do que uma correção sugerida fará, escolha o **link** Visualizar alterações à direita antes de aplicar a correção.)

O erro anterior é um erro comum que você geralmente corrige adicionando uma nova `using` instrução ao seu código. Há vários erros comuns e semelhantes a esse, como Esses tipos de erros podem indicar uma referência de assembly ausente (clique com o botão direito do mouse no projeto, escolha Adicionar Referência ), um nome com erro de ortização ou uma biblioteca ausente que você precisa adicionar `The type or namespace `Name` cannot be found.` > (para C#, clique com o botão direito do mouse no projeto e escolha Gerenciar **pacotes NuGet**).

## Corrigir os erros e avisos restantes

Há mais algumas alternâncias para ver neste código. Aqui, você verá um erro de conversão de tipo comum. Ao passar o mouse sobre a alternância, você verá que o código está tentando converter uma cadeia de caracteres em um int, o que não tem suporte, a menos que você adicione código explícito para fazer a conversão.

![Erro de conversão de tipo](https://docs.microsoft.com/pt-br/visualstudio/debugger/media/write-better-code-conversion-error.png?view=vs-2022)

Como o analisador de código não consegue adivinhar sua intenção, não há lâmpadas para ajudá-lo neste momento. Para corrigir esse erro, você precisa saber a intenção do código. Neste exemplo, não é muito difícil ver que deve ser um valor numérico (inteiro), pois você está tentando `points` `points` adicionar a `totalpoints` .

Para corrigir esse erro, `points` altere o membro da `User` classe deste:

C#Copiar

```csharp
[DataMember]
internal string points;
```

para isto:

C#Copiar

```csharp
[DataMember]
internal int points;
```

As linhas vermelha esquiquisa no editor de códigos vão embora.

Em seguida, passe o mouse sobre a linha de alternância verde na declaração do membro `points` de dados. O analisador de código informa que a variável nunca recebe um valor.

![Mensagem de aviso para variável não atribuída](https://docs.microsoft.com/pt-br/visualstudio/debugger/media/write-better-code-warning-message.png?view=vs-2022)

Normalmente, isso representa um problema que precisa ser corrigido. No entanto, no aplicativo de exemplo, você está, na verdade, armazenar dados na variável durante o processo de desserialização e, em seguida, adicionar esse valor ao `points` `totalpoints` membro de dados. Neste exemplo, você sabe a intenção do código e pode ignorar o aviso com segurança. No entanto, se você quiser eliminar o aviso, poderá substituir o seguinte código:

C#Copiar

```csharp
item.totalpoints = users[i].points;
```

por este:

C#Copiar

```csharp
item.points = users[i].points;
item.totalpoints += users[i].points;
```

A alternância verde desaparecerá.

## Corrigir uma exceção

Quando você tiver corrigido todas as alternâncias vermelhas e resolvidas, ou pelo menos investigadas, todas as alternâncias verdes, você estará pronto para iniciar o depurador e executar o aplicativo.

Pressione **F5** (**Depurar > Iniciar Depuração**) ou o botão Iniciar **Depuração** Iniciar ![Depuração](https://docs.microsoft.com/pt-br/visualstudio/debugger/media/dbg-tour-start-debugging.png?view=vs-2022) na barra de ferramentas Depurar.

Neste ponto, o aplicativo de exemplo lança uma `SerializationException` exceção (um erro de runtime). Ou seja, o aplicativo se desfoque nos dados que está tentando serializar. Como você iniciou o aplicativo no modo de depuração (anexado ao depurador), o Auxiliar de Exceção do depurador leva você até o código que lançou a exceção e fornece uma mensagem de erro útil.

![Ocorre uma SerializationException](https://docs.microsoft.com/pt-br/visualstudio/debugger/media/write-better-code-serialization-exception.png?view=vs-2022)

A mensagem de erro instrui você de que o valor não pode `4o` ser analisado como um inteiro. Portanto, neste exemplo, você sabe que os dados são ruins: `4o` deve ser `40` . No entanto, se você não estiver no controle dos dados em um cenário real (digamos que você os está recebendo de um serviço Web), o que você fará sobre isso? Como consertar isso?

Quando você atinge uma exceção, precisa fazer (e responder) algumas perguntas:

- Essa exceção é apenas um bug que você pode corrigir? Ou,
- Essa exceção é algo que os usuários podem encontrar?

Se for o primeiro, corrige o bug. (No aplicativo de exemplo, isso significa corrigir os dados ruins.) Se for o último, talvez seja necessário lidar com a exceção em seu código usando um bloco (vamos ver outras estratégias `try/catch` possíveis na próxima seção). No aplicativo de exemplo, substitua o seguinte código:

C#Copiar

```csharp
users = ser.ReadObject(ms) as User[];
```

por este código:

C#Copiar

```csharp
try
{
    users = ser.ReadObject(ms) as User[];
}
catch (SerializationException)
{
    Console.WriteLine("Give user some info or instructions, if necessary");
    // Take appropriate action for your app
}
```

Um bloco tem algum custo de desempenho, portanto, você só deseja usá-los quando realmente precisar deles, ou seja, onde (a) eles podem ocorrer na versão de lançamento do aplicativo e em que (b) a documentação do método indica que você deve verificar a exceção (supondo que a documentação está `try/catch` concluída!). Em muitos casos, você pode lidar com uma exceção adequadamente e o usuário nunca precisará saber mais sobre ela.

Aqui estão algumas dicas importantes para tratamento de exceções:

- Evite usar um bloco catch vazio, como , que não toma a `catch (Exception) {}` ação apropriada para expor ou tratar um erro. Um bloco catch vazio ou não informativo pode ocultar exceções e tornar seu código mais difícil de depurar em vez de mais fácil.

- Use o `try/catch` bloco em torno da função específica que lança a exceção ( `ReadObject` , no aplicativo de exemplo). Se você usá-lo em torno de uma parte maior do código, acabará ocultando o local do erro. Por exemplo, não use o bloco em torno da chamada para a função pai , mostrado aqui ou você não sabe exatamente onde `try/catch` `ReadToObject` a exceção ocorreu.

  C#Copiar

  ```csharp
  // Don't do this
  try
  {
      User[] users = ReadToObject(data);
  }
  catch (SerializationException)
  {
  }
  ```

- Para funções desconhecidas que você inclui em seu aplicativo, especialmente aquelas que interagem com dados externos (como uma solicitação da Web), verifique a documentação para ver quais exceções a função provavelmente lançará. Essas informações podem ser críticas para o tratamento de erro adequado e para depurar seu aplicativo.

Para o aplicativo de exemplo, `SerializationException` corrige o `GetJsonData` no método alterando `4o` para `40` .

## Esclarecer sua intenção de código usando assert

Clique no **botão Reiniciar** ![Reiniciar Aplicativo](https://docs.microsoft.com/pt-br/visualstudio/debugger/media/dbg-tour-restart.png?view=vs-2022) na barra de ferramentas de depuração (**Ctrl** + **Shift** + **F5**). Isso reinicia o aplicativo em menos etapas. Você verá a saída a seguir na janela do console.

![Valor nulo na saída](https://docs.microsoft.com/pt-br/visualstudio/debugger/media/write-better-code-using-assert-null-output.png?view=vs-2022)

Você pode ver algo nessa saída que não está correto. **name** e **lastname** para o terceiro registro estão em branco!

Esse é um bom momento para falar sobre uma prática de codificação útil, geralmente subutilizada, que é usar instruções `assert` em suas funções. Ao adicionar o código a seguir, você inclui uma verificação de runtime para garantir que `firstname` e `lastname` não sejam `null` . Substitua o seguinte código no `UpdateRecords` método :

C#Copiar

```csharp
if (existingUser == false)
{
    User user = new User();
    user.firstname = users[i].firstname;
    user.lastname = users[i].lastname;
```

por este:

C#Copiar

```csharp
// Also, add a using statement for System.Diagnostics at the start of the file.
Debug.Assert(users[i].firstname != null);
Debug.Assert(users[i].lastname != null);
if (existingUser == false)
{
    User user = new User();
    user.firstname = users[i].firstname;
    user.lastname = users[i].lastname;
```

Ao adicionar `assert` instruções como esta às suas funções durante o processo de desenvolvimento, você pode ajudar a especificar a intenção do código. No exemplo anterior, especificamos o seguinte:

- Uma cadeia de caracteres válida é necessária para o nome
- Uma cadeia de caracteres válida é necessária para o sobrenome

Especificando a intenção dessa forma, você impõe seus requisitos. Esse é um método simples e útil que você pode usar para surgir bugs durante o desenvolvimento. ( `assert` As instruções também são usadas como o elemento principal em testes de unidade.)

Clique no **botão Reiniciar** ![Reiniciar Aplicativo](https://docs.microsoft.com/pt-br/visualstudio/debugger/media/dbg-tour-restart.png?view=vs-2022) na barra de ferramentas de depuração (**Ctrl** + **Shift** + **F5**).

 Observação

O `assert` código está ativo somente em um build de Depuração.

Quando você reinicia, o depurador pausa na instrução , porque `assert` a expressão é avaliada como em vez de `users[i].firstname != null` `false` `true` .

![Assert é resolvido como false](https://docs.microsoft.com/pt-br/visualstudio/debugger/media/write-better-code-using-assert.png?view=vs-2022)

O `assert` erro informa que há um problema que você precisa investigar. `assert` pode abranger muitos cenários em que você não necessariamente vê uma exceção. Neste exemplo, o usuário não verá uma exceção e um `null` valor será adicionado como na lista de `firstname` registros. Isso pode causar problemas posteriormente (como você vê na saída do console) e pode ser mais difícil de depurar.

 Observação

Em cenários em que você chama um método no `null` valor , um `NullReferenceException` resultado. Normalmente, você deseja evitar o uso de um bloco para uma exceção geral, ou seja, uma exceção que não está vinculada à `try/catch` função de biblioteca específica. Qualquer objeto pode lançar um `NullReferenceException` . Verifique a documentação da função de biblioteca se você não tiver certeza.

Durante o processo de depuração, é bom manter uma instrução específica até que você saiba que precisa `assert` substituí-la por uma correção de código real. Digamos que você decida que o usuário pode encontrar a exceção em um build de versão do aplicativo. Nesse caso, você deve refactor o código para garantir que seu aplicativo não lança uma exceção fatal ou resulte em algum outro erro. Portanto, para corrigir esse código, substitua o seguinte código:

C#Copiar

```csharp
if (existingUser == false)
{
    User user = new User();
```

por este código:

C#Copiar

```csharp
if (existingUser == false && users[i].firstname != null && users[i].lastname != null)
{
    User user = new User();
```

Usando esse código, você atende aos seus requisitos de código e garante que um registro com um valor ou de `firstname` não seja adicionado aos `lastname` `null` dados.

Neste exemplo, adicionamos as duas `assert` instruções dentro de um loop. Normalmente, ao usar , é melhor adicionar instruções no ponto de entrada `assert` `assert` (início) de uma função ou método. No momento, você está observando o `UpdateRecords` método no aplicativo de exemplo. Nesse método, você sabe que está com problemas se um dos argumentos do método for , portanto, verifique ambos com uma instrução no ponto de entrada `null` `assert` da função.

C#Copiar

```csharp
public static void UpdateRecords(List<User> db, User[] users)
{
    Debug.Assert(db != null);
    Debug.Assert(users != null);
```

Para as instruções anteriores, sua intenção é que você carregue dados existentes ( ) e recupere novos dados ( ) antes `db` `users` de atualizar qualquer coisa.

Você pode usar `assert` com qualquer tipo de expressão que resolva para ou `true` `false` . Portanto, por exemplo, você pode adicionar uma `assert` instrução como esta.

C#Copiar

```csharp
Debug.Assert(users[0].points > 0);
```

O código anterior será útil se você quiser especificar a seguinte intenção: um novo valor de ponto maior que zero (0) será necessário para atualizar o registro do usuário.

## Inspecionar seu código no depurador

OK, agora que você corrigiu tudo o que está errado com o aplicativo de exemplo, você pode passar para outras coisas importantes!

Mostramos o Auxiliar de Exceção do depurador, mas o depurador é uma ferramenta muito mais poderosa que também permite que você faça outras coisas, como passar pelo código e inspecionar suas variáveis. Esses recursos mais avançados são úteis em muitos cenários, especialmente os seguintes:

- Você está tentando isolar um bug de runtime em seu código, mas não consegue fazer isso usando métodos e ferramentas discutidos anteriormente.

- Você deseja validar seu código, ou seja, observe-o enquanto ele é executado para garantir que ele está se comportando da maneira esperada e fazendo o que você deseja.

  É instrutivo observar seu código enquanto ele é executado. Você pode aprender mais sobre seu código dessa maneira e geralmente pode identificar bugs antes que eles manifestem quaisquer sintomas óbvios.

Para saber como usar os recursos essenciais do depurador, consulte [Depuração para iniciantes absolutos.](https://docs.microsoft.com/pt-br/visualstudio/debugger/debugging-absolute-beginners?view=vs-2022)

## Corrigir problemas de desempenho

Bugs de outro tipo incluem código ineficiente que faz com que seu aplicativo seja executado lentamente ou use muita memória. Em geral, otimizar o desempenho é algo que você faz posteriormente no desenvolvimento do aplicativo. No entanto, você pode encontrar problemas de desempenho no início (por exemplo, você vê que alguma parte do seu aplicativo está em execução lenta) e talvez seja necessário testar seu aplicativo com as ferramentas de criação de perfil no início. Para obter mais informações sobre ferramentas de criação de perfil, como a ferramenta Uso da CPU e o Analisador de Memória, consulte Primeira análise [das ferramentas de criação de perfil](https://docs.microsoft.com/pt-br/visualstudio/profiling/profiling-feature-tour?view=vs-2022).

## Próximas etapas

Neste artigo, você aprendeu a evitar e corrigir muitos bugs comuns em seu código e quando usar o depurador. Em seguida, saiba mais sobre como usar o Visual Studio depurador para corrigir bugs.

[Depuração para iniciantes absolutos](https://docs.microsoft.com/pt-br/visualstudio/debugger/debugging-absolute-beginners?view=vs-2022)

------

## Conteúdo recomendado

- [Depurando código para iniciantes absolutos - Visual Studio (Windows)](https://docs.microsoft.com/pt-br/visualstudio/debugger/debugging-absolute-beginners)

  Se você estiver depurando pela primeira vez, conheça alguns princípios para ajudá-lo a executar seu aplicativo no modo de depuração com o Visual Studio

- [Introdução ao depurador - Visual Studio (Windows)](https://docs.microsoft.com/pt-br/visualstudio/debugger/debugger-feature-tour)

  Introdução à depuração de aplicativos usando o depurador do Visual Studio

- [O que é depuração? - Visual Studio (Windows)](https://docs.microsoft.com/pt-br/visualstudio/debugger/what-is-debugging)

  Entender o que significa depurar um aplicativo

- [Navegar no código com o depurador - Visual Studio (Windows)](https://docs.microsoft.com/pt-br/visualstudio/debugger/navigating-through-code-with-the-debugger)

  Saiba como usar o depurador Visual Studio para solucionar problemas de seu código. Os tópicos incluem a inserção do modo de quebra, o passo a passo do código e a execução para um destino.

Mostrar mais