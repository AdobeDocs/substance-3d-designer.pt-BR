---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/getting-started/system-requirements.html"
breadcrumb-title: ''
description: Revise os requisitos de sistema do Substance 3D Designer para garantir que seu computador atenda às especificações necessárias.
helpx_creative_field: ""
helpx_description: Designer > Getting started > System requirements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Requisitos do sistema
user-guide-description: ''
user-guide-title: ''
source-git-commit: ec787363bab8318804a71d6cf7c5484fc67a987e
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---


# Sistemas compatíveis

Veja abaixo uma lista de hardware e sistemas suportados pelo aplicativo:

## Windows

|  | Mínimo | Recomendado | Ideal |
| --- | --- | --- | --- |
| <b>SO</b> | Windows 11 64 bits versão 23H2 | Windows 11 64 bits versão 24H1 | Windows 11 64 bits versão 24H2 |
| <b>CPU</b> | Intel Core i5 AMD Ryzen 5 | Intel Core i7 AMD Ryzen 7 | Intel Core i9 AMD Ryzen 9 |
| <b>GPU</b> | NVIDIA GeForce RTX 2060 Super NVIDIA Quadro RTX 4000 AMD Radeon RX 5700 XT AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080 NVIDIA Quadro RTX A4000 AMD Radeon RX 6800 XT AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090 NVIDIA Quadro RTX 5000 Ada Generation AMD Radeon RX 7900 XTX AMD Radeon Pro W7800 |
| <b>VRAM</b> | 8 GB | 16 GB | 24 GB |
| <b>RAM</b> | 16 GB | 32 GB | 64 GB |
| <b>Armazenamento</b> | SSD com 30 GB de espaço disponível | SSD com 50 GB de espaço disponível | SSD com 70 GB de espaço disponível |

### macos

|  | Mínimo | Recomendado | Ideal |
| --- | --- | --- | --- |
| <b>SO</b> | macOS 14 Sonoma | macOS 26 Tahoe | macOS 26 Tahoe |
| <b>CPU</b> | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| <b>GPU</b> | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| <b>RAM</b> | 16 GB | 32 GB | 64 GB |
| <b>Armazenamento</b> | SSD com 30 GB de espaço disponível | SSD com 50 GB de espaço disponível | SSD com 70 GB de espaço disponível |

### Linux

| Corporativo | Vapor |
| --- | --- |
| RHEL 8 </br>RHEL 9 | Ubuntu 22.04 |

## Recomendações gerais

* Para trabalhar em condições confortáveis, recomendamos um monitor com uma resolução maior do que 1 Mega Pixel e maior do que 1280 pixels.
* Muitos aplicativos Substance dependem do OpenSSL 1.1.1 para compatibilidade com RHEL8/9. Para sistemas com versões OpenSSL mais recentes, você precisará fornecê-lo manualmente.
* *Somente* versões <b>2019.x</b> e posteriores foram autenticadas para serem executadas no <b>MacOS 10.15</b> (Catalina).
* A conexão com a <b>Área de trabalho remota</b> será possível se um contexto OpenGL 3.3 estiver disponível. Ele funcionará na <b>Nvidia Quadro</b>, mas *não* na Nvidia GeForce porque fornece apenas um contexto OpenGL 1.4. Se isso for um problema, recomendamos o uso de soluções alternativas, como o <b>VNC</b>/<b>Teamviewer</b>.
* Os usuários da versão <b>Steam</b> devem *desabilitar* a <b>Sobreposição de Steam</b> para o Designer, pois isso pode causar problemas de desempenho quando ativo.

## GPUs compatíveis

Veja abaixo uma lista da GPU compatível com o aplicativo:

* NVIDIA GeForce GTX 1060 e posterior
* NVIDIA Quadro P2200 e posterior
* AMD Radeon RX 580 e posterior
* AMD Radeon Pro 5300 M

>[!TIP]
>
> **TDR (somente Windows)**
> 
> Para obter a melhor estabilidade geral ao realizar cálculos pesados na GPU, por exemplo, renderizar gráficos complexos, renderizar na exibição 3D, exportar uma cena da exibição 3D etc., é altamente recomendável verificar se os valores de <b>Detecção e recuperação de tempo limite (TDR)</b> correspondem às recomendações nesta [página](https://experienceleague.adobe.com/pt-br/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) da nossa documentação.

## Configurações sem suporte

<b>Windows</b>

* Não há suporte para máquinas virtuais.
* Não há suporte para o Windows Server.

<b>macOS</b>

* Os sistemas macOS baseados em Intel não são suportados.
* Somente configurações oficiais do Apple são compatíveis.
* Atualmente, não há suporte para eGPUs e elas podem apresentar problemas de estabilidade.

<b>Linux</b>

* Drivers Mesa no Linux não são suportados.

<b>Qualquer plataforma</b>

* As GPUs integradas não são compatíveis com CPUs x86-64 (Intel, AMD).
* O uso do Designer em combinação com software de terceiros que intercepta chamadas Designer para os drivers gráficos não é suportado. Esse software inclui:
  * Injetores pós-processamento, como recodificadores que aplicam correção de cores, efeitos de câmera, etc.
  * Sobreposições na tela, como linhas cruzadas personalizadas, métricas de desempenho de GPU, capas para streaming de vídeo...

## Versões mínimas do driver de GPU

Veja abaixo uma lista das versões mínimas de driver de GPU necessárias para que o aplicativo seja executado sem problemas. Esta lista está sujeita a alterações à medida que novas versões são lançadas.

Para baixar novos drivers, consulte: [A GPU tem drivers desatualizados](https://experienceleague.adobe.com/pt-br/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-has-outdated-drivers).

| SO | NVIDIA | AMD | Intel |
| --- | --- | --- | --- |
| <b>Windows</b> | GeForce 451.48 Quadro 451.48 | Radeon 19.7.1 Radeon Pro/FirePro 18.Q4 | 15.33 |
| <b>Linux</b> | 535.129.03 | Radeon 23.20 Pro 23.Q3 | Sem suporte |

>[!NOTE]
>
> No **sistema operacional Mac**, o driver de GPU é fornecido pelo próprio sistema operacional. Atualize para a versão mais recente do seu sistema operacional para acessar o driver mais recente.

## Rastreamento de raios do GPU para panificação

Para habilitar o Rastreamento de raios do GPU via Optix ou DXR, os drivers recomendados acima devem estar instalados.

O <b>DXR</b> requer a seguinte configuração mínima:

* <b>Windows 10</b> versão 1809, consulte [esta página](https://experienceleague.adobe.com/pt-br/docs/substance-3d/bakers/features/gpu-raytracing) para obter mais informações
* <b>GPU com arquitetura Pascal</b> (Nvidia GeForce 10XX)

>[!TIP]
>
> O Rastreamento de raios do GPU funciona de maneira ideal em hardware de rastreio de raio dedicado, como GPUs NVIDIA GeForce RTX ou NVIDIA Quadro RTX.

## Usando tablets

Os usuários do tablet no <b>Windows</b> devem aplicar as configurações descritas na página a seguir para obter a experiência mais confiável: [Configurar canetas e tablets](https://experienceleague.adobe.com/pt-br/docs/substance-3d-painter/using/technical-support/configuring-pens-and-tablets).

## Idiomas

A interface de software está disponível nos seguintes idiomas:

* Deutsch (Deutschland)
* Inglês (Estados Unidos)
* Español (España)
* Français (França)
* Italiano (Italia)
* Português (Brasil)
* 日本語（日本）
* 한국어(한국)
* 简体中文（中国)
