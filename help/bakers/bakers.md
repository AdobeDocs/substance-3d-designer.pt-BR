---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/bakers.html"
breadcrumb-title: ''
description: Saiba como usar os padeiros do Substance 3D Designer para computar informações baseadas em malha em arquivos de textura.
helpx_creative_field: ""
helpx_description: Designer > Bakers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Baking
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---


# Baking

Preparação refere-se à ação de **transferência de informações baseadas em malha para texturas**. Essas informações são lidas por sombreadores e/ou filtros de Substance para gerar efeitos ou texturas mais avançados.

>[!NOTE]
>
> Para saber mais sobre panificação, consulte a [Documentação de panificação](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/home).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

A janela de cozimento pode ser acessada por meio do arquivo de malha na janela do [Explorer](../interface/the-explorer-window/the-explorer-window.md). Clique com o botão direito do mouse no nome da malha e escolha “**Informações do modelo de cozimento**” para abrir a janela de cozimento.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![ opção&#39;Informações do modo de cozimento&#39; no menu contextual do recurso de cena 3D](../assets/sd-mesh-right-click.png " opção&#39;Informações do modo de cozimento&#39; no menu contextual do recurso de cena 3D")

</td>
</tr>
</table>

![Janela de cozimento](../assets/sd-window-overview.png "Janela de cozimento")

## Visão geral

A janela de cozedura de é dividida em vários painéis que são descritos abaixo.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Elementos para assar

Este painel controla qual parte da malha de baixo-poli será usada para realizar a cozedura.

Ela lista a geometria encontrada dentro do arquivo de malha de baixo polígono. Por padrão, a lista é baseada nos materiais individuais encontrados no arquivo, mas pode ser alterada para submalhas quando relevante. Você pode desmarcar os elementos que devem ser ignorados durante o processo de cozimento.

</td>
<td style="border: 0;" valign="top">

![](../assets/sd-mesh-selection.png)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Saída

Esse painel controla onde a textura assada será localizada.

</td>
<td style="border: 0;" valign="top">

![](../assets/sd-output.png)

</td>
</tr>
</table>

| *Parâmetro* | *Descrição* |
| --- | --- |
| **Método** | Controla como as texturas assadas serão armazenadas com o pacote de Substance.Valores possíveis:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Incorporada</strong>: a textura cozida é armazenada em uma subpasta próxima ao pacote de Substance com nome específico.</li><li data-preserve-html="true"><strong>Vinculado</strong> (padrão): a textura feita bake é armazenada na pasta definida e referenciada no Substance empacotado.</li></ul> |
| **Pasta** | Local das texturas feitas bake quando salvas. Clique no botão de três pontos para abrir uma caixa de diálogo de arquivo e escolher a pasta de exportação. Uma marca de seleção estará visível à direita para indicar se a pasta realmente existe ou não. |
| **Nome** | Convenção de nomenclatura das texturas feitas bake. Clique no botão de três pontos para abrir um menu suspenso e inserir outros espaços reservados (nome do banco, personalizado, material, malha). |
| **Amostra** | Simule um nome de arquivo para testar a convenção de nomenclatura. |
| **Colocar Recurso em uma Pasta Específica do Mesh** | Se ativado, o textura feito bake será salvo dentro de uma pasta nomeada como arquivo de malha. |

### Malhas de alta definição

Este painel controla a lista de malha de alto polígono e as configurações relacionadas. Consulte os [parâmetros comuns](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/common-parameters) para obter mais informações.

![Malhas de alta definição](../assets/sd-high.png "Malhas de alta definição")

### Valores padrão

Consulte os [parâmetros comuns](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/common-parameters) para obter mais informações.

![Valores padrão](../assets/sd-default-values.png "Valores padrão")

### Lista de renderização e configurações de baker

A **lista de renderização de Baker** é onde você pode escolher qual textura feita bake deseja gerar. Por padrão, a lista está vazia.

* **Adicionando um novo baker:** Clique no botão “Adicionar Baker”.
* **Removendo um baker:** selecione o baker na lista e clique no botão “Excluir baker”.
* **Movendo um baker para o topo:** selecione o baker na lista e clique no botão “Puxar para o topo”.
* **Movendo um baker para baixo:** selecione o baker na lista e clique no botão “Empurrar para baixo”.

Cada baker no herda por padrão os Valores padrão (veja acima). O tamanho (resolução), por exemplo, pode ser substituído clicando na célula na linha do padeiro. Isso é verdadeiro para as outras configurações na linha.

Ao clicar em um padeiro na lista, a visualização Parâmetros Baker atualizará com seus parâmetros específicos.

Para saber mais sobre os parâmetros específicos, consulte: [Configurações de preparadores](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/bakers-settings).

![Lista de renderização de preparadores](../assets/sd-baker-list.png "Lista de renderização de preparadores")
