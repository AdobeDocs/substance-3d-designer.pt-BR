---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/fabric-weathering.html"
breadcrumb-title: ''
description: Use o nó Envelhecimento de malha para adicionar efeitos de desgaste e envelhecimento aos materiais de malha com base na geometria e curvatura da malha.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Fabric Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Clima de tecido
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6eb38d6ccaadda1d070e4e0b67311312adb7d082
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 8%

---


# Clima de tecido

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/fabric-weathering.png){width="128px"}

<b>Entrada:</b> Geradores Baseados em Malha > Clima

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Esse é um efeito de material completo que funciona em vários canais de uma só vez. Adiciona um efeito de desgaste de tecido aleatório, com controle para idade e sujeira.<br>Este efeito não funciona muito bem, a menos que você tenha o AO feito bake e os World Space Normalmaps conectados, pois eles são necessários para calcular e gerar tudo adequadamente.

Certifique-se de entender completamente os [Modos de Criação de Link](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) ao trabalhar com materiais completos.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Oclusão de ambiente</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para efeitos internos e mascaramento. |
| <b>Espaço Normal no Mundo</b> <i>Entrada de cores</i> |  |
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
| <b>Dust</b> <i>0.0 - 1.0</i> | Combinar em um efeito de dust mais escuro, com base em áreas voltadas para cima no World Space Normalmap. |
| <b>Sujeira</b> <i>0.0 - 1.0</i> | Combinar em um efeito de dirt/mancha global, com base principalmente em áreas ocultadas (escuras) no AO. |
| <b>Bordas Vestindo</b> <i>0.0 - 1.0</i> | Adiciona um efeito de nitidez/intensificação às bordas, com base no Normal do material. |
| <b>Usado</b> <i>0.0 - 1.0</i> | Combinar em dirt acumulado muito escuro em vincos, com base em AO. Os valores máximo e mínimo tendem a ser muito extremos. Use-os com cuidado. |
| <b>Idade</b> <i>0.0 - 1.0</i> | Combinar sobre um padrão global de desgaste de ladrilhos. O controle de limite abaixo controla a influência do AO. Os valores Máximo e Mínimo tendem a ser muito extremos. |
| <b>Limite de Idade</b> <i>0.0 - 1.0</i> | Define a extensão em que o AO afeta o parâmetro Age. |
| <b>Aumentos de Idade</b> <i>0.0 - 1.0</i> | Controla a mesclagem de vincos adicionais sutis no efeito Idade. |
| <b>Escala de Scratches de Bordas Nítidas</b> <i>1.0 - 32.0</i> | Define a escala de pequenos riscos, que removem principalmente o efeito Usado e Idade. |
| <b>Intensidade de distorção de Scratches de bordas cortantes</b> <i>0.0 - 1.0</i> | Define a intensidade da distorção para os pequenos arranhões acima. |
| <b>Remoção de Saturação de Malha Antiga</b> <i>0.0 - 1.0</i> | Controla a dessaturação do efeito Idade. |
| <b>Brilho do tecido antigo</b> <i>0.0 - 1.0</i> | Controla o brilho do efeito Idade. *Este é um parâmetro muito importante a ser alterado para obter a aparência desejada, mas os resultados podem ser extremos: use com alterações sutis.* |
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
            <img src="../../../../../../assets/fabric-ex.gif" />
        </td>
    </tr>
</table>
