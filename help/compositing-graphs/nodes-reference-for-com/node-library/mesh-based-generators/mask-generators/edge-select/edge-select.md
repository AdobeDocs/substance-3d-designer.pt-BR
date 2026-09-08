---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: Use o nó Seleção de borda para gerar máscaras selecionando bordas de malha para criar efeitos de intemperismo e desgaste baseados em bordas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Seleção de borda
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 7%

---


# Seleção de borda

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/edge-select.png){width="128px"}

<b>Entrada:</b> Geradores > Geradores de máscara Baseados em Malha

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara é a melhor maneira de selecionar qualquer tipo de borda com base na curvatura. Convexo, Côncavo em qualquer nível ou contraste pode ser isolado, fornecendo um atalho excelente para evitar fazer isso manualmente por meio de um [nó Níveis](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para realçar bordas. Obrigatório! |
| <b>Máscara (opcional)</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Nível</b> <i>0.0 - 1.0</i> | Define a quantidade total de realce de borda para Convexo e Côncavo. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta o contraste do realce para Convexo e Côncavo. |
| <b>Convexo</b> |  |
| <b>Largura das Bordas Convexas</b> <i>0.0 - 1.0</i> | Define a largura do realce para bordas convexas. Lembre-se de que aumentar ligeiramente a Suavidade pode levar a bordas mais finas. |
| <b>Suavidade convexa</b> <i>0.0 - 1.0</i> | Defina a suavidade da transição para bordas convexas. |
| <b>Intensidade de convexo</b> <i>0.0 - 1.0</i> | Define a intensidade máxima do realce de Borda para bordas convexas. Defina como 0 para nenhum realce. |
| <b>Côncavo</b> |  |
| <b>Largura das Bordas Côncavas</b> <i>0.0 - 1.0</i> | Defina a largura do realce para bordas côncavas. Lembre-se de que aumentar ligeiramente a Suavidade pode levar a bordas mais finas. |
| <b>Suavidade côncava</b> <i>0.0 - 1.0</i> | Defina a suavidade da transição para bordas côncavas. |
| <b>Intensidade côncava</b> <i>0.0 - 1.0</i> | Defina a intensidade máxima do realce de Aresta para bordas côncavas. Defina como 0 para nenhum realce. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/edge-select-ex.gif" />
        </td>
    </tr>
</table>
