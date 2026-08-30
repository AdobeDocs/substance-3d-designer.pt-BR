---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/panorama-shape.html"
breadcrumb-title: ''
description: Use o nó Forma de panorama para criar formas mapeadas para coordenadas de panorama para geração de textura de ambiente.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Panorama Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forma de Panorama
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 6%

---


# Forma de Panorama

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](panorama-shape.resources/panorama-shape-1.png){width="128px"}

<b>Em:</b> Geradores De Textura > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este é um nó útil para gerar mapas panorâmicos processuais do tipo “Studio”. Permite colocar e modificar imagens de holofote, bem como definir suas propriedades HDR. Ele pode ser encadeado para várias formas.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Matriz de Formas</b> | Move ou traduz o resultado, que pode ser modificado ao interagir diretamente com a tela. |
| <b>Forma</b> <i>quadrado, disco</i> | Define o tipo de forma. |
| <b>Cor da forma</b> <i>(Valor da cor)</i> | Define a cor da forma. |
| <b>Intensidade da forma</b> <i>0.0 - 100.0</i> | Define a intensidade do HDR da forma. |
| <b>Borda Suave da Forma</b> <i>0.0 - 1.0</i> | Altera a suavidade da borda da forma. |
| <b>Intensidade do Ponto de Acesso</b> <i>0.0 - 100.0</i> | Define a intensidade de HDR do ponto ativo da forma. |
| <b>Tamanho do Ponto de Acesso</b> <i>0.0 - 1.0</i> | Altera o tamanho do ponto ativo dentro da forma. |
| <b>Queda do Ponto de Acesso</b> <i>0.0 - 1.0</i> | Altera a mesclagem de borda de declínio do ponto de acesso. |
| <b>Posição do Ponto de Acesso</b> <i>0.0 - 1.0</i> | Move o ponto ativo em relação à forma. |
| <b>Habilitar plano de fundo</b> <i>Falso/Verdadeiro</i> | Permite o preenchimento do plano de fundo com uma cor sólida. Observe que isso significa que você não pode mais encadeá-los por meio de mesclagem. |
| <b>Cor do plano de fundo</b> <i>(Valor da cor)</i> | Define a cor sólida do plano de fundo. |
| <b>Habilitar Entrada de Textura</b> <i>Falso/Verdadeiro</i> | Permite uma entrada personalizada em vez de um tipo de forma predefinido. |
