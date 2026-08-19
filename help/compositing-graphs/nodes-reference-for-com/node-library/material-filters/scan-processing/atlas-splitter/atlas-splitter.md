---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-splitter.html"
breadcrumb-title: ''
description: Use o nó Atlas splitter para dividir atlas de textura em texturas individuais para processar materiais digitalizados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Splitter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas splitter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---


# Atlas splitter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/atlas-splitter.png "Ícone de nó")

<b>Entrada:</b> Filtros de Material/Processamento de Digitalização

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Usa uma entrada de imagem do atlas e divide todos os elementos separados como *materiais individuais*.

Também pode ser usado para reorganizar e mover todos os elementos em uma grade.

O nó funciona como um aplicativo avançado do nó [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md).

</td>
</tr>
</table>

## Parâmetros

<b>Exibição de grade</b> *Booleana*\
Exibe todas as formas detectadas em uma grade.

<b>Opacidade da grade</b> *Flutuante*\
Define a opacidade das linhas de grade quando a visualização de grade é verdadeira. Opção Depurar

<b>Opacidade da Seleção de Grade</b> *Flutuante*\
Define a Opacidade do realce de Seleção de grade se a Exibição de grade for Verdadeira. Opção Depurar

<b>Escala automática</b> *Booleano*\
Dimensione automaticamente as formas para ajustá-las à célula da grade.

<b>Corte Automático</b> *Booleano*\
Corta automaticamente o tamanho da saída de acordo com a maior forma para minimizar o espaço vazio.

<b>Seleção de forma</b> *Inteiro*\
Na visualização Grade define qual célula é destacada, fora da visualização Grade define qual célula é retornada.

<b>Ignorar Forma Menor Que</b> *Flutuante*\
Ignora formas cujo tamanho diagonal é inferior ao valor especificado.

<b>Rotação Automática</b> *Booleano*\
Gira automaticamente a forma de acordo com a proporção de tamanho da caixa delimitadora.

<b>Rotação</b> *Flutuante*\
Ângulo de rotação da forma global

<b>Formato Normal De Entrada</b> *Inteiro*\
Define o formato da entrada normal. Definir o formato errado levará a um resultado incorreto.

<b>Reduzir Máscara De Opacidade</b> *Inteiro*\
Reduz a Máscara de opacidade para remover ruídos potenciais ou pixels isolados. Impede a detecção de formas indesejadas e também aumenta o desempenho.

<b>Largura de Dilatação</b> *Flutuante*\
Aplica um efeito de dilatação com base na máscara de Opacidade em todos os canais, exceto no Normal e no Height.

<b>Habilitar Entradas Adicionais</b> *Booleano*\
Disponibiliza as entradas e configurações do Usuário 1 e do Usuário 2 para todos os mapas adicionais não cobertos.

<b>Cor de fundo personalizada</b> *Booleana*\
Permite escolher uma cor de fundo personalizada, em vez de uma dilatação do conteúdo da camada.

<b>Cor Do Blog De Cor Base</b> *Flutuante3*\
Cor de fundo personalizada para a cor de base.

<b>Cor De Erro Normal</b> *Flutuante3*\
Cor de fundo personalizada para o mapa normal.

<b>Cor Metálica Do Blog</b> *Flutuante*\
Cor de fundo personalizada para metálico.

<b>Cor De Borrão De Aspereza</b> *Flutuante*\
Cor de fundo personalizada para aspereza

<b>Cor do Blog de Height</b> *Flutuante*\
Cor de fundo personalizada para o Height

<b>Cor De Fundo Do Usuário 1</b> *Flutuante*\
Cor de fundo personalizada para o mapa personalizado do usuário 1

<b>Cor de fundo do usuário 2</b> *Flutuante* Cor de fundo personalizada para o mapa personalizado do usuário 1

## Exemplos
