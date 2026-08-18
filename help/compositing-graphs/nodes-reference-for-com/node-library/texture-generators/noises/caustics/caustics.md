---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
breadcrumb-title: ''
description: Use o nó Caustics para gerar padrões de luz cáustica para criar efeitos de iluminação subaquática e refrativa.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Caustics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cáustica
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# Cáustica

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-caustics-grayscale.png){width="128px"}

**Entrada:** *Geradores De Textura**/Ruídos*

**Complexo**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

Gera cáustica projetada com base em um mapa de height e uma direção de luz.Vem nas versões Tons de cinza e coloridas, as diferenças são sutis, mas a versão colorida adiciona efeitos de dispersão de cores. A luz é projetada a partir de um único ponto; nenhum mapa de ambiente é usado.

</td>
</tr>
</table>

## Parâmetros

* **Espaço de cores de saída**: *Raw, sRGB*\
  Defina o espaço da cor de saída.
* **Tamanho da Grade de Fótons**: *Automático, 512, 1024, 2048, 4096*\
  Define a qualidade ajustando o tamanho da grade, mas o padrão é a entrada correspondente. Pode ser usado para acelerar o cálculo.
* **Escala do Height da superfície**: *0.0 - 1.0*\
  Multiplicador para determinar como o height é interpretado.
* **Posição do Height da Superfície**: *0.0 - 1.0*\
  Definir distância da superfície de refração para projeção.
* **IOR De Superfície**: *1.0 - 2.0*\
  Definir o índice de refração, na versão colorida, isso adiciona mais dispersão de cores.
* **Tamanho do fóton**: *1.0 - 50.0*\
  O tamanho do fóton afeta a nitidez do efeito.
* **Dispersão**: *0.0 - 0.01 (somente versão de cores)*\
  Afeta apenas a dispersão de cores. Não visível quando a taxa de transferência interna é baixa.
* **Tremulação**: *0.0 - 1.0*\
  Adicione tremulação irregular às partículas de fóton fundidas.
* **Posição da luz**:\
  Move a posição da luz. Também feito por meio de um gizmo na exibição 2D.
* **Cor do plano de fundo**: *(Valor da cor) (somente versão da cor)*\
  Altere a cor do plano de fundo. Limitado a preto na versão em tons de cinza.
* **Expansão não quadrada**: *Falso/Verdadeiro*\
  Habilite a compensação de abóbora e estiramento com proporções não quadradas.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-caustics-grayscale-1.png" width="300px"/></div> |
| --- |
|  |
