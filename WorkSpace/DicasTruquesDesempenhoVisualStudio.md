# Dicas e truques de desempenho do Visual Studio

- Artigo
- 04/10/2021
- 4 minutos para o fim da leitura
- - [![img](https://github.com/TerryGLee.png?size=32)](https://github.com/TerryGLee)
  - [![img](https://github.com/olprod.png?size=32)](https://github.com/olprod)
  - [![img](https://github.com/OpenLocalizationService.png?size=32)](https://github.com/OpenLocalizationService)

Esta página é útil?

As recomendações de desempenho do Visual Studio destinam-se a situações de baixa memória, o que podem ocorrer em casos raros. Nessas situações, é possível otimizar determinados recursos do Visual Studio que você talvez não esteja usando. As dicas a seguir não devem ser consideradas como as recomendações gerais.

 Observação

Se você estiver tendo dificuldades para usar o produto devido a problemas de memória, nos avise por meio da ferramenta [de comentários](https://docs.microsoft.com/pt-br/visualstudio/ide/how-to-report-a-problem-with-visual-studio?view=vs-2022).

## Usar um sistema operacional de 64 bits

Se você atualizar seu sistema de uma versão de 32 bits do Windows para uma versão de 64 bits, expanda a quantidade de memória virtual disponível para o Visual Studio de 2 GB para 4 GB. Isso permite que o Visual Studio lide com cargas de trabalho significativamente maiores, mesmo sendo um processo de 32 bits.

Para obter mais informações, consulte [Limites de memória](https://docs.microsoft.com/pt-br/windows/desktop/Memory/memory-limits-for-windows-releases) e [Usar /LARGEADDRESSAWARE no Windows de 64 bits](https://blogs.msdn.microsoft.com/oldnewthing/20050601-24/?p=35483/).

 Dica

Visual Studio 2022 no Windows agora é um aplicativo de 64 bits. Isso significa que você pode abrir, editar, executar e depurar até mesmo as soluções maiores e mais complexas sem ficar sem memória. Para saber mais, confira as postagens no blog [Visual Studio 2022 e](https://devblogs.microsoft.com/visualstudio/visual-studio-2022/) [Visual Studio 2022 Preview 1.](https://devblogs.microsoft.com/visualstudio/visual-studio-2022-preview-1-now-available/)

## Desabilitar a restauração de arquivo automática

O Visual Studio reabre automaticamente os documentos que foram deixados abertos na sessão anterior. Isso pode prolongar o tempo necessário para carregar uma solução em até 30% ou mais, dependendo do tipo de projeto e dos documentos sendo abertos. Designers como o Windows Forms e o XAML e alguns arquivos JavaScript e typescript, podem demorar para abrir.

O Visual Studio notifica você em uma barra amarela quando a restauração automática de documentos está fazendo com que a solução seja carregada de maneira significativamente mais lenta. Você pode desabilitar a reabertura de arquivo automática seguindo estas etapas:

1. Selecione **Opções** > **de Ferramentas** para abrir a caixa de **diálogo** Opções.
2. Na página **Projetos e Solução** > **Geral,** desmarque Reabrir documentos no carregamento da **solução**.

Caso você desabilite a restauração automática de arquivos, uma maneira rápida de navegar para os arquivos que deseja abrir é usar um dos comandos [Ir para](https://docs.microsoft.com/pt-br/visualstudio/ide/go-to?view=vs-2022):

- Para a funcionalidade **Ir para** general, selecione **Editar** > **Ir para** > **Ir para Todos** ou pressione **Ctrl**+**T**.
- Vá para o último local de edição em uma solução usando **Editar** Ir para Ir para o Local da Última Edição ou pressionando > > **Ctrl** + **Shift** + **Backspace**.
- Use **Ir Para Arquivo Recente** para ver uma lista dos arquivos visitados recentemente em uma solução. Selecione **Editar** > **Ir para** Ir para Arquivo > **Recente** ou pressione **Ctrl** + **1,** **Ctrl** + **R.**

## Configurar as opções de depuração

Se você tem ficado com pouca memória durante as sessões de depuração normalmente, você pode otimizar o desempenho fazendo uma ou mais alterações de configuração.

- **Habilitar Apenas Meu Código**

  A otimização mais simples é habilitar o recurso **Apenas Meu Código**, que só carrega símbolos para o seu projeto. Habilitar esse recurso pode resultar em uma economia significativa de memória para depurar aplicativos gerenciados (.NET). Esta opção já fica habilitada por padrão em alguns tipos de projeto.

  Para habilitar o **Apenas Meu Código**, escolha **Ferramentas** > **Opções** > **Depuração** > **Geral** e selecione **Habilitar Apenas Meu Código**.

- **Especificar os símbolos a serem carregados**

  Para depuração nativa, carregar arquivos de símbolo (*.pdb*) é caro em termos de recursos de memória. Você pode definir as configurações de símbolo de depuração para economizar memória. Normalmente, você pode configurar a solução para carregar somente os módulos do seu projeto.

  Para especificar o carregamento de símbolos, **escolha Opções** > **de Ferramentas** > **Depurando** > **Símbolos**.

  Defina as opções para **Somente os módulos especificados** em vez de **Todos os módulos** e, em seguida, especifique quais módulos você deseja carregar. Durante a depuração, você também pode clicar com o botão direito do mouse em módulos específicos na janela **Módulos** para incluir explicitamente um módulo no carregamento de símbolo. (Para abrir a janela durante a depuração, escolha **Depurar** > **Windows** > **Módulos**.)

  Para obter mais informações, consulte [Noções básicas sobre arquivos de símbolo](https://docs.microsoft.com/pt-br/visualstudio/ide/visual-studio-performance-tips-and-tricks?view=vs-2019&preserve-view=true).

- **Desabilitar Ferramentas de Diagnóstico**

  É recomendável desabilitar a criação de perfil de CPU após o uso. Esse recurso pode consumir grandes quantidades de recursos. Quando a criação de perfil de CPU está habilitada, esse estado é mantido nas sessões de depuração subsequentes, por isso vale a pena desativá-lo explicitamente após terminar. Você pode economizar alguns recursos desabilitando as ferramentas de diagnóstico durante a depuração se você não precisar dos recursos fornecidos.

  Para desabilitar o **Ferramentas de Diagnóstico**, inicie uma sessão de depuração, selecione Opções de Ferramentas Depuração Geral e desmarque a opção Habilitar Ferramentas de Diagnóstico durante a > > > **depuração.**

  Para obter mais informações, consulte [Ferramentas de Criação de Perfil](https://docs.microsoft.com/pt-br/visualstudio/profiling/profiling-feature-tour?view=vs-2022).

## Desabilitar ferramentas e extensões

Algumas ferramentas ou extensões podem ser desabilitadas para melhorar o desempenho.

 Dica

Geralmente, é possível isolar problemas de desempenho desativando as extensões, uma por vez e verificando novamente o desempenho.

### Serviço de linguagem gerenciado (Roslyn)

Para obter mais informações sobre as considerações de desempenho do .NET Compiler Platform (“Roslyn"), consulte [Considerações de desempenho para grandes soluções](https://github.com/dotnet/roslyn/blob/master/docs/wiki/Performance-considerations-for-large-solutions.md).

- **Desabilitar a análise completa da solução**

  O Visual Studio executa a análise em toda a sua solução para proporcionar uma experiência avançada sobre os erros antes de invocar um build. Esse recurso é útil para identificar erros assim que possível. No entanto, para soluções grandes, esse recurso pode consumir recursos significativos de memória. Se você estiver tendo problemas semelhantes ou pressão de memória, desabilite essa experiência para liberar esses recursos. Por padrão, essa opção é habilitada para o Visual Basic e desabilitada para C#.

  Para desabilitar a **Análise Completa da Solução**, escolha **Ferramentas** > **Opções** > **Editor de Texto** e selecione **Visual Basic** ou **C#**. Escolha **Avançado** e desmarque **Habilitar análise de solução completa**.

- **Desabilitar CodeLens**

  O Visual Studio executa uma tarefa **Localizar todas as referências** em cada método como exibido. O CodeLens fornece recursos como a exibição embutida do número de referências. O trabalho é executado em um processo separado como *ServiceHub.RoslynCodeAnalysisService32*. Em soluções grandes ou em sistemas com recursos restritos, esse recurso pode afetar significativamente o desempenho. Se estiver enfrentando problemas de memória, por exemplo, ao carregar uma solução grande em um computador de 4 GB, ou alta utilização da CPU para esse processo, você poderá desabilitar o CodeLens para liberar recursos.

  Para desabilitar o **CodeLens**, escolha **Ferramentas** > **Opções** > **Editor de Texto** > **Todas as Linguagens** > **CodeLens** e desmarque o recurso.

   Observação

  O CodeLens está disponível nas edições Professional e Enterprise do Visual Studio.

### Outras ferramentas e extensões

- **Desabilitar extensões**

  Extensões são componentes de software adicionais acrescentados ao Visual Studio que fornecem uma funcionalidade nova ou estendem a funcionalidade existente. Extensões geralmente podem ser uma fonte de problemas de recursos de memória. Se você estiver tendo problemas de recursos de memória, tente desabilitar as extensões, uma por vez, para ver como ele afeta o cenário ou o fluxo de trabalho.

  Para desabilitar extensões, acesse **Extensões** > **Gerenciar Extensões** e desabilite uma extensão específica.

- **Desabilitar o modo de mapa**

  [**O modo de**](https://docs.microsoft.com/pt-br/visualstudio/ide/how-to-track-your-code-by-customizing-the-scrollbar?view=vs-2022#display-modes) mapa exibe linhas de código, em miniatura, na barra de rolagem. O modo de mapa está habilitado por padrão.

  Para desabilitar o modo de mapa, acesse Ferramentas Opções Editor de Texto Todas as Barras de Rolagem de Idiomas e, na seção > > > > Comportamento, desmarque a opção Usar modo de mapa para barra de **rolagem vertical.**

- **Desabilitar quebra de linha**

  [**Quebra de**](https://docs.microsoft.com/pt-br/visualstudio/ide/reference/how-to-manage-word-wrap-in-the-editor?view=vs-2022) linha exibe a parte de uma longa linha de código que se estende além da largura atual da janela do editor de código. O quebra-texto está em por padrão.

  Para desabilitar o quebra-texto de um projeto em que você está trabalhando no momento, vá para **Editar** > **Quebra Avançada** do > **Word**. (Você pode alternar essa configuração usando os mesmos comandos de menu.)

  Para desabilitar o quebra-texto para todos os projetos, acesse Ferramentas Opções Geral Editor de Texto Geral Todas as Linguagens Geral e, na seção > > > > > Configurações, desmarque a opção Quebra de linha do Word.

- **Desabilitar o XAML Designer**

  O designer XAML está habilitado por padrão, mas só consumirá recursos se você abrir um *arquivo .xaml.* Se você trabalha com arquivos XAML, mas não quer usar a funcionalidade do designer, desabilite esse recurso para liberar memória.

  Para desabilitar Designer XAML, acesse Opções de > > **Ferramentas Designer XAML** > **Habilitar Designer XAML** e desmarque a opção.

- **Remover as cargas de trabalho**

  Você pode usar o Instalador do Visual Studio para remover as cargas de trabalho que não são mais usadas. Esta ação pode simplificar o custo de inicialização e do runtime ignorando pacotes e assemblies que não são mais necessários.

- **Adicionar arquivos não rastreados ao .gitignore local**

  Visual Studio executa o comando Git com arquivos não rastreados para fornecer uma experiência perfeita ao adicionar `git status` novos arquivos a um repositório. Quando há um grande número de arquivos não rastreados, `git status` o pode consumir memória extra. Para ignorar esses arquivos e melhorar o desempenho do , você pode adicionar esses arquivos ou pastas `git status` ao arquivo .gitignore local. Para acessar o arquivo, acesse **Git** > **Configurações** > **Repositório Git Configurações**. Em seguida, na seção **arquivos git** , clique em **Adicionar** para criar um arquivo. Gitignore ou clique em **Editar** se você já tiver um.

## Forçar uma coleta de lixo

O CLR usa um sistema de gerenciamento de memória de coleta de lixo. Nesse sistema, às vezes a memória é usada pelos objetos que não são mais necessários. Esse estado é temporário. O coletor de lixo liberará esta memória com base em seu desempenho e a heurística de uso de recursos. Você pode forçar o CLR a coletar a memória não utilizada usando uma tecla de atalho no Visual Studio. Se houver uma quantidade significativa de lixo aguardando pela coleta e você forçar uma coleta de lixo, você deverá ver o uso de memória da queda de *devenv.exe* processo no **Gerenciador de tarefas**. Raramente é necessário usar esse método. No entanto, após uma operação cara (como um build completo, sessão de depuração ou um evento de abertura de solução), ele pode ajudar a determinar a quantidade de memória que realmente está sendo usado pelo processo. Como o Visual Studio é misto (gerenciado e nativo), geralmente é possível que o alocador nativo e o coletor de lixo disputem pelos recursos de memória limitada. Em condições de alto uso de memória, pode ser útil forçar o coletor de lixo a ser executado.

Para forçar uma coleta de lixo, use a tecla de atalho: **Ctrl** + **ALT** + **Shift** + **F12**, **Ctrl** + **ALT** + **Shift** + **F12** (pressione-a duas vezes).

Se forçar a coleta de lixo de forma confiável faz seu cenário funcionar, relate isso na ferramenta de comentários do Visual Studio, pois esse comportamento provavelmente trata-se de um bug.

Para ver uma descrição detalhada do coletor de lixo CLR, consulte [Noções básicas da coleta de lixo](https://docs.microsoft.com/pt-br/dotnet/standard/garbage-collection/fundamentals).

## Confira também

- [Otimizar o desempenho do Visual Studio](https://docs.microsoft.com/pt-br/visualstudio/ide/optimize-visual-studio-performance?view=vs-2022)
- [Load solutions faster (Carregar soluções mais rapidamente) (blog do Visual Studio)](https://devblogs.microsoft.com/visualstudio/load-solutions-faster-with-visual-studio-2017-version-15-6/)

------

## Conteúdo recomendado

- [Melhorar o desempenho se o Visual Studio estiver lento](https://docs.microsoft.com/pt-br/visualstudio/ide/optimize-visual-studio-performance)

  saiba como melhorar o desempenho de Visual Studio se você achar que ele está em execução lentamente.

- [Melhorar o tempo de inicialização - Visual Studio (Windows)](https://docs.microsoft.com/pt-br/visualstudio/ide/optimize-visual-studio-startup-time)

  Saiba como controlar as configurações de extensões e janelas de ferramentas na caixa de diálogo Gerenciar Visual Studio Desempenho para melhorar Visual Studio tempo de início.

- [Notas sobre a versão do Visual Studio 2019 versão 16.0](https://docs.microsoft.com/pt-br/visualstudio/releases/2019/release-notes-v16.0)

  Obtenha informações sobre os recursos da versão, o suporte e as correções de bugs mais recentes do Visual Studio 2019 v16.0. Baixe hoje mesmo.

- [Visual Studio notas sobre a versão 2019 versão 16.11](https://docs.microsoft.com/pt-br/visualstudio/releases/2019/release-notes)

  Obter os recursos mais recentes, correções de bugs e suporte para Visual Studio 2019 v16.11. Baixe hoje mesmo.

Mostrar mais