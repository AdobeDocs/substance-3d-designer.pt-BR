---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter-circular.html"
breadcrumb-title: ''
description: Use o nó Circular respingos para dispersão formas circulares entre texturas para criar padrões orgânicos e aleatórios.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter Circular
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Espalhar Circular
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---


# Espalhar Circular

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/splatter-circular.png){width="128px"}

![](../../../../../../assets/splatter-circular-color.png){width="128px"}

## Divisória Circular (Cor)

**Entrada:** *Geradores De Textura**/Padrões*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Splatter Circular gera um padrão baseado em anel com vários controles. Ele pode usar formas predefinidas ou entradas personalizadas. É semelhante a [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), mas com um posicionamento circular em vez de uma grade.

Isso é útil quando você deseja inserir formas de uma forma circular com várias opções de aleatoriedade.

## Parâmetros

### Entradas

Ambas as entradas são opcionais.

* **Entrada de imagem de padrão 1-6**: *entrada em tons de cinza (entrada de cor)*\
  Somente Splatter Circular: imagem de padrão personalizada, usada quando o parâmetro “Pattern” está definido como “Image Input”.
* **Fundo**: *Entrada em tons de cinza (entrada Colorida)*

### Parâmetros

* **Valor do Padrão**: *1 - 64*\
  Quantidade de blocos gráficos de padrão para colocar em um anel.
* **Valor Aleatório do Padrão**: *0.0 - 1.0*\
  Aleatoriedade da quantidade de padrões a serem colocados. Melhor usado com uma quantidade de anel maior que 1.
* **Quantidade Aleatória de Padrões Mín**: *1 - 10* Define a quantidade mínima de padrões para aleatoriedade.
* **Valor do Toque**: *1 - 10*\
  Define o número de toques a preencher. Os anéis são sempre colocados dentro do externo, e o espaço é igual.
* **Expansão não quadrada**: *Falso/Verdadeiro*\
  Permite a compensação de esmagamento e alongamento com proporções não quadradas.
* **Padrão**
  * **Padrão**: *Entrada De Imagem, Quadrado, Disco, Paraboloide, Sino, Gaussiano, Espinho, Pirâmide, Tijolo, Gradação, Ondas, Meio Sino, Sino Ondulado, Crescente, Cápsula, Cone*\
    Seleciona a forma de padrão a ser usada.
  * **Número de Entrada de Padrão**: *1 - 6* Define o número de entradas de Imagem diferentes a serem usadas. Disponível somente quando a *Entrada de imagem* está selecionada acima.
  * **Distribuição de Entrada de Padrão**: *Aleatória, Por Número de Padrão, Por Número de Toque* Define como várias Entradas de Padrão são escolhidas. Aleatório significa que um número aleatório foi escolhido, Número de padrão significa que eles foram colocados em uma sequência em loop. Por números de anel significa que cada anel tem um diferente na sequência.
  * **Filtragem de Entrada de Imagem**: *Bilinear + Mipmaps, Bilinear, Mais Próximo*
  * **Específico de Padrão**: *0.0 - 1.0*\
    Permite que você altere a forma do padrão selecionado. O efeito depende do padrão selecionado.
  * **Simetria aleatória**: *0.0 - 1.0*\
    Define o número de ladrilhos que devem ser invertidos/espelhados aleatoriamente, de acordo com o comportamento abaixo.
  * **Modo de simetria aleatória**: *Horizontal + Vertical, Horizontal, Vertical* Determina o comportamento de espelhamento de simetria.
* **Posição**
  * **Raio**: *0.0 - 1.0*\
    Define o raio a partir do centro no qual os padrões são colocados.
  * **Raio aleatório**: *0.0 - 1.0* Dispõe aleatoriamente o raio de cada bloco de padrão.
  * **Multiplicador de Raio de Anel**: *0.0 - 1.0*\
    Afeta o espaçamento de vários anéis.
  * **Ângulo Aleatório**: *0.0 - 1.0* Aleatório o ângulo de cada padrão. Um montante mais elevado significa mais rotação.
  * **Fator de Espiral**: *0.0 - 1.0*\
    Transforma os anéis em Espirais, onde cada ladrilho é colocado em um raio levemente crescente.
  * **Difusão**: *0.0 - 2.0* Define a quantidade de voltas que um anel faz. Isto pode ser aumentado além de seus limites.
  * **Deslocamento ao longo da direção**: *0.0 - 1.0*\
    Move todos os padrões para fora do centro ao longo de seu ângulo. O efeito depende muito do Ângulo aleatório ou se parece apenas com um multiplicador do Raio.
  * **Deslocamento Global**: *0.0 - 1.0*\
    Converte toda a forma.
* **Tamanho**
  * **Conectar padrões**: *Falso/Verdadeiro* Torna o comprimento dos blocos gráficos de padrão dependente do raio, o que significa que cada forma deve tocar na anterior e na próxima.
  * **Tamanho (Conectado)**: *0.0 - 1.0*\
    Altera globalmente o tamanho de cada padrão. Quando conectado, é relativo ao raio total.
  * **Tamanho Aleatório**: *0.0 - 1.0*\
    Aleatório o tamanho de cada padrão individualmente.
  * **Escala**: *0.0 - 2.0*\
    Dimensiona uniformemente cada padrão.
  * **Escala aleatória**: *0.0 - 1.0*\
    Dispõe aleatoriamente o dimensionamento uniforme.
  * **Dimensionar por Número de Padrão**: *0.0 - 1.0* Torna a escala de padrão dependente da posição ao longo do anel.
  * **Inverter Número De Padrão**: *Falso/Verdadeiro*\
    Usado com a opção anterior, pode inverter o dimensionamento de pequeno para grande e vice-versa.
  * **Escala por Número de Anel**: *0.0 - 1.0* Torna a escala dependente do número de anel.
  * **Inverter Número de Anel**: *Falso/Verdadeiro* Usado com a opção anterior, pode inverter o dimensionamento de pequeno para grande e vice-versa.
* **Rotação**
  * **Rotação de Padrão**: *0.0 - 1.0* Gira todos os padrões uniformemente.
  * **Rotação de Padrão Aleatória**: *0.0 - 1.0*\
    Dispõe aleatoriamente a rotação do padrão.
  * **Tabela Dinâmica de Rotação de Padrão**: *Centro, Mín. X, Máx. X, Mín. Y, Máx. Y*\
    Define a posição do ponto de giro em torno da qual cada padrão será girado individualmente.
  * **Orientação Central**: *Falso/Verdadeiro*\
    Gira todos os padrões para que fiquem voltados para o centro do anel. Desativá-la fornece a todos a mesma orientação, o que pode produzir efeitos indesejados com Deslocamento ao longo da direção.
  * **Rotação de anel**: *0.0 - 1.0* Gira todo o anel ao redor do centro.
  * **Rotação aleatória de anel**: *0.0 - 1.0* Torna aleatória a rotação por anel.
  * **Deslocamento de Rotação de Anel**: *0.0 - 1.0*\
    Desloca a rotação por anel.
* **Cor**
  * **Cor**: *(valor de tons de cinza)*Cor para multiplicar pelo padrão selecionado.
  * **Luminância aleatória**: *0.0 - 1.0* Dispõe aleatoriamente a cor ou a luminância de cada bloco de padrão.
  * **Luminância por escala**: *0.0 - 1.0* Torna a Luminância dependente da escala de padrão individual.
  * **Luminância por Número de Padrão**: *0.0 - 1.0* Torna a Luminância dependente da sequência de padrão. Pode, por exemplo, ser usado com espirais.
  * **Inverter Número de Padrão**: *Falso/Verdadeiro* Inverte a opção anterior.
  * **Luminância por Número de Toque**: *0.0 - 1.0* Torna a Luminância dependente da sequência de toques.
  * **Inverter Número de Toque**: *Falso/Verdadeiro* Inverte a opção anterior.
  * **Máscara aleatória**: *0.0 - 1.0* Oculta padrões aleatoriamente.
  * **Cor do plano de fundo**: *(valor em tons de cinza)*Altera a cor do plano de fundo sólido.
  * **Modo de Mesclagem**: *Adicionar, Máx, Adicionar Sub* Define como mesclar padrões sobrepostos.
  * **Opacidade global**: *0.0 - 1.0* Define a opacidade global de todo o resultado.

## Imagens de exemplo

![](../../../../../../assets/circularsplatter-ex.png)

</td>
</tr>
</table>
