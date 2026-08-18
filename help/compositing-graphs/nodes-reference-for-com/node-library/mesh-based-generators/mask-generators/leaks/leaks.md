---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leaks.html"
breadcrumb-title: ''
description: Use o nó Vazamentos para gerar padrões de vazamento com base na geometria de malha para criar manchas de água e efeitos de fluido.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leaks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Vazamentos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 1%

---


# Vazamentos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leaks.png){width="128px"}

## Vazamentos

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esse nó representa listras de vazamento de dirt e sujeira provenientes de bordas nítidas. À medida que as listras são geradas com a Posição assada, elas sempre correm para baixo.

Experimente alterar a máscara de variação: como ela orienta o posicionamento das listras, pode ter uma influência muito maior do que com outros geradores de máscaras.

## Parâmetros

### Entradas

* **Posição**: *Entrada em Tons de Cinza*\
  Mapa de posição assado, usado para direções de riscas. Obrigatório!
* **Curvatura**: *Entrada em tons de cinza*\
  Mapa baked usado para o posicionamento da faixa. Obrigatório!
* **Oclusão De Ambiente**: *Entrada Em Tons De Cinza*\
  Mapa baked usado para efeitos internos e mascaramento. Recomendado, mas você pode usar branco plano.
* **Espaço Mundial Normal**: *Entrada De Cores*\
  Baked World Space Normalmap, usado para a direção da faixa. Obrigatório!
* **Máscara de Variação**: *Entrada em Tons de Cinza*\
  Máscara de variação opcional, ative definindo a substituição como True.
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Nível**: *0.0 - 1.0*\
  Nível total do resultado. Progressivamente revela o efeito, afeta o comprimento também. Deve ser ajustado razoavelmente alto para obter gotas longas.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste do resultado.
* **Variação**: *0.0 - 1.0* Define a quantidade de variação de larga escala usada para mascarar as listras. Definir esse valor como 0 leva a listras totalmente uniformes, portanto, evite isso.
* **Comprimento**: *0.0 - 8.0* Comprimento das gotas de listras. A definição desse valor muito alto em uma escala pequena resultará em etapas visíveis. Brinque também com o Level.
* **Ocultar**: *X, Y, Z, None* Define a direção que o AO deve afetar.
* **Substituir máscara de variação**: *Falso/Verdadeiro* Permite substituir a máscara de variação por um slot de entrada personalizado. Usar máscaras mais esparsas ou mais densas pode ser interessante e é uma boa maneira de controlar os gotejamentos.

## Imagens de exemplo

![](../../../../../../assets/leaks-ex.gif)

</td>
</tr>
</table>
