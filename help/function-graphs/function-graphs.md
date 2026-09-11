---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/function-graphs.html"
breadcrumb-title: ''
description: Saiba como criar e usar gráficos de função de Substance no Designer para criar funções personalizadas e redes de nós reutilizáveis.
helpx_creative_field: ""
helpx_description: Designer > Substance function graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: gráficos de função Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# gráficos de função Substance

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[![](../assets/function-1.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td style="border: 0;" valign="top">

[gráficos de função Substance](https://substance3d.adobe.com/) <b>processar valores únicos</b> (inteiros, flutuantes, vetores) em vez de dados de imagem (conjuntos inteiros de pixels). As funções também são Gráficos com redes de nós, mas os [Nós usados](../function-graphs/nodes-reference-for-fun/function-nodes-overview/function-nodes-overview.md)e a interface é diferente dos [gráficos de Substance regulares](../compositing-graphs/substance-compositing-graphs.md). O fluxo de trabalho é completamente baseado em <b>operações matemáticas</b> e não mostra miniaturas de visualização de imagem, tornando-o uma <b>maneira muito mais avançada de trabalhar</b> com o Substance 3D Designer.

As funções podem ser usadas em muitos contextos diferentes, sendo os principais a modificação do comportamento de [um Parâmetro exposto](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), a criação do comportamento de [Processadores de pixels](../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) ou [FX-Maps](../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) e o uso de [valores em gráficos de Substance](../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md).

</td>
</tr>
</table>

## Exemplos

Abaixo estão alguns exemplos de casos de uso comuns para Funções.

### Função Simples

![](../assets/lerpfunction_1.png)

Uma função simples no contexto de um parâmetro exposto. Ele obtém um valor de flutuação de entrada chamado “Intensidade”, que é determinado para ir de 0 a 1 (um intervalo fácil de entender) e o remapeia para um intervalo definido de 0,1 a 0,8. Isso significa que se o usuário definir Intensidade como 0, internamente será usado 0,1, se a interface estiver definida como 1, será usado 0,8 e qualquer valor intermediário será interpolado linearmente. Este tipo de função é algo comumente usado ao [expor parâmetros](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), mas usar funções personalizadas.

Esta função também pode ser escrita como *lerp(0.1, 0.8, Intensity)* em um pseudocódigo semelhante a HLSL ou GLSL.

### Função Avançada

![](../assets/pixel-function_1.png){width="545px"}

Esta Função avançada mostra o funcionamento interno de um [Processador de pixels](../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) destinado ao ajuste da Matiz de uma entrada do mapa de cores com base na intensidade de uma segunda entrada de máscara em tons de cinza.

Ele faz a amostragem de ambas as entradas com a variável “$pos” do sistema, retira o Alpha, converte o valor da cor em HSL e modifica o componente Matiz, multiplicando-o pelo valor da amostra de tons de cinza. Depois, ele remonta o vetor, converte o HSL de volta para RGB e adiciona o Alpha de volta para a saída final.

em pseudo-código esta seria uma função muito mais complicada que não caberia em uma única linha.
