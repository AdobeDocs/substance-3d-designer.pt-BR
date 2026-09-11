---
title: respingo de forma v2 para máscara
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Gerador > Padrão > respingo de forma v2 para máscara
source-git-commit: f688c618b01d3ca8059e67cf0797268e44e94b17
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 0%

---


# respingo de forma v2 para máscara

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![respingo de forma v2 para ícone de máscara](shape-splatter-v2-to-mask.png "respingo de forma v2 para máscara")

<b>Entrada:</b> Gerador > Padrão

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Computa uma máscara a partir de uma seleção de formas geradas pelo nó [respingo de forma v2](../shape-splatter-v2/shape-splatter-v2.md) .<br><br>As opções disponíveis incluem a seleção aleatória, bem como a seleção de intervalos de formas por identificador exclusivo e/ou ID de material/ID de padrão*.<br><br>As formas são pré-mascaradas pelo nó [respingo de forma v2](../shape-splatter-v2/shape-splatter-v2.md) a partir da <i>mesclagem de height</i> com o height de plano de fundo.<br>O plano de fundo e as formas não selecionadas são totalmente pretos. (Ou seja, um valor de 0)<br><br><b>*:</b> Um dos valores recuperados da entrada UVW de respingo de Forma é a ID de material ou a ID de padrão, dependendo do <b>tipo de forma</b> usado no nó de respingo de Forma v2:<br>- <i>SDF/primitivo</i>: ID de Material<br>- <i>Entrada/Grade de atlas de padrão:</i> ID de padrão, ou seja, o índice do padrão na lista/atlas.

</td>
</tr>
</table>

>[!INFO]
>
> Este nó requer dados de entrada gerados pelo nó [respingo de forma v2](../shape-splatter-v2/shape-splatter-v2.md).
> 
> Outros nós na família Shape splatter v2:
> * [Escala de cinza do mapeador de respingo de forma v2](../shape-splatter-v2-mapper-grayscale/shape-splatter-v2-mapper-grayscale.md)
> * [Cor do mapeador do respingo de forma v2](../shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md)

>[!TIP]
> 
> A [**&#39;Rusty bolts&#39;** amostra de material](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md#material-sample) está disponível para começar com os nós Shape splatter v2.
> 
> Para saber mais sobre conceitos e fluxos de trabalho que envolvem Funções SDF, acesse a página dedicada: [Trabalhando com Funções SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md)

<a name="inputs"></a>

## Entradas

|                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:----------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Splatter UVW</b> *Cor* | <b>R</b> - Componente U dos UVs das formas.<br><b>G</b> - Componente V dos UVs das formas.<br><b>B</b> - height das formas. (W)<br><b>A</b> - Dados empacotados:<br> - <i>Parte inteira:</i> O identificador exclusivo das formas. (ID)<br> - <i>Parte fracionária:</i> depende do <b>tipo de forma</b>: ID de material se SDF/primitiva, ID de padrão* se entrada/grade de atlas de padrão.<br><br><b>*:</b> A ID de padrão é o índice da forma na lista/atlas. |

<a name="outputs"></a>

## Saídas

|               |                                           |
|:--------------|:------------------------------------------|
| <b>Saída</b> | A máscara calculada das formas selecionadas. |

<a name="parameters"></a>

## Parâmetros

|                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Saída</b> *Inteiro* | Os valores usados para as formas selecionadas na máscara de saída.<br><br>- <b>Máscara binária:</b> todas as formas selecionadas usam um valor de 1.<br>- <b>ID de forma (inteiro):</b> as formas selecionadas usam seu identificador exclusivo. (ID)<br>- <b>ID de Material (inteiro):</b> as formas selecionadas usam sua ID de material.<br>- <b>ID de Forma (normalizada):</b> as formas selecionadas usam seu identificador exclusivo (ID) mapeado para o intervalo [0, 1], da menor ID selecionada para a maior.<br>- <b>ID de Material (normalizada):</b> as formas selecionadas usam sua ID de material mapeada para o intervalo [0, 1] da menor ID de material selecionada para a maior. |
| <b>Intervalo inicial da ID da forma</b> *Inteiro* | O identificador exclusivo da forma (ID) usado como o início do intervalo de seleção. (Incluído) |
| <b>Intervalo final da ID da forma</b> *Inteiro* | O identificador exclusivo da forma (ID) usado como o final do intervalo de seleção. (Incluído) |
| <b>Deslocamento da ID da forma</b> *Inteiro* | Desloca os identificadores exclusivos das formas pelo valor especificado, no contexto do intervalo de seleção.<br><br>Isso facilita o deslocamento da seleção atual pelo valor especificado sem precisar ajustar manualmente os limites inicial e final. |
| <b>Combinação de máscara de ID de material/padrão</b> *Inteiro* | Especificado o operador lógico usado para combinar a seleção por identificador exclusivo (ID) com a seleção por ID de material/ID de padrão.<br><br>- <b>Nenhum:</b> Ignore totalmente a ID de material/ID de padrão para a seleção.<br>- <b>E:</b> As formas selecionadas devem ser incluídas nos intervalos de ID e ID de material/ID de padrão. (Inclui menos formas)<br>- <b>OU:</b> As formas selecionadas devem ser incluídas nos intervalos de ID ou ID de material/ID de padrão. (Inclui mais formas) |
| <b>Intervalo inicial de ID de material/padrão</b> *Inteiro* | A ID de material ou ID de padrão* usada como o início da faixa de seleção. (Incluído)<br><br><b>*:</b> Consulte a descrição do nó para obter detalhes. |
| <b>Intervalo final de ID de material/padrão</b> *Inteiro* | A ID de material ou ID de padrão* usada como o final da faixa de seleção. (Incluído)<br><br><b>*:</b> Consulte a descrição do nó para obter detalhes. |
| <b>Máscara aleatória da forma</b> *Flutuante* | Um fator para o mascaramento aleatório de formas, onde 1 significa que todas as formas estão mascaradas. |

