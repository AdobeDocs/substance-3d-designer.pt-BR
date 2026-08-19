---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leather-wear.html"
breadcrumb-title: ''
description: Use o nó Desgaste de couro para gerar máscaras de desgaste em superfícies de couro com base na curvatura da malha e nos pontos de contato.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leather Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desgaste de couro
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# Desgaste de couro

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leather-wear.png){width="128px"}

## Desgaste de couro

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara representa um desgaste com um padrão de couro, com mais desgaste nas bordas com base na curvatura. É semelhante à [Edge Wear de vidro de fibra](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear/fiber-glass-edge-wear.md) em funcionalidade e tem, em sua maioria, os mesmos parâmetros.

## Parâmetros

### Entradas

* **Curvatura**: *Entrada em tons de cinza*\
  Mapa baked usado para o posicionamento de bordas. Obrigatório!
* **Oclusão De Ambiente**: *Entrada Em Tons De Cinza*\
  Mapa baked usado para ocultar determinadas áreas. Recomendado, mas não obrigatório.
* **Entrada de Desgaste**: *Entrada em Tons de Cinza*\
  Slot de entrada opcional do mapa de Desgaste que pode ser alternado pelo parâmetro “Usar Desgaste personalizado”.
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Nível de desgaste**: *0.0 - 1.0* Define o nível de desgaste global, revelando gradualmente.
* **Usar contraste**: *0.0 - 1.0* Define o contraste do efeito.
* **Quantidade de Desgaste**: *0.0 - 1.0* Define a quantidade de desgaste (padrão de couro) a ser mesclada entre as bordas.
* **Mascaramento de Oclusão de ambiente**: *0.0 - 1.0* Define a extensão em que o AO mascara os efeitos de desgaste.
* **Espessura da curvatura**: *0.0 - 1.0* Define a extensão em que as bordas da curvatura afetam o resultado final. Mesmo se definido como 0, você ainda precisa de um mapa de curvatura.
* **Usar Desgaste Personalizado**: *Falso/Verdadeiro* Habilita a substituição do padrão de couro padrão interno. Em vez disso, use um slot de entrada personalizado.

## Imagens de exemplo

![](../../../../../../assets/leather-wear-ex.gif)

</td>
</tr>
</table>
