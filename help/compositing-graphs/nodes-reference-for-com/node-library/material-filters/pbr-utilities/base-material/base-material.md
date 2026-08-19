---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/base-material.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 4%

---


# Material de base

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-base-material.png){width="128px"}

## Material de base

**Entrada:** *Filtros de Material/Utilitários PBR*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

A maneira mais rápida e fácil de criar um material Multicanal no [Adobe Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html). Este nó retorna um material completo incorporado com base em configurações e valores de cor simples e sólidos. Isso pode ser usado como um espaço reservado ou para refinar em um material complexo.

O nó é muito útil ao texturizar adereços completos e mesclar vários materiais. Na verdade, você poderia começar cada material deste nó, sem precisar de uma base material complexa.

## Parâmetros

### Entradas

* Entradas opcionais para cada canal que pode ser alternado com as opções em “Entradas definidas pelo usuário”.

### Parâmetros

* **Fluxo de Trabalho de PBR**: *Metal - Aspereza, Specular - Textura reluzente* Define o modelo de PBR usado.
* **Predefinição de material**: *Personalizado, Dielétrico, Ouro, Prata, Alumínio, Ferro, Cobre, Titânio, Níquel, Cobalto, Platina* Atalho rápido para criar determinados metais. Desativa opções irrelevantes.
* **Cor base**: *(valor da cor)*Cor sólida usada para a Cor base.
* **Metálico**: *(valor em tons de cinza)*Valor sólido usado para Metálico.
* **Cor Difusa**: *(valor da cor)*Cor sólida usada para Difusa.
* **Specular**: *(valor da cor)*Cor sólida usada para Specular.
* **Predefinições de Specular**: *Plástico, Madeira, Pedra, Tijolo, Areia, Concreto, Tecido, Metal enferrujado, Água, Gelo, Vidro* Predefinições rápidas opcionais para definir valores de Specular corretos para PBR.
* **Intervalo de Speculares**: *0.0 - 1.0* Ajusta o intervalo de Speculares.
* **Aspereza - Textura reluzente**
  * **Valor de aspereza**: *(valor de tons de cinza)*Defina o valor global de aspereza base, se o canal estiver ativo.
  * **Valor da Textura Reluzente**: *(valor em Tons de Cinza)*Cor sólida usada para Textura Reluzente, se o canal estiver ativo.
  * **Quantidade de Desgaste**: *0.0 - 1.0* A extensão na qual a entrada opcional do mapa de Desgaste é mesclada para Brilho ou Aspereza.
  * **Divisão em blocos gráficos**: *1 - 16* Extensão para colocar em blocos o mapa de Desgaste opcional por.
  * **Entrada de Desgaste personalizado**: *Falso/Verdadeiro* Habilita ou desabilita o mapa de Desgaste personalizado opcional.
* **Normal**
  * **Normal a partir da Intensidade de Height**: *0.0 - 16.0* Opcionalmente, converte o Heightmap personalizado em normal e retorna isso como o Normalmap do material.
* **Height**
  * **Posição do Height**: *0.0 - 1.0* Valor sólido usado para saída de Height.
  * **Intervalo de Heights**: *0.0 - 1.0* Define a influência do Heightmap Definido pelo Usuário, se habilitado.
* **Mapas Definidos pelo Usuário**
  * Ativa ou desativa todos os mapas definidos pelo usuário, retornando-os ao invés de quaisquer valores sólidos.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
