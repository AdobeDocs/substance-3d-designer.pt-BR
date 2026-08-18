---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-scatter.html"
breadcrumb-title: ''
description: Use o nó Atlas scatter para dispersão texturas em um atlas a fim de criar padrões lado a lado a partir de materiais digitalizados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Scatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas scatter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1226'
ht-degree: 0%

---


# Atlas scatter

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/atlas-scatter.png){width="200px"}

## Atlas scatter

**Entrada:** *Filtros de Material/Processamento de Digitalização*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Extraia elementos de um Atlas e dispersão-os em um plano de fundo. As entradas Atlas são materiais completos, consistindo em elementos individuais organizados e embalados em uma única folha de textura. Este nó os divide (usando um processo interno de [Atlas splitter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-splitter/atlas-splitter.md)) e os dispersão, semelhante a [Divisória de Forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md). O atlas scatter requer no mínimo uma entrada do mapa de Opacidade e uma entrada do mapa de Height para o Atlas funcionar.

>[!NOTE]
>
> Centenas de [Atlas](https://source.substance3d.com/allassets?assetType=substanceAtlas), prontos para uso no nó do Atlas scatter, estão disponíveis em [Substance Source](https://source.substance3d.com/).

## Entradas e Parâmetros

### Parâmetros

* **Resolução da Entrada Atlas**: *Resolução, 1 a 12*\
  Defina manualmente a resolução do atlas de entrada completo para garantir um bom desempenho versus uma taxa de qualidade.
* Valor **X**: *1 - 64*\
  Quantidade de repetições X do padrão.
* **Valor de Y**: *1 - 64*\
  Quantidade de repetições Y do padrão.
* **Padrão**
  * **Intervalo de Padrões**: *0 - 10*\
    Define o intervalo de padrões a serem dispersos. Se definido como 0, todos os padrões serão usados.
  * **Modo de Distribuição de Padrão**: *Aleatório, Índice de Padrão, Índice de Linha, Índice de Coluna* Define a ordem na qual os elementos atlas são usados.
  * **Multiplicador de Mapa de Distribuição de Padrões**: *0.0 - 1.0*\
    Selecione o padrão de forma em função do valor de tons de cinza da imagem de entrada.
  * **Rotação de Padrão**: *0, 90, 180, 270*\
    Aplica uma rotação fixa a cada elemento do atlas, de acordo com a quantidade selecionada de graus.
  * **Rotação de Padrão Aleatória**: *0.0 - 1.0*\
    Aplica uma rotação aleatória à parte definida dos elementos do atlas.
  * **Precisão de Detecção de Forma Atlas**: *Formas simples ou pequenas, Formas complexas ou grandes, Modo sem falha*\
    Define a precisão com que as formas são detectadas. Quanto maior a precisão, maior o impacto no desempenho.
  * **Reduzir a Opacidade do Atlas (detecção mais rápida)**: *-4 - 0*\
    Permite controlar a taxa de redução do mapa de opacidade do atlas de entrada, usado para detecção de formas. Uma resolução mais baixa melhora o desempenho às custas da precisão.
  * **Ignorar Forma Menor que**: *0.0 - 1.0* Define o tamanho mínimo que uma forma deve ter para ser detectada, expresso como proporção da imagem geral
* **Tamanho**
  * **Escala**: *0.0 - 5.0*\
    Define a escala relativa de formas dispersas.
  * **Escala aleatória**: *0.0 - 1.0*\
    Define o multiplicador para aplicar o dimensionamento aleatório a cada forma dispersa.
  * **Escala sem sobreposição**: *0.0 - 1.0*\
    Reduz a escala da forma para que ela não se sobreponha.
  * **Multiplicador de Mapa de Escala**: *0.0 - 1.0*\
    Multiplica a escala da forma em função do valor de tons de cinza da imagem de entrada.
  * **Tamanho**: *0.0 - 1.0*\
    Define a escala relativa de formas dispersas por comprimento (X) e largura (Y).
  * **Proporção de Tamanho da Inclinação de Erro**: *0.0 - 1.0*\
    Modifica a taxa de tamanho da forma em função da inclinação do height de plano de fundo.
  * **Preservar Proporções**: *0.0 - 1.0*\
    Determina por qual intensidade as proporções originais das formas dispersas devem ser preservadas, em vez de usar a proporção de células da grade, por exemplo, a proporção dos valores de Intensidade X e Intensidade Y.
* **Posição**
  * **Posição Aleatória**: *0.0 - 2.0*\
    Um multiplicador para mover cada forma em uma direção aleatória a partir do ponto de partida da grade.
  * **Distribuição Aleatória**: *Gaussiana, Uniforme*\
    Alterna de uma distribuição Gaussiana para uma Distribuição Uniforme para a posição aleatória. A distribuição gaussiana produzirá um resultado mais orgânico comparado com a distribuição uniforme.
  * **Multiplicador de Mapa Vetorial**: *0.0 - 1.0*\
    Controla a influência da entrada do mapa de vetor para mover as formas na direção do vetor especificado pelos canais vermelho (X) e verde (Y) do mapa.
  * **Deslocamento horizontal**: *-2.0 - 2.0*\
    Um multiplicador para deslocamento de posição ao longo do eixo X.
  * **Deslocamento Vertical**: *-2.0 - 2.0*\
    Um multiplicador para deslocamento de posição ao longo do eixo Y.
  * **Opção Fora dos Limites**: *Forma de Escala, Restringir Posição*\
    Devido à natureza técnica do respingo, as formas não podem ser desenhadas a mais de 2 células de tamanho de distância de sua posição original. Se uma forma ficar muito grande ou for movida para longe demais, você terá duas opções: - Dimensionar forma reduzirá o tamanho da forma quando ela atingir um limite - Restringir posição moverá a forma de volta à sua posição original
* **Rotação**
  * **Rotação**: *0.0 - 1.0*\
    Permite controlar a rotação local de todas as formas.
  * **Rotação Aleatória**: *0.0 - 1.0*\
    Um multiplicador para uma quantidade aleatória de rotação aplicada por forma.
  * **Rotação da Inclinação de erros**: *0.0 - 1.0*\
    Modifica a rotação da forma em função da inclinação do height de plano de fundo. Normalmente usado em combinação com o parâmetro “Size Ratio from Bg Inclinação”
  * **Multiplicador de Mapa de rotação**: *0.0 - 1.0*\
    Multiplica a rotação da forma em função do valor da imagem de entrada em tons de cinza.
  * **Multiplicador de Mapa Vetorial**: *0.0 - 1.0*\
    Define a rotação da forma em função da entrada da imagem vetorial.
* **Height**
  * **Ajuste Automático Da Escala Do Height**: *Falso/Verdadeiro*\
    Ajuste automaticamente o height em função da escala de padrão para manter o height da forma proporcional ao height do plano de fundo.
  * **Modo de Mesclagem**: *Mesclagem de Height, Teste de Alpha*\
    Define o método para resolver sobreposições de formas.
  * **Deslocamento de Height**: *-1.0 - 1.0*\
    Aplica um deslocamento global ao height de formas
  * **Deslocamento de Height Aleatório**: *0.0 - 1.0*\
    Um multiplicador para um deslocamento de height aleatório aplicado por forma
  * **Multiplicador de Mapa de Deslocamento de Height**: *0.0 - 1.0*\
    Multiplica o deslocamento do height de forma em função do valor de tons de cinza da imagem de entrada.
  * **Escala do Height**: *0.0 - 1.0*\
    Permite controlar a escala de height global das formas dispersas
  * **Escala de Height Aleatória**: *0.0 - 1.0*\
    Um multiplicador para uma escala de height aleatória aplicada por forma
  * **Multiplicador de Mapa de Escala de Height**: *0.0 - 1.0*\
    Multiplica a escala do height de forma em função do valor da imagem de entrada em tons de cinza.
  * **Em conformidade com o plano de fundo**: *0.0 - 1.0*\
    Em 0, o height da forma permanece intacto; em 1, o height da forma será deformado pelo plano de fundo subjacente do height.
  * **Plano de Fundo Suave**: *0.0 - 2.0*\
    Permite controlar a quantidade de suavização aplicada à deformação do height da forma quando ela está em conformidade com seu plano de fundo.
  * **Inclinar da Inclinação de erros**: *0.0 - 1.0*\
    Deforma o height da forma em função da inclinação do height do plano de fundo local: um gradiente linear correspondente à inclinação do plano de fundo é adicionado ao height da forma.
  * **Smoothness de Inclinação em segundo plano**: *0.0 - 2.0*\
    Controla a quantidade de suavização aplicada à inclinação de plano de fundo quando a forma é inclinada com base nessa inclinação.
  * **Recortar pixels pretos**: *Falso/Verdadeiro*\
    Ignora o valor preto das entradas de padrão.
  * **Base de Padrão Nivelado**: *Falso/Verdadeiro*\
    Permite nivelar a height do plano de fundo sob uma forma para que corresponda à height inicial.
* **Mascaramento**
  * **Máscara aleatória**: *0.0 - 1.0*\
    Mascara uma quantidade aleatória de formas, expressa como uma proporção da quantidade total.
  * **Multiplicador de Mapa Aleatório de Máscara**: *0.0 - 1.0*\
    Define o mascaramento de forma aleatório em função da entrada da imagem em tons de cinza.
  * **Máscara da Inclinação de erros**: *-1.0 - 1.0*\
    Controla o mascaramento das formas com base na inclinação do plano de fundo em seu local.
* **Cor**
  * **Ajuste de Cor**: *-1.0 - 1.0*\
    Permite ajustar as cores dos elementos dispersos globalmente.
  * **Aleatório de cores**: *0.0 - 1.0*\
    Um multiplicador para mudar os valores das cores por uma quantidade aleatória por forma.
  * **Cor do plano de fundo**: *0.0 - 1.0*\
    Muda as cores da forma para a cor do plano de fundo em seu local.
* **Normal**
  * **Inclinar da Inclinação de erros**: *0.0 - 1.0*\
    Inclinar a forma normal de acordo com a normal de fundo.
  * **Aleatório Normal**: *0.0 - 1.0*\
    Um multiplicador para inclinar a forma normal em uma quantidade aleatória por forma.
  * **Formato Normal**: *DirectX, OpenGL*\
    Alternar entre Formatos de mapa normais diferentes (inverte o canal verde)
* **Aspereza**
  * **Ajuste De Aspereza**: *-1.0 - 1.0*\
    Permite que você desloque a aspereza da forma global.
  * **Aspereza de plano de fundo**: *0.0 - 1.0*\
    Move a aspereza da forma para a aspereza do plano de fundo em sua localização.
  * **Aspereza aleatória**: *0.0 - 1.0* Um multiplicador para compensar a aspereza por uma quantidade aleatória por forma.

## Imagens de exemplo

![](../../../../../../assets/atlas-scatter-11.png){width="512px"}

</td>
</tr>
</table>
