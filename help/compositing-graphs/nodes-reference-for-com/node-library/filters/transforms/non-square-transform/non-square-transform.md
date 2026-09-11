---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: Use o nó Transformação não quadrada para aplicar transformações a texturas não quadradas com dimensionamento independente de X e Y.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformação não quadrada
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 4%

---


# Transformação não quadrada

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](non-square-transform.resources/safe-transform.png)

![](non-square-transform.resources/safe-transform-grayscale.png)

<b>Entrada:</b> Filtros > Transformas

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Versão não segura para quadrados de [Transformar 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Detecta automaticamente proporções não quadradas e pode transformar imagens de entrada quadradas em uma tela não quadrada.

Certifique-se de entender completamente os [Parâmetros de Gráfico](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)para fazer o melhor uso deste nó, pois você precisará definir algumas configurações corretamente:

* O tamanho do seu **gráfico** não deve ser quadrado, caso contrário, não há necessidade para este nó.
* Defina o Tamanho de Saída do **nó** de Transformação Não Quadrada como “*Relativo ao Pai*”.
* Defina o modo de divisão em blocos gráficos do **nó** como “*Sem divisão em blocos gráficos*” se desejar transformar apenas a entrada em uma única posição.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Modo Lado a Lado</b> <i>Automático, Manual</i> | Habilite compensações automáticas não quadradas ou não. |
| <b>Bloco</b> <i>1 - 16</i> | Acessível somente quando o Modo lado a lado está definido como Manual. Permite alterar a escala de maneira segura para a divisão em blocos gráficos. |
| <b>Deslocamento</b> <i>0.0 - 1.0</i> | Move ou traduz o resultado. Clique duas vezes no controle deslizante para inserir valores negativos. |
| <b>Rotação</b> <i>0.0 - 1.0</i> | Gira a imagem de entrada. |
| <b>Rotação Segura (Somente Quadrados)</b> <i>Falso/Verdadeiro</i> | Ajusta aos valores seguros para manter a nitidez dos pixels. |
| <b>Cor do plano de fundo</b> <i>(Valor da cor)</i> | Cor do plano de fundo para preencher a imagem. Visível somente quando o [Modo de Enquadramento em Parâmetros Básicos estiver definido como “*Sem Enquadramento*”](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md). |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="non-square-transform.resources/nonsquare-ex.png" />
        </td>
    </tr>
</table>
