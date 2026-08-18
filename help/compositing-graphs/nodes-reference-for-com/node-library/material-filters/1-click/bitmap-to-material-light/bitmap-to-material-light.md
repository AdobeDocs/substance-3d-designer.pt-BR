---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/1-click/bitmap-to-material-light.html"
breadcrumb-title: ''
description: Use o nó Bitmap para luz de material para converter rapidamente imagens bitmap em materiais com iluminação otimizada para workflows rápidos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > 1-Click > Bitmap to Material Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bitmap para Luz de Material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---


# Bitmap para Luz de Material

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/b2m-light.png)

## Bitmap para Luz de Material

**Entrada:** *Filtros De Material/1-Clique*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este nó converte uma única entrada Difusa/Basecolor em um material completo. Como a versão simples e “leve” do Bitmap2Material completo do [Allegorithmic, que pode ser comprado separadamente](https://www.allegorithmic.com/products/bitmap2material), ela dá a você um pouco do gosto da versão completa. Pode funcionar bem para casos mais simples.

Embora não haja garantia de resultar em materiais perfeitos e corretos para PBR, essa é uma maneira boa e rápida de começar se você tiver apenas uma única imagem e quiser um material completo.

## Parâmetros

* **Canais**
  * Ativa e desativa os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza.
* **Global**
  * **Equilíbrio de Profundidade**: *-1.0 - 1.0* Define um viés/deslocamento para o Heightmap.
* **Difusa**
  * **Nitidez**: *0.0 - 1.0* Adiciona nitidez ao resultado difuso.
  * **Matiz**: *0.0 - 1.0* Tons se difundem com uma mudança de matiz selecionada pelo usuário.
  * **Saturação**: *0.0 - 1.0* Modifica a saturação do resultado Difuso.
  * **Brilho**: *0.0 - 1.0* Ajusta o brilho do resultado Difuso.
  * **Contraste**: *-1.0 - 1.0*\
    Ajusta o contraste do resultado.
* **Relevo**\
  O grupo de Relevos controla as saídas Normal e de Height.
  * **Formato de saída normal**: *DirectX, OpenGL* alterna entre formatos normais (fica verde).
  * **Inverter Relevo Gerado**: *Falso/Verdadeiro* Inverte a interpretação de height.
  * **Intensidade normal**: *0.0 - 20.0* Define a intensidade do Normalmap gerado.
  * **Equalizador de Relevo**: *0.0 - 1.0* Define saldos de conversão para diferentes escalas de detalhes.
  * **Intensidade de pinça**: *0.0 - 1.0* Torna as transições normais mais nítidas. Adiciona efetivamente um filtro de nitidez antes de converter para o normal, tornando as arestas mais evidentes.
  * **Nitidez normal**: *0.0 - 1.0* Nitidez do Normalmap após a conversão, realça os detalhes.
  * **Suavização Normal**: *0.0 - 1.0* Suaviza O Normalmap após a conversão, oculta detalhes.
* **Specular**
  * **Influência Difusa do Specular**: *0.0 - 1.0* Define a influência difusa no Specular. Afeta também as saídas de Textura reluzente e Aspereza.
  * **Saturação do Specular**: *0.0 - 1.0* Altera a saturação da saída do Specular.
  * **Nitidez do Specular**: *0.0 - 1.0* Agrava a saída do Specular.
  * **Speculares leveis de Entrada**: *0.0 - 1.0* Define níveis de entrada para interpretação de Specular.
  * **Speculares leveis de saída**: *0.0 - 1.0* Modifica os níveis de saída do Specular.
  * **Influência do Specular metálico**: *0.0 - 1.0* Determina a influência da entrada metálica opcional no mapa de Specular.
* **Textura reluzente**
  * **Níveis de Textura Reluzente em**: *0.0 - 1.0* Define níveis de entrada para a interpretação de Textura Reluzente.
  * **Níveis de Textura Reluzente Enviados**: *0.0 - 1.0* Modifica os níveis de saída de Textura Reluzente.
  * **Influência de Textura Reluzente Metálica**: *0.0 - 1.0* Determina a influência da entrada Metálica opcional no mapa de Textura Reluzente.
* **Aspereza**
  * **Níveis De Aspereza Em**: *0.0 - 1.0* Define níveis de entrada para a interpretação de Aspereza.
  * **Níveis de aspereza externos**: *0.0 - 1.0* Modifica os níveis de saída de aspereza.
  * **Influência de aspereza metálica**: *0.0 - 1.0* Determina a influência da entrada metálica opcional no mapa de Textura reluzente.
* **Oclusão de ambiente**
  * **Oclusão Ambiente em Difusa**: *0.0 - 1.0* Mescla o AO gerado com a saída Difusa.
  * **Propagação de Oclusão ambiente**: *0.0 - 1.0* Define até onde o AO gerado se espalha.
  * **Distância da luz de Oclusão ambiente**: *0.0 - 1.0* Define a interpretação de “profundidade” do AO. Tem menos influência quando há uma grande propagação.
  * **Ângulo de luz de Oclusão ambiente**: *0.0 - 1.0* Define o ângulo de projeção ao de iluminação falso. Pode ser usado para compensar qualquer AO direcional que já esteja no Difuso, se definido para um ângulo oposto.
  * **Níveis de Oclusão ambiente**: *0.0 - 1.0* Modifica os níveis de saída do AO.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
