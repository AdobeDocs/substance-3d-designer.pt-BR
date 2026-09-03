---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blend/blending-modes-description.html"
breadcrumb-title: ''
description: Saiba mais sobre os modos de mesclagem disponíveis no Substance 3D Designer para combinar texturas com diferentes efeitos de composição.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blend > Blending modes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Modos de mesclagem
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 2%

---


# Modos de mesclagem

O nó [Mesclagem](../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) oferece os seguintes modos de mesclagem:

## Copiar

O modo de mesclagem de *Cópia* apenas colocará o primeiro plano sobre o plano de fundo.

![Modo de mesclagem: copiar](blending-modes-description.resources/blending-modes-description-01.png "Modo de mesclagem: copiar"){zoomable="yes"}

Para imagens coloridas, o canal alfa é considerado por padrão na opacidade.

Isso pode ser alterado usando o parâmetro &#39;Alpha blending&#39;.

![Modo de mesclagem: Copiar (2)](blending-modes-description.resources/blending-modes-description-02.png "Modo de mesclagem: Copiar (2)"){zoomable="yes"}

## Adicionar (Subexposição linear)

O modo de mesclagem *Adicionar* adicionará o valor de entrada do primeiro plano a cada pixel correspondente no plano de fundo.

![Modo de mesclagem: Adicionar (Subexposição Linear)](blending-modes-description.resources/blending-modes-description-03.png "Modo de mesclagem: Adicionar (Subexposição Linear)"){zoomable="yes"}

## Subtrair

O modo de mesclagem *Subtrair* subtrairá o valor de entrada do primeiro plano de cada pixel correspondente no plano de fundo.

Se o resultado da subtração for inferior a 0, o valor será limitado a 0, resultando em preto puro.

![Modo de mesclagem: Subtrair](blending-modes-description.resources/blending-modes-description-04.png "Modo de mesclagem: Subtrair"){zoomable="yes"}

## Multiplicar

O modo de mesclagem *Multiplicar* multiplicará o valor de entrada do plano de fundo por cada pixel correspondente no primeiro plano.

Como o valor de cada pixel está compreendido entre 0 e 1, o resultado é sempre igual ou menor (mais escuro) em comparação com o original.

![Modo de mesclagem: Multiplicar](blending-modes-description.resources/blending-modes-description-05.png "Modo de mesclagem: Multiplicar"){zoomable="yes"}

## Adicionar/subtrair

O modo de mesclagem *Adicionar Sub* funciona da seguinte maneira:

* Os pixels do primeiro plano com valor superior a 0,5 são adicionados aos respectivos pixels do plano de fundo.
* Os pixels do primeiro plano com valor inferior a 0,5 são subtraídos dos respectivos pixels do plano de fundo.

![Modo de mesclagem: adicionar sub](blending-modes-description.resources/blending-modes-description-06.png "Modo de mesclagem: adicionar sub"){zoomable="yes"}

## Max (Clarear)

O modo de mesclagem *Máx* escolherá o valor mais alto entre o plano de fundo e o primeiro plano.

![Modo de mesclagem: Máx. (Clarear)](blending-modes-description.resources/blending-modes-description-07.png "Modo de mesclagem: Máx. (Clarear)"){zoomable="yes"}

## Min (escurecer)

O modo de mesclagem *Min* escolherá o valor mais baixo entre o plano de fundo e o primeiro plano.

![Modo de mesclagem: Min (Escurecer)](blending-modes-description.resources/blending-modes-description-08.png "Modo de mesclagem: Min (Escurecer)"){zoomable="yes"}

## Alterar

O modo de mesclagem do *Switch* é semelhante ao modo de cópia, com uma diferença *crucial*:

* &#39;Opacidade&#39; definida como 0: o fluxo de nós conectados à entrada &#39;Primeiro Plano&#39; *não será computado*.
* &#39;Opacidade&#39; definida como 1: o fluxo de nós conectados à entrada &#39;Fundo&#39; *não será computado*.

Portanto, esse modo pode ser usado para melhorar o desempenho do seu gráfico.

Os nós [Chave](../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md) e [Chave em tons de cinza](../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md) estão configurados para usar os nós de mesclagem nessas configurações específicas.

![Modo de mesclagem: alternar](blending-modes-description.resources/blending-modes-description-01.png "Modo de mesclagem: alternar"){zoomable="yes"}

## Dividir

O modo de mesclagem *Dividir* dividirá o valor dos pixels de entrada do plano de fundo por cada pixel correspondente no primeiro plano.

![Modo de mesclagem: Dividir](blending-modes-description.resources/blending-modes-description-09.png "Modo de mesclagem: Dividir"){zoomable="yes"}

## Sobrepor

O modo de mesclagem *Sobreposição* combina os modos de mesclagem Multiplicação e Tela:

* 
  * Se o valor do pixel da camada inferior estiver abaixo de 0,5, a mesclagem de tipo *Multiplicar* será aplicada
  * Se o valor do pixel da camada inferior estiver acima de 0,5, uma mesclagem de tipo de *Tela* será aplicada

![Modo de mesclagem: Sobreposição](blending-modes-description.resources/blending-modes-description-10.png "Modo de mesclagem: Sobreposição"){zoomable="yes"}

## Tela

Com o modo de mesclagem Tela, os valores de pixels nas duas entradas são invertidos, multiplicados e, em seguida, invertidos novamente.

O resultado é o efeito oposto ao da multiplicação e é sempre igual ou maior (mais claro) em comparação com o original.

![Modo de mesclagem: Tela](blending-modes-description.resources/blending-modes-description-11.png "Modo de mesclagem: Tela"){zoomable="yes"}

## Luz indireta

O modo de mesclagem Luz Suave cria um resultado sutil mais claro ou mais escuro, dependendo do brilho da cor de primeiro plano.

A mesclagem de cores com mais de 50% de brilho clareia os pixels do plano de fundo, e as cores com menos de 50% de brilho escurecem os pixels do plano de fundo.

![Modo de mesclagem: Luz suave](blending-modes-description.resources/blending-modes-description-12.png "Modo de mesclagem: Luz suave"){zoomable="yes"}
