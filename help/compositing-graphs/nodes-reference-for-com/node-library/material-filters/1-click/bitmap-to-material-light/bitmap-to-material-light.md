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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 11%

---


# Bitmap para Luz de Material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bitmap-to-material-light.resources/bitmap-to-material-light-01.png)

<b>Entrada:</b> Filtros Materiais > 1 clique

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este nó converte uma única entrada Difusa/Basecolor em um material completo. Como a versão simples e “leve” do Bitmap2Material completo do [Allegorithmic, que pode ser comprado separadamente](https://www.allegorithmic.com/products/bitmap2material), ela dá a você um pouco do gosto da versão completa. Pode funcionar bem para casos mais simples.

Embora não haja garantia de resultar em materiais perfeitos e corretos para PBR, essa é uma maneira boa e rápida de começar se você tiver apenas uma única imagem e quiser um material completo.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Canais</b> | Ativa e desativa os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza. |
| <b>Global</b> |  |
| <b>Saldo da Profundidade</b> <i>-1.0 - 1.0</i> | Define uma polarização/deslocamento para o Heightmap. |
| <b>Difusa</b> |  |
| <b>Ajustar nitidez</b> <i>0.0 - 1.0</i> | Adiciona nitidez ao resultado difuso. |
| <b>Matiz</b> <i>0.0 - 1.0</i> | As Tonalidades se difundem com um deslocamento de matiz selecionado pelo usuário. |
| <b>Saturação</b> <i>0.0 - 1.0</i> | Modifica a saturação do resultado da Difusão. |
| <b>Brilho</b> <i>0.0 - 1.0</i> | Ajusta o brilho do resultado da Difusão. |
| <b>Contraste</b> <i>-1.0 - 1.0</i> | Ajusta o contraste do resultado. |
| <b>Relevo</b> | O grupo de Relevos controla as saídas Normal e de Height. |
| <b>Formato Normal De Saída</b> <i>DirectX, OpenGL</i> | Alterna entre os formatos Normais (verde virado). |
| <b>Inverter Relevo Gerado</b> <i>Falso/Verdadeiro</i> | Inverte a interpretação do height. |
| <b>Intensidade Normal</b> <i>0.0 - 20.0</i> | Define a intensidade do Normalmap gerado. |
| <b>Equalizador de Relevo</b> <i>0.0 - 1.0</i> | Define saldos de conversão para diferentes escalas de detalhes. |
| <b>Intensidade de pinça</b> <i>0.0 - 1.0</i> | Torna as transições normais mais nítidas. Adiciona efetivamente um filtro de nitidez antes de converter para o normal, tornando as arestas mais evidentes. |
| <b>Nitidez Normal</b> <i>0.0 - 1.0</i> | Ajusta a nitidez do Normalmap após a conversão, realça os detalhes. |
| <b>Suavização Normal</b> <i>0.0 - 1.0</i> | Suaviza o Normalmap após a conversão, oculta detalhes. |
| <b>Specular</b> |  |
| <b>Influência das Difusões do Specular</b> <i>0.0 - 1.0</i> | Define a influência de difusa no Specular. Afeta também as saídas de Textura reluzente e Aspereza. |
| <b>Saturação do Specular</b> <i>0.0 - 1.0</i> | Altera a saturação da saída do Specular. |
| <b>Nitidez do Specular</b> <i>0.0 - 1.0</i> | Aumenta a nitidez da saída de Specular. |
| <b>Speculares leveis Em</b> <i>0.0 - 1.0</i> | Define níveis de entrada para interpretação de Specular. |
| <b>Speculares leveis de saída</b> <i>0.0 - 1.0</i> | Modifica os níveis de saída do Specular. |
| <b>Influência do Specular metálico</b> <i>0.0 - 1.0</i> | Determina a influência da entrada Metálica opcional no mapa de Specular. |
| <b>Textura reluzente</b> |  |
| <b>Níveis De Brilho Em</b> <i>0.0 - 1.0</i> | Define níveis de entrada para a interpretação de Textura reluzente. |
| <b>Níveis de Textura Brilhante Externos</b> <i>0.0 - 1.0</i> | Modifica os níveis de saída de Textura reluzente. |
| <b>Influência de Textura Reluzente Metálica</b> <i>0.0 - 1.0</i> | Determina a influência da entrada Metálica opcional no mapa de Textura reluzente. |
| <b>Aspereza</b> |  |
| <b>Níveis De Aspereza Em</b> <i>0.0 - 1.0</i> | Define níveis de entrada para a interpretação de aspereza. |
| <b>Níveis De Aspereza Externos</b> <i>0.0 - 1.0</i> | Modifica os níveis de saída de aspereza. |
| <b>Influência de Aspereza metálica</b> <i>0.0 - 1.0</i> | Determina a influência da entrada Metálica opcional no mapa de Textura reluzente. |
| <b>Oclusão de ambiente</b> |  |
| <b>Oclusão de ambiente Em Difusões</b> <i>0.0 - 1.0</i> | Combinar no AO gerado na saída do Difusão. |
| <b>Propagação de Oclusão de ambiente</b> <i>0.0 - 1.0</i> | Define o quanto o AO gerado se espalha. |
| <b>Distância da Luz de Oclusão de ambiente</b> <i>0.0 - 1.0</i> | Define a interpretação de “profundidade” do AO. Tem menos influência quando há uma grande propagação. |
| <b>Ângulo de Luz de Oclusão de ambiente</b> <i>0.0 - 1.0</i> | Define o ângulo de projeção do AO de iluminação falsa. Pode ser usado para compensar qualquer AO direcional que já esteja no Difuso, se definido para um ângulo oposto. |
| <b>Níveis de Oclusão de ambiente</b> <i>0.0 - 1.0</i> | Modifica os níveis de saída do AO. |
