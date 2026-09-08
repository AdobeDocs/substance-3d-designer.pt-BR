---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-color-equalizer.html"
breadcrumb-title: ''
description: Use o nó MultiColor Equalizer para equalizar cores em vários canais de textura para um processamento de material digitalizado consistente.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Multi Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 7%

---


# Multi Color Equalizer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer-multi.png){width="128px"}

<b>Entrada:</b> Filtros Materiais > Processamento de materiais escaneados

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Esta é a versão de várias entradas do [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md). Ele nivela as diferenças de cor e remove matizes indesejadas em uma escala selecionável pelo usuário. Destina-se principalmente ao uso com fotos de vários ângulos, que são então combinadas com [Vários ângulos para Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) ou [Vários ângulos para Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Consulte o [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md) original para obter mais informações.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada 1-8</b> <i>Entrada de cores</i> | Várias entradas para processar. |
| <b>Entrada de máscara</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Contagem de entradas</b> <i>1 - 8</i> | Define o número de entradas a serem processadas em paralelo. |
| <b>Entrada lado a lado</b> <i>Falso/Verdadeiro</i> | Opcionalmente, preserva a divisão em blocos gráficos nas bordas. |
| <b>Raio</b> <i>0.0 - 50.0</i> | Define o raio de equalização. Um raio maior removerá apenas grandes diferenças de cores. Isso requer ajustes para cada imagem. |
| <b>Equilíbrio de brilho/escuro</b> <i>0.0 - 1.0</i> | Configuração de polarização para deixar ou remover tons mais escuros. |
| <b>Variação de cor personalizada</b> <i>Falso/Verdadeiro</i> | Permite variar o efeito em direção a uma cor especificada pelo usuário. |
| <b>Variação de cor</b> | Ativa somente se a Variação de cor personalizada estiver ativada. As configurações permitem selecionar um deslocamento de tom no qual equalizar. |
| <b>Matiz</b> <i>0.0 - 360.0</i> |  |
| <b>Croma</b> <i>0.0 - 1.0</i> |  |
| <b>Luma</b> <i>0.0 - 1.0</i> |  |
| <b>Origem da máscara</b> <i>Nenhum, Média De Imagens, Parâmetro De Cor, Entrada</i> | Define se algum mascaramento deve acontecer. O parâmetro de cor ativa as configurações adicionais abaixo, a entrada alterna para uma entrada de máscara definida pelo usuário. |
| <b>Máscara</b> | Ativo somente com o mascaramento do parâmetro de cor. Contém parâmetros de mascaramento adicionais para determinar a máscara com base na própria imagem. Os parâmetros abaixo permitem converter com precisão um matiz em uma máscara binária na qual a equalização é aplicada. Observe que os efeitos do parâmetro Raio podem se tornar muito menos pronunciados ao usar essas configurações. |
| <b>Cor</b> <i>(Valor da cor)</i> |  |
| <b>Intervalo de matiz</b> <i>0.0 - 360.0</i> |  |
| <b>Intervalo cromático</b> <i>0.0 - 1.0</i> |  |
| <b>Intervalo Luma</b> <i>0.0 - 1.0</i> |  |
| <b>Desfoque</b> <i>0.0 - 2.0</i> |  |
| <b>Smoothness</b> <i>0.0 - 2.0</i> |  |
