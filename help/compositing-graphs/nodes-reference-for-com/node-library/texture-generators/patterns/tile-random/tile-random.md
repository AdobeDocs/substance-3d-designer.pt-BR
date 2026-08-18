---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random.html"
breadcrumb-title: ''
description: Use o nó Aleatório de bloco para criar padrões de bloco aleatórios com variação de procedimento para efeitos de textura orgânica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lado a lado aleatório
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---


# Lado a lado aleatório

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-random.png){width="128px"}

## Mosaico aleatório (cor)

**Entrada:** *Geradores/Padrões*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

O Bloco Aleatório gera um padrão de bloco de procedimento que tem um pouco mais de caos nas formas do bloco do que seu correspondente, [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Ele faz isso dividindo aleatoriamente certos ladrilhos em ladrilhos menores. Sugerimos que você primeiro encontre o seu caminho em torno do Tile Generator antes de abordar o Telha Aleatória, como muitos conceitos são semelhantes.

O Bloco Aleatório é usado em vez de [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) quando a meta é um padrão mais antigo e menos organizado. No entanto, ele tem suas limitações. Portanto, considere o [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) para atender a quaisquer outras necessidades avançadas.

## Parâmetros

### Entradas

* **Entrada de Padrão**: *Entrada em Tons de Cinza (Entrada de Cores)*\
  Imagem de padrão personalizado, usada quando o parâmetro “Pattern” está definido como “Image Input”.
* **Entrada em segundo plano**: *Entrada em tons de cinza (entrada colorida)*

### Parâmetros

* Valor **X**: *1 - 64*\
  Quantidade de repetições X do padrão.
* **Valor de Y**: *1 - 64*\
  Quantidade de repetições Y do padrão.
* **Expansão não quadrada**: *Falso/Verdadeiro*\
  Permite a compensação de esmagamento e alongamento com proporções não quadradas.
* **Padrão**
  * **Padrão**: *Entrada De Padrão, Quadrado, Disco, Paraboloide, Sino, Gaussiano, Espinho, Pirâmide, Tijolo, Gradação, Ondas, Meio Sino, Sino Ondulado, Crescente, Cápsula, Cone*\
    Seleciona a forma de padrão a ser usada.
  * **Filtragem de Entrada de Imagem (Mecanismo > v4)**: *Bilinear + Mipmaps, Bilinear, Mais Próximo*
  * **Específico de Padrão**: *0.0 - 1.0*\
    Permite que você altere a forma do padrão selecionado. O efeito depende do padrão selecionado.
  * **Aleatório Específico de Padrão**: *0.0 - 1.0* O efeito de aleatoriedade depende do padrão selecionado.
  * **Rotação**: *0, 90, 180, 270, aleatório horizontal, aleatório vertical* Define a rotação em etapas de 90 graus, com aleatorização opcional.
  * **Rotação Aleatória**: *0.0 - 1.0* Adiciona rotação livre aleatória.
  * **Simetria aleatória**: **0.0 - 1.0** espelha aleatoriamente determinados padrões pelo Modo aleatório de Simetria selecionado. Quanto maior for esse valor, mais padrões serão espelhados.
  * **Modo Aleatório de Simetria**: *Horizontal + Vertical, Horizontal, Vertical* Determina o comportamento de espelhamento quando a Simetria aleatória é maior que 0.
* **Dividir**
  * **Modo**: *nenhum, automático, horizontal automático, vertical automático, h+v aleatório* Define a regra sobre como dividir blocos.
  * **Limite**: *0.0 - 1.0* Limite de tamanho para quando dividir um bloco.
  * **Multiplicador**: *0 - 10* Dividindo o multiplicador. Quanto maior esse valor, mais divisões.
* **Tamanho**
  * **X Aleatório**: *0.0 - 1.0* Aleatório não uniforme em escala sobre o eixo X.
  * **Y Aleatório**: *0.0 - 1.0* Aleatório dimensionamento não uniforme sobre o eixo Y.
* **Interstício**
  * **Modo**: *Em relação ao menor tijolo, em relação ao maior tijolo* Define a que tamanho de tijolo o interstício está relativo.
  * **Valor**: *0.0 - 1.0* Define o tamanho do espaço entre os tijolos.
* **Forma**
  * **Escala**: *0.0 - 1.0* Escala globalmente cada bloco.
  * **Escala Aleatória**: *0.0 - 1.0* Escala aleatória por bloco.
  * **Rotação**: *0.0 - 1.0* Rotação global para cada bloco.
  * **Rotação Aleatória**: *0.0 - 1.0* Gira aleatoriamente por bloco.
  * **Restrição de Rotação**: *False/True* Restringe a escala para que os blocos girados nunca se sobreponham.
* **Posição**
  * **Deslocamento**: *0.0 - 1.0*\
    Move ou traduz os ladrilhos globalmente, desliza somente no eixo X
  * **Deslocamento Aleatório**: *0.0 - 1.0* Deslocamento aleatório por bloco, slides somente sobre o eixo X
  * **Aleatório**: *0.0 - 1.0* Dispõe aleatoriamente a posição, os blocos se movem nos eixos X e Y.
  * **Restrições Aleatórias**: *Falso/Verdadeiro* Restringe a escala para que os blocos toquem, mas não se sobreponham. Reduz significativamente o efeito Posição aleatória.
* **Cor**
  * **Cor**: *(valor em tons de cinza) / (valor da cor)*Define a cor sólida para todos os blocos.
  * **Aleatório de cores**: *0.0 - 1.0* Aleatório de cores por bloco.
  * **Parametrização de Cor**: *nenhuma, área, tamanho x, tamanho y* Torna a variação de cor dependente de uma dessas configurações.
  * **Intensidade de parametrização de cor**: *0.0 - 1.0* Multiplicador para o efeito Parametrização acima.
  * **Efeito de Parametrização de Cor (somente para Cor):** **RGB+Alpha, somente RGB, somente Alpha** Determina o efeito de parametrização somente de cor.
  * **Cor do plano de fundo**: *(valor em tons de cinza) / (valor da cor)*Define a cor do plano de fundo sólida.
  * **Modo de Mesclagem**: *Adicionar/Sub, Máx. /* Adicionar/Sub, Alpha de Mesclagem (Cor)**Define o modo de mesclagem para blocos no plano de fundo.
* **Máscara**
  * **Aleatório**: *0.0 - 1.0* Inicia aleatoriamente o mascaramento de blocos externos. Quanto maior o valor, mais blocos desaparecem.
  * **Inverter**: *Falso/Verdadeiro*\
    Inverte o resultado da máscara.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/tile-random-1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
