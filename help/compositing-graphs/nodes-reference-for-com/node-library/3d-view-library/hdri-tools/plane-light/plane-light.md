---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/plane-light.html"
breadcrumb-title: ''
description: Use o nó Luz de plano para adicionar fontes de luz planar a ambientes HDRI para controle de iluminação direcional.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Plane Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz do plano
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---


# Luz do plano

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-plane-light.png){width="200px"}

## Luz do plano

**Entrada:** *Exibição 3D/Ferramentas HDRI*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma forma plana projetada esfericamente. O plano pode ser colocado e orientado em 3d usando os parâmetros de entrada.

Ela difere da [Luz de forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) mais simples, pois tem opções de posicionamento mais avançadas fora da projeção de Distância da origem mais simples e mais padrões e máscaras podem ser aplicados, semelhante à [Luz de linha](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/line-light/line-light.md).

## Entradas

* **Entrada de Imagem de Plano de Fundo**: *Entrada de Cores*\
  Fundo opcional no qual compor a luz gerada.
* **Entrada de Imagem de Forma**: *Entrada de Cores*\
  Imagem opcional para mapear para a luz da linha. Usado somente quando o Modo de cor da forma está definido como Entrada de imagem.
* **Entrada de imagem de padrão**: *entrada em tons de cinza*\
  Imagem de padrão personalizado, usada quando o parâmetro “Pattern” está definido como “Image Input”.

## Parâmetros

* **Modo De Posição**: *Solo/Teto, Distância da origem, Posições Mundiais*\
  Selecione um dos três modos diferentes de inserção. O solo/teto e a Distância da origem suportam a manipulação na visualização 2D, as posições do mundo só podem ser alteradas por meio de propriedades, mas suportam um posicionamento mais exato.
* **Mostrar Grade Terrestre**: *Falso/Verdadeiro*\
  Função auxiliar para habilitar o desenho de uma grade de aterramento de depuração. Ajuda a estimar a posição das linhas no espaço.
* **Coordenadas de Posição**
  * **Vetor Para Cima**: *Z Para Cima, Y Para Cima*\
    Somente com o modo Posição mundial, determine a orientação do sistema de coordenadas.
  * **Posição UV do plano**:\
    Somente com chão / teto e Distância da origem. Define a posição do plano no espaço UV.
  * **Posição Mundial do Plano**: *-2.0 - 2.0*\
    Somente com o modo Posições Mundiais. Define o espaço mundial da posição do plano. Não há suporte para interação de exibição 2D.
  * **Height Absoluto de Plano**: *0.0 - 1.0*\
    Somente com o modo de posição do solo/teto, define o height absoluto a partir do teto. Use Mostrar grade terrestre para estimar melhor a posição.
  * **Distância da origem**: *0.0 - 1.0*\
    Somente com o Modo de posição de Distância da origem. Define a distância a partir do centro do panorama para ambos os pontos.
* **Modo De Cores Da Forma**: *RGB, Temperatura (Kelvin), Entrada De Imagem*\
  Escolha o método a ser usado para definir a cor da forma. A Entrada de imagem permite o uso do segundo slot de entrada.
* **Cor**: *(valor da cor)*\
  Somente com o Modo de cor da forma definido como RGB. Escolhe a cor da forma.
* **Temperatura**: *800.0 - 20000.0*\
  Somente com o Modo de cor da forma definido como Temperatura. Define o valor de Kelvin para a cor da forma.
* **Modo UV da Imagem da Forma**: *Alongar, Alongar apenas no Meio, Repetir + Espaçamento*\
  Somente com o Modo de cor da forma definido como Entrada de imagem. Define como a imagem é aplicada à forma de linha e determina o comportamento de repetição UV.
* **Espaçamento de repetição da imagem da forma**: *0.0 - 1.0*\
  Somente com o Modo de cor da forma definido como Entrada de imagem e com o Modo UV definido como Repetir + Espaçamento. Define a quantidade de espaçamento quando a imagem se repete ao longo da linha.
* **Gama de Imagem da Forma**: *sRGB, Linear*\
  Somente com o Modo de cor da forma definido como Entrada de imagem. Determine como interpretar a entrada de imagem de forma.
* **Exposição (EV)**: *0.0 - 10.0*\
  Defina o valor de exposição para a forma gerada, de forma ideal para o valor de exposição da imagem de plano de fundo.
* **Escala do Plano**: *0.0 - 1.0*\
  Defina a escala uniforme da forma Plano.
* **Tamanho do Plano**: *0.0 - 1.0*\
  Defina o tamanho não uniforme da forma Plano.
* **Rotação do Plano**: *0.0 - 1.0*\
  Girar plano ao longo de seu eixo central.
* **Padrão**: *Quadrado Suave, Quadrado Nítido, Cone, Hemisfério, Entrada de Imagem*\
  Selecione a forma de padrão a ser usada.
* **Dureza do padrão**: *0.0 - 1.0*\
  Definir dureza/contraste do padrão.
* **Modo UV de Padrão**: *Alongar, Alongar apenas no Meio*\
  Definir como usar a máscara de padrão secundária, aplicada sobre a Imagem da Forma.
* **Habilitar recorte terrestre**: *Falso/Verdadeiro*\
  Habilite se o plano pode ser cortado por um plano terrestre ou ainda é mostrado quando estiver abaixo dele. Use Mostrar grade terrestre para estimar melhor isso.
* **Height terrestre**: *-2.0 - 0.0*\
  Ajuste o height do solo para recorte.
* **Habilitar Entrada em Segundo Plano**: *Falso/Verdadeiro*\
  Alterna o uso da imagem de fundo opcional. Os compostos geraram luz na parte superior do plano de fundo.
* **Cor do plano de fundo**: *(Valor da cor)*\
  Se a Entrada do plano de fundo não for usada, defina um valor de plano de fundo de cor sólida aqui.
* **Gama de Plano de Fundo**: *sRGB, Linear* Se a Entrada de Plano de Fundo for usada, defina como interpretar a entrada de Plano de Fundo.

## Imagens de exemplo

![](../../../../../../assets/plane-light-ex.gif)

</td>
</tr>
</table>
