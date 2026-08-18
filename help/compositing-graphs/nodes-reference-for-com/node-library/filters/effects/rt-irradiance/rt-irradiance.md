---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-irradiance.html"
breadcrumb-title: ''
description: Use o nó Irradiância RT para calcular informações de irradiância em tempo real a partir da geometria para cálculos de iluminação realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Irradiance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Irradiância RT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 1%

---


# Irradiância RT

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-irradiance.png){width="128px"}

**Entrada:** *Filtros/Efeitos*

**Complexo**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

Gera irradiância rastreada de raio em uma entrada de mapa de height gerada por um mapa de ambiente e um mapa emissivo. Pode ser usado para “assar” a iluminação em uma textura dentro de um gráfico. Usado para iluminação global falsa e brilho.Este nó não deve ser usado em combinação com o mecanismo da CPU (SSE) devido ao tempo de computação. Retorna dois mapas: uma saída de irradiância na qual a irradiância é aplicada às entradas de material, um mapa de irradiância bruto contendo apenas os valores de irradiância calculados.

</td>
</tr>
</table>

## Parâmetros

### Entradas

* **Height:** a *entrada em tons de cinza* Height é a única entrada necessária do slot de material. Sem ele, o nó não funcionará bem.
* **Emissivo:** *A entrada de cor* Emissivo deve estar em um formato em que o preto puro não emita luz, qualquer outro valor colorido emite luz. Alpha é ignorado. Uma conexão com este slot ou o slot Ambiente é necessário para ver qualquer resultado.
* **Ambiente**: *Entrada de cores*\
  Ambiente de iluminação HDR para calcular a irradiância. Uma conexão com este slot ou o slot Emissivo é necessário para ver qualquer resultado.

### Parâmetros

* **Escala do Height**: *0.0 - 1.0*\
  Dimensionar para interpretar height em. Afeta a aparência da cena inteira.
* **Qualidade**: *32 raios, 64 raios, 128 raios*\
  Determina a qualidade do resultado, mas também afeta o desempenho. Menos raios significa mais ruído.
* **Rejeições de Computação**: *Falso/Verdadeiro*\
  Alterna o cálculo de saltos. Afeta a qualidade e a velocidade.
* **Rotação do Ambiente**: *0.0 - 1.0*\
  Gire o ambiente ao redor.
* **Exposição Do Ambiente (EV)**: *-4.0 - 4.0*\
  O valor de exposição a ser usado para o ambiente afeta o brilho total do efeito.
* **Intensidade Emissiva**: *0.0 - 20.0*\
  O multiplicador da entrada Emissiva afeta a força da irradiância do emissivo.
* **Espaço de cores missivo**: *sRGB, Linear*\
  Espaço de cores usado para interpretar a entrada Dissipante.
* **Sombras IBL em Alpha de Irradiância Bruta**: *Falso/Verdadeiro*\
  Alternar se deseja adicionar Sombras ao
* **Polarização de LOD Emissiva**: *-1.0 - 1.0* Ajuste a qualidade da irradiância emissiva. Um valor mais baixo significa mais ruído.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-irr-03-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/rt-irr-01-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/rt-irr-02-1.jpg" width="300px"/></div> |
| --- | --- | --- |
|  |  |  |
