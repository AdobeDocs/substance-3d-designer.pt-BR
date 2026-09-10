---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/smart-auto-tile.html"
breadcrumb-title: ''
description: Use o nó Bloco Automático Inteligente para criar blocos gráficos perfeitos automaticamente a partir de materiais digitalizados usando a detecção inteligente de padrões.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Smart Auto Tile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bloco Automático Inteligente
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 5%

---


# Bloco Automático Inteligente

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](smart-auto-tile.resources/smart-auto-tile.png){width="128px"}

<b>Entrada:</b> Filtros Materiais > Processamento de materiais escaneados

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Esse nó transforma um conjunto não ladrilhado de mapas Basecolor, Normal e Heightmaps em uma versão ladrilhada de acordo com a análise inteligente das entradas. É semelhante a [Criar foto lado a lado](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md), mas muito mais avançado, pois usa informações de todos os canais para misturar as coisas da maneira mais inteligente (semelhante ao que o [Clonar correção](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md) faz). Ele também tem uma função interna [Cortar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) para determinar qual área usar ao colocar lado a lado. Certifique-se de [ler mais sobre o nó Cortar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) para entender essa função corretamente.

Para usar este nó, comece definindo a área Cortada e use as configurações de Borda para determinar como as bordas lado a lado são mescladas no centro. Os parâmetros de limiar são de importância fundamental para isso! Lembre-se de que áreas grandes e uniformes não funcionam muito bem com esse efeito. Quanto mais detalhes e formas existirem, mais será necessário trabalhar com elas.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Máscara</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. Pode ser alternado com o parâmetro “Usar máscara”. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Cortar</b> |  |
| <b>Tamanho de entrada</b> <i>0 - 8192</i> | Insira a resolução e as proporções das imagens. Muito importante para imagens não quadradas. |
| <b>Transformar</b> <i>(Matriz de Transformação)</i> | Gira e dimensiona o resultado. O resultado pode ser modificado ao interagir diretamente com a tela. |
| <b>Deslocamento</b> <i>0.0 - 1.0</i> | Move ou traduz o resultado. O resultado pode ser modificado ao interagir diretamente com a tela. |
| <b>Borda</b> |  |
| <b>Detectar bordas</b> <i>Falso/Verdadeiro</i> | Ativa ou desativa a mesclagem de borda especial detectada. |
| <b>Usar Limite Por Canal</b> <i>Falso/Verdadeiro</i> | Alterna entre um valor de limite global ou um para cada canal. |
| <b>Limite</b> <i>0.0 - 1.0</i> |  |
| <b>Cor de base de Limite</b> <i>0.0 - 1.0</i> |  |
| <b>Limite Normal</b> <i>0.0 - 1.0</i> |  |
| <b>Height de Limite</b> <i>0.0 - 1.0</i> |  |
| <b>Cortar deslocamento</b> <i>0.0 - 0.5</i> | Controle principal para mover o corte, ambos os eixos X e Y são separados. |
| <b>Desfoque</b> <i>0.0 - 2.0</i> | Desfoca a transição de mesclagem. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Controla a irregularidade dos resultados da análise de borda. |
| <b>Resolução da Grade</b> <i>1 - 11</i> | Resolução de qualidade da análise de bordas. |
| <b>Usar Cor de base</b> <i>Falso/Verdadeiro</i> | Alterna o processamento de Cor de base (entrada e saída). |
| <b>Usar Normal</b> <i>Falso/Verdadeiro</i> | Alterna o processamento Normal (entrada e saída). |
| <b>Usar Height</b> <i>Falso/Verdadeiro</i> | Alterna o processamento Normal (entrada e saída). |
| <b>Usar máscara</b> <i>Falso/Verdadeiro</i> | Ativa ou desativa o uso do Mapa de máscaras para formas de máscara de carimbo personalizadas. |
