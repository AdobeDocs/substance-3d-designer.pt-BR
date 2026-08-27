---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/interface/the-explorer-window/send-to-interoperability.html"
breadcrumb-title: ''
description: Use o recurso Enviar para interoperabilidade no Substance 3D Designer para exportar materiais para outros aplicativos.
helpx_creative_field: ""
helpx_description: Designer > Interface > The Explorer window > Send to...  Interoperability
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Enviar para...  Interoperabilidade
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 1%

---


# Enviar para...  Interoperabilidade

![Enviar do Designer para aplicativos da Substance 3D](../../../assets/explorer-interop.png "Enviar do Designer para aplicativos da Substance 3D"){width="512px"}

O Adobe Substance 3D Designer tem interoperabilidade com o [Substance 3D Sampler](https://www.adobe.com/br/products/substance3d-sampler.html), o [Substance 3D Painter](https://www.adobe.com/br/products/substance3d-painter.html) e o [Substance 3D Stager](https://www.adobe.com/br/products/substance3d-stager.html). Isso permite *enviar* e *reenviar* seu trabalho rapidamente, facilitando a iteração no ecossistema do Substance 3D.

O fluxo de trabalho geralmente é o seguinte:

1. Definir o atributo <b>Type</b> nas propriedades de um gráfico [Substance](../../../compositing-graphs/graph-parameters/graph-parameters.md)
1. No painel [Explorer](../the-explorer-window.md), selecione o pacote que deseja enviar
1. Na lista suspensa <b>Publish/Send</b> do Explorer, selecione o aplicativo de destino
1. Fazer alterações no(s) gráfico(s)
1. Repita a etapa 3 para reenviar o pacote e atualizar o ativo enviado existente com suas alterações

>[!WARNING]
>
> Os recursos de interoperabilidade *não* estão disponíveis na versão <b>Vapor</b>.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Definir o tipo de gráfico

Os gráficos de Substance podem ter muitas funcionalidades. Você terá que definir com antecedência qual é a funcionalidade exata de um gráfico, para ter certeza de que ele pode ser enviado corretamente.

Na seção <b>Atributos </b>de propriedades de um gráfico [Substance](../../../compositing-graphs/graph-parameters/graph-parameters.md), há uma opção <b>Tipo</b>, com um menu suspenso que tem as seguintes opções:

</td>
<td style="border: 0;" valign="top">

Atributo Type do gráfico ![Substance](../../../assets/type-attribute.jpg "atributo Type do gráfico Substance")

</td>
</tr>
</table>

* **Não especificado** é o tipo padrão se você não o definiu. Dependendo do aplicativo para o qual você envia, ele pode ser interpretado de forma diferente. O [Substance 3D Painter](https://www.adobe.com/br/products/substance3d-painter.html) assumirá como padrão o Material, por exemplo;
* O **Material Padrão** é para materiais PBR multicanal, com [saídas](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) adequadamente rotuladas;
* O **Material de Decalque** é para um material PBR multicanal com canal alfa, a ser aplicado como Decalque no [Substance 3D Painter](https://www.adobe.com/br/products/substance3d-painter.html) ou no [Substance 3D Sampler](https://www.adobe.com/br/products/substance3d-sampler.html);
* O **Material de Atlas** é para um material PBR multicanal que consiste em várias imagens de atlas, para uso com o [nó de Atlas scatter](../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-scatter/atlas-scatter.md) no Designer ou no [Substance 3D Sampler](https://www.adobe.com/br/products/substance3d-sampler.html);
* O **filtro** é para filtros de uso geral, ambos usados no [Substance 3D Painter](https://www.adobe.com/br/products/substance3d-painter.html) ou no [Substance 3D Sampler](https://www.adobe.com/br/products/substance3d-sampler.html);
* O **Gerador Baseado em Malha** é para geradores de máscara de várias entradas. Isto é usado somente pelo [Substance 3D Painter](https://www.adobe.com/br/products/substance3d-painter.html);
* O **Gerador de Textura** é para mapas de canal único, como procedimentos 2D e ruídos;
* A **Luz ambiente** é para um Ambiente de iluminação de canal único, usado para iluminar cenas e objetos;
* A **Textura clara** é para uma textura de canal único aplicada a uma Luz física.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Menu &#39;Enviar para&#39;

O processo de envio envolveu a [publicação](../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) de um ou mais pacotes em arquivos de ativos da Substance 3D (SBSAR) em segundo plano.

O envio de conteúdo pode ser executado das seguintes maneiras:

* Clique com o botão direito do mouse em um pacote e abra o submenu <b>Enviar para...</b> no menu contextual. Em seguida, escolha a opção <b>Enviar para...</b> para o aplicativo de destino;
* Clique no botão ![](../../../assets/sendto-icon.jpg) <b>Publish/Send</b> na parte superior do painel do Explorer e escolha a opção <b>Enviar para...</b> para o aplicativo de destino.

</td>
<td style="border: 0;" valign="top">

![Menu Publish/Enviar para no Explorer](../../../assets/explorer-sendto-displayed.jpg "Menu Publish/Enviar para no Explorer")

</td>
</tr>
</table>

### Reenviando

Ao enviar novamente um pacote que *já foi enviado uma vez* para o aplicativo *mesmo destino*, o ativo será *atualizado* no aplicativo de destino com a nova versão.

## Enviar para Player

O [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html) tem suporte para *ambos* os <b>arquivos Substance 3D</b> (SBS) e os <b>ativos Substance 3D</b> (SBSAR).

O envio ao Player requer que o executável do Substance Player seja *localizado manualmente* pelo usuário, o que pode ser feito:

* Quando avisado se o Player *nunca foi localizado* desde que o Designer foi instalado;
* A qualquer momento no menu <b>Ferramentas</b>, usando a opção <b>Substance Player > Localizar...</b>.

No Player, receber do Designer requer que o *diretório de instalação* do Substance 3D Designer seja localizado manualmente pelo usuário, o que pode ser feito:

* Quando avisado se o Designer *nunca foi localizado* desde que o Player foi instalado;
* A qualquer momento no menu <b>Opções</b>, usando a opção <b>Localizar Adobe Substance 3D Designer</b>.

>[!NOTE]
>
> Ao enviar arquivos do Substance 3D (SBS) para o Player, um ativo do Substance 3D (SBSAR) é publicado como um *arquivo temporário*.

## Problemas

Você pode receber erros ao enviar pacotes, como:

```
Error sending package to Substance 3D Painter. Check the console for details. SBSAR export failed.
```


Isso geralmente ocorre devido a erros e avisos padrão. Corrija-os para resolver o problema:

* Nenhum nó de [saída](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)definido no gráfico. Adicione nós de saída e conecte algo a eles;
* Variáveis ausentes ou quebradas em [Obter nós](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) em [gráficos de funções](../../../function-graphs/function-graphs.md). Rastreie-os pelo *emblema de aviso amarelo* nos nós afetados.
