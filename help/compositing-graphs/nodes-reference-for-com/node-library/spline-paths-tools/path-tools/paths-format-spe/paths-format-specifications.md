---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-format-specifications.html"
breadcrumb-title: ''
description: Saiba mais sobre as especificações de formato de caminhos e a estrutura de dados usada pelos nós de caminho e spline.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Format Specifications
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Especificações de formato de caminhos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '2491'
ht-degree: 0%

---


# Especificações de formato de caminhos

Esta página descreve o formato de Caminhos e fornece orientação para manipular dados nesse formato usando as funções incluídas nas ferramentas de Caminhos.

## Especificações de formato

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Esta seção explica como um <b>documento de caminhos</b> (ou imagem) é codificado:

Um documento Caminhos é uma lista de caminhos, cada um descrevendo uma lista de segmentos codificados em uma <b>textura de cores de ponto flutuante de 32 bits</b>.

A textura é dividida em partes &#39;superior&#39; (*$pos.y &lt; 0,5*) e &#39;inferior&#39; (*$pos.y > 0,5*).

Quaisquer dados em um pixel na parte &#39;superior&#39; estão semanticamente relacionados ao pixel correspondente na parte &#39;inferior&#39; e vice-versa.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Dados codificados do polígono dos caminhos](paths-format-specifications.resources/PathsPolygon_Data.jpg "Dados codificados do polígono dos caminhos")

</td>
</tr>
</table>

>[!NOTE]
>
> Os dados de caminhos exigem uma precisão de 32 bits, e o uso de uma profundidade de bits menor produzirá resultados incorretos.
> 
> Portanto, certifique-se de definir o parâmetro &#39;Formato de saída&#39; dos nós que geram dados de Caminhos como &#39;Alta precisão HDR (32F)&#39;.

Seja `*uv\_pos*` um endereço 2D (como *$pos*) de um pixel da parte &#39;superior&#39;.

No restante deste documento:

* <b>top[uv\_pos].XYZW</b> se referirá aos 4 flutuadores armazenados no pixel da parte superior.\
  top[uv\_pos] == amostra\_cor(caminhos, uv\_pos)
* <b>bottom[uv\_pos].XYZW</b> se refere aos 4 flutuantes armazenados no pixel correspondente da parte inferior.\
  inferior[uv\_pos] == amostra\_cor(caminhos, uv\_pos + Flutuante2(0, 0.5))

top[uv\_pos] e bottom[uv\_pos] juntos estão formando uma unidade semântica U[uv\_pos] do documento, composta de 8 flutuações.

### Cabeçalho do documento

Todo documento de Caminhos começa com um cabeçalho de documento. É a primeira unidade semântica U[(0,0)]:

+++Superior
<b>X</b>

O número de caminhos (deve ser um inteiro positivo em [0; 16777216]).

Se alguns caminhos estiverem vazios, eles ainda contam aqui. Portanto, você pode pensar nele como um “número de cabeçalhos de caminhos a serem decodificados”.

<b>YZ</b>

O tamanho do pixel deste documento (ou seja, exatamente `Float2(1,1) / $size`).

Isso é útil ao ler os Caminhos de um [processador de pixels](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) ou de um [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md), por exemplo, cujo Tamanho de Saída é diferente.

<b>W</b>

1/16 = 0.0625 (sinalizador de cabeçalho)

+++

+++Inferior
<b>XY</b>

O endereço do último vértice definido neste documento. É útil acrescentar novos dados.

Pode, portanto, ser qualquer endereço que seja maior (em ordem de linha de varredura) do que o endereço do último vértice. Ele deve estar no intervalo ]0, 1[×]0,.5[

<b>ZW</b>

Sem uso, deve ser Float2(0, 1)

+++

### Cabeçalhos de caminho

O cabeçalho do documento é imediatamente seguido por number-of-paths = top[(0,0)].X path-headers, um por unidade semântica.\
E.g. se houver 3 caminhos no documento, eles serão armazenados em U[(0,1)\*pixel\_size], U[(0,2)\*pixel\_size] e U[(0,3)\*pixel\_size] (com pixel\_size = top[(0,0)].YZ).

Se houver mais caminhos do que uma linha de pixel pode conter, os cabeçalhos de caminho restantes serão gravados na(s) próxima(s) linha(s), na ordem de linhas de varredura.\
É permitido ter cabeçalhos de caminho nulos (`top[...].XYZW = Float4(0,0,0,0)`); esse caminho ainda pode ter um caminho vazio.

O cabeçalho de caminho do enésimo caminho será definido no endereço `path\_addr` será definido como:

+++Superior
<b>X</b>

Número de vértices nesse caminho. Deve estar no intervalo [0, 16777216].

Se os vértices inicial e final de um caminho fechado estiverem na mesma posição, eles ainda contam para 2 vértices.\
Um caminho com 0 vértices é um caminho válido mesmo assim.

<b>A</b>

Sinalizador *Is\_closed*: 1 se o caminho estiver fechado (por exemplo, um círculo); caso contrário, 0 (por exemplo, uma linha reta).

<b>Z</b>

O índice de caminho *N.* Deve corresponder absolutamente a *path\_addr* (veja a observação abaixo).

<b>W</b>

O sinalizador de cabeçalho: 1/16 = 0,0625.

+++

+++Inferior
<b>XY</b>

Endereço do primeiro vértice.

<b>ZW</b>

Endereço do último vértice.

+++

>[!NOTE]
>
> Você pode computar `path\_addr` de N usando a função `Utils/pixel\_index\_to\_position` em paths\_tools.sbs: `path\_addr = pixel\_index\_to\_position(N+1)`

### Informações de vértices

Os vértices podem ser encontrados em qualquer lugar na imagem após os cabeçalhos (cabeçalhos de documento ou caminho). Os vértices podem ser de vários “tipos” (Início, Meio ou Fim) e são explicitamente vinculados usando dois ponteiros de endereço (”links”).

Os vértices de <b>Início</b> e <b>Fim</b> são especiais a esse respeito: para permitir a representação de caminhos fechados ou de uma rede arbitrária de caminhos vinculados, um dos vínculos é realmente usado para formar uma lista circular vinculada à frente de todos os outros vértices de Início ou Fim que representam o mesmo vértice. Esses vértices que se combinam entre si são chamados de “irmãos”. [Ilustração bem-vinda]

Formalmente, cada vértice no endereço `*vert\_addr*` é definido da seguinte forma:

+++Superior
<b>XY</b>

A posição do vértice. As coordenadas podem ser qualquer valor de flutuação que não seja NaN ou ±inf. Não há noção de azulejos neste nível (pode ser manipulado ou não pela implementação de cada filtro), então os caminhos devem ser definidos no plano euclidiano.

<b>Z</b>

O índice do caminho do vértice. Um vértice só pode pertencer a um Caminho. (Como mencionado anteriormente, os vértices inicial e final podem ter irmãos.) O índice de caminho pode ser usado para recuperar o cabeçalho path (consulte Cabeçalhos de caminho de seção acima), portanto certifique-se de mantê-lo sincronizado.

<b>W</b>

Tipo de vértice. É dividido entre o sinal do valor e seu valor absoluto:

Na parte de sinal, um valor de 0 significaria que não há nenhum vértice aqui realmente (todos os outros componentes devem ser 0 também). Um valor negativo significa que o vértice está marcado como um “canto”; um positivo indica que o vértice é “suave”. O vértice de canto vs. suave é um atributo puro e isolado e não tem impacto ou significado no restante da codificação de Caminhos.

Na parte do valor absoluto, o tipo de pixel (Início, Meio ou Fim) e outro sinalizador (trivial\_link) são codificados:

* *0.125*: vértice final (o último vértice da forma; sempre links não triviais, veja abaixo)

* *0.25*: iniciar vértice (o primeiro vértice da forma; sempre links não triviais, veja abaixo)

* *0.5*: vértice intermediário com links não triviais

* *1*: vértice intermediário com links triviais

“Links triviais” referem-se ao fato de que os vértices anteriores e seguintes (na lista de vértices do caminho atual) são armazenados no pixel à esquerda (vert\_addr-(0,pixel\_size)) e à direita (vert\_addr+(0,pixel\_size)) respectivamente, enquanto “links não triviais” significa que pelo menos um deles é armazenado em outro lugar.

+++

+++Inferior
Independentemente da “trivialidade” dos links, os valores confiáveis dos links são armazenados na parte inferior:

<b>XY</b>

O endereço do vértice anterior deste caminho. Para vértices iniciais, isso aponta para o próximo vértice irmão.\
se |top[vert\_addr].W| = 1, then bottom[vert\_addr].XY = vert\_addr - (0,pixel\_size)

<b>ZW</b>

O endereço do próximo vértice deste caminho. Para vértices de término, isso aponta para o próximo vértice irmão.\
se |top[vert\_addr].W| = 1, then bottom[vert\_addr].ZW = vert\_addr + (0,pixel\_size)

+++

## Lendo e gravando informações de caminhos

Para criar seus próprios nós de processamento de caminhos, você tem várias ferramentas.

O básico é fornecido pelos nós [Processador de Vértice de Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md) e [Processador de Vértice de Caminhos Simples](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md), que podem ser usados basicamente da mesma maneira que um [Processador de Pixels](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md).

Se você precisar de recursos além do que os nós do Processador de Vértice de Caminhos oferecem (mais texturas de entrada ou mais vértices anteriores ou seguintes), copiar a implementação deste gráfico pode ser um bom ponto de partida (pressupondo que você substitua o nó <b>Get(”%perVertex”)</b> por seu processamento personalizado).

Mas no caso de você querer fazer algo mais estranho do que aplicar uma função por vértice, aqui está uma explicação detalhada das ferramentas que você pode usar. Geralmente, são pequenas funções auxiliares que podem ser encontradas no mesmo pacote que os outros nós de Caminhos (*paths\_tools.sbs)*. (Essas funções não são expostas na [<b>Biblioteca</b>](../../../../../../interface/the-library/the-library.md) e no <b>menu Nó</b>.)

### Funções de &#39;leitura&#39;

Na pasta `Read`, você pode encontrar várias delas, úteis para coletar informações sobre os Caminhos:

Alguns podem fornecer informações sobre um determinado pixel. Todos eles usam o valor de amostra Float4 na parte \*top\* como entrada. Se você observar a implementação deles, eles são super simples. Seu objetivo é transmitir mais significado do que apenas nós atômicos:

+++is_header
Verifique se o valor de amostra atual é um cabeçalho de caminho ou um cabeçalho de documento.

+++

+++path_is_closed
Marque o sinalizador Is\_Closed (.Y) em um cabeçalho de caminho. Ele \*supõe que você já verificou que é um caminho\* com `is\_header` e que `current\_pixel\_is\_document\_header` retornou false.

+++

+++is_vertex
Verifique se o valor amostrado atual é um vértice, isto é, não um cabeçalho, nem um pixel vazio.

+++

+++is_start_vertex
Verifique se um valor de \*parte superior amostrada\* é um vértice inicial (não é necessário marcar `is\_vertex` primeiro).

+++

+++is_mid_vertex
Verifique se um valor de \*parte superior amostrada\* é um vértice que não é um vértice de Início ou de Término (não é necessário marcar `is\_vertex` primeiro).

+++

+++is_end_vertex
Verifique se um valor de \*parte superior amostrada\* é um vértice de término (não é necessário marcar `is\_vertex` primeiro).

+++

+++is_segment_start
Curto para `is\_start\_vertex || is\_mid\_vertex`. Mais útil para o processamento baseado em [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) para processar cada segmento no máximo uma vez.

+++

+++is_corner
Verifique o sinalizador de canto do vértice (não é necessário marcar `is\_vertex` primeiro: se a resposta for verdadeira, você está em um vértice com certeza). Lembre-se de que este sinalizador ainda não é suportado por nós oficiais.

+++

+++has_trivial_links
Se esse for um vértice, indica se você pode deduzir facilmente a posição dos vértices anterior e seguinte sem amostrar a parte inferior. (Observação: um não-vértice sempre retornará false.)

Você provavelmente não deseja usar isso diretamente, mas sim usar uma das funções `sample\_next\*` ou `sample\_prev\*`, que cuidam disso para você.

+++

+++sample_next, sample_prev
Dado o valor de amostra da parte superior `*sampled*` e sua posição `*sampled\_position*`, retorna o próximo valor de amostra da parte superior do vértice (respectivamente, anterior) e define uma variável Float2 `*next\_sampled\_pos*` para a posição (na parte superior) desse vizinho (ou seja, &lt;valor retornado> = SampleColor(next\_sampl\_pos, image0)). `*input0PixSize*`deve ser igual ao tamanho de pixel do caminho (top[(0,0)].YZ).

Se o pixel atual (`*sampled*`) for um vértice <b>Início</b>, a *amostra\_prev* retornará o próximo irmão deste vértice; da mesma forma, se for um vértice <b>Fim</b>, a *amostra\_próximo* retornará o próximo irmão deste vértice (ou seja, talvez não seja o que você deseja). Consulte `*sample\_next\_advanced*` e `*sample\_prev\_advanced*` abaixo para resolver isso.

Observe que, para simplificar, presume-se que as informações de caminhos sejam armazenadas em input0!</b> <b>Além disso, diferentemente do que o documento da função indica, não é necessário pré-declarar `*next\_sampled\_pos*`. `*[out]next\_sampled\_pos*` é um parâmetro fictício para lembrá-lo de que este segundo “valor de retorno” existe.

Você pode verificar o `*paths\_trace*` [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md), no parâmetro Iterations do 3º nó Iterar, para obter um exemplo de como usá-lo.

![Caso de uso mínimo de sample_next](paths-format-specifications.resources/paths-spec_fxmap-sample-next_02.png "Caso de uso mínimo de sample_next")



![Caso de uso sample_next em Caminhos de Visualização (path_trace)](paths-format-specifications.resources/paths-spec_fxmap-sample-next_01.png "Caso de uso sample_next em Caminhos de Visualização (path_trace)")



+++

+++sample_next_advanced, sample_prev_advanced
O objetivo é trabalhar em caminhos fechados. Para caminhos abertos, o vértice Start ou End não tem um irmão e, nesse caso, ambas as funções retornam o mesmo e único vizinho. Para vértices inicial ou final com mais de um irmão (Caminhos conectados como uma rede), isso retornaria o vértice vizinho do próximo irmão na lista vinculada.

+++

### Funções de &#39;gravação&#39;

Na pasta `Write`, você encontrará pequenos auxiliares que compilam um Float4 pronto para ser gravado <b> por um [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)</b>.

Na verdade, o [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) multiplica RGB por Alpha antes de desenhar, portanto, os valores reais não são pré-multiplicados para compensar isso. Se você quiser usar essas funções, por exemplo, em um [Processador de pixels](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), recomendamos que você mesmo aplique a pré-multiplicação novamente ou que escreva uma versão personalizada (mais otimizada para seu caso de uso e mais fácil de usar).

+++document_header
Constrói a parte superior do cabeçalho do documento, declarando o número de caminhos que você fornece.

+++

+++document_last_vertex_spec
Cria a parte \*inferior\* do cabeçalho do documento, que especifica o último endereço de vértice (consulte A.1.).

+++

+++path_header
Compila a parte superior de um cabeçalho de caminho, de acordo com o número de vértices no caminho `*nbVertices*`, o sinalizador `*isClosed*` e o `*pathIndex*`.

+++

+++start_vertex, mid_vertex, end_vertex
Constrói a parte superior de um vértice, definindo a posição, o tipo e outras opções de acordo.

Sobre o *mid\_vertex* e o parâmetro *hasTrivialLinks*: idealmente, você deve definir o valor apropriado, mas se por algum motivo você não conseguir dizer se os links serão triviais ou não, você pode defini-los com segurança como false (às custas do processamento mais lento do caminho gerado).

+++

Não há construtor de parte inferior para cabeçalhos de caminho nem vértices: ambos codificam dois links para a parte superior, então esta função seria essencialmente um construtor de vetor Float4 de dois Float2. Não se esqueça de dividir XYZ por W se você estiver escrevendo usando um [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) (W sendo o Y de um endereço, ele nunca deve ser nulo).

Você encontrará um exemplo pertinente de como usar essas funções no pacote <b>*paths\_polygon.sbs* </b>que hospeda o nó [Polígono de Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md).

### Métodos de processamento de caminhos

Você provavelmente usará um Processador de Pixel ou um Mapa de Fx para implementar seu processamento personalizado, cada um dos quais tem sua força e fraquezas:

+++FX-Map
A solução baseada em [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) geralmente será preferida ao executar operações de alto nível que exijam um conhecimento global de todo o caminho (ou caminhos) ou cumulativo (por exemplo, recompactação de vértices após dizimação ou mosaico). Também é a abordagem mais fácil, portanto, se você estiver fazendo um processamento personalizado pela primeira vez, talvez queira usar um Fx-Map, apesar dele *pode ser mais lento*.

Você precisa estar familiarizado com o Fx-Map em primeiro lugar. Se não for esse o caso, verifique a [documentação específica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md).

Recomendamos que você observe a implementação de [Caminhos de visualização](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) em <b>*caminhos\_trace.sbs*</b> e [Polígono dos caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md) em <b>*caminhos\_polygon.sbs*</b> para ter uma ideia sobre como ler e gravar (respectivamente) o caminho usando um Fx-Map.

+++

+++Processador de pixels
A solução [Processador de pixels](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) será adequada se você precisar apenas de informações “locais”. Aqui, queremos dizer “local” não espacialmente (a distância entre os elementos), mas sim topologicamente (vértices ligados entre si). É assim que o Vertex Processor é implementado. O Processador de Pixels é geralmente mais rápido do que o Fx-Map para este tipo de operação, já que cada função de pixel é avaliada em paralelo, enquanto apenas uma quantidade limitada de dados é acessada. Porém, o esforço de implementação pode ser muito mais importante, pois você só pode modificar o pixel atual.

Não entraremos em detalhes, pois há muito a dizer dependendo do caso de uso específico, mas a primeira coisa a fazer é verificar onde você está:

Você está na parte superior ($pos.y &lt; 0,5) ou inferior ($pos.y > 0,5)? Recomendamos que você lembre-se de que em uma variável dedicada (por exemplo, `*isTop*`), e que crie uma `*vert.addr*` Flutuante2, esses valores são `*$pos*` para a parte superior e `$pos - (0,0.5)` para a parte inferior.

O que está em *vert.addr*? Faça uma amostra e verifique se há algo (W != 0) e, se houver, o que exatamente. Um cabeçalho (W = 0.0625) (verifique com `*Read/is\_header*`) ou um vértice (verifique com `Read/is\_vertex`)? Se for um cabeçalho, será o cabeçalho do documento ou um cabeçalho de Caminho? (Você pode usar `*Read/current\_pixel\_is\_document\_header*` para verificar isso.) Use uma ou várias das funções auxiliares para coincidir com o que é interessante para você.

+++
