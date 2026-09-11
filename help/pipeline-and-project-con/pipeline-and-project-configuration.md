---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration.html"
breadcrumb-title: ''
description: Defina as configurações de pipeline e projeto no Substance 3D Designer para otimizar o fluxo de trabalho e a saída.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Configuração de Pipeline e Projeto
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea2e2d76d225a0e17c84c3312934f62aa5ef3915
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---


# Configuração de Pipeline e Projeto

O Substance 3D Designer tem um sistema eficiente para configurar o aplicativo para o uso de pipeline. Por meio de um sistema avançado de arquivos hierárquicos “**Projeto**”, o aplicativo pode ser configurado instantaneamente para os padrões de Estúdio ou Projeto, com todas as configurações e conteúdo da Biblioteca sob controle de versão. O principal objetivo do sistema é centralizar todas as configurações relevantes para o pipeline, mas ainda permitir que várias configurações substituam e expandam umas às outras.

>[!WARNING]
>
> Este sistema não se destina a usuários únicos com requisitos mais simples, mas sim a *estúdios com grandes projetos e equipes* e uma necessidade maior de organização. Para fazer pleno uso deste sistema, uma quantidade razoável de planejamento e preparação, bem como um certo grau de configuração automatizada é recomendado!

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Hierarquia de arquivos de configuração

O Designer tem três camadas ou arquivos de configuração, cada um com uma finalidade diferente. No Windows, todos os arquivos estão localizados em *~User\AppData\Local\Adobe\Adobe Substance 3D Designer.*

A imagem ilustra a relação entre os diferentes arquivos na configuração padrão do Designer, após uma nova instalação.

</td>
<td style="border: 0;" valign="top">

![Hierarquia de arquivos de configuração](pipeline-and-project-configuration.resources/filestructureoverview.png "Hierarquia de arquivos de configuração")

</td>
</tr>
</table>

* <b>[User\_Preferences.XML](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md)</b> contém configurações gerais de programa, das quais todas, exceto uma, não são relevantes para pipelines de projeto. Este arquivo é único e não pode ser trocado, o Designer é codificado para utilizar exatamente este arquivo.\
  Ele contém uma única referência a um arquivo de configuração.
* <b>[Default\_Configuration.SBSCFG](../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md)</b> pode ser trocado para outros arquivos SBSCFG com nomes diferentes, mas apenas um arquivo SBSCFG pode ser usado ao mesmo tempo.\
  Ele contém várias referências a arquivos de projeto. *Observe que, para a configuração padrão, esses arquivos não são explicitamente definidos, mas codificados!*
* <b>[Arquivos Project.SBSPRJ](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)</b> contêm configurações relevantes para projeto/pipeline. Vários projetos podem ser definidos em uma hierarquia, substituindo ou expandindo o projeto definido anteriormente.

## Configuração de pipeline da Designer

Cada tipo de arquivo é explicado com mais detalhes em páginas secundárias desta página, mas a breve visão geral de como definir idealmente uma configuração personalizada para o Designer é a seguinte:

1. <b>Identifique e agrupe as configurações a serem adicionadas aos arquivos do Project.</b> Isso é diferente para cada estúdio e requer uma certa quantidade de planejamento!\
   Em quase todos os casos, pelo menos dois projetos devem ser definidos: um para padrões globais de estúdio (como modelos padrão, arquivos sombreadores, configurações de cozimento) e outro com conteúdo mais específico, como conteúdo da biblioteca. Se você tiver projetos diferentes em execução simultaneamente, talvez queira criar várias configurações de projeto para cada um (ou seja, um total de 3 ou mais).
1. <b>Crie os [arquivos SBSPRJ](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) relevantes e coloque-os, assim como seu conteúdo, sob controle de versão.</b> É altamente recomendável separar o pipeline e o conteúdo da biblioteca do Designer do conteúdo e dos recursos reais do projeto (modelos 3D, texturas, código) criando um *repositório separado* para ele.
1. <b>Crie um arquivo [&#x200B; configuração SBSCFG](../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) listando todos os arquivos de projeto, coloque-o no controle de versão</b>. Se você tiver vários projetos, poderá criar uma configuração para cada projeto.
1. <b>Configure [User\_Preferences.xml](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md) de cada usuário para referenciar seu arquivo de configuração relevante.</b>\
   Cada usuário pode fazer isso manualmente ou criar um script para isso injetando linhas no arquivo XML. [Mais informações na página relevante](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md).
