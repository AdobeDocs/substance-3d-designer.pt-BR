---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/moss-weathering.html"
breadcrumb-title: ''
description: Use o nó Envelhecimento de musgo para adicionar padrões de crescimento de musgo a materiais baseados na curvatura e posição da malha.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Moss Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Molho de água
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 7%

---


# Molho de água

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](moss-weathering.resources/moss-weathering.png){width="128px"}

<b>Entrada:</b> Geradores Baseados em Malha > Clima

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Esse é um efeito de material completo que funciona em vários canais de uma só vez. Ele gera um efeito de musgo supercrescido, com um único controle para a Propagação.

Esse efeito funciona melhor com um mapa de posição do espaço mundial feito bake e um mapa de altura adicional. Embora esse não seja um requisito exato, ele confere ao efeito uma colocação mais confiável.

Certifique-se de entender corretamente os [Modos de Criação de Link](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) ao trabalhar com materiais completos.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Posição</b> <i>Entrada de cores</i> | Posição feita bake no Espaço Mundial. |
| <b>Height</b> <i>Entrada em tons de cinza</i> | Entrada adicional de Heightmap. |
| <b>Máscara</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. Pode ser alternado com o parâmetro “Máscara”. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Canais</b> | Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza. |
| <b>Avançado</b> |  |
| <b>Formato Normal</b> <i>DirectX, OpenGL</i> | Alterna entre diferentes formatos de Mapas Normais (inverte o canal verde). |
| <b>Máscara</b> <i>Falso/Verdadeiro</i> | Ativa ou desativa o uso do Mapa de máscaras. |
| <b>Efeito</b> |  |
| <b>Propagação de Moss</b> <i>0.0 - 1.0</i> | Define a propagação do musgo. Cresce em passos de pouca cobertura para musgo pesado, espesso e escuro. |
| <b>Mesclagem</b> |  |
| <b>Intensidade de Difusão</b> <i>0.0 - 1.0</i> | Intensidade de mesclagem do Difusa. |
| <b>Intensidade de Cor de base</b> <i>0.0 - 1.0</i> | Intensidade de mesclagem da Cor de base. |
| <b>Intensidade normal</b> <i>0.0 - 1.0</i> | Intensidade de mesclagem do Normal. |
| <b>Intensidade de Specular</b> <i>0.0 - 1.0</i> | Intensidade de mistura do Specular. |
| <b>Intensidade de brilho</b> <i>0.0 - 1.0</i> | Intensidade de mistura da Textura reluzente. |
| <b>Intensidade de aspereza</b> <i>0.0 - 1.0</i> | Intensidade de mistura da aspereza. |
| <b>Intensidade de Oclusão de ambiente</b> <i>0.0 - 1.0</i> | Intensidade de mesclagem da Oclusão ambiente. |
| <b>Intensidade de Height</b> <i>0.0 - 1.0</i> | Intensidade de mistura do Height. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="moss-weathering.resources/moss-ex.gif" />
        </td>
    </tr>
</table>
