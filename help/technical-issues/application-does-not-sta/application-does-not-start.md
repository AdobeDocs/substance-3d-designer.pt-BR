---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/application-does-not-start.html"
breadcrumb-title: ''
description: Solucione problemas que impedem o Substance 3D Designer de iniciar e encontre soluções para iniciar o aplicativo.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Application does not start
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: O aplicativo não inicia
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5e56914c9048c513359d578d802097ef18493a5c
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 1%

---


# O aplicativo não inicia

Esta página lista as causas comuns de falhas no Substance 3D Designer ao iniciar corretamente e oferece etapas de solução de problemas para cada uma delas, agrupadas por sistema operacional:

[Designer 15.0 e posterior](#version-15-0)

[Windows 10/11](#windows-10-11)

[Windows 7/8/8.1](#windows-7-8)

[Linux](#linux)

## Designer 15.0 e posterior

<b>![(erro)](../../assets/error.svg) Problema</b>

As versões 15.0 e posteriores do Designer não são iniciadas em sistemas com uma GPU integrada (iGPU) e uma GPU separada (dGPU).

<b>![(tick)](../../assets/check.svg) Etapas recomendadas</b>

Atualize os drivers gráficos da iGPU. Você pode encontrar os drivers mais recentes aqui: [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)  | [AMD](https://www.amd.com/en/support/download/drivers.html)

## Windows 10/11

**![(erro)](../../assets/error.svg) Problema**

O Substance 3D Designer não inicia em sistemas que usam o Windows 10 ou o Windows 11.

**![(tick)](../../assets/check.svg) Etapas recomendadas**

Versões mais antigas do Designer podem falhar ao iniciar no Windows 10 ou Windows 11 devido a uma biblioteca *desatualizada* `libeay32.dll` usada no processo de validação de licença.

Você pode tentar substituir a biblioteca por uma *versão atualizada*, como aquela distribuída [aqui](https://support.networkoptix.com/hc/en-us/articles/115015730007-Nx-Software-crashes-due-to-libeay32-dll-on-Windows) (selecione o arquivo para Windows de 32 bits), seguindo estas etapas:

1. Localize o arquivo `libeay32.dll` no diretório de instalação do Designer
1. Faça backup do arquivo em um local seguro se precisar restaurá-lo no futuro
1. Substituir o arquivo pela versão atualizada
1. Iniciar o Designer

>[!WARNING]
>
> Configurações sem suporte
> 
> Não há suporte para o Windows 10. Você pode saber mais na página [Requisitos de sistema](../../getting-started/system-requirements/system-requirements.md).
> 
> Versões do Designer fora do período de manutenção não são compatíveis. Essas versões podem não ser mais executadas de forma confiável se forem feitas alterações significativas no sistema, como atualizações do sistema operacional.

## Windows 7/8/8.1

**![(erro)](../../assets/error.svg) Problema**

O Substance 3D Designer não inicia em sistemas que usam o Windows 7, Windows 8 ou Windows 8.1.

**![(tick)](../../assets/check.svg) Etapas recomendadas**

Como parte da atualização da versão **11.3.0**, atualizamos várias bibliotecas, ferramentas e SDKs que *quebraram a compatibilidade* com versões do Windows anteriores ao Windows 10.

Recomendamos *atualizar para o Windows 10, pois a própria Microsoft não oferece mais suporte às versões anteriores do Windows para uso principal (consulte [aqui](https://www.microsoft.com/en-us/windows/windows-7-end-of-life-support-information) e [aqui](https://docs.microsoft.com/en-us/lifecycle/faq/windows#windows-8.1)).* Portanto, o uso contínuo dessas versões apresenta um *problema de segurança*.\
Se não for possível atualizar para o Windows 10, *não atualize* a instalação da versão **11.2.2** do *Designer* anterior.

>[!WARNING]
>
> Configurações sem suporte
> 
> Observe que o Windows 7, o Windows 8 e o Windows 8.1 *não são oficialmente suportados*. Você pode saber mais na página [Requisitos de sistema](../../getting-started/system-requirements/system-requirements.md).

## Linux

<b>![(erro)](../../assets/error.svg) Problema</b>

Falha ao fechar a tela inicial e exibir a janela principal.

<b>![(tick)](../../assets/check.svg) Etapas recomendadas</b>

O Designer falha ao carregar componentes Python porque carrega a biblioteca <b>libffi.so</b> do sistema em vez da própria biblioteca.

Para garantir que o Designer carregue sua própria biblioteca, use este comando no diretório de instalação do Designer, substituindo `%command%` pelo comando para executar o Designer:

```
LD_PRELOAD=./plugins/pythonsdk/lib/python3.11/lib-dynload/libffi.so.6 %command%
```


Observe que o número da versão do Python depende da versão do Designer que está sendo executada:

* Inferior a 14.0.0: python3.9
* Inferior a 12.1.0: python3.7

+++Opções de lançamento a vapor
Os usuários do Linux que iniciam o Designer a partir do Steam podem definir o comando LD\_PRELOAD nas opções de inicialização do Designer, conforme mostrado abaixo.

Depois que isso for feito, o Designer poderá ser iniciado no Steam normalmente para todas as sessões futuras.

![Opções de inicialização por vapor](../../assets/steam_linux_launch_option.jpg "Opções de inicialização por vapor")



+++

**![(erro)](../../assets/error.svg) Problema**

A edição Steam do Designer falha ao iniciar e não produz nenhuma mensagem de erro.

**![(tick)](../../assets/check.svg) Etapas recomendadas**

Em vez disso, você pode adquirir mensagens de erro registrando o aplicativo Steam.

Como recomendado [aqui](https://github.com/ValveSoftware/steam-for-linux/issues/7114#issuecomment-629634260), feche completamente o Steam e execute o seguinte comando a partir de um terminal (ou crie um atalho para este comando):

```
steam 2>&1 | tee /path/to/logfile
```


<b>![(erro)](../../assets/error.svg) Problema</b><b>e</b>

Não é possível carregar o plug-in `<b>xcb</b>`. A seguinte mensagem é exibida na linha de comando:

```
qt.qpa.plugin: Could not load the Qt platform plugin "xcb" in "" even though it was found. 

This application failed to start because no Qt platform plugin could be initialized. Reinstalling the application may fix this problem. 

 

Available platform plugins are: minimal, offscreen, xcb. 

 

Aborted (core dumped)
```


**![(tick)](../../assets/check.svg) Etapas recomendadas**

Alguns pacotes necessários estão ausentes. Execute o seguinte comando no diretório de instalação do Designer:

```
ldd libQt5XcbQpa.so.5
```


Verifique se há pacotes relatados como `not found` na lista impressa e execute o seguinte comando para cada um desses pacotes ausentes:

```
apt-get install <package-name>
```


E.g.

```
apt-get install libxcb-xinput0
```


<b>![(erro)](../../assets/error.svg) Problema</b>

Este erro é gerado ao iniciar o Designer:

```
error while loading shared libraries: libcrypt.so.1: cannot open shared object file: No such file or directory
```


Uma biblioteca de sistema carregada pelo Designer é incompatível com a biblioteca <b>libcrypto.so.1.1</b> própria da Designer.

<b>![(tick)](../../assets/check.svg) Etapas recomendadas</b>

Remova a biblioteca <b>`libcrypto.so.1.1`</b> do diretório de instalação do Designer para que a biblioteca do sistema seja usada.

>[!NOTE]
>
> Esta solução alternativa só funciona quando o sistema tem sua própria biblioteca libcrypto.so.1. Em distribuições recentes, talvez seja necessário instalar um pacote de compatibilidade como <b>libxcrypt-compat</b>.

<b>![(erro)](../../assets/error.svg) Problema</b>

O Substance 3D Designer não inicia em sistemas usando distribuições do Linux *baseadas em arco*.

**![(tick)](../../assets/check.svg) Etapas recomendadas *(![(warning)](../../assets/warning.svg) Instável, somente GPUs AMD!)***

Tente instalar o **progl** (parte dos drivers [AMDGPU-PRO](https://wiki.archlinux.org/title/AMDGPU_PRO)) e inicie o Designer por meio dele. Você pode fazer isso usando o prefixo `progl` no comando de inicialização do aplicativo:

```
progl <designer-application-path>
```


Lembre-se de que `progl` pode estar instável. Portanto, esta tentativa deve ser feita como um *último recurso*.

>[!WARNING]
>
> Observe que as distribuições baseadas em arco do Linux *não são suportadas*. Você pode saber mais na página [Requisitos de sistema](../../getting-started/system-requirements/system-requirements.md).
