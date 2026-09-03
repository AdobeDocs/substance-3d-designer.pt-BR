---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/release-notes/version-12-1.html"
breadcrumb-title: ''
description: Consulte as notas de versão do Substance 3D Designer versão 12.1 para saber mais sobre novos recursos, aprimoramentos e correções de erros.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 12.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versão 12.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1381'
ht-degree: 0%

---


# Versão 12.1

O **Substance 3D Designer 12.1** traz muitos nós novos para gráficos de material de Substance, suporte ao formato de arquivo USD e mais interoperabilidade com o Stager.

Data de lançamento: *26 de abril de 2022*

## Recurso principal

### Novo conteúdo para gráficos de material de Substance

![](version-12-1.resources/version-12-1-01.png)

Muitos nós foram adicionados nesta versão. Você encontrará alguns novos padrões, novos ruídos, novos filtros, ...

Dê uma olhada nas páginas de nó vinculadas abaixo para obter exemplos da amplitude de saída que é obtida por esses novos nós poderosos!

* **Novos padrões**

  * Adicionamos um novo nó <b>Bloco aleatório 2</b> para gerar blocos adjacentes de tamanhos e proporções aleatórias, o que é muito útil para criar rapidamente grades totalmente irregulares com cantos inclinados e arredondados e chanfro.

    ![](version-12-1.resources/version-12-1-02.gif){width="640px"}
  * Novo padrão <b>Triangle Grid</b> para gerar uma grade feita de triângulos. Estamos usando-o no material abaixo para simular fácil e perfeitamente a granulação de couro. Este gerador representa uma superfície de vértices em espaço 3D e pode ser usado para criar uma variedade de estilos poligonais.

    ![](version-12-1.resources/version-12-1-03.png){width="640px"}
* **Novos ruídos**

  * Para lhe dar mais variedade, um conjunto de <b>15 novos Mapas de Desgaste</b> (Concreto, Vazamentos, Respingos Sujos, ...) foi adicionado à biblioteca.

    ![](version-12-1.resources/version-12-1-04.png){width="640px"}
  * Você também encontrará muitos <b>novos Ruídos 2D e 3D</b>, como o Voronoi (2D e 3D), o Voronoi Fractal (2D e 3D), o 3D Ridged Fractal e uma atualização do Ruído 3D Perlin atual (adicionando opções de divisão em blocos gráficos e absolutas).\
    Esses ruídos são todos mapeados no espaço 3D e oferecem vários estilos, permitindo maior variedade e controle, o que lhe dará muita escolha para criar o mapa perfeito para o seu material, como o mar e os painéis de ficção científica abaixo.

    ![](version-12-1.resources/version-12-1-05.gif){width="640px"}

    ![](version-12-1.resources/version-12-1-06.gif){width="640px"}
  * Uma coleção de <b>nós de Textura 3D</b> (Posição, SDF, Deslocamento) e <b>nós de Renderização 3D </b>(Superfície ou Volume) para criar e renderizar texturas 3D, que são um atlas das fatias de um modelo 3D.

    ![](version-12-1.resources/version-12-1-07.png){width="640px"}

* **Novos Filtros**

  * Com o nó <b>Corte automático</b>, você pode colocar uma forma no *centro* da imagem sem ser redimensionada ou redimensioná-la para caber no espaço. Por exemplo, sua forma pode ser ajustada livremente enquanto mantém uma posição e um tamanho consistentes quando dispersa.

    ![](version-12-1.resources/version-12-1-08.gif){width="640px"}
  * Com o nó <b> Extend Shape</b>, você poderá esticar uma seção de uma forma em uma direção e distância personalizadas.

    ![](version-12-1.resources/version-12-1-09.gif){width="640px"}
  * E com o nó <b>Rotação não uniforme</b>, você pode girar uma entrada de acordo com um determinado mapa.

    ![](version-12-1.resources/version-12-1-10.gif){width="640px"}
* **E também...**

  * Funções de atenuação (gráfico de função) que são muito úteis para direcionar um valor de uma forma não linear.
  * Por fim, esta versão também traz uma nova versão mais precisa do nó <b>Quantize</b>, bem como um novo filtro de utilitário <b>Tabela de área somada</b>.

### Melhorar a interoperabilidade

* **Suporte ao USD** Além do

  e

  formatos de arquivo, agora é possível importar e exportar arquivos do USD (

  ,

  ,

  ) para usá-los como recursos de seus gráficos de modelo de Substance, para cozimento ou na visualização 3D para mostrar seu material de Substance. Você também pode usar esse formato para exportar o gráfico de modelo de Substance ou o conteúdo da visualização 3D.
* <b>Enviar para o Stager\
  </b>Agora você pode enviar o material do Substance para o Stager com um clique, pois isso já era possível com o Sampler e o Painter. Graças a esse recurso, não é mais necessário publicar como SBSAR e carregar arquivos individuais (requer o Stager versão 1.2.0 com o novo gerenciador de material)

  ![](version-12-1.resources/version-12-1-11.gif)

### Diversos

* Se estiver trabalhando em tecidos, agora você pode exibir uma malha dedicada na exibição 3D para ver melhor como o material é renderizado em uma forma drapeada. Abra o menu <b>Cena</b> no painel de exibição 3D e selecione a opção <b>Pano</b> para exibir esse modelo.

  ![](version-12-1.resources/version-12-1-12.png){width="640px"}

* Também adicionamos alguns novos nós de gerenciamento de cena para gráficos de modelo de Substance. Esses nós permitem renomear, alterar a hierarquia, fundir ou expandir os elementos da cena para organizar a hierarquia de cenas. Há também um novo nó para definir a tabela dinâmica de um ou mais elementos de uma cena.

* Ao trabalhar em projetos no Designer, você pode encontrar avisos e mensagens de erro, que o notificam de um problema no projeto. Nesta versão, <b>melhoramos o sistema de gerenciamento de erros</b> para mostrar todos os erros e avisos no Explorer: tudo está listado em um só lugar e, portanto, é mais fácil verificar se o projeto contém problemas.

  ![](version-12-1.resources/version-12-1-13.png){width="640px"}

## Notas de versão

### 12.1.0

*(Lançado Em 19 De abril De 2022)*

<b>Adicionado:</b>

* [Principal] Novo conteúdo para gráficos de material
* [Principal] Enviar materiais para o Stager
* [Principal] Suporte a arquivos do USD
* [Principal] Melhore o relatório de erros na interface do usuário
* [Principal] Nós de gerenciamento de cena para gráficos de modelo
* [Conteúdo] Adicionar mais opções a Ruídos Perlin 3D (lado a lado, absoluto...)
* [Conteúdo] Novo nó Fractal de ruído ondulado 3D
* [Content] Novo nó Deslocamento de textura 3D
* [Conteúdo] Novo nó de posição de textura 3D
* [Content] Novo nó de superfície de renderização de textura 3D
* [Content] Novo nó de volume de renderização de textura 3D
* [Content] Novo Campo de distância sinalizado de textura 3D
* [Content] Novo nó Corte automático
* [Conteúdo] Novas funções de atenuação
* [Content] Novos nós de Extend Shape
* [Conteúdo] Novos mapas de Desgaste
* [Content] Novo nó de rotação não uniforme
* [Conteúdo] Novo filtro de Tabela de Área Somada
* [Content] Novo bloco gerador aleatório 2
* [Content] Novo gerador de padrão de Triangle Grid
* [Content] Nova versão do nó Quantizar escala de cinza
* [Conteúdo] Novos ruídos fractais de Voronoi e Voronoi (2D/3D)
* [Conteúdo] Limite: adicionar o modo de comparação “Inferior” e “Inferior e igual”
* [Conteúdo]&#x200B;[Exibição 3D] Adicionar um ajuste de malha para exibir tecidos aos recursos enviados
* [modelos Substance] Novo nó Expandir instâncias de grupo
* [modelos de Substance] Novo nó de Fuse
* [Substance models] Novo nó Renomear
* [Substance models] Novo nó Reparent
* [Substance models] Novo nó Definir tabela dinâmica
* [Modelos Substance] Atualização para SDK 1.6.0
* [ThirdParty] Atualização do Qt (e QtForPython) para a versão 5.15.8
* [Terceiros] Atualize o Python para a versão 3.9.9
* [Terceiros] Atualize o OpenSSL para 1.1.1 m
* [UI] Melhorar o comportamento do menu Nó ao clicar incorretamente
* [UI] Abrir subgrafos na mesma guia, mesmo que estejam fixados
* [UI] Botão Remover pino da barra de título do painel do Explorer
* [UI] Salvar a opção “Não exibir novamente” na tela de boas-vindas nas versões
* [Exibição 3D] Exibe a unidade de Grade na viewport quando o auxiliar “Eixo” está ativado
* [Automation] Fornecer ferramenta de linha de comando sbsbaker com Designer
* [Gerenciamento de cores] Implementar o novo back-end de GPU para Adobe ACE
* [Fogão] Adicionar uma opção para cozinhar um pacote sem carimbo de data e hora
* [Gráfico] Adicionar medalhas no gráfico FxMap
* [Biblioteca] Adicionar novo filtro para funções de atenuação
* [Player] Suporte ao USD
* [Properties] Adiciona um erro de aviso no parâmetro “PKG Resource Path” de um nó Bitmap quando o recurso não é encontrado
* [Substance Engine] Atualização para 8.4.1
* [Yebis] Avisa o usuário de que os pós-efeitos Yebis serão removidos na próxima versão
* [Documentação] Nova página “Avisos e erros”
* [Documentação] Nova página que descreve a herança em gráficos de Substance
* [Documentação] Atualizar seção &#39;Iray&#39;
* [Documentação] Atualizar seção &#39;Gráficos MDL&#39;

<b>Corrigido:</b>

* [UI] Problemas de recorte nas dicas de ferramentas de modelos na nova janela de gráfico
* [UI] Texto em branco de difícil leitura em nós ao usar o Modo escuro no macOS
* [IU] Problema de layout em algumas caixas de diálogo
* [UI] A mensagem de aviso aparece truncada ao criar o gráfico de função Substance no Explorer.
* [UX] O seletor de cores está se movendo para baixo em cada nova abertura
* [UX] A janela do editor de degradê se move para cima cada vez que é gerada
* [UX] As propriedades do gráfico não são exibidas automaticamente para pacotes carregados
* [Content] Mapeador de Flood Fill: seleção de entrada incorreta em um caso específico
* [Content] Flood Fill: Sangria de texto nos botões de parâmetros booleanos
* [Content] Intervalo incorreto do parâmetro Ângulo de luz de primeira amostra do nó Multiângulo para Normal
* [modelos Substance] Propriedades do nó mostra o identificador em vez do rótulo
* [Modelos Substance]&#x200B;[visualização 3D] Problema de atualização ao reabrir um projeto
* [Modelos Substance]&#x200B;[3Dview] Problema de atualização ao usar a visualização de wireframe
* [Parâmetros] Falha ao excluir entradas de gráfico em sucessão rápida em um caso específico
* [Parameters] Falha ao redefinir um parâmetro de instância ao editar sua descrição de referência
* [Bitmap] A detecção de UDIM não é acionada para arquivos de bitmap descartados no gráfico
* [Graph] Os nós de bitmap/SVG não são invalidados quando o recurso é modificado no disco após o carregamento do pacote
* [GraphRender] Vazamento de memória quando a avaliação do gráfico de Substance é cancelada
* [Localization] A cadeia de caracteres “Reprogramar todos os mapas para este recurso” está aparecendo deslocalizada
* [MDL] Parâmetro exposto inicializado como 0 se a entrada estiver conectada ao nó Ponto desconectado
* [Preferências] As dicas de ferramenta são exibidas mesmo quando o cursor está em um espaço vazio
* [Propriedades] Ao desfazer a alteração do valor do espaço de cores, o valor padrão é definido em um caso específico
* [Texto] Não é possível desfazer a opção de fonte para recurso de fonte ausente
