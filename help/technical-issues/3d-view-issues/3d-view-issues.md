---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/technical-issues/3d-view-issues.html"
breadcrumb-title: ''
description: Solucionar problemas de visualização 3D no Substance 3D Designer, incluindo problemas de renderização, exibição e desempenho.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > 3D View issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Problemas de visualização 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: d81d92788a4d52b5ae1ed3ac4287f07260894f3c
workflow-type: tm+mt
source-wordcount: '1643'
ht-degree: 0%

---


# Problemas de visualização 3D

Esta página lista problemas técnicos relacionados à [exibição 3D](../../interface/3d-view/3d-view.md) no Substance 3D Designer e oferece etapas de solução de problemas para cada um.

## Baixo desempenho: não é usada GPU separada

**![(erro)](../../assets/error.svg) Problema**

O Substance 3D Designer não usa a GPU *separada* do sistema (<b>dGPU</b>) e usa a GPU *integrada* (<b>iGPU</b>). Isso resulta em baixo desempenho ao renderizar gráficos e/ou a [exibição 3D](../../interface/3d-view/3d-view.md).

**![(tick)](../../assets/check.svg) Etapas recomendadas**

Sistemas com gráficos alternáveis podem *forçar a dGPU*, que deve ser usada para um *aplicativo específico* em um software dedicado, dependendo do fabricante da GPU.

Por exemplo, usuários com uma <b>dGPU Nvidia</b> podem fazer o seguinte:

1. Fechar o Substance 3D Designer
2. Abra o <b>Painel de Controle do NVIDIA</b>
3. Vá para a tela <b>Gerenciar configurações 3D</b> na seção <b>Configurações 3D</b>
4. Procure a entrada “Substance 3D Designer” na guia <b>Configurações do programa</b>
5. Selecione o <b>processador NVIDIA de alto desempenho</b> na caixa de combinação <b>GPU Preferencial</b>
6. Iniciar o Substance 3D Designer

>[!WARNING]
>
> Observe que as GPUs integradas (iGPU) *não são suportadas*. Você pode saber mais na página [Requisitos de sistema](../../getting-started/system-requirements/system-requirements.md).

## O objeto 3D é plano

**![(erro)](../../assets/error.svg) Problema**

Um objeto 3D que apresentou volumes detalhados em uma sessão torna-se plano na próxima sessão, no entanto, o gráfico não mudou e o mapa de Height transporta os mesmos dados.

**![(tick)](../../assets/check.svg) Etapas recomendadas**

O efeito de deformação de um objeto 3D de acordo com um mapa de Height é executado usando uma técnica chamada **deslocamento de mosaico**. Essa técnica envolve duas etapas:

1. **Mosaico**: a geometria do objeto é *subdividida* em vértices, resultando em uma *geometria mais densa* para dar suporte a detalhes de volume mais finos
2. **Deslocamento**: os vértices são *movidos* - isto é, deslocados - ao longo de seu *vetor normal*. O vetor normal segue a direção para a qual um polígono está apontado e tem uma magnitude (isto é, comprimento) de 1

A *direção* do deslocamento é conhecida: a direção do vetor normal.\
A *distância* do deslocamento pela qual os vértices são movidos é calculada da seguinte forma: `Distance = Height scale * Height map`. Como o mapa de Heights *não foi alterado* no gráfico, isso deixa a **escala de Heights**.

O valor padrão da escala de Height é **1.0**, que pode resultar em um efeito de deslocamento *não perceptível* dependendo da malha exibida na Exibição 3D e do mapa de Height aplicado a ela.

Esse valor pode ser modificado das seguintes maneiras:

| Na visualização 3D | Na visualização Gráfico |
|:--------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Use o **pop-up de Deslocamento** na barra de ferramentas à esquerda.<br>Saiba mais na [página dedicada](../../interface/3d-view/displacement/displacement.md). | Crie um nó [Saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) e defina o uso de `heightScale` em suas propriedades.<br>Forneça um valor para esta saída com um valor, usando um [nó Flutuante constante](../../compositing-graphs/nodes-reference-for-com/node-library/values/constant.md#floats) por exemplo, depois *reaplique o gráfico* na Exibição 3D. |

>[!TIP]
>
> Usando este método, você pode definir um valor de escala de Height personalizado *por gráfico*, que permite ajustá-lo para corresponder ao material específico desse gráfico.

## A visualização 3D é totalmente preta

**![(erro)](../../assets/error.svg) Problema**

Nas versões 15.0.0 e posteriores, a viewport da visualização 3D é preta plana. Vejo algumas sobreposições de texto (por exemplo, amostras e tempo de renderização), mas a cena 3D não está visível.

**![(tick)](../../assets/check.svg) Etapas recomendadas**

Versão 15.1 e superior

Os novos renderizadores 3D foram atualizados na versão 15.1 e exigem drivers de GPU recentes. Atualize os drivers de GPU do sistema para a versão mais recente.

Você pode encontrar drivers aqui: [NVIDIA](https://www.nvidia.com/Download/index.aspx?lang=en-us) [AMD](https://www.amd.com/en/support) [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)

Versão 15.0 e superior

O Designer [15.0.0](../../release-notes/version-15-0/version-15-0.md) apresentou nossos novos [renderizadores 3D](../../interface/3d-view/3d-renderers/3d-renderers.md) internos, que usam tecnologias modernas e, portanto, não são compatíveis com GPUs mais antigas.

As GPUs suportadas incluem a série NVIDIA RTX 20 (Turing) ou superior, de acordo com os [requisitos de sistema](../../getting-started/system-requirements/system-requirements.md) da Designer.

Você pode continuar usando o renderizador OpenGL por padrão, usando a [nova opção nas configurações do Projeto](../../interface/preferences-window/project-settings/project-settings.md):

1. Acesse Editar > Preferências > Projetos
2. Selecione o último arquivo de projeto na lista
3. Na lista de arquivos de projeto, selecione a guia Visualização 3D
4. Defina a opção &#39;Renderizador padrão&#39; como &#39;OpenGL (deprecated)&#39;
5. Clique em &#39;OK&#39; para validar as alterações

Agora, toda nova visualização 3D usará o renderizador OpenGL por padrão, o que permitirá que você continue trabalhando como antes.

>[!NOTE]
>
> O mesmo problema e as etapas de solução de problemas se aplicam à maioria das GPUs AMD e Intel, que atualmente *não são suportadas* por nossos novos renderizadores 3D.

>[!IMPORTANT]
>
> O renderizador OpenGL foi *descontinuado* e poderá ser removido do Designer no futuro. Recomendamos atualizar a GPU do sistema para evitar interrupções no fluxo de trabalho e garantir o suporte contínuo.

## A mensagem “Renderizador não compatível” é exibida

**![(erro)](../../assets/error.svg) Problema**

Nas versões 15.0.0 e posteriores, a mensagem “Renderizador não compatível” aparece no canto inferior direito da janela de visualização ao usar os novos renderizadores 3D (Rasterizador, rastreador de caminho de GPU). A cena 3D não está visível.

**![(tick)](../../assets/check.svg) Etapas recomendadas**

O Designer [15.0.0](../../release-notes/version-15-0/version-15-0.md) apresentou nossos novos [renderizadores 3D](../../interface/3d-view/3d-renderers/3d-renderers.md) internos, que usam tecnologias modernas e, portanto, não são compatíveis com GPUs mais antigas.

As GPUs suportadas incluem a série NVIDIA RTX 20 (Turing) ou superior, de acordo com os [requisitos de sistema](../../getting-started/system-requirements/system-requirements.md) da Designer.

Nas configurações padrão, a Exibição 3D retornará automaticamente ao renderizador OpenGL se a opção “Renderizador padrão” estiver definida como “Padrão (renderizador predefinido)” nas [Configurações do projeto](../../interface/preferences-window/project-settings/project-settings.md).

Você pode localizar e ajustar essa opção seguindo estas etapas:

1. Acesse Editar > Preferências > Projetos
2. Selecione o último arquivo de projeto na lista
3. Na lista de arquivos de projeto, selecione a guia Visualização 3D
4. A opção “Renderizador padrão” está listada nas configurações da guia

>[!NOTE]
>
> No momento, apenas GPUs da <b>série NVIDIA GTX</b> podem ser detectadas como não suportadas.
> 
> No entanto, a maioria das GPUs AMD e Intel também não é compatível e produzirá uma renderização em preto sem mensagem. Consulte o item “A exibição 3D é totalmente preta” acima para obter orientações sobre essas GPUs.

>[!IMPORTANT]
>
> O renderizador OpenGL foi *descontinuado* e poderá ser removido do Designer no futuro. Recomendamos atualizar a GPU do sistema para evitar interrupções no fluxo de trabalho e garantir o suporte contínuo.

## O objeto 3D parece totalmente suave

**![(erro)](../../assets/error.svg) Problema**

Depois de trabalhar nos dados enviados para a **saída [do** do Height](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md), o objeto parece ter algum volume, mas *parece totalmente suave*, como se as informações do height tivessem sido ignoradas no sombreamento.

<table style="margin-left: 0; margin-right: 0;">
<tr style="border: 0;">
<td style="border: 0; width: 60%; vertical-align: top">

**![(tick)](../../assets/check.svg) Etapas recomendadas**

Verifique se os dados do height estão *convertidos em normais* que estão conectados à saída **Normal** [&#128279;](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md).

Ao usar a técnica de **Deslocamento de mosaico** - consulte “objeto 3D plano” acima - os objetos podem *se deformar* para seguir os dados do height, mas sua superfície *não reagirá de forma diferente à luz* até que seus *normais* também sejam modificados para levar em conta os dados do height.

A solução é bem simples: conecte o último nó do fluxo que leva à saída do Height a um nó [Normal](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md). Ajuste o parâmetro de **Intensidade** desse nó de acordo com o material em que você está trabalhando e conecte o nó Normal à saída **Normal**.

</td>
<td style="border: 0; width: 40%; vertical-align: top">

![](../../assets/3dview-height-without-normals.gif){width="256px"}

</td>
</tr>
</table>

## A renderização está desfocada/pixelada

**![(erro)](../../assets/error.svg) Problema**

A imagem renderizada parece desfocada ou pixelada quando o sistema usa o *dimensionamento de exibição*.

<table style="margin-left: 0; margin-right: 0;">
<tr style="border: 0;">
<td style="border: 0; width: 60%; vertical-align: top">

**![(tick)](../../assets/check.svg) Etapas recomendadas**

Por padrão, o Designer usa a resolução de exibição *dimensionada* para definir a resolução de renderização da [exibição 3D](../../interface/3d-view/3d-view.md). Você pode alterar isso para que a resolução de exibição *nativa* seja usada em vez disso para uma renderização nítida.

Abra o menu **Editar** e selecione a opção **Preferências...**. Na janela [Preferências](../../interface/preferences-window/preferences-window.md), abra a seção **Exibição 3D** e defina o parâmetro **Escala de viewport** como *Nenhum*.

</td>
<td style="border: 0; width: 40%; vertical-align: top">

![](../../assets/demo-viewport-scaling-option.png){width="256px"}

</td>
</tr>
</table>

## Não consigo encontrar a propriedade &#39;Fator de mosaico&#39;

**![(erro)](../../assets/error.svg) Problema**

Depois de atualizar o Designer para a versão 15.0.0, não consigo encontrar o parâmetro “Fator de mosaico” nas propriedades do material onde ele estava.

**![(tick)](../../assets/check.svg) Etapas recomendadas**

Ao usar os novos renderizadores (Rasterizador e GPU Pathtracer), o “fator de mosaico” é encontrado nas propriedades desses renderizadores. No Modo de Exibição 3D, vá para <b>Renderizador > Editar configurações</b>. A propriedade será listada na área de Propriedades.

>[!NOTE]
>
> O escopo do mosaico varia de acordo com o renderizador:
> 
> * Rasterizador/GPU Pathtracer: um valor exclusivo aplicado globalmente a toda a cena.
> * OpenGL: um valor por material.
> * Iray: um valor por malha.

## Objetos 3D parecem errados: o sombreamento não combina com a iluminação

**![(erro)](../../assets/error.svg) Problema**

O sombreamento de objetos depende de seus vetores normais, tangentes e binormais. Suas coordenadas usam o intervalo [-1, 1], enquanto os mapas normais usam o intervalo [0, 1] na maioria dos casos. Para adaptar valores de um para o outro, uma <b>polarização e escala</b> precisam ser aplicadas: valor\*escala+polarização.

Por exemplo, uma escala de 2 e uma polarização de -1 adapta o valor x de [0, 1] para [-1, 1] assim: x\*2-1.

O Designer não aplica uma escala e uma polarização normais a menos que sejam especificadas por uma malha 3D. Se essas informações estiverem ausentes, um aviso será emitido no Console ao [substituir qualquer um de seus materiais](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md):

```
[SceneGraph]No 'scale' or 'bias' defined on the UsdUVTexture shader '/root/material/<materialName>' (the rendering may be incorrect)
```


**![(tick)](../../assets/check.svg) Etapas recomendadas**

Para cenas exportadas para formatos USD há algum tempo: exporte a cena novamente usando uma versão recente do USD, que incluirá os dados necessários. Preste atenção às propriedades relacionadas à escala normal e à polarização, se houver, que dependerá do software usado para exportar a cena.

Ao [substituir um material](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md), o Designer processa a malha e computa todos os dados ausentes relacionados às suas normais, tangentes e binormais. Se a escala e a polarização padrão do Designer corresponderem às necessárias para a malha, ela parecerá correta quando substituída.

## Falha ao iniciar a Visualização 3D

**![(erro)](../../assets/error.svg) Problema**

O Designer falha no momento de iniciar a Visualização 3D ao criar um projeto, carregar um projeto ou iniciar manualmente uma Visualização 3D.

**![(tick)](../../assets/check.svg) Etapas recomendadas**

Primeiro, verifique se o seu sistema atende aos [requisitos de sistema](../../getting-started/system-requirements/system-requirements.md) da Designer.

Em seguida, atualize seus drivers gráficos. Você pode encontrar os drivers mais recentes para sua GPU seguindo estes links: [NVIDIA](https://www.nvidia.com/Download/index.aspx?lang=en-us)  | [AMD](https://www.amd.com/en/support)  | [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)

Se o seu sistema incluir uma GPU integrada (iGPU) e uma GPU separada (dGPU), certifique-se de *atualizar os drivers para ambos*!

Em seguida, desative qualquer software que possa injetar ou sobrepor dados em um processo gráfico 3D. Os exemplos incluem:

* Injetores de pós-processo, como ReShade
* Sobreposições, como métricas de desempenho de GPU ou linhas cruzadas personalizadas
* Software de captura de tela para gravar, transmitir ou compartilhar gráficos 3D em tempo real
