---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/manage-parameters.html"
breadcrumb-title: ''
description: Saiba como gerenciar e organizar parâmetros em gráficos de composição de Substance para melhor organização do fluxo de trabalho.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Manage parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gerenciar parâmetros
user-guide-description: ''
user-guide-title: ''
source-git-commit: de08d20ea8428939ccfd3f31497c0f17421b9254
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 3%

---


# Gerenciar parâmetros

Quando você precisar controlar parâmetros de alguma forma que não seja ajustá-los diretamente, o Designer oferece várias ações úteis para:

* [Copiar e colar](#copy-paste-parameters) os valores de todos os parâmetros de um nó
* Salve os valores ou todos os parâmetros de um nó em um [arquivo de predefinição](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md), a ser reutilizado posteriormente
* [Exponha os parâmetros](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) dos nós para torná-los acessíveis e vinculá-los
* [Ocultar ou mostrar parâmetros](../../compositing-graphs/visible-control-vis/visible-if-control-visibility-of-inputs-outputs-and-parameters.md) de acordo com os valores de outros parâmetros
* Use um [gráfico de função Substance](../../function-graphs/function-graphs.md) para calcular o valor de um parâmetro

## Ações de parâmetro

As ferramentas disponíveis para gerenciar parâmetros estão disponíveis nos seguintes locais:

### Ações globais

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Quando as propriedades de um nó são exibidas no Dock Propriedades, os parâmetros do nó podem ser gerenciados globalmente usando o menu &#39;<b>Gerenciar parâmetros</b>&#39; no seguinte cabeçalho da seção:

* Para [nós atômicos](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md): parâmetros específicos
* Para [nós de instância](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md): parâmetros de instância

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Menu global &#39;Gerenciar parâmetros&#39; em Propriedades](manage-parameters.resources/manage-parameters-menu-global.png "Menu global &#39;Gerenciar parâmetros&#39; em Propriedades"){zoomable="yes"}

</td>
</tr>
</table>

As ações neste menu afetarão *todos* os parâmetros listados nesta seção:

* <b>Expor parâmetros:</b> abre a caixa de diálogo &#39;Parâmetros de exposição em lote&#39;. Para cada parâmetro exposto, a ação cria uma nova entrada de gráfico e define automaticamente uma função usando essa entrada de gráfico. Saiba mais sobre como expor parâmetros em [esta página dedicada](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md).
* <b>Copiar parâmetros:</b> Consulte a seção [Copiar e colar parâmetros](#copy-paste-parameters) abaixo.
* <b>Colar parâmetros:</b> Consulte a seção [Copiar e colar parâmetros](../../compositing-graphs/manage-parameters/manage-parameters.md) abaixo.
* <b>Salvar parâmetros como um arquivo de predefinição:</b> Saiba mais sobre predefinições de parâmetro em [esta página dedicada](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md).
* <b>Aplicar parâmetros de um arquivo de predefinição:</b> Saiba mais sobre predefinições de parâmetro em [esta página dedicada](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md).
* <b>Redefinir tudo:</b> redefine todos os parâmetros para seus valores e intervalos padrão. Se uma função foi aplicada a qualquer parâmetro, ela é descartada.

>[!NOTE]
>
> Algumas ações não estão disponíveis para alguns nós atômicos. Consulte [Limitações de nós atômicos](#atomic-nodes-limitations) abaixo.

### Ações de parâmetro único

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Para gerenciar um parâmetro *único*, use o menu &#39;<b>Gerenciar função</b>&#39; oposto ao rótulo do parâmetro.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Menu &#39;Gerenciar parâmetros&#39; local em Propriedades](manage-parameters.resources/manage-parameters-menu.png "Menu &#39;Gerenciar parâmetros&#39; local em Propriedades"){zoomable="yes"}

</td>
</tr>
</table>

Você pode aplicar um [gráfico de função Substance](../../function-graphs/the-function-graph/the-function-graph.md) a esse parâmetro de três maneiras:

* <b>Expor como nova entrada de gráfico:</b> cria uma nova entrada de gráfico e define automaticamente uma função usando essa entrada de gráfico. Saiba mais sobre como expor parâmetros em [esta página dedicada](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md).
* <b>Função vazia:</b> crie uma função do zero.
* <b>Valor constante:</b> edite uma função começando de um [nó de valor constante](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) definido como o valor atual do parâmetro.
* <b>Redefinir:</b> redefine o parâmetro para seu valor e intervalo padrão. Se uma função foi aplicada ao parâmetro, ela é descartada.

>[!NOTE]
>
> As ações copiar/colar e arquivo de predefinição são globais para todos os parâmetros e, portanto, não estão disponíveis para parâmetros únicos.

### Menu contextual do nó

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Algumas ações de parâmetro do menu *global* listadas acima estão disponíveis no menu contextual do nó. Clique em RMB em um nó e vá para &#39;Gerenciar parâmetros&#39; para acessá-los.

Observe que as ações de copiar/colar não estão disponíveis nesse menu. Você pode encontrá-las nas propriedades do nó, conforme explicado acima.

As mesmas limitações listadas abaixo para nós atômicos se aplicam a este menu.

</td>
<td width="50.00%" style="border: 0;" valign="top">

![&#x200B; menu&#39;Gerenciar parâmetros&#39; no menu contextual do nó](manage-parameters.resources/manage-parameters-node-menu.png " menu&#39;Gerenciar parâmetros&#39; no menu contextual do nó"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Copiar e colar parâmetros

É possível copiar todos os valores de parâmetros para um nó de origem e colá-los em um nó de destino. Os parâmetros dos nós de origem e de destino são <b>correspondidos com base em seus identificadores e tipos</b>.

Por exemplo, um parâmetro &#39;Scale&#39;, cujo identificador é &#39;scale&#39; e o tipo é &#39;Float&#39;, pode ser copiado e colado em outro parâmetro &#39;Shape Scale&#39; quando seu identificador também é &#39;scale&#39; e seu tipo também é &#39;Float&#39;.

Este recurso funciona da mesma maneira que o uso de um [arquivo de predefinição de parâmetro](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md). Na verdade, os dados copiados para a área de transferência são os mesmos que os dados armazenados nos arquivos predefinidos do SBSPRS e podem ser colados em qualquer editor de texto para serem revisados e editados.

</td>
<td style="border: 0;" valign="top">

![Copiar e colar parâmetros](manage-parameters.resources/copy-paste-parameters.gif "Copiar e colar parâmetros"){zoomable="yes"}

</td>
</tr>
</table>

## Limitações de nós atômicos

Alguns recursos não estão disponíveis para alguns [nós atômicos](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md), devido à sua implementação e controles específicos.

Estas ações...

* [Copiar/colar parâmetros](#copy-paste-parameters)
* [Salvar/aplicar arquivo de predefinição](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)

...não estão disponíveis para estes nós atômicos:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)

[Curva](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)

[Distância](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md)

[FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)

[Gradiente (dinâmico)](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-dynamic/gradient-dynamic.md)

</td>
<td style="border: 0;" valign="top">

[Mapa de gradiente](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md)

[Cor de entrada](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)

[Tons de cinza de entrada](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)

[Valor de entrada](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)

[Saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)

</td>
<td style="border: 0;" valign="top">

[Processador de pixels](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)

[SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)

[Texto](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)

[Cor uniforme](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)

[Processador de valor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
