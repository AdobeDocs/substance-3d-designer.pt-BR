---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/working-with-3d-scenes/extracting-materials-values-and-textures.html"
breadcrumb-title: ''
description: Extraia propriedades de material de cenas 3D para usar em gráficos de Substance para fluxos de trabalho de criação de material.
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Extracting materials values and textures
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extraindo valores e texturas de materiais
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 0%

---


# Extraindo valores e texturas de materiais

As propriedades dos materiais podem ser extraídas para serem usadas em gráficos de Substance.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Novo gráfico a partir de texturas

</td>
<td style="border: 0;" valign="top">

### Extrair textura

</td>
<td style="border: 0;" valign="top">

### Extrair valor

</td>
</tr>
</table>

## Novo gráfico a partir de texturas

A ação “Criar gráfico a partir das entradas de textura” cria um novo gráfico de Substance com todas as texturas usadas por um material

Algumas coisas acontecem ao usar esta ação:

* Um gráfico de Substance com o nome do material criado no local selecionado.
* Um [recurso de bitmap](../../resources/bitmap-resource/bitmap-resource.md) é criado para cada textura usada pelo material e colocado em uma pasta nomeada após o material, em uma pasta “Recursos”.
* No gráfico, os nós [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) são criados para cada um desses recursos de bitmap e conectados automaticamente aos nós [Saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) configurados após as propriedades de material que usam texturas.
* Se cada canal de uma mesma textura for usado para orientar propriedades de material diferentes (a técnica é chamada de [embalagem de canal](../../glossary/glossary.md)), os nós de [conversão de tons de cinza](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/grayscale-conversion/grayscale-conversion.md) serão adicionados automaticamente para selecionar os canais apropriados.
* O gráfico é conectado automaticamente ao material e sua aparência não deve ser alterada até que você faça edições no gráfico.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Criar gráfico a partir das entradas de textura - Ação no visor &#39;Exibição 3D&#39;](../../assets/createGraphFromTexturesActionViewport.png "Criar gráfico a partir das entradas de textura - Ação no visor &#39;Exibição 3D&#39;"){zoomable="yes"}

*Ação no visor 3D*

</td>
<td style="border: 0;" valign="top">

![Criar gráfico a partir das entradas de textura - Ação no menu &#39;Materiais&#39;](../../assets/createGraphFromTexturesActionMaterials.png "Criar gráfico a partir das entradas de textura - Ação no menu &#39;Materiais&#39;"){zoomable="yes"}

*Ação no menu Materiais*

</td>
<td style="border: 0;" valign="top">

![Criar gráfico a partir de entradas de textura - Ação no encaixe &#39;Propriedades&#39;](../../assets/createGraphFromTexturesActionProps.png "Criar gráfico a partir de entradas de textura - Ação no encaixe &#39;Propriedades&#39;"){zoomable="yes"}

*Ação na área de Propriedades*

</td>
</tr>
</table>

![Resultado da criação de gráfico a partir de texturas de material](../../assets/createGraphFromTexturesResult.png "Resultado da criação de gráfico a partir de texturas de material"){zoomable="yes"}

*Resultado da criação do gráfico a partir de texturas de material*

+++Demonstração
![Criar gráfico a partir de entradas de textura - Demonstração](../../assets/createGraphFromTextures.gif "Criar gráfico a partir de entradas de textura - Demonstração"){zoomable="yes"}



+++

>[!TIP]
>
> É possível acessar a ação rápida e diretamente na janela de visualização 3D, colocando o cursor no objeto e pressionando <b>Shift+LMB</b> para selecioná-lo. em seguida, clique em RMB para acessar um menu contextual que hospeda a ação.

>[!NOTE]
>
> Para formatos que usam *texturas incorporadas* (por exemplo: USDZ), as texturas precisam ser extraídas e copiadas em disco. Isso resulta em uma etapa adicional para selecionar o local para o qual as texturas devem ser extraídas.

## Extrair textura

A ação “Extrair textura para gráfico” cria um novo nó Bitmap em um gráfico existente para uma textura usada por um material.

Algumas coisas acontecem ao usar esta ação:

* Um [recurso de bitmap](../../resources/bitmap-resource/bitmap-resource.md) é criado para a textura usada pelo material e colocado em uma pasta nomeada após o material, em uma pasta “Recursos”.
* No gráfico selecionado, um nó [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) é criado para esse recurso de bitmap e conectado automaticamente a um nó [Saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) configurado após a propriedade de material que usa essas texturas.

Se uma Saída configurada para a propriedade de material *já existir* no gráfico, *nenhum nó será criado* e apenas a criação do recurso de bitmap será executada.

Por exemplo: extrair uma textura da propriedade “Cor base” para um gráfico que já hospeda um nó de saída configurado para “Cor base” resultará em nenhum nó criado no gráfico.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Extrair textura para gráfico - Ação no encaixe Propriedades](../../assets/extractTextureAction.png "Extrair textura para gráfico - Ação no encaixe Propriedades"){zoomable="yes"}

Ação para a propriedade de material na área de Propriedades

</td>
<td style="border: 0;" valign="top">

![Extrair textura para gráfico - caixa de diálogo “Selecionar gráfico de destino”](../../assets/extractTextureSelectGraph.png "Extrair textura para gráfico - caixa de diálogo “Selecionar gráfico de destino”"){zoomable="yes"}

Caixa de diálogo “Selecionar gráfico de destino”

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

![Resultado da extração de textura](../../assets/extractTextureResult.png "Resultado da extração de textura"){zoomable="yes"}

Resultado da extração da textura

+++Demonstração
![Extrair textura para gráfico - Demonstração](../../assets/extractTextureToGraph.gif "Extrair textura para gráfico - Demonstração"){zoomable="yes"}



+++

A ação “Extrair textura como recurso” cria apenas um recurso de bitmap para a textura usada pelo material e o coloca em uma pasta nomeada em homenagem ao material, na pasta “Recursos”.

>[!NOTE]
>
> Para formatos que usam *texturas incorporadas* (por exemplo: USDZ), a textura precisa ser extraída e copiada em disco. Isso resulta em uma etapa adicional para selecionar o local para o qual a textura deve ser extraída.

## Extrair valor

A ação “Extrair valor para gráfico” cria um novo nó [Processador de valores](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) em um gráfico existente para um valor de propriedade de material.

Algumas coisas acontecem ao usar esta ação:

* No gráfico selecionado, um nó [Processador de valores](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) é criado para esse valor de propriedade e conectado automaticamente a um nó [Saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) configurado após essa propriedade de material.
* No [gráfico de função Substance](../../function-graphs/function-graphs.md) do nó Processador de valores, um [nó de constante](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) correspondente ao tipo de valor é criado, definido como o valor extraído conforme definido como a saída do gráfico.

Se uma Saída configurada para a propriedade de material *já existir* no gráfico, *nenhum nó será criado*.

Por exemplo: extrair um valor da propriedade “nível de Anisotropia” para um gráfico que já hospeda um nó de saída configurado para “nível de Anisotropia” resultará na ausência de nós criados no gráfico.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Extrair valor para gráfico - Ação no Dock de propriedades](../../assets/extractValueAction.png "Extrair valor para gráfico - Ação no Dock de propriedades"){zoomable="yes"}

Ação para a propriedade de material na área de Propriedades

</td>
<td style="border: 0;" valign="top">

![Extrair valor para gráfico - caixa de diálogo “Selecionar gráfico de destino”](../../assets/extractValueSelectGraph.png "Extrair valor para gráfico - caixa de diálogo “Selecionar gráfico de destino”"){zoomable="yes"}

Caixa de diálogo “Selecionar gráfico de destino”

</td>
<td style="border: 0;" valign="top">

![Extrair valor para o gráfico - Nó constante na função do nó do processador de valores](../../assets/extractValueResult2.png "Extrair valor para o gráfico - Nó constante na função do nó do processador de valores"){zoomable="yes"}

Nó constante na função do nó do processador de valor

</td>
</tr>
</table>

![Resultado da extração de valor](../../assets/extractValueResult.png "Resultado da extração de valor"){zoomable="yes"}

Resultado da extração do valor

+++Demonstração
![Extrair valor para gráfico - Demonstração](../../assets/extractValueToGraph.gif "Extrair valor para gráfico - Demonstração"){zoomable="yes"}



+++
