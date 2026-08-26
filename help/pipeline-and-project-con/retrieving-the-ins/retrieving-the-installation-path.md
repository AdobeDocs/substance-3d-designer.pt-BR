---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/pipeline-and-project-configuration/retrieving-the-installation-path.html"
breadcrumb-title: ''
description: Saiba como recuperar o caminho de instalação do Substance 3D Designer para fins de script e automação.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Retrieving the installation path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recuperação do caminho de instalação
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 6%

---


# Recuperação do caminho de instalação

Esta página reagrupa informações sobre maneiras de recuperar o caminho de instalação do [Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html), dependendo da versão e da plataforma.

## Windows

### Creative Cloud para desktop

1. Abrir <b>editor do Registro do Windows</b> (regedit)
1. Navegue até a chave de registro: <b>HKEY\_LOCAL\_MACHINE\Software\Microsoft\Windows\CurrentVersion\App Paths\&lt;/b>
1. Abra a subchave denominada <b>Adobe Substance 3D Designer.exe</b>
1. O valor da chave contém o caminho para o executável do aplicativo no qual ela está instalada

>[!NOTE]
>
> Esta chave do registro está disponível somente desde a versão 11.2.\
> Para versões mais antigas, o caminho de instalação pode ser recuperado das associações de arquivos em HKEY\_CURRENT\_USER\Software\Microsoft\Windows\CurrentVersion\ Explorer\FileExts

### Substance edition (independente)

1. Abrir <b>editor do Registro do Windows</b> (regedit)
1. Navegue até a chave do Registro: <b>HKEY\_LOCAL\_MACHINE\ SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall</b>
1. Localize a subchave correspondente à <b>AppID</b> da versão do seu aplicativo (veja a tabela abaixo)
1. O valor da chave contém o caminho para o local de instalação do aplicativo

| Versão | AppId |
| --- | --- |
| **Versão 5.x** | {25E7D16D-1FBA-49EA-BF36-E2D6B20A9206} |
| **Versão 6.x** | {09a302b1-8da8-4f62-b0cb-a208faa210f9} |
| **Versão 7.x (2017.x) para 11.1** | {e9e3d6d9-3023-41c7-b223-11d8fdd691b9} |
| **Versão 11.2 (ou mais recente)** | {662bb79f-5616-44e6-a84d-b3d6abebe002} |

### Edição de vapor

O aplicativo é instalado na subpasta steamapps/common/ da pasta de instalação do Steam.

## macOS

No Mac, o aplicativo é instalado no seguinte:

| Versão | Caminho |
| --- | --- |
| **11.2 ou mais recente** | **/Aplicativos/Adobe Substance 3D Designer.app** |
| **Herdado** | **/Aplicativos/Substance Designer.app** |

## Linux

No Linux, o pacote rpm é instalado no seguinte caminho:

| Versão | Caminho |
| --- | --- |
| **11.2 ou mais recente** | **/opt/Adobe/Adobe\_Substance\_3D\_Designer** |
| **Herdado** | **/opt/Allegorithmic/Substance\_Designer** |
