---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/working-with-3d-scenes/exporting-scenes.html"
breadcrumb-title: ''
description: Exporte cenas 3D com todas as edições feitas no Designer usando a ação Exportar cena no menu Visualização de cena 3D.
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Exporting scenes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Exportação de cenas
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---


# Exportação de cenas

Quando precisar exportar a cena com todas as edições feitas no Designer, use as ações “Exportar cena...” no menu “Cena” da [Exibição 3D](../../interface/3d-view/3d-view.md).

Para exportações em formatos USD, o conteúdo da cena corresponderá à árvore exibida no [Navegador de cena](../../interface/3d-view/scene-browser/scene-browser.md).

Para outros formatos, o conteúdo da cena e sua estrutura interna dependerão dos recursos compatíveis com o formato de arquivo selecionado.

>[!NOTE]
>
> Todos os itens adicionados à cena pelo Designer serão incluídos na cena exportada: a câmera padrão, o ambiente padrão, todos os materiais copiam quaisquer luzes adicionais.

![Ações de exportação de cena](../../assets/exportActions.png "Ações de exportação de cena"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Exportar cena

</td>
<td style="border: 0;" valign="top">

### Exportar cena como camadas

</td>
<td style="border: 0;" valign="top">

### Texturas

</td>
</tr>
</table>

## Exportar cena

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

A ação “Exportar cena...” no menu “Cena” exporta cenas 3D editadas de forma destrutiva: a cena é *achatada* e qualquer referência ao original é perdida.

Isso significa que as edições na cena original não afetam a cena exportada.

</td>
<td style="border: 0;" valign="top">

![Arquivos de cena exportados - Achatados](../../assets/exportFlattened.png "Arquivos de cena exportados - Achatados"){zoomable="yes"}

</td>
</tr>
</table>

## Exportar cena como camadas

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

A ação “Exportar cena como camadas...” exporta para os formatos <b>USD</b> (.usd, .usda, .usdc, .usdz) e é *não destrutiva*: o arquivo principal exportado comanda uma *cadeia de referências* onde todos os aspectos editados da nova cena são armazenados em arquivos USD separados.

Isso significa que as edições na cena original são transportadas para a cena exportada.

</td>
<td style="border: 0;" valign="top">

![Arquivos de cena exportados - Em camadas](../../assets/exportLayered.png "Arquivos de cena exportados - Em camadas"){zoomable="yes"}

</td>
</tr>
</table>

Os arquivos exportados seguem esta estrutura:

* <b>Arquivo principal</b>
  * <b>.layers</b>: Referencia as subcamadas abaixo e declara as substituições de material, que ligam a geometria às cópias de material criadas pelo Designer.
    * <b>.assembly</b>: referencia o arquivo .scene# e declara as substituições de geometria, que trazem os dados recalculados pelo Designer da geometria afetada pelos materiais substituídos.
      * <b>.scene#</b>: Referencia a cena original.
    * <b>.câmera</b>: declara a câmera adicionada pelo Designer à cena.
    * <b>.light</b>: declara as luzes adicionadas pelo Designer à cena.
    * <b>.material</b>: declara as cópias de materiais adicionadas pelo Designer à cena, que usam as texturas exportadas.

## Texturas

As texturas são exportadas em um diretório ao lado do arquivo exportado e nomeado com base nele, com um sufixo ‘<b>\_texturas</b>’.

Eles usam o formato <b>PNG</b>, exceto texturas HDR (ponto flutuante) que usam o formato <b>EXR</b>.
