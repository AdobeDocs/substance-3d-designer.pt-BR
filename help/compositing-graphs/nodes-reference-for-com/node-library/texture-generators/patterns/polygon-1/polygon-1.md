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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 1%

---


# Polígono 1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/polygon-1-1.png){width="128px"}

## Polígono 1

**Entrada:** *Geradores De Textura**/Padrões*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma forma poligonal, com muitas opções de ajuste. Consulte o [Polígono 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/polygon-2/polygon-2.md) para obter uma versão mais simples.

## Parâmetros

* **Lados**: *3 - 32* Define a quantidade de lados que o polígono deve ter.
* **Explodir**: *0.0 - 1.0* Move as “fatias” do polígono para longe.
* **Tamanho do Triângulo**: *0.0 - 1.0* Ajusta o tamanho de fatias/triângulos. Qualquer ajuste pode separar a forma, apenas 1,1. está perfeitamente conectado!
* **Escala**: *0.0 - 1.0* Dimensiona toda a forma como uma só.
* **Escala automática**: *Falso/Verdadeiro* Ajusta a escala para que todo o polígono se ajuste à exibição, com parâmetros padrão.
* **Rotação**: *0.0 - 1.0* Gira toda a forma.
* **Gradiente**: *Falso/Verdadeiro* Gera fatias/triângulos de gradiente em vez de sólidos. Observação: se torna semelhante ao Polígono 2 com essa configuração ativada.
* **Inversão de gradiente**: *Falso/Verdadeiro* Inverte a direção do gradiente se “Gradiente” estiver habilitado.
* **Divisão em blocos gráficos**: *1 - 16*\
  Define a quantidade de vezes que o resultado deve ser colocado lado a lado.
* **Expansão não quadrada**: *Falso/Verdadeiro*\
  Permite a compensação de esmagamento e alongamento com proporções não quadradas.
* **Divisão em blocos gráficos não quadrados**&#x200B;**:** *Falso/Verdadeiro*Quando o Expansão não quadrada estiver habilitado, ele irá cobrir a forma sem esmagamento.

## Imagens de exemplo

![](../../../../../../assets/polygon-1-ex.gif)

</td>
</tr>
</table>
