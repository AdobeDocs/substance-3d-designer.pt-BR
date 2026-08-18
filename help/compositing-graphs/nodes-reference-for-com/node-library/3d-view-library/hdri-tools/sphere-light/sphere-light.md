---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/sphere-light.html"
breadcrumb-title: ''
description: Use o nó Luz da esfera para adicionar fontes de luz esféricas a ambientes HDRI para um controle de iluminação aprimorado.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Sphere Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz da esfera
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# Luz da esfera

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-sphere-light.png){width="200px"}

## Luz da esfera

**Entrada:** *Exibição 3D/Ferramentas HDRI*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma forma de esfera projetada esfericamente. A transformação da esfera é impulsionada por um gizmo de transformação.

A luz da esfera é bastante versátil e tem opções que lhe permitem não só gerar luzes redondas simples, mas também planetas ou outros corpos celestes. Se você não precisa de opções mais avançadas de iluminação e rotação, dê uma olhada na [Luz de Forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md).

## Entradas

* **Entrada de imagem de fundo**: *Entrada de cor* Plano de fundo opcional no qual compor a luz gerada.
* **Entrada de imagem da forma**: *Entrada de cores* Imagem opcional para mapear para a luz da esfera. Usado somente quando o Modo de cor da forma está definido como Entrada de imagem.

### Parâmetros

* **Modo De Posição**: *Distância da origem, Posição Mundial*\
  Escolha entre dois modos de posicionamento. A distância da origem é semelhante às coordenadas polares, a esfera é definida em relação ao centro do panorama, a posição do mundo funciona como coordenadas 3D padrão.
* **Coordenadas de Posição**
  * **Vetor Para Cima**: *Z Para Cima, Y Para Cima*\
    Somente com o modo Posição mundial, determine a orientação do sistema de coordenadas.
  * **Posição Mundial da Esfera**: *-2.0 - 2.0*\
    Somente com o modo Posição mundial define a posição da esfera no espaço global.
  * **Posição**:\
    Somente com o modo de Distância da origem. Define a posição em relação ao centro. Pode ser manipulado na Visualização 2D.
  * **Distância da origem**: *0.0 - 20.0* Somente com o modo de Distância da origem. Define a distância para a origem, afeta o tamanho visível da esfera.
* **Modo De Cores Da Forma**: *RGB, Temperatura (Kelvin), Entrada De Imagem*\
  Escolha o método a ser usado para definir a cor da forma. A Entrada de imagem permite o uso do segundo slot de entrada.
* **Cor**: *(valor da cor)*\
  Somente com o Modo de cor da forma definido como RGB. Escolhe a cor da forma.
* **Temperatura da forma**: *800.0 - 20000.0*\
  Somente com o Modo de cor da forma definido como Temperatura. Define o valor de Kelvin para a cor da forma.
* **Gama de Entrada de Imagem da Esfera**: *sRGB, Linear*\
  Somente com o Modo de cor da forma definido como Entrada de imagem. Determine como interpretar a entrada de imagem de forma.
* **Rotação de Esfera**: *0.0 - 1.0*\
  Somente com o Modo de cor da forma definido como Entrada de imagem. Gira a esfera ao redor de seu centro para orientar a imagem mapeada.
* **Exposição (EV)**: *0.0 - 10.0*\
  Defina o valor de exposição para a forma gerada, de forma ideal para o valor de exposição da imagem de plano de fundo.
* **Raio da esfera**: *0.0 - 1.0*\
  Define o raio/tamanho da esfera.
* **Dureza da esfera**: *0.0 - 1.0*\
  Define a dureza/declínio da esfera.
* **Sombreamento**: *Nenhum, Escurecimento De Membro, Luz De Sombreamento*\
  Defina se algum sombreamento deve ser aplicado à esfera. Permite que a esfera não apareça como um objeto sólido e sem iluminação. Escurecimento do membro significa um leve escurecimento que aparece nas bordas. Luz do Sombreamento significa que a esfera é iluminada por uma Luz do Sombreamento opcional.
* **Posição Mundial de Luz do Sombreamento**: *-1.0 - 1.0*\
  Se o Sombreamento estiver definido como Luz do Sombreamento, a posição da luz na esfera é controlada aqui.
* **Transparência Penombra**: *0.0 - 1.0*\
  Se Sombreamento estiver definido como Luz do Sombreamento, controla a queda do sombreamento.
* **Habilitar Entrada em Segundo Plano**: *Falso/Verdadeiro*\
  Alterna o uso da imagem de fundo opcional. Os compostos geraram luz na parte superior do plano de fundo.
* **Cor do plano de fundo**: *(Valor da cor)*\
  Se a Entrada do plano de fundo não for usada, defina um valor de plano de fundo de cor sólida aqui.
* **Gama de Plano de Fundo**: *sRGB, Linear* Se a Entrada de Plano de Fundo for usada, defina como interpretar a entrada de Plano de Fundo.

## Imagens de exemplo

![](../../../../../../assets/sphere-light-ex.gif)

![](../../../../../../assets/spherelight-ex1.png)

</td>
</tr>
</table>
