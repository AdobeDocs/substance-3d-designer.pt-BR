---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/glow.html"
breadcrumb-title: ''
description: Use o nó Brilho para adicionar efeitos de brilho às texturas para criar aparências de material luminoso e de emissivo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Brilho
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 5%

---


# Brilho

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](glow.resources/glow-01.png){width="128px"}

![](glow.resources/glow-02.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Executa um efeito do tipo “Brilho externo”, como visto em outros softwares populares de edição de imagens. Basicamente, adiciona um contorno de gradiente esmaecido ao redor da entrada.

Lembre-se de que esse recurso não deve funcionar para imagens com canais alfa, como seria de esperar. Mesmo a versão colorida espera apenas máscaras binárias, pretas e brancas como entrada; ela só permite o uso de um brilho colorido. Se você está atrás de uma versão que funcione em imagens com transparência, consulte [Brilho da forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-glow/shape-glow.md).

Importante: certifique-se de usar a versão apropriada para sua entrada! Use “Brilho” para entradas de cor ou “Escala de cinza brilhante” para entradas de tons de cinza.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Quantidade de brilho</b> <i>0.0 - 1.0</i> | Opacidade global do efeito de brilho. |
| <b>Limpar Valor</b> <i>0.0 - 1.0</i> | Limite para quando cortar o efeito de brilho. Útil para áreas semitransparentes. |
| <b>Tamanho do brilho</b> <i>0.0 - 20.0</i> | Controla o quanto o efeito de brilho alcança. |
| <b>Cor do brilho</b> <i>(Valor da cor) (Somente Versão da Cor)</i> | Define a cor do efeito de brilho. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="glow.resources/glow-03.png" />
        </td>
    </tr>
</table>
