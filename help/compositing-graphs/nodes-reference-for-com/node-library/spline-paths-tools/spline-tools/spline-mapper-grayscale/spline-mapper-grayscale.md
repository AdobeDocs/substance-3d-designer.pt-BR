---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale.html"
breadcrumb-title: ''
description: Use o nó Tons de cinza do mapeador de spline para mapear texturas em tons de cinza ao longo de caminhos de spline com parâmetros personalizáveis.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mapeador de spline em tons de cinza
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 0%

---


# Mapeador de spline em tons de cinza

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/spline-mapper-grayscale-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Mapeia uma imagem em tons de cinza de entrada em uma forma primitiva esticada ao longo das linhas de entrada.

A forma primitiva pode ser um plano, um meio-cilindro ou cilindro. Os cilindros podem ser torcidos ao longo da spline para deformar a imagem mapeada adequadamente.

</td>
</tr>
</table>

O nó gera a imagem mapeada como uma imagem em tons de cinza, bem como outras informações, como height, UVs (isto é, coordenadas de imagem) e uma máscara de ID para selecionar cada spline mapeada independentemente.

>[!IMPORTANT]
>
> O resultado pode incluir artefatos indesejados fora do envelope da spline ao usar valores de thickness muito baixos. Esse é um problema conhecido.

>[!NOTE]
>
> Consulte também [Cor do mapeador de spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-color/spline-mapper-color.md).

## Conectores de entrada

<b>Cordas de spline</b> *Cor* As coordenadas dos pontos das splines de entrada codificadas nos canais RGBA de uma imagem colorida:\
<b> R</b> - Posição X\
<b> G</b> - posição Y\
<b> B</b> - Height\
<b>A</b> - Dados empacotados:\
* Sinal: Spline é fechado (negativo) ou aberto (positivo);\
* Valor absoluto: Thickness + 1.

<b>Dados de Spline</b> *Cor* Dados adicionais das splines de entrada codificados nos canais RGBA de uma imagem colorida.\
<b> R</b> - Tangentes X\
<b> G</b> - Tangentes Y\
<b> B</b> - Não Usado\
<b> A</b> - Não Usado

<b>Valor da spline</b> *Inteiro* O número de splines de entrada.

<b>Mapa de cores</b> *Tons de cinza* A imagem em tons de cinza de entrada que deve ser mapeada ao longo das linhas divisórias de entrada.

<b>Mapa de Heights</b> *Escala de cinza* O mapa de height em escala de cinza de entrada que deve ser mapeado ao longo das linhas de spline de entrada.

<b>Twist curve</b> *Tons de cinza* A imagem que descreve uma curva usando os valores da primeira linha de pixels.\
Quando o parâmetro <b>Forma</b> é definido como *Meio Cilindro* ou *Cilindro*, essa entrada é usada para controlar a torção dos UVs em torno da forma. Seu impacto é controlado usando o parâmetro <b>Multiplicador de curva de UVs de torção</b>.\
A curva fornece um perfil para a quantidade de rotação ao longo da spline, onde o primeiro pixel na linha é a rotação no início da spline e o último é a rotação no final. O valor da escala de cinza representa um número de voltas.\
Você pode usar um nó [Curva](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) para criar a curva.

## Conectores de saída

<b>Cor</b> *Tons de cinza* Resultado do mapeamento da imagem colorida de entrada pelas linhas divisórias de entrada, como uma imagem em tons de cinza.

<b>Height</b> *Tons de cinza* O resultado do mapeamento da imagem do Height de entrada nas linhas divisórias de entrada, como uma imagem em tons de cinza.

<b>UV</b> *Cor* Os UVs (isto é, coordenadas) do mapeamento nas linhas de entrada, codificados em uma imagem colorida.

<b>ID</b> *Tons de cinza* Uma máscara das imagens mapeadas ao longo das linhas divisórias de entrada, onde os valores de branco são incrementados em 1 de uma linha divisória para a seguinte, de modo que cada forma possa ser selecionada independentemente.

## Parâmetros

<b>Valor de Segmentos</b> *Inteiro* As splines são simplificadas em segmentos antes que as coordenadas da imagem os atravessem.\
Uma quantidade maior de segmentos resulta em um mapeamento mais suave ao longo das curvas.

<b>UVs de Escala Automática</b> *Booleano* Ajusta o dimensionamento das coordenadas automaticamente para manter uma imagem quadrada ao mapeá-la ao longo das linhas.<b></b>

<b>Escala UV</b> *Flutuante2* Ajusta a escala das coordenadas mapeadas em X (horizontalmente) e Y (verticalmente).\
Valores mais altos resultam em uma imagem lado a lado mais densa.<b></b>

<b>Modo</b> *Inteiro* O método de selecionar as splines ao longo das quais a imagem deve ser mapeada:\
*- Desenhar Lista Spline*: todas as linhas na lista de entrada são usadas;\
*- Desenhar spline única*: apenas a spline com o índice especificado é usada;\
*- Desenhar Intervalo de spline*: Somente as splines cujo índice está incluído no intervalo especificado são usadas.

<b>Desenhar Índice de Spline</b> *Inteiro* (Disponível quando ‘Mode’ estiver definido como ‘Draw Single Spline’)O índice da spline ao longo da qual a imagem deve ser mapeada.

<b>Desenhar Intervalo De Spline</b> *Inteiro2* (Disponível quando ‘Mode’ estiver definido como ‘Draw Spline Range’)O intervalo de índices para as splines ao longo do qual a imagem deve ser mapeada.

<b>Iniciar</b> *Flutuante* Desloca o início da parte da spline que deve ser mapeada.\
O valor representa o comprimento normalizado da spline.

<b>Fim</b> *Flutuante* Desloca a extremidade da parte da spline que deve ser mapeada.\
O valor representa o comprimento normalizado da spline.

<b>Modo de Thickness</b> *Inteiro* O método de definição do thickness da imagem mapeada:\
*- Manual*: Defina o thickness explicitamente com um valor arbitrário;\
*- Da spline*: use o thickness da spline.

<b>Thickness</b> *Flutuante* (Disponível quando ‘Modo de Thickness’ está definido como ‘Manual’)O valor arbitrário para o thickness da imagem mapeada ao longo das splines.<b></b>

<b>Multiplicador de Thickness</b> *Flutuante* (Disponível quando ‘Modo de Thickness’ está definido como ‘De Spline’)Um multiplicador global para o thickness da imagem mapeada ao longo das splines, quando esse thickness é acionado pelo das splines.

<b>Forma</b> *Inteiro* A forma primitiva usada para mapear as coordenadas da imagem ao longo das splines:\
*- Plano*: As coordenadas são mapeadas para um plano plano;\
*- Meio Cilindro*: as coordenadas são mapeadas para um meio cilindro cujo eixo do círculo de base segue a direção da spline;\
*- Cilindro*: as coordenadas são mapeadas para um cilindro cujo eixo do círculo base segue a direção da spline.<b></b>

<b>Multiplicador de Height de cilindro</b> *Flutuante* (Disponível quando “Forma” está definido como “Meio Cilindro” ou “Cilindro”)Um multiplicador para a intensidade da contribuição do height do cilindro na saída do Height.\
Os ajustes de height são cumulativos.

<b>Deslocamento do Height do cilindro</b> *Flutuante* (Disponível quando “Forma” estiver definido como “Meio Cilindro” ou “Cilindro”)\
Desloca o centro do perfil de forma Cilindro ou Meio Cilindro da superfície do spline para um diâmetro abaixo da superfície.

<b>Intensidade de UVs de torção</b> *Flutuante* (Disponível quando “Forma” está definida como “Meio Cilindro” ou “Cilindro”)A torção das coordenadas da imagem ao redor do cilindro, em número de voltas.\
A torção envolve girar o cilindro apenas no final da spline. A rotação é então interpolada ao longo da spline.

<b>Multiplicador de curva de UVs de torção</b> *Flutuador* (Disponível quando “Forma” é definido como “Meio Cilindro” ou “Cilindro”)Um multiplicador para a intensidade da contribuição da entrada do Twist curve para a torção do cilindro.\
A curva fornece um perfil para a quantidade de rotação ao longo da spline, onde o primeiro pixel na linha é a rotação no início da spline e o último é a rotação no final. O valor da escala de cinza representa um número de voltas.

<b>Deslocamento de curva de UVs de torção</b> *Flutuante* (Disponível quando “Forma” estiver definido como “Meio Cilindro” ou “Cilindro”)Aplica um deslocamento global aos valores de rotação fornecidos pelo Twist curve, em número de voltas.

<b>Multiplicador de Height de spline</b> *Flutuante* Ajusta a intensidade da contribuição da entrada do Height de spline para a saída do Height.\
Os ajustes de height são cumulativos.<b></b>

<b>Multiplicador de Height de entrada</b> *Flutuante* Ajusta a intensidade da contribuição da entrada do Mapa de Height para a saída do Height.\
Os ajustes de height são cumulativos.

<b>Correção não quadrada </b>*Booleana* Ajuste as posições e o thickness dos pontos para manter a forma de spline em resoluções não quadradas.\
Isso também afeta a distribuição uniforme.

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineMapperColor-Variant1-Before.jpg" alt="SplineMapperColor-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineMapperGrayscale-Variant1-After.jpg" alt="SplineMapperGrayscale-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](../../../../../../assets/SplineMapperGrayscale-Demo.gif "Exemplo de nó 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 3](../../../../../../assets/SplineMapperGrayscale-Variant1-After1.jpg "Exemplo de nó 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
