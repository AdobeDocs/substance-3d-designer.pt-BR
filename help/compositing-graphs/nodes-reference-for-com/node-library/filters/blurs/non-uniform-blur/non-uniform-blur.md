---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/non-uniform-blur.html"
breadcrumb-title: ''
description: Use o nó Desfoque não uniforme para aplicar desfoque com intensidades diferentes nas direções X e Y para efeitos anisotrópicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Non Uniform Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desfoque não uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# Desfoque não uniforme

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-blur-grayscale.png){width="128px"}

![](../../../../../../assets/non-uniform-blur.png){width="128px"}

## Desfoque não uniforme (tons de cinza)

**Entrada:** *Filtros/Desfoques*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Executa um Desfoque de alta qualidade, onde a intensidade é orientada por uma máscara de entrada. As opções permitem adicionar Anisotropia e assimetria.

## Parâmetros

### Entradas

* **Mapa de desfoque**: *Entrada em tons de cinza* Mapa de máscaras para determinar a intensidade do efeito.

### Parâmetros

* **Intensidade**: *0.0 - 50.0* Intensidade máxima para aplicar o desfoque. Mascarada pelo Mapa de desfoque, portanto, essa configuração não terá efeito sobre as áreas pretas desse mapa.
* **Anisotropia**: *0.0 - 1.0* Opcionalmente, adiciona direcionalidade ao efeito de desfoque. Direcionado pelo parâmetro Ângulo.
* **Assimetria**: *0.0 - 1.0* Opcionalmente, adiciona um viés à amostragem. Direcionado pelo parâmetro Ângulo.
* **Ângulo**: *0.0 - 1.0*&#x200B;Ângulo para definir a direcionalidade e o viés de amostragem.
* **Amostras**: *1 - 16* Quantidade de amostras determina a qualidade. Multiplicado pela quantidade de lâminas.
* **Pás**: *1 -* 9\
  Quantidade de setores de amostragem, determina a qualidade. Multiplicado pela quantidade de amostras.

## Imagens de exemplo

*O exemplo abaixo é orientado por uma rampa de gradiente (a 90 graus) no slot do Mapa de Desfoque.*

![](../../../../../../assets/nonuniform-example.gif)

</td>
</tr>
</table>
