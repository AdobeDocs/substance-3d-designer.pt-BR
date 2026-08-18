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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 1%

---


# Color Equalizer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer.png){width="128px"}

## Color Equalizer

**Entrada:** *Filtros de Material/Processamento de Digitalização*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este nó funciona como um [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) de alta qualidade para diferenças de cores. Quando um Highpass normal remove a saturação e pode gerar nitidez indesejada, o Color Equalizer funciona para compensar as diferenças de cor e remover tons indesejados em uma escala selecionável pelo usuário.

Isso é muito útil se uma foto ou uma digitalização tiver diferenças de cor indesejadas ou uma tonalidade que você deseja remover. Se você usou o [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md), este nó deve parecer familiar.

As opções de mascaramento destinam-se a remover tons muito específicos ou a operar apenas em faixas de valores específicas. Use-os se achar que o efeito é muito amplo.

## Parâmetros

### Entradas

* **Entrada**: *Entrada de Cores*
* **Entrada de máscara**: *entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó. Ativo somente quando a Máscara está definida como “Entrada”.

### Parâmetros

* **Entrada lado a lado**: *Falso/Verdadeiro* Preserva opcionalmente a divisão em blocos gráficos nas bordas.
* **Raio**: *0.0 - 50.0* Define o raio de equalização. Um raio maior removerá apenas grandes diferenças de cores. Isso requer ajustes para cada imagem.
* **Equilíbrio claro/escuro**: *0.0 - 1.0* Configuração de polarização para deixar ou remover tons mais escuros.
* **Variação de Cor Personalizada**: *Falso/Verdadeiro* Permite variar o efeito em direção a uma cor especificada pelo usuário.
* **Variação de cor**\
  Ativa somente se a Variação de cor personalizada estiver ativada. As configurações permitem selecionar um deslocamento de tom no qual equalizar.
  * **Matiz**: *0.0 - 360.0*
  * **Croma**: *0.0 - 1.0*
  * **Luma**: *0.0 - 1.0*
* **Origem da Máscara**: *Nenhuma, Média de Imagens, Parâmetro de Cor, Entrada* Defina se algum tipo de mascaramento deve acontecer. O Parâmetro de cor ativa as configurações adicionais abaixo e a Entrada alterna para uma entrada de máscara definida pelo usuário.
* **Máscara**\
  Isso só está ativo com o mascaramento do parâmetro de cor. Parâmetros de mascaramento adicionais para determinar a máscara com base na própria imagem. Os parâmetros abaixo permitem converter com precisão um matiz em uma máscara binária na qual a Equalização é aplicada. Observe que os efeitos do parâmetro Raio podem se tornar muito menos pronunciados ao usar essas configurações.
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
