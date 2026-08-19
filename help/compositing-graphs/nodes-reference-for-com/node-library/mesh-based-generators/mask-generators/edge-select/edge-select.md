---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: Use o nó Seleção de borda para gerar máscaras selecionando bordas de malha para criar efeitos de intemperismo e desgaste baseados em bordas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Seleção de borda
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# Seleção de borda

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-select.png){width="128px"}

## Seleção de borda

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara é a melhor maneira de selecionar qualquer tipo de borda com base na curvatura. Convexo, Côncavo em qualquer nível ou contraste pode ser isolado, fornecendo um atalho excelente para evitar fazer isso manualmente por meio de um [nó Níveis](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md).

## Parâmetros

### Entradas

* **Curvatura**: *Entrada em tons de cinza*\
  Mapa baked usado para realçar bordas. Obrigatório!
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Nível**: *0.0 - 1.0*\
  Define a quantidade total de realce de borda para Convexo e Côncavo.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste do realce para Convexo e Côncavo.
* **Convexo**
  * **Largura das Bordas Convexas**: *0.0 - 1.0* Define a largura do realce para bordas Convexas. Lembre-se de que aumentar ligeiramente a Suavidade pode levar a bordas mais finas.
  * **Suavidade convexa**: *0.0 - 1.0* Defina a suavidade da transição para bordas convexas.
  * **Intensidade convexa**: *0.0 - 1.0* Define a intensidade máxima do realce de borda para bordas convexas. Defina como 0 para nenhum realce.
* **Côncavo**
  * **Largura das Bordas Côncavas**: *0.0 - 1.0* Defina a largura do realce para bordas Côncavas. Lembre-se de que aumentar ligeiramente a Suavidade pode levar a bordas mais finas.
  * **Suavidade côncava**: *0.0 - 1.0* Defina a suavidade da transição para bordas côncavas.
  * **Intensidade côncava**: *0.0 - 1.0* Defina a intensidade máxima do realce de borda para bordas côncavas. Defina como 0 para nenhum realce.

## Imagens de exemplo

![](../../../../../../assets/edge-select-ex.gif)

</td>
</tr>
</table>
