---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
breadcrumb-title: ''
description: Use o nó Caustics para gerar padrões de luz cáustica para criar efeitos de iluminação subaquática e refrativa.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Caustics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cáustica
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 5%

---


# Cáustica

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](caustics.resources/caustics-01.png){width="128px"}

<b>Entrada:</b> Geradores de Textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera cáustica projetada com base em um mapa de altura e uma direção de luz.Vem nas versões Tons de cinza e coloridas, as diferenças são sutis, mas a versão colorida adiciona efeitos de dispersão de cores. A luz é projetada a partir de um único ponto; nenhum mapa de ambiente é usado.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Espaço de cores de saída</b> <i>Raw, sRGB</i> | Defina o espaço da cor de saída. |
| <b>Tamanho da grade de fótons</b> <i>Automático, 512, 1024, 2048, 4096</i> | Define a qualidade ajustando o tamanho da grade, mas o padrão é a entrada correspondente. Pode ser usado para acelerar o cálculo. |
| <b>Escala do Height da superfície</b> <i>0.0 - 1.0</i> | Multiplicador para determinar como o height é interpretado. |
| <b>Posição do Height da Superfície</b> <i>0.0 - 1.0</i> | Definir distância da superfície de refração para projeção. |
| <b>Superfície IOR</b> <i>1.0 - 2.0</i> | Definir o índice de refração, na versão colorida, isso adiciona mais dispersão de cores. |
| <b>Tamanho do fóton</b> <i>1.0 - 50.0</i> | O tamanho do fóton afeta a nitidez do efeito. |
| <b>Dispersão</b> <i>0.0 - 0.01 (somente versão de cores)</i> | Afeta apenas a dispersão de cores. Não visível quando a taxa de transferência interna é baixa. |
| <b>Tremulação</b> <i>0.0 - 1.0</i> | Adicione tremulação irregular às partículas de fóton fundidas. |
| <b>Posição da luz</b> | Move a posição da luz. Também feito por meio de um gizmo na exibição 2D. |
| <b>Cor do plano de fundo</b> <i>(Valor da cor) (Somente versão da cor)</i> | Altere a cor do plano de fundo. Limitado a preto na versão em tons de cinza. |
| <b>Expansão não quadrada</b> <i>Falso/Verdadeiro</i> | Habilite a compensação de abóbora e estiramento com proporções não quadradas. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="caustics.resources/caustics-02.png" />
        </td>
    </tr>
</table>
