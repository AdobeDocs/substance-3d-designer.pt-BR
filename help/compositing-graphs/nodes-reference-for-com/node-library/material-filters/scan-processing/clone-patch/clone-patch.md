---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/clone-patch.html"
breadcrumb-title: ''
description: Use o nó Patch de clone para clonar e corrigir áreas em materiais digitalizados para remover artefatos e imperfeições.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Patch do clone
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 3%

---


# Patch do clone

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](clone-patch.resources/clone-patch.png){width="128px"}

![](clone-patch.resources/clone-patch-grayscale.png){width="128px"}

<b>Entrada:</b> Filtros Materiais > Processamento de materiais escaneados

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Patch de clone é um nó “Carimbo” paramétrico e processual. Ele clona uma área de uma entrada para outra, ocultando detalhes potencialmente indesejados. Embora não seja tão rápido e fácil quanto usar uma ferramenta familiar em um aplicativo baseado em pincel, ele oferece a principal vantagem de não ser destrutivo e trabalhar em um fluxo de trabalho baseado em nó. Além disso, este nó executa uma análise inteligente da área de destino e de origem e tenta mesclar as coisas da melhor maneira possível com base no contraste, nos valores e nas formas.

Isso é destinado principalmente para aqueles momentos raros onde você deseja fazer uma correção manual de uma área específica, no caso de haver um detalhe indesejado em algum lugar.

Lembre-se de que isso não funciona como um pincel padrão, simples, de “carimbo”. A forma da área mesclada é baseada nas formas e valores das áreas com as quais você está trabalhando, o que significa que este é um nó bastante pesado que requer paciência, mas oferece excelentes resultados.

Também é importante entender o fato de que você pode mover a área de destino com um cursor, mas a área de origem precisa ser definida alterando os parâmetros da “Matriz de origem”.

>[!NOTE]
>
> Se você quiser isso para um material completo (como é o caso com mais frequência), consulte [Correção de clonagem de material](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md).
> 
> Para os casos em que você deseja executar esta operação em várias entradas ao mesmo tempo (sem que seja um material), consulte [Patch de vários clones](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>É Normal (somente para Cor)</b> <i>Falso/Verdadeiro</i> | Define se a entrada é um mapa normal e se a mesclagem deve ser tratada como tal. |
| <b>Forma</b> <i>Quadrado, Disco</i> | Define a forma do carimbo. Usado somente como base. |
| <b>Borda</b> |  |
| <b>Limite</b> <i>0.0 - 1.0</i> | Define o quanto a área mesclada deve chegar. Isso cresce em etapas, ao longo das formas na área de destino e tem muito pouco efeito com fundos uniformes<i>.</i> |
| <b>Desfoque</b> <i>0.0 - 2.0</i> | Desfoca as bordas da área do carimbo caso seja necessária uma transição mais suave. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Arredonda as bordas da forma do carimbo, criando contornos de fluxo mais suaves. |
| <b>Resolução da Grade</b> <i>1 - 11</i> | Define a resolução de qualidade da análise de mesclagem. Um valor mais alto significa uma mesclagem mais precisa. |
| <b>Transformações</b> |  |
| <b>Matriz de Origem</b> <i>(Matriz de Transformação)</i> | Transforma a origem (Dimensionamento e rotação). Não pode ser feito na tela, altere somente através destes parâmetros. |
| <b>Deslocamento de Origem</b> <i>-0.5 - 0.5</i> | Converte o local de origem. Não pode ser feito na tela, altere somente através destes parâmetros. <i>Este parâmetro é provavelmente o principal que você deseja alterar!</i> |
| <b>Matriz de Destino</b> <i>(Matriz de Transformação)</i> | Transforma o local de destino (Dimensionamento e rotação). Também pode ser feito por meio do gizmo na tela. |
| <b>Deslocamento de Destino</b> <i>-0.5 - 0.5</i> | Converte o local de destino. Também pode ser feito por meio do gizmo na tela. |
