---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/bent-normal.html"
breadcrumb-title: ''
description: Use o nó Normal torto para gerar mapas normais tortos que levam em conta a oclusão ambiente e a iluminação indireta.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Bent Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dobra normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 2%

---


# Dobra normal

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![Ícone de nó Normal Torto](../../../../../../assets/rt-bent-normal.png "Ícone de nó Normal Torto")

<b>Entrada:</b> *Filtros/Mapa Normal*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

Gera um Mapa normal torto com base em uma entrada de mapa de height. Um mapa Tentado Normal é uma versão especial do [Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) e da [Oclusão Ambiente (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md), gerando um mapa normal com oclusão ambiente incorporada.\
Isso pode ser usado em mecanismos de tempo real para ter a Oclusão ambiente inserida no mapa normal, por exemplo, para reflexões de oclusão mais precisas em metais.

Este nó não deve ser usado em combinação com o mecanismo da CPU (SSE) devido ao tempo de computação.

</td>
</tr>
</table>

## Parâmetros

<b>Usar Tamanho físico</b> *Booleano*\
Alterne para usar as configurações de Tamanho físico para determinar a escala do height.

<b>Tamanho físico</b> *Flutuante3* (Disponível quando <b>Usar Tamanho físico</b> estiver definido como *Verdadeiro*)\
Ajusta a escala do height com base no tamanho físico real da superfície.

<b>Amostras</b> *Inteiro*\
Número de raios utilizados para calcular a curva normal.\
Um resultado mais alto fornece um resultado mais tranquilo e preciso, em detrimento do desempenho.

<b>Escala de Height</b> *Flutuante (Disponível quando Usar Tamanho físico está definido como Falso)*\
Multiplicador da intensidade de entrada do mapa de height.

<b>Distribuição</b> *Inteiro*\
Define o método de distribuição. Afeta a queda em direção a áreas sombreadas.

<b>Distância Máxima</b> *Flutuante*\
Define a distância máxima que os raios podem percorrer para serem ocultados.

<b>Ângulo de Propagação</b> *Flutuante*\
Define o ângulo de propagação para os raios em que serão disparados. Um valor de 1 é um hemisfério completo.

<b>Formato Normal</b> *Inteiro*\
Inverte o canal verde da saída.

## Imagens de exemplo

![Nó normal dobrado - Exemplo 1](../../../../../../assets/bent-normal-ex-1.jpg "Nó normal dobrado - Exemplo 1")
