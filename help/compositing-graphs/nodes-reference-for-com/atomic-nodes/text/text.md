---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/text.html"
breadcrumb-title: ''
description: Use o nó Texto para gerar texturas de texto com fontes e estilos personalizáveis para criar padrões baseados em texto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Text
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Texto
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b6f65bd88f3c83bf6682c7bca91615166389a91
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---


# Texto

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: Texto](text.resources/comp_text_1.png "Nó atômico: Texto"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

O nó Texto fornece uma maneira de colocar o texto criado pelo usuário em seus gráficos. Os usuários também podem selecionar configurações como Fonte, Alinhamento e rotação para personalizar o posicionamento do texto.

O nó Texto é muito poderoso e a única maneira de inserir texto facilmente. Pode ser um pouco complicado de usar, pois o posicionamento sempre acontece em uma tela quadrada e limitada e as fontes são orientadas por uma lista externa definida pelo sistema.

</td>
</tr>
</table>

Somente há suporte para Truetype (.ttf) e determinadas fontes Opentype. Se alguma fonte estiver ausente na lista, esse é provavelmente o motivo. <b>As fontes não podem ser expostas como um parâmetro.</b>

Quando um gráfico que usa texto é publicado no sbsar, a fonte é incorporada ao pacote, assim como com bitmaps e outros recursos, para garantir o funcionamento em todos os sistemas e aplicativos.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Conectores de saída

</td>
<td style="border: 0;" valign="top">

### Exemplos

</td>
</tr>
</table>

## Parâmetros

|  |  |
| --- | --- |
| <b>Modo de cores</b> *Booleano* | Alterna entre uma imagem em tons de cinza e uma imagem colorida de saída. |
| <b>Texto</b> *Cadeia de Caracteres* | Determina a descrição do texto. |
| <b>Fonte</b> *Cadeia de Caracteres* | O recurso de fonte usado para processar o texto. |
| <b>Tamanho da fonte</b> *Flutuante* | O tamanho da fonte do texto em pontos. |
| <b>Alinhamento</b> *Inteiro* | Define o alinhamento do texto como esquerda, centro (padrão) ou direita. |
| <b>Transformação</b> *Flutuante4* | A matriz de transformação 2x2 aplicada ao texto renderizado. |
| <b>Posição</b> *Flutuante2* | A posição do texto na imagem de saída. |
| <b>Fundo</b> *Flutuante/Flutuante4* | A cor de plano de fundo da imagem de saída. |
| <b>Cor da fonte</b> *Flutuante/Flutuante4* | A cor do texto. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Fundo</b> *Tons de Cinza/Cor* PRIMÁRIO | A cor de plano de fundo da imagem de saída. |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Tons de cinza/Cor* |  |

## Exemplos

*Em breve.*
