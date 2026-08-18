---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-sampler.html"
breadcrumb-title: ''
description: Use o nó Sampler lado a lado para obter amostras e organizar blocos de texturas de entrada para criar padrões lado a lado no Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Sampler
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bloco Sampler
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---


# Bloco Sampler

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-sampler.png){width="128px"}

## Bloco Sampler (Cor)

**Entrada:** *Geradores De Textura**/Padrões*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Tile Sampler é o último nó de geração de padrão de ladrilho. É uma versão evoluída e mais complexa do [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). A partir do 2017 2.1, as diferenças são muito menores entre o Tile Sampler e o [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). As principais diferenças estão agora apenas nos sete diferentes slots de mapa que estão disponíveis para dirigir a Escala, Posição, Rotação, Tamanho, Cor e Mascaramento. Seu efeito pode ser mesclado separadamente.

O Tile Sampler é útil para criar padrões de procedimentos feitos pelo homem, com controle adicional sobre determinados parâmetros orientados por mapas de entrada externos.

Certifique-se de estar familiarizado com o [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) antes de passar para o Tile Sampler. Na maioria dos casos, você encontrará [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) o suficiente e não precisará da complexidade adicional de Tile Sampler.

## Parâmetros

### Entradas

* **Entrada de padrão 1-6**: *Entrada em tons de cinza/Entrada de cores*\
  Imagem de padrão personalizado, usada quando o parâmetro “Pattern” está definido como “Image Input”.\
  A quantidade de entradas disponíveis é determinada pelo parâmetro **Número de Entrada de Padrão**.
* **Entrada do Mapa de Escala**: *Entrada em Escala de Cinza* Mapa de escala de cinza para o dimensionamento de bloco de unidade.
* **Entrada do Mapa de Deslocamentos**: *Entrada em Tons de Cinza* Mapa em tons de cinza para o deslocamento de blocos de unidade.
* **Entrada de Mapa de rotação**: *Entrada em Tons de Cinza*\
  Mapa em tons de cinza para girar o ladrilho.
* **Entrada do Mapa Vetorial**: *Entrada de Cores*\
  Mapa de vetor de cores para direcionar um dimensionamento não uniforme.
* **Entrada do Mapa de Cores**: *Entrada em Tons de Cinza/Entrada de Cores* Mapeie para definir a tonalidade por ladrilho.
* **Entrada do mapa de máscaras**: *entrada em tons de cinza*\
  Slot de máscara usado para ocultar certos blocos.
* **Entrada do Mapa de Distribuição de Padrões**: *Entrada em Tons de Cinza*\
  Slot de máscara usado para direcionar várias entradas de padrão personalizadas.
* **Entrada de plano de fundo**: *Entrada em tons de cinza/Entrada em cores* Imagem de plano de fundo opcional.

### Parâmetros

* Valor **X**: *0 - 64*\
  Quantidade de repetições X do padrão.
* **Valor de Y**: *0 - 64*\
  Quantidade de repetições Y do padrão.
* **Expansão não quadrada**: *Falso/Verdadeiro*\
  Permite a compensação de esmagamento e alongamento com proporções não quadradas.
* **Padrão**
  * **Padrão**: *Entrada Padrão, Quadrado, Disco, Paraboloide, Sino, Gaussiano, Espinho, Pirâmide, Tijolo, Gradação, Ondas, Meio Sino, Sino Ondulado, Crescente, Cápsula, Cone*\
    Seleciona a forma de padrão a ser usada.
  * **Número de Entrada de Padrão**: *1 - 6* Quantidade de padrões personalizados para escolher aleatoriamente.
  * **Distribuição de Entrada de Padrão**: *Aleatória, Número de Padrão, Mapa de Distribuição* Define como várias Entradas de Padrão são escolhidas. Aleatório significa que um aleatório foi escolhido, Número de padrão significa que eles foram colocados em uma sequência em loop. O mapa de distribuição usa uma entrada de mapa em tons de cinza para o posicionamento da unidade.
  * **Filtragem de Entrada de Padrão (Mecanismo > v4)**: *Bilinear + Mipmaps, Bilinear, Mais Próximo*
  * **Específico de Padrão**: *0.0 - 1.0*\
    Permite que você altere a forma do padrão selecionado. O efeito depende do padrão selecionado.
  * **Aleatório Específico de Padrão**: *0.0 - 1.0* O efeito de aleatoriedade depende do padrão selecionado.
  * **Rotação**: *0, 90, 180, 270* Rotação em etapas (90 graus).
  * **Rotação Aleatória**: *0.0 - 1.0* Rotação aleatória livre por bloco.
  * **Simetria aleatória**: *0.0 - 1.0* Define o número de blocos que devem ser invertidos/espelhados aleatoriamente de acordo com o comportamento abaixo.
  * **Modo de simetria aleatória**: *Horizontal + Vertical, Horizontal, Vertical* Determina o comportamento de espelhamento de simetria.
* **Tamanho**
  * **Modo de Tamanho**: *Normal, Manter Proporção, Absoluto, Pixel* Define o comportamento geral do tamanho do padrão.\
    Normal permite definir o tamanho dos elementos do padrão. É afetada pelo valor X e Y.\
    Manter proporção permite definir um tamanho afetado pela quantidade X e Y, mas a proporção X e Y entre os dois permanece intacta.\
    Absoluto permite definir um tamanho absoluto que não é afetado pela quantidade X e Y.\
    Pixel permite definir um tamanho absoluto em pixels, não afetado pela quantidade X e Y. Alterar a resolução afetará o tamanho dos elementos.
  * **Tamanho (Absoluto/Pixel)**: *0.0 - 1.0* Altera proporções não uniformes para blocos. O comportamento exato depende do Modo de Tamanho.
  * **Tamanho Aleatório**: *0.0 - 1.0* Aleatório proporções por bloco.
  * **Escala**: *0.0 - 10.0* Define a escala global do ladrilho.
  * **Escala aleatória**: *0.0 - 1.0* Escala aleatória por bloco
  * **Multiplicador de Mapa de Escala**: *0.0 - 1.0* Mescla o efeito do Mapa de Escala.
  * **Multiplicador de Mapa de Vetor de Escala**: *0.0 - 1.0* Combina o efeito do mapa de vetor de escala para orientar um dimensionamento não uniforme.
  * **Afetar parametrização da escala**: *X e Y, X, Y* Define quais eixos a parametrização da escala afeta. Pode ser usado para fazer com que o Mapa de escala afete apenas os elementos X ou Y.
* **Posição**
  * **Posição Aleatória**: *0.0 - 10.0* Dispõe aleatoriamente a posição do bloco sobre os dois eixos.
  * **Deslocamento**: *0.0 - 1.0*\
    Desloca os blocos de acordo com o Tipo de deslocamento.
  * **Tipo de Deslocamento**: *quincux horizontal, quincux vertical, global horizontal, global vertical* Altera a direção em que o Deslocamento opera.
  * **Deslocamento global**: *0.0 - 1.0* Desloca globalmente todos os blocos no eixo X ou Y.
  * **Intensidade do Mapa de Deslocamento**: *0.0 - 1.0* Mescla a intensidade do mapa de Deslocamento no Deslocamento.
  * **Ângulo do Deslocamento**: *0.0 - 1.0* Define o ângulo no qual deslocar.
  * **Deslocamento de Mapas Vetoriais**: *0.0 - 1.0* Usa o mapa Vetorial para orientar o deslocamento e o Ângulo.
* **Rotação**
  * **Rotação**: *0.0 - 1.0* Gira globalmente todos os blocos.
  * **Rotação Aleatória**: *0.0 - 1.0* Gira aleatoriamente por bloco.
  * **Multiplicador de Mapa de rotação**: *0.0 - 1.0* Combina o efeito de Mapa de rotação na rotação por Bloco.
  * **Multiplicador de Mapa Vetorial**: *0.0 - 1.0* Usa o Mapa Vetorial para direcionar a rotação por bloco.
* **Cor**
  * **Limite de Mapa de Máscaras**: *0.0 - 1.0* Limite para mapa de máscara quando iniciar a ocultação de blocos.
  * **Inversão de mapa de máscara**: *Falso/Verdadeiro* Inverte o efeito de mapa de máscara.
  * **Técnica de amostragem de mapa de máscaras**: *Centro de padrão, Caixa delimitadora de padrão (mais lenta)*Se a ocultação deve ser determinada por um único ponto ou por uma caixa delimitadora. Evita pixels isolados, causando efeitos estranhos.
  * **Máscara aleatória**: *0.0 - 1.0* Máscara aleatória, funciona em paralelo com o mapa de máscara.
  * **Inverter Máscara**: *Falso/Verdadeiro* Inverte o mascaramento aleatório.
  * **Modo de Mesclagem**: *Adicionar/Sub, Máx. (Bloco Sampler) /* Adicionar/Sub, Alpha Blend* (Bloco Sampler Color)*Modo de mesclagem para blocos no plano de fundo e entre si.
  * **Cor**: *(valor em tons de cinza) / (valor da cor)*Cor sólida e global do ladrilho.
  * **Cor/Luminância Aleatória**: *0.0 - 1.0* Aleatória de cor por bloco.
  * **Modo De Parametrização De Cores**: *Entrada De Cores, Escala, Índice De Linhas, Índice De Linhas, Índice De Padrões (Sampler Lado A Lado)*\
    */ *Mapa de Cores, Escala, Índice de Linhas, Índice de Linhas, Índice de Padrões, Posição do Centro do Padrão, Posição do Centro do Padrão (RG) Tamanho da esfera (B) (Cor Sampler Lado a Lado)**Define exatamente como a aleatoriedade de cores é parametrizada.
  * **Multiplicador de Parametrização de Cores**: *0.0 - 1.0* Mescla o efeito Parametrização acima.
  * **Afeta a Parametrização de Cor (somente Cor):** **RGB+Alpha, somente RGB, somente Alpha** Define como a Parametrização afeta a cor.
  * **Opacidade global (somente tons de cinza)**: *0.0 - 1.0* Define a opacidade global do bloco.
  * **Cor do plano de fundo**: *(valor em tons de cinza) / (valor da cor)*Define a cor do plano de fundo sólida.
  * **Ordem inversa de renderização**: *Falso/Verdadeiro* Ordem inversa de renderização para ir de trás para frente.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/tilesampler-ex2.png" width="256px"/></div> |
| --- |
|  |

*O exemplo mostra como os parâmetros são orientados por mapas de entrada (Distribuição de Padrões, Escala, Rotação).*

</td>
</tr>
</table>
