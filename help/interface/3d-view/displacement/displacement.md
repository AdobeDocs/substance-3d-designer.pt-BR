---
helpx_url: ""
breadcrumb-title: ''
description: Use o pop-up Deslocamento para ajustar rapidamente o deslocamento e o mosaico aplicados às malhas em uma cena 3D.
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Visualização 3D - pop-up de Deslocamento
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 2%

---


# pop-up deslocamento

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            <p>O pop-up Deslocamento disponível na barra de ferramentas Visualização 3D oferece controles diretos para o deslocamento e a mosaico de malhas.</p>
            <p>Há três parâmetros:<ul>
                <li>Escala da altura</li>
                <li>Nível da altura</li>
                <li>Tesselação</li></ul>
        </td>
        <td style="width: 60%; margin-left: 32px; border: 0">
            <img src="./displacement.resources/displacement-01.gif" alt="pop-up de deslocamento no Visualização 3D" />
        </td>
    </tr>
</table>

## Escala da altura

A distância máxima de deslocamento para os vértices de malha ao longo de seu normal, em unidades de cena.<br>
Essa é a distância percorrida para um valor de 1,0 no mapa de altura.

Quando um gráfico de Substance é conectado a um material e esse gráfico inclui um [nó de saída](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) com
a <code>heightScale</code> uso, o parâmetro de escala de Height no pop-up será *desabilitado* para esse material
já que está sendo acionado pelo gráfico.

>[!TIP]
> 
>Use o nó [Height para unidades do mundo normal](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/height-normal-world-units/height-to-normal-world-units.md) e faça com que o parâmetro &#39;Height profundidade&#39; corresponda ao valor &#39;Height scale&#39;
>para garantir o sombreamento correto ao usar o deslocamento.

## Nível da altura

O valor de tons de cinza no mapa de altura que é usado como o *ponto médio* do height de deslocamento.
Ou seja, o valor limite usado como elevação 0,0.

Valores abaixo desse limite resultam em vértices deslocados para trás, enquanto valores acima do limite resultam em
vértices deslocados para a frente.

## Tesselação

O mosaico envolve a subdivisão de faces de malha individuais adicionando um vértice em seus segmentos e conectando
todos os vértices para um novo vértice no centro, de modo que 1 face se torne **6**.

O parâmetro define a quantidade de vezes que as faces devem ser subdivididas recursivamente.

O *escopo* do parâmetro de mosaico varia de acordo com o *renderizador* atualmente em uso: ele pode ser aplicado
por malha ou por material.

### Por malha

Ao usar o renderizador [Rasterizador](../3d-renderers/3d-renderers.md#rasterizer) ou o renderizador [GPU Pathtracer](../3d-renderers/3d-renderers.md#gpu-pathtracer), cada objeto de Malha na cena tem um *objeto separado*
valor de subdivisão.

A subdivisão é contextual: é otimizada de tal forma que apenas a superfície com um *valor de height não uniforme* ou
um *mapa de altura não simples* será subdividido, independentemente do valor do parâmetro.

### Por material

Ao usar o renderizador [OpenGL](../3d-renderers/3d-renderers.md#opengl), cada material na cena tem um valor de subdivisão *separado*, que
é aplicado a *todas as faces que usam esse material*.

A subdivisão não é contextual: as superfícies são subdivididas na quantidade especificada de vezes, independentemente de sua corrente
height valor ou textura.

## Visualização do mosaico

Você pode visualizar o resultado do mosaico verificando o **wireframe** da malha.<br>
As etapas para exibir o wireframe de cada renderizador estão descritas abaixo:

### Rasterizador/GPU Pathtracer

Use o <img src="../3d-view.resources/3d-view-18.png" width="22" /> **Configurações do renderizador**
 , em seguida, na área Propriedades, vá para **Configurações de renderização > Modo de diagnóstico** e selecione o **Wireframe
 (espaço global) opção**.

### OpenGL

Use o <img src="../3d-view.resources/3d-view-scene-toolbar-wireframe.png" width="22" /> **Wireframe**
 botão.
