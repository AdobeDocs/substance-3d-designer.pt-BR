---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/fabric-weathering.html"
breadcrumb-title: ''
description: Use o nó Envelhecimento de malha para adicionar efeitos de desgaste e envelhecimento aos materiais de malha com base na geometria e curvatura da malha.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Fabric Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Clima de tecido
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---


# Clima de tecido

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fabric-weathering.png){width="128px"}

## Clima de tecido

**Entrada:** *Geradores Baseados Em Malha**/Clima*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Esse é um efeito de material completo que funciona em vários canais de uma só vez. Adiciona um efeito de desgaste de tecido aleatório, com controle para idade e sujeira.\
Esse efeito não funciona muito bem, a menos que você tenha o AO assado e os World Space Normalmaps conectados, uma vez que requer que eles calculem e gerem tudo adequadamente.

Certifique-se de entender completamente os [Modos de Criação de Link](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) ao trabalhar com materiais completos.

## Parâmetros

### Entradas

* **Oclusão De Ambiente**: *Entrada Em Tons De Cinza*\
  Mapa baked usado para efeitos internos e mascaramento.
* **Espaço Normal Do Mundo**: *Entrada De Cores*
* **Máscara** : *Entrada Em Tons De Cinza*\
  Slot de máscara usado para mascarar os efeitos do nó. Pode ser alternado com o parâmetro “Máscara”.

### Parâmetros

* **Canais**
  * Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza.
* **Avançado**
  * **Formato Normal**: *DirectX, OpenGL*\
    Alterna entre diferentes formatos de Mapas Normais (inverte o canal verde).
  * **Máscara**: *Falso/Verdadeiro*\
    Ativa ou desativa o uso do Mapa de máscaras.
* **Efeito**
  * **Dust**: *0.0 - 1.0* Combina em um efeito de dust mais escuro, com base nas áreas voltadas para cima no World Space Normalmap.
  * **Sujeira**: *0.0 - 1.0* Combina em um efeito de dirt/borrão global, com base principalmente em áreas ocultadas (escuras) no AO.
  * **Desgaste de bordas**: *0.0 - 1.0* Adiciona um efeito de nitidez/intensificação às bordas, com base no Normal do Material.
  * **Usado**: *0.0 - 1.0* Mistura em dirt acumulado muito escuro em vincos, com base em AO. Os valores máximo e mínimo tendem a ser muito extremos. Use-os com cuidado.
  * **Idade**: *0.0 - 1.0* Mistura sobre um padrão global de desgaste de ladrilhos. O controle de limite abaixo controla a influência do AO. Os valores Máximo e Mínimo tendem a ser muito extremos.
  * **Limite de Idade**: *0.0 - 1.0* Define a extensão em que o AO afeta o parâmetro Age.
  * **Aumentos de Idade**: *0.0 - 1.0* Controla a mesclagem de vincos adicionais sutis no efeito Idade.
  * **Escala de Scratches de Bordas Nítidas**: *1.0 - 32.0* Define a escala de pequenos riscos, que removem principalmente o efeito Usado e Idade.
  * **Intensidade de distorção de Scratches de Bordas Nítidas**: *0.0 - 1.0* Define a intensidade da distorção para os pequenos arranhões acima.
  * **Dessaturação de Malha Antiga**: *0.0 - 1.0* Controla a dessaturação do efeito Idade.
  * **Brilho de Tecido Antigo**: *0.0 - 1.0* Controla o brilho do efeito Idade. *Este é um parâmetro muito importante a ser alterado para obter a aparência desejada, mas os resultados podem ser extremos: use com alterações sutis.*
* **Mesclagem**
  * **Intensidade Difusa**: *0.0 - 1.0*\
    Intensidade de mesclagem do Difusa.
  * **Intensidade de cor base**: *0.0 - 1.0*\
    Intensidade de mesclagem da Cor de base.
  * **Intensidade Normal**: *0.0 - 1.0*\
    Intensidade de mesclagem do Normal.
  * **Intensidade de Specular**: *0.0 - 1.0*\
    Intensidade de mistura do Specular.
  * **Intensidade de textura reluzente**: *0.0 - 1.0*\
    Intensidade de mistura da Textura reluzente.
  * **Intensidade de aspereza**: *0.0 - 1.0*\
    Intensidade de mistura da aspereza.
  * **Intensidade de Oclusão do ambiente**: *0.0 - 1.0*\
    Intensidade de mesclagem da Oclusão ambiente.
  * **Intensidade de Height**: *0.0 - 1.0*\
    Intensidade de mistura do Height.

## Imagens de exemplo

![](../../../../../../assets/fabric-ex.gif)

</td>
</tr>
</table>
