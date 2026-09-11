---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/function-graphs/variables/system-variables.html"
breadcrumb-title: ''
description: Saiba mais sobre as variáveis de sistema incorporadas disponíveis nos gráficos de função do Substance 3D Designer para fluxos de trabalho avançados.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Built-in variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variáveis internas
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 3%

---


# Variáveis internas

Você pode usar variáveis internas em [gráficos de função Substance](../../../function-graphs/function-graphs.md) para acessar valores específicos. Eles sempre começam com o símbolo `$` (dólar).

Algumas variáveis estão disponíveis apenas em contextos específicos.

<b>Todos os nós</b>

Variáveis do sistema

| Nome | Tipo | Finalidade |
| --- | --- | --- |
| $size | Float2 | Retorna o tamanho do nó atual em pixels.   Se usado no parâmetro [Tamanho de Saída](../../../compositing-graphs/output-size/output-size.md) definido como um *Método de herança [Relativo a...* &lbrace;4](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md), retorna o *valor herdado*. |
| $sizelog2 | Float2 | Como acima, mas retorna o tamanho como valores power-of-2 (por exemplo: para a imagem 2048\*2048, `$sizelog2` retorna 11).   Se usado no parâmetro [Tamanho de Saída](../../../compositing-graphs/output-size/output-size.md) definido como um *Método de herança [Relativo a...* &lbrace;4](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md), retorna o *valor herdado*. |
| $pixelratio | Integer | Retorna um valor inteiro correspondente à proporção de pixels do nó atual (herdada ou absoluta): 0: Esticar 1: Quadrado |
| $tiling | Integer | Retorna um valor inteiro correspondente ao modo de divisão em blocos gráficos do nó atual (herdado ou absoluto): 0: Sem divisão em blocos gráficos 1: Divisão em blocos horizontais 2: Divisão em blocos verticais 3: Divisão em blocos gráficos H e V |
| $physicalsize | Float3 | Retorna o valor da propriedade <b>Tamanho físico</b>[&#128279;](../../../compositing-graphs/graph-parameters/graph-parameters.md) do gráfico . |
| $uvtile | Integer2 | Ao usar fluxos de trabalho UDIM, essa variável retorna o índice do udim atual em U e V.   Por exemplo, (2, 0) para o bloco 1003, (7, 11) para o bloco 1118, ... |

<b>FX-Map</b>

Variáveis do sistema

| Nome | Tipo | Finalidade |
| --- | --- | --- |
| $pos | Float2 | Retorna a posição de nascimento do padrão. A origem (0, 0) está localizada no canto superior esquerdo da imagem. |
| $profundidade | Float | Retorna o número de oitava (nível) do nó [FX-Map](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md). Isso permite que um nó modifique seu comportamento de acordo com o nível na árvore quádrupla que representa. |
| $depthpow2 | Float | Como acima, mas retorna o inverso multiplicativo de 2 elevado à potência do número de oitava (nível) - ou seja, 1/(2^octave). Esse é um valor auxiliar que é útil para alguns cálculos comuns. |
| $number | Float | Retorna o número do padrão desenhado. Isso pode ser acessado pelos gráficos de Função Dinâmica que controlam um nó [Iterar](../../../function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-var/iterate-and-number-variable.md) para modificar seu comportamento em cada etapa de iteração.   Observe que `$number` começa a contar de 0, não de 1.   Ao usar uma cadeia de nós Iterate, a variável `$number` retornará o número de iteração do último nó Iterate conectado antes do parâmetro de função usado. Se você deseja recuperar o número de iteração de vários nós Iterar, use “variáveis personalizadas” por meio de nós [Definir](../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md). |

<b>Processador de pixels</b>

Variáveis do sistema

| Nome | Tipo | Finalidade |
| --- | --- | --- |
| $pos | Float2 | Retorna a posição do pixel que está sendo avaliado. |

<b>Global</b>

Variáveis do sistema

| Nome | Tipo | Finalidade |
| --- | --- | --- |
| $time | Float | Esta variável retorna o tempo em segundos desde que o Substance Engine foi iniciado. Pode ser usado em gráficos que o resultado deve mudar de acordo com o tempo decorrido.  **Observação:** embora no momento não seja possível fazer essa alteração de valor no Designer, os aplicativos que integram o Substance Engine podem aproveitá-la, como o [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html) para animação ou o [Substance 3D Painter](https://experienceleague.adobe.com/pt-br/docs/substance-3d-painter/using/home) para [traçados dinâmicos](https://experienceleague.adobe.com/pt-br/docs/substance-3d-painter/using/painting/dynamic-strokes/creating-custom-dynamic-strokes). |
| $normalformat | Integer | O formato normal (ou seja, DirectX ou OpenGL) usado no ambiente atual.  **Observação:** esta variável não tem efeito no Designer e pode ser usada por outros aplicativos que integram o Substance Engine. |
