---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/scripting/packaging-plugins.html"
breadcrumb-title: ''
description: Saiba como empacotar plug-ins Python para o Substance 3D Designer para distribuição e instalação.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Packaging plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Empacotando plug-ins
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 3%

---


# Empacotando plug-ins

## Conteúdo do pacote de plug-ins

Os pacotes são um único arquivo, internamente um arquivo zip, que contém um arquivo **pluginInfo.json** com metadados sobre o plug-in,

o código do plug-in e outros arquivos ou recursos necessários para o plug-in funcionar.

**Entradas PluginInfo.json:**

| Entrada | Descrição | Valor padrão | Observações |
| --- | --- | --- | --- |
| metadados\_format\_version | O formato do arquivo de metadados. | 1 | Obrigatório.Atualmente deve ser definido como 1. |
| nome | O nome do plugin. |  | Obrigatório. Deve corresponder ao nome do módulo Python que contém o código do plug-in |
| versão | A versão do plugin. |  | Opcional. |
| autor | O autor do plug-in. |  | Opcional. |
| email | O e-mail do autor do plug-in. |  | Opcional. |
| min\_designer\_version | Versão mínima do aplicativo exigida pelo plug-in para funcionar. | 2019.2 | Opcional. |
| plataforma | Plataforma na qual o plug-in é executado. | qualquer | Opcional.Para plug-ins que contenham código compilado, esta entrada pode ser usada para desativar o plug-in em plataformas não compatíveis.Valores possíveis: win, linux, osx, any. |

## Criando um novo projeto de pacote de plug-ins

Fornecemos um projeto de modelo do [Cookiecutter](https://cookiecutter.readthedocs.io/en/latest/) para simplificar a criação de projetos de pacote de plug-ins.

Você pode usá-lo diretamente ou modificá-lo para suas próprias necessidades.

O modelo pode ser encontrado no diretório do aplicativo, em <b>plugins/tools/pkgplugintemplate</b>.

1. <b>Instale o Python se ele ainda não estiver instalado no sistema</b>

   O Cookiecutter é compatível com Python 2 e Python 3
1. <b>Instale o Cookiecutter se ainda não o tiver</b>

   Normalmente isto pode ser feito usando pip:

   ```
   pip install cookiecutter
   ```


   Para formas alternativas de instalar o Cookiecutter ou para obter mais informações sobre o Cookiecutter, consulte a documentação em <https://cookiecutter.readthedocs.io/en/latest/installation.html>
1. <b>Criar um novo projeto de pacote de plug-ins</b>

   Em uma janela de terminal, execute:

   ```
   cookiecutter path/to/pkgplugintemplate -o path/to/new/project
   ```


   Preencha as informações necessárias. O novo projeto será criado no diretório especificado.
1. <b>Empacotar seu plug-in após a conclusão do desenvolvimento</b>

   Em uma janela de terminal, execute:

   ```
   python makepackage.py
   ```

1. O pacote de plug-ins será gerado no diretório de compilação
