---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/publishing-substance-3d-asset-files-sbsar.html"
breadcrumb-title: ''
description: Saiba como publicar arquivos de ativos do Substance 3D (SBSAR) a partir do Designer para uso em outros aplicativos e mecanismos.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Publishing Substance 3D asset files (SBSAR)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Publicação de arquivos de ativos do Substance 3D (SBSAR)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1238'
ht-degree: 2%

---


# Publicação de arquivos de ativos do Substance 3D (SBSAR)

Esta página explica como a Substance 3D Designer pode publicar pacotes como arquivos de <b>ativos do Substance 3D</b>, um formato de arquivo especial com a extensão <b>SBSAR</b>, usado no ecossistema de Substance bem como em outros aplicativos que dão suporte a ele.

Normalmente, é melhor usar um ativo do Substance 3D em vez de bitmaps, pois ele é muito mais flexível e leve. Se você estiver usando o [Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home), o [Sampler](https://experienceleague.adobe.com/en/docs/substance-3d-sampler/using/home) ou o [Player](https://helpx.adobe.com/substance-3d-player/home.html) do Substance 3D, é mais rápido usar o recurso [&#39;Enviar para...&#39;](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md).

![Publicação de arquivos SBSAR simplificada](publishing-substance-3d-asset-files-sbsar.resources/publishing-substance-3d-asset-files-sbsar-01.png "Publicação de arquivos SBSAR simplificada")

## Publicando conceitos

é bom ter o seguinte em mente ao publicar um gráfico de Substance:

* Você<b> publica um pacote</b>, com todo o seu conteúdo, não um [gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md) individual. Um ativo do Substance 3D permite gerar conteúdo de todos os gráficos de Substance dentro deste pacote.
* Os pacotes publicados são <b>completamente autônomos</b>: todos os recursos necessários estão incorporados ao arquivo. Isso significa que eles são muito mais fáceis de compartilhar do que arquivos SBS.
* A saída dos ativos do Substance 3D pode ser <b>completamente dinâmica</b>. [A resolução não está definida; os parâmetros expostos podem ser modificados.](../../compositing-graphs/compositing-graph-key-con/substance-compositing-graph-key-concepts.md) No entanto, não é mais possível editar o gráfico.
* Os ativos do Substance 3D podem ser usados fora do Designer, em todos os produtos Adobe Substance 3D, no Adobe Dimension e em qualquer outro aplicativo que tenha uma [integração de Substance](https://experienceleague.adobe.com/en/docs/substance-3d/ecosystem/home).
* A publicação é diferente de[Exportar](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md). Certifique-se de entender bem a diferença.

## Preparando para publicar

A publicação requer mais preparação do que a exportação de bitmaps. Isso ocorre porque seus ativos do Substance 3D publicados são ferramentas dinâmicas, não apenas um instantâneo estático do estado atual de suas texturas. Especificamente, lembre-se do seguinte:

* Verifique se as resoluções de gráfico ([Tamanho de Saída](../../compositing-graphs/output-size/output-size.md)) estão definidas para o *método de herança [ Relativo ao pai*](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md), o que significa que elas são dinâmicas e podem ser alteradas sem interrupções.
* Verifique se as [saídas de gráfico](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) estão configuradas corretamente com nomes, rótulos e marcas de uso.
* Verifique se os [Parâmetros, se necessários, estão organizados e nomeados corretamente](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md).
* Se um gráfico descreve um material, defina seu atributo [modelo de material](../graph-parameters/graph-parameters.md) para o modelo desse material.
* Verifique se a propriedade [Tamanho de saída](../../compositing-graphs/output-size/output-size.md) de todos os nós [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) está definida como o método de herança ](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) *[* Absoluto. Se não for esse o caso, o [recurso de bitmap](../../resources/bitmap-resource/bitmap-resource.md) referenciado nele será salvo na resolução padrão <b>256\*256</b> no arquivo de ativo do Substance 3D publicado, o que* afetará a qualidade* de uma ou mais saídas.
* Se os gráficos estiverem presentes no pacote que não deve estar disponível fora do Designer (por exemplo, subgráficos auxiliares ou de “ferramenta” que funcionam apenas em um contexto específico), configure-os para ficarem ocultos em suas propriedades. Veja mais abaixo.

## Métodos de publicação

Quando estiver pronto para publicar, há duas maneiras de acessar a Caixa de Diálogo de Publicação, ambas por meio do [Explorer](../../interface/the-explorer-window/the-explorer-window.md).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

No Explorer, clique com o botão direito do mouse no pacote e escolha ![](publishing-substance-3d-asset-files-sbsar.resources/publishing-substance-3d-asset-files-sbsar-02.png) **arquivo .sbsar do Publish...**, tecla de atalho alternativa Ctrl + P.

Depois de publicar com caixa de diálogo uma vez, você também pode usar o arquivo ![](publishing-substance-3d-asset-files-sbsar.resources/publishing-substance-3d-asset-files-sbsar-03.png) **Publish .sbsar como anterior** para repetir o processo de publicação sem ver as caixas de diálogo, publicando imediatamente com as mesmas configurações.

</td>
<td style="border: 0;" valign="top">

![](publishing-substance-3d-asset-files-sbsar.resources/publishing-substance-3d-asset-files-sbsar-04.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

No Explorer, clicando no botão do Publish ![](publishing-substance-3d-asset-files-sbsar.resources/publishing-substance-3d-asset-files-sbsar-02.png) na barra de ferramentas superior.

Depois de Publicar com caixa de diálogo uma vez, você também pode usar o Publish como botão anterior ![](publishing-substance-3d-asset-files-sbsar.resources/publishing-substance-3d-asset-files-sbsar-03.png) para repetir o processo de publicação sem ver as caixas de diálogo, publicando imediatamente com as mesmas configurações.

</td>
<td style="border: 0;" valign="top">

![](publishing-substance-3d-asset-files-sbsar.resources/publishing-substance-3d-asset-files-sbsar-05.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Opções de publicação de ativos

Antes de as Opções do Publish de ativo serem exibidas, você será solicitado a salvar o arquivo Substance 3D (SBS) se isso não tiver sido feito, e você será solicitado onde salvar o ativo Substance 3D. Para evitar ver as caixas de diálogo e os prompts de arquivo, e obter o arquivo mais rapidamente, use o <b>Publish como métodos anteriores</b> descritos acima.

</td>
<td style="border: 0;" valign="top">

![Opções de publicação de ativos](publishing-substance-3d-asset-files-sbsar.resources/publishing-substance-3d-asset-files-sbsar-06.png "Opções de publicação de ativos")

</td>
</tr>
</table>

As seguintes opções estão disponíveis:

<b>Caminho do arquivo</b> abre uma caixa de diálogo de arquivo para escolher onde salvar o arquivo de ativos do Substance 3D. O caminho padrão são os documentos do usuário do sistema. Se o pacote foi salvo, o caminho é o local do pacote. Se o pacote tiver sido publicado durante a sessão, o caminho será o último local de publicação.

A <b>compactação do arquivo</b> define opções de compactação para o arquivo. Isso afeta o tamanho do arquivo.

<b>Gerar ícones ausentes</b> usa técnicas de [Renderização PBR](../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md) integradas para criar miniaturas para cada atributo do gráfico.

<b>Gráficos expostos </b>lista todos os gráficos que serão expostos neste pacote; veja abaixo os gráficos de exclusão.

>[!NOTE]
>
> **Exposição Aleatória de Sementes**
> 
> As configurações de exposição de propagação aleatória não estão mais disponíveis na caixa de diálogo Publish. Em vez disso, defina o atributo de propagação aleatória do gráfico [como Absoluto em vez de relativo para evitar que ele se torne disponível.](../../compositing-graphs/graph-parameters/graph-parameters.md)

## Excluindo gráficos do ativo publicado

Alguns gráficos do pacote podem não ser destinados ao uso externo. Estes sub-grafos são geralmente entendidos como parte de um todo maior, uma sub-rotina de um material mestre.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Para impedir que um gráfico se torne visível ou utilizável em um arquivo de ativos do Substance 3D, acesse as propriedades desse gráfico (clique duas vezes na área vazia na exibição do gráfico ou clique uma vez no gráfico no Explorer) e abra o lançamento de <b>Atributos</b>. Defina <b>Exposto em SBSAR</b> como <b>Não</b> para ocultá-lo quando publicado.

</td>
<td style="border: 0;" valign="top">

![](publishing-substance-3d-asset-files-sbsar.resources/publishing-substance-3d-asset-files-sbsar-07.png)

</td>
</tr>
</table>

### Avisos da caixa de diálogo Publish

A caixa de diálogo Publish às vezes exibe avisos em amarelo. Os mais comuns estão listados abaixo, com uma explicação e solução.

* Um ou mais gráficos não têm uma saída\
  Este aviso significa que você está tentando publicar um pacote com um ou mais gráficos que não têm nós de saída. A solução é adicionar [nós de saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)aos gráficos com um triângulo amarelo de aviso.
* Um ou mais gráficos têm um parâmetro de tamanho de saída não relativo ao principal\
  Este aviso significa que um ou mais gráficos foram definidos com tamanhos de saída incorretos. Normalmente são as propriedades de um gráfico em si. O aviso indica que você não terá controle dinâmico de resolução sobre este gráfico quando publicado. A solução é acessar as propriedades de gráfico com um triângulo amarelo e definir o [método de herança](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) do Tamanho de Saída como *Relativo ao Pai*.

## Limitações dos ativos do Substance 3D

Embora o ativo do Substance 3D seja o formato mais poderoso e dinâmico do ecossistema de Substance, há algumas pequenas limitações técnicas que você deve conhecer.

* Os pacotes de ativos do Substance 3D publicados são um formato de arquivo unidirecional. Não é possível “descompilar” um ativo do Substance 3D em um arquivo do Substance 3D (SBS). A única maneira de “editar” um ativo do Substance 3D é editar o arquivo original do Substance 3D. Você ainda pode usar o conteúdo do pacote de ativos do Substance 3D como nós dentro de novos gráficos de Substance (abrir e arrastar e soltar), portanto, essa não é uma grande limitação.
* Os arquivos de ativos do Substance 3D têm versões que inferem a compatibilidade. O Substance Engine principal é atualizado periodicamente com novos recursos. os pacotes que usam esses recursos precisam ser lidos por aplicativos que oferecem suporte a esses novos recursos. Isso não é um problema para todos os aplicativos Substance, pois todos são atualizados ao mesmo tempo, mas os plug-ins e as integrações podem ter atrasos de compatibilidade mais longos.\
  Use as opções de exibição de Compatibilidade de Substance Engine nas [Preferências do Projeto](../../interface/preferences-window/project-settings/project-settings.md)para rastrear possíveis problemas.
* Alguns parâmetros expostos, como os parâmetros *estáticos*, são *ocultos* assim que um gráfico é publicado como parte de um ativo do Substance 3D. Consulte a seção [Limitações](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) da página [Expondo um parâmetro](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) para obter uma lista desses parâmetros e saber mais sobre parâmetros estáticos em geral.
