---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/output.html"
breadcrumb-title: ''
description: ''
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Output
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Saída
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---


# Saída

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: Saída](../../../../assets/comp_output_1.png "Nó atômico: Saída"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

O nó Saída especifica o <b>resultado</b> de um gráfico de Substance, ou um de seus resultados se mais de um nó Saída estiver presente nele.

A imagem ou o valor conectado ao nó de Saída de um gráfico é gerado por qualquer [nó de instância](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) que represente esse gráfico e pode [ser exportado como uma saída de gráfico](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md).

</td>
</tr>
</table>

Da mesma forma, quando um [arquivo SBSAR publicado](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) inclui este gráfico, esse arquivo pode gerar a saída dessa imagem em qualquer integração ou plug-in que consuma o arquivo.

Ele tem um único slot de entrada que é tipo-agnóstico, o que significa que ele se digita após o tipo de dados conectado a ele.

Não tem parâmetros, mas sim atributos que são de grande importância para rotular corretamente a saída e colocá-la no uso pretendido.

Todo gráfico de Substance deve ter *pelo menos um* nó de saída. Se não houver nenhuma saída, o gráfico nunca retornará um resultado real e um [aviso](../../../../technical-issues/warnings-and-errors/warnings-and-errors.md) será gerado.

## Atributos

|  |  |
| --- | --- |
| <b>Identificador</b> *Cadeia de Caracteres* | O identificador exclusivo da saída. Esta propriedade não pode ser deixada em branco e não pode conter caracteres especiais ou espaços.   O identificador é usado porque o rótulo do nó é a propriedade &#39;Label&#39; deixada em branco. Ele também pode ser usado para nomear [texturas exportadas](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md). |
| <b>Descrição</b> *Cadeia de Caracteres* | A descrição opcional usada como dica de ferramenta da saída é Substance graphics. |
| <b>Rótulo</b> *Cadeia de Caracteres* | Isso é usado como um rótulo para o nó de saída e seu conector correspondente nos [nós de instância](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) que representam esse gráfico. O rótulo pode conter espaços e caracteres especiais. |
| <b>Dados do usuário</b> *Cadeia de Caracteres* | Metadados opcionais que podem ser usados para operações de filtragem específicas. O [Substance 3D Painter](https://www.adobe.com/br/products/substance3d/apps/painter.html) usa esses dados para [orientar alguns recursos](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/content/creating-custom-effects/user-data). |
| <b>Grupo</b> *Cadeia de Caracteres* | Atributo usado para agrupar saídas para os [modos de criação de link](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) do Designer.   Saídas com um atributo &#39;Group&#39; idêntico são apresentadas como uma única conexão no modo de criação de link &#39;Compact Material&#39;. |

## Atributos de integração

Estes são atributos que devem ser usados por integrações/plug-ins que consomem o gráfico em um [arquivo SBSAR publicado](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md).

Dessa forma, eles não têm impacto no formato de [exportações de bitmap](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md). Além disso, apenas o atributo <b>Uso</b> é usado no Designer. Veja os detalhes abaixo.

<b>Uso</b>

|  |  |
| --- | --- |
| <b>Componente</b> *Cadeia de Caracteres* | Usado para mapear alguns canais de textura para as entradas de sombreador SVBRDF apropriadas em fluxos de trabalho do AxF. |
| <b>Uso</b> *Cadeia de Caracteres* | Define o tipo e o uso do nó de saída. Essa propriedade é importante, pois conduz:<ul data-preserve-html="true"> <li data-preserve-html="true">Conexão de nós em gráficos de Substance ao usar alguns [modos de criação de link](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) </li> <li data-preserve-html="true">Conexão de texturas a sombreadores na Exibição 3D (veja abaixo: &#39;[Sobre a função de usos na Exibição 3D](#usages-role-3dview)&#39;)</li> <li data-preserve-html="true">Conexão de texturas com materiais em integrações/plug-ins</li> </ul> |
| <b>Espaço de cores</b> *Cadeia de Caracteres* | Define o espaço de cores no qual esta saída deve ser interpretada. É usado por algumas integrações em outros aplicativos e não tem impacto no Designer. |

### Sobre a função de usos na Visualização 3D

Como as saídas de gráfico são geralmente destinadas a ser o resultado final para um canal de textura específico, as saídas podem ser enviadas automaticamente para o amostrador apropriado do sombreador usado na Visualização 3D.

Na verdade, uma saída que <b>Propriedade de uso</b> *corresponde a um uso de amostrador* na exibição 3D será conectada a esse amostrador. Por exemplo, uma Saída com uso `basecolor` será conectada ao amostrador `basecolor` do sombreador de Exibição 3D. Saiba mais na seção [Exibir dados na Exibição 3D](../../../../interface/3d-view/3d-view.md) da página [Exibição 3D](https://substance3d.adobe.com/documentation/display/draftdesigner/.3d%20view%20vdraftversion).

Clique em RMB em uma área vazia na [Exibição de gráfico](../../../../interface/the-graph-view/the-graph-view.md) e selecione a opção <b>Exibir saídas na exibição 3D</b> no menu contextual para conectar todas as saídas aos classificadores de exibição 3D com *usos correspondentes*.

>[!IMPORTANT]
>
> Se vários usos forem configurados para, por exemplo, atribuir usos a canais em uma textura compactada, somente o *primeiro uso* da lista será conectado à Exibição 3D. Essa é uma limitação conhecida.

## Saída padrão

Quando um gráfico tem mais de uma saída, uma delas pode ser definida como a saída padrão para esse gráfico. Especifica quais das saídas devem ser usadas para:

* A miniatura de qualquer nó de instância que representa esse gráfico
* Visualizar esses nós de instância na Visualização 2D
* A miniatura desse gráfico na Biblioteca (saiba como adicionar seus próprios recursos [aqui](../../../../interface/preferences-window/project-settings/project-settings.md))

Esse recurso permite organizar as saídas do gráfico em qualquer ordem, independentemente de como o gráfico será visualizado como um nó.

Para definir um nó Saída como a saída padrão do gráfico:

* Clique com o botão direito do mouse em um nó Saída e selecione a ação “Definir como saída padrão” no menu contextual.
* Nas propriedades do nó Saída, use o botão “Definir como padrão” no cabeçalho da seção “Atributos”.

Aqui está um exemplo de nós de instância antes e depois de definir uma saída padrão:

<table>
  <tr style="border: 0">
    <td style="border: 0">
      <img src="../../../../assets/defaultouput2.png" alt="defaultouput2">
      <br><i>Antes</i>
    </td>
    <td style="border: 0">
      <img src="../../../../assets/defaultouput1.png" alt="defaultouput1">
      <br><i>Depois</i>
    </td>
  </tr>
</table>
