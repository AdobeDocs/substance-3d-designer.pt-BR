---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-irradiance.html"
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
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 4%

---


# Irradiância RT

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](rt-irradiance.resources/rt-irradiance.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera irradiância rastreada de raio em uma entrada de mapa de altura gerada por um mapa de ambiente e um mapa de emissivo. Pode ser usado para “fazer bake” a iluminação em uma textura dentro de um gráfico. Usado para iluminação global falsa e brilho.Este nó não deve ser usado em combinação com o mecanismo da CPU (SSE) devido ao tempo de computação. Retorna dois mapas: uma saída de irradiância na qual a irradiância é aplicada às entradas de material, um mapa de irradiância bruto contendo apenas os valores de irradiância calculados.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Height</b> <i>Entrada em tons de cinza</i> | O height é a única entrada necessária do slot de material. Sem ele, o nó não funcionará bem. |
| <b>Emissivo</b> <i>Entrada de cores</i> | O emissivo deve estar em um formato em que o preto puro não emita luz e qualquer outro valor colorido emite luz. Alpha é ignorado. Uma conexão com este slot ou o slot Ambiente é necessário para ver qualquer resultado. |
| <b>Ambiente</b> <i>Entrada de cores</i> | Ambiente de iluminação do HDR para calcular a irradiância. Uma conexão com este slot ou o slot de Emissivo é necessária para ver qualquer resultado. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Escala de Height</b> <i>0.0 - 1.0</i> | Dimensionar para interpretar height em. Afeta a aparência da cena inteira. |
| Qualidade <b>1</b> <i>32 raios, 64 raios, 128 raios</i> | Determina a qualidade do resultado, mas também afeta o desempenho. Menos raios significa mais ruído. |
| <b>Rejeições de Computação</b> <i>Falso/Verdadeiro</i> | Alterna o cálculo de saltos. Afeta a qualidade e a velocidade. |
| <b>Rotação do ambiente</b> <i>0.0 - 1.0</i> | Gire o ambiente ao redor. |
| <b>Exposição do Ambiente (EV)</b> <i>-4.0 - 4.0</i> | O valor de exposição a ser usado para o ambiente afeta o brilho total do efeito. |
| <b>Intensidade de Emissivo</b> <i>0.0 - 20.0</i> | O multiplicador da entrada Emissiva afeta a força da irradiância do emissivo. |
| <b>Espaço da Cor do Emissivo</b> <i>sRGB, Linear</i> | Espaço de cores usado para interpretar a entrada Dissipante. |
| <b>Sombras IBL em Alpha de Irradiância Bruta</b> <i>Falso/Verdadeiro</i> | Alternar se deseja adicionar Sombras ao |
| <b>Polarização de carga de Emissivo</b> <i>-1.0 - 1.0</i> | Ajuste a qualidade da irradiância do emissivo. Um valor mais baixo significa mais ruído. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irr-03-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irr-01-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irr-02-1.jpg" />
        </td>
    </tr>
</table>
