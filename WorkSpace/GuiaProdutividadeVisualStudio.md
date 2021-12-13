# Guia de produtividade para Visual Studio

- Artigo
- 14/09/2021
- 7 minutos para o fim da leitura
- - [![img](https://github.com/TerryGLee.png?size=32)](https://github.com/TerryGLee)
  - [![img](https://github.com/olprod.png?size=32)](https://github.com/olprod)

Esta página é útil?

Se você quiser economizar tempo enquanto estiver escrevendo código, você está no lugar certo. Este guia de produtividade inclui dicas que podem ajudá-lo a começar a usar o Visual Studio, escrever código, depurar código, tratar erros e usar atalhos de teclado em uma — página.

Para saber mais sobre atalhos de teclado úteis, confira [Atalhos de produtividade](https://docs.microsoft.com/pt-br/visualstudio/ide/productivity-shortcuts?view=vs-2022). Para obter uma lista completa de atalhos de comando, confira [Atalhos de teclado padrão](https://docs.microsoft.com/pt-br/visualstudio/ide/default-keyboard-shortcuts-in-visual-studio?view=vs-2022).

## Introdução

Economize tempo em busca de menus pesquisando rapidamente tudo o que você precisa, incluindo comandos, configurações, documentação e opções de instalação. Consulte atalhos de teclado para comandos em seus resultados de pesquisa Visual Studio para que você possa memorizá-los com mais facilidade.

- **Código de simulação usando a lista de tarefas**. Se você não tiver requisitos suficientes para concluir um trecho de código, use Lista de Tarefas para acompanhar comentários de código que usam tokens como e `TODO` ou tokens personalizados e para gerenciar atalhos que levam você diretamente para um local predefinido no `HACK` código. Para obter mais informações, [consulte Usar o Lista de Tarefas](https://docs.microsoft.com/pt-br/visualstudio/ide/using-the-task-list?view=vs-2022).
- **Use Gerenciador de Soluções atalhos**. Se você for novo no Visual Studio, esses atalhos serão úteis e economizarão tempo enquanto você estiver agilizar uma nova base de código. Para ver a lista completa de atalhos, consulte [Atalhos de teclado padrão no Visual Studio](https://docs.microsoft.com/pt-br/visualstudio/ide/default-keyboard-shortcuts-in-visual-studio?view=vs-2022#bkmk_solutionexplorerGLOBAL).
- **[Identifique e personalize atalhos de teclado Visual Studio](https://docs.microsoft.com/pt-br/visualstudio/ide/identifying-and-customizing-keyboard-shortcuts-in-visual-studio?view=vs-2022)**. Você pode identificar atalhos de teclado para comandos do Visual Studio, personalizar esses atalhos e exportá-los para que outras pessoas os usem. Você sempre pode encontrar e alterar um atalho de teclado na caixa de diálogo Opções.
- **Tornar Visual Studio mais acessível.** O Visual Studio tem recursos internos de acessibilidade que são compatíveis com leitores de tela e outras tecnologias assistenciais. Confira [Dicas e truques de acessibilidade Visual Studio](https://docs.microsoft.com/pt-br/visualstudio/ide/reference/accessibility-tips-and-tricks?view=vs-2022) para ver a lista completa de recursos disponíveis.
- **Confira a caixa Visual Studio ciclo de vida e manutenção do produto.** Para obter informações sobre como obter atualizações do Visual Studio, opções de suporte para clientes do Enterprise e do Professional, suporte para versões mais antigas do Visual Studio e componentes não cobertos pela manutenção do Visual Studio, consulte [Ciclo](https://docs.microsoft.com/pt-br/visualstudio/releases/2019/servicing)de vida e manutenção do produto Visual Studio .
- **Instale e gerencie NuGet pacotes no Visual Studio**. A interface do usuário do Gerenciador de Pacotes do NuGet no Visual Studio no Windows possibilita instalar, desinstalar e atualizar pacotes do NuGet com facilidade em projetos e soluções. Para obter mais informações, [consulte Instalar e gerenciar pacotes no Visual Studio usando o NuGet Gerenciador de Pacotes](https://docs.microsoft.com/pt-br/nuget/consume-packages/install-use-packages-visual-studio).

## Escrever código

Escreva código mais rapidamente usando os seguintes recursos.

- **Usar comandos de conveniência**. O Visual Studio contém vários comandos para ajudar você a realizar tarefas comuns de edição mais rapidamente. Por exemplo, você pode escolher um comando para duplicar com facilidade uma linha de código sem precisar copiá-la, reposicionar o cursor e, em seguida, colá-la. Escolha **Editar** > **Duplicar** ou pressione **Ctrl** + **E**,**V**. Você também pode expandir ou contrair rapidamente uma seleção de texto escolhendo Editar Seleção de Expansão Avançada ou Editar Seleção De Contrato Avançada ou pressionando > > > > **Shift** + **Alt** + **=** ou **Shift** + + **-** Alt.

- **Use o IntelliSense.** À medida que você inserir código no editor, informações do IntelliSense, como Membros da Lista, Informações do Parâmetro, Informações Rápidas, Ajuda de Assinatura e Completar Palavras, serão exibidas. Esses recursos são compatíveis com a correspondência difusa de texto; Por exemplo, as listas de resultados para Listar Membros incluem não apenas entradas que começam com os caracteres inseridos, mas também entradas que contêm a combinação de caracteres em qualquer lugar em seus nomes. Para obter mais informações, confira [Usar o IntelliSense](https://docs.microsoft.com/pt-br/visualstudio/ide/using-intellisense?view=vs-2022).

- **Altere a inserção automática de opções do IntelliSense à medida que você insere o código**. Ao alternar o IntelliSense para o modo de sugestão, você pode especificar que opções do IntelliSense será inseridas somente se você as escolher explicitamente.

  Para habilitar o modo de sugestão, escolha as teclas da barra de espaços **Ctrl** Alt ou, na barra de menus, escolha Editar Modo de Conclusão do + + > **IntelliSense.** >

- **Use snippets de código**. Você pode usar snippets internos ou criar seus próprios snippets.

  Para inserir um snippet, na barra de menus, escolha Editar Snippet de Inserção do > **IntelliSense** ou Cercar com ou abra o menu de atalho em um arquivo e escolha > Snippet inserir **snippet** > ou Cercar com . Para obter mais informações, consulte [Snippets de Código](https://docs.microsoft.com/pt-br/visualstudio/ide/code-snippets?view=vs-2022).

- **Corrija erros de código embutidos**. As Ações Rápidas permitem refatorar, gerar ou, de outro modo, modificar o código de maneira fácil com uma única ação. Essas ações podem ser aplicadas usando o ícone de chave de fenda ou ícones de lâmpada ícones de lâmpada ou pressionando ![ Alt Enter ](https://docs.microsoft.com/pt-br/visualstudio/ide/media/screwdriver-icon.png?view=vs-2022) ou ![ ](https://docs.microsoft.com/pt-br/visualstudio/ide/media/light-bulb-icon.png?view=vs-2022) + **Ctrl** + **.** quando o cursor estiver sobre a linha de código apropriada. Consulte [Ações Rápidas](https://docs.microsoft.com/pt-br/visualstudio/ide/quick-actions?view=vs-2022) para obter mais informações.

- **Exibir e editar a definição de um elemento de código**. Você pode exibir e editar rapidamente o módulo no qual um elemento de código, como um membro, uma variável ou um local, é definido.

  Para abrir uma definição em uma janela pop-up, realça o elemento e, em seguida, escolha as teclas + **Alt F12** ou abra o menu de atalho para o elemento e escolha **Espiar Definição**. Para abrir uma definição em uma janela de código separada, abra o menu de atalho para o elemento de código e então escolha **Ir Para Definição**.

- **Use aplicativos de exemplo**. É possível acelerar o desenvolvimento de aplicativos baixando e instalando aplicativos de exemplo do [Microsoft Developer Network](https://code.msdn.microsoft.com/). Você também pode aprender uma tecnologia em particular ou um conceito baixando e explorando um Sample Pack para essa área.

- **Altere a formatação de chave com Formatação/Novas Linhas**. Use a **página Opções de** formatação para definir opções para formatação de código no editor de códigos, incluindo novas linhas. Para obter mais informações sobre como usar essa configuração em C#, consulte a caixa de diálogo Opções: Editor de [Texto > C# > estilo de](https://docs.microsoft.com/pt-br/visualstudio/ide/reference/options-text-editor-csharp-formatting?view=vs-2022)código > formatação . Para C++, consulte Definir suas preferências de codificação [do C++ no Visual Studio](https://docs.microsoft.com/pt-br/cpp/ide/how-to-set-preferences). Para Python, consulte [Formatar código Python.](https://docs.microsoft.com/pt-br/visualstudio/python/formatting-python-code?view=vs-2022)

- **Altere o recuo com guias**. Use configurações personalizadas do editor, personalizadas para cada base de código, para impor estilos de codificação consistentes para vários desenvolvedores que trabalham no mesmo projeto em diferentes editores e IDEs. Verifique se toda a equipe segue as mesmas convenções de linguagem, convenções de nomenu e regras de formatação. Como essas configurações personalizadas são portáteis e viajam com seu código, você pode impor estilos de codificação mesmo fora do Visual Studio. Para obter mais informações, [consulte Opções, Editor de Texto, Todos os Idiomas, Guias](https://docs.microsoft.com/pt-br/visualstudio/ide/reference/options-text-editor-all-languages-tabs?view=vs-2022#tabs).

## Navegue dentro do código e do IDE

Você pode usar várias técnicas para localizar e mover para locais específicos em seu código com mais rapidez. Você também pode alterar o layout de suas janelas Visual Studio com base em suas preferências.

- **Usar indicadores em linhas de código**. Você pode usar indicadores para navegar rapidamente para linhas específicas do código em um arquivo.

  Para definir um indicador, na barra de menus, **escolha Editar** > **Indicadores** > **Alternar Indicador .** Você pode exibir todos os indicadores para uma solução na janela **Indicadores**. Para obter mais informações, confira [Definir indicadores no código](https://docs.microsoft.com/pt-br/visualstudio/ide/setting-bookmarks-in-code?view=vs-2022).

- **Pesquisar definições de símbolo em um arquivo**. Você pode pesquisar em uma solução para localizar definições de símbolos e nomes de arquivos, mas os resultados da pesquisa não incluirão os namespaces ou as variáveis locais.

  Para acessar esse recurso, na barra de menus, **escolha Editar** > **Navegar para**.

- **Procure a estrutura geral do seu código**. No **Gerenciador de Soluções**, você pode pesquisar e procurar classes e seus tipos e membros em seus projetos. Você também pode pesquisar símbolos, exibir a Hierarquia de Chamada de um método, localizar referências de símbolos e realizar outras tarefas. Se você escolher um elemento de código no **Gerenciador de Soluções**, o arquivo associado será aberto em uma guia **Visualização** e o cursor se moverá para o elemento no arquivo. Para obter mais informações, confira [Exibir a estrutura do código](https://docs.microsoft.com/pt-br/visualstudio/ide/viewing-the-structure-of-code?view=vs-2022).

- **Ir para um local em um arquivo com o modo de mapa**. O modo de mapa exibe linhas de código, em miniatura, na barra de rolagem. Para obter mais informações sobre esse modo de exibição, [consulte Como personalizar a barra de rolagem](https://docs.microsoft.com/pt-br/visualstudio/ide/how-to-track-your-code-by-customizing-the-scrollbar?view=vs-2022#map-mode).

- **Entenda sua estrutura de código com o mapa de código**. Os mapas de código podem ajudá-lo a visualizar dependências em seu código e ver como ele se encaixa sem ler arquivos e linhas de código. Para saber mais, confira [Mapear as dependências com mapas de código](https://docs.microsoft.com/pt-br/visualstudio/modeling/map-dependencies-across-your-solutions?view=vs-2022).

- **Consulte arquivos usados com frequência com Editar/Ir para Arquivo Recente.** Use os comandos Ir para no Visual Studio para executar uma pesquisa focada de seu código para ajudá-lo a encontrar rapidamente os itens especificados. Para obter instruções detalhadas, consulte [Encontrar código usando os comandos Ir para](https://docs.microsoft.com/pt-br/visualstudio/ide/go-to?view=vs-2022).

- **Mova o [janela Propriedades](https://docs.microsoft.com/pt-br/visualstudio/ide/reference/properties-window?view=vs-2022) para o lado direito.** Se você estiver procurando um layout de janela mais familiar, poderá mover o janela Propriedades no Visual Studio pressionando **F4**.

## Localizar itens mais rapidamente

Você pode procurar no IDE comandos, arquivos e opções, bem como filtrar o conteúdo de janelas de ferramenta para mostrar somente as informações relevantes para sua tarefa atual.

- **Filtrar o conteúdo de janelas de ferramentas**. Você pode pesquisar no conteúdo de muitas janelas de ferramentas, como a **Caixa de Ferramentas**, a janela **Propriedades** e o **Gerenciador de Soluções**, mas só poderá exibir itens cujos nomes contenhamos caracteres que você especificar.

- **Exiba apenas os erros que você deseja resolver**. Se você escolher o botão **Filtrar** na barra de ferramentas **Lista de Erros**, poderá reduzir o número de erros que aparecem na janela **Lista de Erros**. Você só pode exibir os erros em arquivos que estão abertos no editor, somente os erros no arquivo atual ou somente os erros no projeto atual. Você também pode pesquisar na janela **Lista de** Erros para encontrar erros específicos.

- **Localizar caixas de diálogo, comandos de menu, opções e mais**. Na caixa de pesquisa, digite as palavras-chave ou frases dos itens que você está tentando localizar. Por exemplo, as seguintes opções aparecerão se você inserir **novo projeto**:

  ![Resultados para o 'novo projeto'](https://docs.microsoft.com/pt-br/visualstudio/ide/media/vs-2019/productivity-quick-launch-new-project.png?view=vs-2022)

  Pressione **Ctrl** + **Q** para ir diretamente para a caixa de pesquisa.

## Depurar o código

A depuração pode consumir muito tempo, mas as dicas a seguir podem ajudar a acelerar o processo.

- **Use as ferramentas Visual Studio do depurador .** No contexto Visual Studio, quando você *depura* seu aplicativo , isso geralmente significa que você está executando o aplicativo no modo de depurador. O depurador fornece várias maneiras de ver o que seu código está fazendo enquanto ele é executado. Consulte [First look at the Visual Studio Debugger](https://docs.microsoft.com/pt-br/visualstudio/debugger/debugger-feature-tour?view=vs-2022) para obter um guia de como começar.

- **Teste a mesma página, aplicativo ou site em navegadores diferentes**. À medida que você depura seu código, poderá facilmente mudar entre os navegadores da Web instalados, incluindo o [Inspetor de Página (Visual Studio)](https://docs.microsoft.com/pt-br/previous-versions/hh974728(v=vs.140)), sem ter que abrir a caixa de diálogo **Procurar Com**. Você pode usar a lista Destino de **Depuração,** que está na barra de ferramentas **Padrão** ao lado do botão Iniciar **Depuração,** para verificar rapidamente qual navegador você está usando ao depurar ou exibir páginas.

  ![Selecionar opções de depuração de navegador da Web](https://docs.microsoft.com/pt-br/visualstudio/ide/media/webbrowserdropdowntoolbar.png?view=vs-2022)

- **Definir pontos de interrupção temporários**. Você pode criar um ponto de interrupção temporário na linha de código atual e iniciar o depurador simultaneamente. Quando você atinge esta linha de código, o depurador entra em modo de interrupção. Para obter mais informações, confira [Navegar pelo código com o depurador](https://docs.microsoft.com/pt-br/visualstudio/debugger/navigating-through-code-with-the-debugger?view=vs-2022).

  Para usar esse recurso, escolha as teclas **Ctrl** + **F10** ou abra o menu de atalho para a linha de código na qual você deseja quebrar e, em seguida, escolha Executar para **o Cursor**.

- **Mover o ponto de execução durante a depuração**. Você pode mover o ponto de execução atual para uma seção de código diferente e então reiniciar a depuração desse ponto. Essa técnica será útil se você quiser depurar uma seção de código sem precisar recriar todas as etapas necessárias para acessar a seção. Para obter mais informações, confira [Navegar pelo código com o depurador](https://docs.microsoft.com/pt-br/visualstudio/debugger/navigating-through-code-with-the-debugger?view=vs-2022).

  Para mover o ponto de execução, arraste a seta amarela para um local em que você deseja definir a próxima instrução no mesmo arquivo de origem e, em seguida, escolha a **tecla F5** para continuar a depuração.

- **Capturar informações de valor de variáveis**. Você pode adicionar um DataTip a uma variável no seu código e fixá-lo para poder acessar o último valor conhecido da variável após a conclusão da depuração. Para obter mais informações, consulte [Exibir valores de dados em Dicas de Dados](https://docs.microsoft.com/pt-br/visualstudio/debugger/view-data-values-in-data-tips-in-the-code-editor?view=vs-2022).

  Para adicionar um DataTip, o depurador deverá estar em modo de interrupção. Coloque o cursor na variável e então escolha o botão de fixação no DataTip em que ele aparece. Quando a depuração é interrompida, um ícone de pino azul aparece no arquivo de origem ao lado da linha de código que contém a variável. Se você apontar para o pino azul, será exibido o valor da variável de sessão de depuração mais recente.

- **Limpar a janela Imediata**. Você pode apagar o conteúdo da janela [Imediata em](https://docs.microsoft.com/pt-br/visualstudio/ide/reference/immediate-window?view=vs-2022) tempo de design inserindo `>cls` ou `>Edit.ClearAll`

  Para obter mais informações sobre comandos adicionais, [consulte Visual Studio aliases de comando](https://docs.microsoft.com/pt-br/visualstudio/ide/reference/visual-studio-command-aliases?view=vs-2022).

- **[Encontre alterações de código e outro histórico com o CodeLens.](https://docs.microsoft.com/pt-br/visualstudio/ide/find-code-changes-and-other-history-with-codelens?view=vs-2022)** O CodeLens permite que você mantenha o foco no trabalho enquanto descobre o que aconteceu com seu código – sem sair do editor. Encontre referências e alterações no código, bugs vinculados, itens de trabalho, revisões de código e testes de unidade.

- **Use Live Share para depurar em tempo real com outras** pessoas. O Live Share permite que você edite e depure em colaboração com outras pessoas em tempo real, sejam quais forem as linguagens de programação usadas ou os tipos de aplicativo criados. Para obter mais informações, consulte [O que é Visual Studio Live Share?](https://docs.microsoft.com/pt-br/visualstudio/liveshare/)

- **Use a Janela Interativa para escrever e testar código pequeno.** Visual Studio fornece uma janela interativa read-evaluate-print-loop (REPL) que permite inserir código arbitrário e ver resultados imediatos. Essa maneira de codificação ajuda você a aprender e experimentar apIs e bibliotecas e desenvolver interativamente o código de trabalho para incluir em seus projetos. Para Python, consulte [Trabalhar com o python Janela interativa](https://docs.microsoft.com/pt-br/visualstudio/python/python-interactive-repl-in-visual-studio?view=vs-2022). O recurso Janela Interativa também está disponível para C#.

## Acessar ferramentas do Visual Studio

Você poderá acessar rapidamente o Prompt de Comando do Desenvolvedor ou outra ferramenta do Visual Studio se você fixá-la no menu Iniciar ou na barra de tarefas.

1. No Windows Explorer, procure *%ProgramData%\Microsoft\Windows\Start Menu\Programs\Visual Studio 2019\Visual Studio Tools*.

1. Clique com botão direito do mouse ou abra o menu de contexto para o **Prompt de Comando do Desenvolvedor** e, em seguida, selecione **Fixar na tela inicial** ou **Fixar na barra de tarefas**.

## Gerenciar arquivos, barras de ferramentas e janelas

A qualquer momento, você pode estar trabalhando em vários arquivos de código e se mover entre várias janelas de ferramenta enquanto desenvolve um aplicativo. Você pode se manter organizado usando as seguintes dicas:

- **Manter arquivos que você usa frequentemente visíveis no editor**. Você pode fixar arquivos no lado esquerdo da guia para que eles permaneçam visíveis, independentemente de quantos arquivos estão abertos no editor.

  Para fixar um arquivo, escolha a guia do arquivo e, em seguida, escolha o botão **Alternar Status do Pino.**

- **Mover documentos e janelas para outros monitores**. Se você usar mais de um monitor quando desenvolver aplicativos, poderá trabalhar em partes do seu aplicativo mais facilmente movendo arquivos que estejam abertos no editor para outro monitor. Você também pode mover janelas de ferramentas, como as de depuração, para outro monitor e encaixar as janelas de documentos e de ferramentas para criar "rafts". Para obter mais informações, consulte [Personalização de layouts de janela no Visual Studio](https://docs.microsoft.com/pt-br/visualstudio/ide/customizing-window-layouts-in-visual-studio?view=vs-2022).

  Você também pode gerenciar arquivos mais facilmente criando outra instância do **Gerenciador de Soluções** e movendo-a para outro monitor. Para criar outra instância do **Gerenciador de Soluções**, abra um menu de atalho no **Gerenciador de Soluções** e então escolha **Novo Modo de Exibição do Gerenciador de Soluções**.

- **Personalizar as fontes que aparecem no Visual Studio**. Você pode alterar o tipo de fonte, a cor e o tamanho usados para o texto no IDE. Por exemplo, você pode personalizar a cor de elementos de código específicos no editor e a fonte em janelas de ferramenta ou por meio do IDE. Para obter mais informações, [consulte Como alterar fontes](https://docs.microsoft.com/pt-br/visualstudio/ide/how-to-change-fonts-and-colors-in-visual-studio?view=vs-2022) e cores e Como alterar fontes e cores no [editor.](https://docs.microsoft.com/pt-br/visualstudio/ide/reference/how-to-change-fonts-and-colors-in-the-editor?view=vs-2022)

## Confira também

- [Postagem no blog de dicas e truques sobre o Visual Studio](https://devblogs.microsoft.com/visualstudio/visual-studio-tips-and-tricks/)
- [Atalhos de teclado padrão para comandos usados com frequência](https://docs.microsoft.com/pt-br/visualstudio/ide/default-keyboard-shortcuts-for-frequently-used-commands-in-visual-studio?view=vs-2022)
- [Como personalizar menus e barras de ferramentas](https://docs.microsoft.com/pt-br/visualstudio/ide/how-to-customize-menus-and-toolbars-in-visual-studio?view=vs-2022)
- [Passo a passo: criar um aplicativo simples](https://docs.microsoft.com/pt-br/visualstudio/get-started/csharp/tutorial-wpf?view=vs-2022)
- [Dicas e truques de acessibilidade](https://docs.microsoft.com/pt-br/visualstudio/ide/reference/accessibility-tips-and-tricks?view=vs-2022)

------

## Conteúdo recomendado

- [Funcionalidades do editor de códigos - Visual Studio (Windows)](https://docs.microsoft.com/pt-br/visualstudio/ide/writing-code-in-the-code-and-text-editor)

  saiba mais sobre os recursos que o editor de código do Visual Studio fornece para facilitar a gravação e o gerenciamento de seu código e texto.

- [Desenvolver o código sem projetos nem soluções - Visual Studio (Windows)](https://docs.microsoft.com/pt-br/visualstudio/ide/develop-code-in-visual-studio-without-projects-or-solutions)

  saiba como desenvolver código diretamente no Visual Studio sem a necessidade de projetos ou soluções.

- [Personalizar o IDE - Visual Studio (Windows)](https://docs.microsoft.com/pt-br/visualstudio/ide/personalizing-the-visual-studio-ide)

  Saiba como personalizar o IDE Visual Studio de maneiras que melhor suportam seu próprio estilo de desenvolvimento e requisitos.

- [Introdução à edição no editor de códigos - Visual Studio (Windows)](https://docs.microsoft.com/pt-br/visualstudio/get-started/tutorial-editor)

  saiba como usar o editor de código em Visual Studio para adicionar código a um arquivo e também como escrever código, navegar até ele e refactoá-lo.