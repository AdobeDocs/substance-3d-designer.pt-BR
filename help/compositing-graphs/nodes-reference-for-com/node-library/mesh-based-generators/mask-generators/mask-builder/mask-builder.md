---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/mask-builder.html"
breadcrumb-title: ''
description: Use o nó Construtor de máscaras para combinar várias entradas de máscara e criar padrões de máscara complexos para efeitos de material.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Mask Builder
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Construtor de máscaras
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 10%

---


# Construtor de máscaras

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](mask-builder.resources/mask-builder.png){width="128px"}

<b>Entrada:</b> Geradores > Geradores de máscara Baseados em Malha

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Essa é basicamente a versão Designer do Construtor de máscaras do Painter.

É uma ferramenta complicada destinada como um criador de máscaras abrangente, com base em mapas baked, parâmetros do usuário e mapas e padrões de desgaste. Destina-se principalmente como um nó de controle completo muito avançado para misturar no dirt de vincos e desgaste de bordas. Este nó é poderoso o suficiente para imitar todos os outros Geradores de máscaras.

Não há necessidade explícita de cozedura, mas quanto mais você fornecer, mais esse nó será capaz de fazer.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Oclusão de ambiente</b> <i>Entrada em tons de cinza</i> |  |
| <b>Curvatura</b> <i>Entrada em tons de cinza</i> |  |
| <b>Espaço Mundial Normal</b> <i>Entrada de cores</i> |  |
| <b>Entrada de Desgaste</b> <i>Entrada em tons de cinza</i> |  |
| <b>Entrada de Desgaste 2</b> <i>Entrada em tons de cinza</i> |  |
| <b>Entrada de Dispersão</b> <i>Entrada em tons de cinza</i> | Carimbo de dispersão personalizado, necessário para usar os parâmetros de Dispersão. |
| <b>Máscara (opcional)</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |
| <b>Posição</b> <i>Entrada de cores</i> | Usado para efeitos Triplanar e Superior-Inferior. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Nível</b> <i>0.0 - 1.0</i> | Define o nível total do efeito, revelando gradualmente. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta o contraste do resultado. |
| <b>Inverter</b> <i>Falso/Verdadeiro</i> | Inverte o resultado. Útil para atingir o oposto da máscara que você está criando. |
| <b>Usar Triplanar</b> <i>Falso/Verdadeiro</i> | Permite a projeção triplanar, evitando costuras com mapas de desgaste. |
| <b>Contraste de Mesclagem Triplanar</b> <i>0.0 - 1.0</i> | Define o contraste para a Mesclagem triplanar. |
| <b>Desgaste</b> <i>0.0 - 1.0</i> | Define a quantidade de Desgaste para se misturar globalmente. |
| <b>Desgaste</b> |  |
| <b>Escala</b> <i>0 - 10</i> | Define a escala do Desgaste global. |
| <b>Usar Desgaste Personalizado</b> <i>Falso/Verdadeiro</i> | Habilita a entrada de Desgaste personalizado. |
| <b>Desgaste Personalizado Secundário</b> <i>0.0 - 1.0</i> | Habilita uma segunda entrada de Desgaste personalizado. |
| <b>Inverter</b> <i>Falso/Verdadeiro</i> | Inverte o mapa de Desgaste. |
| <b>AO</b> <i>-1.0 - 1.0</i> | Define a extensão em que o efeito deve aparecer nas áreas do AO ocultas. Pode ser ajustado com o grupo abaixo. |
| <b>AO</b> |  |
| <b>Intervalo</b> <i>0.0 - 1.0</i> | Define o limite ou intervalo para a aparência do dirt. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta o contraste do efeito AO. |
| <b>Ruído</b> <i>0.0 - 1.0</i> | Define a quantidade de ruído/desgaste a ser mesclada no efeito AO. |
| <b>Escala de Ruído</b> <i>0 - 10</i> | Define a escala do ruído/desgaste do AO. |
| <b>Tipo de Ruído</b> <i>Manchas, Nuvem, Umidade, Ruído Branco</i> | Alterna entre 4 tipos diferentes de ruído de AO. |
| <b>Inverter</b> <i>Falso/Verdadeiro</i> | Inverte a interpretação do mapa do AO: o ruído aparecerá nas áreas claras do AO, não nas escuras. |
| <b>Curvatura</b> <i>0.0 - 1.0</i> | Define quanto efeito deve aparecer nas bordas de curvatura; pode ser convexo e côncavo. Ajuste isso com o grupo abaixo. |
| <b>Curvatura</b> |  |
| <b>Intervalo Convexo</b> <i>-1.0 - 1.0</i> | Define o efeito que será exibido nas bordas de curvatura convexas (brilhantes). |
| <b>Contraste convexo</b> <i>0.0 - 1.0</i> | Define o contraste do efeito Convexo. |
| <b>Inversão Convexa</b> <i>Falso/Verdadeiro</i> | Inverte a interpretação das bordas convexas. |
| <b>Intervalo côncavo</b> <i>-1.0 - 1.0</i> | Define o efeito que será exibido nas bordas de curvatura côncavas (escuras). |
| <b>Contraste côncavo</b> <i>0.0 - 1.0</i> | Define o contraste do Intervalo côncavo. |
| <b>Inversão côncava</b> <i>Falso/Verdadeiro</i> | Inverte a interpretação das bordas côncavas. |
| <b>Smoothness</b> <i>0.0 - 16.0</i> | Quantidade de desfoque e suavização a ser aplicada às bordas de Curvatura. |
| <b>Aumento de Nível</b> <i>0.0 - 1.0</i> | Reforço adicional se o efeito não for suficientemente visível. |
| <b>Ruído</b> <i>0.0 - 1.0</i> | Define a influência do ruído/desgaste no efeito Curvatura. |
| <b>Escala de Ruído</b> <i>0 - 10</i> | Define a escala do ruído. |
| <b>Tipo de Ruído</b> <i>Manchas, Nuvem, Umidade, Ruído Branco</i> | Escolha entre 4 tipos de ruído diferentes. |
| <b>Gradiente Superior/Inferior</b> <i>-1.0 - 1.0</i> | Combinar ou máscaras com gradiente de cima para baixo com base no mapa de Posição. Valores positivos tornam as coisas mais brilhantes, valores negativos mascaram os efeitos existentes. |
| <b>Gradiente</b> |  |
| <b>Intervalo</b> <i>0.0 - 1.0</i> | Define a posição do gradiente. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta o contraste do gradiente. |
| <b>Inverter</b> <i>Falso/Verdadeiro</i> | Inverte o gradiente. Alterna efetivamente entre a parte inferior e a superior. |
| <b>Espaço Mundial Normal</b> <i>0.0 - 1.0</i> | Semelhante ao Gradiente superior/inferior, mas com o mapa de posição e em seis direções, semelhante à iluminação falsa. Valores positivos clareiam, valores negativos escurecem. |
| <b>Espaço Mundial Normal</b> |  |
| <b>Intensidade Superior</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensidade inferior</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensidade frontal</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensidade de fundo</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensidade correta</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensidade da esquerda</b> <i>-1.0 - 1.0</i> |  |
| <b>Scratches</b> <i>-1.0 - 1.0</i> | Combinar arranha as áreas brancas. |
| <b>Scratches</b> |  |
| <b>Valor</b> <i>0 - 4096</i> | Define a quantidade total de riscos. |
| <b>Escala</b> <i>0.0 - 1.0</i> | Define a escala de arranhões individuais. |
| <b>Dispersão</b> <i>-1.0 - 1.0</i> | Dispersão uma estampa personalizada dentro de áreas brancas. |
| <b>Dispersão</b> |  |
| <b>Escala</b> <i>0 - 50</i> | Escala total do efeito. |
| <b>Densidade</b> <i>0.0 - 1.0</i> | Controle de densidade de dispersão, número que deve aparecer. |
| <b>Tamanho</b> <i>0.0 - 4.0</i> | Tamanho do carimbo disperso. |
| <b>Variação de Tamanho</b> <i>0.0 - 1.0</i> | Variação no tamanho do carimbo. |
| <b>Variação de opacidade</b> <i>0.0 - 1.0</i> | Variação na opacidade do carimbo. |
