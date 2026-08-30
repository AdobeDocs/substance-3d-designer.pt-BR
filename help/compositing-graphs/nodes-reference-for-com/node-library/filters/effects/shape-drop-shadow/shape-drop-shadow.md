---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-drop-shadow.html"
breadcrumb-title: ''
description: Use o nó Sombra projetada da forma para adicionar efeitos de sombra projetada às formas para criar profundidade e dimensão no textura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Drop Shadow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sombra projetada da forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 6%

---


# Sombra projetada da forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-drop-shadow.resources/shape-dropshadow-grayscale.png){width="128px"}

![](shape-drop-shadow.resources/shape-dropshadow.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Executa o conhecido efeito “Sombra projetada” de outro software de processamento de imagens 2D, em uma máscara em preto e branco de entrada (para a versão em tons de cinza) ou imagem com transparência (para a versão colorida).

Ele difere do efeito [Sombras](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shadows-filter-node/shadows-filter-node.md) por retornar imagens com transparência total aplicada, proporcionando um efeito mais completo semelhante ao que você esperaria em outro software.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Ângulo</b> <i>0.0 - 1.0</i> | Ângulo de incidência da luz (falsa). |
| <b>Distância</b> <i>-0.5 - 0.5</i> | Distancie o menu suspenso de sombras até/afaste-se da forma. |
| <b>Tamanho</b> <i>0.0 - 1.0</i> | Controla o desfoque/fuzzines da sombra. |
| <b>Propagação</b> <i>0.0 - 1.0</i> | Corte/limite para o efeito de desfoque faz com que a sombra se espalhe ainda mais. |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Opacidade de mistura para o efeito de sombra. |
| <b>(Sombra) Cor</b> <i>(Valor da cor)</i> | Tonalidade de cor a ser aplicada à sombra. |
| <b>Cor da máscara</b> <i>(Valor da cor) (Somente Versão em Tons de Cinza)</i> | Cor sólida a ser usada para a saída mapeada de transparência. |
| <b>A Entrada É Pré-Multiplicada</b> <i>Falso/Verdadeiro (Somente Versão Colorida)</i> | Se a entrada deve ser assumida como pré-multiplicada. |
| <b>Saída Pré-Multiplicada</b> <i>Falso/Verdadeiro</i> | Se a saída deve ser pré-multiplicada. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-drop-shadow.resources/dropshadowex.png" />
        </td>
    </tr>
</table>
