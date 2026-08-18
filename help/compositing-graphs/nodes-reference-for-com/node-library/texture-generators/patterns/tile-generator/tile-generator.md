---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-generator.html"
breadcrumb-title: ''
description: Use o nó Tile Generator para criar padrões de ladrilhos de procedimento com controles personalizáveis de tamanho, deslocamento e variação.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gerador de blocos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 0%

---


# Gerador de blocos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-generator.png){width="128px"}

## Tile Generator (Cor)

**Entrada:** *Geradores De Textura**/Padrões*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

O Tile Generator é um dos nós mais avançados da biblioteca. Se aprender a dominá-lo, você pode criar qualquer tipo de padrão (dentro de algumas limitações). A partir da versão 2017 2.1, houve algumas grandes atualizações, tornando esse nó mais alinhado com o que o [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) pode fazer.

Este nó é altamente útil para uma variedade de cenários, mas tenha em mente que a simples leitura de parâmetros não ensinará totalmente como usá-los. Sugerimos que você experimente também!

Em 99% dos casos, a versão colorida NÃO é necessária.

Algumas dicas de uso geral:

* Você pode começar com uma forma básica, mas se tiver uma entrada personalizada (Defina **Tipo de Padrão** para *Entrada de Imagem*), crie-a primeiro! Determina muito o visual.
* Comece definindo corretamente os valores X e Y.
* Encontre o modo **Tamanho** correto: modos relativos, como **Interstício**, se comportam de maneira bem diferente dos modos **Absolutos**.
* Ajuste a **Escala** global e o **Tamanho** não uniforme em seguida.
* Por fim, ajuste qualquer parâmetro de **”Variação”** até que ele atenda às suas necessidades. Sutileza é a chave com variação!

## Parâmetros

### Entradas

* **Entrada de padrão 1-6**: *Entrada em tons de cinza*\
  Imagem de padrão personalizado, usada quando o parâmetro “Pattern” está definido como “Image Input”.
* **Plano de fundo**:*Entrada em tons de cinza* Plano de fundo a ser usado em vez da cor sólida.

### Parâmetros

* Valor **X**: *1 - 64*\
  Quantidade de repetições X do padrão.
* **Valor de Y**: *1 - 64*\
  Quantidade de repetições Y do padrão.
* **Expansão não quadrada**: *Falso/Verdadeiro*\
  Permite a compensação de esmagamento e alongamento com proporções não quadradas.
* **Padrão**
  * **Padrão**: *Entrada De Imagem, Quadrado, Disco, Paraboloide, Sino, Gaussiano, Espinho, Pirâmide, Tijolo, Gradação, Ondas, Meio Sino, Sino Ondulado, Crescente, Cápsula, Cone*\
    Seleciona a forma de padrão a ser usada.
  * **Número de Entrada de Padrão**: *1 - 6* Número de entradas de Imagem diferentes a serem usadas. Disponível somente quando a *Entrada de imagem* está selecionada acima.
  * **Distribuição de Entrada de Padrão**: *Aleatória, Por Número de Padrão* Como escolher entre as diferentes Entradas de Imagem, se mais de 1 estiver selecionado.
  * **Específico de Padrão**: *0.0 - 1.0*\
    Permite que você altere a forma do padrão selecionado. O efeito depende do padrão selecionado.
  * **Filtragem de Entrada de Imagem (Mecanismo >v4 somente)**: *Bilinear + Mipmaps, Bilinear, Mais Próximo*
  * **Rotação**: *0, 90, 180, 270* gira todos os blocos globalmente por um ângulo definido em etapas de 90 graus.
  * **Rotação Aleatória**: *0.0 - 1.0* A aleatoriedade gira um ladrilho em uma das quatro etapas de 90 graus.
  * **Inversão de Quincunx**: *Falso/Verdadeiro* Gira todos os outros ladrilhos em 90 graus.
  * **Simetria aleatória**: *0.0 - 1.0* Espelha aleatoriamente determinados padrões pelo Modo aleatório de Simetria selecionado. Quanto maior for esse valor, mais padrões serão espelhados.
  * **Modo Aleatório de Simetria**: *Horizontal + Vertical, Horizontal, Vertical* Determina o comportamento de espelhamento quando a Simetria aleatória é maior que 0.
* **Tamanho**
  * **** Modo de Tamanho **:***Normal - Interstício, Normal - Tamanho, Manter Proporção, Absoluto, Pixel*Define o comportamento geral do tamanho do padrão.\
    Normal - O Interstício permite definir a lacuna entre os elementos do padrão. É afetada pelo valor X e Y.\
    Normal - Tamanho permite que você defina o tamanho dos elementos do padrão, independentemente do espaço. É afetada pelo valor X e Y.\
    Manter proporção permite definir um tamanho afetado pela quantidade X e Y, mas a proporção X e Y entre os dois permanece intacta.\
    Absoluto permite definir um tamanho absoluto que não é afetado pela quantidade X e Y.\
    Pixel permite definir um tamanho absoluto em pixels, não afetado pela quantidade X e Y. Alterar a resolução afetará o tamanho dos elementos.
  * **Tamanho Médio**: *0.0 - 1.0* Altera o tamanho em uma base de coluna e linha alternada.
  * **Interstice X/Y**: *0.0 - 1.0* Disponível somente no modo Normal - Tamanho Interstice. Altera o intervalo de interstício. Afeta a junção entre as formas. Permite um controle não uniforme, diferentemente da **Escala**.
  * **Tamanho (Absoluto/Pixel)**: *0.0 - 1.0*\
    Disponível apenas fora de Normal - Modo de tamanho interstício. Define o tamanho não uniforme, diferentemente da **Escala**.
  * **Escala**: *0.0 - 2.0* Define a escala global.
  * **Escala aleatória**: *0.0 - 1.0* Define a variação de escala global por bloco.
  * **Dimensionar Distribuição Aleatória**: *0 - 1000* Desloca a semente de variação de escala.
* **Posição**
  * **Deslocamento**: *0.0 - 1.0* Desloca o padrão inteiro de forma incremental em cada linha ou coluna consecutiva (o comportamento depende do parâmetro Deslocamento Vertical).
  * **Deslocamento Aleatório**: *0.0 - 1.0* Aleatório deslocamento de linha.
  * **Deslocamento de propagação aleatória**: *0 - 1000* Altera a propagação relativa para o efeito de deslocamento aleatório.
  * **Deslocamento vertical**: *Falso/Verdadeiro* Define se o efeito Deslocamento ocorre sobre linhas ou linhas; Horizontal ou Vertical.
  * **Posição aleatória**: *0.0 - 1.0* Dispõe aleatoriamente a posição de maneira não uniforme, com controle separado para X e Y.
  * **Deslocamento Global**: *0.0 - 1.0* Desloca todo o resultado sobre os eixos X e Y.
* **Rotação**
  * **Rotação**: *0.0 - 1.0* Faz uma Rotação livre uniforme de todos os blocos de padrão.
  * **Rotação Aleatória**: *0.0 - 1.0* Torna aleatória a rotação livre de todos os blocos. Quanto maior o valor, mais blocos podem ser girados.
* **Cor**
  * **Cor**: *(valor de tons de cinza)*Define a cor sólida dos ladrilhos.
  * **Luminância/Aleatória de Cores**: *0.0 - 1.0* Introduz a variação de Cor ou Luminância por bloco.
  * **Luminância por número**: *Falso/Verdadeiro* Atenua a Luminância sobre todo o padrão.
  * **Luminância por escala**: *Falso/Verdadeiro* Torna a variação da Luminância dependente da escala do ladrilho.
  * **Máscara de Verificador**: *Falso/Verdadeiro* Oculta todos os outros ladrilhos.
  * **Máscara horizontal**: *Falso/Verdadeiro* Oculta todas as outras colunas.
  * **Máscara vertical**: *Falso/Verdadeiro* Oculta todas as outras linhas.
  * **Máscara aleatória**: *0.0 - 1.0* Oculta os blocos aleatoriamente. Quanto maior esse valor, mais blocos desaparecerão.
  * **Inverter Máscara**: *Falso/Verdadeiro* Inverte o resultado de quaisquer efeitos de mascaramento desta seção.
  * **Modo de mesclagem**: *Adicionar, Máx, Adicionar Sub* Define o modo de mesclagem a ser usado.
  * **Cor do plano de fundo**: *(valor de tons de cinza)*Define a cor do plano de fundo sólida.
  * **Opacidade global**: *0.0 - 1.0* Define a opacidade global dos blocos.
  * **Ordem inversa de renderização**: *Falso/Verdadeiro* Renderiza os blocos de volta para a frente ou vice-versa.

## Imagens de exemplo

![](../../../../../../assets/tilesampler-ex.png)

![](../../../../../../assets/image2020-9-17-14-50-18.png)

![](../../../../../../assets/image2020-9-17-14-52-4.png)

![](../../../../../../assets/image2020-9-17-14-53-47.png)

</td>
</tr>
</table>
