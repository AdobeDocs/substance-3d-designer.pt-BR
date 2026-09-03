---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/vector-graphics-svg-resource/vector-editing-tools.html"
breadcrumb-title: ''
description: Use ferramentas de edição de vetores para criar e modificar gráficos de SVG no Substance 3D Designer para texturas de procedimento.
helpx_creative_field: ""
helpx_description: Designer > Resources > Vector graphics (SVG) resource > Vector editing tools
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ferramentas de edição de vetor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1850'
ht-degree: 0%

---


# Ferramentas de edição de vetor

Esta página descreve as ferramentas de edição disponíveis no painel [Exibição 2D](https://docs.substance3d.com/display/SDDOC/2D+view) para gráficos vetoriais compatíveis.

## Visão geral

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

O painel [Exibição 2D](https://docs.substance3d.com/display/SDDOC/2D+view) oferece ferramentas básicas de edição vetorial que permitem criar ou editar gráficos vetoriais *manualmente* diretamente no [Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html). Essas ferramentas são particularmente úteis, por exemplo, para criar rapidamente *máscaras* ou *padrões*.

As ferramentas são compatíveis com a entrada da caneta. Para aproveitar as vantagens de exibições com caneta, você pode [desencaixar](https://docs.substance3d.com/display/SDDOC/Customizing+your+workspace) o painel [exibição 2D](https://docs.substance3d.com/display/SDDOC/2D+view) e, em seguida, colocá-lo e redimensioná-lo em qualquer configuração que seja mais confortável para pintura.

As edições podem ser *desfeitas individualmente*, e todos os outros recursos do painel Exibição 2D ainda estão *disponíveis* enquanto você edita a imagem vetorial, como o painel [Histograma](https://docs.substance3d.com/display/SDDOC/2D+view#id-2Dview-Histogram), a [Exibição lado a lado](https://docs.substance3d.com/display/SDDOC/2D+view#id-2Dview-Viewport) e a [Imagem de fundo](https://docs.substance3d.com/display/SDDOC/2D+view#id-2Dview-Backgroundimage).

</td>
<td style="border: 0;" valign="top">

![](vector-editing-tools.resources/vector-editing-tools-01.png){width="512px"}

</td>
</tr>
</table>

>[!TIP]
>
> **Somente Windows**
> 
> Os usuários do tablet devem aplicar as configurações descritas na página a seguir para obter a experiência mais confiável no Designer: [Configurando Canetas e Tablets](https://docs.substance3d.com/display/SPDOC/Configuring+Pens+and+Tablets)

>[!IMPORTANT]
>
> Você pode pintar *somente* em *recursos de gráficos vetoriais[ de ](../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)8 bits* que são [novos ou importados](https://docs.substance3d.com/display/SDDOC/Importing%2C+Linking+and+New+Resources).

![Caixa de diálogo Novo recurso de SVG](vector-editing-tools.resources/vector-editing-tools-02.png "Nova caixa de diálogo de recurso de SVG"){width="512px"}

## Ativação das ferramentas de edição de vetores

As ferramentas de edição vetorial serão habilitadas automaticamente no painel [exibição 2D](https://docs.substance3d.com/display/SDDOC/2D+view) quando os seguintes critérios relativos a uma imagem gráfica vetorial forem atendidos:

* A imagem de gráficos vetoriais é um recurso [novo ou importado](https://docs.substance3d.com/display/SDDOC/Importing%2C+Linking+and+New+Resources)
* O bitmap é exibido no painel [exibição 2D](https://docs.substance3d.com/display/SDDOC/2D+view)

*Novas* imagens de gráficos vetoriais podem ser criadas das seguintes maneiras:

* No painel [Explorador](https://docs.substance3d.com/display/SDDOC/The+Explorer+Window), clique no RMB em um *pacote SBS* ou em uma *pasta* dentro de um pacote para abrir o menu contextual, abra o submenu **Novo** e selecione a opção **SVG**
* Em um [gráfico](https://docs.substance3d.com/display/SDDOC/The+Graph+view), crie um [nó de SVG](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) e selecione a opção **Do novo recurso...** no menu contextual

A janela **Novos dados vetoriais** será aberta, permitindo que você defina o *nome* e a *resolução* do novo recurso de gráficos vetoriais.

>[!TIP]
>
> Para obter o melhor desempenho com as ferramentas de edição de vetores, recomendamos o uso de imagens de gráficos vetoriais com resoluções que são *potências de dois*, por exemplo, 128, 256, 512, 1024, ...

### Exportação de gráficos vetoriais de outro software

O *somente* do Designer oferece suporte para gráficos vetoriais usando o formato de arquivo **SVG**.

Para obter a melhor compatibilidade e confiabilidade no Designer e em suas ferramentas de edição, verifique se todos os objetos são convertidos em *contornos* e desagrupados em *objetos separados* usando *cores simples*, de modo que *nenhum dos seguintes itens permaneça*:

* **Texto**
* **Gradientes**
* **Padrões** (para preenchimentos e contornos de traçado)
* **Estilos**

Os usuários do **Adobe Illustrator** podem consultar a imagem anexada para obter as *configurações de exportação recomendadas para o SVG.*

+++Opções de exportação para Adobe Illustrator
![Opções de exportação do Illustrator para o SVG](vector-editing-tools.resources/vector-editing-tools-03.png "Opções de exportação do Illustrator para o SVG")



+++

>[!NOTE]
>
> Para saber mais sobre limitações de SVG, exportando de outros softwares e propriedades de SVG no Designer, consulte a seção [Recurso de gráficos vetoriais (SVG)](../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md).

## Ferramentas

As ferramentas e opções de pintura estão organizadas em *barras de ferramentas* no painel [exibição 2D](https://docs.substance3d.com/display/SDDOC/2D+view). Essas barras de ferramentas podem ser realocadas para *qualquer lado* do painel ou como uma *barra de ferramentas flutuante*, clicando e segurando **LMB** na *alça* - exibido como uma linha tripla - e depois soltando **LMB** no local desejado.

Duas barras de ferramentas são exibidas quando as ferramentas de edição de vetor estão ativadas:

* **Seleção de ferramenta** **barra de ferramentas**: permite *selecionar uma ferramenta*, bem como as *cores de preenchimento/contorno*, e é colocada no lado *esquerdo* do painel Exibição 2D por padrão
* **Barra de ferramentas de opções**: permite definir as *opções* da *ferramenta atualmente selecionada* e está posicionada no lado *superior* do painel Exibição 2D por padrão

Os atalhos de teclado permitem acessar as ferramentas rapidamente e são marcados abaixo entre parênteses após o nome da ferramenta/função:

+++Seleção de cor
A ![](vector-editing-tools.resources/vector-editing-tools-04.png)![](vector-editing-tools.resources/vector-editing-tools-05.png) **seleção de cores** *miniaturas* permite definir uma cor de *preenchimento* e de *contorno* para formas vetoriais. Você pode abrir o **Editor de cores** para cada uma dessas cores das seguintes maneiras:

* **Cor de preenchimento:** clique na miniatura de cores de *preenchimento* (parte superior) ou clique duas vezes em LMB na tela

* **Cor do contorno:** clique na miniatura de *cores do contorno* (inferior) ou *mantenha a tecla Ctrl* pressionada e clique duas vezes no LMB na tela

As cores definidas serão então aplicadas às *formas atualmente selecionadas*.

Se a cor atual do *contorno* for *preta* - isto é, luminância 0 ou RGB (0, 0, 0) - ela *não* será aplicada às formas selecionadas até que você *clique na miniatura da cor do contorno*.

+++

+++Transformação
![Ferramenta de transformação](vector-editing-tools.resources/vector-editing-tools-06.png "Ferramenta de transformação"){width="512px"}



A ferramenta ![](vector-editing-tools.resources/vector-editing-tools-07.png) <b>Transformação</b> (<b>V</b>) pode selecionar formas, que são incluídas em um gizmo de transformação. Este gizmo permite executar as seguintes ações:

<b>Mover</b>: clique e segure o LMB *dentro* do cursor

<b>Escala</b>: clique e segure o LMB em qualquer uma das *alças quadradas* ao longo do cursor para *dimensionar* o objeto horizontalmente, verticalmente ou ambos. Por padrão, o dimensionamento é feito relativamente à alça no lado *oposto* do gizmo. Você pode pressionar a tecla <b>Alt</b> para executar o dimensionamento relativamente ao *centro* do cursor e manter pressionada a tecla <b>Shift</b> para *bloquear* a *proporção* de largura/height do cursor

<b>Gire: </b>clique e segure o LMB próximo a qualquer uma das *alças quadradas* ao longo do cursor, *fora* do cursor.

+++

+++Nó
![Ferramenta Nó](vector-editing-tools.resources/vector-editing-tools-08.png "Ferramenta Nó"){width="512px"}



A ferramenta ![](vector-editing-tools.resources/vector-editing-tools-09.png) <b>Nó</b> (<b>A</b>) permite selecionar vértices individuais (ou seja, nós) da forma selecionada e editar sua posição e alças, bem como adicionar e remover vértices. Depois que uma forma é selecionada, as seguintes ações podem ser executadas:

<b>Adicionar vértice:</b> Ctrl+LMB no contorno da forma

<b>Remover vértice</b>: Ctrl+LMB no vértice

<b>Mover vértice</b>: manter LMB no vértice

<b>Mover alças de vértice</b>: manter LMB na alça

<b>Mover a alça do vértice independentemente</b>: mantenha Alt+LMB pressionado na alça. Observe que os identificadores serão *desvinculados* após esse ponto até que sejam *redefinidos*

<b>Redefinir alças</b>: clique em Alt+LMB no vértice. As alças serão redefinidas para a *posição do vértice*

<b>Mover as alças de redefinição de vértice</b>: pressione Alt+LMB no vértice. Os identificadores *vinculados* serão exibidos

+++

+++Forma
![Ferramenta Forma](vector-editing-tools.resources/vector-editing-tools-01.png "ferramenta Forma"){width="512px"}



A ferramenta ![](vector-editing-tools.resources/vector-editing-tools-10.png) <b>Formas</b> (<b>M</b>) oferece um conjunto de formas primitivas, usando a cor de *preenchimento* atual, que pode ser criada e editada:

* <b>Retângulo;</b>

* <b>Elipse;</b>

* <b>Retângulo arredondado:</b> os ângulos arredondados têm um raio bloqueado;

* <b>Polígono:</b> cria um octógono.

Para desenhar uma primitiva, Mantenha o <b>LMB</b> em qualquer lugar na tela por qualquer um dos seus *cantos*. Pressione <b>Alt+LMB</b> para desenhar a forma a partir do seu *centro*.

+++

+++Caneta
![Ferramenta Caneta](vector-editing-tools.resources/vector-editing-tools-11.png "Ferramenta Caneta"){width="512px"}



A ferramenta ![](vector-editing-tools.resources/vector-editing-tools-12.png) <b>Caneta</b> (<b>P</b>) permite desenhar uma nova forma personalizada, usando a cor de *preenchimento* atual. Dois modos estão disponíveis:

No modo <b>Caminho </b>, a forma é desenhada *um vértice por vez*. Os seguintes controles estão disponíveis:

Adicionar <b>entrada direta/saída direta </b>vértice: clique no LMB

Adicionar vértice <b>curvo para dentro/para fora</b> (*alinhado* tangentes): segure LMB e arraste

Adicionar <b>curva para dentro/para fora </b>vértice (*desalinhado* tangentes)\*: segure LMB e arraste, depois segure Alt+LMB

Adicionar <b>vértice de entrada/saída </b>\*: igual ao vértice de entrada/saída de curva (tangentes desalinhadas), mas a linha de saída precisa ser colocada* sobre o novo vértice*

Adicionar <b>entrada direta/saída de curva</b> vértice\*: mantenha Alt+LMB pressionado e arraste

<b>Fechar forma</b> no *próximo* vértice: pressione Ctrl

<b>Fechar forma</b> no *vértice* atual: pressione Enter ou clique em LMB no *primeiro vértice* da forma atual

<b>segurar o modo </b>permite desenhar formas diretamente arrastando a caneta pela tela enquanto usa o LMB.

Os vértices são *colocados automaticamente* ao longo do traçado para que o caminho resultante corresponda ao traçado o mais próximo possível. A forma é *fechada automaticamente* quando o traçado termina, conectando o primeiro vértice ao último no traçado.

+++

+++Extrusão
![Ferramenta Extrusão](vector-editing-tools.resources/vector-editing-tools-13.png "Ferramenta Extrusão"){width="512px"}



A ferramenta ![](vector-editing-tools.resources/vector-editing-tools-14.png) **Extrusão** (E) *adiciona* uma forma de um *diâmetro de conjunto*, desenhada ao longo de um caminho usando o *modo de desenho* selecionado, e aplica o resultado na tela seguindo o *modo de mesclagem* definido na barra de ferramentas de opções.

Os *modos de desenho* a seguir estão disponíveis:

![](vector-editing-tools.resources/vector-editing-tools-15.png) **Forma livre**: desenha a forma *diretamente ao arrastar* a caneta pela tela enquanto mantém o LMB pressionado. A forma é adicionada quando o traçado termina.

![](vector-editing-tools.resources/vector-editing-tools-16.png) **Poligonal**: desenha a forma *uma face por vez* clicando em LMB para adicionar um ângulo. A forma é adicionada quando a tecla Enter é pressionada.

A forma desenhada pode ser controlada usando estes parâmetros:

<b>Tamanho</b>: controla o diâmetro da forma radial desenhada no local do cursor.

<b>Smoothness</b>: controla a quantidade pela qual a forma desenhada deve ser *suavizada e simplificada* quando adicionada ao final do traçado.

Quando o desenho é concluído, a forma é adicionada e mesclada com a forma atualmente selecionada usando um destes *modos de mesclagem* disponíveis:

![](vector-editing-tools.resources/vector-editing-tools-17.png) **Sem mesclagem**: a forma é desenhada *na parte superior* da forma selecionada como um *objeto separado*.

![](vector-editing-tools.resources/vector-editing-tools-18.png) **União**: a forma está *adicionada* à forma selecionada.

![](vector-editing-tools.resources/vector-editing-tools-19.png) **Subtração**: a forma está *recortada* da forma selecionada.

![](vector-editing-tools.resources/vector-editing-tools-20.png) **Interseção**: somente as *partes sobrepostas* da forma nova e selecionada permanecem.

+++

## Operações de forma

![Operações de forma](vector-editing-tools.resources/vector-editing-tools-21.png "Operações de forma"){width="512px"}

Além das ferramentas listadas acima, várias operações podem ser executadas em *formas selecionadas* usando o menu contextual disponível ao clicar em RMB. Essas operações quase todas têm um atalho de teclado (entre parênteses abaixo) organizado nas seguintes categorias:

+++Adição e remoção de formas
<b>Copiar seleção</b> (Ctrl+C): *Copiar* as formas selecionadas para a área de transferência

<b>Recortar seleção</b> (Ctrl+X): *Copiar* as formas selecionadas para a área de transferência e *remover* as formas

<b>Colar</b> (Ctrl+V): cria a forma copiada atualmente na área de transferência, no *local do cursor*

<b>Colar no local</b> (Ctrl+Shift+V): crie a forma copiada atualmente na área de transferência, no *local da forma copiada*

<b>Excluir seleção</b> (Del): *Remover* as formas selecionadas

+++

+++Organização de formas
As formas são organizadas em uma *pilha*, que define a *ordem* das formas na tela, ou seja, que está sobre a qual. Novas formas são criadas *na parte superior* da tela por padrão, e os seguintes controles permitem alterar essa organização:

<b>Trazer para frente</b> (Residência): *eleva* as formas selecionadas para o *topo* da pilha de formas

<b>Avançar</b> (PgUp): *eleva* as formas selecionadas até *um nível* na pilha de formas

<b>Recuar</b> (PgDown): *reduz* as formas selecionadas para baixo em *um nível* na pilha de formas

<b>Enviar para trás</b> (Fim): *reduz* as formas selecionadas para a *parte inferior* da pilha de formas

+++

+++Enviar para nova imagem do SVG
Você pode usar formas na imagem atual para criar um *novo [recurso SVG](../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)* no [pacote SBS](../../../getting-started/overview/overview.md) atual. A este respeito, estão disponíveis as seguintes ações:

<b>Copiar seleção para o novo SVG</b>: cria um novo recurso de SVG e copia as formas selecionadas *no local* nesta nova imagem.

<b>Recortar seleção para novo SVG</b>: cria um novo recurso de SVG, copia as formas selecionadas *no local* nesta nova imagem e *remove*-as da *imagem atual*.

+++
