---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs.html"
breadcrumb-title: ''
description: Saiba mais sobre gráficos de composição de Substance no Substance 3D Designer para criar texturas de procedimento e fluxos de trabalho de material.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gráficos do Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e53313d3c368803a95ebb1f9eee712ae2a05817
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 1%

---


# Gráficos do Substance

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](substance-compositing-graphs.resources/graph-5.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td width="100.00%" style="border: 0;" valign="top">

[gráficos de Substance](https://substance3d.adobe.com/) são o tipo principal de gráfico criado no Substance 3D Designer. A finalidade é <b>gerar e processar dados de imagem 2D</b> que não estejam restritos a uma resolução, cor ou forma definidas. Eles são feitos com ferramentas extremamente versáteis de processamento de imagens e geração, não apenas resultados estáticos e predefinidos.

Os resultados podem estar na forma de um padrão simples em preto e branco, um filtro que roda apenas em outras imagens e não gera conteúdo por si só, ou mesmo um material de procedimento completo com vários canais.

gráficos de Substance são[o tipo de gráfico mais amplamente suportado](../getting-started/overview/overview.md) e podem ser exportados e usados em uma infinidade de fluxos de trabalho diferentes.

</td>
</tr>
</table>

## Exemplos

Abaixo você pode encontrar alguns exemplos típicos de casos de uso comuns.

+++Forma simples
![Forma simples no gráfico de Substance](substance-compositing-graphs.resources/simpleshape.png "Forma simples no gráfico de Substance"){width="512px"}



Uma forma de máscara simples para um decalque é criada gerando[um pedaço de texto](../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) e uma [forma de disco](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape/shape.md), [extraindo a borda](../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md) do disco e finalmente [mesclando-os](../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) antes de defini-los como saída final [9}.](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)

O Texto com o número, ou o thickness da aresta, pode ser exposto externamente para tornar este um gráfico mais dinâmico.

+++

+++Filtro de ajuste
![Filtro de ajuste no gráfico de Substance](substance-compositing-graphs.resources/simplefilter.png "Filtro de ajuste no gráfico de Substance"){width="512px"}



Um gráfico de filtro usa um mapa normal como [entrada](../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)(com uma visualização personalizada), [converte-o em curvatura](../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) e depois [ajusta o contraste](../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) para criar uma máscara de bordas convexas como [saída](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) final.

Os valores de contraste definidos no Histograma podem ser expostos, tornando-o um filtro simples, mas útil, em combinação com o slot de entrada dinâmico.

+++

+++Material completo
![Material completo no gráfico de Substance](substance-compositing-graphs.resources/simplematerial.png "Material completo no gráfico de Substance"){width="512px"}



Um gráfico mais complicado[mescla dois Materiais de base](../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-blend/material-blend.md). Um [Material de base](../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) é mantido simples, o outro usa algumas entradas personalizadas para adicionar interesse. Uma máscara é usada para determinar qual dos dois materiais aparece onde antes de ser definido como [saídas](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) finais.

Este exemplo usa os [Modos de Criação de Link](../interface/the-graph-view/link-creation-modes/link-creation-modes.md) para simplificar usando vários links.

+++
