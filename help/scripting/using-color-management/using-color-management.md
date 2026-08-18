---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/using-color-management.html"
breadcrumb-title: ''
description: Saiba como usar os recursos de gerenciamento de cores em scripts Substance 3D Designer Python para cores precisas.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using color management
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uso do gerenciamento de cores
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# Uso do gerenciamento de cores

A classe </b>SDColorManagementEngine <b>, acessível da classe <b>SDApplication</b>, contém informações sobre as *configurações atuais de gerenciamento de cores*.

## Acesso e consulta do Mecanismo de gerenciamento de cores

```
import sd 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

 

## Access the color management engine.

cm = app.getColorManagementEngine() 

 

## Currently getName can return "legacy", "ace" or "ocio"

## depending on the color management settings in the preferences.

cmName = cm.getName()  

print(cmName) 

 

print(cm.getWorkingColorSpaceName()) 

print(cm.getRawColorSpaceName()) 

 

if cmName == "ocio": 

## If OpenColorIO is enabled, print the config file name.

    print(cm.getOCIOConfigFileName()) 

 

## List all color spaces.

colorSpaces = cm.getColorSpaces() 

for cs in colorSpaces: 

    print(cs.get())
```


Além disso, é possível *atribuir espaços de cores* a recursos de bitmap de Python.

### Configuração de espaços de cores em recursos de bitmap

```
import sd 

import sd 

from sd.api.sdproperty import * 

from sd.api.sdresourcebitmap import SDResourceBitmap 

from sd.api.sdvaluestring import SDValueString 

from sd.api.sdvaluebool import SDValueBool 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

pkgMgr = app.getPackageMgr() 

cm = app.getColorManagementEngine() 

 

colorSpaces = cm.getColorSpaces() 

 

## Get all the resources in the first package.

pkg = pkgMgr.getPackages()[0] 

resources = pkg.getChildrenResources(isRecursive=True) 

 

for res in resources: 

 if isinstance(res, SDResourceBitmap): 

  props = res.getProperties(SDPropertyCategory.Annotation) 

 

## Print the current color space for the resource.

  p0 = res.getPropertyFromId("bitmap_color_space", SDPropertyCategory.Annotation) 

  cs = res.getAnnotationPropertyValueFromId("bitmap_color_space") 

  print(cs.get()) 

 

## Print the current premultiplied alpha setting for the resource.

  p1 = res.getPropertyFromId("bitmap_premultiplied_alpha", SDPropertyCategory.Annotation) 

  cs = res.getAnnotationPropertyValueFromId("bitmap_premultiplied_alpha") 

  print(cs.get()) 

 

## Assign new values for the color space and premultiplied alpha properties.

  res.setPropertyValue(p0, colorSpaces[2]) 

  res.setPropertyValue(p1, SDValueBool.sNew(False))
```


## Gravação de SDTextures com conversões de espaço de cores

O método **save** da classe **SDTexture** agora aceita um parâmetro **outputColorSpace** opcional. Quando especificado, a conversão do espaço de cores será *aplicada antes de salvar a imagem*.

Se o modo de gerenciamento de cores oferecer suporte aos perfis ICC incorporados *e* o formato do arquivo de destino também oferecer suporte a eles, o perfil ICC do espaço de cores será *incorporado no arquivo de imagem resultante*.
