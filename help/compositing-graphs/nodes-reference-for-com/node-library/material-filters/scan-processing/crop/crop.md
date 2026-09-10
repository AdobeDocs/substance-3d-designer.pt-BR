---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/crop.html"
breadcrumb-title: ''
description: Use o nó Cortar para cortar as saídas de material em regiões específicas para processar materiais e texturas digitalizados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cortar
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 3%

---


# Cortar

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](crop.resources/crop-10.png){width="128px"}

![](crop.resources/crop-grayscale.png){width="128px"}

<b>Entrada:</b> Filtros Materiais > Processamento de materiais escaneados

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O Corte é uma versão paramétrica e não destrutiva da conhecida ferramenta de corte. Você seleciona uma área de uma imagem e o resultado é retornado com as áreas não selecionadas descartadas.

Pode ser útil de várias maneiras, pois realizar uma operação Cortar com nós atômicos não é tão simples. Especialmente para converter imagens não quadradas, esse nó é útil. Certifique-se de definir a resolução de entrada corretamente nesse caso.

É muito importante entender que, para usar este nó com facilidade, você deve fazer bom uso da capacidade de visualizar um nó diferente daquele cujos parâmetros você está editando!\
Resumindo: **Clique duas vezes** no nó que você está usando como entrada para este (a imagem original não cortada) e **clique uma vez** no nó de corte que se segue logo após ele. Em seguida, você pode modificar o gizmo de corte para se ajustar à área que deseja cortar.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Tamanho de entrada</b> <i>0 - 8192</i> | Resolução e proporções da imagem de entrada. Muito importante para imagens não quadradas. |
| <b>Fundo</b> <i>(Valor da cor) / (Valor em tons de cinza)</i> | Valor uniforme do plano de fundo para as áreas não cobertas pela cultura. |
| <b>Transformar</b> <i>(Matriz de Transformação)</i> | Gira e dimensiona o resultado. O resultado pode ser modificado ao interagir diretamente com a tela. |
| <b>Deslocamento</b> <i>0.0 - 1.0</i> | Move ou traduz o resultado. O resultado pode ser modificado ao interagir diretamente com a tela. |
| <b>É Normal (somente para a versão Color)</b> <i>Falso/Verdadeiro</i> | Se a entrada deve ou não ser tratada como um mapa normal. |
