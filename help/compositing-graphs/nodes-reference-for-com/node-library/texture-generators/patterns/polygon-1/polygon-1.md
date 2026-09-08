---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/polygon-1.html"
breadcrumb-title: ''
description: Use o nó Polígono 1 para gerar padrões poligonais básicos com lados e propriedades personalizáveis para texturas geométricas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Polygon 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Polígono 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 7%

---


# Polígono 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/polygon-1-1.png){width="128px"}

<b>Em:</b> Geradores De Textura > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma forma poligonal, com muitas opções de ajuste. Consulte o [Polígono 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/polygon-2/polygon-2.md) para obter uma versão mais simples.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Lados</b> <i>3 - 32</i> | Define a quantidade de lados que o polígono deve ter. |
| <b>Explodir</b> <i>0.0 - 1.0</i> | Move as “fatias” do polígono para longe. |
| <b>Tamanho do Triângulo</b> <i>0.0 - 1.0</i> | Ajusta o tamanho de fatias/triângulos. Qualquer ajuste pode separar a forma, apenas 1,1. está perfeitamente conectado! |
| <b>Escala</b> <i>0.0 - 1.0</i> | Dimensiona toda a forma como uma. |
| <b>Escala automática</b> <i>Falso/Verdadeiro</i> | Ajusta a escala para que o polígono inteiro se ajuste à exibição, com parâmetros padrão. |
| <b>Rotação</b> <i>0.0 - 1.0</i> | Gira toda a forma. |
| <b>Gradiente</b> <i>Falso/Verdadeiro</i> | Gera fatias/triângulos de gradiente em vez de sólidos. Observação: se torna semelhante ao Polígono 2 com essa configuração ativada. |
| <b>Inversão de gradiente</b> <i>Falso/Verdadeiro</i> | Inverte a direção do gradiente se “Gradiente” estiver ativado. |
| <b>Divisão em blocos gráficos</b> <i>1 - 16</i> | Define a quantidade de vezes que o resultado deve ser colocado lado a lado. |
| <b>Expansão não quadrada</b> <i>Falso/Verdadeiro</i> | Permite a compensação de esmagamento e alongamento com proporções não quadradas. |
| <b>Divisão em blocos gráficos não quadrados</b> <i>Falso/Verdadeiro</i> | Quando o Expansão não quadrada estiver ativado, ele irá cobrir a forma sem esmagar. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/polygon-1-ex.gif" />
        </td>
    </tr>
</table>
