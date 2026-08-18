---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/line-light.html"
breadcrumb-title: ''
description: Use o nó Luz de linha para criar fontes de luz linear em ambientes HDRI para simular iluminação fluorescente e de faixa.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Line Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz de linha
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---


# Luz de linha

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-line-light.png){width="200px"}

## Luz de linha

**Entrada:** *Exibição 3D/Ferramentas HDRI*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma forma de linha projetada esfericamente com base nas coordenadas de dois pontos no espaço. Em comparação à [Luz de forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md), ela tem mais opções para orientar formas e aplicar padrões repetidos à forma de luz.

Os modos de posicionamento para este nó são ligeiramente mais complexos do que outros nós de luz HDRI. É recomendável experimentar alguns modos de tamanho diferentes para descobrir qual funciona para o seu cenário.

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
  * **Posição UV de ponto 1**:\
    Somente com chão / teto e Distância da origem. Define a posição do primeiro ponto no espaço UV.
  * **Posição UV de ponto 2**:\
    Somente com chão / teto e Distância da origem. Define a segunda posição de ponto no espaço UV.
  * **Posição Mundial do Ponto 1**: *-2.0 - 2.0*\
    Somente com o modo Posições Mundiais. Define o primeiro ponto no espaço global. Não há suporte para interação de exibição 2D.
  * **Posição Mundial do Point 2**: *-2.0 - 2.0*\
    Somente com o modo Posições Mundiais. Define o segundo ponto no espaço global. Não há suporte para interação de exibição 2D.
  * **Height Absoluto de Linha**: *0.0 - 1.0*\
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
* **Rotação de Linha**: *0.0 - 1.0*\
  Gira a linha ao longo do eixo de seu comprimento. A linha é tratada como uma placa plana ao girar.
* **Thickness de Linha**: *0.0 - 1.0*\
  Define o thickness da placa de linha.
* **Padrão**: *Quadrado Suave, Quadrado Nítido, Cone, Hemisfério, Entrada de Imagem*\
  Selecione a forma de padrão a ser usada.
* **Dureza do padrão**: *0.0 - 1.0*\
  Definir dureza/contraste do padrão.
* **Modo UV de Padrão**: *Alongar, Alongar apenas no Meio, Repetir + Espaçamento*\
  Definir como usar a máscara de padrão secundária, aplicada sobre a Imagem da Forma.
* **Espaçamento de Repetição de Padrão**: *0.0 - 1.0*\
  Somente se o Modo UV de padrão estiver definido como Repetição + Espaçamento. Defina a quantidade de espaçamento entre os padrões repetidos.
* **Habilitar recorte terrestre**: *Falso/Verdadeiro*\
  Habilitar corte de desenho de linha. O efeito não é visível ao usar o modo de posicionamento Terra/Teto.
* **Height terrestre**: *-2.0 - 0.0*\
  Define o height relativo do plano frontal, usado para recorte. Afeta a grade do solo desenhada.
* **Habilitar Entrada em Segundo Plano**: *Falso/Verdadeiro*\
  Alterna o uso da imagem de fundo opcional. Os compostos geraram luz na parte superior do plano de fundo.
* **Cor do plano de fundo**: *(Valor da cor)*\
  Se a Entrada do plano de fundo não for usada, defina um valor de plano de fundo de cor sólida aqui.
* **Gama de Plano de Fundo**: *sRGB, Linear* Se a Entrada de Plano de Fundo for usada, defina como interpretar a entrada de Plano de Fundo.

## Imagens de exemplo

![](../../../../../../assets/line-light-ex.gif)

</td>
</tr>
</table>
