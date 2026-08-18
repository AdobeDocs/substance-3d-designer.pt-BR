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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---


# Multi Color Equalizer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer-multi.png){width="128px"}

## Multi Color Equalizer

**Entrada:** *Filtros de Material/Processamento de Digitalização*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Esta é a versão de várias entradas do [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md). Ele nivela as diferenças de cor e remove matizes indesejadas em uma escala selecionável pelo usuário. Destina-se principalmente ao uso com fotos de vários ângulos, que são então combinadas com [Vários ângulos para Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) ou [Vários ângulos para Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Consulte o [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md) original para obter mais informações.

## Parâmetros

### Entradas

* **Entrada 1-8**: *Entrada de cores* Várias entradas para processar.
* **Entrada de máscara**: *entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Contagem de entradas**: *1 - 8* Define o número de entradas a serem processadas em paralelo.
* **Entrada lado a lado**: *Falso/Verdadeiro* Preserva opcionalmente a divisão em blocos gráficos nas bordas.
* **Raio**: *0.0 - 50.0* Define o raio de equalização. Um raio maior removerá apenas grandes diferenças de cores. Isso requer ajustes para cada imagem.
* **Equilíbrio claro/escuro**: *0.0 - 1.0* Configuração de polarização para deixar ou remover tons mais escuros.
* **Variação de cor personalizada**: *False/True* Permite variar o efeito em direção a uma cor especificada pelo usuário.
* **Variação de cor**\
  Ativa somente se a Variação de cor personalizada estiver ativada. As configurações permitem selecionar um deslocamento de tom no qual equalizar.
  * **Matiz**: *0.0 - 360.0*
  * **Croma**: *0.0 - 1.0*
  * **Luma**: *0.0 - 1.0*
* **Origem da Máscara**: *Nenhuma, Média de Imagens, Parâmetro de Cor, Entrada* Define se algum mascaramento deve acontecer. O parâmetro de cor ativa as configurações adicionais abaixo, a entrada alterna para uma entrada de máscara definida pelo usuário.
* **Máscara**\
  Ativo somente com o mascaramento do parâmetro de cor. Contém parâmetros de mascaramento adicionais para determinar a máscara com base na própria imagem. Os parâmetros abaixo permitem converter com precisão um matiz em uma máscara binária na qual a equalização é aplicada. Observe que os efeitos do parâmetro Raio podem se tornar muito menos pronunciados ao usar essas configurações.
  * **Cor**: *(valor da cor)*
  * **Intervalo de matiz**: *0.0 - 360.0*
  * **Intervalo Cromático**: *0.0 - 1.0*
  * **Intervalo Luma**: *0.0 - 1.0*
  * **Desfoque**: *0.0 - 2.0*
  * **Smoothness**: *0.0 - 2.0*

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
