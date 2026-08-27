---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-index.html"
breadcrumb-title: ''
description: Use o nó Flood Fill para indexar para preencher regiões com valores de índice para criar padrões numerados e rotulados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Index
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill para Índice
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 2%

---


# Flood Fill para Índice

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-index.png){width="200px"}

## Flood Fill para Índice

**Entrada:** *Filtros/Efeitos*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Flood Fill para Índice converte cada célula de Flood Fill em um valor de acordo com seu número de índice, começando com 0 no canto superior esquerdo. Ele pode ser usado para retornar tons de tons de cinza em uma forma normalizada (0,0 a 1,0, dividido por tantas células quantas encontradas por Flood Fill) ou como um valor não bloqueado HDR (0 a n onde n é o número de células).

Além disso, o Flood Fill para Índice usa [valores](../../../../../values-compositing-graphs/values-in-substance-compositing-graphs.md), retornando a quantidade de formas encontradas e a tabela de dados interna opcional.

### Entradas

* **Flood Fill Bbox**: *Entrada de cores* Mapa de entrada de Flood Fill padrão. Obrigatório.
* **Informações de Forma Especial**: a *Entrada de Cores* Mapa de Flood Fill extra precisa ser habilitada explicitamente no nó de Flood Fill anterior e precisa ser conectada!.

### Parâmetros

* **Saída**: *Normalizado, Inteiro* Determine se a saída está no intervalo 0-1 LDR ou no intervalo 0-n HDR.
* **Ignorar Forma Menor que**: *0.0 - 1.0* Valor de tolerância para ignorar formas pequenas.
* **Mostrar Tabela de Dados de Flood Fill**: *Falso/Verdadeiro* Retorna dados extras (depuração) para uso avançado.

## Exemplos

![](../../../../../../assets/flood-fill-ex02.jpg)

</td>
</tr>
</table>
