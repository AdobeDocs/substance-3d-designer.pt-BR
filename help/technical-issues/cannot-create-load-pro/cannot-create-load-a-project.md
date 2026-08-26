---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/cannot-create-load-a-project.html"
breadcrumb-title: ''
description: Solucione problemas de criação ou carregamento de projetos no Substance 3D Designer e encontre soluções.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Cannot createload a project
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Não é possível criar um carregamento de projeto
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---


# Não é possível criar/carregar um projeto

Esta página lista as causas comuns para falhas ao criar ou carregar projetos no Substance 3D Designer e oferece etapas de solução de problemas para cada um.

## O aplicativo é muito antigo para abrir a URL

**![(erro)](../../assets/error.svg) Problema**

O **arquivo do Substance 3D (SBS)** está sendo carregado por uma versão do Substance 3D Designer que *não oferece suporte ao seu formato*. O arquivo do Substance 3D provavelmente foi *salvo em uma versão mais recente* do software que usa um formato atualizado para esses arquivos.

**![(tick)](../../assets/check.svg) Etapas recomendadas**

À medida que o Substance 3D Designer evolui, o formato de arquivo Substance 3D (SBS) também evolui. Na maioria das vezes, uma nova versão do software precisará *atualizar seus arquivos* para que eles possam oferecer suporte aos recursos mais recentes.

Você é *solicitado* a executar esta atualização ao *carregar o arquivo pela primeira vez* em uma nova versão.

>[!WARNING]
>
> Se o arquivo for salvo *após* a atualização ter sido aplicada, sua versão de formato também será alterada. Neste ponto, ele não pode mais *ser carregado em versões anteriores* do Substance 3D Designer.
> 
> Essa limitação também se aplica ao [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html).

Primeiro, verifique se você está usando a versão mais recente do Substance 3D Designer permitida por sua licença atual. Veja a seguir os pontos de acesso às atualizações de cada edição:

* <b>Assinatura do Adobe Substance 3D:</b> acesse a seção Atualizações da guia Aplicativos no aplicativo [Adobe Creative Cloud para desktop](https://creativecloud.adobe.com/en/apps/download/creative-cloud)
* Assinatura do <b>[Substance3d.com](http://Substance3d.com):</b> atualize quando solicitado no Substance 3D Designer ou baixe o instalador mais recente na seção [Minhas Licenças](https://store.substance3d.com/user) do site [Substance3d.com](http://substance3d.com)
* <b>Vapor:</b> o aplicativo será atualizado automaticamente por padrão. Você pode acionar manualmente a atualização iniciando o Substance 3D Designer ou acessando a tela Downloads

>[!WARNING]
>
> Certifique-se de que você não precisará carregar seus arquivos em uma versão anterior do Substance 3D Designer *antes de salvar* um arquivo que foi atualizado.
> 
> Como alternativa, você pode *fazer uma cópia* do seu arquivo *antes* de carregá-lo em uma nova versão do Substance 3D Designer, para que você sempre tenha um arquivo para retornar caso precise usar uma versão anterior do software.

## Falha ao criar ou carregar um projeto

<b>![(erro)](../../assets/error.svg) Problema</b>

Uma falha ao criar ou carregar um projeto geralmente é causada por um erro durante a inicialização da [Exibição 3D](../../interface/3d-view/3d-view.md), que ocorre quando o espaço de trabalho está sendo configurado.

Se o sistema for um laptop, um aplicativo de terceiros poderá impor um *plano de gerenciamento de energia* que impeça a Exibição 3D de usar a GPU do sistema. Isso pode resultar em uma falha se nenhum outro dispositivo de GPU puder executar a tarefa em seu lugar.

Também pode ocorrer uma falha quando a *configuração de exibição ou o dimensionamento* foi alterado entre as sessões, de modo que o quadro de renderização de Exibição 3D é criado em coordenadas inválidas.

<b>![(tick)](../../assets/check.svg) Etapas recomendadas</b>

Considerando as várias causas possíveis dessa falha, sugerimos seguir as seguintes etapas de solução de problemas em ordem:

Atualizar drivers gráficos

Primeiro, verifique se os drivers gráficos estão atualizados. Você pode encontrar a versão mais recente da sua GPU [aqui](https://www.nvidia.com/Download/index.aspx?lang=en-us) (NVIDIA), [aqui](https://www.amd.com/en/support) (AMD) ou [aqui](https://downloadcenter.intel.com/product/80939/Graphics-Drivers) (Intel).

Forçar melhor desempenho

Procure qualquer software que gerencie o *plano de energia* do seu sistema (por exemplo, o AOS Armory Crate), especialmente quando o sistema for um laptop.

Alguns aplicativos de gerenciamento de energia podem limitar o acesso de outros aplicativos à GPU do sistema ou prejudicar o desempenho da GPU, o que pode resultar em falhas. Se um aplicativo de gerenciamento de energia existir e estiver ativo, mude para o plano que permite o melhor desempenho.

Forçar o uso de GPU separada

Se o seu sistema tiver *gráficos alternáveis*, considere forçar o uso da GPU (dGPU) separada para aplicativos do Substance 3D.

Na maioria dos casos, isso é feito em um aplicativo dedicado que controla as configurações da GPU. Por exemplo, para GPUs NVIDIA, você pode fazer isso no aplicativo “Painel de controle NVIDIA”.

Redefinir interface de usuário salva no Registro

Se a falha for causada por uma alteração na configuração de exibição ou no dimensionamento, você pode tentar excluir as entradas de registro existentes do Designer para redefinir completamente a interface do usuário, entre outras configurações.

O procedimento para executar essa redefinição por sistema operacional é descrito abaixo:

+++Windows
* Fechar o Designer

Fechar o Designer

* Abrir o aplicativo <b>Prompt de comando</b>

Abrir o aplicativo <b>Prompt de comando</b>

* Insira o seguinte comando e pressione <b>Enter</b>:

  <b>Área de trabalho do Creative Cloud</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Adobe\Adobe Substance 3D Designer" /f
  ```


  <b>Edição de vapor/Substance</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Allegorithmic\Substance Designer" /f
  ```


Insira o seguinte comando e pressione <b>Enter</b>:

<b>Área de trabalho do Creative Cloud</b>

<b>Edição de vapor/Substance</b>

* Desconecte o segundo monitor do sistema e conecte-o novamente (ignore esta etapa se você *não* tiver vários monitores conectados)

Desconecte o segundo monitor do sistema e conecte-o novamente (ignore esta etapa se você *não* tiver vários monitores conectados)

* Inicie o Designer, mas *não* crie ou abra um projeto

Inicie o Designer, mas *não* crie ou abra um projeto

* Na barra superior, abra o menu <b>Janelas</b> e selecione a opção <b>Nova Exibição 3D</b>

Na barra superior, abra o menu <b>Janelas</b> e selecione a opção <b>Nova Exibição 3D</b>

* Verifique se a <b>Exibição 3D</b> foi inicializada corretamente e tente outras malhas de visualização no menu <b>Cena</b> da barra superior do painel

Verifique se a <b>Exibição 3D</b> foi inicializada corretamente e tente outras malhas de visualização no menu <b>Cena</b> da barra superior do painel

* Criar ou abrir um material

Criar ou abrir um material

+++

+++macOS
* Fechar o Designer

Fechar o Designer

* Abrir o aplicativo <b>Terminal</b>

Abrir o aplicativo <b>Terminal</b>

* Insira o seguinte comando e pressione <b>Enter</b>:

  <b>Área de trabalho do Creative Cloud</b>

  ```
  rm ~/Library/Preferences/com.adobe.Adobe\ Substance\ 3D\ Designer.plist
  ```


  <b>Edição de vapor/Substance</b>

  ```
  rm ~/Library/Preferences/com.allegorithmic.Substance\ Designer.plist
  ```


Insira o seguinte comando e pressione <b>Enter</b>:

<b>Área de trabalho do Creative Cloud</b>

<b>Edição de vapor/Substance</b>

* Desconecte o segundo monitor do sistema e conecte-o novamente (ignore esta etapa se você *não* tiver vários monitores conectados)

Desconecte o segundo monitor do sistema e conecte-o novamente (ignore esta etapa se você *não* tiver vários monitores conectados)

* Inicie o Designer, mas *não* crie ou abra um projeto

Inicie o Designer, mas *não* crie ou abra um projeto

* Na barra superior, abra o menu <b>Janelas</b> e selecione a opção <b>Nova Exibição 3D</b>

Na barra superior, abra o menu <b>Janelas</b> e selecione a opção <b>Nova Exibição 3D</b>

* Verifique se a <b>Exibição 3D</b> foi inicializada corretamente e tente outras malhas de visualização no menu <b>Cena</b> da barra superior do painel

Verifique se a <b>Exibição 3D</b> foi inicializada corretamente e tente outras malhas de visualização no menu <b>Cena</b> da barra superior do painel

* Criar ou abrir um material

Criar ou abrir um material

+++
