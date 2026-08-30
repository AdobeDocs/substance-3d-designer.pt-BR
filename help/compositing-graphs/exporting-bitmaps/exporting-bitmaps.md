---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/exporting-bitmaps.html"
breadcrumb-title: ''
description: Saiba mais sobre como exportar texturas e bitmaps do gráfico de composição de Substance para uso em aplicativos e fluxos de trabalho externos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exporting Bitmaps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Exportação de bitmaps
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 2%

---


# Exportação de bitmaps

Esta página explica como o Substance 3D Designer pode exportar para muitos formatos de arquivo Bitmap diferentes e como exportar vários blocos UV em lotes.Se você deseja [exportar para arquivos de PSD](../exporting-psd-files/exporting-psd-files.md), há uma página dedicada separada para isso.

![Exportando simplificado](exporting-bitmaps.resources/exportflow.png "Exportando simplificado")

## Exportação de conceitos

É bom ter em mente o seguinte ao exportar um bitmap:

* Você <b> exporta de um Graph</b>, não de um Pacote. Um pacote não gera conteúdo de imagem por si só.
* O número (e a resolução) de bitmaps exportados é determinado pelas <b>Saídas</b> de um Gráfico.
* O tipo de arquivo é definido para todas as saídas/bitmaps.
* Exportar é diferente de [publicar](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md). Certifique-se de entender bem a diferença!

## Métodos de exportação

Quando estiver pronto para exportar, há duas maneiras de acessar a caixa de diálogo Exportar:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Na janela do [Explorer](../../interface/the-explorer-window/the-explorer-window.md), clique com o botão direito do mouse no gráfico para exportar e escolha **”Exportar saídas como bitmaps”**

![](exporting-bitmaps.resources/export-explorer.gif)

</td>
<td style="border: 0;" valign="top">

Na [Exibição de Gráfico](../../interface/the-graph-view/the-graph-view.md), clicando no botão Ferramentas ![](exporting-bitmaps.resources/image2019-9-17-14-44-17.png) e escolhendo **”Exportar Saídas...”**

![](exporting-bitmaps.resources/export-graph.gif)

</td>
</tr>
</table>

## Caixa de diálogo Exportar

A caixa de diálogo Exportar oferece algumas opções para personalizar a exportação.

A versão mostrada à direita é a caixa de diálogo padrão. Alterar a resolução acontece no gráfico, em saídas ou ao definir a resolução principal antes de abrir a caixa de diálogo.

1. <b>Destino: </b>local para todos os arquivos a serem salvos.
1. <b>Formato:</b> tipo de arquivo usado para todos os arquivos exportados.
1. <b>Padrão</b>: método genérico para gerar tipos de arquivo com base em palavras-chave de metadados. Um nome de arquivo de exemplo baseado na primeira saída é mostrado abaixo para verificação.\
   Todas as opções disponíveis estão listadas abaixo:
   1. *$(gráfico)* - nome do gráfico atual
   1. *$(identificador)* - identificador da saída atual
   1. *$(descrição)* - descrição da saída atual
   1. *$(label)* - rótulo da saída atual
   1. *$(user\_data)* - dados de usuário personalizados da saída atual
   1. *$(grupo)* - grupo de saída da saída atual
   1. *$(colorspace)* - espaço de cores da saída atual (disponível somente para os modos *OCIO* e *Adobe ACE* [gerenciamento de cores](../../color-management/color-management.md))
1. <b>Saídas:</b> ative ou desative Saídas e Grupos de Saída específicos do seu Gráfico. Os botões ativam ou desativam tudo. Útil quando apenas um bitmap foi alterado.
1. <b>Exportação automática:</b> botão de alternância para habilitar a reexportação automática de saídas de gráfico assim que uma alteração for feita. Somente para o gráfico atual. Pode ser pesado e lento, dependendo das configurações.
1. <b>Botão Exportar:</b> exporta com as configurações atuais ou fecha a caixa de diálogo.

![Caixa de diálogo Exportar saídas](exporting-bitmaps.resources/fromgraph-1.png "Caixa de diálogo Exportar saídas")

## Caixa de diálogo Exportar (blocos em lote/UV)

Ao trabalhar com malhas UV-Tile no Designer, a caixa de diálogo Exportar pode ser usada de uma maneira ligeiramente diferente que permite a exportação em lote de vários UV-Tiles de uma só vez. Certifique-se de que você entende este fluxo de trabalho e atribuiu corretamente um [Substance gráfico](../../compositing-graphs/substance-compositing-graphs.md) a um ou mais UV-Tiles.\
A guia Lote também é uma maneira mais rápida de exportar o gráfico com uma resolução diferente da resolução de trabalho (principal).

Inicie a caixa de diálogo com os mesmos métodos detalhados acima, apenas verificando se você clicou com o botão direito do mouse *no gráfico atribuído por UV-Tile no Explorer* ou se você *abriu o gráfico atribuído por UV-Tile específico* na visualização Gráfico ao usar o botão Ferramentas.

1. <b>Guia Lote</b>: certifique-se de selecionar esta guia em vez do método padrão <b>Do gráfico </b>, caso contrário, as opções 2 a 3 não estarão disponíveis.
1. <b>Blocos UV:</b> Assim como com as Saídas, permite ativar ou desativar a exportação de Blocos UV específicos.
1. <b>[Tamanho da saída](../../compositing-graphs/output-size/output-size.md): </b>substitua a resolução de exportação, permitindo que você trabalhe menor e mais eficiente ao exportar no tamanho máximo.

![Caixa de diálogo de saídas de exportação em lote](exporting-bitmaps.resources/batch.png "Caixa de diálogo de saídas de exportação em lote")
