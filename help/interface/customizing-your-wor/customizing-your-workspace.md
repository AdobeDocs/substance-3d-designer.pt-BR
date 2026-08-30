---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/interface/customizing-your-workspace.html"
breadcrumb-title: ''
description: Saiba como personalizar seu espaço de trabalho no Substance 3D Designer para otimizar suas preferências de fluxo de trabalho e layout.
helpx_creative_field: ""
helpx_description: Designer > Interface > Customizing your workspace
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Personalizar sua área de trabalho
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 0%

---


# Personalizar sua área de trabalho

Esta página apresenta as maneiras de organizar os painéis na interface de usuário do [Adobe Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html) e aproveitar seus recursos para aprimorar seus fluxos de trabalho.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

## Menu Janelas

Esse menu permite gerenciar os principais elementos da interface do usuário do Designer. Cada opção está descrita na seção <b>Windows</b> de [esta página](../the-main-toolbar/the-main-toolbar.md) sobre a barra de ferramentas principal. Aqui, forneceremos conceitos adicionais relacionados a este menu.

### Exibir/ocultar uma exibição

Para exibir ou ocultar um item de interface específico, clique em seu nome no menu *Janelas*. Os itens exibidos têm uma marca de seleção ![](customizing-your-workspace.resources/image2015-12-17-10-43-24.png).

### Preencher um encaixe com uma exibição

No Designer, um encaixe é um *contêiner separado de seu conteúdo*. Isso significa que um encaixe da <b>Biblioteca</b> pode existir e estar vazio, pois não contém exibição da *Biblioteca*.

As opções <b>Novo Explorer</b>, <b>Nova exibição 3D</b> e <b>Nova exibição Biblioteca</b> criam exibições, que serão colocadas de acordo com o estado atual da interface do usuário:

* Se um encaixe vazio estiver disponível, o novo modo de exibição será criado *dentro dele*
* Se as docas vazias *não* estiverem disponíveis, uma *nova doca* será criada para manter a nova exibição

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Menu do Windows](customizing-your-workspace.resources/windows-menu-1.png "Menu do Windows")

</td>
</tr>
</table>

## Redimensionando encaixes

As docas podem ser redimensionadas movendo qualquer uma de suas bordas. Outras docking stations serão redimensionadas dinamicamente para se ajustarem.

![Redimensionando docas](customizing-your-workspace.resources/interface-customisation-resize.gif "Redimensionando docas")

## Movendo docas

Qualquer encaixe pode ser movido pela janela principal usando sua *barra de título*. Dependendo do local para o qual o encaixe é movido, ele será redimensionado para se ajustar.

![Movendo docas](customizing-your-workspace.resources/interface-customisation-move.gif "Movendo docas")

## Tabulação de encaixes

As docas podem ser empilhadas em tabulações. Isso é útil para salvar o espaço na tela ou agregar exibições que se relacionam entre si de alguma forma.

Você pode tabular encaixes movendo um encaixe usando sua barra de título *sobre um encaixe existente*, como encaixes que não são redimensionados nem movidos, mas um *quadro* aparece ao redor do encaixe de destino.

![Docas de tabulação](customizing-your-workspace.resources/interface-customisation-tab.gif "Docas de tabulação")

## Desencaixando

Um encaixe pode ser desencaixado em uma *janela flutuante*, que pode ser redimensionada e movida para fora da janela principal, inclusive para outro monitor.

Isso pode ser feito de duas maneiras:

* Movendo o encaixe usando sua *barra de título* e colocando-o *fora da janela principal* ou em uma área da janela principal que *não é um encaixe*. Você pode reencaixar este encaixe movendo-o em outro encaixe *na janela principal* ou clicando no botão <b>![](customizing-your-workspace.resources/dock-icons-redock.png) Reencaixar</b>;
* Clique no botão <b>![](customizing-your-workspace.resources/dock-icons-undock.png) Desencaixar</b>. Um encaixe desencaixado com este método pode *apenas* ser reencaixado clicando no botão <b>![](customizing-your-workspace.resources/dock-icons-redock.png) Reencaixar</b>.

![Desencaixando](customizing-your-workspace.resources/interface-customisation-undock.gif "Desencaixando")

## Maximização de encaixes

Qualquer encaixe pode ser maximizado para se ajustar à área ou à sua *janela pai*:

* As docas encaixadas se espalharão por toda a área da *janela principal*, excluindo a barra de título, a barra de ferramentas principal e a barra de status
* As docas desencaixadas se espalharão por toda a *tela*

As docking stations podem ser maximizadas de duas maneiras:

* Colocando o *cursor sobre o encaixe* e pressionando o pressionamento da tecla <b>Shift+Espaço</b>
* Clique no botão <b>![](customizing-your-workspace.resources/dock-icons-maximise.png) Maximizar</b>

As docking stations maximizadas podem ser minimizadas no tamanho e local em que elas estavam *antes de serem maximizadas*. Isso pode ser feito de três maneiras:

* Colocando o *cursor sobre o encaixe* e pressionando o pressionamento da tecla <b>Shift+Espaço</b>
* Clicando no botão <b>![](customizing-your-workspace.resources/dock-icons-minimise.png) Minimizar</b>
* Abrindo o menu <b>Janelas</b> e selecionando a opção <b>Não maximizar janela</b>

>[!NOTE]
>
> Somente *um* encaixe pode ser maximizado por vez.

>[!IMPORTANT]
>
> Quando um encaixe é maximizado, alguns comportamentos de interface podem diferir:
> 
> * As docking stations que aparecem/atualizam automaticamente farão isso em segundo plano (por exemplo, Propriedades, Visualização 2D)
> * Os itens de menu estão *desabilitados* no menu **Janelas**
> * Os botões estão *desabilitados* na barra de título do Dock
> * Um encaixe maximizado na janela principal *não pode ser movido* usando sua barra de título

![Maximizando encaixes](customizing-your-workspace.resources/interface-customisation-maximise.gif "Maximizando encaixes")

## Fixação de encaixes

Fixar um encaixe *evita que ele seja populado* com outro conteúdo ou uma exibição diferente.

Quando um encaixe é fixado, qualquer conteúdo futuro que deve ser exibido em seu será, em vez disso, *criado um novo encaixe* para hospedá-lo. Esse novo encaixe não será fixado e, portanto, poderá atualizar e hospedar novo conteúdo.

Para fixar um encaixe, clique no botão ![](customizing-your-workspace.resources/dock-icons-pin.png) <b>Fixar</b>. Depois, você pode *desafixar* usando o botão ![](customizing-your-workspace.resources/dock-icons-pinned.png) <b>Desafixar</b> para torná-lo mais uma vez *disponível* para hospedar qualquer conteúdo novo.

*Mais de um* encaixe pode ser fixado por vez, incluindo vários encaixes do *mesmo tipo*.

A fixação de encaixes proporciona os seguintes recursos:

* Exibição e ajuste de propriedades de vários nós ao mesmo tempo
* Exibição simultânea de dois bitmaps
* Trabalhar em vários gráficos simultaneamente

![Fixando docas](customizing-your-workspace.resources/interface-customisation-pin.gif "Fixando docas")

## Fechando docas

Qualquer encaixe pode ser fechado clicando no botão ![](customizing-your-workspace.resources/dock-icons-close.png) <b>Fechar</b>.

## Redefinição do layout da interface

Toda a interface de usuário pode ser redefinida para seu layout padrão abrindo o menu <b>Janelas</b> e selecionando a opção <b>Redefinir layout</b>.

Seu estado de exibição também será redefinido, o que significa que as docas fechadas podem ser *reabertas* (por exemplo, exibição 3D) e as docas exibidas podem ser *fechadas* (por exemplo, Console, Gerenciador de dependências, docas criadas por plug-ins).

![Redefinir layout](customizing-your-workspace.resources/interface-customisation-reset.gif "Redefinir layout")
