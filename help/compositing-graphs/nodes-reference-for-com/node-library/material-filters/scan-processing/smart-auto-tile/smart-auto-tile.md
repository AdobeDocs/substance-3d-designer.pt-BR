---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/smart-auto-tile.html"
breadcrumb-title: ''
description: Use o nó Bloco Automático Inteligente para criar blocos gráficos perfeitos automaticamente a partir de materiais digitalizados usando a detecção inteligente de padrões.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Smart Auto Tile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bloco Automático Inteligente
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---


# Bloco Automático Inteligente

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/smart-auto-tile.png){width="128px"}

## Bloco Automático Inteligente

**Entrada:** *Filtros de Material/Processamento de Digitalização*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Esse nó transforma um conjunto não ladrilhado de mapas Basecolor, Normal e Heightmaps em uma versão ladrilhada de acordo com a análise inteligente das entradas. É semelhante a [Criar foto lado a lado](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md), mas muito mais avançado, pois usa informações de todos os canais para misturar as coisas da maneira mais inteligente (semelhante ao que o [Clonar correção](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md) faz). Ele também tem uma função interna [Cortar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) para determinar qual área usar ao colocar lado a lado. Certifique-se de [ler mais sobre o nó Cortar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) para entender essa função corretamente.

Para usar este nó, comece definindo a área Cortada e use as configurações de Borda para determinar como as bordas lado a lado são mescladas no centro. Os parâmetros de limiar são de importância fundamental para isso! Lembre-se de que áreas grandes e uniformes não funcionam muito bem com esse efeito. Quanto mais detalhes e formas existirem, mais será necessário trabalhar com elas.

## Parâmetros

### Entradas

* **Máscara**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó. Pode ser alternado com o parâmetro “Usar máscara”.

### Parâmetros

* **Cortar**
  * **Tamanho de entrada**: *0 - 8192* Resolução e proporções das imagens de entrada. Muito importante para imagens não quadradas.
  * **Transformar**: *(Matriz de Transformação)*\
    Gira e dimensiona o resultado. O resultado pode ser modificado ao interagir diretamente com a tela.
  * **Deslocamento**: *0.0 - 1.0*\
    Move ou traduz o resultado. O resultado pode ser modificado ao interagir diretamente com a tela.
* **Borda**
  * **Detectar bordas**: *Falso/Verdadeiro* Ativa ou desativa a mesclagem de bordas especiais detectadas.
  * **Usar Limite por Canal**: *Falso/Verdadeiro* Alterna entre um valor de limite global ou um para cada canal.
  * **Limite**: *0.0 - 1.0*
  * **Cor Base do Limite**: *0.0 - 1.0*
  * **Limite Normal**: *0.0 - 1.0*
  * **Height de Limite**: *0.0 - 1.0*
  * **Deslocamento do corte**: *0.0 - 0.5* O controle principal para mover o corte, os eixos X e Y, são separados.
  * **Desfoque**: *0.0 - 2.0* Desfoca a transição de mesclagem.
  * **Smoothness**: *0.0 - 2.0* Controla a irregularidade dos resultados da análise de borda.
  * **Resolução da grade**: *1 - 11* Resolução de qualidade da análise de borda.
  * **Usar cor base**: *Falso/Verdadeiro* Alterna o processamento de cor base (entrada e saída).
  * **Usar Normal**: *Falso/Verdadeiro* Alterna o processamento Normal (entrada e saída).
  * **Usar Height**: *Falso/Verdadeiro* Alterna o processamento Normal (entrada e saída).
  * **Usar máscara**: *Falso/Verdadeiro*\
    Ativa ou desativa o uso do Mapa de máscaras para formas de máscara de carimbo personalizadas.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
