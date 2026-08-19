---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/surface-brush.html"
breadcrumb-title: ''
description: Use o nó Pincel de superfície para gerar máscaras com base na orientação da superfície para criar efeitos de intemperismo e desgaste direcionais.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Surface Brush
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pincel de superfície
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---


# Pincel de superfície

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/surface-brush.png){width="128px"}

## Pincel de superfície

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara representa um efeito interessante do pincel de metal em uma superfície de objeto, ocultado pela geometria de objetos e pelo AO.

## Parâmetros

### Entradas

* **Espaço Mundial Normal**: *Entrada de Cores*
* **Curvatura**: *Entrada em tons de cinza*\
  Mapa baked usado para efeitos internos e mascaramento.
* **Oclusão De Ambiente**: *Entrada Em Tons De Cinza*\
  Mapa baked usado para efeitos internos e mascaramento.
* **Posição**: *Entrada em Tons de Cinza*
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Nível**: *0.0 - 1.0*\
  Define o nível de efeito global, revelando gradualmente.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste do resultado.
* **Scratches Comprimento**: *0.0 - 8.0* Define o comprimento dos arranhões. Valores menores são mais como pontos, valores maiores são listras longas.
* **Ocultar eixo**: *X, Y, Z, nenhum* Eixo do objeto que deve receber riscos. Não altera a direção dos arranhões.
* **Intensidade do Eixo de Oclusão**: *0.0 - 1.0* Intensidade do efeito de oclusão do eixo.
* **Oclusão**: *0.0 - 1.0* Força do AO ao ocluir riscos.
* **Intensidade de nitidez**: *0.0 - 1.0* Defina a quantidade de pós-nitidez a ser aplicada aos arranhões.

## Imagens de exemplo

![](../../../../../../assets/surface-brush-ex.gif)

</td>
</tr>
</table>
