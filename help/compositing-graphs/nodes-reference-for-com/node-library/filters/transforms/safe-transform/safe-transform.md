---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: Use o nó Transformação segura para aplicar transformações enquanto preserva os limites da textura e evita artefatos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformação segura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# Transformação segura

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## Transformação segura (tons de cinza)

**Entrada:** *Filtros/Transformações*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Versão lado a lado de [Transformar 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Permite dimensionar, girar e deslocar sem quebrar a divisão em blocos gráficos e sem perder os detalhes de pixels (perda de nitidez) devido a pequenos deslocamentos e rotações.

Útil para transformar o ruído quando o controle máximo ou a nitidez perfeita são necessários.

## Parâmetros

* **Bloco**: *1 - 16* Reduz a entrada colocando-a lado a lado.
* **Modo de Deslocamento**: *Manual, Aleatório* Alterna para um deslocamento aleatório em vez de um definido manualmente.
* **Deslocamento**: *0.0 - 1.0*\
  Move ou traduz o resultado. Verifica se os pixels são encaixados e não interpolados.
* **Rotação**: *0.0 - 1.0* Gira a entrada ao longo do ângulo.
* **Rotação segura de blocos**: *Falso/Verdadeiro* Determina o comportamento da Rotação, se ela deve se ajustar a valores seguros que não desfocam nenhum pixel.
* **Simetria**: *nenhuma, X, Y, X+Y*
* **Cor do plano de fundo**: *(Valor da cor) (Somente versão da cor)*
* **Modo de mipmap**: *Automático, Manual* Determina o modo de mipmapping. Defini-lo como Manual leva a resultados mais nítidos.
* **Nível do mipmap**: *0 - 10* Quando o modo Mipmap está definido como Manual, você pode escolher um Mipmap diferente.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
