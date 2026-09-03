---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/iray.html"
breadcrumb-title: ''
description: Use o renderizador Iray na visualização 3D do Substance 3D Designer para visualização de material baseada fisicamente e iluminação realista.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > Iray
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Iray
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '2151'
ht-degree: 1%

---


# Iray

Esta página apresenta o renderizador Iray disponível no painel de exibição 3D do [Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html), que oferece rastreamento de caminho interativo para renderização fotorrealista com aceleração por CPU e/ou GPU (somente GPUs Nvidia).

>[!WARNING]
> 
> O renderizador Iray e todos os recursos relacionados foram removidos do Designer na versão 16.0.0.
> 
> Saiba mais aqui: [Fim da vida útil do gráfico MDL e da Iray](../../../technical-issues/mdl-graph-iray-eol/mdl-graph-iray-eol.md)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Visão geral

A <b>Iray</b> é uma tecnologia de renderização altamente *interativa* e intuitiva com base física que gera *imagens fotorrealistas* simulando o comportamento físico da luz e dos materiais. Saiba mais na página da Web [Nvidia Iray](https://www.nvidia.com/en-us/design-visualization/iray/).

</td>
<td style="border: 0;" valign="top">

[![Logotipo da NVIDIA Iray](iray.resources/iray-01.jpg)](https://www.nvidia.com/en-us/design-visualization/iray/)

</td>
</tr>

<tr style="border: 0;">
<td style="border: 0;" valign="top">

Como a Exibição 3D usa o *renderizador progressivo* do Iray, uma imagem é produzida assim que pelo menos uma amostra é executada em cada pixel. A imagem é *atualizada automaticamente* à medida que iterações de amostragem são executadas, resultando em uma imagem bruta inicial tornar-se *mais limpa em cada iteração*.

O renderizador está disponível no painel [Exibição 3D](../../../interface/3d-view/3d-view.md): abra o menu <b>Renderizador</b> e selecione a opção <b>Iray</b> para alternar o renderizador usado nesse painel de exibição 3D para Iray.\
Alternar para o renderizador Iray *altera as opções disponíveis* em alguns dos menus de exibição 3D. Essas alterações são explicadas na seção <b>Exibição 3D</b> abaixo.

Por padrão, a renderização progressiva é iniciada assim que o renderizador Iray é selecionado. O processo de renderização será executado até que *uma* destas condições seja atendida:

* O *número máximo de amostras* é executado
* O *limite de tempo de renderização* foi atingido

Consulte a seção <b>Renderizador</b> desta página para saber mais sobre como ajustar essas condições.

</td>
<td style="border: 0;" valign="top">

![Material de parede de castelo medieval renderizado em Iray](iray.resources/iray-02.png "Material de parede de castelo medieval renderizado em Iray")

*Material: [parede do castelo medieval](https://oggyart.artstation.com/projects/Xnzx0a)* *por [Mark Foreman](https://www.artstation.com/oggyart)* *disponível em nossos [ativos do Substance 3D](https://substance3d.adobe.com/assets)* *biblioteca*

</td>
</tr>
</table>

>[!WARNING]
>
> Somente *uma* instância de renderização Iray pode ser executada a qualquer momento.\
> Isso significa que quando um painel de exibição 3D usa esse renderizador, o menu **Renderizador** é *desabilitado* em outros painéis de exibição 3D e estes são padronizados para o renderizador **OpenGL**.

## Opções de visualização 3D

<a name="scene"></a>

### Cena

Selecione a opção <b>Editar</b> no menu <b>Cena</b> para localizar as propriedades de cena específicas do Iray no painel <b>Propriedades</b>.

* <b>Está habilitado:</b> quando definido como *Falso*, o objeto está oculto e *não contribui mais* para a cena

Exibir componente

* <b>Está visível</b>: quando definido como *Falso*, o objeto está oculto, mas *ainda contribui* para a cena, isto é, refletir a luz, absorver a luz e projetar sombras

Componente de exibição de malha

* Subdivisão
  * <b>Método</b>: o método usado para subdividir proceduralmente a malha em geometria mais fina
    * *Nenhum*: nenhuma subdivisão foi aplicada
    * *Paramétrico*: subdivide a malha em `4^x` triângulos, onde `x` é o valor especificado por este parâmetro
    * *Comprimento*: subdivide a malha até que todas as bordas tenham um comprimento (no espaço de objeto) abaixo do valor especificado pelo parâmetro de comprimento mínimo
  * <b>Comprimento mínimo</b>: subdivide a malha até que todas as bordas tenham um comprimento abaixo desse valor especificado no espaço de objeto (aplica-se somente ao método *Comprimento*)
  * <b>Número</b>: o número de iterações de subdivisão que deve ser aplicado à malha (aplica-se somente ao método *Paramétrico*)

>[!WARNING]
>
> A subdivisão da malha *aumenta seu tempo de processamento exponencialmente* antes e durante a renderização. Sugerimos ser *conservadores* com a entrada de valores.\
> Tenha cuidado ao usar valores *altos* **Números** para o método Paramétrico e valores *baixos* **mínimos** para o método Comprimento.

![Opções de cena](iray.resources/iray-03.gif "Opções de cena")

<a name="materials"></a>

### Materiais

Como a Iray depende do [modelo de sombreamento MDL](https://www.nvidia.com/en-us/design-visualization/technologies/material-definition-language/) desenvolvido pela NVIDIA, os materiais disponíveis para materiais de cena são substituídos pela biblioteca MDL carregada pela Designer. Essa biblioteca é criada usando as seguintes fontes:

* Os arquivos MDL incluídos na instalação do Designer
* Os arquivos MDL encontrados nos [diretórios listados pelo usuário](../../../interface/preferences-window/project-settings/project-settings.md) nos [arquivos de projeto](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) carregados
* A biblioteca [NVIDIA vMaterials](https://developer.nvidia.com/vmaterials), se estiver instalada

>[!NOTE]
>
> Para obter uma visão mais detalhada do modelo de sombreamento MDL, confira o [Manual de MDL](http://mdlhandbook.com/), escrito e mantido pela NVIDIA.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

A lista cumulativa de materiais MDL carregados está disponível no menu <b>Materiais</b>, em qualquer submenu de materiais listados, conforme mostrado na imagem à direita.

Além disso, se um [gráfico MDL](../../../mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md) for carregado no Designer, ele poderá ser aplicado a qualquer material na Cena. Nesse ponto, ele é adicionado à lista de materiais MDL disponíveis.

Outras opções notáveis neste menu são:

* Selecione a opção <b>Editar</b> para acessar as *entradas expostas* do MDL no painel <b>Propriedades</b> e ajustar o material conforme necessário
* A opção <b>Carregar...</b> permite *carregar manualmente qualquer arquivo MDL* a ser adicionado à lista cumulativa e aplicado à cena
* A opção <b>Exportar predefinição...</b> abre a caixa de diálogo <b>Exportar predefinição de material MDL</b>, que permite exportar um arquivo MDL predefinido usando as configurações atuais aplicadas na Exibição 3D

</td>
<td style="border: 0;" valign="top">

![Menu Materiais](iray.resources/iray-04.png "Menu Materiais")

</td>
</tr>
</table>

>[!NOTE]
>
> Ao carregar um **gráfico MDL**, o renderizador de exibição 3D é *alternado automaticamente para **Iray*** para carregá-lo e aplicá-lo.

<a name="camera"></a>

### Câmera

A principal diferença entre o OpenGL e o Iray em relação às configurações da câmera é como a *profundidade de campo* é gerenciada. Na verdade, sendo o Iray um renderizador fisicamente preciso, a profundidade de campo ocorre “naturalmente”, dependendo da *abertura* da câmera.

Os seguintes parâmetros estão disponíveis nas propriedades da câmera quando o renderizador Iray está selecionado:

* <b>Distância do foco</b>: a distância da câmera do ponto focal, isto é, onde a imagem está com a nitidez mais alta
* <b>Diâmetro da abertura</b>: o valor que orienta a abertura da câmera. Quanto menor o valor, mais nítidos serão os elementos da imagem antes e depois do ponto focal. Em termos mais simples, esse valor controla a intensidade do efeito da profundidade de campo

![Configurações da câmera](iray.resources/iray-05.png "Configurações da câmera")

<a name="environment"></a>

### Ambiente

Abra o menu <b>Ambiente</b> e selecione a opção <b>Editar</b> para exibir as propriedades do ambiente no painel <b>Propriedades</b>.

As seguintes propriedades estão disponíveis:

Domo

* <b>Tipo de cúpula</b>: define os objetos que delimitam a cena, na qual a textura do ambiente é projetada
  * *Esfera infinita*: ambiente esférico infinito
  * *Solo*: ambiente esférico infinito, mas com um plano terrestre texturizado
  * *Esfera*: domo em forma de esfera de tamanho finito de raio personalizado
  * *Esfera com solo*: cúpula em forma de esfera de tamanho finito com raio personalizado onde a parte inferior do ambiente é projetada no plano que divide as partes superior e inferior da esfera
  * *Caixa com chão*: cúpula em forma de caixa de tamanho finito com largura, height e comprimento personalizados, onde a parte inferior do ambiente é projetada no plano que divide as partes superior e inferior da caixa
* <b>Ângulo de rotação</b>: controla o ângulo de rotação da cúpula ao redor do *eixo Y*
* <b>Raio</b>: o raio da esfera (aplica-se apenas à *Esfera* e à *Esfera com chão* tipos de domo)
* <b>Largura</b>: a largura da caixa (aplica-se apenas à *Caixa com chão* tipo de cúpula)
* <b>Height</b>: o height da caixa (aplica-se somente à *Caixa com tipo de cúpula* terrestre)
* <b>Comprimento</b>: o comprimento da caixa (aplica-se somente à *Caixa com tipo de cúpula* terra)
* <b>Visualizar</b>: habilita uma sobreposição de cor falsa da geometria de ambiente de tamanho finito. Isso pode ser usado para alinhar a geometria com a projeção do mapa de ambiente capturado (aplica-se apenas à *Esfera*, *Esfera com solo* e *Caixa com solo* tipos de cúpula)

>[!NOTE]
>
> Para cúpulas de tamanho finito, toda a geometria da cena deve estar *fechada* dentro da cúpula.

Cúpula\
Os parâmetros a seguir se aplicam aos tipos de domo *Solo*, *Esfera com solo* e *Caixa com solo*:

* **Solo**: habilita o plano terrestre
* **Posição**: a posição da origem da cúpula finita (também se aplica ao tipo de cúpula *Esfera*)
* **Refletividade**: a opacidade e a tonalidade do reflexo do solo, em que preto significa que o reflexo não está visível
* **Textura reluzente**: a textura reluzente do reflexo do solo
* **Intensidade da sombra**: a opacidade da projeção de sombra no chão
* **Escala de textura**: controla o tamanho da projeção de textura do ambiente no chão (também se aplica ao tipo de domo *Esfera*)

O impacto de algumas dessas configurações é demonstrado abaixo:

+++Ambiente de exibição


<table>
  <tr>
    <td>
      <img src="iray.resources/iray-06.png" alt="Iray - Ambiente oculto">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="iray.resources/iray-07.png" alt="Iray - Ambiente visível">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![Iray - Ambiente oculto](iray.resources/iray-06.png "Iray - Ambiente oculto")

![Iray - Ambiente visível](iray.resources/iray-07.png "Iray - Ambiente visível")

+++

+++Habilitar plano do solo


<table>
  <tr>
    <td>
      <img src="iray.resources/iray-08.png" alt="Iray - somente esfera infinita">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="iray.resources/iray-09.png" alt="Iray - Esfera infinita com plano do solo">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![Iray - Somente esfera infinita](iray.resources/iray-08.png "Iray - Somente esfera infinita")

![Iray - Esfera infinita com plano do solo](iray.resources/iray-09.png "Iray - Esfera infinita com plano do solo")

+++

+++Girar ambiente
![Girar ambiente](iray.resources/iray-10.gif "Girar ambiente")



+++

+++Ajustar o plano do solo
![Reflexão do solo](iray.resources/iray-11.gif "Reflexão do solo")



+++

+++Ajustar esfera infinita
![Escala do ambiente (esfera)](iray.resources/iray-12.gif "Escala do ambiente (esfera)")



+++

+++Ajustar caixa delimitadora
![Escala do ambiente (cubo)](iray.resources/iray-13.gif "Escala do ambiente (cubo)")



+++

<a name="display"></a>

### Exibir

Essas opções exibem uma *sobreposição de texto* sobre a imagem renderizada com informações úteis sobre a renderização.

* <b>Tempo decorrido</b>: a duração da renderização em segundos. Esse temporizador e o processo de renderização serão interrompidos quando uma das condições finais for atendida
* <b>Iterações</b>: o número de iterações de amostragem executadas. Esse contador e o processo de renderização serão interrompidos quando uma das condições finais for atendida
* <b>Método de renderização</b>: o caminho de renderização usado. Para a maioria dos propósitos em uma máquina local, o Photoreal é usado
* <b>Resolução</b>: a resolução de renderização efetiva. Se a opção Usar resolução de janela nas propriedades da câmera estiver definida como Falso, a proporção da imagem será ajustada automaticamente para corresponder à proporção da resolução
* <b>Estatísticas de cena</b>: uma lista de estatísticas relacionadas à cena renderizada, que inclui contagem de triângulos e contagem de materiais entre outros dados

![Opções de exibição](iray.resources/iray-14.png "Opções de exibição"){width="512px"}

<a name="renderer"></a>

### Renderizador

Abra o menu <b>Renderizador</b> e selecione a opção <b>Editar</b> para exibir as propriedades do renderizador no painel <b>Propriedades</b>.

Renderização progressiva

* <b>Amostras mínimas</b>: o número mínimo de amostras por pixel a serem computadas antes de considerar os critérios para interromper a renderização progressiva
* <b>Máximo de amostras</b>: se este número de amostras por pixel tiver sido renderizado, pare a renderização progressiva automaticamente
* <b>Tempo máximo (segundos)</b>: tempo em segundos após o qual a renderização progressiva deve terminar automaticamente
* <b>Amostra cáustica habilitada</b>: aumente a amostra padrão com uma amostra cáustica dedicada. Caustics são um resultado da passagem de luz através de um objeto não opaco, portanto, é necessário apenas se um material [MDL](../../../mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md) que suporte translucidez for aplicado em qualquer objeto na cena
* <b>filtro de Firefly habilitado</b>: habilite o filtro de vaga-lumes, que usa um algoritmo predefinido para remover vaga-lumes na imagem computada à medida que a renderização avança. Firefly são artefatos visuais em que os *pixels isolados* de uma imagem são *visivelmente mais brilhantes* do que os vizinhos e são resultado de amostras de raios insuficientes para determinar com precisão a distribuição da luz
* Pós-denoiser\
  O renderizador Iray usa o algoritmo [NVIDIA Optix AI-Accelerated denoiser](https://developer.nvidia.com/optix-denoiser) para a negação iterativa de alta qualidade da imagem à medida que ela é renderizada.

  * <b>Habilitado</b>: permite que um *algoritmo de desativação* predefinido seja acionado em uma iteração de renderização definida e fique ativo até o *fim* da renderização
  * <b>Iniciar iteração</b>: se o desenrolador estiver habilitado, esta opção definirá a iteração na qual o processo de desenrolamento será iniciado. Isso pode impedir que a sobrecarga de desempenho do denoiser afete a interatividade, por exemplo, ao mover a câmera. Além disso, as primeiras iterações muitas vezes não são adequadas como entrada para o denoiser devido à convergência insuficiente, levando a resultados insatisfatórios.

O impacto de algumas dessas configurações é demonstrado nas comparações de imagem abaixo:

+++Amostrador cáustico


<table>
  <tr>
    <td>
      <img src="iray.resources/iray-15.png" alt="Iray - Renderização base">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="iray.resources/iray-16.png" alt="Iray - Amostrador cáustico ativado">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![Iray - Renderização base](iray.resources/iray-15.png "Iray - Renderização base")

![Iray - Amostra cáustica habilitada](iray.resources/iray-16.png "Iray - Amostra cáustica habilitada")

+++

+++filtro Firefly


<table>
  <tr>
    <td>
      <img src="iray.resources/iray-16.png" alt="Iray - filtro Firefly desabilitado">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="iray.resources/iray-17.png" alt="Iray - filtro de Firefly habilitado">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![Iray - filtro de Firefly desabilitado](iray.resources/iray-16.png "Iray - filtro de Firefly desabilitado")

![Iray - filtro de Firefly habilitado](iray.resources/iray-17.png "Iray - filtro de Firefly habilitado")

+++

+++Pós-denoiser


<table>
  <tr>
    <td>
      <img src="iray.resources/iray-17.png" alt="Iray - Pós-desabilitado">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="iray.resources/iray-18.png" alt="Iray - Pós-denoiser habilitado">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![Iray - Pós-denoiser desabilitado](iray.resources/iray-17.png "Iray - Pós-denoiser desabilitado")

![Iray - Pós-denoiser habilitado](iray.resources/iray-18.png "Iray - Pós-denoiser habilitado")

+++

*Material: MDL de vidro espesso* *disponível nas definições de núcleo de MDL* *da NVIDIA*

## Aceleração por hardware

O renderizador Iray oferece aceleração de hardware exclusivamente nas GPUs NVIDIA, o que oferece os seguintes benefícios:

* Aumento significativo da velocidade de renderização
* [Denoização acelerada por IA do Optix](https://developer.nvidia.com/optix-denoiser) (consulte “Pós-denoiser” na seção <b>Renderizador</b> desta página)

Você pode selecionar o hardware que deve ser usado pelo Iray para renderização na seção <b>Exibição 3D</b> da janela [Preferências](../../../interface/preferences-window/preferences-window.md), conforme mostrado na imagem à direita.

Quando uma GPU compatível é detectada, ela é listada nesta seção, é *selecionada automaticamente* por padrão e a CPU é desmarcada. Qualquer alteração manual substitui esse comportamento automático para que as alterações personalizadas sejam salvas para sessões futuras.

>[!NOTE]
>
> Se uma GPU com suporte for detectada e listada, recomendamos *deixar a CPU desmarcada*, pois usar a CPU para renderização Iray tem um *impacto significativo* no desempenho e na capacidade de resposta geral do aplicativo.

>[!WARNING]
>
> A aceleração por hardware da GPU usa a tecnologia [NVIDIA CUDA](https://developer.nvidia.com/cuda-zone). Verifique se o *driver gráfico está atualizado* para obter a melhor compatibilidade e confiabilidade. Localize o driver mais recente para sua GPU NVIDIA [aqui](https://www.nvidia.com/Download/index.aspx?lang=en-us).\
> Para configurações de várias GPUs, é recomendável *desabilitar o SLI* e selecionar apenas uma GPU para obter a melhor confiabilidade.

![Preferências de Iray](iray.resources/iray-19.png "Preferências de Iray")
