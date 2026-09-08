---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/highpass.html"
breadcrumb-title: ''
description: Use o nó Highpass para extrair detalhes de alta frequência do textura para criar efeitos de nitidez e aprimoramento de detalhes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Highpass
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# Highpass

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/high-pass-greyscale.png){width="128px"}

![](../../../../../../assets/high-pass.png){width="128px"}

<b>Entrada:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Executa um filtro Highpass, disponível em cores e em uma versão em tons de cinza. Semelhante à ação Photoshop com o mesmo nome.\
Útil para remover grandes diferenças de luminância em imagens, como ao limpar texturas para divisão em blocos gráficos.

Importante: certifique-se de usar a versão apropriada para sua entrada! Use “Highpass” para entradas de cor e “Highpass Grayscale” para entradas de tons de cinza.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Raio</b> <i>0.0 - 64.0</i> | Raio do filtro: um raio pequeno remove pequenas diferenças, um raio maior remove áreas grandes. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/highpass.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/highpass-example.png" />
        </td>
    </tr>
</table>
