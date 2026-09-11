---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/interface/preferences-window/project-settings.html"
breadcrumb-title: ''
description: Defina as configurações do projeto nas preferências do Substance 3D Designer para personalizar o comportamento padrão do projeto.
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences window > Project settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Configurações do projeto
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9297416d538a70b80b8be3b2d23a3c442a79a23b
workflow-type: tm+mt
source-wordcount: '2687'
ht-degree: 1%

---


# Configurações do projeto

Esta página apresenta as <b>configurações de projetos</b> no [Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html) e as configurações contidas nele.

O Substance 3D Designer permite criar preferências *por projeto* e compartilhá-las entre estações de trabalho. Essas preferências podem ser encontradas na guia <b>Projetos</b> da janela [Preferências](../../../interface/preferences-window/preferences-window.md).

Isso é muito útil se você quiser configurar um ambiente de trabalho comum para uma equipe que trabalha no mesmo projeto, usando o arquivo de projeto *igual* em *todos* sistemas.

>[!NOTE]
>
> Para obter mais informações sobre a configuração e a integração do Substance 3D Designer em um **pipeline de produção**, *recomendamos fortemente* consultar a seção [Configuração de Pipeline e Projeto](../../../pipeline-and-project-con/pipeline-and-project-configuration.md) da documentação.

![Configurações do projeto](project-settings.resources/2019-3-0-prefs-proj-01.png "Configurações do projeto"){zoomable="yes"}

## Configuração

### Arquivos de configuração

Isso permite definir o caminho do <b>Arquivo de Configuração</b> do Substance 3D Designer. Um arquivo de configuração usa a extensão <b>\*.sbscfg</b> e contém uma lista de arquivos de projeto junto com uma configuração definida de Exibição de Compatibilidade.

*Padrão:\_configuration.sbscfg* padrão

>[!NOTE]
>
> Você pode usar a opção de linha de comando **—config-file** para iniciar o Designer com um arquivo de configuração específico.\
> Para obter mais informações sobre Arquivos de Configuração, consulte a página [Lista de Configuração - SBSCFG](../../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) da documentação.

### Arquivos de projeto

Um arquivo de projeto contém várias configurações que definem os principais aspectos do ambiente de trabalho no Designer, organizados em guias. Essas configurações são listadas no capítulo Projeto desta página. Os arquivos de projeto usam a extensão <b>\*.sbsprj</b>.

É possível importar vários arquivos de projeto para serem usados em seu ambiente de trabalho no Designer. Quando existem vários arquivos de projeto, as configurações que são listas (por exemplo, caminhos observados da biblioteca, aliases etc.) são *combinados*, e as configurações que são valores de conjunto exclusivos são definidas pelo *último arquivo de projeto da lista*.

*Padrão: padrão\_project.sbsprj (somente leitura), usuário\_project.sbsprj*

>[!NOTE]
>
> Para obter mais informações sobre o uso de Arquivos de Projeto em um pipeline de produção, consulte a página [Arquivos de Configuração de Projeto - SBSPRJ](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) da documentação.

### Exibição de compatibilidade

Alguns nós criados com uma versão recente do Designer não são compatíveis com versões mais antigas do Substance Engine.

O <b>Modo de Compatibilidade</b> realçará os nós *não* compatíveis com o Substance Engine selecionado, com contorno amarelo.

*Padrão: Substance Engine v7*

### Visualização 3D

|                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Renderizador padrão</b> | Esta configuração permite selecionar o [renderizador 3D](../../../interface/3d-view/3d-renderers/3d-renderers.md) que deve ser usado por padrão ao iniciar um *novo* [Modo de exibição 3D](../../../interface/3d-view/3d-view.md).<br><br>*Padrão: padrão (renderizador predefinido)* |
| <b>Sombreador padrão</b> | Esta configuração permite selecionar o sombreador que deve ser usado por padrão ao iniciar uma *nova* [Exibição 3D &#x200B;](../../../interface/3d-view/3d-view.md)<br><br>*Padrão: open_pbr.glslfx* |
| <b>Mapa de ambiente padrão</b> | Esta configuração permite selecionar a textura que deve ser aplicada por padrão ao Ambiente ao iniciar uma *nova* [Exibição 3D &#x200B;](../../../interface/3d-view/3d-view.md)<br><br>*Padrão: panorama\_map.hdr* |
| <b>Arquivo de estado padrão</b> | O [Arquivo de **Estado da Cena** da Visualização 3D](../../../interface/3d-view/3d-view.md) inclui várias configurações para a Visualização 3D, como posição da câmera, exposição do ambiente e malha. É usado para armazenar o estado da Visualização 3D para que você possa carregar rapidamente uma cena personalizada para suas necessidades. Os arquivos de Estado de Cena usam a extensão **\*.sbsscn**.Esta configuração permite selecionar o arquivo de Estado da cena de visualização 3D que deve ser usado ao iniciar uma nova visualização 3D.  **Alerta:** algumas atualizações de software podem alterar o modo como os estados da cena são salvos/carregados. Se a cena *não for restaurada corretamente*, é recomendável definir manualmente o estado desejado da cena e *reexportar* o arquivo de estado de Cena usado como padrão. <br><br>*Padrão: vazio (neste caso, um estado de cena predefinido é usado)* |
| <b>Estado de iluminação padrão</b> | Esta configuração permite selecionar quais luzes predefinidas disponíveis devem ser habilitadas ao iniciar uma nova [Exibição 3D](../../../interface/3d-view/3d-view.md), *se nenhum arquivo estiver definido* no campo **Arquivo de Estado Padrão**<br><br>*Padrão: somente Luz Ambiente* |

### Aliases

Os aliases são usados para *encurtar* caminhos do sistema e permitir que as equipes *compartilhem* ativos de maneira mais eficiente. Os aliases são usados *em todo o software*, bem como em *arquivos SBS*.

Estas configurações permitem *adicionar* e *editar* aliases. Quando um alias é aplicado, ele *substitui* o caminho mapeado usando a seguinte sintaxe: <b>://</b>.

Exemplo: se um recurso *myResource* na pasta *myFolder* for colocado no local *C:/Users/user/Documents*, o mapeamento deste local para *myalias* resultará no caminho *myalias://myFolder/myResource* usado no aplicativo *e* no pacote SBS ao qual o recurso pertence.

*Padrão: sbs; sd-3dview-shapes; sd-3dview-maps; sd-3dview-shaders (projeto padrão)*

>[!WARNING]
>
> Os aliases são *globais para o aplicativo*. Isso significa que eles serão aplicados a *todos os caminhos* usados no aplicativo, bem como a todos os caminhos em *arquivos de Configurações do Projeto SBSPRJ carregados*. Lembre-se disso ao configurar o ambiente do projeto.\
> Além disso, recomendamos *não aninhar* aliases, isto é, suavizar um caminho que também está incluído em outro alias.

### Baking

|                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Nome do recurso padrão</b> | Esta configuração permite definir um **modelo de nomeação** padrão que será usado para os arquivos de imagem de saída. Os aliases disponíveis na [janela de cozimento](../../../bakers/bakers.md) também podem ser usados aqui (por exemplo, *$(malha)*, *$(nome do baker)*, *$(udim)*, *$(personalizado)*)<br><br>*Padrão: $(mesh)\_$(nome do baker)* |
| <b>Predefinição padrão</b> | Ao abrir a [janela de cozimento](../../../bakers/bakers.md), você pode tê-la **já configurada** com preparadores e configurações específicos usando esta opção para apontar para um arquivo de predefinições *JSON*. Este arquivo pode ser exportado da janela de cozimento depois de configurado de acordo com suas necessidades.<br><br>*Padrão: nenhum* |
| <b>Modo de filtragem de nome</b> | O objeto da cena cujo nome deve ser usado para corresponder aos objetos de cena com poli baixo e com poli alto:<ul data-preserve-html="true"> <li data-preserve-html="true">Nome da geometria: use o nome do objeto de geometria de malha</li> <li data-preserve-html="true">Nome do pai (legado): use o nome do pai do objeto de geometria de malha (o mesmo que nas versões 14.1 e anteriores do Designer)</li> </ul>*Padrão: nome da geometria* |
| <b>Macros de nome de recurso</b> | Em vez do alias *$(bakername)*, você pode usar suas próprias cadeias de caracteres para [cada padeiro](https://experienceleague.adobe.com/pt-br/docs/substance-3d/bakers/bakers-settings/bakers-settings).  Quando o alias ***$(personalizado)*** for usado no nome da imagem de saída de qualquer preparador, ele será substituído pela cadeia de caracteres correspondente a esse preparador na lista. Se uma célula da lista correspondente a um padeiro for deixada em branco, o alias *$(personalizado)* *não* será substituído por este padeiro.Exemplo: o valor &#39;c-mesh&#39; atribuído ao padeiro &#39;Curvature Map From Mesh&#39; renomeará automaticamente *t\_mymesh\_&#x200B;**$(personalizado)*** para *t\_mymesh\_&#x200B;**c-mesh*** para a saída do padeiro Curvatura from Mesh *somente *<br><br>*Padrão: Nenhum* |
| <b>Filtro de nome de sub-malhas</b> | Ao usar a opção **Corresponder por nome** nos [padeiros](../../../bakers/bakers.md), as partes das versões de baixa e alta definição de uma malha serão *correspondidas* se o nome dessas partes antes dos **sufixos** definidos for *idêntico*. Essa configuração permite definir seus próprios sufixos para se adequar ao seu fluxo de trabalho específico. Partes correspondentes de malhas podem fazer com que os raios ignorem a geometria indesejada em operações de cozimento.Exemplo: o objeto *tronco corporal&#x200B;**\_baixo*** na malha *corpo.fbx* seria comparado ao objeto *tronco corporal&#x200B;**\_alto &#x200B;*** em *corpo\_alto.fbx,* *se esses objetos existirem* nessas malhas *.**Padrão: \_baixo (Malha de baixa polaridade) / \_alto (Malha de alta polaridade)*Similarmente,**&#x200B;faces traseiras&#x200B;**podem ser *ignoradas seletivamente* para as partes de uma malha cujo nome inclui o &#x200B;** sufixo&#x200B;**definido, para [padeiros específicos](https://experienceleague.adobe.com/pt-br/docs/substance-3d/bakers/bakers-settings/bakers-settings) que incluem a opção &#x200B;** Ignorar face traseira**<br><br>* Padrão: \_ignorebf *<br><br>* Observação:* os sufixos Ignorar face traseira e Malha de baixa/alta poly podem ser *combinados em qualquer ordem* (por exemplo, *tronco corporal\_low\_ignorebf*) |

### Gerenciamento de cores

Consulte a página [Gerenciamento de cores](../../../color-management/color-management.md).

>[!WARNING]
>
> As alterações nessas configurações terão efeito após a reinicialização do Designer.

### Geral

|                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>modelos de Substance</b> | Ao criar um novo gráfico, você é solicitado a começar a trabalhar em um **modelo** que pode ter várias configurações e conteúdo *pré-configurados*, como saídas (por exemplo, *PBR (Metallic/Roughness)*).Essa configuração permite que você direcione o Designer para diretórios em que você pode armazenar seus próprios arquivos SBS para usar como modelos. Seus modelos personalizados serão *adicionados à lista* durante a criação de um novo gráfico <br><br>*Padrão: Nenhum *<br><br>*Observação:* recomendamos usar os modelos atuais como referência para configurar e formatar seus arquivos SBS de modelo.  Os modelos podem ser encontrados na pasta **recursos > modelos** do diretório de instalação do Substance 3D Designer. |
| <b>Cenas 3D</b> | Por padrão, o Designer usa o **espaço tangente MikkT** na Visualização 3D. MikkT é amplamente utilizado e é o padrão em programas como Unity, Unreal Engine 4, Blender e xNormal.Você pode usar **seu próprio espaço tangente** para a Exibição 3D, que você fornece à Designer na forma de um *arquivo DLL* de entrada nesta configuração. O rótulo é detectado automaticamente do arquivo DLL, e você pode editar a descrição do plug-in <br><br>*Padrão: mikktspace.dll* Sempre recalcular quadros tangentes <br><br>*Padrão: desmarcado*&#x200B;Ângulo de suavização normal e tangente <br><br>*Padrão: 180.0°* |
| <b>Diversos</b> | Mapas normais podem ser gerados ou processados usando o formato <b>DirectX</b> ou <b>OpenGL</b>. Essa configuração define o valor desse formato em vários locais, como [propriedades de material](../../../interface/3d-view/material-properties/material-properties.md) no modo de exibição [3D](../../../interface/3d-view/3d-view.md) e nos parâmetros do nó de filtro [Normal](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md).<br><br>*Padrão: DirectX*<br><br> Em relação ao nó de filtro [Normal](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md), você pode definir o valor padrão do parâmetro <b>Conteúdo do Canal de Alpha</b>. Você pode optar por forçar o alfa para 1 em todos os casos ou preenchê-lo com informações de sua entrada.<br><br>*Padrão: forçar Alpha para 1* |
| <b>Formatos de imagem</b> | Isso permite especificar as configurações de formato padrão para imagens *exportadas*<br><br>*Padrão: padrão (BMP) / Wavelet baseado em Piz, desmarcado, desmarcado (EXR) / Desmarcado, desmarcado, 75 (JPG) / Melhor velocidade, desmarcado (PNG) / Padrão (TGA) / LZW (TIF) / Desmarcado, 75 (WEBP)* |
| <b>Caminhos de dependências</b> | <p>Os pacotes SBS geralmente têm <b>dependências</b>, ou seja, dependem de <i>recursos externos</i>, como outros pacotes SBS, bitmaps ou arquivos vetoriais.<br>Essas dependências, que estão listadas no [Gerenciador de Dependências](../../../interface/dependency-manager/dependency-manager.md), estão armazenadas e são <i>referenciadas no pacote SBS</i> com um <b>caminho</b> que aponta para esses recursos.</p><p>Para dependências que incluem o <i>mesmo caminho</i> do pacote SBS (isto é, que estão localizadas nos mesmos locais ou subpastas desse local), o caminho de referência é gravado em <b>relação</b> ao local do pacote SBS.</p><p>Exemplo: para um pacote SBS <code>myproject/mypackage.sbs</code>, uma imagem <code>myproject/myfolder/myimage.png</code> será referenciado ao <code>myfolder/myimage.png</code> caminho em <code>mypackage.sbs</code>).</p><p>Para dependências que <i>não</i> incluem o mesmo caminho que o pacote SBS (isto é, estão localizadas em um local totalmente diferente do pacote SBS), você pode escolher como o caminho é gravado.</p><p>Se estiver definido como <b>caminhos relativos</b>, o recurso será referenciado da mesma maneira que descrito acima.</p><p>Exemplo: para um pacote SBS <code>myparentfolder/myproject/mypackage.sbs</code>, uma imagem <code>myparentfolder/myotherfolder/myimage.png</code> será referenciado ao <code>../myotherfolder/myimage.png</code> caminho em <code>mypackage.sbs</code>.</p><p>Se estiver definido como <b>caminhos absolutos</b>, o recurso será referenciado por seu caminho de sistema completo.</p><p>Exemplo: para um pacote SBS <code>myparentfolder/myproject/mypackage.sbs</code>, uma imagem <code>myparentfolder/myotherfolder/myimage.png</code> será referenciado a este mesmo caminho completo em <code>mypackage.sbs</code></p><p><i>Padrão: ...caminhos relativos.</i></p><p><i>Observação:</i> em todos os casos, mover os recursos <i>quebrará as dependências</i>, o que resultará em nós de <b>instância fantasma</b> em gráficos.  Para <i>consolidar</i> todas as dependências em uma única pasta de projeto junto com o pacote SBS, você pode usar os recursos <b>Exportar com dependências...</b> no painel [Explorer](../../the-explorer-window/the-explorer-window.md). Isso cria efetivamente uma pasta de projeto <i>independente</i> que pode ser movida livremente. |

### Biblioteca

Esta seção permite <b>gerenciar o conteúdo personalizado</b> da [Biblioteca](../../../interface/the-library/the-library.md).

O conteúdo de todas as pastas listadas na lista <b>Caminhos adicionados</b> será incluído na Biblioteca. Qualquer alteração no conteúdo é refletida na Biblioteca, após um período de atualização que pode ser definido na [&#128279;](../../../interface/preferences-window/preferences-window.md)guia [&#x200B; da &#x200B;](../../../interface/preferences-window/preferences-window.md) &#x200B; janela [Preferências](../../../interface/preferences-window/preferences-window.md).

Nas colunas da lista, você pode encontrar opções que dão a você um controle mais granular sobre a maneira como o conteúdo dessas pastas é adicionado à biblioteca:

* **Habilitado:** o conteúdo da pasta é mostrado na Biblioteca (*Padrão: Marcado*)
* **Recursivo:** o conteúdo de todas as pastas filho também é mostrado na Biblioteca (*Padrão: marcado*)
* **Padrão de exclusão:** arquivos cujo *nome* corresponde ao Regex (expressão regular) de entrada são *não* mostrados na Biblioteca (por exemplo, `wip-*`). Saiba mais sobre a sintaxe da expressão regular [aqui](https://doc.qt.io/qt-5/qregularexpression.html#wildcardToRegularExpression)
* **Exclusão de extensão:** os arquivos que *extensão* incluem a cadeia de caracteres de texto de entrada são *não* mostrados na Biblioteca. Várias cadeias de caracteres devem ser separadas por `;` ponto e vírgula. (E.g. `jpg;png;tif;fbx`)

Se pacotes SBS forem adicionados à Biblioteca, os **gráficos** e os **recursos** que eles contêm poderão ser *mostrados na Biblioteca* como entradas separadas, se o parâmetro **Visível na Biblioteca** estiver definido como &#39;Sim&#39;.\
Há opções disponíveis para definir se este parâmetro deve ser definido como &#39;Sim&#39; *por padrão* ao criar/adicionar um novo gráfico ou recurso em um pacote.

*Padrão: Verificado*

Se um documento do [Photoshop](https://www.adobe.com/br/products/photoshop.html) (arquivo\*.PSD) incluído na biblioteca tiver <b>várias camadas</b>, uma opção permitirá exibir o conteúdo de* cada camada como uma entrada de imagem separada* na biblioteca.

*Padrão: Verificado*

>[!NOTE]
>
> Embora seus recursos personalizados sejam adicionados à Biblioteca, ela pode *não estar visível* devido às regras de filtragem definidas para as categorias de Biblioteca existentes. Recomendamos criar *seus próprios filtros* organizados em pastas, para garantir que seu conteúdo possa ser encontrado de forma confiável ao trabalhar em seus projetos.\
> Consulte a seção [Gerenciando conteúdo e filtros personalizados](../../the-library/managing-custom-content/managing-custom-content-and-filters.md) da documentação para obter mais informações.

### Python

O Substance 3D Designer carregará automaticamente todos os [plug-ins](../../../scripting/plugin-basics/plugin-basics.md) localizados nas pastas que você adicionar à lista <b>Url</b>.

*Padrão: nenhum*

>[!WARNING]
>
> As alterações nessas configurações terão efeito após a reinicialização do Designer.\
> [Pacotes de plug-ins](../../../scripting/plugins-packages/plugins-packages.md) ainda precisam ser instalados *manualmente* usando o [Gerenciador de plug-ins](../../../scripting/plugin-manager/plugin-manager.md).

### Scripts

>[!WARNING]
>
> Este recurso será *desativado* em uma versão futura em favor da **API Python** mais robusta. Portanto, recomendamos que você alterne seus scripts o mais rápido possível.\
> Você pode ir para a página [Retornos de chamada do aplicativo](../../../scripting/application-callbacks/application-callbacks.md) na seção [Scripts](../../../scripting/scripting.md) de nossa documentação para começar.

Esta seção permite configurar e controlar *scripts* a serem executados quando *eventos* específicos ocorrerem no Designer. Isso é particularmente útil quando usado em conjunto com a integração [Perforce](https://www.perforce.com/), que pode ser configurada na guia Controle de Versão das Configurações do Projeto.

|                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Ações</b> | O Designer tem **acionadores de retornos de chamada** pré-configurados, que *executarão o script* fornecido usando a configuração do intérprete na lista **Intérpretes** descrita abaixo.Os callbacks incluídos são os seguintes:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>onBeforeFileLoaded</strong> - executa o script <em>antes</em> de um pacote SBS ser carregado</li><li data-preserve-html="true"><strong>onAfterFileLoaded</strong> - executa o script <em>depois</em> de um pacote SBS ser carregado</li><li data-preserve-html="true"><strong>onBeforeFileSaved</strong> - executa o script <em>antes</em> de um pacote SBS ser salvo</li><li data-preserve-html="true"><strong>onAfterFileSaved</strong> - executa o script <em>depois</em> de um pacote SBS ser salvo</li><li data-preserve-html="true"><strong>getGraphExportOptions</strong> - executa o script quando as opções [Exportar Saídas](../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md) são chamadas</li></ul>Um script [Python](https://www.python.org/) está incluído nos arquivos de instalação, com as funções acionadas por cada retorno de chamada *já configuradas* e prontas para uso. Você pode usá-la como ponto de partida e adicionar funcionalidades de acordo com suas necessidades. Este script é **functions.py**, localizado na pasta **ferramentas > scripts** dos arquivos de instalação <br><br>*Padrão: Nenhum *<br><br>*Observação:* inicialmente, selecionar um script para qualquer um dos retornos de chamada inserirá esse script em *todos* retornos de chamada para sua conveniência. Você pode configurar scripts diferentes livremente para retornos de chamada específicos após esse ponto. |
| **Intérpretes** | Nesta lista, você pode fornecer *intérpretes* específicos que o Designer deve usar para executar os scripts configurados na lista **Ações** descrita acima. Os intérpretes são identificados usando um *alias personalizado* que pode ser editado no campo de texto de cada entrada da lista. Um intérprete [Python](https://www.python.org/) 3.6 vem junto com os arquivos de instalação do Designer. Você pode encontrá-lo na pasta **plug-ins > pythonsdk** dos arquivos de instalação <br><br>*Padrão: nenhum* |

### Controle de versão

>[!WARNING]
>
> [Perforce](https://www.perforce.com/) é a ferramenta *somente* que atualmente tem suporte para o controle de versão.

Consulte a página [Controle de versão](../../../interface/preferences-window/version-control/version-control.md).

**Como você deve usar isto?**

Você deve definir todas as preferências que são *específicas de projeto* em um arquivo de projeto (\*.sbsprj) no Designer. Essas preferências incluem:

* Plug- in Tangent space
* Biblioteca
* Aliases
* Configurações de exibição 3D
* Configurações de cozimento
* [Configurações do Controle de versão](../../../interface/preferences-window/version-control/version-control.md)

Todos os caminhos são armazenados *relativos* ao Arquivo de Projeto (.spsprj). para que você possa ter uma pasta **biblioteca** no mesmo local que seu Arquivo de Projeto em Perforce, com a seguinte árvore de subpastas:

* maps/
* malhas/
* sbs/
* sbsar/
* psd/
* 3Dview/
* ...

No mesmo nível que o Arquivo do projeto, você também pode armazenar um plug-in de espaço tangente ou sombreador padrão.

O Arquivo de configuração (\*.sbscfg) deve ser colocado no espaço de trabalho Executar ao lado do Arquivo de projeto.

>[!NOTE]
>
> Para obter mais informações sobre a configuração e a integração do Substance 3D Designer em um **pipeline de produção**, *recomendamos fortemente* consultar a seção [Configuração de Pipeline e Projeto](../../../pipeline-and-project-con/pipeline-and-project-configuration.md) da documentação.
