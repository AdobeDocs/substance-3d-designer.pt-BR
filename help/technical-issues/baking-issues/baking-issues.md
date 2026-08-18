---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/technical-issues/baking-issues.html"
breadcrumb-title: ''
description: Encontre etapas de solução de problemas técnicos relacionados a texturas de cozimento no Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Baking issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Problemas de cozimento
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# Problemas de cozimento

Esta página lista problemas técnicos relacionados às [texturas de cozimento](../../bakers/bakers.md) no Substance 3D Designer e oferece etapas de solução de problemas para cada um.

## Nesta página

&#39;Corresponder por nome&#39; não funciona

## &#39;Corresponder por nome&#39; não funciona

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>![(erro)](../../assets/error.svg) Problema</b>

Quando a opção “Corresponder” está definida como “Por nome da malha”, a correspondência não parece ser aplicada ou não está consistentemente em todos os objetos da cena.

<b>![(tick)](../../assets/check.svg) Etapas recomendadas</b>

Nas versões 14.1 e anteriores do Designer, os objetos de poli baixo e poli alto eram combinados usando o nome dos objetos *pai* deles - na maioria dos casos, a transformação pai.

Desde o Designer 15.0, o nome dos objetos *geometria* são usados diretamente.

</td>
<td style="border: 0;" valign="top">

![Objeto de geometria e seu pai na árvore de cena](../../assets/sceneTree_objectsName.png "Objeto de geometria e seu pai na árvore de cena"){zoomable="yes"}

</td>
</tr>
</table>

Há dois caminhos que você pode seguir para obter a correspondência esperada:

* Ajuste o nome dos objetos de geometria para aplicar nomes correspondentes.
* Reverta para o comportamento ou versões anteriores do Designer ajustando a opção [&#39;Modo de filtragem de nome&#39;](../../interface/preferences-window/project-settings/project-settings.md) nas configurações do Projeto:
  1. Acesse Editar > Preferências > Projetos
  1. Selecione o último arquivo de projeto na lista
  1. Abaixo da lista de arquivos de projeto, selecione a guia “Padeiros”
  1. Defina o &#39;Modo de filtragem de nome&#39; como &#39;Nome do pai (legado)
