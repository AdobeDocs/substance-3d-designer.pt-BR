---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter.html"
breadcrumb-title: ''
description: Use o nó respingo de forma para dispersão formas entre texturas para criar padrões e detalhes de procedimentos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: respingos de forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---


# respingos de forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter.png){width="128px"}

## respingos de forma

**Entrada:** *Geradores De Textura**/Padrões*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Um nó muito complexo, projetado para ser usado em conjunto com os nós acompanhantes [Mistura de respingo de forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-blend/shape-splatter-blend.md), [Separador de forma para máscara](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-to-mask/shape-splatter-to-mask.md) e [Extração de dados de respingo de forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-data-ext/shape-splatter-data-extract.md). Usado para respingar formas de forma semelhante ao [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) ou ao [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), mas com um processo dinâmico e não destrutivo que permite o controle sobre cada etapa por meio de um sistema de vários níveis semelhante ao [Flood Fill.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) Enquanto o Flood Fill obtém um mapa de entrada base de uma fonte externa, o Shape Splatter gera o mapa e os dados subsequentes em uma única etapa, como uma espécie de versão mais avançada do [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md).

Seu principal objetivo é permitir a colocação de formas sobre e orientado por um mapa de height e, em seguida, gerar vários mapas a partir dos dados de Splatter. Por exemplo, colocar rochas, galhos e folhas em uma paisagem, orientada e conduzida por vários mapas. Mapas diferentes podem então ser usados para height, normal, basecolor, rugosidade e qualquer outro canal, enquanto todos ainda são baseados nos mesmos dados de respingo compartilhados.

## Parâmetros

### Entradas

* **Height de plano de fundo**: *Entrada em tons de cinza* height de plano de fundo para inserir blocos e direcionar vários efeitos.
* **Padrão 1-8**: *Entrada Em Tons De Cinza**Padrão Opcional*
* **Distribuição de Padrão**: *Entrada em Tons de Cinza* mapear para
* **Escala de forma**: *Entrada em tons de cinza* mapa em tons de cinza para dimensionar ladrilhos de unidade.
* **Rotação de Forma**: *Entrada em Tons de Cinza* mapa em Tons de Cinza para girar ladrilhos.
* **Deslocamento de Height**: *Entrada em tons de cinza* mapa em tons de cinza a ser usado como um deslocamento para height de blocos.
* **Escala de Height**: *Entrada em tons de cinza* mapa em tons de cinza a ser usado como um deslocamento para height de blocos.
* **Máscara aleatória**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.
* **Mapa vetorial**: *Entrada de cores* Mapa vetorial de cores para orientar o posicionamento e a rotação de blocos.

### Parâmetros

* Valor **X**: *1 - 64*\
  Quantidade de repetições X do padrão.
* **Valor de Y**: *1 - 64*\
  Quantidade de repetições Y do padrão.
* **Padrão**
  * **Número de Entrada de Padrão**: *1 - 8* Defina a quantidade de padrões diferentes a serem usados. Desbloqueia novos slots de Entrada de padrão.
  * **Modo de Distribuição de Padrão**: *Aleatório, Índice de Padrão, Índice de Linha, Índice de Coluna* Defina como determinar qual padrão usar. Aleatoriamente ou por padrão, linha ou coluna.
  * **Multiplicador de Mapa de Distribuição de Padrões**: *0.0 - 1.0* Defina a influência do mapa de Distribuição opcional para o posicionamento de padrões.
  * **Rotação de padrão**: *0, 90, 180, 270* Definir predefinição, rotação de padrões de 90 graus.
  * **Rotação de padrão aleatória**: *0.0 - 1.0* Defina a quantidade de rotação de etapa aleatória de 90 graus para padrões.
* **Tamanho**
  * **Escala**: *0.0 - 5.0*\
    Defina a escala uniforme para cada ladrilho.
  * **Escala aleatória**: *0.0 - 1.0* Aleatório, escala uniforme para cada ladrilho.
  * **Escala sem sobreposição**: *0.0 - 1.0* Dimensione aleatoriamente de maneira uniforme, mas somente para baixo, para evitar a sobreposição de blocos. Não deve ser usado em conjunto com os dois parâmetros anteriores.
  * **Multiplicador de Mapa de Escala**: *0.0 - 1.0* Definir influência do mapa de escala.
  * **Tamanho**: *0.0 - 1.0* Permite o dimensionamento não uniforme de blocos.
  * **Taxa de Tamanho da Inclinação Bg**: *0.0 - 1.0* Usa a inclinação do mapa de plano de fundo (Normal calculado) para dimensionar ladrilhos de maneira não uniforme. Simula a distorção de perspectiva.
  * **Taxa de Quantidade X/Y do Tamanho**: *0.0 - 1.0* Escala não uniforme para compensar uma taxa diferente nos Valores X e Y.
* **Posição**
  * **Posição Aleatória**: *0.0 - 2.0* Posição de deslocamento aleatório para cada bloco.
  * **Distribuição Aleatória**: *Gaussiana, Uniforme* Define o cálculo a ser usado para o parâmetro anterior. Não faz uma grande diferença, mais perceptível com números altos. Gaussiana tende a dar uma disseminação mais uniforme.
  * **Multiplicador de Mapa Vetorial**: *0.0 - 1.0* Influência do mapa de entrada de vetor em deslocamentos.
  * **Deslocamento horizontal**: *-2.0 - 2.0* Deslocamento horizontal global.
  * **Deslocamento vertical**: *-2.0 - 2.0* Deslocamento vertical global.
  * **Opção Fora dos Limites**: *Forma de Escala, Restringir Posição* Ação a ser executada quando um bloco parecer Fora dos Limites.
* **Rotação**
  * **Rotação**: *0.0 - 1.0* Gira globalmente todos os blocos.
  * **Rotação Aleatória**: *0.0 - 1.0* Gira aleatoriamente por bloco.
  * **Rotação da Inclinação Bg**: *0.0 - 1.0* Usa a inclinação do mapa de plano de fundo (normal calculado) para girar blocos. Pode ser usado para fazer com que as formas apontem para cima ou para baixo no inclinação.
  * **Multiplicador de Mapa de rotação**: *0.0 - 1.0* Combina o efeito de Mapa de rotação na rotação por Bloco.
  * **Multiplicador de Mapa Vetorial**: *0.0 - 1.0* Combina o efeito de Mapa de rotação na rotação por Bloco.
* **Height**
  * **Ajuste Automático da Escala de Heights**: *Falso/Verdadeiro* Ajuste automaticamente o intervalo de heights relativo ao plano de fundo, em vez de definir um intervalo absoluto. Permite menos ou mais controle.
  * **Deslocamento de Height**: *-1.0 - 1.0* Modificador para deslocar/mover todos os blocos uniformemente pelo intervalo de height.
  * **Deslocamento de Height Aleatório**: *0.0 - 1.0* Altera aleatoriamente o deslocamento de height por bloco.
  * **Multiplicador de Mapa de Deslocamento de Height**: *0.0 - 1.0* Modificador para definir a influência do Mapa de Deslocamento.
  * **Escala de Height**: *0.0 - 1.0* Modificador para dimensionar/expandir todos os blocos uniformemente sobre o intervalo de height. Em oposição a deslocar isso, afasta os valores, como contraste.
  * **Escala de Height Aleatória**: *0.0 - 1.0* Altera aleatoriamente a escala de height para cada bloco.
  * **Multiplicador de Mapa de Escala de Height**: *0.0 - 1.0* Modificador para definir a influência de Mapa de Escala.
  * **Conformidade com o plano de fundo**: *0.0 - 1.0* Afeta a mesclagem de blocos com o plano de fundo. Sem conformidade significa que os mapas de altura permanecem rígidos, o que significa que a forma de fundo a seguir. Bom para folhas vs varetas, por exemplo.
  * **Plano de fundo suave e em conformidade**: *0.0 - 2.0* Valor de suavização do efeito anterior, para evitar variações incorretas ou extremas.
  * **Inclinar da Inclinação Bg**: *0.0 - 1.0* height de blocos Ajustar/inclinação acionado pela inclinação de Plano de Fundo (normal calculado).
  * **Smoothness de Inclinação do plano de fundo**: *0.0 - 2.0* Valor de suavização do efeito anterior, para evitar variações incorretas ou extremas.
  * **Recortar pixels pretos**: *Falso/Verdadeiro* Alterne para ignorar pixels pretos completos (0) das formas de base lado a lado.
  * **Base do Padrão Nivelado**: *Falso/Verdadeiro* Ajusta o comportamento de mesclagem do bloco com o plano de fundo: os blocos se cruzarão com o plano de fundo (Falso) ou substituirão o plano de fundo quando menor.
* **Mascaramento**
  * **Máscara aleatória**: *0.0 - 1.0* Oculta os blocos aleatoriamente. Quanto maior esse valor, mais blocos desaparecerão.
  * **Multiplicador de Mapa Aleatório de Máscara**: *0.0 - 1.0* Limite para mapa de máscara quando iniciar a ocultação de blocos.
  * **Máscara da Inclinação Bg**: *-1.0 - 1.0* Usa a inclinação do mapa de plano de fundo (normal calculado) para ocultar blocos.

## Imagens de exemplo

</td>
</tr>
</table>
