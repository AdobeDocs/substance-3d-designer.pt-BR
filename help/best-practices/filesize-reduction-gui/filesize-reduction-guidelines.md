---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/best-practices/filesize-reduction-guidelines.html"
breadcrumb-title: ''
description: Saiba mais sobre as diretrizes para reduzir o tamanho dos arquivos de gráfico de Substance para otimizar os requisitos de desempenho e armazenamento.
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Filesize Reduction Guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Diretrizes de redução de tamanho de arquivo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 1%

---


# Visão geral

Em alguns casos, o tamanho total do arquivo dos [ativos do Substance 3D (SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) pode ser um fator importante. Esta página aborda algumas áreas e configurações críticas a serem consideradas ao tentar reduzir o tamanho do arquivo.

O tamanho do arquivo é determinado principalmente por [bitmaps incorporados.](../../resources/bitmap-resource/bitmap-resource.md) São arquivos vinculados, incorporados ou feitos bake e adicionados ao arquivo do [Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html) (SBS) como um recurso. Somente os bitmaps usados em um gráfico, ou seja, conectados a uma saída diretamente ou por meio da cadeia de nós, são publicados no ativo do Substance 3D. Em um arquivo do Substance 3D, os bitmaps não têm impacto no tamanho do arquivo, pois todos os recursos de bitmap ainda são armazenados fora do arquivo.

>[!IMPORTANT]
>
> Verifique se a propriedade [Tamanho de saída](../../compositing-graphs/output-size/output-size.md) de todos os nós [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) está definida como o método de herança [&#128279;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) ** Absoluto. Se não for esse o caso, o [recurso de bitmap](../../resources/bitmap-resource/bitmap-resource.md) referenciado nele será salvo na resolução padrão de 256\*256 no arquivo de ativo do Substance 3D publicado, o que* afetará a qualidade* de uma ou mais saídas.

## Fatores de tamanho de arquivo

Existem alguns fatores diferentes que afetam o tamanho total do arquivo do SBSAR. Eles estão listados abaixo com uma breve explicação.

+++Resolução
Obviamente tem um grande efeito. Use a menor resolução possível, tendo em mente que você também pode desejar que o arquivo de Substance funcione em grandes resoluções. Você pode usar truques padrão de mascaramento de resolução para fazer com que os bitmaps menores pareçam maiores.

*Encontrado em: software externo ou bitmap de importação/reexportação no Designer.*

+++

+++Modo de cores do arquivo
Definido no Editor de imagens antes da exportação, o modo de cores também afeta o tamanho do arquivo ao usar o formato de bitmap Raw. Os bitmaps somente em tons de cinza são menores que as imagens RGB(A).

*Encontrado em: software externo ou bitmap de importação/reexportação no Designer ao configurar [nós de saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) corretamente.*

+++

+++Formato de arquivo
O formato de arquivo das imagens faz a diferença, embora possa ser ignorado em alguns casos. Um programa como o Photoshop permite um pouco mais de controle sobre a compressão JPG e, às vezes, pode oferecer um meio-termo decente.

*Encontrado em: software externo ou bitmap de importação/reexportação no Designer.*

+++

+++Uso no gráfico
O modo para o qual você define o nó Bitmap também tem um efeito em como o Designer compacta o arquivo. O uso de um arquivo no modo Tons de Cinza como bitmap colorido no gráfico resultará em arquivos maiores. Certifique-se de defini-las corretamente.

*Encontrado em:[Propriedades do nó de bitmap.](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)*

+++

+++Formato de bitmap no pacote
Nas Propriedades do recurso, você pode escolher entre a compactação “Raw” e “Jpeg”. Isso pode ter um efeito considerável no resultado final.

*Encontrado em: Propriedades do Recurso de Bitmap, através da janela do Explorer.*

+++

+++Qualidade da compactação de bitmap no pacote
Ao usar o formato Bitmap “Jpeg”, o controle deslizante abaixo pode afetar a qualidade e o tamanho do arquivo. Este controle deslizante não se comporta muito previsível, mas 1 tende a corresponder à compressão JPG de alta qualidade, e 0,5 tende a dar o menor tamanho.

*Encontrado em: Propriedades do Recurso de Bitmap, através da janela do Explorer.*

+++

+++Modo de compactação ao publicar
Ao publicar no SBSAR, você tem a opção de escolher entre “Automático”, “Melhor” e “Nenhum” para compactação. Isso pode fazer uma diferença considerável se você estiver usando o formato de bitmap “Raw”. Também afeta muito a velocidade de exportação. Geralmente não é recomendado usar “nenhum”, pois não oferece nenhum aumento de qualidade.

*Encontrado em: configurações de publicação final para um pacote SBSAR.*

+++

## Comparação de tamanho de arquivo

A tabela abaixo mostra a influência de todas as configurações entre si. O bitmap usado é uma imagem de ruído gerado de 4096 x 4096, exportada do Photoshop como TGA de 24 bits ou JPG de qualidade 8. TGA&#39;s também foram exportados como tons de cinza e modo RGBA.

O gráfico apenas coloca um único nó de bitmap conectado a uma única saída. O modo Bitmap é definido de acordo com o modo de arquivo de origem.

Embora a tabela à direita não seja totalmente conclusiva, é possível aprender o seguinte ao comparar os resultados visuais e os tamanhos de arquivo:

* O Bitmap Bruto + Compactação Máxima oferece a melhor qualidade com um tamanho de arquivo aceitável.
* Arquivos de origem pré-compactados podem reduzir o tamanho dos arquivos na maioria dos casos, mas a um custo de qualidade.
* Menores tamanhos de arquivo, mas a pior qualidade é obtida com o formato de pacote JPG de qualidade 0,5.
* A escala de cinza nem sempre é menor no tamanho do arquivo, mas terá mais qualidade que a cor em configurações semelhantes.

>[!NOTE]
>
> **Formato De Bitmap Jpeg**
> 
> É importante observar que mapas especiais que exigem alta precisão, como Mapas normais, Mapas de vetor e outros, provavelmente não devem ser definidos para compactação Jpeg, pois isso levará a artefatos muito mais visíveis!

| Imagem de origem | TGA colorida | Cor JPG | TGA em tons de cinza | JPG de escala de cinza |
| --- | --- | --- | --- | --- |
| <b>Formato de Bitmap Bruto</b> Modo de compactação: *Nenhum* | 48 MB | 48 MB | 16 MB | 16 MB |
| <b>Formato de Bitmap Bruto</b> Modo de compactação: *Melhor* | 9,11 MB | 3,37 MB | 5,06 MB | 4,75 MB |
| <b>Formato De Bitmap Jpeg</b> Qualidade Da Compactação: *1* | 5,09 MB | 1.94 MB | 6,30 MB | 2,49 MB |
| <b>Formato De Bitmap Jpeg</b> Qualidade Da Compactação: *0.5* | 231 KB | 230 KB | 626 KB | 569 KB |
| <b>Formato De Bitmap Jpeg</b> Qualidade Da Compactação: *0* | 407 KB | 433 KB | 990 KB | 808 KB |
