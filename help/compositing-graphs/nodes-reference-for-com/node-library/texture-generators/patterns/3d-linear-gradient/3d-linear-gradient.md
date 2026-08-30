---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-linear-gradient.html"
breadcrumb-title: ''
description: Use o nó 3D linear gradient para criar gradientes lineares com base na posição do mundo 3D para efeitos espaciais.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Linear Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D linear gradient
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---


# 3D linear gradient

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-linear-gradient.resources/3d-linear-gradient.png){width="128px"}

<b>Em:</b> Geradores De Textura > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Cria um gradiente volumétrico com base no mapa de posição de entrada. Gera efetivamente uma transição de preto para branco entre 2 pontos no espaço 3D. Projetado para uso apenas com o mecanismo de GPU.

Consulte também [Máscara de volume 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) para obter um efeito semelhante.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Modo de Posição de Pontos</b> <i>Posições UV, Posições Espaciais Mundiais</i> | Escolha se os Pontos de gradiente funcionam no espaço UV (funcionam melhor ao defini-los em Visualização 2D) ou em coordenadas 3D, se desejar inserir manualmente uma posição exata. |
| <b>Ponto 1</b> | Ponto inicial do gradiente. Podem ser coordenadas 2D ou 3D com base no modo de posição. |
| <b>Ponto 2</b> | Ponto final do gradiente. Podem ser coordenadas 2D ou 3D com base no modo de posição. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta o contraste do resultado. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-linear-gradient.resources/3d-gradient.gif" />
        </td>
    </tr>
</table>
