---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/best-practices/performance-optimization-guidelines.html"
breadcrumb-title: ''
description: Saiba mais sobre as diretrizes de otimização de desempenho para o Substance 3D Designer para melhorar o desempenho do gráfico e reduzir o tempo de processamento.
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Performance optimization guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Diretrizes de otimização de desempenho
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 0%

---


# Diretrizes de otimização de desempenho

## Gráficos do Substance

Quanto mais complexos forem os [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md), mais poder de processamento será necessário para renderizá-los. Você deve tentar <b>encontrar um equilíbrio entre a complexidade e a velocidade de renderização</b>.\
Isso é *especialmente* importante se você for usá-los em aplicativos gráficos em tempo real, como jogos.

Em geral, os nós que expõem parâmetros personalizados - que podem ser modificados em tempo de execução - <b>devem ser colocados o mais próximo possível do final do gráfico</b>.

Isso ocorre porque a saída de cada nó é armazenada em cache sempre que possível. Portanto, quanto mais acima o gráfico seu nó ajustável estiver, mais saídas precisarão ser processadas sempre que um desses parâmetros expostos for modificado. Se o nó exposto estiver próximo ao final do gráfico, somente alguns nós entre ele e os nós de saída precisarão ser recalculados.

Por exemplo, se ajustar uma cor uniforme no início do seu gráfico, todos os nós seguintes serão recalculados. Se você ajustar um nó HSL colocado logo antes da saída, somente esse nó será recalculado, melhorando significativamente o desempenho do gráfico.

Anote bem as seguintes diretrizes:

### CONFIGURAÇÕES GERAIS RELACIONADAS AO DESEMPENHO

+++O mecanismo da GPU é muito mais rápido do que o mecanismo da CPU
A menos que você tenha uma placa gráfica não suportada (integrada), use o mecanismo do Substance GPU (altere com a tecla de atalho F9).

+++

+++A alternância da resolução principal do gráfico é lenta
Ele recalcula gráficos, cache e todas as miniaturas. É melhor usar a [guia <b>Lote </b> da caixa de diálogo de exportação](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md), pois ela evita recálculos extensivos e desnecessários (por exemplo, ao exportar para resolução 8192).

+++

+++Em casos extremos, pode ser necessário aumentar o cache de memória
O aplicativo [limita a quantidade de RAM que pode ser usada](../../interface/preferences-window/preferences-window.md) para o cache de imagem, mas você pode substituí-la e aumentá-la (com cuidado).

+++

### OTIMIZAÇÃO DE GRÁFICOS

+++Preste muita atenção às resoluções de nós e herança em geral!
Valores altos afetarão seriamente o desempenho, portanto, considere como o material é susceptível de ser usado e se você pode reduzir os tamanhos dos dados envolvidos.

Recomendamos que você saiba mais sobre a [resolução de nós (tamanho da saída)](../../compositing-graphs/output-size/output-size.md) e a [herança em gráficos de Substance](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md).

+++

+++Usar escala de cinza quando nenhuma cor for necessária
As operações de cor demoram quatro vezes mais do que as operações em tons de cinza. Tente também minimizar as conversões de texto entre cores e tons de cinza.

+++

+++Usar 8 bits quando não for necessário usar 16 bits
Na verdade, a versão de CPU do Substance Engine (SSE2) *não* é compatível com cores de 16 bits ou tons de cinza de 8 bits. O mecanismo de GPU é compatível com todas as 4 combinações de 8/16 bits e escala de cinza/cor. *Atualmente, apenas o mecanismo da CPU é usado nos plug-ins Unity e Unreal Engine*.

+++

+++Minimizar o tamanho da saída do nó sempre que possível
Às vezes, o downsizing de alguns nós não afeta o resultado final, mas afetará o desempenho. Por exemplo, usar um nó de Cor uniforme definido com o mesmo tamanho de saída que o documento não tem sentido: a Cor uniforme deve ser definida como Absoluta [16px x 16px] e o nó subsequente como Relativo ao pai. Geralmente, esse truque funciona bem para imagens de baixa frequência, como o ruído de Perlin.

+++

+++Não use imagens menores do que 16 * 16 pixels
Isso reduz o desempenho da renderização.

+++

+++Ao usar o nó Combinar, desative a mesclagem de alfa quando não for necessário


+++

+++Desfoques e deformações são os nós que exigem mais do processador


+++

+++Alguns geradores de ruído são afetados pela quantidade de padrões desenhados
Por exemplo, o nó [Tile Generator](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) ficará mais lento para processar os mais padrões que você adicionar a ele.

+++

+++Alguns ruídos são afetados por um fator de escala
Este fator irá, de fato, desenhar mais padrões. Os nós afetados incluem ruídos, padrões de Células etc. Se você precisar de um padrão de ruído branco, não use um ruído com um valor de escala muito alto e use os nós [Ruído branco](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise/white-noise.md) ou [Ruído branco rápido](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise-fast/white-noise-fast.md).

+++

+++Por outro lado, existem alguns geradores de ruído muito rápidos
Estes incluem [Ruído Branco Rápido](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise-fast/white-noise-fast.md), [Base de Soma fractal](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md) e [Ruído Anisotrópico](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/anisotropic-noise/anisotropic-noise.md).

+++

+++Cuidado com funções pesadas de amostragem de imagem em alguns casos
As funções são executadas no mecanismo da CPU, exceto em [Processadores de Pixel](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md). Se você estiver fazendo muita amostragem de imagens pesadas (alterando as coordenadas do $pos) nos [Processadores de Valor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) ou nos [FXmaps](../../function-graphs/fxmaps/fxmaps.md), haverá muita troca entre o VRAM e a RAM da CPU, causando atrasos de desempenho.

+++

### OTIMIZAÇÕES PARA USO EM DISPOSITIVOS MÓVEIS

+++Não é recomendável usar deformações e FX-Maps
Eles são muito caros.

+++

+++Evite desfocar nós
Use transformações em escala reduzida.

+++

+++Trabalhe o máximo possível em tons de cinza
Alterne para o modo de cores no final do gráfico.

+++

+++Compartilhar nós o máximo possível entre as saídas


+++

### OTIMIZAÇÕES DE TAMANHO PARA BITMAPS INCORPORADOS

[Os bitmaps](../../resources/bitmap-resource/bitmap-resource.md) têm seu [Tamanho de saída](../../compositing-graphs/output-size/output-size.md) definido como [&#39;Absoluto&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) por padrão. Isso significa que, se o bitmap for conectado por meio da cadeia de nós a uma saída, ele forçará a saída final a ser do tamanho do bitmap incorporado.\
Um nó inserido após o bitmap terá seu Tamanho de Saída definido como [&#39;Relativo à Entrada&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md). Isso significa que o nó também será inerente ao tamanho do bitmap e transportará esse tamanho pela cadeia do nó até as saídas. Para corrigir isso, é necessário definir o nó após o bitmap para ter seu Tamanho de Saída definido como [&#39;Relativo ao Pai&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md).

Se o gráfico estiver definido para ter uma resolução dinâmica, você poderá alterar o Tamanho de saída no bitmap incorporado para Relativo ao pai.\
Dessa forma, o tamanho do bitmap será alterado com base no gráfico pai, e você não entrará em uma situação em que o gráfico esteja processando uma resolução mais alta no bitmap do que a necessária.

>[!WARNING]
>
> Definir um nó [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) como “Relativo ao pai” e [publicar](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) o gráfico em um ativo do Substance 3D (SBSAR) salvará o bitmap em uma resolução de **256x256** em vez do tamanho original. Em vez disso, é aconselhável manter o [método de herança](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) dos nós de Bitmap&#39; [Tamanho de Saída](../../compositing-graphs/output-size/output-size.md) como &#39;Absoluto&#39; e usar um nó [Transformation 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) definido como &#39;Relativo ao pai&#39; logo após o nó de Bitmap.

![Otimização de bitmaps incorporados 1](performance-optimization-guidelines.resources/performance-optimization-guidelines-01.jpg "Otimização de bitmaps incorporados 1")

![Otimização de bitmaps incorporados 2](performance-optimization-guidelines.resources/performance-optimization-guidelines-02.jpg "Otimização de bitmaps incorporados 2")

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Além disso, é aconselhável definir o formato dos recursos de bitmap para Jpeg para minimizar o tamanho dos ativos do Substance 3D publicados (SBSAR).

</td>
<td style="border: 0;" valign="top">

![Otimização de bitmaps incorporados 3](performance-optimization-guidelines.resources/performance-optimization-guidelines-03.jpg "Otimização de bitmaps incorporados 3")

</td>
</tr>
</table>
