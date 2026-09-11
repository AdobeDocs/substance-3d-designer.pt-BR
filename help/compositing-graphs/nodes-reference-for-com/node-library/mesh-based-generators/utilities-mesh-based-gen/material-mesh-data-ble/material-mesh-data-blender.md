---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-mesh-data-blender.html"
breadcrumb-title: ''
description: Use o nó Misturador de dados de malha de material para mesclar dados de malha de material para criar transições suaves entre diferentes zonas de material.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Mesh Data Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Misturador de dados de malha de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 8%

---


# Misturador de dados de malha de material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-mesh-data-blender.resources/material-mesh-data-blender.png){width="128px"}

<b>Entrada:</b> Geradores Baseados Em Malha > Utilitários

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Esse nó tem como objetivo facilitar bastante a adição de detalhes com base em dados feitos bake. Ele vem com vários controles deslizantes para modificar um material de entrada completo, com base em todos e quaisquer mapas baked como entrada. Experimente, pois há muitas opções.

É útil para fazer coisas como adicionar realce de borda com base em curvatura ou outros mapas, mesclar em algum AO com Difusão/Basecolor, adicionar Oclusão de Specular com base em curvatura e/ou AO etc.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada Completa De Material (Grupo “Material”)</b> | Conjunto completo de mapas de materiais.<br><br>Eles são modificados por este nó e retornados novamente como saída. |
| <b>Oclusão de ambiente</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para efeitos internos e mascaramento. |
| <b>Curvatura</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para efeitos internos e mascaramento. |
| <b>Height</b> <i>Entrada em tons de cinza</i> |  |
| <b>Normal</b> <i>Entrada de cores</i> |  |
| <b>Cor do vértice</b> <i>Entrada de cores</i> |  |
| <b>Espaço Mundial Normal</b> <i>Entrada de cores</i> |  |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Canais</b> | Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza. Afeta a disponibilidade dos parâmetros abaixo. |
| <b>Mapas baked</b> | Se os mapas baked listados devem ou não ser usados para cálculos. Afeta a disponibilidade dos parâmetros abaixo. |
| <b>Difusão AO</b> <i>0.0 - 1.0</i> | Quantidade de Oclusão de ambiente para se misturar à Difusão. |
| <b>Bordas cortantes de Difusão</b> <i>0.0 - 1.0</i> | Quantidade do mapa de curvatura para se misturar com a Difusão. |
| <b>Cor Da Difusão Da Cor Do Vértice</b> <i>0.0 - 1.0</i> | Quantidade do faço bake de cores de vértice para mesclar na Difusão. |
| <b>Pré-Iluminação de Difusão</b> <i>0.0 - 1.0</i> | Quantidade de pré-iluminação (falsa), com base nos World Space Normals. |
| <b>Equilíbrio de iluminação do desenho animado de Difusões</b> <i>0.0 - 1.0</i> | Muda entre iluminação realista e caricatura para a Difusão. |
| <b>Desenho Animado de Difusões Pré-Camadas de Iluminação</b> <i>0 - 10</i> | Controla a aparência dos cálculos de iluminação animada. |
| <b>Contornos de Desenho Animado de Difusão</b> <i>0.0 - 1.0</i> | Controla a aparência dos cálculos de iluminação animada. |
| <b>Cor de base AO</b> <i>0.0 - 1.0</i> | Quantidade de Oclusão de ambiente para mesclar na cor de base. |
| <b>Cor de base bordas cortantes</b> <i>0.0 - 1.0</i> | Quantidade do mapa de curvatura para mesclar com a cor de base. |
| <b>Cor de base da Cor do Vértice</b> <i>0.0 - 1.0</i> | Quantidade do faço bake de cores de vértice para mesclar na cor de base. |
| <b>Intensidade normal do material</b> <i>0.0 - 1.0</i> | Intensidade de mesclagem do Normalmap feito bake (tangente). |
| <b>SpecularAO</b> <i>0.0 - 1.0</i> | Intensidade de mistura do AO no Specular. |
| <b>Bordas cortantes brilhantes do Specular</b> <i>0.0 - 1.0</i> | A intensidade de mistura da Curvatura no Specular. |
| <b>Contornos do Desenho Animado de Specular</b> <i>0.0 - 1.0</i> | Força de mistura de um efeito de contorno de borda de Specular de desenho animado, com base na Curvatura. |
| <b>Bordas cortantes escuras e reluzentes</b> <i>0.0 - 1.0</i> | A intensidade de mistura da Curvatura na Textura reluzente. |
| <b>Aspereza de bordas cortantes e brilhantes</b> <i>0.0 - 1.0</i> | A intensidade de mistura da Curvatura na Aspereza. |
| <b>Contornos de Desenho Animado de Aspereza</b> <i>0.0 - 1.0</i> | Força de mistura de um efeito de contorno de borda de aspereza de desenho animado, com base na Curvatura. |
| <b>Bordas cortantes e brilhantes metálicas</b> <i>0.0 - 1.0</i> | A intensidade de mistura da Curvatura no Metálico. |
| <b>Contornos de desenhos animados metálicos</b> <i>0.0 - 1.0</i> | Força de mistura de um efeito de contorno de borda metálico de desenho animado, com base na Curvatura. |
| <b>Intensidade de material do AO</b> <i>0.0 - 1.0</i> | Combinar força do AO mapa baked com AO gerado por material, que grau combinar ambos os mapas de AO em. |
| <b>Intensidade de material do Height</b> <i>0.0 - 1.0</i> | Combinar força do Height de mapa baked com Height gerado por material, que grau combinar ambos os mapas de altura. |
| <b>Tipo de Mesclagem de Material de Height</b> <i>Reforçar, Interpolação</i> | Modo de mesclagem para combinar ambos os mapas de altura. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="material-mesh-data-blender.resources/blenddata-ex.gif" />
        </td>
    </tr>
</table>
