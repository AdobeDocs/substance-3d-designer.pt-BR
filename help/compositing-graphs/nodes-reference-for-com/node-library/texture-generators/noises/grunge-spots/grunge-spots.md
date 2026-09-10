---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/grunge-spots.html"
breadcrumb-title: ''
description: Use o nó Pontos do Desgaste para gerar padrões de pontos para adicionar efeitos de desgaste e desgaste aos materiais.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Grunge Spots
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pontos de desgaste
user-guide-description: ''
user-guide-title: ''
source-git-commit: 988f0cb19339a2ab3ca4ef392fef7ca723254cd9
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---


# Pontos de desgaste

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](grunge-spots.resources/grungespots.jpg){width="200px"}

<b>Entrada:</b> Geradores de Textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O nó **Pontos de Desgaste** gera um mapa de desgaste semelhante a pontos espalhados finos.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Saldo</b> <i>Flutuante</i> | Ajusta o equilíbrio entre valores escuros e brilhantes. |
| <b>Contraste</b> <i>Flutuante</i> | Ajusta o contraste da imagem. |
| <b>Inverter</b> <i>Booleano</i> | Inverte a saída da imagem, usando uma operação `1-x`. |
| <b>Expansão não quadrada</b> <i>Booleano</i> | Permite a compensação de esmagamento e alongamento com proporções não quadradas. |
| <b>Avançado</b> |  |
| <b>Detalhes</b> <i>Flutuante</i> | Ajusta a quantidade de manchas *distorcidas* e divididas em pontos mais finos. |
| <b>Cobertura</b> <i>Flutuante</i> | Ajusta a cobertura das manchas na imagem. |
| <b>Contraste de cobertura</b> <i>Precisão decimal</i> | Ajusta o contraste da *máscara* usada para controlar a cobertura das manchas na imagem. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="grunge-spots.resources/grungespots-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="grunge-spots.resources/grungespots-variant.jpg" />
        </td>
    </tr>
</table>
