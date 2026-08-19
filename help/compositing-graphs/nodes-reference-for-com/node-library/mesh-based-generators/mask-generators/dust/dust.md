---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dust.html"
breadcrumb-title: ''
description: Use o nó Dust para gerar máscaras de acumulação de dust com base na geometria da malha para criar efeitos realistas de dust e sujeira.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dust
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---


# Dust

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dust.png){width="128px"}

## Dust

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara representa o dust acumulado em áreas ocultas, rebaixadas, bem como apenas em áreas voltadas para cima. Requer AO cozido e World Space Normals adequados para funcionar.

## Parâmetros

### Entradas

* **Oclusão De Ambiente**: *Entrada Em Tons De Cinza*\
  Mapa baked usado para o posicionamento do dust. Obrigatório!
* **Espaço Mundial Normal**: *Entrada de Cores*\
  Mapa baked usado para o posicionamento do dust. Obrigatório!
* **Ruído**: *Entrada em Tons de Cinza*\
  O mapa de dusts personalizado (opcional) só aparece quando Substituir ruído está definido como Verdadeiro.
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Nível**: *0.0 - 1.0*\
  Define a quantidade total de dust.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste da dust.
* **Quantidade de Oclusão**: *0.0 - 1.0* Define a influência de AO; mais dust aparecerá em áreas ocultadas.
* **Opacidade do ruído**: *0.0 - 1.0* Define a quantidade de ruído visível nas áreas empoeiradas.
* **Substituir Ruído**: *Falso/Verdadeiro* Defina para usar a entrada do mapa de dusts personalizado.

## Imagens de exemplo

![](../../../../../../assets/dust-ex.gif)

</td>
</tr>
</table>
