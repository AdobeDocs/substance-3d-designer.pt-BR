---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/preferences-window.html"
breadcrumb-title: ''
description: Acesse a janela Preferências no Substance 3D Designer para personalizar as configurações e o comportamento do aplicativo.
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Preferências
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '1973'
ht-degree: 1%

---


# Janela Preferências

![Janela Preferências](../../assets/image2021-6-22-20-56-1.png "Janela Preferências")

Esta página apresenta a janela <b>Preferências</b> e todas as suas configurações.

Você pode encontrar a janela Preferências no menu <b>Editar</b> na barra superior principal do aplicativo. Esta caixa de diálogo permite ajustar várias configurações. Está organizado em guias que abrangem diferentes áreas de comportamento e funcionalidade.\
Recomendamos a revisão de todas essas configurações para obter uma visão melhor de como o aplicativo opera e como ele pode ser ajustado ao seu fluxo de trabalho.

>[!NOTE]
>
> Para obter mais informações sobre como essas preferências são armazenadas e como integrá-las em um ambiente de produção, consulte a página [Preferências do Usuário - Automatizando a Instalação](../../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md) da documentação.

## Geral

### Documentos recentes

|  |                                                                                                                                         |
| --- |-----------------------------------------------------------------------------------------------------------------------------------------|
| <b>A lista de documentos recentes contém</b>  *Padrão: 10* | Isso permite selecionar o número de documentos a serem listados na entrada <b>Pacotes Recentes</b> do item <b>Arquivo</b> no [menu principal](../the-main-toolbar/the-main-toolbar.md). |

### Histórico

|  |  |
| --- | --- |
| **Tamanho da pilha do histórico** *Padrão: 200* | Isso indica o número de operações de desfazer disponíveis a qualquer momento no item <b>Editar > Desfazer</b> do [menu principal](../the-main-toolbar/the-main-toolbar.md).  **Cuidado:** quanto mais operações de desfazer você precisar, mais memória o aplicativo precisará. |

### Idioma

|  |  |
| --- | --- |
| **Escolha o idioma do aplicativo** *Padrão: Sistema* | Esta configuração define o idioma usado na interface do aplicativo. A opção &#39;*Sistema*&#39; detecta automaticamente o idioma das configurações de idioma do sistema. Os idiomas disponíveis estão listados em nossos [Requisitos de sistema](../../getting-started/system-requirements/system-requirements.md).  **Observação:** a alteração desta configuração somente terá efeito após a reinicialização do aplicativo. |

### Exibições

|  |  |
| --- | --- |
| <b>Inverter exibições de zoom</b>  *Padrão: Desmarcado* | Se marcado, os controles de zoom serão invertidos na [Exibição 2D](../../interface/2d-view/2d-view.md), na [Exibição 3D](../../interface/3d-view/3d-view.md) e nos [gráficos](../../interface/the-graph-view/the-graph-view.md). |

### Caminhos

|  |  |
| --- | --- |
| <b>Caminho de salvamento/exportação</b>  *Padrão: último caminho* | Determina se o caminho de salvamento/exportação sugerido é o último caminho selecionado ou o caminho do [pacote SBS](../../getting-started/overview/overview.md). O último caminho selecionado é salvo entre as sessões. |
| <b>Pasta temporária</b>  *Padrão: caminho que depende do sistema operacional* | Quando os dados da imagem de um gráfico excedem o pool de memória alocado (veja abaixo <b>Memória > Cache de Imagem</b>), os dados de estouro são gravados no disco. Essa configuração permite definir o local no qual os dados excedentes do cache de imagem são gravados.   Este local também é usado para armazenar uma cópia do pacote SBS atualmente aberto com as modificações mais recentes desde o último salvamento manual. |

### Memória

#### Cache de imagem

O aplicativo mantém em cache uma *imagem descompactada de resolução total* para cada nó renderizado no gráfico atual.\
Os nós de instância gerarão essas imagens para todos os nós do gráfico ao qual fazem referência e as excluirão depois que suas [saídas](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) forem computadas. Somente as saídas são mantidas na memória nesse ponto.

Você pode definir o tamanho máximo de cache alocado para miniaturas e imagens na memória do sistema e ver o uso atual. Se os dados do cache estourarem o pool alocado, os dados em excesso serão gravados na <b>pasta Temporária</b> (consulte acima <b>Caminhos > pasta Temporária</b>).

|  |  |
| --- | --- |
| <b>Orçamento de memória</b>  *Padrão: Automático* | Essa alocação é calculada automaticamente para aproximadamente 75% do total do pool de memória do sistema. Para definir esse valor manualmente, selecione a opção &#39;*Personalizado*&#39; e defina um valor no campo de entrada adjacente. |

Observe que a gravação no disco é *ordens de magnitude mais lenta* do que a gravação na memória do sistema. Portanto, o tempo de renderização do gráfico *aumentará exponencialmente*, pois os dados excedentes precisam ser gravados na Pasta Temporária.\
Para evitar que isso aconteça, recomendamos dar uma olhada nas sugestões para diminuir o impacto de memória de um gráfico na seção [Diretrizes de Otimização de Desempenho](../../best-practices/performance-optimization/performance-optimization-guidelines.md) da documentação.

#### Agendador de tarefas

Durante tarefas específicas, como conversões de imagem para miniaturas ou a [Exibição 2D](../../interface/2d-view/2d-view.md), trabalhos separados serão criados e distribuídos pelos núcleos de processamento do sistema para proporcionar eficiência. Cada trabalho gravará dados na memória do sistema para executar suas operações.\
Esta configuração permite definir o pool de memória alocado para *todos os trabalhos simultâneos*. Quando este pool for totalmente usado, novos trabalhos serão enfileirados até que os trabalhos atuais sejam concluídos.

|  |  |
| --- | --- |
| <b>Orçamento de memória</b>  *Padrão: Automático* | Essa alocação é calculada automaticamente para aproximadamente 10% do total do pool de memória do sistema. Para definir esse valor manualmente, selecione a opção &#39;*Personalizado*&#39; e defina um valor no campo de entrada adjacente. |

### Interface

|  |  |
| --- | --- |
| **Desabilitar DPI Alto** *Padrão: Desmarcado* | O modo <b>DPI alto</b> manterá o dimensionamento consistente de elementos de texto e interface de usuário *independentemente* das configurações de exibição e dimensionamento do sistema.   Desabilitar (isto é, caixa de seleção *preenchida*) essa configuração permitirá que a interface seja dimensionada, o que resulta em texto maior e mais legível em algumas exibições, mas também pode criar inconsistências no tamanho do texto, juntamente com outros problemas de layout.  **Cuidado:** o Designer adquire a escala específica dos elementos da interface do usuário *do sistema operacional*. Portanto, qualquer ajuste no dimensionamento da interface de usuário deve ser feito nas configurações de exibição do SO. Para garantir que as configurações de exibição sejam aplicadas corretamente no Designer, *saia* da sessão de usuário do sistema operacional e entre novamente após alterar essas configurações.  **Observação:** a alteração desta configuração somente terá efeito após a reinicialização do aplicativo. |

### Backup automático

Um recurso de salvamento automático está incluído por padrão, criando cópias do estado atual de [pacotes SBS](https://docs.substance3d.com/display/DRAFTDESIGNER/.Overview+vDraftVersion) abertos em períodos definidos. Os salvamentos automáticos são colocados em uma pasta <b>.autosave</b> no local do pacote SBS.

|  |  |
| --- | --- |
| <b>Backup automático a cada # minutos</b>  *Padrão: 5* | O período entre cada salvamento automático. |
| <b>Manter até # versões</b>  *Padrão: 6* | O número máximo de salvamentos automáticos a serem mantidos em um determinado momento. |

Quando a quantidade máxima de versões for atingida, os backups mais recentes excluirão os mais antigos.\
Observe também que os salvamentos automáticos devem ser abertos *depois de movê-los* para o local do pacote SBS original. Eles *não* devem ser abertos em seu local atual.

### Publicação e envio de arquivos SBSAR

|  |  |
| --- | --- |
| <b>Sempre salvar o arquivo .sbs ao publicar em .sbsar ou enviar para outro aplicativo</b>  *Padrão: Verdadeiro* | Controla o salvamento automático do pacote SBS ao [publicá-lo](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) ou enviá-lo para outro aplicativo. |

### Preparador

|  |                                                                                                                                                                                                                                                                                                 |
| --- |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Limite de tamanho da cozinha</b>  *Padrão: 8.192 pixels* | Define a resolução máxima de pixels permitida para todos os nós em qualquer Substance [gráfico](../../compositing-graphs/substance-compositing-graphs.md). Como as saídas de gráfico são sempre imagens quadradas de potências de 2 resoluções, o valor definido aqui define a largura e o height máximos, em pixels. |

### Mecanismo

|  |  |
| --- | --- |
| <b>Limite de cache da GPU</b>  *Padrão: 2048 MB* | Essa configuração permite definir quanta memória deve ser reservada para os estágios de renderização de cache. Normalmente, o Substance Engine armazenará em cache a saída de cada nó em um gráfico de Substance. |

>[!NOTE]
>
> Recomendamos dar uma olhada nas sugestões para diminuir a área de memória de um gráfico na seção [Diretrizes de Otimização de Desempenho](../../best-practices/performance-optimization/performance-optimization-guidelines.md) da documentação.

## Projetos

Consulte a página [Configurações de projetos](../../interface/preferences-window/project-settings/project-settings.md).

## Gráfico

### Comum

|  |  |
| --- | --- |
| <b>A tecla Tab mostra o menu do nó</b>  *Padrão: Verificado* | Se marcada, a tecla &#39;Tab&#39; abrirá o <b>menu Nó</b>, replicando a funcionalidade da tecla &#39;Espaço&#39;. |
| <b>Habilite a criação de nós arrastando conectores com clique</b>  *Padrão: Verificado* | Se marcada, quando você clica em qualquer conector, arraste o cursor e solte o link criado no espaço vazio do gráfico para exibir o <b>menu Nó</b>.   O menu também será *filtrado* de acordo com o tipo do conector no qual você clicou. Isso significa que somente os nós compatíveis com o conector clicado serão exibidos. |
| <b>Exibir saídas na exibição 3D ao abrir um gráfico</b>  *Padrão: Verificado* | Se marcada, todas as saídas de gráfico serão aplicadas automaticamente na [Exibição 3D](../../interface/3d-view/3d-view.md) quando o gráfico for aberto.   Isso também tem o efeito de renderizar todos os nós que fazem parte de um fluxo que leva a um nó [Saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md). |

### Gráfico de composição do Substance

|  |  |
| --- | --- |
| <b>Calcular automaticamente todas as miniaturas de nós ao abrir um gráfico</b>  *Padrão: Verificado* | Se esta opção estiver marcada, todas as miniaturas de nós serão renderizadas automaticamente ao carregar o gráfico. |
| <b>Exibir saída em exibição 2D ao abrir um gráfico</b>  *Padrão: Verificado* | Se marcada, a primeira saída de gráfico será exibida automaticamente na [Exibição 2D](../../interface/2d-view/2d-view.md) quando o gráfico for aberto. Isso também tem o efeito de renderizar todos os nós que fazem parte de um fluxo que leva a esse nó [Saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md). |
| <b>Exibir automaticamente o nó de composição recém-criado</b>  *Padrão: Verificado* | Se marcada, a [Exibição 2D](../../interface/2d-view/2d-view.md) será atualizada automaticamente para exibir a saída de um nó recém-criado. |
| <b>Inserir automaticamente nó de conversão de cor/escala de cinza</b>  *Padrão: Desmarcado* | Se marcada, resolva automaticamente as inconsistências de tipos de conexão de Cor/Tons de Cinza, *colocando nós específicos* para executar a conversão apropriada.   Quando uma saída *Tons de Cinza* (conector cinza) é conectada a uma entrada *Cor* (conector amarelo), um nó [Mapa de Degradê](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) é colocado automaticamente entre os dois conectores.   Quando uma saída *colorida* (conector amarelo) é conectada a uma entrada *tons de cinza* (conector cinza), um nó [conversão de tons de cinza](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/grayscale-conversion/grayscale-conversion.md) é colocado automaticamente entre os dois conectores. |
| <b>Habilitar edição de gráfico no contexto</b>  *Padrão: Desmarcado* | Por padrão, ao abrir um gráfico referenciado por um [nó de instância](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) com um clique com o botão direito do mouse no nó e selecionando <b>Abrir Referência</b>, esse gráfico é carregado e editado *isoladamente*.   Se marcada, você pode editar gráficos referenciados por instâncias *usando as informações passadas na instância* pelo gráfico atual. Para fazer isso, clique com o botão direito do mouse em um nó de instância e selecione <b>Abrir Referência no Contexto</b> ou use o pressionamento de tecla Ctrl+E.   Isso significa que um gráfico com instância pode ser editado no contexto do gráfico no qual a instância é inserida. Isso é muito útil para visualizar os efeitos das edições no gráfico em que você estava trabalhando. Veja o exemplo abaixo.  **Observação:** as guias <b>Visualização</b> e <b>Predefinições</b> estão *desabilitadas* nas [propriedades de gráfico](../../compositing-graphs/graph-parameters/graph-parameters.md) ao usar a edição em contexto. |

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Edição do contexto interno desabilitada](../../assets/substance3ddesigner_incontext_no.gif "Edição do contexto interno desabilitada")

*Abrir Referência*

</td>
<td style="border: 0;" valign="top">

![Edição do contexto interno habilitada](../../assets/substance3ddesigner_incontext_yes.gif "Edição do contexto interno habilitada")

*Abrir Referência No Contexto*

</td>
</tr>
</table>

## Visualização 3D

### Diversos

|  |  |
| --- | --- |
| <b>Ambiente oculto por padrão</b>  *Padrão: Verificado* | Determina a configuração de visibilidade padrão do [Ambiente](../../interface/3d-view/3d-view.md). Quando oculto, o plano de fundo da Exibição 3D é substituído por uma *cor sólida*. |
| <b>Dimensionamento do visor</b>  *Padrão: Automático* | Controla o dimensionamento da resolução de renderização da Exibição 3D quando o sistema usa o dimensionamento de exibição.<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Automático</i>: a resolução de renderização é baseada na resolução de exibição <i>dimensionada</i></li> <li data-preserve-html="true"><i>Nenhum</i>: a resolução de renderização é baseada na resolução de exibição <i>nativa</i></li> </ul> |

### OpenGL

|  |  |
| --- | --- |
| <b>Contagem de exemplos</b>  *Padrão: 64* | Afeta o tamanho da tabela de amostra dos sombreadores de visualização 3D. Um valor mais alto resultará em uma qualidade de imagem mais alta em detrimento do desempenho.  **Observação:** a tabela de exemplo dos sombreadores também é afetada pela GPU e pelo sistema operacional do sistema. |

## Baking

|  |  |
| --- | --- |
| <b>Rastreamento de raios do GPU</b>  *Padrão: Verificado* | Se marcado, o rastreamento de raios será executado na GPU para [padeiros compatíveis](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing).   As seguintes infraestruturas de Rastreamento de raios do GPU serão o padrão, dependendo da arquitetura da GPU NVIDIA:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>DXR</i>: Turing e mais recentes</li> <li data-preserve-html="true"><i>Optix</i>: Pascal e Maxwell</li> </ul>  **Observação:** mais informações sobre padeiros alimentados por GPU estão disponíveis na seção [Rastreamento de raios do GPU](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing) da documentação do [Substance Bakers](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/home).  **Dica:** você pode usar os *argumentos de linha de comando* a seguir ao iniciar o aplicativo para *forçar* o uso de uma infraestrutura de Rastreamento de raios do GPU diferente: <ul data-preserve-html="true"> <li data-preserve-html="true"><code>—force-optix</code> : forçar o uso do Optix na Turing da Nvidia ou GPUs mais novas</li> <li data-preserve-html="true"><code>—force-dxr</code> : forçar o uso de DXR em GPUs Nvidia Pascal</li> </ul> |

## Biblioteca

|  |  |
| --- | --- |
| <b>Reconstruir miniaturas</b> | A opção acionará um recálculo de todas as miniaturas da [biblioteca](../../interface/the-library/the-library.md), que substituirá automaticamente as anteriores. |

## Atalhos

Você pode atribuir atalhos de teclado personalizados para criar nós nos gráficos.

Atalhos podem ser atribuídos para nós em todos os tipos de gráficos: [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md), [gráficos de função de Substance](../../function-graphs/function-graphs.md) e [gráficos de FX-Map](../../function-graphs/fxmaps/fxmaps.md).

Um atalho pode ser atribuído a qualquer nó, até mesmo a nós de biblioteca personalizados. Um mesmo atalho pode ser atribuído em diferentes tipos de gráficos. Nenhum atalho é atribuído por padrão. Você pode personalizar isso como quiser.

Em caso de conflito com outro atalho de nó ou um atalho de programa incorporado, a entrada será destacada e será exibido um aviso. O atalho terá *nenhum efeito* até que o conflito seja resolvido.

>[!IMPORTANT]
>
> Atalhos substituídos por plug-ins Python
> 
> Quando um plug-in Python define um atalho de teclado atribuído a um nó, o plug-in substitui esse atalho. Isso significa que a tecla acionará a ação do plug-in em vez de criar um nó.
> 
> Esse já é o caso para as teclas H, S e V usadas pelas [ferramentas de alinhamento de nó](../../interface/the-graph-view/node-alignment-tools/node-alignment-tools.md).
