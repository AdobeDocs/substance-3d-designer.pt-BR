---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/the-quadrant-node.html"
breadcrumb-title: ''
description: Use o nó Quadrante em FXMaps para dividir as texturas em quatro seções para criar variações e padrões lado a lado.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > The Quadrant Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: O Nó Quadrante
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4e61f5588fb279e139240ac5939d6b7e58e1027a
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 2%

---


# O Nó Quadrante

Muitos FX-Maps consistem inteiramente de cadeias de nós Quadrantes. Os nós Quadrant são o nó mais poderoso e flexível do grupo FX-Map, portanto vale a pena entender como esse nó funciona.

A coisa mais importante sobre os nós Quadrantes é que eles são o único nó que pode aumentar a profundidade ou *oitava*, do gráfico FX-Map. Cada nó Quadrante adiciona ao gráfico de árvore quádrupla subjacente; nenhum dos outros nós faz isso.

O nó Quadrante tem vários parâmetros:

## Cor/luminosidade

Quando o nó está adicionando uma imagem ao FX-Map, essas configurações definem como os canais são mesclados com outras imagens na cadeia. Os parâmetros *Cor / Luminosidade* se aplicam a todas as imagens renderizadas por este nó específico.

### Desvio da ramificação

Desloca a imagem do nó. O deslocamento é aplicado a todas as outras imagens renderizadas pelos nós subsequentes no gráfico. O Deslocamento de ramificação aplica a conversão ao nó Quadrante atual e a todos os nós abaixo dele na mesma ramificação do gráfico.

Este parâmetro pode ser controlado com uma Função Dinâmica.

### Padrão

Define a imagem (se houver) a ser adicionada ao FX-Map por esse nó.

Os nós Quadrantes oferecem suporte a uma longa lista de padrões, que serão descritos mais adiante neste tópico.

>[!WARNING]
>
> Este parâmetro não pode ser controlado por uma função dinâmica em um arquivo sbsar.

### Deslocamento do padrão

Desloca a imagem do nó de acordo com a quantidade especificada, mas não afeta os nós subsequentes. Este parâmetro pode ser controlado com uma Função Dinâmica.

### Tamanho do padrão

Define o tamanho da imagem (se aplicável) a ser adicionada ao FX-Map. Este parâmetro pode ser controlado com uma Função Dinâmica.

### Rotação padrão

Define a rotação da imagem (se aplicável) a ser adicionada ao FX-Map. Este parâmetro pode ser controlado com uma Função Dinâmica.

### Variação de padrão

Alguns padrões têm variantes. Essa configuração permite escolher qual variante usar. Este parâmetro pode ser controlado com uma Função Dinâmica.

### Modo de mesclagem

Especifica o processo de mesclagem a ser usado ao misturar a imagem desse nó (se aplicável) com a imagem FX-Map. Este parâmetro pode ser controlado com uma Função Dinâmica.

### Semente aleatória

Propagação do gerador de números aleatórios.

O gerador usa essa semente como ponto de partida, criando uma sequência do que parece ser números aleatórios. A vantagem dessa abordagem é que, ao contrário do mundo real, você pode garantir que a mesma sequência exata de números aleatórios seja gerada a cada vez, produzindo resultados previsíveis, repetíveis, mas de aparência aleatória.

Este parâmetro pode ser controlado com uma Função Dinâmica.

### Herança aleatória

Se definido como “Sim”, a semente do gerador de números aleatórios é herdada do nó anterior no gráfico (ou seja, o nó acima deste na árvore quádrupla.) Se este é o primeiro nó, ele obtém sua semente aleatória do [gráfico de Substance](../../../compositing-graphs/substance-compositing-graphs.md) que o contém.

## Padrões

Cada nó Quadrante pode opcionalmente adicionar uma imagem ao FX-Map final.

Por padrão, a opção Nenhum padrão está selecionada, portanto nenhuma imagem é renderizada. O nó Quadrante simplesmente subdivide a imagem FX-Map, dividindo-a em quatro para o próximo nó na cadeia.

A próxima opção, *Imagem de entrada*, é usar uma imagem fornecida para o nó FX-Map. O nó FX-Map aceita imagens coloridas ou em tons de cinza para uso como plano de fundo ou como substituição de um dos padrões integrados. Observe que o nó Quadrante só pode renderizar uma imagem de entrada em tons de cinza em um Fx-Map em tons de cinza e, inversamente, só pode renderizar uma imagem de entrada colorida em um FX-Map colorido. Se quiser misturar tipos de cores, é necessário converter as entradas antes no gráfico.

Finalmente, você pode escolher um dos padrões incorporados: Quadrado, Disco, parabolóide, Sino, Gaussiano, Espinho, Pirâmide, Tijolo, Gradação, Ondas, Meio sino, Sino ondulado, Crescente e Cápsula.

Observação adicional: você tem a possibilidade de criar uma função dinâmica neste parâmetro, mas ela funcionará somente no Substance 3D Designer. Para ter acesso à entrada de imagem por uma função dinâmica, você terá que usar valores de 256 (entrada de imagem 1) a valores mais altos (257 para entrada de imagem 2 etc.).

### Tipos de padrão.

Todos os padrões são em tons de cinza. Algumas podem ser modificadas um pouco usando o parâmetro *Variação de padrão*.

Muitos dos padrões integrados têm alguma forma de preenchimento gradiente radial ou semelhante. Isso os torna muito úteis para muitos tipos de ruídos e padrões. Outros padrões, como tijolo, disco e quadrado, são formas simples e planas.

O parâmetro Variação de padrão ajusta um recurso definido do padrão.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](the-quadrant-node.resources/fxmap-quadrants.png){width="80px"}

</td>
<td style="border: 0;" valign="top">

![](the-quadrant-node.resources/quadrant-parameters.jpg)

</td>
</tr>
</table>
