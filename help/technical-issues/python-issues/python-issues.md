---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/python-issues.html"
breadcrumb-title: ''
description: Solução de problemas de script Python no Substance 3D Designer, incluindo problemas de plug-in e API.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Python issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Problemas de Python
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Problemas de Python

Esta página lista problemas técnicos relacionados à [API Python](../../scripting/scripting.md) da Substance 3D Designer, bem como recursos implementados em Python e oferece etapas de solução de problemas para cada um.

Os recursos implementados em Python incluem as ações [Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[Enviar para](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md) na barra de ferramentas do [Explorer](../../interface/the-explorer-window/the-explorer-window.md), bem como a ferramenta para remover nós não utilizados em gráficos.

## O módulo &#39;QtForPython&#39; falha ao carregar

<b>![(erro)](../../assets/error.svg) Problema</b>

O módulo &#39;QtForPython&#39; em Python falha ao carregar, o que leva a recursos ausentes implementados em Python, como as ações [Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[Enviar para](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md) na barra de ferramentas do [Explorer](../../interface/the-explorer-window/the-explorer-window.md), bem como a ferramenta para remover nós não usados em gráficos.

Além disso, vários [plug-ins Python](../../scripting/plugin-basics/plugin-basics.md) falharão ao carregar ou não funcionarão conforme o esperado.

<b>![(tick)](../../assets/check.svg) Etapas recomendadas</b>

Existe provavelmente um conflito entre a instalação do QtForPython pela Designer e suas dependências, e uma instalação existente no sistema.

Remova qualquer outra instalação de sistema do [QtForPython](https://doc.qt.io/qtforpython-5/index.html) ([PySide2](https://pypi.org/project/PySide2/)) e do [Shiboken2](https://pypi.org/project/shiboken2/).

Alternativamente, em vez de uma instalação do QtForPython em todo o sistema, você pode considerar o uso de *ambientes virtuais* Python ou um *gerenciador de pacotes*, como [rez](https://github.com/AcademySoftwareFoundation/rez).
