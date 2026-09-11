---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/mask-to-paths.html"
breadcrumb-title: ''
description: Use o nó Máscara para caminhos para converter texturas de máscara em dados de caminho para geração de caminho de procedimento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Mask to Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mascarar caminhos
user-guide-description: ''
user-guide-title: ''
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 0%

---


# Mascarar caminhos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](mask-to-paths.resources/mask-to-paths-icon.png "Ícone de nó")

<b>Ferramentas de Spline e Caminho </b> > Ferramentas de Caminho

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Converte um padrão de entrada em tons de cinza <b>Máscara</b> em uma lista de segmentos de caminho codificados nos <b>Caminhos</b> de saída.

Controles sobre a posição inicial dos caminhos gerados, bem como sua ordem na lista, estão disponíveis.

Os Caminhos gerados podem ser processados posteriormente usando nós dedicados - Por exemplo, [Transformação de 2D de Caminho](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md), [Distorção de Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-warp/paths-warp.md) - ou convertidos em splines usando o nó [Caminho para Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) para mapear ou dispersão formas ao longo deles.

</td>
</tr>
</table>

>[!NOTE]
>
> O método usado para codificar caminhos é explicado na página [Especificações de formato de caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Máscara</b> <i>Tons de cinza</i> | O padrão de entrada que deve ser convertido em uma lista de Caminhos. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Visualizar</b> <i>Cor</i> | Uma visualização composta sobre a máscara para ajudar a visualizar os efeitos dos parâmetros. |
| <b>Caminhos</b> <i>Cor</i> | Uma lista de caminhos codificados em uma imagem colorida. cada caminho descreve uma lista de segmentos codificados.<br>O resultado pode ser processado usando outro nó de processamento de Caminhos ou enviado para um nó [Caminhos para Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) para processá-lo posteriormente como Splines. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Máscara suave</b> <i>Flutuante</i> | Aplique suavização na máscara de entrada.<br>Útil quando o padrão de entrada tem bordas muito nítidas, o que geralmente causa artefatos. |
| <b>Valor de Limite de Máscara</b> <i>Flutuante</i> | O valor em tons de cinza da <b>Máscara</b> que será usado para separar o exterior (valores &lt; Valor Limite da Máscara) e o interior (valores > Valor Limite da Máscara) da forma. |
| <b>Decimar Caminho</b> <i>Flutuante</i> | Controla implicitamente a quantidade de segmentos que será gerada.<br>Uma quantidade alta de decimação tornará as formas arredondadas um pouco poligonais, enquanto nenhuma decimação gerará quase um segmento por pixel.<br>Uma quantidade razoável corresponderá melhor à forma de linhas retas e curvas sem criar muitos pontos intermediários para linhas retas. |
| <b>Fechar caminhos abertos</b> <i>Booleano</i> | Crie um segmento entre os vértices inicial e final de caminhos abertos.<br>Desativar essa opção poderá corrigir linhas indesejáveis que atravessam o padrão de forma inesperada, mas os caminhos talvez não sejam mais fechados. |
| <b>Limite de Cantos</b> <i>Flutuante</i> | Cada vértice codificado em caminhos pode conter uma bandeira indicando se é duro (ou seja, um canto) ou suave.<br>Este parâmetro permite marcar mais ou menos cantos de acordo com o ângulo entre os segmentos adjacentes.<br><i>Observação:</i> no momento, nenhum nó existente oferece suporte a este sinalizador de &#39;canto&#39;, mas eles estão disponíveis para serem usados em um nó do [Processador de Vértice de Caminho](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md). Você também pode visualizar os cantos com o nó [Visualizar caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md). |
| <b>Modo de Inicialização do Caminho</b> <i>Inteiro</i> | O método de selecionar qual vértice deve ser o início de cada Caminho gerado ao redor das formas na Máscara.<br>Isso tem um impacto significativo ao converter os <b>Caminhos para Splines</b> gerados usando o nó dedicado, pois vários nós de Spline usam o início e o fim das Splines.<br>*- Vértice mais agudo:* O vértice que forma o ângulo mais baixo com seus vértices anteriores e seguintes <br>*- Vértice na extremidade de uma direção especificada:* O último vértice em uma determinada direção <br>*- Vértice mais próximo de uma posição especificada<br>* Vértice mais distante de uma direção posição especificada<br>* Função de inicialização personalizada:* Use uma função personalizada para selecionar o vértice que deve ser usado como o início de cada Caminho |
| <b>Direção da Inicialização</b> <i>Flutuante</i> | O ângulo que descreve a direção usada para selecionar o vértice de inicialização. Para cada Caminho, o último vértice nessa direção é selecionado.<br>O valor é um *número de voltas* usado para girar um vetor de direção X para a esquerda. Isso significa que 0 define um vetor de direção de (-1, 0), e 0,25 (90 graus) define um vetor de direção de (0, 1).<br><i>Observação:</i> este parâmetro está disponível quando o <b>Modo de Inicialização do Caminho</b> está definido como &#39;Vértice no extremo de uma direção especificada&#39; |
| <b>Posição de Destino de Inicialização</b> <i>Flutuante2</i> | A posição na imagem usada para selecionar o vértice de inicialização.<br>Para cada Caminho, o vértice mais próximo ou mais distante desta posição é selecionado, de acordo com o <b>Modo de Inicialização do Caminho</b> selecionado.<br><i>Observação:</i> este parâmetro está disponível quando o <b>Modo de Inicialização do Caminho</b> está definido como &#39;Vértice mais próximo de uma posição especificada&#39; ou &#39;Vértice mais distante de uma posição especificada&#39; |
| <b>Função de Inicialização</b> <i>Precisão decimal</i> | A função usada para selecionar o vértice de inicialização. Retorna um valor de Precisão decimal.<br>Para cada vértice, a função é executada e o vértice para o qual a função retorna o *maior resultado* é selecionado.<br>Variáveis disponíveis:<br>*-* vertex.cornerness(Precisão decimal)*:* A pontuação do vértice como candidato a um vértice <br>*-* vertex.pos(Precisão decimal 2)*:* A posição do vértice no espaço de imagem<br><i>Observação:</i> Este parâmetro está disponível quando o Modo de Inicialização do Caminho está definido como &#39;Vértice mais próximo de uma posição especificada&#39; ou &#39;Função de inicialização personalizada&#39; |
| <b>Modo de Pedido</b> <i>Inteiro</i> | O método de ordenação dos Caminhos gerados.<br>A *caixa delimitadora* dos Caminhos de posição ou tamanho (Bbox) pode ser usada como critério para ordenar os Caminhos.<br>Isso tem um impacto significativo ao converter os <b>Caminhos gerados em Splines</b> usando o nó dedicado, pois vários nós Spline usam a ordem dos Splines.<br>*- Legado (rápido):* O método usado na versão anterior deste nó, que oferece um desempenho significativamente melhor <br>*- Por posição central da Bbox ao longo da direção:* Os caminhos são ordenados de acordo com a do centro de sua caixa, do primeiro ao último ao longo da direção especificada <br>*- Por caixa de caixa de caixa de caixa de caixa superior à esquerda ao longo da direção:* Os caminhos são ordenados de acordo com a posição do canto superior esquerdo de sua caixa de caixa de caixa de caixa, do primeiro ao último ao longo da direção especificada <br>*- Por tamanho de caixa de bbox - Do maior ao menor:* Os caminhos são ordenados de acordo com o tamanho de sua caixa de bbox, do maior ao menor <br>*- Por tamanho de caixa de bbox - Do menor ao maior:* Os caminhos são ordenados de acordo com o tamanho de sua caixa de bbox, do menor para o maior <br>*- Função de ordenação personalizada:* Use uma função personalizada para ordenar Caminhos |
| <b>Direção da ordem</b> <i>Precisão decimal</i> | O ângulo que descreve a direção usada para ordenar os Caminhos do primeiro para o último ao longo dessa direção.<br>O valor é um *número de voltas* usado para girar um vetor de direção X para a esquerda. Isso significa que 0 define um vetor de direção de (-1, 0) e 0,25 (90 graus) define um vetor de direção de (0, 1). |
| <b>Ordenando função</b> <i>Precisão decimal</i> | A função usada para ordenar os Caminhos. Retorna um valor de Precisão decimal.<br>Os caminhos são ordenados em *ordem crescente* de acordo com o valor desta função. Em outras palavras, o resultado da função para cada Caminho é a *chave de classificação* usada para ordenar os Caminhos.<br>Variáveis disponíveis:<br>* bbox.center (Precisão decimal 2): a posição do centro da Caixa de Caminho<br>* bbox.topleft (Precisão decimal 2): a posição do canto superior esquerdo da Caixa de Caminho<br>* bbox.size (Precisão decimal 2): o tamanho da Caixa de Caminho (X: width, Y: height) |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="mask-to-paths.resources/MaskToPaths-Variant2-Before.jpg" alt="MaskToPaths-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="mask-to-paths.resources/MaskToPaths-Variant2-After.jpg" alt="MaskToPaths-Variant2-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="mask-to-paths.resources/MaskToPaths-Variant1-Before.jpg" alt="MaskToPaths-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="mask-to-paths.resources/MaskToPaths-Variant1-After.jpg" alt="MaskToPaths-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 2](mask-to-paths.resources/MaskToPaths-Demo2.gif "Exemplo de nó 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 1](mask-to-paths.resources/MaskToPaths-Demo1.gif "Exemplo de nó 1"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 3: Modos de inicialização](mask-to-paths.resources/MaskToPaths-Demo3.gif "Exemplo de nó 3: Modos de inicialização"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 3: modos de ordenação](mask-to-paths.resources/MaskToPaths-Demo4.gif "Exemplo de nó 3: modos de ordenação"){zoomable="yes"}

</td>
</tr>
</table>
