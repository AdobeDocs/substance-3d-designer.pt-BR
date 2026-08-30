---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leaks.html"
breadcrumb-title: ''
description: Use o nó Vazamentos para gerar padrões de vazamento com base na geometria de malha para criar manchas de água e efeitos de fluido.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leaks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Vazamentos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 3%

---


# Vazamentos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](leaks.resources/leaks.png){width="128px"}

<b>Entrada:</b> Geradores > Geradores de máscara Baseados em Malha

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esse nó representa listras de vazamento de dirt e sujeira provenientes de bordas nítidas. À medida que as listras são geradas com a Posição assada, elas sempre correm para baixo.

Experimente alterar a máscara de variação: como ela orienta o posicionamento das listras, pode ter uma influência muito maior do que com outros geradores de máscaras.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Posição</b> <i>Entrada em tons de cinza</i> | Mapa de posição assado, usado para direções de riscas. Obrigatório! |
| <b>Curvatura</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para o posicionamento da faixa. Obrigatório! |
| <b>Oclusão de ambiente</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para efeitos internos e mascaramento. Recomendado, mas você pode usar branco plano. |
| <b>Espaço Mundial Normal</b> <i>Entrada de cores</i> | Baked World Space Normalmap, usado para a direção da faixa. Obrigatório! |
| <b>Máscara de Variação</b> <i>Entrada em tons de cinza</i> | Máscara de variação opcional, ative definindo a substituição como True. |
| <b>Máscara (opcional)</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Nível</b> <i>0.0 - 1.0</i> | Nível total do resultado. Progressivamente revela o efeito, afeta o comprimento também. Deve ser ajustado razoavelmente alto para obter gotas longas. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta o contraste do resultado. |
| <b>Variação</b> <i>0.0 - 1.0</i> | Define a quantidade de variação de grande escala usada para mascarar as listras. Definir esse valor como 0 leva a listras totalmente uniformes, portanto, evite isso. |
| <b>Comprimento</b> <i>0.0 - 8.0</i> | Comprimento das gotas da faixa. A definição desse valor muito alto em uma escala pequena resultará em etapas visíveis. Brinque também com o Level. |
| <b>Ocultar</b> <i>X, Y, Z, Nenhum</i> | Define a direção que o AO deve afetar. |
| <b>Substituir máscara de variação</b> <i>Falso/Verdadeiro</i> | Permite a substituição da máscara de variação por um slot de entrada personalizado. Usar máscaras mais esparsas ou mais densas pode ser interessante e é uma boa maneira de controlar os gotejamentos. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="leaks.resources/leaks-ex.gif" />
        </td>
    </tr>
</table>
