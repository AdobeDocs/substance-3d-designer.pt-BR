---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-graph-view/graph-items/comment.html"
breadcrumb-title: ''
description: Adicione comentários aos gráficos do Substance 3D Designer para documentar seu fluxo de trabalho e explicar as conexões de nós.
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view > Graph items > Comment
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Comentário
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---


# Comentário

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Ícone de comentário](../../../../assets/graphatomic-comment_1.png "Ícone de comentário")

</td>
<td width="100.00%" style="border: 0;" valign="top">

Um comentário é simplesmente um pedaço de texto flutuante que pode ser colocado em qualquer lugar de um gráfico.

Destina-se a anotar e explicar partes de um gráfico. Sua propriedade <b>Description</b> contém o texto que está sendo exibido.

</td>
</tr>
</table>

>[!NOTE]
>
> Os comentários têm quebra de linha automática, o que visa minimizar seu impacto em um gráfico.

## Criação de comentários

O tipo padrão de comentário é colocado independentemente dos nós no gráfico.

Ela pode ser criada das seguintes maneiras:

+++Menu Nó
Pressione a <b>Barra de espaço</b> no modo de exibição Gráfico para abrir o <b>menu Nó</b> e selecione o item &#39;Comentário&#39; na lista.

Digite “comment” no campo de pesquisa para mostrar o item e encontrá-lo mais rapidamente.

+++

+++Atalho
Se um atalho de teclado estiver mapeado para o item &#39;Comentário&#39; nas [Preferências](../../../../interface/preferences-window/preferences-window.md), pressione esse atalho quando o Modo de Exibição de Gráfico tiver foco.

+++

+++Menu contextual
Na Exibição de Gráfico, pressione <b>RMB</b> em qualquer objeto ou em um espaço vazio e selecione a opção <b>Adicionar Comentário</b>.

+++

+++Barra de ferramentas Gráfico
Na barra de ferramentas Exibição de Gráfico, clique no botão &#39;Comentário&#39; na <b>Paleta de nós</b>.

+++

+++Biblioteca
Na Biblioteca, selecione a categoria <b>Itens de gráfico</b> e arraste e solte o item &#39;Comentário&#39; no Modo de Exibição de Gráfico.

+++

>[!TIP]
>
> Quando um comentário é criado, sua propriedade “Description” ganha foco automaticamente para que você possa editar imediatamente o texto do comentário.

## Comentários com pai

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Um comentário com parentesco é um comentário *anexado a um nó específico* no gráfico para que, quando o nó for movido, o comentário siga e, quando o nó for excluído, o comentário seja excluído junto com ele.

Os comentários criados quando um nó *único* está selecionado no momento ou por meio do menu contextual de um único nó têm como pai esse nó.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Comentários: comentários com parentesco](../../../../assets/graph-comment_parented.gif "Comentários: comentários com parentesco")

</td>
</tr>
</table>

## formatação HTML

O texto pode ser formatado usando tags HTML. Essa formatação é alternada usando o botão ![](../../../../assets/graph-frames_html-markup-button.png) <b>marcação de HTML</b> na propriedade <b>Descrição</b> do comentário.

>[!TIP]
>
> Saiba mais sobre este recurso na seção <b>Descrição</b> da documentação de [Quadros](../../../../interface/the-graph-view/graph-items/frame/frame.md).

![Comentários: marcação HTML](../../../../assets/graph-comment_html-markup.gif "Comentários: marcação HTML")
