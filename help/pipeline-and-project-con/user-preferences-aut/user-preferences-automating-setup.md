---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/user-preferences-automating-setup.html"
breadcrumb-title: ''
description: Saiba como automatizar a configuração de preferências do usuário no Substance 3D Designer para otimizar a configuração do fluxo de trabalho.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > User Preferences - Automating Setup
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Preferências do usuário - Automatizando a configuração
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---


# Preferências do usuário - Automatizando a configuração

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

O arquivo user\_preferences.xml contém todas as configurações específicas do usuário que estão fora das definidas em uma [Configuração de Projeto](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md). Eles se relacionam principalmente a configurações específicas de interface e desempenho.

A única configuração relevante a ser alterada é o [Arquivo de Configuração](../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md), que contém uma lista de projetos. Isso pode ser feito de algumas maneiras, conforme listado abaixo.

Como alternativa, você pode ignorar completamente a modificação das Preferências do Usuário e fazer uma substituição baseada em sessão do arquivo SBSCFG usando um argumento de linha de comando no atalho do Designer, consulte abaixo.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Ícone de arquivo XML](user-preferences-automating-setup.resources/user-preferences-automating-setup-01.png "ícone de arquivo XML")

</td>
</tr>
</table>

## Permanente ou baseado em sessão

Há duas maneiras diferentes de configurar o Designer para usar outro [arquivo de configuração](../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) diferente do padrão, ambos com vantagens e desvantagens:

* <b>Modificando permanentemente user\_preferences.xml\
  </b>Este arquivo está localizado no *~User\AppData\Local\Adobe\Adobe Substance 3D Designer* para Windows. Se você modificá-lo, o Designer sempre usará o que está definido nele, independentemente de como, quando ou onde você o iniciou. Para fazer alterações, é necessário modificar novamente o XML, ambos descritos abaixo, e que costumam estar um pouco envolvidos.
* <b>Definindo temporariamente a sessão por meio de um argumento de linha de comando\
  </b>O Designer pode usar um argumento de linha de comando na inicialização para substituir o arquivo SBSCFG para essa sessão (veja abaixo como). É uma solução simples e elegante, que permite alternar projetos de maneira muito mais rápida do que modificando um XML. O perigo é que, se você abrir por vários atalhos (por exemplo, Menu Iniciar e Desktop no Windows), poderá ter resultados diferentes sem que isso seja totalmente óbvio. Além disso, não é tão à prova de violação, pois os usuários podem excluir, mover ou modificar seus atalhos com muito mais facilidade do que seu user\_preferences.xml.

## Modificação de XML

### Modificação manual de preferências

Se não houver uma configuração automatizada ou para fins de teste, é possível acessar manualmente <b>Editar > Preferências...</b> e clicar na seção “<b>Projetos</b>” à esquerda.

![Configurações do projeto](user-preferences-automating-setup.resources/user-preferences-automating-setup-02.png "Configurações do projeto")

O botão marcado em vermelho permite que o usuário escolha um [arquivo SBSCFG](../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) diferente.

### Modificando por meio de script

Assim como os arquivos de Projeto e Configuração, as preferências do usuário são um XML estruturado, com a configuração relevante claramente identificável. Em vez de modificá-lo por meio de um editor de texto como o Notepad++ ou o Sublime Text, ele é bastante adequado para modificações por meio de uma configuração externa com script.

A vantagem do script é que o usuário não precisa fazer mais nada além de clicar em um botão e, se um sistema suficientemente complicado for criado, será possível gerenciar e trocar o projeto facilmente, sem a necessidade de gerenciar arquivos e configurações manualmente.

A linha relevante se parece com isto:

```
  <configuration> 

   <configurationfile>file:///C:/Users/John/AppData/Local/Adobe/Adobe Substance 3D Designer/default_configuration.sbscfg</configurationfile> 

  </configuration>
```


#### Exemplo em Python

Veja a seguir um exemplo de função Python 2.7 simples para Windows que modifica o usuário\_preferences.xml para outro arquivo de configuração. Isso altera permanentemente o valor até que seja retrocedido. A função SetConfigurationFile pode ser chamada com o caminho do arquivo sbscfg personalizado como um parâmetro.

Um script python permite um código poderoso e limpo, e pode ser facilmente integrado em outros lugares, mas a desvantagem é que para um usuário executá-lo, ele precisa ser compilado para um executável, ou o usuário precisa de uma implantação Python.

```
import xml.etree.ElementTree as ElementTree 

import os 

 

##Example Python script for changing Substance 3D Designer user preference file## 

 

def SetConfigurationFile(p_ConfigPath): 

## Check is the path passed as parameter exists.

    if(os.path.isfile(p_ConfigPath)): 

## replace backslashes by forwardslahes to ensure consistency

        p_ConfigPath = p_ConfigPath.replace("\", "/") 

## get Local Appadata path from Environment variables, construct full path to user_preferences.xml and check if it exists.

        m_AppDataPath = os.environ.get('LOCALAPPDATA') 

        if m_AppDataPath != None: 

            m_UserPrefsPath = os.path.join(m_AppDataPath, str("Adobe/Adobe Substance 3D Designer/user_preferences.xml")) 

            if(os.path.isfile(m_UserPrefsPath)): 

## read XML elementtree from file, find correct element until we get to the actual line that defines the configurationfile path

                m_PrefsTree = ElementTree.parse(m_UserPrefsPath) 

                m_PrefsRoot = m_PrefsTree.getroot() 

                m_PrefsElement = m_PrefsRoot.find("preferences") 

                m_XMLError = True 

                if(m_PrefsElement != None): 

                    m_ConfigElement = m_PrefsElement.find("configuration") 

                    if(m_ConfigElement != None): 

                        m_ConfigFileElement = m_ConfigElement.find("configurationfile") 

                        if(m_ConfigFileElement != None): 

                            m_XMLError = False 

## Check if path is already set, to avoid double work

                            if m_ConfigFileElement.text.replace("file:///","") == p_ConfigPath: 

                                print "configurationfile is already set to desired path. Aborting." 

                                return True 

                            else: 

## construct correctly formatted path, insert into elementtree

                                m_ConfigPath = str("file:///" + p_ConfigPath) 

                                m_ConfigFileElement.text = m_ConfigPath 

 

## Write to file

                                m_XMLString = str("<?xml version="1.0" encoding="UTF-8"?>n") + ElementTree.tostring(m_PrefsRoot, 'utf-8') 

                                m_File = open(m_UserPrefsPath,'w') 

                                m_File.write(m_XMLString) 

                                m_File.close() 

                                print "configuration file path succesfully changed!" 

                                return True 

                if m_XMLError: 

## if this flag was not set to false, we can assume something was missing or went wrong when walking through the XML

                    print("Error: malformed content in user_preferences.xml!") 

                    return False 

            else: 

                print "Error: user_preferences.xml does not exist, try starting Substance 3D Designer first!" 

                return False 

        else: 

            print "Error: LocalAppData path returned None" 

            return False 

    else: 

        print "Error: Invalid Configuration File path!" 

        return False
```


## Atalho de argumento da linha de comando

De uma forma muito mais simples, o Designer pode ser instruído a usar um SBSCFG específico na inicialização através do argumento “—config-file” (opcional).

### Configuração manual

Embora não seja recomendado usar um método manual em um ambiente de produção, para fins de teste, isso pode ser feito com bastante rapidez se você já tiver configurado o arquivo SBSCFG.

1. Adicionar um espaço
1. Adicione —config-file após o caminho para o designer na seção Destino.
1. Adicionar outro espaço
1. Adicione seu caminho, *delimitado por aspas* para evitar problemas com espaços no caminho
1. O resultado deve ser assim:

   *”C:\Program Files\Adobe\Adobe Substance 3D Designer\Adobe Substance 3D Designer.exe” —config-file “C:\Dev\Substance\custom\_configuration.sbscfg”*

![Entrada de arquivo de configuração nas propriedades do arquivo executável](user-preferences-automating-setup.resources/user-preferences-automating-setup-03.jpg "Entrada de arquivo de configuração nas propriedades do arquivo executável")
