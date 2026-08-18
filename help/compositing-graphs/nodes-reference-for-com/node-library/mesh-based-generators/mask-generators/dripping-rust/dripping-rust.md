---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: Use o nó Ferrugem de gotejamento para gerar padrões de gotejamento de ferrugem com base na geometria da malha e na direção da gravidade.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ferrugem de gotejamento
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---


# Ferrugem de gotejamento

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dripping-rust.png){width="128px"}

## Ferrugem de gotejamento

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara representa lascas e manchas de ferrugem, com vazamentos diminuindo.

## Parâmetros

### Entradas

* **Curvatura**: *Entrada em tons de cinza*\
  Mapa planejado ou gerado para ajudar com o posicionamento das ferrugens.
* **Oclusão De Ambiente**: *Entrada Em Tons De Cinza*\
  Mapa planejado ou gerado para ajudar com o posicionamento das ferrugens.
* **Posição**: *Entrada em Tons de Cinza*\
  Mapa cozido ou gerado para direções de gotejamento.
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Propagação de Ferrugem**: *0.0 - 1.0* Controle principal para a quantidade de ferrugem.
* **Contraste de Ferrugem**: *0.0 - 1.0* Define a quantidade de contraste nas manchas de ferrugem geradas (não afeta as gotas).
* **Smoothness de propagação**: *0.0 - 1.0* Quantidade de efeito de desfoque/mancha a ser aplicada às manchas de ferrugem.
* **Intensidade de gotas**: *0.0 - 1.0* Define a intensidade e o comprimento das gotas de manchas.
* **Smoothness de gotas**: *0.0 - 1.0* Quantidade de desfoque e suavização a ser aplicada a gotas.
* **Quantidade de Amostras de Gotas**: *0 - 32* Define o nível de qualidade (etapas) para o efeito de gotas. Tem um pequeno efeito na velocidade.

## Imagens de exemplo

![](../../../../../../assets/dripping-rust-ex3.gif)

</td>
</tr>
</table>
