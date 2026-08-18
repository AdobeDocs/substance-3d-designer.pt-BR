---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/mask-builder.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 0%

---


# Construtor de máscaras

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mask-builder.png){width="128px"}

## Construtor de máscaras

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Essa é basicamente a versão Designer do Construtor de máscaras do Painter.

É uma ferramenta complicada destinada como um criador de máscaras abrangente, com base em mapas baked, parâmetros do usuário e mapas e padrões de desgaste. Destina-se principalmente como um nó de controle completo muito avançado para misturar no dirt de vincos e desgaste de bordas. Este nó é poderoso o suficiente para imitar todos os outros Geradores de máscaras.

Não há necessidade explícita de cozedura, mas quanto mais você fornecer, mais esse nó será capaz de fazer.

## Parâmetros

### Entradas

* **Oclusão De Ambiente**: *Entrada Em Tons De Cinza*
* **Curvatura**: *Entrada em tons de cinza*
* **Espaço Mundial Normal**: *Entrada de Cores*
* **Entrada de Desgaste**: *Entrada em Tons de Cinza*
* **Entrada de Desgaste 2**: *Entrada em Tons de Cinza*
* **Entrada de Dispersão**: *Entrada em Tons de Cinza*\
  Carimbo de dispersão personalizado, necessário para usar os parâmetros de Dispersão.
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.
* **Posição**: *Entrada de cores*\
  Usado para efeitos Triplanar e Superior-Inferior.

### Parâmetros

* **Nível**: *0.0 - 1.0*\
  Define o nível total do efeito, revelando gradualmente.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste do resultado.
* **Inverter**: *Falso/Verdadeiro*\
  Inverte o resultado. Útil para atingir o oposto da máscara que você está criando.
* **Usar Triplanar**: *Falso/Verdadeiro* Habilita a projeção Triplanar, evitando quaisquer emendas com mapas de desgaste.
* **Contraste de Mesclagem Triplanar**: *0.0 - 1.0* Define o contraste para a Mesclagem Triplanar.
* **Desgaste**: *0.0 - 1.0* Define a quantidade de Desgaste a ser mesclada globalmente.
* **Desgaste**
  * **Escala**: *0 - 10* Define a escala do Desgaste global.
  * **Usar Desgaste Personalizado**: *Falso/Verdadeiro* Habilita a entrada de Desgaste personalizado.
  * **Desgaste Personalizado Secundário**: *0.0 - 1.0* Habilita uma segunda entrada de Desgaste personalizado.
  * **Inverter**: *Falso/Verdadeiro*\
    Inverte o mapa de Desgaste.
* **AO**: *-1.0 - 1.0* Define a extensão em que o efeito deve aparecer nas áreas do AO ocultas. Pode ser ajustado com o grupo abaixo.
* **AO**
  * **Intervalo**: *0.0 - 1.0* Define o limite ou intervalo para a aparência do dirt.
  * **Contraste**: *0.0 - 1.0*\
    Ajusta o contraste do efeito AO.
  * **Ruído**: *0.0 - 1.0* Define a quantidade de ruído/desgaste a ser mesclada no efeito AO.
  * **Escala de Ruído**: *0 - 10* Define a escala do ruído/desgaste do AO.
  * **Tipo de Ruído**: *Manchas, Nuvem, Umidade, Ruído Branco* Alterna entre 4 tipos diferentes de ruído do AO.
  * **Inverter**: *Falso/Verdadeiro*\
    Inverte a interpretação do mapa do AO: o ruído aparecerá nas áreas claras do AO, não nas escuras.
* **Curvatura**: *0.0 - 1.0* Define quanto efeito deve aparecer nas bordas da curvatura; pode ser convexo e côncavo. Ajuste isso com o grupo abaixo.
* **Curvatura**
  * **Intervalo convexo**: *-1.0 - 1.0* Define quanto efeito deve aparecer nas bordas de curvatura convexas (brilhantes).
  * **Contraste convexo**: *0.0 - 1.0* Define o contraste do efeito convexo.
  * **Inversão Convexa**: *False/True* Inverte a interpretação das bordas Convexas.
  * **Intervalo côncavo**: *-1.0 - 1.0* Define o efeito a ser exibido nas bordas de curvatura côncavas (escuras).
  * **Contraste côncavo**: *0.0 - 1.0* Define o contraste do Intervalo côncavo.
  * **Inversão côncava**: *Falso/Verdadeiro* Inverte a interpretação das bordas côncavas.
  * **Smoothness**: *0.0 - 16.0* Quantidade de desfoque e suavização a ser aplicada às bordas de Curvatura.
  * **Aumento de Nível**: *0.0 - 1.0* Aumento adicional se o efeito não estiver visível o suficiente.
  * **Ruído**: *0.0 - 1.0* Define a influência do ruído/desgaste no efeito Curvatura.
  * **Escala de ruído**: *0 - 10* Define a escala do ruído.
  * **Tipo de Ruído**: *Manchas, Nuvem, Umidade, Ruído Branco* Escolha entre 4 tipos de Ruído diferentes.
* **Gradiente Superior/Inferior**: *-1.0 - 1.0* Mistura sobre as máscaras ou com um gradiente de cima para baixo com base no mapa de Posição. Valores positivos tornam as coisas mais brilhantes, valores negativos mascaram os efeitos existentes.
* **Gradiente**
  * **Intervalo**: *0.0 - 1.0* Define a posição do gradiente.
  * **Contraste**: *0.0 - 1.0*\
    Ajusta o contraste do gradiente.
  * **Inverter**: *Falso/Verdadeiro*\
    Inverte o gradiente. Alterna efetivamente entre a parte inferior e a superior.
* **Espaço Mundial Normal**: *0.0 - 1.0* Semelhante ao Gradiente Superior/Inferior, mas com o mapa de posição e em seis direções, semelhante à iluminação falsa. Valores positivos clareiam, valores negativos escurecem.
* **Espaço Mundial Normal**
  * **Intensidade Superior**: *-1.0 - 1.0*
  * **Intensidade Inferior**: *-1.0 - 1.0*
  * **Intensidade Frontal**: *-1.0 - 1.0*
  * **Intensidade do plano de fundo**: *-1.0 - 1.0*
  * **Intensidade da direita**: *-1.0 - 1.0*
  * **Intensidade da esquerda**: *-1.0 - 1.0*
* **Scratches**: *-1.0 - 1.0* Mescla os arranhões nas áreas brancas.
* **Scratches**
  * **Valor**: *0 - 4096* Define a quantidade total de riscos.
  * **Escala**: *0.0 - 1.0* Define a escala de arranhões individuais.
* **Dispersão**: *-1.0 - 1.0* Dispersão um carimbo personalizado dentro de áreas brancas.
* **Dispersão**
  * **Escala**: *0 - 50* Escala total do efeito.
  * **Densidade**: *0.0 - 1.0* Controle de densidade de dispersão, número que deve aparecer.
  * **Tamanho**: *0.0 - 4.0* Tamanho do carimbo disperso.
  * **Variação de Tamanho**: *0.0 - 1.0* Variação no tamanho do carimbo.
  * **Variação de opacidade**: *0.0 - 1.0* Variação na opacidade do carimbo.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
