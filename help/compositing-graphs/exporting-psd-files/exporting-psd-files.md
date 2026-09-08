---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/exporting-psd-files.html"
breadcrumb-title: ''
description: Saiba como exportar gráficos de composição de Substance como arquivos de PSD para uso no Adobe Photoshop e em outros fluxos de trabalho de edição de imagens.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exporting PSD files
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Exportação de arquivos PSD
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 1%

---


# Exportação de arquivos PSD

O Substance 3D Designer permite exportar texturas para o Documento ou arquivo PSD do Adobe Photoshop.Esta página explica a interface especial usada para converter os nós de um gráfico em camadas.**Este processo não é automático: você tem muito controle, mas é limitado e geralmente não é possível obter uma correspondência precisa entre nós e camadas.** Além disso, não há garantia de que seu PSD contém as mesmas saídas que seu gráfico, a menos que você o configure explicitamente para fazê-lo. Geralmente, quanto mais preciso e correto você quiser ser, mais esforço será necessário para o usuário. Em geral, a única coisa que pode ser replicada de forma não destrutiva é a [mesclagem de nós](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md). As Camadas de ajuste não são compatíveis, os Estilos de camada ou qualquer outra coisa além dos modos de mesclagem de camada também não são.

[O Substance 3D Designer também pode exportar para arquivos bitmap.](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)

## caixa de diálogo de exportação de PSD

A caixa de diálogo Exportar PSD só pode ser aberta por um método. Na [exibição de gráfico](../../interface/the-graph-view/the-graph-view.md) do gráfico que você deseja exportar para o PSD, clique no botão ![](../../assets/image2019-9-17-14-44-17.png) <b>Ferramentas</b> e selecione <b>Exportar PSD</b>. A interface torna-se visível na <b>Exibição de gráfico</b>.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![interface de usuário do PSD Exporter](../../assets/psd-dialog.png "interface de usuário do PSD Exporter")

</td>
<td style="border: 0;" valign="top">

1. <b>Nome do arquivo e Local:</b> configure a pasta e o nome do arquivo para exportação aqui. Pressione o botão Exportar para executar o processo de exportação.
1. <b>Adicionar Grupo:</b> Adiciona um grupo de camadas
1. <b>Menu suspenso Adicionar Camada:</b> escolha um dos dois métodos para adicionar uma camada. As camadas também podem ser adicionadas *arrastando nós com o botão direito do mouse* para a pilha.
1. <b>Menu suspenso Remover Camada:</b> remova as camadas selecionadas ou todas.
1. <b>Pilha de camadas:</b> a maioria dos trabalhos de instalação se executados aqui. A interface espelha opções limitadas no Photoshop. Configure o nome da camada, o modo de mesclagem e a opacidade aqui. Se uma camada tiver duas miniaturas, a segunda representa o canal do Alpha.

</td>
</tr>
</table>

## Fluxo de trabalho (WRK)

Como o Photoshop não suporta diretamente materiais de várias saídas, há várias maneiras de configurar seu PSD. Veja a seguir um resumo do método mais comum.

* Configure várias pastas para todas as saídas. Uma pasta para Basecolor, uma para Normal, uma para Aspereza, etc.
* Arraste e solte as saídas com o botão direito do mouse no grupo apropriado. Se você quiser manter as coisas simples, o PSD pode ser deixado apenas isso.
* Para expandir mais o PSD: trabalhe de volta à esquerda do gráfico, soltando as etapas relevantes no meio do gráfico no grupo apropriado. Não será possível compartilhar camadas entre saídas/grupos.

No caso raro em que seu PSD é a saída mais importante, você pode construir seu gráfico de modo que você só faça uso de modos de mesclagem. Nesse caso, deve ser possível recriar uma versão mais editável do gráfico como um documento em camadas.
