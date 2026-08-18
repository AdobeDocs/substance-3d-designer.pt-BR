---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear.html"
breadcrumb-title: ''
description: Use o nó Edge Wear de fibra de vidro para gerar máscaras de desgaste nas bordas de fibra de vidro com base na curvatura da malha.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Fiber Glass Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear de fibra de vidro
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---


# Edge Wear de fibra de vidro

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fiber-glass-edge-wear.png){width="128px"}

## Edge Wear de fibra de vidro

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Representa uma máscara especificamente destinada a um tipo de desgaste de fibra de vidro, que talvez pudesse ser usada para tecidos. Devido à natureza muito ladrilhada e repetitiva das fibras, a mesclagem triplanar pode ser ativada opcionalmente.

## Parâmetros

### Entradas

* **Curvatura**: *Entrada em tons de cinza*\
  Mapa baked usado para realce de aresta. Obrigatório!
* **Oclusão De Ambiente**: *Entrada Em Tons De Cinza*\
  Mapa baked usado para mascarar áreas ocultadas. Não é necessário, mas definitivamente recomendado.
* **Entrada de Desgaste**: *Entrada em Tons de Cinza*\
  Slot personalizado opcional para substituir o padrão de fibra.
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.
* **Espaço Mundial Normal**: *Entrada de Cores*\
  Usado apenas para Triplanar.
* **Posição**: *Entrada de cores*\
  Usado apenas para Triplanar.

### Parâmetros

* **Nível de desgaste**: *0.0 - 1.0* Como uma [Varredura de histograma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), revela progressivamente o desgaste.
* **Desgastar Contraste**: *0.0 - 1.0* Define o contraste total do efeito.
* **Smoothness de bordas**: *0.0 - 16.0* Define a sangria/o desfoque das bordas realçadas.
* **Quantidade de Desgaste**: *0.0 - 1.0* Define a quantidade do efeito de fibra a ser mesclada entre as bordas. Ajuste isso junto com o Nível de desgaste para obter o máximo de controle.
* **Mascaramento de Oclusão de ambiente**: *0.0 - 1.0* Define a quantidade de influência que o AO tem sobre como ocultar o efeito.
* **Espessura da curvatura**: *0.0 - 1.0* Define a quantidade de influência que as bordas convexas da curvatura têm.
* **Usar Desgaste Personalizado**: *Falso/Verdadeiro* substitui fibras incorporadas por mapa personalizado.
* **Usar Triplanar**: *Falso/Verdadeiro* Habilita o [Triplanar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) para ocultar costuras.
* **Contraste de Mesclagem Triplanar**: *0.0 - 1.0* Controla o contraste do efeito Triplanar.

## Imagens de exemplo

![](../../../../../../assets/fiber-glass-edge-wear-ex.gif)

</td>
</tr>
</table>
