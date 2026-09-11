---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-mapper-color.html"
breadcrumb-title: ''
description: Use o nó Cor do mapeador de spline para mapear texturas de cores ao longo de caminhos de spline com parâmetros personalizáveis.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Point List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cor do mapeador de spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4ae20991693573dd44016a411c233b071fa96df6
workflow-type: tm+mt
source-wordcount: '1132'
ht-degree: 0%

---


# Cor do mapeador de spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](spline-mapper-color.resources/spline-mapper-color-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Mapeia uma imagem colorida de entrada em uma forma primitiva esticada ao longo das linhas de entrada.

A forma primitiva pode ser um plano, um meio-cilindro ou cilindro. Os cilindros podem ser torcidos ao longo da spline para deformar a imagem mapeada adequadamente.

</td>
</tr>
</table>

O nó gera a imagem mapeada como uma imagem colorida, bem como outras informações, como height, UVs (coordenadas de imagem, por exemplo) e uma máscara de ID para selecionar cada spline mapeada independentemente.

>[!IMPORTANT]
>
> O resultado pode incluir artefatos indesejados fora do envelope da spline ao usar valores de thickness muito baixos. Esse é um problema conhecido.

>[!NOTE]
>
> Consulte também [Escala de cinza do mapeador de spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale/spline-mapper-grayscale.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de entrada codificadas nos canais RGBA de uma imagem colorida:<br><b>R</b> - posição X<br><b>G</b> - posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br> - Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines de entrada codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de entrada. |
| <b>Mapa de cores</b> <i>Cor</i> | A imagem de cor de entrada que deve ser mapeada ao longo das linhas de entrada. |
| <b>Mapa de Heights</b> <i>Tons de cinza</i> | O mapa de altura de tons de cinza de entrada que deve ser mapeado ao longo das linhas de entrada. |
| <b>Twist curve</b> <i>Tons de cinza</i> | A imagem que descreve uma curva usando os valores de sua primeira linha de pixels.<br>Quando o parâmetro <b>Forma</b> é definido como <i>Meio Cilindro</i> ou <i>Cilindro</i>, essa entrada é usada para controlar a torção dos UVs em torno da forma. Seu impacto é controlado usando o parâmetro <b>Multiplicador de curva de UVs de torção</b>.<br>A curva fornece um perfil para a quantidade de rotação ao longo da spline, onde o primeiro pixel na linha é a rotação no início da spline e o último é a rotação no final. O valor da escala de cinza representa um número de voltas.<br>Você pode usar um nó [Curva](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) para criar a curva. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Cor</b> <i>Cor</i> | O resultado do mapeamento da imagem de cor de entrada nas linhas de entrada, como uma imagem colorida. |
| <b>Height</b> <i>Tons de cinza</i> | O resultado do mapeamento da imagem do Height de entrada nas splines de entrada, como uma imagem em tons de cinza. |
| <b>UV</b> <i>Cor</i> | Os UVs (ou seja, coordenadas) do mapeamento nas linhas de entrada, codificados em uma imagem colorida. |
| <b>ID</b> <i>Tons de cinza</i> | Máscara das imagens mapeadas ao longo das splines de entrada, na qual os valores de branco são incrementados em 1 de uma spline para a próxima, para que cada forma possa ser selecionada de maneira independente. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Valor de Segmentos</b> <i>Inteiro</i> | As splines são simplificadas em segmentos antes que as coordenadas da imagem os atravessem.<br>Uma quantidade maior de segmentos resulta em um mapeamento mais suave ao longo das curvas. |
| <b>UVs de Escala Automática</b> <i>Booleano</i> | Ajusta a escala das coordenadas automaticamente para manter uma imagem quadrada ao mapeá-la ao longo das linhas. |
| <b>Escala UV</b> <i>Flutuante2</i> | Ajusta a escala das coordenadas mapeadas em X (horizontalmente) e Y (verticalmente).<br>Valores mais altos resultam em uma imagem lado a lado mais densa. |
| <b>Modo</b> <i>Inteiro</i> | O método de seleção das splines ao longo das quais a imagem deve ser mapeada:<br>- <i>Desenhar Lista de Spline</i>: todas as splines na lista de entrada são usadas;<br>- <i>Desenhar Spline Único</i>: apenas a spline com o índice especificado é usada;<br>- <i>Desenhar Intervalo de Spline</i>: apenas as splines com índice incluído no intervalo especificado são usadas. |
| <b>Desenhar Índice de Spline</b> <i>Inteiro</i> | (Disponível quando “Modo” estiver definido como “Desenhar spline único”) O índice da spline ao longo da qual a imagem deve ser mapeada. |
| <b>Desenhar Intervalo De Spline</b> <i>Inteiro2</i> | (Disponível quando “Modo” estiver definido como “Desenhar intervalo de spline”) O intervalo de índices das splines ao longo do qual a imagem deve ser mapeada. |
| <b>Iniciar</b> <i>Flutuante</i> | Desloca o início da parte da spline que deve ser mapeada.<br>O valor representa o comprimento normalizado da spline. |
| <b>Fim</b> <i>Flutuante</i> | Desloca a extremidade da parte da spline que deve ser mapeada.<br>O valor representa o comprimento normalizado da spline. |
| <b>Modo de Thickness</b> <i>Inteiro</i> | O método de definição do thickness da imagem mapeada:<br>- <i>Manual</i>: defina o thickness explicitamente com um valor arbitrário;<br>- <i>Da spline</i>: use o thickness da spline. |
| <b>Thickness</b> <i>Flutuante</i> | (Disponível quando o “Modo de Thickness” está definido como “Manual”) O valor arbitrário para o thickness da imagem mapeada ao longo das splines. |
| <b>Multiplicador de Thickness</b> <i>Flutuante</i> | (Disponível quando o “Modo de Thickness” está definido como “De spline”) Um multiplicador global para o thickness da imagem mapeada ao longo das splines, quando esse thickness é acionado pelo das splines. |
| <b>Forma</b> <i>Inteiro</i> | A forma primitiva usada para mapear as coordenadas da imagem ao longo das splines:<br>- <i>Plano</i>: as coordenadas são mapeadas para um plano plano plano;<br>- <i>Meio Cilindro</i>: as coordenadas são mapeadas para um meio cilindro cujo eixo do círculo de base segue a direção da spline;<br>- <i>Cilindro</i>: as coordenadas são mapeadas para um cilindro cujo eixo do círculo de base segue a direção da spline. |
| <b>Multiplicador de Height de cilindro</b> <i>Flutuante</i> | (Disponível quando “Forma” é definida como “Meia garrafa” ou “Cilindro”) Um multiplicador da intensidade da contribuição do height do cilindro na saída do Height.<br>Os ajustes de Height são cumulativos. |
| <b>Deslocamento do Height do cilindro</b> <i>Flutuante</i> | (Disponível quando “Forma” está definida como “Meio cilindro” ou “Cilindro”) Desloca o centro do perfil de forma de Cilindro ou Meio cilindro da superfície da spline para um diâmetro abaixo da superfície. |
| <b>Intensidade de UVs de torção</b> <i>Flutuante</i> | (Disponível quando “Forma” é definida como “Meio Cilindro” ou “Cilindro”) A torção das coordenadas da imagem em torno do cilindro, em número de voltas.<br>A torção envolve girar o cilindro somente no final da spline. A rotação é então interpolada ao longo da spline. |
| <b>Multiplicador de curva de UVs de torção</b> <i>Flutuante</i> | (Disponível quando “Forma” é ajustada para “Meia garrafa” ou “Cilindro”) Um multiplicador para a intensidade da contribuição do Twist curve para a torção do cilindro.<br>A curva fornece um perfil para a quantidade de rotação ao longo da spline, onde o primeiro pixel na linha é a rotação no início da spline e o último é a rotação no final. O valor da escala de cinza representa um número de voltas. |
| <b>Deslocamento de curva de UVs de torção</b> <i>Flutuante</i> | (Disponível quando “Forma” estiver definida como “Meia garrafa” ou “Cilindro”) Aplica um deslocamento global aos valores de rotação fornecidos pelo Twist curve, em número de voltas. |
| <b>Multiplicador de Height de spline</b> <i>Flutuante</i> | Ajusta a intensidade da contribuição da entrada do Height de spline para a saída do Height.<br>Os ajustes de Height são cumulativos. |
| <b>Multiplicador de Height de entrada</b> <i>Flutuante</i> | Ajusta a intensidade da contribuição da entrada do Mapa de altura para a saída do Height.<br>Os ajustes de Height são cumulativos. |
| <b>Cor do plano de fundo</b> <i>Flutuante4</i> | A cor do plano de fundo na saída de cores. |
| <b>Correção Não Quadrada</b> <i>Booleano</i> | Ajuste a posição e o thickness dos pontos para manter a forma de spline em resoluções não quadradas.<br>Isso também afeta a distribuição uniforme. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-mapper-color.resources/SplineMapperColor-Variant1-Before.jpg" alt="SplineMapperColor-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-mapper-color.resources/SplineMapperColor-Variant1-After.jpg" alt="SplineMapperColor-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](spline-mapper-color.resources/SplineMapperColor-Demo.gif "Exemplo de nó 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 3](spline-mapper-color.resources/SplineMapperColor-Variant1-After1.jpg "Exemplo de nó 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
