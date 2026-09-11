---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/debugging-plugins-using-visual-studio-code.html"
breadcrumb-title: ''
description: Saiba como depurar plug-ins Python da Substance 3D Designer usando o Visual Studio Code para um desenvolvimento eficiente.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Debugging plugins using Visual Studio Code
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Depurando plug-ins usando o Visual Studio Code
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# Depurando plug-ins usando o Visual Studio Code

Como padrão de fluxo de trabalho para muitos desenvolvedores, o **Visual Studio Code IDE** está disponível para depurar plug-ins Python.

>[!WARNING]
>
> O método <b>debugpy.listening()</b> pode permitir que qualquer pessoa que possa se conectar à porta especificada execute código arbitrário no processo depurado.
> 
> Portanto, a depuração deve *<b>somente</b>* ser configurada e executada em *redes seguras*.

Para configurar a sinergia entre o Visual Studio Code e o Substance 3D Designer, siga estas etapas:

1. Instale o **[Código do Visual Studio](https://code.visualstudio.com/)** e a **[extensão Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)**.
1. Instale o **[módulo Python de depuração](https://github.com/microsoft/debugpy)**.

   >[!NOTE]
   >
   > Verifique se o interpretador Python no Designer pode localizar o módulo &#39;*debugpy*&#39;. A maneira mais fácil de fazer isso é adicionar o diretório em que o módulo &#39;*debug*&#39; está à variável de ambiente **PYTHONPATH**. Uma alternativa seria modificar sys.path em seu script para adicionar o caminho ao módulo de depuração.
1. Inicie o aplicativo, abra o Editor de Python e **execute o seguinte código**:

   ```
   import sys 
   
   
   
   debugpy_path = '/path/to/debugpy/module' 
   
   debugpy_port = 5678 
   
   designer_py_interpreter = '/path/to/python/executable/bundled/in/designer' 
   
   
   
   if not debugpy_path in sys.path: 
   
       sys.path.append(debugpy_path) 
   
   
   
   import debugpy 
   
   
   
   debugpy.configure(python=designer_py_interpreter) 
   
   debugpy.listen(debugpy_port)
   ```

1. No Visual Studio Code, abra seu projeto e crie um arquivo **launch.json**. Adicione o seguinte ao arquivo:

   ```
   { 
   
       "name": "Attach to Designer", 
   
       "type": "python", 
   
       "request": "attach", 
   
       "port": <port number used in the script above>, 
   
       "host": "127.0.0.1" 
   
   }
   ```

1. Clique no ícone <b>Depurar</b>, crie ou edite a configuração do depurador, se necessário.
1. Selecione a configuração **Python: Anexar ao Designer** e clique em **Iniciar Depuração**.

   Agora você pode definir pontos de interrupção, avançar pelo código e usar todos os outros recursos do depurador do Visual Studio Code.
