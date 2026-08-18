---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter.html"
breadcrumb-title: ''
description: Use o nó respingos para dispersão formas entre texturas para criar padrões aleatórios e detalhes de textura orgânica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Respingo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# Respingo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/splatter.png)

![](../../../../../../assets/splatter-color.png)

## Respingo (cor)

**Entrada:** *Geradores De Textura**/Padrões*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Splatter é um gerador de padrões destinado ao posicionamento aleatório de uma entrada de mapa. Ele tem muitos controles para posicionamento geometricamente padronizado e é mais simples em uso do que o [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Este último pode alcançar resultados semelhantes, mas é muito mais complexo.

O Splatter funciona bem para rapidamente carimbar algumas formas, sem precisar de muitos ajustes.

Lembre-se de que os parâmetros padrão de Splatter não parecem aleatórios: você precisa ajustar alguns deles para obter aleatoriedade (principalmente parâmetros de desordem). Lembre-se também de que o Splatter requer uma entrada de mapa para funcionar.

## Parâmetros

* **Largura do Tamanho do Padrão**: *0.0 - 1000.0* Número de padrões a serem usados no eixo X.
* **Height de Tamanho de Padrão**: *0.0 - 1000.0* Número de padrões a serem usados no eixo Y.
* **Rotação**: *-360.0 - 360.0* Gira cada padrão em um valor definido.
* **Variação de Rotação**: *0.0 - 360.0* Introduz a rotação aleatória para cada forma separada.
* **Zoom**: *100.0 - 10000.0* Aumenta o resultado final. Lembre-se de que isso quebra a divisão em blocos gráficos!
* **Ganho**: *0.0 - 10.0* Ajusta o ganho de mesclagem de cada padrão. Faz com que se destaquem mais.
* **Panorâmica X**: *-100.0 - 100.0* Panorâmica do resultado inteiro no eixo X.
* **Panorâmica Y**: *-100.0 - 100.0* Panorâmica do resultado inteiro no eixo Y.
* **Desordem**: *0.0 - 100.0*\
  Desloca as formas aleatoriamente.
* **Número da Grade**: *0 - 8* Salta por diferentes tamanhos de grade para ajustar a escala do resultado. Mantém a divisão em blocos gráficos.
* **Ângulo do Distúrbio**: *0.0 - 360.0* Controla o ângulo de deslocamento do distúrbio.
* **Distúrbio Aleatório**: *Falso/Verdadeiro* Aleatório o ângulo do distúrbio, adicionando muito mais caos.
* **Tamanho do Padrão**: *5 - 12*
* **Variação de Tamanho**: *0.0 - 100.0* Introduz escala aleatória para cada forma.
* **Filtragem de Entrada de Imagem (Mecanismo > somente v4)**: *Bilinear + Mipmaps, Bilinear, Mais Próximo* Qual filtragem aplicar à imagem de entrada.
* **Nível de Saída Mínimo**: *0.0 - 1.0* Ajuste de nível mínimo de saída.
* **Nível Máximo de Saída**: *0.0 - 1.0* Ajuste de nível máximo de saída.
* **Cor do plano de fundo**: *(valor de tons de cinza)*Define a cor do plano de fundo sólida.
* **Variação de luminância**: *0.0 - 1.0 (somente versão em tons de cinza)*Introduz a variação de luminância.
* **Variação de cor**: *0.0 - 1.0 (Somente versão de cor)*Introduz a variação de cor.

## Imagens de exemplo

![](../../../../../../assets/splatter-ex.gif)

</td>
</tr>
</table>
