---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter.html"
breadcrumb-title: ''
description: Use o nó respingo de forma para dispersão formas no textura a fim de criar padrões e detalhes processuais.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: respingos de forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 7%

---


# respingos de forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-splatter.resources/shape-splatter.png){width="128px"}

<b>Em:</b> Geradores De Textura > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Um nó muito complexo, projetado para ser usado em conjunto com os nós acompanhantes [Shape Splatter Combinar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-blend/shape-splatter-blend.md), [Shape Splatter to Mask](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-to-mask/shape-splatter-to-mask.md) e [Shape Splatter Data Extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-data-ext/shape-splatter-data-extract.md). Usado para respingar formas de forma semelhante ao [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) ou ao [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), mas com um processo dinâmico e não destrutivo que permite o controle sobre cada etapa por meio de um sistema de vários níveis semelhante ao [Flood Fill.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) Enquanto o Flood Fill obtém um mapa de entrada base de uma fonte externa, o Shape Splatter gera o mapa e os dados subsequentes em uma única etapa, como uma espécie de versão mais avançada do [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md).

Seu principal objetivo é permitir a colocação de formas sobre e orientado por um mapa de altura e, em seguida, gerar vários mapas a partir dos dados de Splatter. Por exemplo, colocar rochas, galhos e folhas em uma paisagem, orientada e conduzida por vários mapas. Mapas diferentes podem então ser usados para height, normal, basecolor, rugosidade e qualquer outro canal, enquanto todos ainda são baseados nos mesmos dados de respingo compartilhados.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Height de fundo</b> <i>Entrada em tons de cinza</i> | Height de fundo para inserir ladrilhos e gerar vários efeitos. |
| <b>Padrão 1-8</b> <i>Entrada em tons de cinza</i> | Padrão opcional |
| <b>Distribuição de Padrões</b> <i>Entrada em tons de cinza</i> | Mapa em tons de cinza para |
| <b>Escala de Forma</b> <i>Entrada em tons de cinza</i> | Mapa em tons de cinza para dimensionar o ladrilho. |
| <b>Rotação de Forma</b> <i>Entrada em tons de cinza</i> | Mapa em tons de cinza para girar o ladrilho. |
| <b>Deslocamento de Height</b> <i>Entrada em tons de cinza</i> | Mapa em tons de cinza para usar como deslocamento no height lado a lado. |
| <b>Escala de Height</b> <i>Entrada em tons de cinza</i> | Mapa em tons de cinza para usar como deslocamento no height lado a lado. |
| <b>Máscara aleatória</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |
| <b>Mapa vetorial</b> <i>Entrada de cores</i> | Mapa vetorial de cores para orientar o posicionamento e a rotação do bloco. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Valor X</b> <i>1 - 64</i> | Quantidade de repetições X do padrão. |
| <b>Valor Y</b> <i>1 - 64</i> | Quantidade de repetições Y do padrão. |
| <b>Padrão</b> |  |
| <b>Número de Entrada de Padrão</b> <i>1 - 8</i> | Defina a quantidade de diferentes padrões a serem usados. Desbloqueia novos slots de Entrada de padrão. |
| <b>Modo de Distribuição de Padrão</b> <i>Aleatório, Índice de Padrão, Índice de Linha, Índice de Coluna</i> | Defina como determinar qual padrão usar. Aleatoriamente ou por padrão, linha ou coluna. |
| <b>Multiplicador de Mapa de Distribuição de Padrões</b> <i>0.0 - 1.0</i> | Defina a influência do mapa de distribuição opcional para o posicionamento dos padrões. |
| <b>Rotação de padrão</b> <i>0, 90, 180, 270</i> | Defina uma predefinição, rotação de padrões em 90 graus. |
| <b>Rotação de padrão aleatória</b> <i>0.0 - 1.0</i> | Defina a quantidade de rotação de passo aleatória de 90 graus para padrões. |
| <b>Tamanho</b> |  |
| <b>Escala</b> <i>0.0 - 5.0</i> | Defina a escala uniforme para cada ladrilho. |
| <b>Escala aleatória</b> <i>0.0 - 1.0</i> | Tornar a escala uniforme aleatória para cada ladrilho. |
| <b>Escala sem sobreposição</b> <i>0.0 - 1.0</i> | Dimensione aleatoriamente de maneira uniforme, mas somente para baixo, para evitar ladrilhos sobrepostos. Não deve ser usado em conjunto com os dois parâmetros anteriores. |
| <b>Multiplicador de Mapa de Escala</b> <i>0.0 - 1.0</i> | Definir influência do mapa de escala. |
| <b>Tamanho</b> <i>0.0 - 1.0</i> | Permite um dimensionamento não uniforme dos ladrilhos. |
| <b>Proporção de Tamanho da Inclinação de Erro</b> <i>0.0 - 1.0</i> | Usa a inclinação do mapa de plano de fundo (Normal calculado) para dimensionar ladrilhos de maneira não uniforme. Simula uma distorção de Perspectiva. |
| <b>Taxa de Quantidade X/Y do Tamanho</b> <i>0.0 - 1.0</i> | Escala não uniforme para compensar uma proporção diferente nos Valores X e Y. |
| <b>Posição</b> |  |
| <b>Posição Aleatória</b> <i>0.0 - 2.0</i> | Deslocar aleatoriamente a posição de cada peça. |
| <b>Distribuição Aleatória</b> <i>Gaussiano, Uniforme</i> | Define o cálculo a ser usado para o parâmetro anterior. Não faz uma grande diferença, mais perceptível com números altos. Gaussiana tende a dar uma disseminação mais uniforme. |
| <b>Multiplicador de Mapa Vetorial</b> <i>0.0 - 1.0</i> | Influência do mapa de entrada de vetor nos deslocamentos. |
| <b>Deslocamento horizontal</b> <i>-2.0 - 2.0</i> | Deslocamento horizontal global. |
| <b>Deslocamento vertical</b> <i>-2.0 - 2.0</i> | Deslocamento vertical global. |
| <b>Opção Fora dos Limites</b> <i>Dimensionar Forma, Restringir Posição</i> | Ação a ser executada quando um bloco aparece Fora dos Limites. |
| <b>Rotação</b> |  |
| <b>Rotação</b> <i>0.0 - 1.0</i> | Gira globalmente todos os blocos gráficos. |
| <b>Rotação aleatória</b> <i>0.0 - 1.0</i> | Gira aleatoriamente por bloco. |
| <b>Rotação da Inclinação de erros</b> <i>0.0 - 1.0</i> | Usa a inclinação do mapa de plano de fundo (normal calculado) para girar os ladrilhos. Pode ser usado para fazer com que as formas apontem para cima ou para baixo no inclinação. |
| <b>Multiplicador de Mapa de rotação</b> <i>0.0 - 1.0</i> | Combinar no efeito de Mapa de rotação na rotação por bloco. |
| <b>Multiplicador de Mapa Vetorial</b> <i>0.0 - 1.0</i> | Combinar no efeito de Mapa de rotação na rotação por bloco. |
| <b>Height</b> |  |
| <b>Ajuste Automático De Escala De Height</b> <i>Falso/Verdadeiro</i> | Ajuste automaticamente o intervalo de heights em relação ao plano de fundo, em vez de definir um intervalo absoluto. Permite menos ou mais controle. |
| <b>Deslocamento de Height</b> <i>-1.0 - 1.0</i> | Modificador para deslocar/mover todos os ladrilhos uniformemente pela faixa de height. |
| <b>Deslocamento de Height Aleatório</b> <i>0.0 - 1.0</i> | Altera aleatoriamente o deslocamento de height em uma base por ladrilho. |
| <b>Multiplicador de Mapa de Deslocamento de Height</b> <i>0.0 - 1.0</i> | Modificador para definir influência de Offset Map. |
| <b>Escala de Height</b> <i>0.0 - 1.0</i> | Modificador para dimensionar/expandir todos os ladrilhos uniformemente sobre a faixa de height. Em oposição a deslocar isso, afasta os valores, como contraste. |
| <b>Escala de Height aleatória</b> <i>0.0 - 1.0</i> | Altera aleatoriamente a escala do height em uma base por ladrilho. |
| <b>Multiplicador de Mapa de Escala de Height</b> <i>0.0 - 1.0</i> | Modificador para definir a influência do Mapa de Escala. |
| <b>Conformidade com o plano de fundo</b> <i>0.0 - 1.0</i> | Afeta a mesclagem de blocos com o plano de fundo. Sem conformidade significa que os mapas de altura permanecem rígidos, o que significa que a forma de fundo a seguir. Bom para folhas vs varetas, por exemplo. |
| <b>Plano de fundo suave</b> <i>0.0 - 2.0</i> | Valor de suavização do efeito anterior, para evitar variações incorretas ou extremas. |
| <b>Inclinar da Inclinação de erros</b> <i>0.0 - 1.0</i> | Height de telha de ajuste/inclinação acionado pela inclinação de fundo (normal calculado). |
| <b>Smoothness de Inclinação em segundo plano</b> <i>0.0 - 2.0</i> | Valor de suavização do efeito anterior, para evitar variações incorretas ou extremas. |
| <b>Recortar pixels pretos</b> <i>Falso/Verdadeiro</i> | Alterne para ignorar pixels totalmente pretos (0) das formas de base lado a lado. |
| <b>Achatar base de padrão</b> <i>Falso/Verdadeiro</i> | Ajusta o comportamento de mesclagem dos ladrilhos com o plano de fundo: os ladrilhos se cruzarão com o plano de fundo (Falso) ou substituirão o plano de fundo quando menor. |
| <b>Mascaramento</b> |  |
| <b>Máscara aleatória</b> <i>0.0 - 1.0</i> | Oculta ladrilhos aleatoriamente. Quanto maior esse valor, mais blocos desaparecerão. |
| <b>Multiplicador de Mapa Aleatório de Máscara</b> <i>0.0 - 1.0</i> | Limite do mapa de máscaras quando iniciar a ocultação de ladrilhos. |
| <b>Mascarar da Inclinação de erros</b> <i>-1.0 - 1.0</i> | Usa a inclinação do mapa do plano de fundo (Normal calculado) para ocultar os blocos. |
