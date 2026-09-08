---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/base-material.html"
breadcrumb-title: ''
description: Use o nó Material de base para criar propriedades de material de base para criar materiais baseados fisicamente do zero.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > Base Material
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Material de base
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 6%

---


# Material de base

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/pbr-base-material.png){width="128px"}

<b>Entrada:</b> Filtros Materiais > Utilitários PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

A maneira mais rápida e fácil de criar um material Multicanal no [Adobe Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html). Este nó retorna um material completo incorporado com base em configurações e valores de cor simples e sólidos. Isso pode ser usado como um espaço reservado ou para refinar em um material complexo.

O nó é muito útil ao texturizar adereços completos e mesclar vários materiais. Na verdade, você poderia começar cada material deste nó, sem precisar de uma base material complexa.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
|  | Entradas opcionais para cada canal que pode ser alternado com as opções em “Entradas definidas pelo usuário”. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Fluxo de trabalho de PBR</b> <i>Metal - Aspereza, Specular - Textura reluzente</i> | Define o modelo PBR usado. |
| <b>Predefinição de material</b> <i>Personalizado, Dielétrico, Ouro, Prata, Alumínio, Ferro, Cobre, Titânio, Níquel, Cobalto, Platina</i> | Atalho rápido para criar certos metais. Desativa opções irrelevantes. |
| <b>Cor base</b> <i>(Valor da cor)</i> | Cor sólida usada para Cor de base. |
| <b>Metálico</b> <i>(Valor em tons de cinza)</i> | Valor sólido usado para Metálico. |
| <b>Cor da Difusão</b> <i>(Valor da cor)</i> | Cor sólida usada para Difusões. |
| <b>Specular</b> <i>(Valor da cor)</i> | Cor sólida usada para Specular. |
| <b>Predefinições de Specular</b> <i>Plástico, Madeira, Pedra, Tijolo, Areia, Concreto, Tecido, Metal Enrugado, Água, Gelo, Vidro</i> | Predefinições rápidas opcionais para definir valores de Specular corretos para PBR. |
| <b>Intervalo de Speculares</b> <i>0.0 - 1.0</i> | Ajusta a faixa de Specular. |
| <b>Aspereza - Textura reluzente</b> |  |
| <b>Valor de aspereza</b> <i>(Valor em tons de cinza)</i> | Defina o valor global de aspereza base, se o canal estiver ativo. |
| <b>Valor da Textura Reluzente</b> <i>(Valor em tons de cinza)</i> | Cor sólida usada para Textura reluzente, se o canal estiver ativo. |
| <b>Valor do Desgaste</b> <i>0.0 - 1.0</i> | A extensão na qual a entrada opcional do mapa de Desgaste é mesclada para Brilho ou Aspereza. |
| <b>Divisão em blocos gráficos</b> <i>1 - 16</i> | Extensão para colocar o mapa de Desgaste em bloco por. |
| <b>Entrada de Desgaste personalizada</b> <i>Falso/Verdadeiro</i> | Habilita ou desabilita o mapa de Desgaste personalizado opcional . |
| <b>Normal</b> |  |
| <b>Normal a partir da Intensidade de Height</b> <i>0.0 - 16.0</i> | Opcionalmente, converte o Heightmap personalizado em normal e o retorna como o Normalmap do material. |
| <b>Height</b> |  |
| <b>Posição do Height</b> <i>0.0 - 1.0</i> | Valor sólido usado para saída de Height. |
| <b>Intervalo de Heights</b> <i>0.0 - 1.0</i> | Define a influência do mapa de altura definido pelo usuário, se ativado. |
| <b>Mapas Definidos pelo Usuário</b> | Ativa ou desativa todos os mapas definidos pelo usuário, retornando-os ao invés de quaisquer valores sólidos. |
