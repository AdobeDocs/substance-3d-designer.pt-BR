---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/color-equalizer.html"
breadcrumb-title: ''
description: Use o nó Color Equalizer para equilibrar variações de cores em materiais digitalizados para uniformizar a aparência da textura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 6%

---


# Color Equalizer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-equalizer.resources/color-equalizer.png){width="128px"}

<b>Entrada:</b> Filtros Materiais > Processamento de materiais escaneados

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este nó funciona como um [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) de alta qualidade para diferenças de cores. Quando um Highpass normal remove a saturação e pode gerar nitidez indesejada, o Color Equalizer funciona para compensar as diferenças de cor e remover tons indesejados em uma escala selecionável pelo usuário.

Isso é muito útil se uma foto ou uma digitalização tiver diferenças de cor indesejadas ou uma tonalidade que você deseja remover. Se você usou o [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md), este nó deve parecer familiar.

As opções de mascaramento destinam-se a remover tons muito específicos ou a operar apenas em faixas de valores específicas. Use-os se achar que o efeito é muito amplo.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Entrada de cores</i> |  |
| <b>Entrada de máscara</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. Ativo somente quando a Máscara está definida como “Entrada”. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Entrada lado a lado</b> <i>Falso/Verdadeiro</i> | Opcionalmente, preserva a divisão em blocos gráficos nas bordas. |
| <b>Raio</b> <i>0.0 - 50.0</i> | Define o raio de equalização. Um raio maior removerá apenas grandes diferenças de cores. Isso requer ajustes para cada imagem. |
| <b>Equilíbrio de brilho/escuro</b> <i>0.0 - 1.0</i> | Configuração de polarização para deixar ou remover tons mais escuros. |
| <b>Variação de cor personalizada</b> <i>Falso/Verdadeiro</i> | Permite variar o efeito em direção a uma cor especificada pelo usuário. |
| <b>Variação de cor</b> | Ativa somente se a Variação de cor personalizada estiver ativada. As configurações permitem selecionar um deslocamento de tom no qual equalizar. |
| <b>Matiz</b> <i>0.0 - 360.0</i> |  |
| <b>Croma</b> <i>0.0 - 1.0</i> |  |
| <b>Luma</b> <i>0.0 - 1.0</i> |  |
| <b>Origem da máscara</b> <i>Nenhum, Média De Imagens, Parâmetro De Cor, Entrada</i> | Defina se algum tipo de mascaramento deve acontecer. O Parâmetro de cor ativa as configurações adicionais abaixo e a Entrada alterna para uma entrada de máscara definida pelo usuário. |
| <b>Máscara</b> | Isso só está ativo com o mascaramento do parâmetro de cor. Parâmetros de mascaramento adicionais para determinar a máscara com base na própria imagem. Os parâmetros abaixo permitem converter com precisão um matiz em uma máscara binária na qual a Equalização é aplicada. Observe que os efeitos do parâmetro Raio podem se tornar muito menos pronunciados ao usar essas configurações. |
| <b>Cor</b> <i>(Valor da cor)</i> |  |
| <b>Intervalo de matiz</b> <i>0.0 - 360.0</i> |  |
| <b>Intervalo cromático</b> <i>0.0 - 1.0</i> |  |
| <b>Intervalo Luma</b> <i>0.0 - 1.0</i> |  |
| <b>Desfoque</b> <i>0.0 - 2.0</i> |  |
| <b>Smoothness</b> <i>0.0 - 2.0</i> |  |
