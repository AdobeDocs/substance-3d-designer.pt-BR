---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/all-changes.html"
breadcrumb-title: ''
description: Revise todas as alterações e atualizações nas versões do Substance 3D Designer para acompanhar a evolução e as melhorias de recursos.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > All changes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Todas as alterações
user-guide-description: ''
user-guide-title: ''
source-git-commit: e71846d2834d9c1979fe840f1cf9e321f2d4d93f
workflow-type: tm+mt
source-wordcount: '31814'
ht-degree: 0%

---


# Todas as alterações

## Versão 16

### 16.0.4

*(Lançado Em 2 De julho De 2026)*

**Adicionado:**

* [Exibição 3D] Aumente a resolução da renderização para 4096 em X e Y
* [Bakers] Atualize o bake-sdk para 3.22.3
* [Engine] Atualize o mecanismo de Substance para a versão 9.4.4
* [OpenGL]&#x200B;[OpenPBR] Reduza o ruído no lóbulo do specular para obter mais rugosidade + anisotropia
* [Cenas] Preservar o modo de interpolação primvar UV

**Corrigido:**

* [3D View] Exportação em USD: o caminho dos recursos é armazenado com o caminho absoluto
* [Padeiros] Falha no cozimento quando o carregamento da malha alta poli é cancelado (Windows)
* [Padeiros] A lista de cenas 3D de alta poli não inclui recursos com o mesmo identificador de baixa poli
* [Padeiros] Espaço de mundo normal: um WS normal é sempre retornado quando há uma entrada normal
* [Content] Normal incorreto ao dimensionar o padrão de forma não uniforme no respingo de forma V2
* [Content] respingo de forma V2: normais pretos para as formas “Plano” e “Disco”
* [Conteúdo] respingo de forma v2: a primeira forma não é mesclada corretamente com o plano de fundo
* [Falha] Falha aleatória possivelmente vinculada ao vídeo (dicas de ferramentas avançadas)
* [Graph] Falha ao colar um nó copiado de um novo gráfico com identificador em branco
* [PSD] Os arquivos de PSD são carregados muitas vezes

### 16.0.3

*(Lançado Em 29 De maio De 2026)*

**Corrigido:**

* [Falha] Corrigir uma regressão introduzida na v16.0.2 que causa uma falha na inicialização para alguns usuários

### 16.0.2

*(Lançado Em 28 De maio De 2026)*

**Adicionado:**

* [OpenPBR] Adicionar suporte para constantes de cor base/AO

**Corrigido:**

* [Exibição 3D] Vazamento de VRAM no rastreador de caminho de GPU quando o deslocamento está habilitado
* [Exibição 3D] O thread principal permanece ocupado quando a Exibição 3D existe
* [3D View]&#x200B;[OpenPBR] OpenGL: Os widgets de &#39;Peso&#39; parecem estar apertados, mas aceitam valores fora do intervalo
* [Falha] Falha ao mover a entrada referenciada em mais de um local por vez
* [Falha] Falha ao maximizar uma janela
* [Crash] Falha ao escrever TARGA ou BMP do padeiro
* [Falha] Falha aleatória ao exibir a visualização 3D
* [Gráfico] Ordem incorreta de pinos de E/S ao mover a E/S após editar identificadores
* [Linux]&#x200B;[Exportar] As caixas de diálogo “Publish sbsar” e “Enviar para” não adicionam a extensão de arquivo

### 16.0.1

*(Lançado Em 5 De maio De 2026)*

**Adicionado:**

* [Amostras] Adicionar uma amostra de material dedicada ao respingo de forma/SDF
* [Conteúdo] Visualizador 3D: Alterar o estado padrão
* [Conteúdo] Visualizador 3D: Adicionar ambiente padrão
* [Content] Mapeador de respingo de forma v2: adicionar parâmetro de centro de projeção por eixo para mapeamento triplanar
* [Content] Mapeador de respingo de forma v2: adicionar parâmetro de divisão em blocos gráficos
* [Conteúdo] respingo de forma v2: ativar a extrusão de forma por padrão
* [3DView] Suporte às GPUs Intel Panther Lake no Pathtracer
* [Exibição 3D] Melhorar dicas de ferramentas pop-up de formatação do &#39;Deslocamento&#39;
* [Engine] Atualização para o Substance Engine v9.4.3
* [OpenPBR] geometry_tangent: adicionar suporte para constantes
* [Preferências] Adicione uma opção para que TGA/BMP grave o canal alfa se estiver totalmente opaco
* [ThirdParty] Atualização para “Adobe Color Engine” (ACE) 7.0
* [IU] Tornar a janela Gerenciador de plug-ins sempre visível (modal)

**Corrigido:**

* [Visualização 3D] O dimensionamento da janela de visualização é aplicado ao usar resolução fixa
* [Exibição 3D]&#x200B;[OpenPBR] Congela ao carregar uma cena GLTF exportada do Designer e usar um material de OpenPBR
* [Exibição 3D]&#x200B;[OpenPBR] Os materiais exportados do Painter não podem ser substituídos no Designer
* [Content] 3D Viewer: shape.id não é inicializado e gera mensagens no console
* [Content] Shape splatter v2 mapper grayscale: entrada de padrão 4 não é usada em projeção triplanar
* [Content] Mapeador de respingo de forma v2: a ID do SDF é deslocada por -1 ao usar o modo “1 imagem por ID de material”
* [Eclair]&#x200B;[USD] resultado incorreto ao aplicar um material em um USD gerado pelo Designer
* [Engine] Computação de um novo nó Níveis Shape splatter V2 gráfico principal embaralhado após cálculos
* [Engine] O módulo de uma variável em relação a seu valor igual não retorna 0 com o mecanismo de GPU em alguns casos
* [Engine]&#x200B;[Content] Arc tangent 2 retorna 0 ou Pi para vetores X-right em um caso específico
* [Engine]&#x200B;[Ubuntu]&#x200B;[SSE2] Falha ao carregar um SBSAR específico no gráfico
* [Graph] Falha ao conectar a saída do Processador de valor à entrada de bitmap
* [Graph] Falha ao conectar o valor à entrada da imagem em alguns casos
* [Graph] O gráfico é calculado automaticamente em cada salvamento automático ao usar mapas baked
* [GraphRender] Falha ao conectar a saída de valor do Atlas scatter à entrada de imagem do Atlas splitter
* [Linux]&#x200B;[Exportar] O formato de arquivo editado é ignorado nas caixas de diálogo de salvamento de arquivo
* O pop-up de segurança do [Mac]&#x200B;[Steam] é exibido quando iniciamos o Designer
* [Mesh] Os materiais OBJ não são importados corretamente
* [PSD] Solicitações do importador de PSD para extrair camadas do arquivo PSD em cada salvamento automático

### 16.0.0

*(Lançado Em 14 De abril De 2026)*

**Adicionado:**

* [Content] Nó v2 de respingo de forma
* [Conteúdo] Nós de cores/tons de cinza do mapeador de respingo de forma v2
* [Conteúdo] respingo de forma v2 para nó de máscara
* Nós de Grade de atlas [Content]
* [Conteúdo] Nó do visualizador 3D
* [Content] Nós do operador SDF 3D
* [Conteúdo] Nós primitivos SDF 3D
* [Conteúdo] Nós de transformação 3D SDF
* [Content] Nós de material SDF 3D
* [Content] Ângulo para nó de vetor
* [Content] Nós de valor constante
* [Visualização 3D] Sombreador de OpenPBR para renderizador OpenGL
* [Visualização 3D] Sombreador de OpenPBR para renderizadores Rasterizador e GPU Pathtracer
* [Visualização 3D] Janela do Deslocamento para definir a escala do height, o nível do height e o mosaico
* [Exibição 3D] Reorganizar os itens da barra de ferramentas
* [Visualização 3D] Definir OpenPBR como o modelo de material padrão na Visualização 3D
* [3D View] Fazer com que a visualização 3D leve em consideração o atributo do gráfico “Modelo de material”
* [Exibição 3D] Sincronizar modelos de material ao alternar entre os renderizadores Rasterizador/GPU Pathtracer e OpenGL
* [Exibição 3D] Garanta que o modelo de material seja persistente ao alternar renderizadores 3D e alterações de definição de material estejam sincronizadas
* [Exibição 3D] GPU Pathtracer: ativar ciclo de pixel de ruído azul
* [Exibição 3D] Expor controle de opacidade de oclusão ambiente
* [3D View] Define o intervalo do parâmetro &#39;Tiling&#39; como [0, 10] para todos os sombreadores
* [Exibição 3D] Renomear a ação “Foco” como “Quadro”
* [Visualização 3D] Manipular o novo parâmetro refineLevel que substitui tessellationFactor
* [Exibição 3D] Adicionar contador de FPS
* [Visualização 3D] Mova a barra de progresso na mesma barra de ferramentas horizontal que o espaço de cores na parte inferior
* [Padeiros] Exibir o UV do padeiro selecionado na visualização
* [Graph] Adicionar novo atributo &#39;Modelo de material&#39; aos gráficos de Substance
* [NewGraph] Adiciona separadores na visualização de miniaturas
* [Parâmetros] Defina o valor de constante padrão para parâmetros de entrada com o editor &#39;Function&#39;
* [Parâmetros] Preencha a caixa de combinação dos parâmetros de nó `Set` e `Is defined` com as variáveis disponíveis
* [Preferências] Remover a opção obsoleta “Fator de desescala” na guia “Visualização 3D”
* [Publish] Caixa de diálogo Publish: incluir modelo de material nas informações do gráfico
* [Python] Adicionar nova classe SDMaterialModelDescription para obter as informações de um modelo de material
* [Python] Permite obter/definir a propriedade modelo de material de objetos SDSBSCompGraph
* [Editor Python] Aumentar tamanho da fonte para 12
* [Modelos] Adicionar modelos de OpenPBR
* [Modelos] Converter amostras de material em OpenPBR
* [ThirdParty] Atualizar o impulso para a versão 1.88
* [Terceiros] Atualizar API C++ para C++ 20
* [ThirdParty] Atualize o NGL para 1.42
* [Terceiros] Atualize uma versão para a versão 2022.x
* [ThirdParty] Atualizar o OpenColorIO para a versão 2.5.x
* [Terceiro] Atualizar o OpenEXR para a versão 3.4.x
* [ThirdParty] Atualize Qt e QtForPython para 6.8.x e Python para 3.13.x
* [Terceiros] Atualize o TBB para oneTBB 2021.x
* [Descontinuação] Remover Iray e o Editor de MDL

**Corrigido:**

* [2D View] O intervalo de seleção do histograma não é preservado quando a largura do widget se torna pequena
* [Exportação 3D] As malhas exportadas do Designer não renderizam o mesmo no usdview
* [Exibição 3D] Atribuir objetos não udim à Exibição 3D deixa o modo de renderização de bloco único
* [Exibição 3D] Resultado apertado ao usar o OCIO
* [Exibição 3D] Falha ao aplicar uma textura de gráfico em um material não substituído para uma cena específica
* [3D View] Falha ao criar buffers de quadro
* [3D View] Eclair GPU Pathtracer: geometria quebrada e baixo desempenho ao renderizar um modelo específico
* [Visualização 3D] Transformação de textura incorreta para cena(s) específica(s)
* [Exibição 3D] Enquadramento inconsistente de cena/seleção ao usar a resolução de renderização fixa
* [Exibição 3D] Cor difusa incorreta ao renderizar determinado arquivo GLTF
* [Exibição 3D] Ambiente invisível ao alternar renderizadores em um caso específico
* [3D View] Os materiais não são detectados corretamente quando importados alguns arquivos .fbx
* [Exibição 3D] Substituir materiais mais de uma vez redefine a divisão em blocos gráficos para 1
* [Exibição 3D] As propriedades na categoria “UVs” não são salvas em arquivos SBSSCN
* [Exibição 3D] “Redefinir e exibir saídas na exibição 3D” de gráficos de saída única não redefine materiais
* [Exibição 3D] “Salvar renderização”: o formato de imagem editado não é preservado
* [Exibição 3D] A seleção não funciona em GPUs AMD
* [Exibição 3D] A cena 3D independente não é atualizada quando modificada no disco
* [Exibição 3D] Algumas propriedades do material de cores não são gerenciadas corretamente quando substituídas
* [Exibição 3D] As texturas UDIM não são aplicadas corretamente em uma malha específica
* [Exibição 3D] A cena com material MaterialX no USD não é mais renderizada corretamente
* [Padarias] Falhas com algumas malhas
* [Bakers] Transferência de textura: Falha em bkBufferViewCopy
* [Cooker] Loop infinito no nó de Loop While em um caso que poderia ser evitado
* [Engine] Parar o mecanismo Substance ao fechar o aplicativo
* [Geral] Evitar falhas aleatórias ao sair do aplicativo (somente Windows)
* [Graph] Gráfico de função: a propagação de tipo não funciona corretamente em algumas situações
* [Gráfico] Os vínculos de gráfico são excluídos quando um nó de entrada de imagem é renomeado
* [Gráfico] Links e pinos às vezes exibem artefatos
* [Preferences] &#39;Viewport scaling&#39; é invertido
* [Propriedades] Falha ao modificar o ajuste de entrada do gráfico ao exibir seus parâmetros de instância
* [Python] Não é possível importar módulos PySide6 (possível conflito com a instalação existente do PySide6)
* [Python] Os módulos existentes do PySide e do Shiboken entram em conflito com os
* [UI] O estilo hover desaparece nos botões em casos específicos (somente Windows)
* [UI] O estilo de foco não é visível nos botões suspensos quando clicados (somente no macOS)
* [UI] O botão “Saiba mais” na dica de ferramenta “?” não funciona quando a dica de ferramenta está fora dos limites da caixa de diálogo (somente Windows)

**Problemas conhecidos:**

* [Gráfico] Os ícones gerados para gráficos de OpenPBR não são precisos
* [Exibição 3D] As cenas com primitivas animadas não são suportadas corretamente
* [Exibição 3D] Não há suporte para Pathtracer em todas as placas gráficas AMD

## Versão 15

### 15.1.3

*(Lançado Em 10 De março De 2026)*

**Adicionado:**

* [Padeiros] Adicionar macros outputsize para o nome do arquivo
* [Padarias] Evite carregar a malha de alta pressão antes de assar
* [Bakers] CLI: Atualizar a descrição da opção &#39;output-size&#39; com macros de tamanho
* [Padeiros] Converta o formato de textura de entrada para o formato solicitado
* [Padeiros] Desabilitar a opção &#39;Deslocar mapa&#39; quando a opção &#39;Usar gaiola&#39; estiver marcada
* [Padeiros] Exibir os mapas baked quando a janela de cozimento for reaberta
* [Padarias] Mantenha a janela da panificação aberta até que todos os processos de panificação sejam efetivamente cancelados
* [Bakers] função Migrar BindTexture
* [Padeiros] [Configurações] Define o valor padrão de &#39;Modo de filtragem de nome&#39; como &#39;Nome do pai (legado)&#39;
* [Padeiros] [Dica de ferramenta] Adicionar o valor &#39;Modo de filtragem de nome&#39; à dica de ferramenta do parâmetro &#39;Corresponder&#39;
* [Engine] Atualização do mecanismo de Substance para a versão 9.3.4

**Corrigido:**

* [Visualização 3D] “Visualizar saídas na visualização 3D” não substitui a atribuição existente em gráficos com saída única
* [Exibição 3D] Não é possível exibir UVs em alguns casos
* [Exibição 3D] As tangentes calculadas aparecem quebradas para USD
* [Exibição 3D] Falha ao abrir o menu Renderizador
* [Padeiros] Não é possível definir uma distância maior que 1 quando a opção “Em relação à caixa” está desmarcada
* [Padeiros] O acabamento do padeiro a cores é excessivamente demorado em casos específicos
* [Padarias] Cor: falha ao assar Ilhas UV
* [Padeiros] Os intervalos de parâmetros de distância e raio são muito estreitos quando o valor é absoluto
* [Padeiros] Falha ao assar a partir de alto poli tangente ausente e bitangents que não são necessários
* [Padeiros] As cores do material não estão corretas na linha de comando do padeiro
* [Padeiros] Várias malhas de alta poli são ignoradas em algumas situações
* [Padeiros] Normal: saída em preto ao usar suavização de borda e difusão (somente macOS)
* [Bakers] A verificação do caminho do mapa de deslocamento relata falhas inesperadas ao usar recursos de pacote de bitmap
* [Padeiros] A dica de ferramenta do mapa de deslocamento está incorreta
* [Padeiros] Colocar recurso em uma pasta de malha específica não funciona
* [Padeiros] Transferência de textura: o valor “conjunto UV” não é restaurado como era ao reabrir a janela de cozimento
* [Padarias] Transferência de textura: uma entrada em tons de cinza não resulta em uma saída em tons de cinza
* [Bakers] Aviso para padeiro herdado desativado não é limpo ao alterar a origem da textura no padeiro de destino
* [Padeiros] [UDIM] O mapa de deslocamento é aplicado apenas ao UDIM 1001
* [Graph] O UDIM 1001 é sempre calculado independentemente do UVTile usado

### 15.1.2

*(Lançado Em 3 De fevereiro De 2026)*

**Corrigido:**

* [Engine] Níveis: Os valores de ponto flutuante são sempre fixados em [0, 1]
* [Padeiros] A correspondência de geometria por nome de pai (herdado) não funciona para submalhas
* [Padeiros] Cor: as edições de cores materiais na interface são ignoradas
* [3D View]&#x200B;[Bakers] O arquivo OBJ leva muito tempo para ser carregado

### 15.1.1

*(Lançado Em 20 De Janeiro De 2026)*

**Adicionado:**

* [Amostras] Adicione duas amostras para criar seções para alimentar a ferramenta da faixa de opções Painter
* [Engine] Atualização para o Substance Engine v9.3.2
* [Engine]&#x200B;[Metal] Melhorar o desempenho
* [Engine] A interpolação bilinear de texturas de inteiros agora é executada com maior precisão (backend da CPU)
* [Padeiros] Registrar um aviso se a cor do vértice estiver ausente da malha alta de poli
* [Marca] Atualizar ícones de tipos de arquivo
* [NewGraph] Aplicar estilos hover no ícone (i) nos modos de exibição &#39;Lista&#39;, &#39;Pacotes&#39; e &#39;Diretórios&#39;

**Corrigido:**

* [3DView] As malhas UDIM não estão mais renderizando um único bloco
* [3DView] Falha quando nenhum renderDevice é detectado
* [Identidade visual] Corrigir ícones para arquivos .SBS no Linux
* [Content] RGB para função HSL: resultado incorreto para entradas próximas a 0
* [Gráfico] O gerador de ícones/miniaturas do gráfico não funciona
* [Gráfico] Menu Nó: itens agrupados sem miniatura não têm recuo
* [Engine]&#x200B;[Content] Color to mask v2: Artefatos no mecanismo SSE2 ao usar o espaço de cor de distância Lab
* [Engine]&#x200B;[Content] Color to mask v2: Artefatos em mecanismos de GPU arm64 ao usar o espaço de cores de distância Lab
* [Engine]&#x200B;[Metal] Saída de irradiância preta para o nó Renderização PBR
* [Engine]&#x200B;[Mac] Resultado incorreto em uma função de processador de pixels no Metal
* [Engine]&#x200B;[Mac] Melhore a precisão de algumas instruções usadas em processadores Pixel em GPUs Apple Silicon M1/M2
* [Engine] O redimensionamento de imagens de entrada (ou recursos incorporados) não introduzirá mais artefatos de borda (back-end de CPU)
* [Engine] O filtro de níveis não fixará mais seus valores de entrada de ponto flutuante ao gerar texturas 8I/16I (back-end da CPU)
* [Engine] Correção de um erro de FxMaps em que imagens de entrada em tons de cinza consumidas por nós FxMaps podiam ter uma amostra incorreta (back-end de CPU)
* [Engine] Alguns artefatos corrigidos na versão de propagação 1 do filtro Distância (infraestruturas de GPU)

### 15.1.0

*(Lançado Em 11 De dezembro De 2025)*

**Adicionado:**

* [NewGraph] Retrabalho da janela do novo gráfico
* [NewGraph] Adicione amostras de materiais e amostras avançadas
* [NewGraph] Adiciona um novo atributo para o gráfico para os dados do modelo (categoria e sub- título)
* [NewGraph] Remover opção de formato de saída
* [Conteúdo] Adicionar funções de hash
* [Content] Adicionar mapeadores de tons a functions.sbs
* [Content] Ruído anisotrópico v2: adicionar formato de saída padrão, adicionar distúrbio
* [Content] Aplique capitalização de sentença a rótulos de nó e parâmetros
* [Content] BnW spots 1 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] BnW spots 2 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] BnW spots 3 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] Células 1, 2, 3, 4 v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos, opções de desordem
* [Content] Nuvens 1 v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos
* [Content] Nuvens 2 v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos
* [Content] Nuvens 3 v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos
* [Conteúdo] Cor para mascarar v2
* [Content] Ruído direcional 1 v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos
* [Content] Ruído direcional 2 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] Ruído direcional 3 v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos
* [Content] Ruído direcional 4 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] Arranhões direcionais v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos
* [Content] Dirt 1 v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos
* [Content] Dirt 2 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] Dirt 3 v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos
* [Content] Dirt 4 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] Dirt 5 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Conteúdo] Degradê de Dirt v2: adicionar formato de saída padrão, novas opções de doença
* [Content] Soma fractal Base v2: adicionar formato de saída padrão, distúrbio, sem suporte a divisão em blocos gráficos
* [Content] Soma fractal 1, 2, 3, 4 v2: adicionar formato de saída padrão
* [Content] Ruído gaussiano v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] Manchas gaussianas 1 e 2 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] Messy fiber 1,2,3 v2: adicionar formato de saída padrão, sem suporte a azulejos, opções de desordem
* [Content] Ruído por umidade v2: adicionar formato de saída padrão, sem suporte para revestimento
* [Content] Novo nó “Umidade noise 2”
* [Content] Ruídos: atualize para adicionar um formato de saída padrão
* [Content] Perlin noise v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Conteúdo] Mapeador de formas: adicionar modo de filtragem
* [Content] Mapeador UV: adicionar modo de filtragem
* [Content] Forma de onda 1 v2: usar formato de saída padrão + novas opções
* [Content] White noise v2: usar formato de saída padrão, adicionar opções de distribuição
* [Padeiros] Exibir os UVs somente da malha selecionada
* [Padeiros] Adicione uma opção para selecionar o método de correspondência de geometria por nome
* [Padeiros] Selecione o Padeiro mais próximo quando um padeiro é excluído
* [Padarias] UDIM: defina uma lista de blocos UV para assar
* [Bakers] Atualize o bake sdk para 3.15.4
* [3D View/SceneBrowser] Evite selecionar um UsdPrimitive ao fazer um clique com o botão direito nele
* [ColorManagement] Suporte para ACES 2.0
* [Gráfico de composição] Permite definir um nó de saída como a “Saída padrão”
* [Fogão] Remover aviso sobre entradas desconectadas de instâncias de função¬†
* [Funções] Adicionar operador isDefined
* [Graph] Agrupar os itens por atributo &#39;group&#39; no menu do nó
* [Gráfico] Melhorar a renderização de miniaturas

**Corrigido:**

* [3D View] A textura da Escala de cinza L16 é exibida com uma tonalidade vermelha quando conectada ao ambiente ou à baseColor
* [Exibição 3D] Alterar a vinculação de material de uma cena sem material cria um novo material “padrão”
* [3D View] As normais computadas não são corretas para malhas OBJ específicas
* [Exibição 3D] O ambiente personalizado de SBSSCN não é visível no carregamento no Pathtracer
* [Visualização 3D] Erros no console ao girar um ambiente desativado
* [Exibição 3D] O Specular level não foi aplicado corretamente
* [Exibição 3D] O Specular edge color não funciona ao usar o rasterizador de Eclair
* [Exibição 3D] O material adicionado do usuário não é aplicado em cenas padrão
* [3D View]&#x200B;[Padarias] A cor do material fica muito escura depois de substituída ou ao usar um padeiro “Colorido”
* [Exibição 3D]&#x200B;[Padeiros] Sem cor material do arquivo FBX
* [Padeiros] As cores do material em arquivos FBX não são detectadas corretamente
* [Bakers] A opção &#39;recompute\_tangents&#39; é sempre &#39;false&#39; nas exportações predefinidas JSON
* [Bakers] CLI: Falha ao executar o mesmo panificador consecutivamente através do arquivo JSON
* [Padeiros] A atualização do parâmetro &#39;color-generator&#39; não funciona para &#39;Grayscale&#39;
* [Conteúdo] Máscara para caminhos: falha em proporções não quadradas
* [Content] Renderizador de Renderização PBR/ícone: função incorreta do lobo de specular
* [Content] Caminhos para spline: defina o &#39;Tamanho de saída&#39; como &#39;Em relação ao pai&#39; por padrão
* [Content] Lista de pontos: os pontos não estão na ordem correta quando a textura dos dados é não quadrada
* [Content] Mapeador de spline: falha de linha de 1 px em casos aleatórios
* [Content] Mapeador de spline: UVs esticados em alguns casos quando o thickness é 0
* [Graph] Falha ao excluir a saída de um subgrafo de função
* [Graph] O tipo de cor do nó de entrada pode ser alterado em pacotes somente leitura
* [Graph] A entrada principal pode ser alterada em pacotes somente leitura
* [Propriedades] A cor do widget de visualização de cor não corresponde ao estado do botão sRGB
* [Cena] Não é possível carregar um arquivo OBJ maior que 2 GB
* [IU] Os estados de encaixe do console e do gerenciador de dependências não são restaurados após a reinicialização

### 15.0.3

*(Lançado Em 23 De outubro De 2025)*

**Corrigido:**

* [Conteúdo] A saída de visualização de nós do Ferramenta de linha flexível não é exibida por padrão
* [Graph] Falha ao excluir a saída de um subgrafo de função

### 15.0.2

*(Lançado Em 18 De setembro De 2025)*

**Adicionado:**

* [3D View/OpenGL] Remove o efeito de wireframe aplicado na malha selecionada
* [Exibição 3D] Permitir o uso da tecla “F” para focalizar em uma malha selecionada quando o Navegador de cena tiver foco
* [Exibição 3D] A renderização não é atualizada ao alterar o formato de mapa normal
* [BakersCLI] Adicionar opção para controlar o tamanho do cache de superfície
* [BakersCLI] Renomeie a opção “use\_cache” para “keep\_meshes\_in\_cache”
* [IU] Ícone de atualização para cenas 3D na Biblioteca

**Corrigido:**

* [Visualização 3D] Falha ao atribuir um nó de material a uma cena de vários materiais
* [Exibição 3D] O gráfico criado a partir de entradas de textura é sempre exibido na Exibição 3D, independentemente das preferências
* [Exibição 3D] Uso incorreto em uma dica de ferramenta de emblema “Exibido na Exibição 3D” em um caso específico
* [Exibição 3D] Muitos erros de USD ao substituir cenas específicas
* [Exibição 3D] Artefatos de sombra ao usar o deslocamento em uma cena plana no rasterizador
* [Visualização 3D] Algumas cenas específicas não são visíveis ao usar o renderizador OpenGL
* [Exibição 3D] A caixa de diálogo usada para “Selecionar o Gráfico do Substance de destino” sempre tem o ícone de gráfico “Pendente”
* [Exibição 3D] O menu contextual do visor não é exibido para cenas específicas
* [Exibição 3D] Os emblemas “Exibido na Exibição 3D” não são apagados ao alternar cenas em um caso específico
* [Exibição 3D] Cor lavada na exibição 3D ao usar o gerenciamento de cores Adobe ACE
* [Exibição 3D]&#x200B;[Linux] Várias cenas renderizam em preto no renderizador OpenGL
* [Exibição 3D]&#x200B;[Navegador de cena] As teclas de seta movem a seleção para a raiz
* [BakerCLI] Não é possível substituir alguns parâmetros
* [Padeiros] Artefatos em dilatação ao usar padeiros normais com suavização de serrilhado
* [Padeiros] O processo de cozimento parou repentinamente no CLI ao assar uma quantidade alta de UDIMs em 4K
* [Padeiros] Falha ao empurrar o padeiro para baixo na lista de padeiro em caso específico
* [Padeiros] Opções de seleção de formato de .surface para .dds
* [Padarias] Congelar ao assar uma quantidade alta de UDIMs em 4K
* [Bakers]&#x200B;[macOS] Falha ao assar transferência de textura com antialitização
* [Content] Lista de pontos: os pontos não estão na ordem correta quando a textura dos dados é não quadrada
* [Content] Visualizar paleta de cores: os nós internos são computados em resoluções muito altas
* [Data] Falha ao renomear a saída para corrigir a saída fantasma em instância
* [Engine] Distância: a luminância da máscara de entrada é alterada
* [FxMap] $tiling não tem efeito se o FX-Map estiver em um subgrafo
* [Graph] A pesquisa difusa retorna resultados irrelevantes
* [Editor Python] Os scripts carregados não são reabertos entre as sessões

### 15.0.1

*(Lançado Em 22 De julho De 2025)*

**Adicionado:**

* [Exibição 3D] Permita a texturização de malhas USD que têm displayColor e sem vinculações de material
* [Exibição 3D] Não crie automaticamente um material por malha que não tenha uma ligação de material
* [Exibição 3D] Renomear “amostras de pixels convergidos” para “amostras”
* [Exibição 3D] Renomeie o parâmetro “Escala UV ativada” para “Ativar Tamanho físico do gráfico”
* [Exibição 3D] Reduza a intensidade do deslocamento de acordo com o parâmetro “Lado a lado”
* [3D View/OpenGL/Iray] Adicionar uma mensagem no visor quando o ambiente padrão estiver desativado
* [Padeiros] Use ícones para botões a fim de reordenar linhas na lista de renderização Padeiros
* [Preferências] Adicionar uma opção para definir o renderizador de exibição 3D padrão
* [Propriedades] Fazer com que “Redefinir para padrão” use os valores padrão criados, se houver

**Corrigido:**

* [Exibição 3D] Artefatos em uma cena específica quando renderizados com o OpenGL
* [3D View] O ambiente padrão não é desativado ao carregar um recurso de cena 3D USD que contém um
* [Visualização 3D] A exibição do menu contextual da viewport leva vários segundos em cenas grandes
* [3D View] “Intensidade emissiva” é 0 ao substituir materiais não USD usando apenas “Cor emissiva”
* [Exibição 3D] Os canais vermelho e azul são trocados em textura de 8 bits usada como ambiente
* [Exibição 3D] Arrastar e soltar RMB não funciona consistentemente por causa do registro do clique com o botão direito
* [Exibição 3D] “Mostrar apenas” no subconjunto oculta sua malha pai
* [Visualização 3D] As cenas padrão carregadas de um arquivo aparecem com uma cor base incorreta
* [3D View] A propriedade “Escala UV” é redefinida ao alternar do OpenGL para outro renderizador e vice-versa
* [Exibição 3D]&#x200B;[Iray] Os renderizadores geralmente são desfocados e pixelados
* [Padeiros] Artefatos ao usar a difusão em uma GPU AMD
* [Padarias] A cozedura falha em algumas cenas de conjuntos UV diferentes de 0
* [Bakers] &#39;Textura transferida&#39;: a lista &#39;Conjunto UV&#39; não leva em consideração a opção &#39;Usar baixo como alto poli&#39;
* [Padeiros] A seleção de blocos UV é sempre redefinida como “Todos”
* [Graph] Falha ao excluir um nó no contexto
* [Mac OS]&#x200B;[Exibição 3D] Resolução de renderização incorreta em telas mac
* [Parâmetros] Os parâmetros modificados não são estilizados na primeira exibição
* [UX] Os itens desativados no menu suspenso ficam invisíveis

### 15.0.0

*(Lançado Em 15 De julho De 2025)*

**Adicionado:**

* [Exibição 3D] Renderizador completamente novo, com modos rasterizador e rastreador de caminho
* [Visualização 3D] Adicione uma ferramenta de seleção para escolher um objeto na cena 3D
* [Exibição 3D] Adicionar nova “Exportar cena com camadas...” ação no menu “Cena”
* [Visualização 3D] Adicionar novos botões da barra de ferramentas
* [Exibição 3D] Adicione a possibilidade de alternar entre várias câmeras contidas em uma cena do USD
* [Visualização 3D] Permita que o foco se concentre no objeto selecionado ao pressionar “F” na janela de visualização
* [Exibição 3D] Permite gerar um Substance Gráfico de composição a partir de um material existente
* [Exibição 3D] Permite enviar um Gráfico de composição SBS na Exibição 3D e atribuir sua saída exclusiva ao uso de Ambiente/Panorama
* [Visualização 3D] Limpe a seleção atual pressionando a tecla Escape
* [Visualização 3D] Exibir uma cena 3D importada com texturas
* [Visualização 3D] Distinguir controles de repetição de textura X e Y
* [Exibição 3D] Ativar/desativar sombras
* [Exibição 3D] Ativar/desativar plano terrestre
* [Exibição 3D] No menu “Materiais”, adicione “Remover” apenas para os Materiais que foram adicionados manualmente e não são usados
* [Exibição 3D] No menu “Materiais”, remova a ação “Remover tudo”
* [Visualização 3D] Tornar arquivos USDZ exportados independentes
* [Exibição 3D] Tornar as propriedades do renderizador persistentes ao alternar o modo de renderizador
* [Exibição 3D] Preservar as entradas de material existentes ao substituir um Material
* [Exibição 3D] Reorganizar propriedades da câmera
* [Exibição 3D] Remover ações “Câmera/Salvar captura de tela...” e “Captura de tela da câmera/cópia para a área de transferência”
* [Exibição 3D] Remover a ação de menu “Material/Reconstruir tudo”
* [Visualização 3D] Remover o prefixo “Padrão” do rótulo da câmera padrão
* [Exibição 3D] Defina a ação do menu “Redefinir para valor padrão” como a última no menu de hambúrguer de propriedade de entrada de material
* [Exibição 3D] Ajustes de atalho
* [Visualização 3D] Suporte a sombras e translucidez no modo de tempo real
* [Visualização 3D] Compatibilidade com shaders MaterialX de uma cena importada em USD
* [3D View/OpenGL] Renomeie o parâmetro “Escala UV ativada” para “Ativar Tamanho físico do gráfico”
* [Exibição 3D/Pós-efeitos] Bloom
* [Visualização 3D/Pós-efeitos] Profundidade de campo
* [Visualização 3D/pós-efeitos] Mapeamento de tom
* [3D View / Navegador de cena] Permite exibir as propriedades do material ao selecioná-lo no Navegador de cena
* [Visualização 3D/Navegador de cena] Ocultar a coluna “Material”
* [Visualização 3D / Navegador de cena] Coloque em negrito as Primitivas do USD que são controladas por uma entidade Predefinida
* [Padeiros] Adicione um menu contextual na exibição de árvore com as ações “Selecionar tudo”/”Desmarcar tudo”
* [Padeiros] Adicione uma opção para controlar a interpolação de bitangente
* [Padeiros] Adicionar divisor horizontal na interface
* [Bakers] Adicione a macro UDIM por padrão no nome de saída quando a cena estiver udim
* [Padeiros] Permitir recalcular tangente
* [Padeiros] Permite renomear um padeiro sem quebrar as ligações
* [Padeiros] Alterar o tamanho padrão do painel do meio
* [Padeiros] Textura de entrada para fluxo de trabalho UDIM
* [Padeiros] Fazer com que a ordem da lista de mapas de exibição 2D corresponda à ordem da lista de renderização Padeiros
* [Padarias] Tornar modal a janela de cozedura
* [Padeiros] Gerenciar parâmetros de mapeamento de tons
* [Padeiros] Remover a seleção de plug-in do espaço tangente
* [Padeiros] Salvar status “enabled” ou “disabled” para Padeiros ao salvar uma predefinição
* [Padeiros] Selecione o material por padrão no widget de seleção
* [Padeiros] Defina a orientação padrão da textura de saída normal em relação à preferência
* [Padeiros] Por padrão, defina os blocos UV como Todos
* [Bakers] Opção de adição WordSpaceDirection FromTexture/FromValue
* [Bakers] Mundo à tangente: defina a entrada padrão como “de textura”
* [SBSBaker] Criar uma opção para controlar a ordem de backend
* [SBSBaker] Melhorar o uso do argumento StringList
* [SBSBaker] Renomear “match\_source\_instance” para “match\_mesh\_name”
* [SBSBaker] Renomear “Submesh” para “GeomSubset”
* [SBSBaker] Renomeie para substance3d\_baker
* [Conteúdo] Adicionar a forma &#39;Hemisfério&#39; aos nós geradores expondo as formas do Quadrante
* [Interop] Suporte ao formato de arquivo GLTF
* [Interop] Suporte ao formato de arquivo PLY
* [Interop] Suporte ao formato de arquivo STL
* [Biblioteca] Uniformizar dicas de ferramentas para nós atômicos
* [Mac] Parar de oferecer suporte à plataforma MacIntel
* [Nodes] Adicionar richtooltips para nós atômicos
* [Parâmetros] Fechar a seção &#39;Atributos&#39; por padrão
* [Parâmetros] Permite que o usuário especifique valores padrão de parâmetro base para novas instâncias
* [Preferências] Preparadores: adicione uma opção booleana para calcular o espaço tangente por fragmento
* [Preferências] Remover os plug-ins de espaço tangente
* [Preferências] Armazenar as preferências por versão secundária do SD (XX.X)
* [VFX] Atualizar o aumento para 1.85.0
* [VFX] Atualizar a versão mínima do MacOS para 12.0
* [VFX] Atualizar o OpenColorIO para 2.4.2
* [VFX] Atualizar o OpenColorIO para 2.4.x
* [VFX] Atualizar o OpenExr para 3.3.x
* [VFX] Atualize o Qt para 6.5.8

**Corrigido:**

* [Exibição 3D] As texturas na cena USD exportada não são aplicadas corretamente
* [Exibição 3D] [UDIM] Não é possível exibir as saídas de gráficos UDIM na Exibição 3D quando a exibição automática na abertura do gráfico está desativada nas preferências de gráfico
* [Padeiros] &#39;Suavização de borda.&#39; e &#39;Média as células normais de padeiros não aplicáveis ficam em branco e são editáveis
* [Bakers] A ação “Atualizar” usa a infraestrutura de rastreamento de raios quando está desativada nas preferências
* [Padeiros] Padeiros bloqueados como ocupados após falha durante o processo &#39;Atualizar todos os mapas baked&#39;
* [Bakers] Falha em mais de 180 UDIMs ao assar o mapa de posição OpenGL em uma malha específica
* [Padeiros] Falha ao abrir a caixa de diálogo “Informações do modelo de bolo” várias vezes seguidas (somente macOS)
* [Bakers] Na exportação predefinida JSON, o valor “udim” é substituído por “1001” quando foi definido como “Todos”
* [Bakers] A memória não é detectada corretamente no Linux
* [Padeiros] A dependência de entrada de mapa ausente não aciona o aviso e/ou a renderização de bloco
* [Padeiros] Nenhum rótulo de erro quando o nome de saída está vazio
* [Bakers] Alternar a malha alta poli do arquivo não tem efeito
* [Padeiros] O padeiro de destino não é selecionado por padrão ao usar a ação &#39;Reassentar&#39;
* [Engine] Distância: “corte” visível em algumas situações
* [Engine] Fx-Map: não há suporte para cores negativas quando a profundidade de bits é de 8 bits (somente mecanismos de GPU)
* [Localização] A entrada do caractere volta do japonês para o latim no menu do nó
* [Security] Vulnerabilidade de Análise de Arquivo USDC Fora de Gravação Associada
* [Security] Out-of-Bound WRITE Vulnerability II, ao analisar arquivo NEF
* [Security] Out-of-Bound Read Vulnerability III, ao analisar o arquivo DNG
* [Preferências] Problemas de UX nas configurações do projeto para projetos somente leitura
* [Recursos] Vários conjuntos UV não são exibidos ao abrir arquivos FBX
* [UI] Rótulos sobrepostos na barra de status
* [UI] As dicas de ferramenta do menu suspenso “Modo de criação de link” não são exibidas

## Versão 14

### 14.1.2

*(Lançado Em 15 De abril De 2025)*

**Adicionado:**

* [Gráfico] Usar o mecanismo de GPU padrão para gerar miniaturas para o gráfico atual
* [Biblioteca] Usar o mecanismo de GPU padrão para gerar miniaturas para a biblioteca

**Corrigido:**

* [Graph] Não é possível mover conexões em alguns casos no modo de criação de link &#39;Standard&#39;
* [Content] Artefatos na saída do filtro MLV em um caso específico
* [Content] Atlas splitter/dispersão: somente a primeira célula é desenhada corretamente (somente macOS + mecanismo de GPU)
* [Content] Suavização de chanfro: o formato é 32f absoluto
* [Content] Fibras 1: artefatos visuais ao converter em mapa normal
* [Content] RT AO, sombras, renderização normal torta incorretamente em alguns casos
* [Padeiros] Os itens de menu com submenus não têm alguma margem à direita do texto
* [MacArm]&#x200B;[sbsrender] Mecanismo de CPU incorreto quando o mecanismo da GPU não foi encontrado
* [Mac/Linux]&#x200B;[sbsrender] Mecanismo de GPU padrão incorreto

### 14.1.1

*(Lançado Em 20 De fevereiro De 2025)*

**Adicionado:**

* [Gráfico] Ferramentas de alinhamento de nó: restabeleça os atalhos de teclado e ative o empilhamento por padrão
* [MDL] Avisa aos usuários que “gráficos MDL” serão descontinuados em uma versão futura
* [Preferências] Avisa os usuários que “Plug-ins de espaço tangente personalizados” serão descontinuados em uma versão futura

**Corrigido:**

* [Visualização 2D] Exibir coordenadas de pixel do centro em vez de no canto superior esquerdo
* [Content] Anisotrópico Kuwahara Tons de Cinza: Aviso de cookie para variável “ignore\_alpha” ausente
* [Conteúdo] Avisos de cookie em alguns nós de Desgaste
* [Content] Erros de cozinha para parâmetro ausente no nó “Níveis automáticos”
* [Content] Erros de cozinha no console ao renderizar miniaturas de alguns pacotes
* [Content] Entalhe de borda: aviso de cozinha no console
* [Content] MLV Color: Color bleed apesar de não usar nenhuma divisão em um caso específico
* [Conteúdo] Mascarar para caminhos: caminhos podem ser muitos, muito poucos ou de comprimento zero em casos específicos
* [Conteúdo] Renderização PBR v1: alguns gráficos de utilitários são expostos na Biblioteca
* [Conteúdo] Dispersão na spline: um padrão é desenhado mesmo que não haja entrada de spline
* [Parâmetros] Rótulo &#39;Valor fantasma&#39; ao colar parâmetro de lista com índice incompatível
* [UI] Falha ao fechar o Designer por meio da ação “Sair” no macOS Dock (somente macOS)
* [UI] Os caminhos de textura nas propriedades do sombreador não são cortados na largura do encaixe

### 14.1.0

*(Lançado Em 14 De Janeiro De 2025)*

**Adicionado:**

* [Exibição 2D] Adicionar exibição de pixels fixados no painel Informações
* [API] Expor o tamanho da caixa de nós na cena da Exibição de gráfico
* [Content] &#39;Mesclagem de Height de material&#39;: adicionar saída de &#39;Máscara de Height&#39;
* [Content] &#39;Processador de Vértice de Caminho&#39;: Use o botão &#39;Editar função&#39; para o parâmetro &#39;Função por vértice&#39;
* [Conteúdo] Níveis automáticos: limpar parâmetro não utilizado, ajustar rótulos e dica de ferramenta
* [Conteúdo] Mascarar para caminhos v2
* [Conteúdo] Novo nó de MLV (Média da Menor Variação)
* [Content] Novo nó Filtro Mediano
* [Content] Quantificar cor: adicionar uma opção de filtragem “Mais próximo”
* [Content] Lista de pontes de spline: adicionar parâmetros de deslocamento de spline aleatórios
* [Content] Ferramenta de linha flexível: Novo nó de Spline (Quadrático)
* [Content] Triangle Grid: alterar método de triangulação e usar loops
* [Content] Nova Dispersão de Splines no nó Splines
* [Cooker] Expor parâmetro base &#39;Pixel ratio&#39; como variável estática &#39;$pixelratio&#39;
* [CrashReport] Integrar nova janela de relatório de falhas
* [Engine] Adicionar a versão Vulkan/Metal do mecanismo de mesclagem
* [Graph] Modo de material: permite a conexão com a entrada sem uso quando um único link é selecionado
* [Graph] Link de material: permitir conexões padrão quando a conexão não for ambígua
* [Gráfico] Ferramentas de alinhamento de nós: adicionar distribuições horizontais/verticais, alinhamentos à esquerda/direita/superior/inferior e suportar nós empilhados
* [Biblioteca] Corrigir cor do texto em menus contextuais
* [Parâmetros] Copiar parâmetros de um nó para outro
* [Propriedades] “Redefinir tudo”: remove a janela pop-up de confirmação
* [Recursos] Defina o formato como “Todos os formatos” na caixa de diálogo “Vincular bitmap”
* [Pesquisar] Adicionar uma maneira de ativar/desativar um modo recursivo
* [Pesquisar] Adicionar uma maneira de habilitar/desabilitar a pesquisa difusa
* [Search] Sempre mostrar e definir o foco no campo de termo de pesquisa ao ativar o Localizador de nós usando seu atalho de teclado
* [Pesquisar] Reprocessar a opção de filtro
* [Atalhos] Permitir que as teclas &#39;V&#39;, &#39;H&#39; e &#39;S&#39; sejam atribuídas
* [Terceiro] Atualize para o Qt 6.5.7
* [UX] As caixas de diálogo modais não devem ser minimizáveis
* [UX] Remover rolagem horizontal na caixa de diálogo de alerta

**Corrigido:**

* [Conteúdo] Chanfro: o formato normal não é afetado pela preferência global
* [Conteúdo] O nó Cor para máscara não ignora o alfa
* distância direcional [Content]: resultado incorreto quando a entrada tem uma proporção de imagem vertical
* [Content] Mapeador de Flood Fill: aviso gerado para variável ausente
* [Content] Computação de histograma: o resultado é 16 vezes o que deveria ser
* [Conteúdo] A cáustica de IR não funciona em resolução não quadrada
* [Content] Lista de pontes de spline: resultado incorreto ao usar deslocamentos de Início/Fim
* [Conteúdo] Seleção de spline: a quantidade de spline de saída pode ser maior que a quantidade de spline de entrada
* [Conteúdo] Distorção de spline produz um resultado em preto com o mecanismo SSE
* [Content] Triangle Grid: o padrão não está posicionado adequadamente no lado a lado
* [Content] Triangle Grid: A divisão em blocos gráficos é interrompida em um caso específico
* [Data] Falha ao alterar o identificador de entrada do gráfico em um caso específico
* [Gráfico de funções] Valores longos aparecem sobrepostos em nós &#39;Float&#39;
* [Fx-Map] Falha ao exibir as propriedades do nó Quadrante
* [Graph] [UDIM] Ter uma barra de rolagem na lista UDIM resulta em entradas 1..1 1..2
* [Graph]&#x200B;[Atalhos] O nó criado usando um atalho não é colocado em um link existente após a duplicação do nó
* [Propriedades] Exibição incorreta de parâmetro quando o valor é inválido
* [Publish] As dependências recíprocas resultam em um loop infinito ao publicar um pacote
* [Publish] Falha silenciosa ao usar a ação &#39;Publish&#39; no pacote com dependência descarregada
* [UI] O widget “Tamanho do pai” não é exibido corretamente quando expandido e pode bloquear a interface (somente no macOS)
* [IU] A janela principal fica atrás de outros aplicativos em alguns casos (somente Windows)

### 14.0.2

*(Lançado Em 10 De outubro De 2024)*

<b>Adicionado:</b>

* [Gráfico de função] Aprimorar o alinhamento de texto nos nós
* [MacOS] Repermitir instalação na versão Big Sur (11.0)
* [Windows] Repermitir instalação no Windows 10 19H2

<b>Corrigido:</b>

* [Bitmap] Os traços de tinta no recurso de bitmap não marcam o pacote de host como modificado
* [Gráfico de função] Falha ao fechar pacote com o gráfico de função hospedando um nó de instância
* [Gráfico de função] Falha ao desfazer dois ajustes de nó de Cor de amostra em uma linha

### 14.0.1

*(Lançado Em 24 De setembro De 2024)*

<b>Adicionado:</b>

* [Engine] Atualização para o Substance Engine 9.1.4
* [Content] Triangle Grid: alterar método de triangulação e usar loops

<b>Corrigido:</b>

* [API] Plug-ins descarregados não podem ser carregados novamente
* [Content] Computação de histograma: o resultado é 16 vezes o que deveria ser
* [Content] Triangle Grid: o padrão não está posicionado adequadamente no lado a lado
* [Data] Falha ao alterar o identificador de entrada do gráfico em um caso específico
* [Engine] O nó Distância produz artefatos ao usar tamanhos de pixel muito baixos
* [Engine] Resultado de nó Distância incorreto na resolução de 8K no mecanismo SSE2
* [Gráfico de funções] Valores longos aparecem sobrepostos em nós &#39;Float&#39;
* [Graph]&#x200B;[Atalhos] O nó criado usando um atalho não é colocado em um link existente após a duplicação do nó
* [Propriedades] Exibição incorreta de parâmetro quando o valor é inválido

### 14.0.0

*(Lançado Em 30 De julho De 2024)*

<b>Adicionado:</b>

* [Conteúdo] Novo filtro Kuwahara anisotrópico
* [Content] Nó Nova Suavização de chanfro
* [Content] Novo nó Curvatura suave v2
* [Content] Novo nó de Distância direcional
* [Content] Novas Ferramentas De Histograma: Calcular, Equalizar, Renderizar
* [Content] Novo ID para nó Máscara
* [Content] Novo nó Descombinar normal
* [Content] Novos nós de Paleta: Criar, Aplicar, Modificar, Exibir
* [Content] Novo nó Quantificar cor
* [Content] Distorção direcional não uniforme: defina o valor padrão do mapa de intensidade como 1
* [Conteúdo] Adicionar sufixo &#39;Cor&#39; ou &#39;Tons de Cinza&#39; a todos os rótulos de nó que possuem essas versões
* [Content] Preterir “White Noise” e manter apenas “White Noise Fast”
* [Content] Preterir nó &#39;Negate Float1&#39; no gráfico de função Substance
* [Content] Renomeie “Quantize cor” para “Quantize cor (simples)”
* [Exibição 2D] Exibe valores no painel Informações para pixels fora do intervalo 0-1
* [Mecanismo]&#x200B;[Texto] Novo kerning para algumas fontes
* [Graph] Melhorar o tempo de invalidação ao editar subgrafos profundos ao usar a edição no contexto
* [Vinculador] Não duplicar bitmaps em SBSASM
* [Parâmetros] Adiciona um novo widget “função” para todos os tipos de parâmetro de entrada
* [Propriedades] Aprimorar a exibição de parâmetros herdados
* [UX] Melhorar o suporte a trackpad (somente Mac)
* [UX] Modernizar panorâmica ao atingir a borda do gráfico ao selecionar
* [UX] Remover a funcionalidade “Desativar Hi DPI”
* [Branding] Nova marca para a tela de apresentação e a janela Sobre
* [Mapa de degradê] Adicionar uma maneira de deslocar todas as teclas e loop
* [Library] Alternar todos os filtros padrão para maiúsculas e minúsculas da frase
* [API] Adicionar método para enquadrar um nó específico no visor da Exibição de gráfico
* [API] Adicionar método para abrir um recurso de pacote em seu editor (por exemplo, um gráfico de Substance na Exibição de gráfico)
* [API] Adicionar método para selecionar um recurso de pacote no Explorer (por exemplo, um gráfico de Substance)
* [API] Adicionar métodos para obter e definir o tipo de gráfico de um gráfico de composição de Substance
* [Terceiros] Siga as recomendações das plataformas 2023 VFX
* [Terceiros] Siga as recomendações das plataformas 2024 VFX
* [Terceiro] Atualize o impulso para 1.82.0 + US$ para 23.08
* [ThirdParty] Atualize o NGL para 1.38
* [Terceiros] Atualize o OpenColorIO para 2.3.x
* [ThirdParty] Atualize o OpenExr para a versão 3.2.x
* [ThirdParty] Atualizar o OpenSubdiv para 3.6.x
* [Terceiros] Atualize o Python para a versão 3.11.x
* [ThirdParty] Atualize o Qt para 6.5.x
* [Terceiro] Atualize o gcc para 11.2.1
* [Terceiro] Atualize o glibc para 2.28
* [ThirdParty] Atualizar libstdc++ ABI para C++11 um
* [Documentação] Nova página de &#39;Glossário&#39;

<b>Corrigido:</b>

* [Bakers] Falha ao reassentar uma cena cujo nome de arquivo foi alterado
* [Padeiros] Falha ao salvar a predefinição de padeiros em arquivo JSON
* [Content] &#39;Dispersão na spline&#39;: Parâmetro alfa Expor imagem de entrada
* [Content] &#39;Tile Sampler Color&#39;: expressão visibleif ausente
* [Conteúdo] Ruído anisotrópico: valor negativo para quantidade X/Y produz resultado incorreto
* [Content] Ruído anisotrópico: problema de divisão em blocos gráficos ao usar um valor ímpar como uma quantidade X e sem smoothness
* [Content] Função de distribuição normal: max() inserido incorretamente pode levar a NaN
* [Content] RTAO, Bent Normal e RT Shadows não funcionam corretamente em algumas plataformas
* [Conteúdo] Cor de mesclagem de respingo de forma: mapas normais de OpenGL não são mesclados corretamente
* [Content] Espaço ingarantido após o prefixo &#39;Multi&#39; nos rótulos do nó
* [Dependências] Falha ao mover o gráfico dentro ou entre pacotes
* [Engine] Erro de precisão em nós de distorção que afetam os nós de Desfoque de Inclinação
* [Engine] A camada SBSAR no SD não é capaz de ler o SBSAR com conteúdo SBSASM > 2 GB
* [Gráfico de função] Resultado incorreto para 0^n
* [Gráfico] A opção “Exibir tamanho do nó” está rotulada incorretamente
* [Graph] Falha ao copiar um comentário com parentesco para outro gráfico
* [Gráfico] Congela ao arrastar um nó Ponto com a tecla Alt pressionada
* [Gráfico] A pesquisa de nós pode não encontrar correspondências óbvias em alguns casos
* [Graph] Problema de desempenho ao editar um gráfico de função instanciado várias vezes com o supergráfico aberto
* [Graph] Muitas invalidações ao criar uma saída
* [Segurança] Vulnerabilidade de gravação fora dos limites de análise de ICO
* [Segurança] Preterir alguns formatos de imagem não usados
* [Parâmetros] O caminho do recurso Bitmap PKG não deve ser editável
* [Parâmetros] Corrigir problemas relacionados à exposição/exposição em lote do parâmetro de um processador de valores
* [Parâmetros] Os parâmetros de cadeia de caracteres são ignorados ao expor o lote
* [Propriedades] Problema de desempenho ao editar um gráfico de função instanciado várias vezes com propriedades abertas
* [SVG] As edições em formas não são aplicadas em imagens rasterizadas
* [UI] Corrigir alguns erros/inconsistências com widgets com rolagem (somente Windows)
* [UI] Ordem inconsistente de formatos de arquivo de cena 3D em listas de importação/exportação
* [UI] As ações da janela são duplicadas na interface do usuário
* [Controle de versão] O script &#39;perforce.py&#39; não funciona em Python 3

## Versão 13

### 13.1.2

*(Lançado Em 16 De abril De 2024)*

<b>Adicionado:</b>

* [Gráfico] Não colocar nós duplicados sobre o nó original
* [Gráfico] Aprimorar o alinhamento de comentários anexados aos nós
* [Gráfico] Aprimorar movimentação de comentários
* [Gráfico] Ajustar quadros colados/duplicados e comentários à grade
* [Quadros] Ajustar novos quadros e comentários à grade
* [Content] &#39;Curvatura suave&#39;: adicione uma observação sobre o suporte a ladrilhos na descrição
* [3DView]&#x200B;[IRay] Permite que a saída int seja atribuída ao parâmetro enum
* [AxF] Adicionar propriedades sobre o modelo de revestimento transparente
* [AxF] Melhorar o gerenciamento de erros durante a exportação
* [AxF] Melhorar os materiais GLSLFX e MDL para representação “SVBRDF” conforme armazenado em um arquivo AXF
* [AxF] Remover a propriedade “CC sem refração” do modelo “AxF para AxF”
* [AxF] Renomear as propriedades “properties.has\_xxx” para “features.has\_xxx”
* [AxF] Atualizar modelo para incluir todas as propriedades usadas por nossos sombreadores SVBRDF

<b>Corrigido:</b>

* [3D View] Falha ao redefinir um parâmetro Int MDL mapeado para uma enumeração de MDL
* [Visualização 3D] Widgets incorretos para propriedades de sombreador SVBRDF quando o material é redefinido após alterar a cena 3D
* [Visualização 3D] Widgets incorretos para propriedades de sombreador SVBRDF quando nenhum gráfico é aplicado
* [Exibição 3D] O botão “Mostrar ambiente” está desabilitado para novas exibições sem arquivo SBSSCN padrão
* [Visualização 3D] Alternar do renderizador Iray para OpenGL desconecta uma saída de gráfico
* [AxF] A variante Fresnel não é atualizada pela saída do gráfico
* [AxF] Os rótulos das propriedades do sombreador AxF são formatados de forma inconsistente
* [AxF] Aviso sobre recursos inalterados aparece somente no console
* [Content] “Não Uniforme” não é escrito de forma consistente em todos os nós
* [Content] Dispersão na spline: Padrões ausentes nas splines da ponte
* [Content] Mapeador de spline: congela ao definir um valor negativo de “Quantidade de segmento”
* [Content] &#39;Symmetry&#39;: Rótulos ausentes e inconsistentes
* [Gráfico] Os comentários existentes estão um pouco deslocados
* [Security] Vulnerabilidade de Leitura Fora dos Limites de Análise de Arquivo RAS

### 13.1.1

*(Lançado Em 8 De fevereiro De 2024)*

<b>Adicionado:</b>

* [AxF] Adicionar propriedades booleanas hasClearCoat, hasSheen etc.
* [AxF] Adicionar algumas propriedades ausentes
* [AxF] Permitir importação de EP-SVBRDF
* [AxF] Renomear propriedades “anisotrópico”, “fresnel” e “variante fresnel”
* [AxF] Atualizar para o AxF-Editing 1.0.0
* [Gráfico] Colar na posição do mouse se a posição estiver dentro da Exibição de gráfico
* [UX] Aumentar o height do campo de texto “Descrição” do Quadro e do Comentário
* [UX] Definir foco em campos de edição de texto ao criar quadros, comentários ou pinos

<b>Corrigido:</b>

* [AxF] Os valores do mapa “Cor do Specular” estão incorretos quando exportados
* [AxF] A visualização e as texturas não são exibidas corretamente na caixa de diálogo “Importar AxF”
* [AxF] A propriedade “CC sem refração” não é injetada corretamente no modelo “AxF para AxF”
* [Conteúdo] &#39;Flood Fill para Posição&#39; está ausente da Biblioteca
* [Content] &#39;Splatter Circular&#39;: Valores negativos de &#39;Intensidade de padrão&#39; resultam em cálculos muito longos e intensivos
* [Content] &#39;Lista de mesclagem de spline&#39;: ordem de entrada incorreta
* [Dependências] A dependência é remapeada para sua cópia depois de ser salva como uma cópia
* [Frames] O botão &#39;Habilitar marcação HTML&#39; não é alternado ao desfazer seu uso
* [Quadros] Selecionar um quadro com o letreiro e seu conteúdo faz com que o conteúdo do quadro inteiro seja movido durante a expansão automática
* [Gráfico] Comentários duplicados de comentários com parentesco são sempre colocados na origem do gráfico
* [Gráfico] A quebra de linha no Comentário é mais pesada na criação
* [Publish] Definir caminho padrão para publicação SBSAR na pasta “Meus Documentos”
* [SBSAR] Refazer o carregamento do SBSAR o torna editável e seus dados podem ser perdidos

### 13.1.0

*(Lançado Em 12 De dezembro De 2023)*

<b>Adicionado:</b>

* [Frames] Expansão automática
* [Quadros] Alterar regras para definir quando um objeto pertence a um quadro
* [Quadros] Desabilitar escala de texto para descrição de quadros
* [Quadros] Ajustar tamanho ao conteúdo
* [Quadros] Novo padrão, passar o mouse e estados selecionados
* [Quadros] Ajustar à grade grande
* [Frames] Código de HTML de suporte para descrição de Frames
* [Quadros] Atualizar zonas de interação
* [Quadros] Atualizar aspecto visual
* [Gráfico] Criar o nó no meio do link visível em vez do meio do link
* [Gráfico] Exibe as propriedades de um item se ele for o único item com propriedades disponíveis em uma seleção
* [Gráfico] Remover a opção “Dimensionamento” para comentários no gráfico
* [Gráfico] Ajustar nós na grade principal ao copiar/colar
* [UX] Permitir pesquisa difusa no menu Nó e na pesquisa Biblioteca
* [UX] Fazer o loop da lista de menus Nó
* [AxF] Suporte para exportação de AxF
* [AxF] Desativar AxF no Linux
* [API] Defina a propriedade &#39;Visible if&#39; de parâmetros de gráficos, entradas e saídas usando a API Python
* [API] Definir a ordem de E/S do gráfico usando a API Python
* [Dependências] Atualizar aumento para 1.80.0
* [Dependências] Atualizar OpenSubdiv para 3.5.x
* [Dependências] Atualizar gcc para 11.2.1 - Problema do Iray/MDL C++20
* [Dependências] Atualize o SDK FBX para 2020.3
* [Dependências] Atualizar NGL para 1.35.0.20
* [Gerenciamento de cores] Adicionar compatibilidade com telas OCIO ICC
* [Níveis] Adicionar uma maneira de redefinir o histograma
* [Python] Avisar os usuários se o QtForPython não puder ser importado
* [Exibição 2D] Salva o estado das opções de exibição
* [Exibição 3D] Adicionar técnica de posição ao sombreador de informações de malha
* [Exportar] Adicione um botão “Salvar configurações” para salvar alterações nas opções de exportação

<b>Corrigido:</b>

* [Exibição 3D] Não é possível atribuir uma textura a uma entrada do tipo textura\_2d de um Material MDL
* [AxF] Os identificadores de gráfico na lista de modelos podem ficar em branco
* [AxF] O campo do modelo de gráfico de Substance está em branco por padrão
* atlas scatter [Content]: comportamento incorreto em casos específicos
* [Content] Mapeador de Flood Fill: saída em branco quando todas as formas têm o mesmo tamanho de caixa
* [Content] FloodFill to Position: artefatos de imprecisão em algumas situações
* [Content] Saída de &#39;Specular&#39; incorreta no nó &#39;BaseColor/Metallic/Roughness converter&#39;
* [Conteúdo] A Máscara para o caminho não funciona na vertical não quadrada
* [Content] Descrição ausente para os nós Valor de entrada, Tons de cinza de entrada, Cor de entrada e Saída
* [Content] Descrição ausente para os nós Definir e Sequência
* [Content] Shape Splatter: artefatos de imprecisão na saída &#39;Splatter data 2&#39;
* [Engine] Booleanos em Processadores de valor sempre avaliam como &#39;False&#39; (somente Apple Silicon)
* [Explorer] A ordem dos botões da barra de ferramentas é inconsistente entre o sistema operacional
* [Quadros] Não utilize nós ao mover um quadro com o modificador CTRL
* [Mapa de degradê] a opção redefinir tudo também deve redefinir o widget de degradê
* [GraphRender] Alguns nós são renderizados em preto ao ajustar no modo de visualização
* [Graph] A visualização “Valor de entrada” fica presa a “Falso” ao ajustar o valor booleano padrão (somente Apple Silicon)
* [Gráfico] Os nós de ponto próximos à borda do Quadro não são movidos pelo Quadro
* [Interoperabilidade] O ícone de reenvio não é atualizado após o envio para a Substance 3D Stager
* [MDL] Impossível alterar a Aspereza em nós onde este parâmetro está disponível
* [MDL] Conexões inválidas no modelo “AxF to Metallic Roughness”
* [UI] A janela “Exportar saídas” pode ser minimizada (somente Windows)
* [UI] As imagens aparecem pixeladas na tela Sobre ao usar o dimensionamento de exibição
* [UI] Ferramentas de alinhamento de nós na barra de ferramentas de gráfico criam várias etapas de desfazer

### 13.0.2

*(Lançado Em 27 De julho De 2023)*

<b>Adicionado:</b>

* [Gráfico de função] Adicionar variável de sistema $getPhysicalSize
* [Tela inicial] Suporte para abrir arquivos SBS arrastando e soltando
* [Content] Mapeador de Spline/Mapeador de Fluxo de Spline : Adicionar parâmetro &#39;Correção Não Quadrada&#39;

<b>Corrigido:</b>

* [Tela inicial] Não exibe a tela inicial quando um arquivo é enviado de outro software
* [Tela inicial] Status incorreto para o ícone do Designer na barra de ferramentas do Windows
* atlas splitter [Content]: descrição incorreta
* [Content] Valor de referência incorreto na função &#39;Linear para sRGB (luminância)&#39;
* A ferramenta de exibição de números [Conteúdo] não é compatível com resoluções não quadradas
* [Content] Lista de Pontos: o parâmetro &#39;Point number&#39; tem um valor mínimo incorreto
* [Content] Sombra projetada da forma: a sombra pode desaparecer quando a divisão em blocos gráficos estiver desativada
* [Conteúdo] Spline (Poly Quadratic): tangentes e thickness de visualização incorretos em resoluções não quadradas não corrigidas
* [Content] Spline (Poly Quadratic): os rótulos de pontos não ficam ocultos ao usar as opções de conexão de início/fim
* [Conteúdo] Ponte de spline (Lista): parâmetro &#39;Correção não quadrada&#39; não tem efeito
* [Conteúdo] Spline Cubic: o parâmetro de correção não quadrada não tem efeito na saída da visualização
* [Content] Mapeador de spline: renderização incorreta quando o spline tem um thickness muito pequeno
* [Conteúdo] Nós de spline: descrição de sinal alfa invertido na dica de ferramenta Coords
* [Conteúdo] Nós de spline: o parâmetro “Correção não quadrada” não tem efeito na saída da Visualização
* [Content] Renderização de spline: o formato de saída é 32F absoluto
* [Content] Renderização de spline: a saída está presa no intervalo [0, 1]
* [Conteúdo] Thickness de amostra de spline: a spline pode ser subtraída em valores negativos
* [Conteúdo] Seleção de spline: as splines são fechadas com um único segmento por padrão
* [Falha]&#x200B;[Fogão] Falha ao carregar gráficos específicos
* [Falha]&#x200B;[IU] Falha ao ativar menus após carregar o pacote da tela inicial
* O link &#39;Documentação do usuário&#39; da [API] na referência de script está desatualizado
* [Propriedades] A função de processador de valor não pode ser aberta em um gráfico bloqueado
* [Publish] Não é possível publicar pacotes contendo gráficos MDL
* [UI] A opção “Gerenciar minha conta...” está desativada no menu Ajuda
* [UI] Entradas ausentes no menu Ajuda ao abrir o Designer por meio de um arquivo

### 13.0.1

*(Lançado Em 27 De junho De 2023)*

<b>Adicionado:</b>

* [Conteúdo] Spline (Poly Quadratic), Lista de pontos: adicionar nome de pontos na saída da visualização
* [Content] Mapeador de spline: adicione um parâmetro para deslocar o centro de perfil do cilindro
* [DotNode] Classificar a lista de portais de entrada em ordem alfabética

<b>Corrigido:</b>

* [Content] Resultado incorreto em vários nós de spline ao usar a distribuição uniforme
* [Conteúdo] Erros secundários nas dicas de ferramentas dos nós de Spline e Caminho
* [Content] Quad Transform on Path: os valores padrão p01 e p10 são alternados
* [Content] Quad Transform: resultado incorreto em uma situação específica
* [Content] Círculo de spline: o resultado da opção “Virar direção” está incorreto quando não está sendo usada a distribuição Uniforme
* [Content] Círculo de spline: as tangentes estão incorretas ao ajustar os parâmetros de espiral e tamanho
* [Content] Mapeador de fluxo de spline: resultados com listras pretas ao usar energia espiral alta no círculo de spline
* [Content] Mapeador de spline / Mapeador UV: a cor de fundo não funciona
* [Content] Mapeador de spline: o height base é 0, resultando em recorte
* [Content] Mapeador de spline: o height de spline é modificado pelo multiplicador de entrada mesmo quando essa entrada não está conectada
* [Content] Mapeador de spline: extremidades de spline que atendem a uma borda de imagem não são mapeadas
* [Content] Mapeador de spline: a Escala UV Y não tem efeito ao usar uma forma não plana
* [Content] Mapeador de spline: luta Z ao renderizar splines sobrepostos do mesmo height
* [Content] Spline Poly Quadratic: o resultado da opção “Virar direção” está incorreto ao não usar a distribuição Uniforme
* [Conteúdo] Renderização de spline: as junções não são tratadas de forma consistente nas opções de Estilo de spline
* [Content] Renderização de spline: o último segmento não é desenhado
* [Content] Renderização de spline: a correção não quadrada não foi aplicada corretamente
* [Conteúdo] A cor do Mapeador UV aparece duas vezes na Biblioteca
* [DotNode] A área de ajuste de conexão não é atualizada após a desabilitação do limite de escala de texto
* [DotNode] A criação por meio do menu contextual foi interrompida
* [DotNode] A posição do nome do portal de entrada não é ajustada após desfazer/refazer uma alteração de nome
* [GraphRender] Número excessivo de invalidações ao modificar um gráfico de função
* [Gráfico] A posição do widget de transformação não é visualmente atualizada corretamente
* [Localização] &#39;Intervalo flexível&#39; e &#39;Intervalo rígido&#39; não estão localizados em gráficos MDL
* [Parâmetros] Alterações consecutivas de texto não são registradas na pilha de histórico
* [Parâmetros] A Hitbox para mover os parâmetros de entrada de gráfico na lista não é confiável
* [Propriedades] Clique simples é considerado como duplo no widget de caixa de rotação em projetos pesados
* [Publish] A ordem dos recursos no pacote não é preservada no ativo publicado

### 13.0.0

*(Lançado Em 6 De junho De 2023)*

<b>Adicionado:</b>

* [Graph] Nó do portal
* [Integração] Nova tela inicial
* Nó de spline (cúbico) [Content]
* Nó de spline (Poly Quadratic) [Content]
* [Content] Nó do círculo de spline
* Nó da Lista de Pontos [Content]
* Nó da Ponte de spline [Content] (2 splines)
* Nó (Lista) da Ponte de Spline [Content]
* [Content] Nó de acréscimo de spline
* [Content] Nó de seleção de spline
* [Content] Nó da lista de mesclagem de spline
* [Conteúdo] Nó de transformação 2D de spline
* [Content] Nó de distorção de spline
* [Content] Nó do Height de amostra de spline
* [Content] Nó do Thickness de amostra de spline
* [Content] Nó de renderização de spline
* [Content] Dispersão no nó Cor de spline
* [Content] Dispersão no nó Spline Grayscale
* [Content] Nó de cor do mapeador de spline
* [Content] Nó de tons de cinza do mapeador de spline
* [Content] Nó de cor do mapeador da ponte de spline
* [Content] Nó em tons de cinza do Mapeador da ponte de spline
* [Content] Nó do mapeador de fluxo de spline
* [Content] Nó de cor do mapeador UV
* [Content] Nó em tons de cinza do Mapeador UV
* [Content] Caminhos para o nó Splines
* [Conteúdo] Nó Máscaras para caminhos
* [Conteúdo] Nó de transformação de caminhos 2D
* [Content] Nó de polígono de caminhos
* [Content] Nó Caminhos de visualização
* [Content] Nó de distorção de caminhos
* [Conteúdo] Nó de seleção de caminhos
* [Content] Nó do processador de vértice dos caminhos
* [Content] Caminhos Processador de vértice Nó simples
* [Content] Quad Transform no nó Caminho
* [Content] Raytraced Ambient Oclusão v2
* [Content] Raytraced Bent Normal v2
* [Content] Raytraced Shadows v2
* [Engine] Atualização para a versão 9
* [Engine] Nó de loop em gráficos de função
* [Mecanismo] Adicionar modo sólido ao gradiente
* [Engine] Nó atômico pow() no Gráfico de funções
* [Engine] Adicionar opções de quebra de borda (fixação à borda / repetição) no nó Sampler
* [Engine] Amostragem mais próxima no nó Distorção e Distorção direcional
* [Engine] Adiciona um modo “alfa perfurado” ao filtro Tornar Nítido para entradas de cores
* [Engine] FxMap: Morfeta do Hemisfério
* [Engine] Operações Atômicas Get/Set em gráficos de função
* [Motor] Funções: usar função precisa de log / log2 / exp, 2pow - Unificar funções entre o fogão e o motor
* [Engine] Adiciona um parâmetro de “deslocamento de intensidade” ao filtro de Distorção direcional
* [API] Suporte ao gerenciamento de predefinições para composição de gráficos
* [Funções] Alterar nome de entrada para nós atômicos de funções
* [Localização] Adicionar idiomas português (Brasil), italiano (Itália) e espanhol (Espanha)
* [Localização] Respeitar a regra “Idioma (País)” na lista de idiomas
* [Predefinições] Desativar os painéis “Visualização” e “Predefinições” nas propriedades do gráfico ao usar a edição no contexto
* [Substance models graph] Fim do suporte dos gráficos de modelos de Substance

<b>Corrigido:</b>

* [Exibição 3D] A exibição de sequências longas nas estatísticas da cena é cortada (somente macOS)
* [API] O módulo &#39;structure::Structure&#39; ainda está incluído na referência de API
* [API] Os nós pontos nos gráficos MDL não têm definição nem propriedades
* [API] Comportamento incorreto ao definir o parâmetro dos nós de função
* [Content] 3D Voronoi e 3D voronoi fractal geram um aviso de cozimento
* [Engine] O parâmetro &#39;Intensity Map Offset&#39; não tem efeito nos dados em tons de cinza no mecanismo SSE2
* [Explorer] A E/S do gráfico pode ser excluída
* [Graph] O bitmap é ignorado quando usado em instâncias
* [Graph] Posição incorreta do nó de ponto quando criado a partir de um nó
* [Graph] Foco incorreto na caixa de diálogo “Expor parâmetro” ao usar a tecla “Enter”
* [Gráfico] Resultado incorreto na verificação de histograma com bitmap na edição de contexto
* [Localização] Corrigir vários problemas de recorte
* [Parâmetros] Falha ao excluir um parâmetro de entrada
* [Publish] Os gráficos nas pastas são movidos para a raiz no pacote publicado
* [Resources] Falha ao atualizar um recurso carregado no disco
* [VisibleIf] Corrigir regressão na avaliação da visibilidade condicional

## Versão 12

### 12.4.1

*(Lançado: 30 De março De 2023)*

**Adicionado:**

* [Cooker]&#x200B;[Gráfico] Leve em consideração as tags de transformação EXIF no arquivo JPEG
* [Segurança] Atualize para USD 23,02
* [Segurança] Remova o suporte ao formato de arquivo importar Collada (.dae)
* [modelos de Substance] Aviso sobre o fim da vida útil dos gráficos de modelos de Substance na próxima versão principal

**Corrigido:**

* [3D View]&#x200B;[ASM] Artefato de aspereza de revestimento ao usar um CoatNormal
* [Content] O parâmetro “Gradiente preenchido da Células do nó Alveolus” está invertido
* [Content] O número de entrada de nós de vários switches não está bloqueado
* [Content] Aviso de cozinha no nó Normal do Gerador de Scratches
* [Data] Falha ao carregar o pacote manualmente após desfazer seu carregamento anterior
* [Dados] Falha ao desfazer rapidamente várias operações de gráfico até a carga do pacote

### 12.4.0

*(Lançado: 31 De Janeiro De 2023)*

**Adicionado:**

* [Visualização 3D] Adicionar todas as opções no menu Exibição como botões da barra de ferramentas
* [API] Permitir a adição de ações às barras de ferramentas de exibição de gráfico
* [API] Permite criar/editar/avaliar um gráfico de modelo de Substance pela API
* [Gerenciamento de cores] Melhorar a qualidade de LUTs 3D cozidos no modo ACE
* [Documentação] Projetos de amostra para gráficos de composição de Substance
* [Documentação] Projeto de amostra para gráficos de função
* [Explorer] Permite mover gráficos e recursos de um pai para outro sem fechar ou invalidar widgets
* [Editor de gradiente] Selecione o pino clicado ao exibir o editor de gradiente
* [Graph] Adiciona a opção no menu contextual de um nó para selecionar todos os seus filhos
* [Graph] Ferramenta Limpar gráfico para detectar e remover nós não usados em todos os tipos de gráficos e gráficos de propriedades
* [Gráfico] Transformar a entrada da imagem em cor/escala de cinza
* [Parâmetros] Adiciona um bloqueio nos widgets integer2
* [Parâmetros] Permite digitar fórmulas básicas como um parâmetro
* [modelo Substance] Alternar entre valores e ícones para nós de valor
* [UI] Botão para gerar um valor aleatório quando uma semente aleatória é necessária
* [UI] O item focalizado não está destacado no navegador de Cenas
* [UX] Redefinir intervalos do controle deslizante quando seu valor é redefinido

**Corrigido:**

* [API] SDProperty.getDefaultValue() quase sempre retorna None
* [3D View] O valor da propriedade “DirectX normal” não é compartilhado entre os renderizadores
* [Exibição 3D] A exibição das estatísticas de cena é ampliada quando a viewport é pequena
* [3D View] A propriedade de exibição do Wireframe não é salva
* [Conteúdo] Os parâmetros de Cor de desfoque radial não têm efeito no canal alfa
* [Localização] Controles deslizantes e botões adicionais são exibidos em Propriedades do OpenGL do ambiente.
* [MDL]&#x200B;[modelo Substance] Falha ao excluir nós expostos
* [Preferências] O arquivo padrão\_config nunca é recriado se excluído
* [Modelo de Substance] Parâmetro de reordenação de falha que não aparece no nível da instância

### 12.3.1

*(Lançado: 24 De novembro De 2022)*

**Adicionado:**

* [3DView] Renderização otimizada para cenas com muitos materiais
* [3DView] Visualizar saídas de um gráfico de modelo de Substance ao descartá-lo do Explorer
* [Licença] Limpar sistema herdado para usuários do Linux
* [Integração] Atualizar transparência do plano de fundo
* [Modelos de Substance] Exibir aviso na Exibição de gráfico quando a entrada e a saída compartilham o mesmo identificador

**Corrigido:**

* [Ativos 3D] &#39;Ajuda > Ativos do Substance 3D&#39; é direcionado por engano ao Creative Cloud Desktop no Linux
* [3D View] Os materiais não são criados quando a malha é carregada
* [3D View] A lista de materiais é aberta ao soltar o gráfico de modelo de Substance no visor
* [Explorer] Não é possível excluir a seleção com o teclado se um gráfico de modelo de Substance estiver incluído
* [Explorer] Falha ao abrir o menu contextual de um item de material de recurso de malha no Mac
* [Graph] Instâncias cujas imagens de entrada dependem de valores geram resultado incorreto em nós subsequentes
* [Graph] Resultado incorreto ao usar a cadeia de subgrafos com a edição de gráfico contextual ativada
* [MDL] Falha ao carregar o gráfico MDL referenciando um gráfico de composição com saídas desatualizadas
* [MDL] O nó 2D de textura não funciona mais
* [Integração] Textos cortados e não localizados
* [Integração] Os painéis não são exibidos corretamente ao iniciar o aplicativo ao abrir um arquivo
* [Preferências] O cache de imagens ignora o local de arquivos temporários definido pelo usuário
* [Propriedades] O ajuste executado nos painéis de visualização/predefinição é mesclado na pilha de desfazer
* [Atalho] O atalho atribuído em nós obsoletos cria conflitos e não pode ser limpo
* [Modelos de Substance] Falha ao fechar um pacote após executar ações específicas
* [Modelos de Substance] Os nós de instância e links de pacotes realocados não são atualizados corretamente
* [Modelos de Substance] Desfazer a exclusão de subgrafos não atualiza os nós de instância e os links de forma consistente
* [Modelos de Substance] O valor aumenta repentinamente muito rápido no nó de transformação
* [UI] Os ícones de aviso de propriedade “Visible if” não têm uma dica de ferramenta
* [UI] O texto com informações da imagem está muito escuro no visor de 2D
* [Desfazer] Mover um widget de posição no modo de visualização armazena todos os valores intermediários

### 12.3.0

*(Lançado: 06 De outubro De 2022)*

**Adicionado:**

* [Geral] Painel de integração para acolher novos usuários
* [Geral] Painel de novidades para aprimorar a descoberta de novos recursos
* [Modelo Substance] Suporte a subgráficos e instâncias
* [modelo Substance] Suporte visível se para parâmetros expostos
* [modelo Substance] Adicionar suporte a nós de saída
* [modelo Substance] Nó de deslocamento de curva
* [modelo Substance] Nó de reversão de curva
* [modelo Substance] Nó de suavização de curva
* [modelo Substance] Nó de subdivisão de curva
* [Substance model] Nó de enxerto
* [Substance model] Atualizar nó “Filter Scene”
* [modelo Substance] Tornar nós não atômicos detectáveis no menu Nó
* [Substance model] Adicione a ação “Open Reference” no menu contextual de um nó de instância
* [Modelo Substance] Adicione uma ação “View in 3DView” no menu contextual de nós que podem ser enviados para o 3DView
* [Substance model] Exibe automaticamente as propriedades de um nó após a exposição
* [Substance model] Criar janela &#39;Novo gráfico de modelo de Substance&#39; com lista de modelos
* [UI] Melhorar a consistência das opções de salvamento de imagem na exibição 2D e na exibição 3D
* [UI] Renomear “Link > Malha 3D” para “Link > Cena 3D” no menu contextual do Explorer
* [UI] Redefinir layout agora se aplica a todas as janelas flutuantes
* [UI] Usar o rótulo “Exibir saídas na visualização 3D” em menus contextuais para gráficos
* [Library] Suporte a gráficos de modelos de Substance não atômicos
* [SBSAR] A descrição das saídas do gráfico de suporte no SBSAR
* [Shader] Define o valor padrão do Fator de mosaico como 1 para todos os sombreadores
* [IU] Expor widget de 2 botões para parâmetros booleanos
* [Engine] Atualização para a versão 8.6.4
* [Steam] Compilação otimizada para o chipset Apple Silicon (Apple M1 / M2)

**Corrigido:**

* [UI] Resolver problemas de dimensionamento para telas de alto DPI
* [UI] modelo &#39;$(udim)&#39; ausente da lista na janela de criação
* [UI] Falha ao exibir o menu Nó na borda direita da tela (somente macOS)
* [UI] O botão de extensão no menu Visualização 3D não está visível
* [IU] O menu de extensão da barra de ferramentas de gráfico está incompleto
* [UI] Valor incorreto do widget de parâmetro após desfazer a ativação do intervalo rígido
* [3D view] A configuração de sombreador não padrão é perdida no Iray de uma sessão para outra
* [Bakers] Falha ao carregar a janela de cozimento com uma cena sem malhas
* [Função] Falha ao copiar uma instância em seu gráfico referenciado
* [Função] Corrigir possível falha ao manipular nós
* [Globalização] O itálico nem sempre é desativado corretamente em japonês/coreano/chinês
* [Graph] Identificador de fallback incorreto para novos gráficos de modelos MDL e Substance
* [Graph] Parâmetros herdados orientados por valores às vezes são computados incorretamente
* [GraphRender] Falha ao alternar mecanismos ao computar gráficos de alta resolução (somente macOS)

### 12.2.1

*(Lançado em: 4 de agosto de 2022)*

**Corrigido:**

* [Graph] Resultados incorretos ao alterar o tamanho pai do gráfico
* [Falha] Falha ao calcular o gráfico de composição de Substance em resolução muito alta
* [Falha] Falha ao ficar sem memória ao carregar o pacote
* [Falha] Falha ao usar colchete nas anotações do parâmetro exposto em um gráfico de modelo de Substance
* [Falha] Melhorar a estabilidade da composição de Substance de renderização de gráficos
* [Iray] Atualização para a versão 2021.1.6

### 12.2.0

*(Lançado: 19 De julho De 2022)*

**Adicionado:**

* [Apple] Suporte nativo para Apple Silicon (M1) (somente versão Creative Cloud)
* [Substance gráfico de modelo] Exibe dicas de ferramentas de nó na Visualização de gráfico
* [Substance gráfico de modelo] Exibe dicas de ferramentas de nó na Biblioteca
* [Gráfico de modelo de Substance] Adicionar uma entrada de menu contextual para visualizar nós
* [Substance model graph] Permite que o usuário crie atalhos para a criação de nós
* [UI] Adicionar a opção “Exibir saída em exibição 2D” no menu contextual do gráfico de composição
* [UI] Dividir a configuração “Exibição automática de saídas” em configurações específicas de exibição 2D/exibição 3D
* [UI] Adicionar seta suspensa e dica de ferramenta ao botão “Exibir saída” na barra de ferramentas de exibição 2D
* [IU] Repalavra e reordenação de itens no painel Informações do Explorer
* [Gerenciamento de cores] Adicione “Linear Adobe RGB (1998)” e “Adobe RGB (1998)” para exportar espaços de cores para o Adobe ACE
* [Gerenciamento de cores] Adicionar espaço de cores de trabalho “Linear Adobe RGB (1998)” para Adobe ACE
* [Gerenciamento de cores] Adicionar compatibilidade com telas OCIO ICC
* [Gerenciamento de cores] Ocultar o espaço de cores de trabalho do Adobe RGB das preferências de ACE
* [Gerenciamento de cores] Melhorar a qualidade de LUTs 3D cozidos no modo ACE
* [Gerenciamento de cores] Usar a nova infraestrutura de GPU no visualizador 3D
* [Localização] Atualização completa do idioma coreano
* [Engine] Atualização para a versão 8.6.0
* [Graph] Atribuir um identificador de gráfico padrão quando essa propriedade for deixada em branco
* [Biblioteca] Desativar hiperlinks de dica de ferramenta para nós que não sejam de instância
* [NewProject] Atualizar resolução padrão
* [Modelos] Adicionar modelo CLO
* [API] Expor a propriedade defaultParentSize para objetos SDSBSCompGraph
* [Dependências] Atualize o Alembic para a versão 1.8.3
* [Dependências] Atualize o AXF para a versão 1.9.0
* [Dependências] Atualize o Boost para a versão 1.76
* [Dependências] Atualize o FBX para a versão 2020.2.1
* [Dependências] Atualize o IRay para a versão 2021.1.0
* [Dependências] Atualize o OpenColorIO para a versão 2.1.1
* [Dependências] Atualize o OpenEXR para a versão 3.1.5
* [Dependências] Atualize o TBB para a versão 2020.3
* [Dependências] Atualização USD para a versão 0.22.3
* [Remover] Desativar o recurso de pós-efeitos (Yebis)
* [Remover] Remover o comando “Salvar renderização em Artstation” do menu Exibição 3D

**Corrigido:**

* [Modelos de Substance] O intervalo rígido definido no parâmetro exposto é salvo ao cancelar a exposição
* [Substance models] O identificador não é amigável nos nós de constantes
* [Modelos de Substance] Aprimorar a pesquisa com base na compatibilidade de nós
* [UI] A ordem do submenu “Novo” está incorreta para recursos de pasta
* [UI] O tamanho padrão da janela principal é muito pequeno
* [UI] As barras de ferramentas não são afetadas pela opção “Redefinir layout”
* [UI] Grade de transparência visível no ícone de recurso de fonte no Explorer
* [Cooker] A composição de gráficos em instancias no gráfico MDL é sempre totalmente recozida
* [Graph] Falha ao colar um nó copiado de um gráfico com identificador em branco
* [MDL] Falha ao fechar um gráfico MDL específico
* [Performances] O aplicativo não responde ao carregar pacotes muito grandes
* [Recursos] O recurso Cena 3D pode ser importado em um caso específico

### 12.1.1

*(Lançado em: 07 de junho de 2022)*

**Corrigido:**

* [Content] O recurso “bluenoise\_256” tem um atributo “colorspace” definido em alguns nós
* [Conteúdo] Os nós “Obter tamanho” não aparecem na Biblioteca e a versão em tons de cinza está rotulada incorretamente
* [Content] O parâmetro “Distribuição de cor aleatória” nos nós Voronoi 2D não tem efeito
* [SBSRender] Exportar um gráfico para EXR não gera o mesmo bpc que o Designer
* [Modelos de Substance] “Tipo de gama” não deve aparecer nas propriedades do parâmetro exposto
* [Modelos de Substance] Falha ao usar colchete nas anotações do parâmetro exposto

### 12.1.0

*(Lançado: 26 De abril De 2022)*

**Adicionado:**

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
* [UI] Melhorar o comportamento do menu Nó ao clicar incorretamente
* [UI] Abrir subgrafos na mesma guia, mesmo que estejam fixados
* [UI] Botão Remover pino da barra de título do painel do Explorer
* [UI] Salvar a opção “Não exibir novamente” na tela de boas-vindas nas versões
* [ThirdParty] Atualização do Qt (e QtForPython) para a versão 5.15.8
* [Terceiros] Atualize o Python para a versão 3.9.9
* [Terceiros] Atualize o OpenSSL para 1.1.1 m
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
* [Documentação] Nova página que descreve a herança em gráficos de composição de Substance
* [Documentação] Atualizar seção &#39;Iray&#39;
* [Documentação] Atualizar seção &#39;Gráficos MDL&#39;

**Corrigido:**

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

## Versão 11

### 11.3.3

*(Lançado em: 01 de fevereiro de 2022)*

**Corrigido:**

* [Modelos de Substance] Intervalos podem ser perdidos em alguns casos
* [Modelos de Substance]&#x200B;[Exportar] A escala é diferente dependendo do tipo de arquivo
* [Modelos de Substance]&#x200B;[Exportar] As malhas são duplicadas

### 11.3.2

*(Lançado: 25 De Janeiro De 2022)*

**Adicionado:**

* [Documentação] Atualizar seção &#39;Iray&#39;

**Corrigido:**

* [Modelos de Substance] Não é possível publicar um pacote que contém gráficos de modelos de Substance
* [Modelos de Substance] Impossível exportar um gráfico de modelo em alguns casos específicos
* [Modelos de Substance] Tornar as faixas de parâmetros mais coerentes
* [MDL] Falha ao exportar arquivo MDLE
* [MDL] Arquivo .mdl incorreto gerado quando um gráfico MDL contém nós Ponto conectados a parâmetros Expostos
* [Visualização 2D] Otimizar a exibição de ferramentas de pintura
* [Content] Configuração inconsistente do parâmetro de tamanho da saída nos gráficos de origem do modelo
* [Propriedades] Rótulos de intervalos Flexível/Rígido estão errados no Painel de Propriedades para nós expostos de modelos MDL e Substance
* [Modelos] Atualizar valores padrão de entradas no modelo “Sampler filter”

### 11.3.1

*(Lançado: 13 de dezembro de 2021)*

**Adicionado:**

* [Gráfico] Adiciona um aviso ao excluir um gráfico usado em outro gráfico/pacote

**Corrigido:**

* [UI] O editor de cores é muito pequeno ao usar um layout de interface específico
* [UI] Falha ao atualizar a lista de modelos usados recentemente
* [IU] Realce incorreto nas preferências de Atalhos
* [UI] O tamanho da janela principal é muito pequeno após a reinicialização de uma sessão em janela (somente macOS)
* [IU] O encaixe maximizado não é minimizado na saída (somente Windows)
* [UI] Espaço ausente na dica de ferramenta do parâmetro “Nível Externo Alto”[3DView] Os eixos na exibição 3D são muito pequenos quando a caixa delimitadora da cena é fina
* [UI] Problema de estilo em algum texto nas configurações do projeto para o idioma francês
* [Modelos de Substance] Os parâmetros expostos não são salvos entre as sessões
* [Modelos de Substance] O modificador Shift ainda está ativado após o uso do atalho de visualização de nó
* [Modelos de Substance] Alguns nós excluídos permanecem no SBSM exportado
* [Modelos de Substance] Os nós de destino da avaliação se acumulam e não são excluídos[API] Falha ao renderizar o nó de curva cujas propriedades foram definidas por meio da API
* [Bakers] O widget “Cor do material” não está visível e não funciona conforme o esperado
* Nó da Renderização PBR [Content]: computação interna não executada na resolução do nó
* [Gráfico de funções] As mensagens que exibem os tipos esperados estão erradas em alguns casos
* [Graph] Entrada relativa à entrada: parâmetros herdados estão incorretos com instâncias conectadas
* [MDL] As instâncias do gráfico de Substance não são atualizadas com segurança nos gráficos MDL
* [Publish] Falha ao publicar o gráfico que contém dependências circulares
* [Atalhos] Shift+Espaço não deve ser um atalho de teclado atribuível para nós
* [Modelos] O formato de saída de modelos personalizados é ignorado

### 11.3.0

*(Lançado: 24 De novembro De 2021)*

**Adicionado:**

* [modelos de Substance] Adicionar dicas de ferramentas para parâmetros de nós
* [Modelos de Substance] Permite exibir em sobreposição na janela de visualização 3D o resultado de um nó intermediário
* [Modelos de Substance] Melhorar a exibição das bases
* [Modelos de Substance] Preserva a hierarquia dos objetos ao exportar um gráfico de Modelo de Substance para .fbx
* [Modelos de Substance] Suporte a vários materiais no gráfico Exportação de FBX/OBJ a partir do modelo de Substance
* [Substance models]&#x200B;[Content] Nó de partículas
* [Modelos de Substance]&#x200B;[Conteúdo] Nó de transformação generativa
* [Substance models]&#x200B;[Content] Organic Pattern node
* [Modelos de Substance]&#x200B;[Conteúdo] Partículas do nó Instâncias
* [Modelos de Substance]&#x200B;[Conteúdo] Nó de remoção de partículas
* [Modelos de Substance]&#x200B;[Conteúdo] nó Lathe
* [Substance models]&#x200B;[Content] Nó do shell
* [Substance models]&#x200B;[Content] Nó de projeção
* [Modelos de Substance]&#x200B;[Conteúdo] Nó Curve Trim
* [Modelos de Substance]&#x200B;[Conteúdo] Atualizar nó Sampler da curva
* [Modelos do Substance]&#x200B;[Conteúdo] Atualizar nó do Mesh Sampler
* [Modelos de Substance]&#x200B;[Conteúdo] Atualizar nó de tremulação
* [UX] Botão para maximizar a visualização atual
* [UX] Atualizar a janela Novo gráfico
* [UX] Adicionar a opção “Baixar Player” no menu Ferramentas e agregar com “Localizar Player”
* [UX] Adicionar a entrada “Fechar tudo” ao menu Arquivo
* [UX] Aplicar uso consistente de maiúsculas e minúsculas no menu principal
* [UX] Exibir automaticamente as propriedades de itens de gráfico duplicados
* [UX] Adicionar botões na barra de ferramentas do gráfico para desativar o tamanho de tela constante para títulos/comentários/pinos de quadros
* [UX] Botões para copiar informações de versão para a área de transferência na caixa de diálogo Sobre
* [Materiais] Entradas relativas às entradas
* [Conteúdo] Adicionar opção de divisão em blocos gráficos em ruídos Perlin 3D
* [Content] Novo nó do processo de difusão
* [Content] Nova versão de nó de Renderização PBR
* [Interoperabilidade] Receber SBS e SBSAR da Sampler
* [Interoperabilidade] Enviar SBSM para o Stager
* [3D View] Adicionar uma opção para desativar a remoção de face
* [Exibição 3D] Adicione uma opção para exibir o espaço tangente do vértice
* [Explorer] Realçar o gráfico no Explorer ao clicar duas vezes no plano de fundo da Exibição de gráfico
* [Explorer] Remover a opção “Explorar” em menus contextuais
* [Padarias] Ocultar padarias obsoletas
* [Gerenciamento de cores] Adicione suporte para as regras do arquivo de configuração OCIO v2
* [Biblioteca] Renomear categorias de acordo com tipos de gráficos
* [Preferences] Desative automaticamente a CPU nas preferências de hardware do Iray se a GPU CUDA compatível for detectada

**Corrigido:**

* [Modelos Substance] Falha no Mac ao usar a opção “as sudb” no .fbx
* [Modelos de Substance] Falha ao exportar para SBSM em um caso específico
* [Modelos de Substance] Falha na exportação ao exportar parâmetros expostos em quais widgets nunca foram criados
* [Modelos Substance] Falha aleatória ao abrir um gráfico que se refere a vários arquivos .fbx
* [Modelos de Substance] Os intervalos não são aplicados dinamicamente nos widgets dos parâmetros expostos
* [Modelos de Substance] A opção Recarregar malha não funciona em recursos usados no gráfico de modelos de Substance
* [Modelos Substance] As cenas não são exibidas em uma visualização 3D disponível em um caso específico
* [IU] A área de desativação é muito grande em opções de material
* [UI] Problema de estilo na caixa de diálogo “Arquivo de pacote não salvo”
* [UI] A tecla Tab deve ser pressionada duas vezes para navegar pelos valores
* [IU] O zoom com arrastar o mouse é invertido entre a Exibição 3D e outras Portas de Visualização
* [UI] Carregar um SBS já aberto usando a lista “Arquivos recentes” aciona incorretamente um prompt “Pacote não encontrado”
* [UI]&#x200B;[macOS] Layout de interface padrão incorreto após iniciar o aplicativo
* [UI] Os pacotes não podem ser salvos na raiz de uma unidade (somente Windows)
* [Graph] A opção “Exibir automaticamente na visualização 2D” é inconsistente em um caso específico
* [Graph] A opção &#39;Abrir referência&#39; está disponível para nós de instância SBSAR
* [Gráfico] As propriedades do pino são exibidas somente quando o item é criado
* [Gráfico] As regras de sequência de caracteres do pino são aplicadas de forma inconsistente
* [Graph] Falha ao salvar um gráfico vazio
* [Visualização 3D] O ângulo de Anisotropia é invertido no sombreador ASM
* [3D View] Sombreador ASM: problemas de linearização com mapas relacionados a SSS
* [Visualização 3D] Renderização OpenGL incorreta após fechar visualizações 3D adicionais em um caso específico
* [Visualização 3D] As posições predefinidas das câmeras não estão corretas na Visualização 3D com alguns arquivos .fbx
* [MDL] “Adicionar Nó” do menu contextual não funciona para Gráficos MDL
* [MDL] Erro: falha na conexão do nó ao usar componentes float2.x e semelhantes (SD 11.1.2)
* [MDL] Falha ao abrir o arquivo specific.sbs
* [MDL] Unidades de cena por metro na Iray não definidas no início da sessão de renderização
* [MDL] Congela ao ajustar um nó de aprendizado no gráfico MDL
* [MDL] Ordem de parâmetros no código MDL exportado
* [Explorer] a pasta de recursos vazia é criada após o cancelamento da criação do recurso
* [Explorer] Somente o primeiro elemento de um pacote pode ser movido para a parte inferior da lista
* [Content] RT Bent Normal e RT AO acionam a computação de nós em gráficos aninhados
* [Nó de entrada] O bitmap nos Nós de entrada não é atualizado quando o UDIM é alterado
* [Iray] Demora ao tentar exibir uma cena de modelos de Substance com muitas instâncias
* [Preferências] Linha vazia ao cancelar a adição de um arquivo de projeto
* [Editor de Python] A opção “Fechar” permanece ativada após fechar o último script e ainda inclui seu nome

### 11.2.2

*(Lançado: 28 De setembro De 2021)*

**Adicionado:**

* [Propriedades] Adicionar novos tipos de gráficos para decalques, atlas, luzes ambiente e texturas de luz

**Corrigido:**

* [UI] Layout de interface incorreto após iniciar o aplicativo
* [Estabilidade] Corrigir falhas ao sair do modo de suspensão no Windows e ao conectar/desconectar telas
* [Visualização 3D] Criar um recurso de Cena 3D a partir do gráfico de modelo de Substance Cena não tem efeito
* [Blend] Valores enum estão ausentes ao expor o modo de mesclagem
* [Exportar] A exportação de cena de modelos de Substance resulta em geometria duplicada
* [MDL] Falha ao abrir um arquivo SBS específico
* [Mesh] Falha ao vincular a malha específica com geometria incorreta
* [Modelos de Substance] A exportação falha quando o valor padrão do parâmetro exposto está fora do intervalo flexível

### 11.2.1

*(Lançado: 27 de julho de 2021)*

**Adicionado:**

* [Substance model] Atualização para a versão 1.0.3
* [Substance model] Complete e melhore a documentação sobre gráficos de modelos de Substance
* [modelo de Substance] Exibir registros no console
* [Substance model]&#x200B;[ScatterOnCurves] Alterar valor padrão para espaçamento
* [Substance model]&#x200B;[ScatterOnCurves] Remove o parâmetro HalfSpaceOddEven desnecessário
* [modelo Substance]&#x200B;[Transformar] Atualizar o intervalo suave da rotação de Euler
* [Publish] Lembrar configurações na janela do Publish
* [Publish] Avisar o usuário quando pelo menos uma dependência tiver alterações não salvas
* [Publish] Inicializar o campo “Caminho do arquivo”
* [Publish] Adicionar feedback visual durante a publicação
* [Interoperabilidade] Adiciona o comando “Enviar para o Player” ao menu “Enviar para”
* [Interoperabilidade] Simplificar o fluxo de trabalho de envio/reenvio para o Sampler e o Painter
* [API] Adicionar SDApplication.getVersion() para permitir a recuperação da versão do aplicativo host
* [Explorer] Adicionar uma ação Abrir a itens de gráfico de modelo de Substance
* [Gráfico] Desativar as ações “Exibir na exibição 3D” para nós de instância fantasma

**Corrigido:**

* [modelo Substance] Falha ao excluir uma sequência
* [modelo Substance] As bases não são desenhadas corretamente em alguns casos
* [Modelo Substance] Falha ao exportar projetos específicos
* [modelo Substance] A atribuição de material é interrompida ao abrir um projeto com o Iray ativado
* [Modelo de Substance] O intervalo rígido mínimo não funciona corretamente em certas circunstâncias
* [Modelo Substance]&#x200B;[Primitivo] O primeiro nível de subdivisão da icosfera não funciona
* [Substance model]&#x200B;[RandomFloat] Manipular corretamente o caso em que Min >= Max
* [Exibição 3D] Falha ao arrastar e soltar mapas
* [Exibição 3D] Cadeias de caracteres expostas em materiais MDL usam o widget de espaço de cores
* [Exibição 3D]&#x200B;[Preparadores] Objetos com parentesco não são tratados corretamente
* [3D View] Mensagem de aviso sobre o nome de uso de “heightScale” para o arquivo .glslfx herdado
* [Content] Avisos de cozinha no nó Extrusão na Altura
* [Content] O nó Irradiância RT não aparece na Biblioteca
* [Content] RT Shadows: cozinhando mensagens de aviso no console
* [Graph] Falha ao abrir um arquivo com alguns nós desativados
* [Graph] O nó de ponto não funciona corretamente no gráfico MDL quando um link é selecionado
* [Graph] A exibição de gráfico não é reaberta automaticamente após recarregar um pacote
* [Interoperabilidade] Caixa de diálogo de erro ao selecionar &#39;Baixar...&#39; ao enviar para o Player
* [Interoperabilidade] O reenvio após a exclusão de todas as saídas resulta em erros de API
* [Interoperabilidade] O reenvio logo após o fechamento do aplicativo de destino resulta em erros de API
* [Explorer] [Graph] Após recarregar um pacote, o primeiro gráfico aberto não é o primeiro gráfico do pacote
* [Explorer] Novos gráficos em um pacote não são colocados da mesma maneira, dependendo do tipo
* [Explorer] Não é possível abrir um gráfico de Substance ou um recurso de cena após movê-lo no explorador
* [Explorer] Falha/congelamento ao mover um gráfico de modelo de Substance para a hierarquia de pacotes
* [Library] Os arquivos SBSAR permanecem no local de arquivos temporários
* [Library] Os arquivos XML permanecem no local de arquivos temporários
* [Player] O material não tem impacto na exibição 3D quando a linguagem está definida como japonês
* O link para download do Substance Player [Player] está desatualizado
* [Widget de cor] A janela do editor de cores é movida para a parte superior da tela
* [IRay] Corrigir carregamento do módulo IRay no Windows quando o diretório de aplicativos contém caracteres não ascii
* [Preferências] O painel MDL é exibido duas vezes no Project
* [API] Os nós do FxMap não suportam getPropertyGraph()

### 11.2.0

*(Lançado: 23 de junho de 2021)*

**Adicionado:**

* [Branding] Substance Designer se torna Adobe Substance 3D Designer
* [Modelos de Substance] Novos gráficos de modelos de Substance para criar modelos 3D de procedimentos
* [Conteúdo] Adicionar novos mapas de ambiente HDR
* [Content] Novo nó Normal Torto
* [Content] Novo nó de Oclusão de ambiente RT
* [Content] Novo nó Caustics RT
* [Content] Novo nó Caustics RT
* [Content] Novo nó de irradiância RT
* [Content] Novo nó de sombras RT
* [Interoperabilidade] Enviar ativo para a Painter abrirá o Painter e adicionará ou atualizará o ativo na biblioteca (requer um plano Adobe Substance 3D)
* [Interoperabilidade] Enviar ativo para a Sampler abrirá o Sampler e adicionará ou atualizará o ativo na biblioteca (requer um plano Adobe Substance 3D)
* [Interoperabilidade] Procure seu ativo no Adobe Bridge e iniciará o Bridge no local do ativo (requer um plano do Adobe Substance 3D)
* [ASM] Suporte ao novo Adobe Standard Material (ASM) no gráfico Gráfico do Substance e MDL
* [ASM] Adicionar modelos de ASM
* [ASM] Adicionar Sombreador OpenGL para ASM
* [ASM] Definir sombreador ASM como o sombreador padrão
* [Geral] Agregar todos os arquivos temporários ao diretório temporário definido pelo usuário
* [Geral] Novo comando “Salvar uma cópia como”
* [Geral] Menu Atualizar arquivo
* [Geral] Atualizar menu Ajuda
* [Publish] Nova janela de publicação
* [Publish] Adicione a opção nas preferências para não salvar o arquivo SBS ao publicar um arquivo SBSAR
* [Propriedades] Adiciona o campo de tipo de gráfico às propriedades de gráfico
* [Propriedades] Reordenar propriedades de gráficos de uma maneira mais relevante
* [Branding] Nova janela Sobre
* [Branding] Atualizar estilo do aplicativo
* [GLSLFX] Adicionar um rótulo às técnicas
* [GLSLFX] Adicionar a possibilidade de definir o rótulo de um sombreador GLSLFX
* [Metadados] Adicionar metadados nos recursos do pacote
* [Metadados] Permitir a edição de metadados para gráficos, entradas, saídas e recursos
* [Localização] Novas traduções para alemão, francês e chinês simplificado
* [UX] Aplicar zoom reverso na visualização 3D no caso de um arrastar com o mouse
* [AXF] Atualização para a versão 1.8.0
* [Logs] Adicionar plug-ins instalados aos logs
* [VFX] Adicionar a configuração OpenColorIO do ACES 1.2
* [API Python] Adicionar um método para consultar a pasta tmp especificada nas configurações
* [API Python] Adicionar um método isModified ao SDPackage para verificar se um pacote foi salvo
* [API Python] Adicionar alguns métodos de conversão de cores ao SDColorManagementEngine
* [API Python] Excluir objetos de gráfico (comentários, pinos, quadros, ...)
* [Python API] Expor propriedade Tamanho físico para nós de instância de gráfico
* [API Python] Expor salvar uma cópia como
* [API Python] Corrigir método SDPackageMgr.savePackage
* [API Python] Obter uma lista de objetos de gráfico selecionados
* [API Python] Introduzir novos nomes de método para trabalhar com seleções de gráficos
* [API Python] Os plug-ins não podem adicionar ações ao primeiro painel do explorador criado

**Corrigido:**

* [Parâmetros] Valores negativos nos parâmetros suspensos Integer1 resultam em comportamento incongruente na instância
* [Parâmetros] Problema ao incrementar um valor em um widget de ângulo
* [Graph] Problemas de temporização quando a saída é exibida na visualização 2D ou 3D.
* [Internacionalização] Alguns caracteres específicos são alterados em espaços em identificadores de arquivo
* [Preferências] O rótulo de arquivo “Projeto do usuário” não é traduzido de volta do japonês
* [Python API] RecursionError ao executar o método SDUIMgr.getCurrentGraphSelectedNodes()
* [Python API] SDApplication.getPath(SDApplicationPath.InstallationDir) não retorna nada
* [API Python] O SDSBSARExporter não envia notificações de salvamento de arquivo

### 11.1.2 (2021.1.2)

*(Lançado: 17 De março De 2021)*

**Corrigido:**

* As miniaturas de [Library] não são atualizadas de forma consistente
* [Content] A propriedade &#39;Pixel ratio&#39; &#39;Vetor morph&#39; graphics&#39; está definida como &#39;Stretch (Absolute)&#39;
* [Conteúdo] Os bitmaps usados nas ferramentas de pintura aparecem no menu Nó
* [Content] Saída NaN para entrada de cor simples no nó Níveis automáticos na precisão de ponto flutuante
* [Engine]&#x200B;[SSE2] Valor &#39;Level in mid&#39; diferente de 0,5 resulta em saída 1,0
* [Miniatura] Os mapas de entrada são reduzidos para 256
* [UI] As dicas de ferramentas dos nós atômicos têm quebra de linha incorreta

### 11.1.1 (2021.1.1)

*(Lançado: 10 De fevereiro De 2021)*

**Corrigido:**

* [Exibição 3D] Problema de renderização ao usar sbs que têm frequências altas no mapa normal
* [3D View] As imagens não são aplicadas se a propriedade de saída &#39;Component&#39; não estiver definida como RGBA ou RGB
* [Exibição 3D] As cenas não são carregadas corretamente em alguma situação específica
* [UI] O campo de entrada “Arquivo de textura” no Editor de pincéis é dimensionado verticalmente
* [UI] Os botões Fixar e Encaixar desaparecem da guia quando a guia ativa é fechada
* [Padeiros] Resultado incorreto quando a caixa global de malha alta não inclui a origem da cena
* [Gerenciamento de cores] A propriedade do material Textura da cor base sRGB não é substituída no estado de Cena personalizado
* [Console] A mensagem de log “GPUs disponíveis” não lista GPUs e aparece aleatoriamente
* [Console] Cadeia de caracteres incorreta registrada ao usar a exportação em lote
* O parâmetro “Formato normal de entrada” do Atlas splitter [Content] afeta o canal Vermelho em vez do Verde
* [Cooker] Falha ou saída NaN ao usar bitmaps \*.surface em SBSAR
* [Engine] Os valores de saída fora do intervalo do mapa de gradiente giram em torno de 0 quando o formato de saída tem intervalo de 0-1
* [Parâmetros] Os controles deslizantes Mín/Máx/Padrão não se ajustam automaticamente na janela de parâmetro Expor
* [SBSAR] Falha ao importar algum SBSAR
* [SVG] Falha ao cancelar importação de recurso

### 11.1.0 (2021.1.0)

*(Lançado: 28 De Janeiro De 2021)*

**Adicionado:**

* [Cores especiais] Cores Pantone compatíveis no Designer
* [Gráfico] Desativar nós
* [Visualização 3D] Exportar malhas em mosaico da janela de visualização
* [Internacionalização] Atualizar a versão em japonês
* [Visualização 3D] Otimizar o consumo de memória quando não estiver usando o Iray
* [API Python] Adicionar método SDResource.delete() para excluir um SDResource
* [API Python] Adicionar compatibilidade com cores especiais na API Python
* [API Python] Novo retorno de chamada para acionar quando um pacote é fechado
* [2D View] Converter banco de dados de pincéis do SQLite para o formato Json
* [Exibição 2D] Melhorar o desempenho e a confiabilidade da renderização (computação da CPU)
* [Library] Adicionar a opção &#39;Excluir padrão&#39; nas configurações do projeto
* [Library] Renomeie “Excluir padrão” para Excluir extensões de arquivo nas configurações do projeto
* [UX] Remover o botão &#39;?&#39; nas barras de título da janela no Windows
* [UX] Mover o atalho Ctrl+E para “Abrir referência” quando a edição no contexto estiver desativada
* [Padeiros] Excluir o cache de visualização ao excluir um padeiro na lista de bolos
* [Desempenho] Melhorar o orçamento do cache de imagem no hardware com GPU com memória compartilhada
* [Preferências] Adaptar o valor de &#39;Limite de cache da GPU&#39; ao pool de memória disponível
* [Propriedades] Exibir atributo de Tamanho físico em instância de nó
* [Script] Marcar sistema de script externo como obsoleto
* [Share] Remover recursos de “Exportar para o Substance share”

**Corrigido:**

* [Content] Ordem de I/O inconsistente em nós de material
* [Content] A entrada principal em nós de distorção é inconsistente
* [Content] Solucionar avisos de Fogão a partir do nó Desfoque radial
* [Exportar] A exportação em lote com mecanismo de CPU usa VRAM para determinar o orçamento de memória
* [Exportar] Exportar para um caminho que não existe criará as pastas
* [Exportar] O orçamento de memória é muito baixo ao usar a exportação em lote
* [Exibição 2D] Artefatos/faixas ao copiar imagens HDR para a área de transferência
* [Exibição 2D] Exportar imagens de recursos sempre exporta 8 bits
* [3D View] Iray: mudar o valor normal usando o editor dá um resultado estranho
* [3D View] Iray: desativar o canal normal não produz o resultado correto
* [Biblioteca] A filtragem por URL não funciona corretamente
* [Library] Os recursos correspondentes a um padrão excluído da biblioteca não podem ser importados manualmente
* [Padeiros] Renomear um padeiro não afeta sua entrada na lista de visualização de Exibição 2D
* [Explorer] Perda de sincronização entre o Explorer e os dados do gráfico
* [Gráfico de função] Falha ao definir o nó da função com o tipo de saída incompatível como saída
* [MDL] Os nós da instância do SBS não têm visualização, saída 0 e não acionam o cálculo do gráfico
* [API Python] A propriedade &#39;editor&#39; do parâmetro de entrada não pode ser modificada
* [Python] A redefinição de layout não redefine corretamente as docking stations criadas pelo Python
* [Recursos] Não é possível vincular/importar o documento PSD de 32 bits

## Versão 10

### 10.2.2 (2020.2.2)

*(Lançado: 17 de dezembro de 2020)*

**Adicionado:**

* [Visualização 3D] Restaurar posição da câmera armazenada em um recurso de Cena
* [Graph] Remover “nós de entrada” no menu contextual para FXMap e processador de valor

**Corrigido:**

* [Content] Ordem de I/O inconsistente em nós de material
* [Conteúdo] Renderização PBR: amostragem incorreta de IBL para a contribuição de specular
* renderização PBR [Conteúdo]: alguns pixels são sempre transparentes
* [Content] Renderização PBR: a saída UV está incorreta para a forma do cilindro
* O parâmetro &#39;Específico de Padrão&#39; da Circular Splatter [Content] não tem efeito
* [MDL] Falha ao criar e conectar um nó
* [MDL] Falha ao duplicar um construtor de matriz color[] com sua entrada de valor exposto conectada
* [MDL] Falha ao reconectar uma conexão inválida
* [MDL] Os MDLs exportados têm parâmetros duplicados
* [MDL] Parâmetros expostos não são exportados para um arquivo .mdl
* [Parâmetros] Um parâmetro de nó pode ser definido duas vezes no SBS em um caso específico
* [Parameters] Falha ao obter o Tipo de saída do Gráfico de função de um parâmetro
* [Parâmetros] Falha ao selecionar a opção “Editar entrada de gráfico exposta” em que não existe nenhuma entrada correspondente
* [3D View] O uso de “Ambiente” não é considerado corretamente pelo renderizador OpenGL
* [Exibição 3D] IOR é 0 e precisa ser redefinido em um caso específico
* [3D View] UVs de alta resolução de plano/plano são deslocadas
* [Bitmap] Falha ao cancelar importação de recurso
* [Bitmap] Falha ao criar um novo nó Bitmap com um tipo de arquivo não suportado
* [Dependências] Falha ao desfazer &#39;Realocar&#39; para resolver uma instância fantasma
* [Gráfico de função] Falha ao abrir o gráfico de função para um parâmetro
* [Editor de gradiente] Mover controles deslizantes e teclas registra muitas ações na pilha de histórico
* [License] Falha ao analisar um arquivo license.key inválido
* [SBSAR] Os nós da instância do SBSAR não podem ser criados na Biblioteca se os gráficos expostos estiverem em pastas

### 10.2.1 (2020.2.1)

*(Lançado em: 04 de novembro de 2020)*

**Corrigido:**

* [Geral] Falha ao sair do modo de suspensão do Windows
* [Geral] Falha ao desfazer após carregar um recurso de cena 3D
* [Engine] As linhas de artefato aparecem na saída do nó Distância no Direct3D
* [Engine] Falha ao selecionar o nó Mapa de degradê em um gráfico atualizado
* [Engine] Nenhum aviso quando o valor padrão de entrada é diferente de 0 no modo de compatibilidade do Engine v7
* [Exibição 3D] “Remover tudo” deixa malhas com materiais predefinidos sem nenhum material aplicado
* [3D View] “Redefinir cena” remove todas as texturas da malha no Iray
* [3D View] OpenGL: modificar o valor padrão de um sampler em um arquivo .glslfx não é refletido corretamente na interface
* [Visualização 3D] Pixels vermelhos e pretos na borda mais à direita de imagens renderizadas no OpenGL
* [Dependências] Não é possível realocar dependências ausentes do tipo &#39;Outro&#39;
* [Dependências] Falha ao sair quando o Visualizador de Dependências está aberto
* [Graph] Falha ao duplicar um nó de Instância fantasma
* [Graph] A Edição do contexto interno está disponível por meio do pressionamento de tecla quando está desativada em Preferências
* [UI] A janela de aviso “Localizar Player” tem um título incorreto
* [UI] O assistente de ativação tem algum comportamento incorreto
* [Explorer] Pacotes integrados são sempre editáveis no Windows
* [MDL] Falha ao carregar o gráfico da versão anterior com conexões inválidas
* [Propriedades] A cor padrão do nó de entrada não é atualizada ao desfazer
* [SBSRender] Os perfis ICC dos bitmaps injetados não são usados

### 10.2.0 (2020.2.0)

*(Lançado: 12 De outubro De 2020)*

**Adicionado:**

* [Content] Adicionar nó “Cross Section”
* [Content] Adicione a função “Cross product vec2” a functions.sbs
* [Content] Adicionar nó de valor “Get Size”
* [Content] Adicione a função “Orthogonal vec2” a function.sbs
* [Content] Adicionar funções Average a function.sbs
* [Conteúdo] Adicionar filtro de Limite
* [Conteúdo] Correspondência de cores: adicione uma entrada de máscara para especificar onde aplicar o filtro
* [Content] Tile Generator/Sampler: adicione novas opções para controlar o tamanho do padrão
* [Content] Atualizar nó de Renderização PBR com valor padrão para entradas de imagem
* [Parâmetros] Adicione ícones de aviso para destacar problemas nos Parâmetros de Instância
* [Parâmetros] Ignorar instruções If visíveis para Entradas/Saídas envolvendo parâmetros que têm uma Função aplicada
* [Parâmetros] Melhorar a UX para associação de grupo
* [Parâmetros] Retrabalho da maneira de expor um único parâmetro
* [Parâmetros] Realçar parâmetros expostos
* [Parâmetros] Melhorar a limpeza de parâmetros não usados
* [Engine] Nó Curve: nova opção para gerar a textura da curva
* [Engine] Valores padrão em imagens de entrada
* [Engine] Nó de distância: novos modos de distância (distâncias de Manhattan e Chebyshev)
* [Engine] Nó de degradê: novo modo de interpolação para ter uma mistura mais natural entre as cores
* [UX] Alguns parâmetros agora estão esmaecidos, dependendo de outros parâmetros
* [UX] Aceitar cores de RGB de 6 dígitos no campo hexadecimal do Seletor de cores
* [UX] Evite mostrar as propriedades dos comentários assim que forem selecionados
* [UX] Exibir grupos relevantes ao começar a gravar um nome de grupo
* [UX] Atalho para exportar novamente as saídas do gráfico
* [UX] Fazer com que todas as caixas de combinação Dropdown-textfield pareçam diferentes das caixas de combinação normais
* [GraphRender] Exibe as miniaturas dos nós uma a uma e não apenas quando são todas computadas
* [GraphRender] Melhorar o atraso de cancelamento durante a renderização do gráfico
* [GraphRender] Aprimorar a precisão da barra de progresso da renderização
* [Miniaturas] Cálculo automático de miniaturas (ícone)
* [Miniaturas] Retrabalho da UX para adicionar uma miniatura (ícone) a um pacote
* [Preferências] Ativar Rastreamento de raios do GPU por padrão para novos usuários
* [Preferências] 3DView / OpenGL / Qualidade: substitua o controle deslizante para contagens de amostras por uma lista mais intuitiva de opções
* [Padarias] Aprimorar o desempenho dos pós-processos
* [Gerenciamento de cores] Mostrar espaço de cores de trabalho atual na caixa de diálogo de preferências.
* [Iray] Alternar automaticamente para o modo CPU quando não houver GPU compatível
* [Desempenho] Melhorar o tempo de resposta para calcular o nó em que estamos interessados (agora calculado primeiro)
* [API Python] Novo método addActionToExplorerToolbar para adicionar ícones à barra de ferramentas do explorador
* [Recursos] Atualização para FBX 2020.0.1
* [iRay] Atualização para o Iray 2020.1.0
* [API] Adicionar acesso Python às configurações e propriedades de gerenciamento de cores

**Corrigido:**

* [Gráfico] Alterar o tamanho pai ou o bloco uv não cancela a renderização atual
* [Graph] Falha ao mover uma conexão de saída e pressionar Alt+LMB
* [Graph] Falha ao mover conexões no modo Material ou Material compacto
* [Graph] Os nós de entrada não podem visualizar recursos de bitmap
* [Graph] Compatibilidade de nó interrompida em instâncias
* [Graph] Muitos nós são invalidados ao alterar um parâmetro de gráfico
* [Content] A forma de saída “Extrusão de forma” é invertida em casos específicos: é necessária uma nova versão, a antiga é obsoleta
* [Content] Resultado incorreto usando a Variação de cor personalizada no nó Correspondência de cores
* [Conteúdo] O tamanho por taxa de quantidade X/Y em Atlas scatter tem o efeito oposto
* [Conteúdo] O tamanho por taxa de quantidade X/Y no respingo de forma tem o efeito oposto
* [3D View] Falha na operação de desfazer após carregar um recurso de cena de um pacote
* [Exibição 3D] O ambiente personalizado não é salvo em SBSSCN se o caminho tiver alias com caracteres especiais
* [Exibição 3D] Alternar o Formato normal nas configurações de Material resulta em estados invertidos
* [UI] O texto do botão “Definir como principal” está excedendo a partir da área de exibição
* [UI] A posição da janela principal não é restaurada corretamente ao trabalhar no modo de janela
* [UI] O texto da barra de status é deslocado quando a janela está em tela cheia ou arrastada perto da borda da tela
* [Iray] Falha com mensagem de “Marca inválida” ao alternar para frente e para trás entre renderizadores
* [Iray] Faces visíveis em superfícies não opacas
* [Predefinições] Falha ao aplicar predefinições em instâncias de alguns gráficos de Substance Source
* [Predefinições] nome incorreto exibido após desfazer na instância do sbs
* [Render] Renderização incorreta ao ajustar um parâmetro no modo de visualização
* [Padarias] A atualização de vários mapas baked resulta em avisos bloqueando alguns tornos
* [Cooker] Ajustar nós SBSAR em instâncias SBS resulta em 0 saída da instância
* [Explorer] Os aliases personalizados não são transmitidos ao usar “Salvar e abrir no Substance Player”
* [Editor de gradiente] A seleção de cor absoluta não afeta todas as teclas selecionadas

### 10.1.3 (2020.1.3)

*(Lançado: 11 de junho de 2020)*

**Adicionado:**

* [Content] Expor o parâmetro “Matte Color” no nó Tons de cinza de transformação segura
* [Content] Renderização PBR: Adicionar uma opção personalizada de Entrada em segundo plano
* [Content] Nós do Panorama Light: nova opção para obter uma amostra da cor da imagem de fundo
* [Parâmetros] Ocultar parâmetros com sinalizador &#39;sem suporte&#39; na lista da janela Expor Parâmetros

**Corrigido:**

* [Exibição 3D] Falha ao alternar malhas personalizadas em um caso específico
* [Visualização 3D] O formato normal é sempre DirectX na inicialização
* [Content] 3D Worley noise: renderizar artefato ao usar um valor de tamanho de grade alto
* [Content] A mesclagem do nó de dissolução está incorreta
* [Content] Renderização PBR: remover aviso de Cooker
* [Content] Renderização PBR: o resultado contém cores negativas em alguns casos
* [Cooker] Problema de injeção de cache para nós de instância de várias saídas
* [Explorer] Falha ao fechar um pacote que contém um gráfico MDL exibido
* [Graph] Cozimento em 2 passos: a alteração do tipo de nó não aciona um recook
* [Graph] Falha ao excluir entradas ao usar a conexão
* [Gráfico] Os pontos de extremidade do link podem ser movidos para um espaço vazio
* [MDL] Falha ao cancelar a exportação MDL do gráfico MaterialX
* [MDL] Erro ao cancelar exportação para MDLE
* [Predefinições] Falha na guia Predefinições após alterar o tipo de parâmetro incluído na predefinição
* [Resources] A lista de materiais está vazia no menu contextual do gráfico para malhas vinculadas como não UDIM

### 10.1.2 (2020.1.2)

*(Lançado: 27 de abril de 2020)*

**Adicionado:**

* [Content] Adicionar modelo de filtro de Alchemist
* [Content] Renderização PBR: adicionar parâmetros para controlar as intensidades das sombras difusas/de specular
* [Content] Nós de luz da forma: adicionar parâmetro de posição da câmera
* [Notícias] O estilo de grupo “Seta” é quebrado na primeira vez que a janela é exibida
* [Padeiros] Adicione o atalho Z à Visualização 2D para ver a imagem em 1:1
* [Project] Ocultar o alias $(PROJECT\_DIR) da lista
* [Explorer] Não criar recurso personalizado para recursos que não são um arquivo no disco

**Corrigido:**

* [Player] Relatar aliases ausentes ao carregar pacotes SBS
* [Player] Exibe o valor de Distribuição aleatória em base decimal
* [Player] Empacotar todos os mapas de ambiente incluídos no Substance Designer
* [Player] Falha ao sair no macOS High Sierra
* [Player] Não é possível carregar pacotes usando sbs://
* [Content] 3D Worley noise: renderizar artefato ao usar um valor de tamanho de grade alto
* [Content] A entrada &#39;GreaterThanZero&#39; no nó &#39;Wave&#39; não é usada
* [Conteúdo] Luz de plano: o modo de posição do espaço global não funciona
* [Conteúdo] Luz da esfera: a posição interna da luz não funciona corretamente
* [Padeiros] Falha ao assar com a janela de cozimento enquanto uma opção “Atualizar todos os mapas baked” está em execução
* [Padeiros] Falha de cozimento no Optix para AO da malha usando baixo como alto com um mapa normal
* [Padeiros] A resolução da visualização dos arquivos UVT não corresponde ao tamanho da tela
* [Exibição 3D] O bitmap atribuído será substituído ao carregar um MDL se o valor padrão não for uma texture2d
* [3D View] Os widgets de Propriedades de materiais mudam após a redefinição de uma propriedade
* [Exibição 3D] A preferência global de Formato normal não funciona mais
* [MatX] Biblioteca: a categoria MaterialX Graph não exibe todos os nós disponíveis
* [MatX] O menu contextual de um Gráfico personalizado pode conter subpastas vazias na pasta “Adicionar nó”
* [SBSAR] A entrada principal é revertida para a primeira entrada da lista
* [Biblioteca] Somente o primeiro gráfico é incluído no SBSAR com vários gráficos
* [CustomGraph] Os nós que não fazem parte do tipo de gráfico atual são criados automaticamente em alguns casos
* [Iray] O parâmetro &#39;Profundidade&#39; de projeção de caixa não funciona corretamente
* [Preferências] Aprimorar layout nas configurações do projeto
* [Parâmetros] Falha ao mover um widget de posição depois de excluir um parâmetro
* [UI] Falha ao alterar a hierarquia de usos no nó de saídas
* [Graph] Falha ao usar uma caixa de seleção em um comentário e um nó com marca

### 10.1.1 (2020.1.1)

*(Lançado: 10 De abril De 2020)*

**Corrigido:**

* [Visualização 3D] O uso da memória é muito alto ao trabalhar em gráficos de composição
* [Content] Formas inesperadas na saída não quadrada de nós &#39;Polygon&#39;
* [Content] Renderização PBR: a câmera ortográfica não funciona corretamente ao usar uma resolução não quadrada
* [Conteúdo] Renderização PBR: bokeh giratório aumenta o brilho da borda da imagem
* [Gerenciamento de cores] O seletor de cores na caixa de diálogo Novo bitmap não é gerenciado por cores.
* [Gerenciamento de cores] Os seletores de cores nas ferramentas de pintura e vetor na exibição 2d não são gerenciados por cores.

### 10.1.0 (2020.1.0)

*(Lançado: 09 de abril de 2020)*

**Adicionado:**

* [Atalhos] Gerenciador de atalhos para criação de nó
* [Content] Nó Nova Renderização PBR
* [Content] Novo filtro FXAA
* [Content] Novo filtro Hald CLUT
* [Content] Expor a filtragem em nós “Cortar”
* [Exibição 3D] Melhorar os parâmetros do sombreador / fluxo de trabalho de atribuição de textura
* [Visualização 3D] Novo sombreador sem iluminação
* [Exibição 3D] Adicione um “Valor zero escalar” aos sombreadores de deslocamento
* [3D View] Adiciona uma opção para reduzir a resolução da viewport quando High DPI está ativada
* [Modo de exibição 3D] GLSLFX: permite definir informações de gui no sampler (padrão, mín, máx, guiMin, guiMax, guiStep, guiWidget, guiName, guiGroup)
* [Exibição 3D] Adicione a opção “Carregar estado com malha...” no menu Cena
* [Exibição 3D] Adicione o ACES tonemapped output transform no modo de gerenciamento de cores herdado
* [Padarias] Novo método de amostragem em AO, Curvatura, Normal Torto, Padarias de Thickness
* [Padeiros] Novas opções de normalização em padeiros de Heights e Thicknesss
* [Gerenciamento de cores] Integrar Adobe ACE (Adobe Color Engine)
* [Gerenciamento de cores] Adicionar opções para definir o comportamento padrão quando o perfil ICC estiver ausente
* [Parâmetros] Tornar os controles deslizantes incrementais consistentes com o Substance Painter
* [Pacote] Incluir o máximo de dlls Qt que pudermos para scripts Python
* [Projeto] Desabilitar configurações para arquivos de projeto somente leitura e comunicar esse estado claramente
* [Preferências] Ocultar configurações não claras específicas relacionadas à capacidade de resposta e aos períodos de cálculo
* [UI] Renomear Pow2 -> 2Pow
* [Propriedades] Otimizar a exibição das propriedades do gráfico de composição
* [AXF] Atualização para o AXF SDK 1.7.1

**Corrigido:**

* [Exibição 3D] Os parâmetros de Luz ambiente não são visíveis, embora estejam ativados
* [Visualização 3D] glslfx: o widget de cor é sempre um vec3 sem alfa
* [3D View] O mapa de ambiente definido de um recurso não é salvo no recurso da cena
* [Visualização 3D] Iray: a luz ambiente é convertida em uma luz de ponto na origem da cena
* [Visualização 3D] glslfx: o widget de cor é sempre um vec3 sem alfa
* [Parâmetros] A URL do Pacote de Instâncias não está correta no grupo de atributos
* [Parâmetros] Falha ao expor parâmetros
* [Parâmetros] Os ícones não estão corretamente alinhados nos parâmetros dos nós Curva
* A cadeia de caracteres do nó [Parameters] &#39;Text&#39; só é exibida no modo &#39;Preview&#39; quando exposta
* [Parameters] Falha ao renomear um parâmetro de entrada usado na instrução &#39;Visible If&#39;
* [Parâmetros] Falha ao excluir um nó de Níveis que tem uma função definida em qualquer um de seus parâmetros
* [IU] O ícone de aviso na lista de parâmetros de entrada é colocado sobre um botão existente
* [UI] Os avisos não são apagados no item de parâmetro de entrada correto em um caso específico
* [UI] Impedir a mensagem “Is mesh UDIM ?” popup para aparecer quando os UVs de malha estiverem estritamente no bloco [0,1]
* [UI] As listas suspensas de predefinições podem ser roladas com a roda do mouse ao passar o mouse
* [UI] A opção “Cálculo de saída(s)” nos atributos do gráfico foi nomeada incorretamente
* [MDL] Falha ao inserir um recurso de gráfico SBS em um gráfico MDL
* [MDL] O nó SBS com entrada de imagem não funciona corretamente
* [MDL] Associações de textura e nomes de uso incorretos
* [Graph] O grupo de valores de entrada e o uso são ignorados no modo de criação de link &#39;Material&#39;
* [Gráfico] Valores de Entrada usam o valor padrão em vez dos dados de entrada para Booleanos
* [Bakers] Normais incorretos no padeiro World Space Normals usando um mapa normal tangente em casos específicos
* [Pães] Uso excessivo de memória ao assar com a janela de visualização aberta
* [Predefinições] a predefinição corrompida causa uma falha na renderização
* [Predefinições] O parâmetro booliano do SBS antigo não é afetado pela predefinição
* [Library] Os recursos do primeiro pacote aberto são listados no menu flutuante de criação de nó
* [Publish] Publicar no SBSAR retorna o código de erro 13 em SBSCooker no macOS
* [Publish] Aviso de argumento preterido no SBSCooker ao publicar no SBSAR
* [API] Não é possível obter os metadados de um pacote que vem de um arquivo .sbsar
* [Exportar] No modo Legado, a opção colorspace é revertida para os padrões de saídas específicas
* [2D View] Copiar para a área de transferência não leva em consideração o estado do Gerenciamento de cores
* [Unix] O Designer ignora os sinais do sistema
* [Library] Alguns filtros da biblioteca não funcionam corretamente devido às tags traduzidas
* [Cooker] A raiz quadrada de números negativos deve retornar 0 em vez de NaN
* [Visualização 2D] Os canais vermelho e azul são trocados após desfazer o primeiro traçado de tinta
* [Console] Mensagem de aviso em excesso no console “QPixmap::scaled: Pixmap é um pixmap nulo”
* [Content] “Shape Glow”: aviso de culinária
* [Dependências] Atribuir um gráfico localizado em um pacote diferente a uma malha não cria dependências
* [Iray] As propriedades do material ficam inativas após alternar a geometria

## Versão 9

### 9.3.3 (2019.3.3)

*(Lançado em: 14 de fevereiro de 2020)*

**Adicionado:**

* [Batchtools] Entregar perfis OCIO padrão com ferramentas de lote

**Corrigido:**

* atlas scatter [Content]: problemas ao usar cores aleatórias/normais em algumas situações

### 9.3.2 (2019.3.2)

*(Lançado em: 4 de fevereiro de 2020)*

**Adicionado:**

* [SBSRender] Adicionar suporte ao gerenciamento de cores

**Corrigido:**

* [Content] Linear sRGB para nó ACEScg: rótulos de E/S incorretos
* [Content] ACEScg para nó sRGB: rótulos de saída incorretos
* [Content] Nós do Panorama Light: ajustar a faixa de temperatura
* [Graph] Grave queda de desempenho e congela ao ajustar um gráfico aninhado com “In-Context Editing” ativo
* [Graph] Falha ao excluir vários nós no FX-Map
* [Desempenho] O processo do Designer pode permanecer ativo após o encerramento

### 9.3.1 (2019.3.1)

*(Lançado: 27 De Janeiro De 2020)*

**Corrigido:**

* [Graph] Grave queda de desempenho e congela ao ajustar um gráfico aninhado com “In-Context Editing” ativo
* [Graph] Não é possível inserir valor de enumeração de [0, 99] no ajuste Integer1
* [Gráfico] O comentário não é movido quando o quadro correspondente é deslocado
* [Graph] Os nomes de entrada estão ausentes no nó da instância personalizada
* [Graph] Miniaturas podem ser renderizadas ao carregar o gráfico, mesmo se a opção correspondente estiver desativada nas Preferências
* [2D View] O alfa negativo mostra o verificador, independentemente da opção de exibição
* [2D View] A conversão de superfície de 32f para 8 bits falha com valores altos
* [2D View] A inclinação superior/esquerda e “Make Square” definem algumas coordenadas com valores enormes em matrizes de transformação de avanço
* [2D View] UVs de todos os objetos de malha não são exibidos em conjuntos UV diferentes de “0”
* [Conteúdo] Chanfro: o modo de Angular não funciona corretamente na máscara de divisão em blocos gráficos
* [Conteúdo] Flood Fill para Gradiente: o valor da imagem de inclinação não é amostrado no meio da forma
* Função [Content]; “Booleano de igualdade” não está funcionando
* [Padarias] Artefatos ao usar o mapeamento automático de tons no padeiro “Curvatura da malha” em casos específicos
* [Padeiros] Falha em DXR quando cozimento enquanto nenhum material é selecionado
* [Bakers] Problema de desempenho na Exibição 2D ao ativar as “informações”
* [Engine] A função &#39;Pow&#39; gera valores enormes ao usar um valor de entrada muito baixo e um expoente alto no mecanismo SSE2
* [Engine] Falha ao usar uma compactação jpg alta em recursos de bitmap
* [Engine] O processador de valores retorna um valor incorreto de $size quando está dentro de um subgrafo
* [Parâmetros] Pop-up vazio aparece ao selecionar um nó de instância com um número alto de parâmetros
* [Parâmetros] O valor inteiro não é exibido em itens de parâmetro suspensos
* [Parâmetros] O botão Matriz de transformação &#39;Editar&#39; não está disponível no modo de visualização
* [Cooker] $size em ValueProcessor está errado quando dentro de uma instância do gráfico
* [Cooker] Tamanho de saída incorreto quando o link de valor passa por um nó de ponto para um nó atômico
* [UI] O botão para exibir todos os itens na barra inferior de Visualização 2D não está visível
* [UI] A visualização dos valores de RGB separados exibe números incorretos ao usar o Gerenciamento de cores
* [Exportar] As imagens RGBA 16f são exportadas em tons de cinza
* [Visualização 3D] Não é possível importar OBJ com vários espaços
* [Gerenciamento de cores] A configuração OCIO não é levada em consideração ao publicar a sbsar
* [Widget de cor] Os intervalos dos controles deslizantes de cor podem se expandir exponencialmente em um caso específico
* [Doc] A seção “paramValue” está incompleta na referência de formato Sbs
* [MDL] O widget de cores nas instâncias do sbsar não está correto
* [Predefinições] Falha ao atualizar predefinições em um caso específico
* [PSD] Erro do FreeImage ao carregar arquivos PSD de versões recentes do Photoshop
* [Resources] Falha ao desfazer a vinculação de bitmap diretamente no gráfico
* [SVG] os nós de SVG não são atualizados automaticamente ao usar as ferramentas de vetor

### 9.3.0 (2019.3.0)

*(Lançado em: 19 de dezembro de 2019)*

**Adicionado:**

* [Geral] Suporte ao gerenciamento de cores usando o arquivo de configuração do OpenColorIO
* [Predefinições] Aprimorar o gerenciamento de predefinições
* [Predefinições] Sincronizar Gizmos de exibição 2D e controles deslizantes de visualização
* [Predefinições] Restaurar valores de visualização ao voltar para o modo de Visualização
* [Predefinições] Manter o modo de visualização ativo ao editar outros nós, recursos ou gráficos
* [Predefinições] Desfazer funciona suavemente ao navegar entre as três guias de predefinições
* [Predefinições] Permitir a redefinição de parâmetros para o valor padrão do gráfico ou Predefinição no modo de visualização
* [Predefinições] Aprimorar fixação de parâmetros
* [Predefinições] Importar/exportar todas as predefinições de um gráfico para um arquivo
* [Padeiros] Novo padeiro &#39;Curvatura de malha&#39; com base em traçado de raio
* [Padeiros] Adicionar opção de plano terrestre no padeiro &#39;AO from Mesh&#39;
* [Padeiros] Adicione a opção de correspondência por nome para ignorar a face traseira no padeiro “AO from Mesh”
* [Content] Novo nó de Atlas scatter
* [Content] Novos nós e funções de conversão do espaço de cores (ACEScg)
* [Conteúdo] Melhorar a consistência de nomenclatura para nós com versões coloridas/em tons de cinza
* [Gráfico] Aprimorar o desempenho no modo de Visualização de predefinições
* [Graph] Adicionar a macro $(colorspace) para exportar a opção de saídas de gráfico
* [Parâmetros] Quando um parâmetro é definido como invisível, oculte o gizmo correspondente na Visualização 2D
* [Parâmetros] Não adicionar &#39;Grupo de entrada de gráfico&#39; como um prefixo ao expor parâmetros
* [Parâmetros] Adicionar dica de ferramenta para VisibleIf nos parâmetros do gráfico
* [AXF] Atualizar o AXF SDK para v1.6

**Corrigido:**

* [Linux] O Designer não inicia no CentOS 8 devido a uma falha de carregamento na plataforma Qt.
* [Linux] AVISO: a biblioteca Freetype foi removida do aplicativo SD: usuários com CentOS versão &lt;= 7.5 precisam instalá-la manualmente.
* [AxF] Falha ao importar arquivos criados com versões mais recentes do AxF
* [2DView] As texturas do pincel alimentadas por um recurso não são aplicadas
* [2DView] Falha ao modificar entradas de gráfico instanciado com ajuste de posição
* [3DView] Falha ao cancelar o “Carregar...” ação
* [3DView] Opção Adicionar espaço da cor para texturas de emissão em Sombreadores GLSLFX
* [Padeiros] Mapas alimentados por recursos são ignorados durante a cozedura
* [Padeiros] As opções de “Direção do espaço mundial” estão bloqueadas incorretamente
* [Bitmap] Os bitmaps EXR com valores de ponto flutuante são renderizados como uma imagem em preto
* [Content] Flood Fill para índice: a detecção de forma falha em um caso específico
* [Content] Cortar: problema de amostragem quando o nó de corte tem uma resolução mais baixa do que a entrada
* [Geral] Falha ao fechar o Designer ao gerar a biblioteca
* [Graph] Os nós de bitmap não refletem a compactação do bitmap associado
* [Gráfico] O cache não é limpo ao limpar as miniaturas de nó após a primeira renderização
* [Graph] Tamanho do nó incorretamente invalidado
* [Graph] Falha ao enviar em alguns casos ao alterar conexões de entrada em um nó de processador de pixel
* [Gráfico MDL] Falha ao restaurar um valor padrão de chamada de função
* [Propriedades] Os botões &#39;Editar&#39; e &#39;Matriz&#39; nos parâmetros de matriz de transformação são confusos

### 9.2.3 (2019.2.3)

*(Lançado: 26 De novembro De 2019)*

**Adicionado:**

* [MacOS] Notarize o software para seguir os novos requisitos de distribuição do MacOS Catalina

**Corrigido:**

* [Padeiros] Falha ao assar usando um recurso de mapa de inclinação com um link inválido
* [Padarias] Os conjuntos de UV diferentes de 0 não são tidos em conta no Embree
* [Bakers] &#39;Bent Normals from Mesh&#39; gera resultados incorretos com conjuntos UV diferentes de 0 em DXR
* [Padeiros] Os parâmetros do &#39;Conjunto UV&#39; são redefinidos para o valor &#39;0&#39; ao reabrir a janela de cozimento
* [Bakers] “Position” gera uma imagem preta com conjuntos UV diferentes de 0
* [Content] Smart Auto Tile: problema de amostragem em 8k
* [Conteúdo] Atlas splitter: a detecção de forma falha em alguns casos, o parâmetro de precisão deve ser exposto
* [Conteúdo] Pow não retorna o valor correto em alguns casos
* [Content] Flood Fill para índice: resultado incorreto quando publicado em sbsar
* [Library] Falha ao carregar o primeiro pacote SBS da sessão
* [Library] A configuração &#39;Show Resources in the Library by Default&#39; é ignorada para recursos importados diretamente para o painel do Explorer
* [Console] Mensagem inesperada no console ao usar o menu de nó
* [Parâmetros] Não é possível remover uma única entrada na lista de uso de saída
* [3DView] a cena não é recarregada corretamente quando o arquivo de cena é modificado no disco.[Graph] A filtragem do menu Nó está incorreta ao usar as saídas de Valor

### 9.2.2 (2019.2.2)

*(Lançado: 23 de outubro de 2019)*

**Corrigido:**

* [Graph] A filtragem do menu Nó está incorreta ao usar saídas de Valor
* [Graph] Falha ao exibir o menu de nó
* [Gráfico] A ferramenta de pesquisa aparece ao usar o atalho de deslocamento
* [Graph] Falha ao gerar menus de nó consecutivamente a partir do conector de entrada de valor
* [Gráfico] Comentários contendo cadeias de caracteres longas são cortados
* [Graph] O realce de fluxo está incorreto ao criar um nó usando o menu arrastar do conector
* [Graph] Falha ao remover todos os itens de gráfico da cena ao carregar um gráfico diferente
* [Graph] Falha ao usar para criar nó ao usar a opção clicar e arrastar do conector
* [Graph] Falha ao usar a ferramenta “Localizador de nós”
* [Graph] A cor do pino de saída está incorreta no modo “Material Compacto”
* [Cooker] Os nós posteriores aos nós de várias saídas não são atualizados corretamente
* [Cooker] Problema com saídas Value e nós de passagem
* [Cooker] O Processador de Valor gera resultados incorretos quando apenas um nó &#39;Get&#39; é usado
* O nó [Content] &#39;Contrast/Luminosity&#39; gera um valor de Alpha de 1.0
* O modelo &#39;Studio Panorama&#39; do [Content] não tem descrição
* [Content] Flood Fill para índice: resultado incorreto quando a entrada contém uma forma de quebra automática
* [Content] &#39;Mesclagem HDR&#39;: cálculo de exposição interna incorreto
* [Nó ponto] Falha ao usar um nível e um nó ponto
* [Gerenciador de Dependências] A ação “Ir para” não funciona mais
* [PSD] Falha ao desfazer a exclusão de vários nós que foram incluídos no PSD Exporter
* [UI] Falha ao fechar o gráfico usando o menu “Janela” e abrir um novamente enquanto um está fixado
* [Editor de Degradê] O botão “Remover Chave” é muito grande
* [Engine] Problema de precisão com sqrt() acos() e asin()
* [Bakers] AO da malha: o controle deslizante “Ângulo de propagação” tem um intervalo de valor incorreto quando ajustado

### 9.2.1 (2019.2.1)

*(Lançado: 20 De setembro De 2019)*

**Adicionado:**

* [Modelos] Adicione nós de entrada padrão a Specular/Textura reluzente e a outros modelos
* [Modelos] Adicionar modelo de Anisotropia PBR
* [Visualização 3D] Aumente as distâncias longas do plano de clipe automático
* [3D View] PBR Coated: alterar valor padrão para herança normal de Coat
* [Content] Atlas splitter: adicionar opção para o recurso “Corte automático”
* [Menu Nó] Não filtrar nós sem entrada

**Corrigido:**

* [Content] Atlas splitter: algumas saídas não são cortadas corretamente ao usar a opção “Corte automático”
* [Content] Mistura de Height de material: erro de cozimento relacionado ao parâmetro inexistente
* [Content] “Plane Light”: o modo UV do padrão não funciona corretamente
* [Content] “Height to Normal World Unit”: a entrada é forçada para 16 bits
* [Content] Formas inesperadas ao usar o nó &#39;Chanfro&#39; de angular sem divisão em blocos gráficos em formas pequenas
* [Biblioteca] Os ícones do sbsar não são visíveis na biblioteca
* [Library] Usar “\” para filtrar o URL não funciona mais
* [Library] Os valores do filtro diferenciam maiúsculas de minúsculas
* [Library] O filtro de pesquisa não funciona quando a opção “Composição” está marcada
* [Preparadores] Clicar duas vezes em células específicas e descartar a alteração as reverte para valores incorretos
* [Bakers] O texto do estado de back-end na janela bakers sempre mostra &#39;aceleração por GPU : enable&#39;
* [Cooker] Falha ao processar uma dependência de &#39;impostor&#39; em um gráfico
* [Fogão] A conversão em tons de cinza tem o tamanho de saída incorreto ao usar o valor
* [Explorer] Falha ao processar “Publish on Share”
* [Graph] Falha ao abrir um pacote específico
* [MDL] Falha ao usar operador cast
* [Modelos] Os identificadores de saída não estão corretos no modelo com revestimento PBR

### 9.2.0 (2019.2.0)

*(Lançado: 29 de agosto de 2019)*

**Adicionado:**

* [Content] Novas formas de “Panorama Light”
* [Conteúdo] Novo filtro de Nadir patch de &#39;Panorama&#39;
* [Conteúdo] Novo filtro “Nadir extract de panorama”
* [Conteúdo] Novo filtro “Panorama Straighten Horizon”
* [Conteúdo] Novo filtro “Rotação de Panorama”
* [Content] Novo nó “Panorama Position”
* [Content] Novo nó “Panorama Physical Sun and Sky”
* [Content] Novos nós “Degradês de panorama”
* [Content] Novo filtro “Mesclagem HDR”
* [Conteúdo] Novo filtro &#39;Visualização HDR&#39;
* [Content] Novo filtro &#39;Color temperature adjustment&#39;
* [Content] Novo nó &#39;Blackbody&#39;
* [Content] Novo filtro de &#39;Exposição&#39;
* [UI] Menu de Criação de Nó: exibir e gerenciar Favoritos no menu
* [UI] Adicionar/Remover um nó dos favoritos do Menu de Criação de Nó
* [UI] Menu de criação de nó: gera o menu ao clicar/arrastar um link de uma saída
* [UI] Menu de Criação de Nó: filtrar o conteúdo de acordo com o tipo de seleção atual
* [Visualização 3D] Anisotropia de suporte
* [Exibição 3D] Efeito Suporte de revestimento
* [Visualização 3D] Suporte à dispersão de subsuperfície
* [Graph] Nó de ponto
* [Gráfico] Otimizar a renderização do gráfico armazenando em cache os resultados do cozimento
* [Preferências] Altere o valor padrão de “Limite de tamanho de cozinha” para 8192
* [Preferências] Adicione um botão de alternância para ativar ou desativar a nova funcionalidade de tecla “Tab”
* [API] Adicionar método SDResource.getPackage()
* [Iray] Atualização para o SDK NVIDIA Iray RTX 2019.1.3 (317500.3714)
* [Explorer] Permite vincular qualquer tipo de arquivo como um recurso no Pacote
* [GradientNode] Pressione ESC para cancelar a separação de gradiente
* [Parâmetros] Remover maiúsculas automáticas em identificadores
* [Project] Adicione uma opção para especificar se os gráficos e recursos são “Visíveis na biblioteca” por padrão
* [Predefinições] Fixar automaticamente parâmetros modificados

**Corrigido:**

* [MDL] Não é possível exportar o módulo devido a um problema de tipo de parâmetro
* [MDL] O int exposto não é visível ao carregar
* [MDL] Falha durante exportação de MDL
* [MDL] Falha ao modificar a cor de um nó de superfície de material
* [MDL] void MDLGraphNodeControllerSelector::updateSelectorCurrentMember(const DataMessage&amp; msg) está quebrado
* [Graph] thickness de vínculo incorreto na exibição do gráfico
* [Graph] Muitas invalidações são acionadas ao ajustar parâmetros
* [Graph] Falha ao fechar um pacote enquanto duas janelas estão abertas e ao usar a edição no contexto
* [Gráfico de funções] O aviso não aparece ao fechar a exibição de função
* [Exibição 3D] Falha na inicialização da exibição 3D quando a projeção da câmera é definida como “ortográfica” como um estado de cena padrão
* [Exibição 3D] O DOF pós-FX permanece habilitado no Iray
* [Visualização 2D] A janela de seleção de pincel desaparece ao alterar o tamanho do pincel
* [2D View] Painel de informações: os valores são cortados com um layout específico
* [2D View] A imagem é deslocada ao minimizar e restaurar a janela principal
* [Padeiros] A lista de seleção &#39;Do recurso&#39; não foi filtrada corretamente
* [Padarias] Falha ao encadear “Mapa de cores da malha” e “Mapa normal da malha” padeiros no Embree
* [Padeiros] A curvatura por cozimento de vértice resulta em artefatos graves
* [Explorer] Não é possível importar os recursos UDIM, arrastá-los e soltá-los no Explorer
* [Explorer] A janela do Explorer não é filtrada corretamente ao vincular malhas e fontes após vincular formatos de arquivo incomuns
* [Explorer] Os recursos ficam visíveis quando o gráfico tem “mostrar na biblioteca” definido como “não”
* [Content] As entradas &#39;Pow&#39; e &#39;clamp&#39; não estão na ordem correta
* As entradas do nó [Content] &#39;RGBA Merge&#39; não estão rotuladas
* [Cooker] Conexões inválidas de valores numéricos são avaliadas mesmo assim
* [Fogão] Afirmar ao conectar uma entrada de imagem a um valor de entrada
* [UI] O cursor do mouse trava no estado “redimensionar” em alguns casos específicos
* [UI] Clicar com o botão direito do mouse na visualização de pacote não exibe o menu correto no Linux
* [Dependências] O caminho do arquivo de recursos temporários não está correto
* [Dependências] Aviso de recurso de bitmap ausente permanece ativo após a realocação
* [Biblioteca] Algumas miniaturas não são geradas
* [Biblioteca] Os arquivos MDL são exibidos na biblioteca
* [Parâmetros] Falha ao expor parâmetros
* [Parâmetros] Falha após recriar um novo elemento na lista suspensa
* [Exportar] Falha na exportação em lote de 8K
* [Predefinições] Falha ao aplicar uma predefinição que envolve booleanos em instâncias do SBS
* [Scripting] A tela &#39;Bem-vindo&#39; ainda aparece ao usar o argumento de linha de comando &#39;—quit&#39;

### 9.1.3 (2019.1.3)

*(Lançado em: 19 de agosto de 2019)*

**Corrigido:**

* [Bakers] Falha no DXR quando as proporções da saída do bake e do mapa de inclinação são incompatíveis
* [Bakers] “Oclusão ambiente da malha” panificação produz resultados incorretos com Optix ou DXR ao usar um mapa normal
* [Bakers] O panificador &#39;Curvatura&#39; gera resultados incorretos ao usar a configuração “Por vértice”
* [Padeiros] As mensagens de erro indicam a back-end que falhou em vez da causa do erro
* [Bakers] Falha ao processar um padeiro de mapa de detalhes sem uma malha alta poli
* [Padeiros] O mapa de inclinação parece não afetar todas as saídas com a DXR ativada
* [Content] mg\_leaks: typo no nome de parâmetros
* [Content] “Shape” retorna um aviso de cozimento
* [Conteúdo] Os polígonos 1 e 2 não oferecem suporte a funções aleatórias
* [Conteúdo] Os polígonos 1 e 2 podem ter menos de 3 lados
* [Content] Normal para Height HQ não funciona corretamente em não quadrado
* [Parâmetros] Parâmetros de entrada inteiros: a lista suspensa não mostra os valores

### 9.1.2 (2019.1.2)

*(Lançado em: 2 de julho de 2019)*

**Corrigido:**

* [Visualização 3D] A exportação de visualização 3D com profundidade de campo ativada parece incorreta
* [3D View] O canal de Alpha das imagens de PSD está incorreto ao usar salvar renderização
* [3D View] PNG e PSD são interrompidos ao usar a opção salvar renderização com o Iray
* [Exibição 3D] o formato dds não funciona ao salvar a renderização
* [Gráfico] Os nós são deslocados ao combinar a ação do clique direito e esquerdo de maneiras específicas
* [Gráfico] Modificar instâncias de Função não atualiza mais o resultado do nó
* [Gráfico] Falha ao exibir o menu Barra de espaço
* [Content] Extrusão de forma: problema de qualidade quando a forma não tem rotação
* [Conteúdo] A Sombra projetada da forma (e Tons de cinza) não produz sombra sem a divisão em blocos gráficos H e V
* [Conteúdo] Problema normal de corte de material
* [Padeiros] As predefinições de padeiros JSON não são carregadas corretamente
* [Bakers] Falha ao assar malhas pesadas usando Optix ou DXR (agora pode falhar devido a Vram insuficiente, mas não falhará)
* [Editor de bitmap] As ferramentas de pintura de bitmap deslocam os traçados e redesenha na caixa delimitadora de traçado
* [Editor de bitmap] Ferramentas de pintura de bitmap corrompidas no OSX
* [IU] Alguns menus de botão estão inacessíveis
* [UI] Falha ao arrastar e soltar uma instância de padeiro
* [SVG] As ferramentas de edição de SVG incorporadas não são confiáveis
* [Parâmetros] Falha ao aplicar uma predefinição com parâmetros boolianos em uma instância SBSAR
* [Network] Às vezes, ocorre uma falha quando ocorre um erro em uma conexão criptografada SSL

### 9.1.1 (2019.1.1)

*(Lançado: 28 de maio de 2019)*

**Adicionado:**

* [PythonIntegration] Salvar e restaurar o estado do gerenciador de plug-ins
* [Preferências]&#x200B;[Dependências] Adicione uma opção para determinar como o caminho do arquivo de dependências é armazenado
* [Content] Mapeador de Flood Fill: adicionar a opção “Ajustar caixa de forma”

**Corrigido:**

* [Content] Mapeador de Flood Fill: “Escala automática de rotação” faz o efeito oposto
* [Content] A entrada “luminance\_offset\_map” não é usada pela “Cor do mapeador de Flood Fill”
* [Content] O nó &#39;Flood Fill Mapper Grayscale&#39; gera artefatos de revisão
* [Content] Não é possível publicar Extrusões na Altura
* [Parâmetros] As predefinições incorporadas no sbsar não são carregadas no Designer
* [Padeiros] O nome do padeiro não é exibido corretamente na lista de padeiros
* [Exibição 3D] “Exibir saídas na exibição 3D” não funciona para valores
* [Fogão] Falha ao corrigir um tipo de parâmetro incorreto
* [API] A função SDResource.setInputPropertyFromId não funciona nos parâmetros de entrada SDSBSCompGraph
* [Updater] alguns sbs não podem ser atualizados em 2019
* [Explorer] Falha ao importar um arquivo .obj específico
* [PythonIntegration] Barras invertidas que não são adequadamente escapadas no Windows ao inicializar PYTHONPATH
* Problema de valor [UI] com alguns controles deslizantes em padeiros
* [Linux] O Designer não pode ser executado no CentOS &lt; 7.6

### 9.1.0 (2019.1.0)

*(Lançado em: 09 de maio de 2019)*

**Adicionado:**

* [API] Adicione o parâmetro &#39;updatePackages&#39; ao método SDPackageMGR.loadUserPackage() para controlar se os atualizadores devem ser aplicados ou não ao carregar
* [API] Adicionar a capacidade de desconectar uma SDConnection
* [API] Adicionar a classe SDSBSARExporter para publicar um SDPackage
* [API] Adicionar classe SDHistoryUtils para gerenciar comandos desativáveis
* [API] Adicionar definição de nó de entrada em tons de cinza no Gráfico de Composição de Substance (sbs::compositing::input\_grayscale)
* [API] Adicionar definição de nó de entrada de valor no Gráfico de Composição de Substance (sbs::compositing::input\_value)
* [API] Adicionar método SDProperty.isFunctionOnly()
* [API] Adicionar suporte a parâmetro de entrada personalizado em SDSBSCompNode
* [API] Adicione o parâmetro &#39;reloadIfModified&#39; ao método SDPackageMGR.loadUserPackage() para controlar se um pacote deve ser recarregado, caso seja modificado
* [API] Adicionar método SDPackageMgr.getPackages()
* [API] Adicionar a possibilidade de obter/adicionar/remover caminhos raiz do SDModuleMgr
* [API] Permite obter o ponteiro do buffer de pixels e o timbre de uma SDTexture
* [API] Permitir a recuperação do ponteiro de MainWindow
* [API] Permite criar menus personalizados no menu principal
* [API] Permite criar DockWidgets personalizados na janela principal
* [API] Usar nomes de objetos para localizar menus nas barras de ferramentas
* [API] Fornece o sistema para gerenciar notificações de aplicativos para a API
* [PythonIntegration] Adicionar variável de ambiente padrão para procurar plug-ins Python
* [PythonIntegration] Adicionar pesquisa de texto e substituir ao editor de Python
* [PythonIntegration] Criar instância de plug-ins Python na inicialização
* [PythonIntegration] Levar em conta a variável de ambiente PYTHONPATH
* [PythonIntegration] Permitir a criação de barras de ferramentas em widgets de gráficos
* [PythonIntegration] Suportar threads Python
* [PythonIntegration] Adicionar um gerenciador de plug-ins (no menu “Ferramentas”)
* [Content] Rotação de vetor normal: adicione uma entrada de imagem opcional para orientar o ângulo
* [Conteúdo] Novo filtro Mín/Máx
* [Content] Novo filtro “Flood Fill para índice”
* [Content] Novo filtro “Flood Fill Mapper”
* [Conteúdo] Novo filtro de Atlas splitter
* [Conteúdo] Melhorar o filtro Triplo Planar
* [Content] Novo filtro de Non Uniform Directional Warp
* [Content] Nova distorção multidirecional
* [Conteúdo] Novo filtro de Extrusões na Altura
* [Engine] Fxmap: novo padrão “Gradação com deslocamento”
* [Engine] Suporte para processamento de valor uniforme (nó Novo processador de valor)
* [3D View]&#x200B;[Bakers] Aprimoram o desempenho do carregador OBJ
* [Exibição 3D] Aumenta as distâncias do plano do clipe da câmera
* [Preferências] Adicionar configurações para preparadores
* [Graph] Tornar a invalidação mais rápida, evitando comparações de strings
* [MDL] Suporte a arrays MDL
* [UI] Melhorias na interface de seleção de mecanismo
* [IRay] Atualização para o SDK do IRay 2018.1.4
* [Gerenciador de Dependências] Usar “último caminho” ao realocar um recurso
* [Cozinhar] Adicionar suporte de rótulos booleanos no sbsar
* Integrar Qt 5.12.2

**Corrigido:**

* [Graph] As conexões são interrompidas ao alterar o nome da entrada
* [Graph] Muitas invalidações são acionadas ao ajustar parâmetros
* [Graph] A ação “Copiar para área de transferência” não funciona se clicarmos com o botão direito do mouse em uma medalha
* [Gráfico] Mover um quadro usando Alt não é armazenado no .sbs
* [MDL] O perfil de cores não é atualizado automaticamente no editor de MDL
* [MDL] falha ao exportar módulo que contém uma configuração específica
* [MDL] Falha ao exportar um gráfico MDL que contém um LightProfile ou um recurso MBSDF
* [IU] Os atalhos não são mais exibidos em menus de contexto
* [IU] A janela flutuante torna-se encaixável após a reinicialização
* [Script] A opção Cancelar não funciona no editor Python
* [Script] A opção “sim para todos” no menu Salvar não funciona
* A lista suspensa [Parâmetros] não é exibida corretamente após a cópia
* [Explorer] A realocação de recursos deve abrir o último caminho realocado por padrão
* [Biblioteca] O conteúdo da biblioteca é sempre recriado ao alternar de uma versão para outra
* [Library] Os bitmaps importados são invalidados ao salvar
* [IRay] O espaço tangente não é calculado corretamente/mapeamento normal incorreto
* [Function] Falha ou falha ao criar um novo gráfico com base na seleção
* O valor padrão de propriedades de [API] não está definido

## Versão 8

### 8.3.4 (2018.3.4)

*(Lançado: 12 de abril de 2019)*

**Adicionado:**

* [Content] Transformação normal/Transformação de material: adicione uma opção para ativar a transformação Dimensionar e Inclinar

**Corrigido:**

* [Content] O filtro espiral não funciona corretamente quando funções aleatórias são usadas em funções de parâmetros
* [Conteúdo] Transformação normal/Transformação de material: Normal não é normalizado após uma transformação de escala
* [Content] Girar fornece resultados incorretos quando a quantidade é aleatória
* [Graph] Falha ao arrastar uma saída com a tecla Shift pressionada e depois alternar para arrastar com a tecla ctrl pressionada
* [Graph] Falha ao manipular pontos de divisão
* [Graph] Queda de desempenho ao exibir emblemas de nó
* [Script] O uso de ações personalizadas pode falhar após 30 segundos
* [Preferências/Projetos] Scripts ativados de todos os projetos devem ser executados (na seção “Scripts”)
* [MDL] falha ao vincular um gráfico MDL a outro gráfico MDL
* [Parâmetros] Os nós não são atualizados após definir a propagação aleatória do gráfico para um parâmetro exposto
* [PSD] A atribuição do nó de cor altera o tamanho da miniatura da camada, atribuindo um nó de tons de cinza não
* [API] Exceção sem tratamento com SDNode.getPropertyValueFromId()

### 8.3.3 (2018.3.3)

*(Lançado em: 19 de fevereiro de 2019)*

**Corrigido:**

* [Content] As saídas de Material de base PBR não têm o nome de grupo correto

### 8.3.2 (2018.3.2)

*(Lançado em: 19 de fevereiro de 2019)*

**Adicionado:**

* [Padeiros] Adicionar um rótulo indicando a configuração do sufixo atual para “Corresponder por nome”

**Corrigido:**

* [Graph] Falha ao manipular pontos de divisão
* [Graph] Problema de invalidação quando a profundidade de bits do nó de entrada é alterada
* [Gráfico] As opções de cálculo de miniatura não funcionam mais
* [Gráfico] O espaço vazio é exibido sob a navegação estrutural com um layout de interface específico
* [Graph] O estilo do link está incorreto no contexto
* [Gráfico] As miniaturas não são exibidas corretamente em gráficos de função/mdl em telas Hi DPI
* [Content] Shape Splatter Blend Color: nenhuma opção para especificar o formato de mapa normal
* [Conteúdo] Erro ortográfico na dica de ferramenta de interpolação linear
* [Conteúdo] A transformação normal não manipula as transformações de espelhamento e inclinação corretamente
* [Content] Gradiente axial, radial, circular não suportam funções aleatórias
* [Content] Gradiente radial não funciona corretamente em não quadrados
* [API] output\_exporter.sbs sempre precisa ser atualizado ao usar o script export\_output
* [API] Falha após usar o script export\_output
* [API] Falha ao definir o valor numérico das anotações nas entradas do Gráfico de composição
* [Explorer] Falha aleatória ao salvar um projeto
* [Explorer] Não é possível abrir sbs com extensão em maiúsculas
* [UI] O tamanho da janela “Novo Substance” não é persistente
* [UI] O menu do botão direito do mouse na instância da função não é consistente com a composição do gráfico
* [Panificadores] Falha ao abrir os panificadores em uma malha específica
* [Padeiros] Cálculo incorreto para padeiros DXR quando UVs têm um valor de ordenada 0
* [Updater] Falha ao cancelar o atualizador
* [Visualização 3D] A esfera primitiva tem seus UVs deslocados em 1 unidade
* [Fogão] Pontilhamento aleatório ao cozinhar bitmaps
* [Player] Os botões de controle da janela são pequenos
* [Player] Os ícones do botão estão quebrados

### 8.3.1 (2018.3.1)

*(Lançado: 20 de dezembro de 2018)*

**Adicionado:**

* [API] Adicionar SDConnection.getOutputProperty() e SDConnection.getOutputPropertyNode()
* [API] Adicionar documento sobre todas as definições de recursos
* [API] Altere a propriedade de anotação SDSBSCompNode &#39;visibleif&#39; para &#39;visible\_if&#39; para fins de consistência

**Corrigido:**

* [Graph] Pressionar a tecla TAB uma segunda vez não fecha o menu Nó
* [Gráfico] Os emblemas do Modo de exibição 3D não funcionam corretamente em algumas situações
* [Graph] Os pacotes somente leitura podem ser modificados
* [Bakers] A barra de progresso age de forma estranha ao carregar uma malha poli muito alta
* [Padarias] Artefatos na malha com normais voltados para dentro
* [Padeiros] O widget de parâmetros e saída de padeiros não pode ser desrecolhido
* [Explorer] Recursos 3D são carregados quando um pacote é aberto
* [CmdLineArgs] “—news hide\_changelog:true” não funciona mais

### 8.3.0 (2018.3.0)

*(Lançado em: 05 de dezembro de 2019)*

**Adicionado:**

* [Gráfico] Adicionar uma Trilha ao editar subgráficos/funções
* [Graph] Adicione TAB como atalho para gerar o “menu de nó”
* [Graph] Realçador de nó para nós pai da seleção
* [Gráfico] Adicionar Ctrl+E como atalho para abrir a função e os subgrafos do Processador de pixels
* [Graph] Conecta o novo nó à primeira saída visível do nó selecionado
* [Gráfico] Adicionar nó &#39;Medalhas&#39;
* [Gráfico] Adicionar aviso sobre a composição de nós por meio de medalhas
* [Gráfico] Adicionar a possibilidade de pesquisar um nó por seu nome, atributos ou UID
* [API] Permitir a criação e modificação de dados
* [API] Permitir a exportação de SDPackage e SDMDLGraph para Módulos MDL (consulte SDMDLExporter)
* [API] Permite recuperar todos os nós, enums e definições de struct (consulte SDModuleMgr)
* [Visualização 3D] Alternar para mapas de cubo para o renderizador OpenGL
* [Visualização 3D] Exportar imagem hdr linear ao salvar em .exr ou .hdr
* [Bakers] Integrar tecnologia de rastreamento de raios DXR
* [IRay] Integrar o SDK do IRay 2018.1
* [Engine] Suporte ao mecanismo SSE (CPU) para processamento de imagens de ponto flutuante hdr
* [Engine] Adicione uma opção de linha de comando (—gpu x) para especificar o dispositivo de GPU dedicado ao mecanismo Substance
* [Content] Novo nó de Renderização PBR
* [UI] Guias de retrabalho e barra de título
* [Gerenciador de Dependências] Impedir a atualização da lista de dependências quando as ações do usuário não afetarem as dependências

**Corrigido:**

* [Graph] Falha ao instanciar um gráfico em si mesmo
* [Graph] O nó duplicado não está selecionado
* [Graph] problema de computação ao usar uma mesma instância de nó em 2 gráficos MDL diferentes
* [Gráfico] a tecla Z deve centralizar a exibição no centro da caixa de cena
* [Gráfico] Ignorar espaço de cores nas regras de conexão ao usar link de material
* [Gráfico] Evitar a abertura de saídas na visualização 3D ao abrir um gráfico em console
* [Graph] A colagem de nós é lenta quando a opção “Abrir nó recém-criado” está ativada
* [Exibição 3D] Declarar ao arrastar e soltar uma malha específica
* [Exibição 3D] A opção habilitada para Escala UV não funciona no mapa de height
* [Content] Tri-Planar: vários problemas relacionados a eixos e transformações
* [Content] Desfoque de Inclinação em Tons de Cinza: uma das amostras não tem o modo de mesclagem correto ao usar mín. ou máx.
* [Conteúdo] Gradiente linear 2 resultado errado em baixa resolução
* [API] SDPackage.findResourceFromUrl() também pôde recuperar recursos localizados em outro SDPackage
* [API] SDPackage.getChildrenResources() sempre retorna o primeiro elemento no modo não recursivo
* [API] [Documentação] Enums, structs localizados na pasta &#39;generated&#39; não são refletidos na documentação
* [UI] A largura da exibição 2D não deve ser restringida
* [Gradiente] Falha ao selecionar no Mac
* [Explorer] Falha ao fechar e reabrir um gráfico
* [Mac] O seletor de cores não funciona em várias telas
* [Parâmetros] A caixa giratória em parâmetros inteiros não funciona
* [Cooker] Falha ao criar determinados nós no OSX 10.13
* [Filtro de curva] As teclas e os pontos de controle podem terminar com um valor -0.0 ou um valor estranho “quase zero” no editor de Curva
* [Visualização 2D] O widget de posição não está disponível para gráficos provenientes de sbsar
* [PSD] Problema de camada após a exportação com dependências

### 8.2.2 (2018.2.2)

*(Lançado em: 4 de outubro de 2019)*

**Corrigido:**

* [Content] A Sombra da forma não funciona corretamente quando a divisão em blocos gráficos está desativada
* [Conteúdo] O preenchimento inundação para tons de cinza aleatórios / cor não funciona corretamente em alguns casos
* O Flood Fill [Content] está incorreto no não quadrado
* [Content] Flood Fill para Cor / Tons de cinza está quebrado
* [Content] O QuadTransform é irregular na CPU
* [Conteúdo] Forma de estrela gera um modo de divisão em blocos gráficos “Sem divisão em blocos gráficos”
* [Conteúdo] Saída de cor de mesclagem de respingo de forma com profundidade de bits absoluta de 32 f
* [Conteúdo] A Cor de mesclagem do respingo da forma é longa para ser computada se seu formato não estiver definido como 32F
* [Graph] Falha ao vincular imagem como entrada de um mapa de fax enquanto as propriedades de iteração são exibidas
* [Graph] Os tempos parecem incorretos ao editar o gráfico no contexto
* [Graph] Falha aleatória ao salvar o gráfico
* [Gráfico] o modo de material não funciona com sbsar
* [Visualização 3D] A atribuição de materiais não é restaurada corretamente
* [Visualização 3D] Algumas configurações de arquivo de estado 3Dview não estão carregadas corretamente
* [2D View] o monitor de Alpha sempre fica preto
* [Visualização 2D] O botão Exibir imagem em tons de cinza não funciona para imagens com alfa
* [UI] o gerenciador de dependência é gerado na inicialização mesmo quando não ativado no Mac
* [IU] Alguns botões executam ações mesmo ao soltar o mouse fora
* [API] Falha ao tentar manter um item de matriz fora do escopo da matriz de onde ele vem
* [Gráfico MDL] A visualização do nó está de cabeça para baixo
* [Gráfico MDL] O Deslocamento do nó de visualização é diferente do da Visualização em 3D
* [Console] O desempenho fica muito lento quando o console contém muitas mensagens
* [Console] Avisos do Qt ao iniciar o Designer no CentOS
* [FX-Map] Falha ao excluir vínculos entre entradas e FX-map
* [Functions] Não é possível definir um nó de tipo de cadeia de caracteres como saída no Recurso de Função
* [Preferências] Não há foco no menu Preferências. O usuário pode alterar um valor acidentalmente ao navegar
* [FX-Map] A caixa de combinação Índice de imagem de entrada não é atualizada corretamente ao adicionar/remover entradas
* [Dependências] Falha ao excluir recursos UDIM usados em um gráfico
* [API] SDLocationContext.getCurrentGraph() sempre retorna nulo
* [Publish] URL incorreto para página de download de Substance Player

### 8.2.1 (2018.2.1)

*(Lançado: 17 de agosto de 2018)*

**Adicionado:**

* [UI] Adicionar uma mensagem na barra de tarefas quando a opção “Edição de contexto interno” estiver ativada
* [Preferências] Reformule o rótulo da opção “Em edição de contexto”

**Corrigido:**

* [Gráfico] O atalho Colar sem link não funciona no gráfico de composição
* [Graph] A invalidação é muito longa quando a edição no contexto está ativada
* [Graph] Falha ao vincular nós
* [Gráfico] Falha ao revincular nós
* [Gráfico] Falha ao mover quadros
* [Graph] Falha ao alternar UVTile em gráfico e malha não é mais udim
* [Graph] Falha ao usar ctrl+z após colar nós
* [Graph] Selecionar nós pai é muito lento
* [Padeiros] Mover mapas para cima/para baixo permite que o usuário redimensione a linha
* [Padeiros] O caminho para salvar ou carregar a predefinição nunca é salvo
* [Padarias] Gaiola é usada mesmo quando não selecionada na janela de cozedura
* [Padeiros] A correção de inclinação não está funcionando corretamente
* [Padarias] Desempenho muito lento quando o espaço UV negativo está na vista
* [Padeiros] Clicar no botão Cancelar não cancela a carga de malha
* [Bakers] Não é possível assar usando uma gaiola se o mapa de inclinação estiver vazio e definido como verdadeiro
* O Flood Fill [Content] é lento em 4K
* [Content] A função linear para sRGB está interrompida
* [Content] O plano de fundo em Escala de Cinza Aleatório Lado a Lado é dirigido por um flutuador4 em vez de um flutuante, impede que o cozimento
* [Conteúdo] Respingo de forma: Multiplicador de mapa de posição/vetor não funciona corretamente
* [Scripts] Ctrl + o não funciona no editor Python
* [Scripting] O editor Python continua solicitando mesmo depois de fechar
* [Scripts] Congela ao criar vários scripts novos
* [IU] Os ícones na biblioteca são pixalados
* [UI] Os painéis que estão flutuando por padrão se comportam mal
* [Explorer] Falha ao importar uma malha no CentOS
* [Explorer] A malha UDIM é carregada duas vezes
* [Fogão] Sem temporização para nós no contexto
* [Fogão] Estouro de pilha ao cozinhar
* [License] Autenticação incorreta com credenciais válidas
* [License] Licença flutuante relatada mais de uma vez para o mesmo usuário
* [Visualização 3D] O valor padrão de V do material de bloco UV está errado
* [Visualização 3D] Regressão de desempenho comparada com 2018.1.x
* [Preferências] Falha ao usar um arquivo de configuração de um servidor
* [Biblioteca] Falha ao excluir um filtro dentro da biblioteca
* [SVG] Problema de dependência ao usar alias
* [Níveis] Os bitmaps HDR de 32 bits fazem o editor de níveis piscar ao mover a posição dos widgets
* [PSD] A janela do PSD de importação vinculada é exibida duas vezes
* [Iray] A cena é atualizada quando uma luz desativada é modificada
* [MDL] Falha ao excluir todos os nós de um modelo MDL
* [Engine] Enorme quantidade de deslocamento no FX-Map pode congelar SD
* Falha no Crashpad na inicialização
* A variável de ambiente Python faz com que o Designer falhe na inicialização

### 8.2.0 (2018.2.0)

*(Lançado: 19 de julho de 2018)*

**Adicionado:**

* [UI] Novo estilo
* [UI] Novos controles deslizantes
* [IU] Fazer janelas flutuantes flutuarem
* [UI] Alterar o layout da janela Preferências
* [UI] Biblioteca: remover barra de filtro
* [UI] Biblioteca: remover sobreposição de exibição de seleção
* [UI] Adicionar uma mensagem na barra de tarefas quando o aplicativo estiver salvando automaticamente um pacote
* [UX] Propriedades: mesclar menus “função” e “redefinir para padrão”
* [Conteúdo] Novos nós de respingos de forma (mais filtros complementares)
* [Conteúdo] Adicionar Flood Fill aos filtros Cor/Tons de Cinza
* [Content] Suporte a novo Flood Fill: suporte a formas com furos
* [Content] Flood Fill para Gradiente: adicionar entrada de imagem de Inclinação e ângulo
* [Conteúdo] Otimizar o filtro Nível automático
* [Conteúdo] Novo filtro de Extrusão de Forma
* [Content] Transformação de material: adicionar suporte para mapas normais girados
* [Conteúdo] Novos filtros de Rotação de vetor normal e Transformação normal
* [Content] Normal Normalize: melhore a qualidade do resultado.
* [Content] Novo filtro de transformação trappezoide
* [Content] Novo filtro Transformação quádrupla
* [Conteúdo] Adicionar padrão do Hemisfério ao nó Forma
* [Conteúdo] Adicione novos Gradientes com controles na Visualização 2D
* [Content] Adicionar saída UV ao nó “Cube GBuffers”
* [Gráfico] Quadro: ignorar texto de título maior que a caixa de quadro para seleção
* [Gráfico] Adicionar suporte para edição em contexto de subgráficos (experimental)
* [Graph] Criar quadro/comentário deve afetar o nó sob o cursor ao usar RMB
* [Gráfico] Quadro: ignorar texto de título maior que a caixa de quadro para seleção
* [Gráfico] Reutilizar a guia existente ao abrir uma função já aberta
* [Gráfico] Criar uma nova guia quando “Abrir referência” for usado
* [Graph] Função: não exibe as propriedades da função ao clicar no plano de fundo
* [Parâmetros] Remover o botão “Expor” dos gráficos fxmap
* [Parâmetros] Nível: Adicione um botão “Inverter”
* [Parâmetros] Expande o grupo “Parâmetros de entrada” ao criar um novo parâmetro de entrada
* [Propriedades] Adiciona as informações de url do pacote nos atributos do gráfico
* [Propriedades] Aumenta o tamanho do campo de descrição para nós de saída
* [Propriedades] Permite inserir a função Por pixel do processador de pixels mesmo para pacotes somente de leitura
* [Script] Novo editor Python API / Python (primeira iteração)
* [Padeiros] Otimizar a transferência de geometria durante a renderização
* [Visualização 3D] Alternar para o perfil principal do OpenGL
* [Exibição 3D] Suporte a mosaico/deslocamento no Mac
* [Functions] Recurso de função: listar entradas de imagem em nós de amostra

**Corrigido:**

* [Graph] falha ao vincular um nó a outro
* [Graph] obter variáveis na função de distribuição aleatória do gráfico não funciona
* [Graph] falha ao arrastar e soltar ruído em um gráfico
* [Graph] falha ao abrir um gráfico específico
* [Content] O resultado é diferente entre a Cor aleatória do bloco e a Escala de cinza
* [Content] Tile Aleatório: o resultado muda ao modificar o “Modo aleatório de simetria”
* [Content] A detecção de borda não funciona com resoluções não quadradas
* [Padarias] Artefatos ao assar curvatura usando uma malha UDIM
* [Padeiros] O mapa de Oclusão ambiente da malha é invertido ao usar um mapa normal
* [Bakers] A lista de conjuntos UV deve ser restrita aos conjuntos UV disponíveis
* [Explorer] falha ao excluir recursos durante o preparo
* [Transform2D] Falha ao expor o nível do mapa de Mip e os parâmetros de Cor de Fundo
* [Transform2D] Erro ao expor um Nível do mipmap de Transformação
* [PSDExport] O exportador de PSD não exporta tons de cinza 32F corretamente
* [2D View] A computação do histograma não funciona com nós 16F
* [PSD] Os PSD vinculados estão quebrados
* [Cooker] Função no parâmetro outputsize não avaliada corretamente
* [Exportar] O caminho das saídas de exportação deve ser igual ao caminho do pacote
* [Exportar] O caminho de exportação não é salvo usando um padrão vazio
* [Modelos] Grupo ausente para a posição no modelo do Painter
* [Ajuda] a ajuda da linha de comando não é exibida —news no Mac
* [Dependências] Exportar duas vezes após modificar um nome de pasta não funciona

### 8.1.2 (2018.1.2)

*(Lançado: 31 de maio de 2018)*

**Adicionado:**

* [Visualização 3D] Permite definir o estado de luz padrão nas configurações do projeto
* [Controle de versão] Remove o tempo limite de 30s ao chamar os scripts python

**Corrigido:**

* [Conteúdo] Base de Soma fractal: resultado incorreto com o terceiro nível (novo gráfico foi adicionado)
* [Content] O Fractal de ruído 3D Perlin é forçado para 32 bits
* [Content] Gradiente linear 3 não fornece o resultado certo ao usar tamanho não uniforme
* [Content] Normal Sobel não suporta opções de divisão em blocos gráficos
* [Conteúdo] O marcador\_1 é forçado para 8 bits
* [Content] Multiângulo para Normal: problema de computação interna
* [Content] O padrão Stripe não é compatível com valores negativos “Shift” (falha no mecanismo)
* [MDL] Falha ao tentar abrir um projeto MDL específico
* [MDL] O gráfico MDL não é calculado após uma operação fechada/reaberta
* [Exportar] As saídas de gráficos não atribuídos são exportadas usando a ferramenta de lote
* [Exportar] Exportar C16F em exr gera uma imagem em tons de cinza
* [Padarias] Os recursos de inclinação não são desativados na interface do usuário ao assar com uma gaiola
* [Padeiros] Falha quando o compartimento não tem o conjunto UV correspondente
* [Cooker] sbscooker: erro de cozimento relacionado ao “blend\_switch.sbs”
* [Cooker] O gráfico publicado não é renderizado corretamente
* [Engine] Transformação 2D: a cor fosca não está correta
* [Explorer] Falha ao reimportar uma malha de FBX
* [Widget de cor] O seletor de cores em tons de cinza seleciona apenas o valor do canal vermelho
* [3D View] O uso de “textcoordN” não funciona mais
* [Iray] O mapa normal é aplicado duas vezes para dielétricos

### 8.1.1 (2018.1.1)

*(Lançado: 12 de abril de 2018)*

**Adicionado:**

* [3D View] Defina o intervalo padrão de “Fator de mosaico” para [0, 16]

**Corrigido:**

* [Exibição 3D] Artefato visual estranho com GPU AMD específica
* [Exibição 3D] Congela com GPUs AMD específicas
* [3D View]&#x200B;[Padeiros] Normais gerados a partir de .obj têm bordas sólidas na costura UV
* [Exibição 3D] Falha ao computar harmônicos esféricos
* [Padeiros] Não é possível definir o recurso como “incorporado”
* [Padarias] falha ao assar
* [Padarias] Cozimento 2 versões diferentes de um mapa da malha UDIM é quebrado
* [Bakers] falha ao alternar entre gráficos contextuais e não contextuais
* [Padeiros] Ter o mesmo padeiro duas vezes os tornará sincronizados
* [Padeiros] renomear a macro $(custom) impede que a cozedura seja feita corretamente
* [Padeiros] A atualização de um mapa baked deve bloquear a interface do usuário
* [Padeiros] Atualizar todos os mapas baked cria recursos vazios
* [Bakers] Pressionar “Enter” para confirmar um valor de parâmetro remove o poli alto
* [Content] Tile Generator: erro de Rotação aleatória quando a Quantidade X e Y são diferentes
* [Conteúdo] alguns mapas de desgaste contêm instâncias fantasmas
* [Content] Cubo 3d: usar funções aleatórias em parâmetros não fornece o resultado esperado
* [Content] Ruídos fractais não são renderizados corretamente quando o Expansão não quadrada está desativado
* [Content] O Células 2 e o Células 4 não se comportam corretamente quando o Expansão não quadrada está desativado
* [Gráfico] Atualizar uma instância do sbsar cria um gráfico fantasma
* [Graph] A atribuição através do clique direito não deve exibir o submenu de blocos UV para malhas não UDIM
* [Gráfico] O sbsar republicado não foi atualizado corretamente
* [Gráfico] Nós não são invalidados corretamente quando o recurso é alterado
* [Cooker] O parâmetro de mesclagem alfa de premult não foi recuperado corretamente do sbsar
* [Fogão] o filtro de níveis não pinça valores quando cozido em uma sbsar
* [Cooker] A transformação implícita é executada antes dos nós FX-Map
* [Explorer] Pressionar a tecla del em um pacote pergunta ao usuário se ele deseja excluí-lo
* [Explorer]&#x200B;[Padeiros] Problema de realocação
* [Curva] Falha aleatória ao manipular teclas no editor de curvas
* [MDL] Tipo de gama não definido corretamente para uso personalizado
* [Parâmetros] Falha ao expor um parâmetro com o mesmo identificador de uma entrada existente
* [Propriedades] O uso de saída é editado sem diferenciação de maiúsculas e minúsculas

### 8.1.0 (2018.1.0)

*(Lançado: 09 de março de 2018)*

**Adicionado:**

* [Padeiros] Otimizar a cozedura de alta polietileno
* [Padarias] Melhorar o resultado em costuras para o padeiro de curvatura
* [Bakers] Mapas de cozimento para malha baseada em UDIM
* [Padeiros] Adicionar uma visualização 2D dedicada na janela Padeiro
* [Graph] Suporte para UDIMs
* [Gráfico] Otimizar o desempenho do fogão
* [Gráfico] Melhorar a velocidade de geração de miniaturas de nós
* [Gráfico] Manter cache de nó apenas para gráficos abertos
* [Gráfico] Adiciona uma barra de ferramentas ao gráfico de composição para controlar o modo de geração de Miniaturas
* [Visualização 3D] Adicionar um cache de geometria para otimizar a exibição de malhas de alta definição
* [3D View] Suporte à exibição UDIM (exibe o bloco atual)
* [3D View] Atualizar Cubo arredondado com topologia uniforme
* [Exibição 3D] Evite salvar a cena o tempo todo
* [Conteúdo] Adicionar nós de Ruídos 3D (Perlin, Perlin Fractal, Worley, Simplex)
* [Conteúdo] Nó Adicionar máscara de volume 3D
* [Conteúdo] Adicionar nó 3D linear gradient
* [Conteúdo] Adicionar nó de Gbuffers de cubo 3D (útil para pré-visualizar nós baseados em 3D)
* [Conteúdo] Adicionar nó de projeção planar 3D
* [Conteúdo] Adicionar filtro de Desfoque radial
* [Parâmetros] Exibe as propriedades de entrada/saída da imagem nas propriedades do gráfico
* [Parâmetros] Permitir a edição do caminho de recursos
* [Engine] Suporte para texturas de até 8k com o mecanismo CPU (SSE2)
* [Engine] Permitir que o Conversor de Tons de Cinza use pesos HDR para mecanismos HDR
* [Preferências] Adicione uma opção para desativar a criação automática de nós de conversão
* [Preferências] Defina a compactação padrão para png como “melhor velocidade”
* [UI] suportar link html nas propriedades do gráfico
* [UI] Centralize os botões “Sim / Não / Cancelar” na caixa de diálogo de confirmação de salvamento
* [Explorer] Aprimorar exibição de hierarquia de malha
* [IRay] Integrar o SDK do IRay 2017.1.4

**Corrigido:**

* [Padeiros] Adicionar uma macro no campo de nome de saída não a adiciona na posição do cursor
* [Padeiros] Nenhum material será exibido na lista se o objeto não tiver material
* [Bakers] Pressione Enter para confirmar os parâmetros do baker para abrir um menu suspenso
* [Padeiros] As texturas de cozimento não devem gerar comandos na pilha Desfazer
* [Padarias] Falha ao assar uma textura transferida da malha sem especificar uma textura
* [Explorer] “Salvar como” deve usar o nome do arquivo existente em vez do primeiro nome do recurso
* [Explorer] Comportamento incorreto ao arrastar e soltar um recurso de um pacote para outro
* [Explorer] Clicar com o botão direito do mouse não deve abrir os dados nas propriedades
* [Explorer] O ícone dos itens da Cena não tem o plano de fundo correto
* [Graph] Ctrl + D não funciona no Linux
* [Graph] A função de revinculação múltipla às vezes conecta apenas um link
* [Graph] Ctrl+Shift+D deve remover apenas links externos, não links internos
* [Gráfico] O vínculo entre tons de cinza e cores não está correto
* [3D View] Não é possível definir um recurso como um mapa de ambiente
* [Exibição 3D] O sombreador de informações da malha não exibe os resultados no espaço de cores certo
* [Parâmetros] Os parâmetros não expostas ainda podem ser expostos usando CTRL+P
* [Parâmetros] Os campos de texto não são atualizados corretamente ao desfazer/refazer
* [Content] Artefatos no Mapa de Desgastes 003
* [Conteúdo] A entrada principal da escala de cinza de metamorfose de vetor parece incorreta
* [Cooker] O subscooker gera um erro quando um recurso está ausente
* [Cozinhar] Falha com estouro de pilha quando a cadeia de nós é muito longa
* [UI] O botão “Sair” no gerenciamento de licenças não funciona

## Versão 7

### 7.2.5 (2017.2.5)

*(Lançado em: 19 de fevereiro de 2018)*

**Adicionado:**

* [Content] Erros de digitação em function.sbs
* [Content] Reduzir o intervalo padrão de ruído perlin e ruído gaussiano
* [3D View] Ajustar intervalo padrão para o parâmetro “Height Scale”
* [AXF] Atualizar modelos mdl

**Corrigido:**

* [Exibição 3D]&#x200B;[Padeiros] Os valores normais não são recalculados se o modelo não tiver normais
* [Graph] O recurso de bitmap não quadrado fica vazio depois de instanciado
* [Content] O ruído de perlin fornece resultados diferentes entre a CPU e o mecanismo de GPU

### 7.2.4 (2017.2.4)

*(Lançado em: 08 de fevereiro de 2018)*

**Adicionado:**

* [Importação AXF] Permite especificar o modo de filtragem em bitmaps de entrada
* [Visualização 2D] Não altere a proporção da imagem na visualização 2D quando o tamanho físico estiver ativado

**Corrigido:**

* [Library] falha ao ativar/desativar caminho nas preferências
* [Baker] Corresponder pelo nome ignorar algumas malhas com nomes específicos
* [Conteúdo] O filtro Premult to Straight remove o canal alfa

### 7.2.3 (2017.2.3)

*(Lançado em: 19 de janeiro de 2018)*

**Corrigido:**

* Erro de digitação [Content] no nó “PBR Basecolor Validate”
* O parâmetro de desordem [Content] está danificado no Células 2
* [Conteúdo] O Células 3 é invertido ao usar valores específicos em parâmetros
* [Conteúdo] Polígono 2: Artefatos visuais com configurações específicas
* [Content] A escala de cinza Tile Generator está em 8 bits por padrão
* [Content] Classificador de blocos: o parâmetro aleatório específico do padrão não funciona
* [Content] Mapeador de formas: funções aleatórias não podem ser usadas para direcionar Quantidade de padrão, Raio, Largura... etc
* [Content] Polygon 2: funções aleatórias não podem ser usadas para determinar a quantidade de lados
* [Content] Alguns ruídos/geradores de padrão geram avisos no console
* [Content] Non-Square-Transform-Grayscale gera um tamanho de pixel incorreto
* O filtro Redemoinho [Conteúdo] não leva em conta o modo de divisão em blocos gráficos
* [Gráfico] Arrastar e soltar o recurso de bitmap no nó de Entrada da imagem não funciona mais
* [Gráfico] CTRL+R (recarregar) não funciona mais
* [Graph] Problema ao usar um quadro em outro quadro
* [Gráfico] Falha ao mover quadros que contêm pinos
* [Graph] A instância “Shape (Legacy)” é transformada em “Shape” ao salvar
* [Baker] falha ao usar sem energia de 2 imagens
* [Padeiros] Cor da malha: Poligrupo, ID de submalha sempre retorna uma imagem preta
* [Bakers] AO da malha: A distância do oclusor é fixada em 1, independentemente do valor de entrada
* [Iray] Falha ao mudar para Iray
* [Iray] O valor de divisão em blocos gráficos deve afetar a intensidade de heighScale
* [Iray] Falha ao carregar IRay em um computador Windows em que VCCOMP110.dll não estava presente
* [3D View]&#x200B;[Bakers] UVs não podem ser decodificados do obj exportado de Modo
* [Visualização 3D] As intensidades do Deslocamento não são consistentes entre Opengl e Iray
* [Visualização 3D] A intensidade de Oclusão de Deslocamento/paralaxe é duas vezes a intensidade que deveria ser
* [Visualização 2D] deslocamento ao exibir imagem alfa
* [Cooker] Parâmetro constante ($tiling) não encontrado quando usado dentro de uma instância de gráfico
* [Cooker] Avaliação incorreta de variável em instâncias encadeadas
* [Parâmetros] O caminho do recurso Bitmap PKG não deve ser editável
* [Parâmetros] Os parâmetros em um mesmo grupo são invisíveis se apenas um parâmetro tiver visibilidade igual a false
* [PSD] Não é possível importar/vincular um arquivo de PSD de uma pasta nomeada com caracteres especiais
* [Functions] Parâmetros em funções não devem ter uma opção de visibilidade
* [LicenseService] Exceção acionada ao obter informações sobre nós
* [UI] Selecionar o texto no campo de descrição o mantém destacado

### 7.2.2 (2017.2.2)

*(Lançado: 23 de novembro de 2017)*

**Corrigido:**

* [Conteúdo] Erros de digitação em “Direcional ...” nós
* [Conteúdo] Vários erros de digitação
* [Content] O Tile Sampler está definido como “32 bits absolutos”
* [Conteúdo] Mapeador de formas: artefatos visíveis na borda da forma em alguns casos
* Os parâmetros “Expansão não quadrada” e “divisão em blocos gráficos” do Polígono 1 estão quebrados
* [Content] “Distribuição aleatória” e “Expansão não quadrada” não funcionam no Ruído anisotrópico
* [Content] Instância “Shape” quebrada em alguns mapas de Desgaste
* [Exibição 3D] A escala UV não será aplicada se a escala de height for 0
* [Exibição 3D] O reflexo com o ícone de sombreador não funciona mais
* [2D View] A janela de informações está com o layout quebrado
* [Graph] problema ao controlar o tamanho da saída com a função em um bitmap vinculado em um gráfico
* [Função] O gráfico não é invalidado quando um link é excluído
* [Biblioteca] Favoritos não funcionam
* [Exportação de PSD] o conteúdo do arquivo de PSD muda sempre que uma exportação é feita
* [Gradiente] Falha ao manipular teclas no editor de gradiente
* [Modelos] O mapa de posição para modelos Substance Painter está incorreto
* [AxF] height físico incorreto
* [MDL] O dimensionamento de UVW a partir do tamanho físico é invertido nos nós MDL SBS
* [Padeiros] $custom não funciona mais
* [Preferências] falha ao iniciar no Mac

### 7.2.1 (2017.2.1)

*(Lançado: 20 de outubro de 2017)*

**Corrigido:**

* [Engine] Falha ao renderizar texto com o mecanismo de GPU
* [Content] Tile Sampler: a ID da linha/coluna não funciona corretamente com quadrados
* [Content] Tile Sampler Color: a parametrização de cor está incorreta
* [Content] Tile Sampler: valor padrão incorreto para a quantidade de padrão X / Y
* [Export] Os metadados dos PSD exportados estão ausentes

### 7.2.0 (2017.2.0)

*(Lançado em: 19 de outubro de 2017)*

**Adicionado:**

* [Conteúdo] Adição de preenchimento de inundação e filtros associados (converter uma máscara em preto e branco em gradientes, cores aleatórias etc.)
* [Conteúdo] Adicionar novos ruídos, mapas de Desgaste e geradores de padrão compatíveis com o formato não quadrado (a versão antiga é marcada como “Legado”)
* [Content] Adicionado novo Splatter Circular com muito mais recursos
* [Conteúdo] Adicionar novo gerador de Scratches
* [Conteúdo] Adicionar filtro Redemoinho
* [Conteúdo] Adicionar seleção de histograma
* [Conteúdo] Adicionar padrão de estrela
* [Conteúdo] Adicionar filtro Mapeador de formas
* [Conteúdo] Adicionar filtro de Morph de vetor
* [Conteúdo] Adicionar gradiente linear 3
* [Conteúdo] Mosaico aleatório / Tile Generator: adicionar modo de simetria (h+v, h, v)
* [Content] Tile Generator: adicionar várias entradas de imagem
* [Content] Renomear “RGB-A Merge” para “Alpha Merge”
* [2D View] exibição da saída do nó do switch usando a tecla C
* [2D View] Otimize Histograma / layout de informações dependendo de sua taxa de exibição
* [2D View] Adicionar um botão para ativar/desativar a exibição lado a lado
* [3DView] Otimizar a velocidade de computação de harmônicos esféricos
* [Exibição 3D] Atualizar sombreadores PBR para usar amostragem Fibonacci em vez de Hammersley
* [Visualização 3D] Adicione uma opção para salvar o estado atual da cena como padrão
* [3D View]&#x200B;[Bakers] Serializar dados em formato legível
* [Padeiros] Adicionar predefinições, exportação/importação (json)
* [Publish] Criar o arquivo sbsar como não sólido
* [Publish] Armazene a imagem/miniatura do gráfico na sbsar
* [Publish] Exibir uma barra de progresso quando um pacote estiver sendo publicado
* [Dependências] Exibe o arquivo .sbs solicitando uma dependência na “Janela de dependência ausente”
* [Dependências] Janela Relatório: exibe um ícone verde quando o problema for resolvido
* [Dependências] Adicione uma opção para abrir as dependências personalizadas do pacote no explorador de pacotes
* [Preferências] Adicione uma opção para definir o estado de cena padrão nas configurações do projeto
* [Preferências] Adicione uma opção para ativar/desativar o caminho para a biblioteca
* [Gráfico] Adicione uma opção para fazer uma captura de tela (em escala 1:1) do gráfico
* [Gráfico] Remover dica de ferramenta do plano de fundo dos gráficos de composição
* [Script] Retornos de chamada Add onBeforeFileLoaded e onAfterFileLoaded
* [Engine] Adicionar um Parâmetro Base para ajustar o modo Proporção de Pixel
* [Console] Aprimorar o desempenho do console
* [Parâmetros] Novo widget Posição (XY)
* [Iray] Atualizar para o IRay SDK 2017.1
* [PSD] Salvar estado do widget PSD como texto em vez de binário
* [Biblioteca] Usar miniaturas do sbsar se houver
* [Explorer] Renomear “Dependências...” entrada para “Gerenciador de Dependências”
* Importação de arquivos AXF

**Corrigido:**

* [MDL] Falha ao exportar o Módulo MDL se a textura estiver conectada a um parâmetro exposto
* [MDL] Tentar registrar dependência para variáveis de cadeia de caracteres MDL (nó de constante)
* [MDL] falha após fechar o pacote
* [MDL] falha ao conectar um flutuante 3 a um nó de cor
* [MDL] não pode abrir a biblioteca de nós ao liberar um nó de link em um quadro
* [MDL] falha ao usar uma textura de arquivo
* [MDL] O comportamento de dependência registra muitos operandos
* [Gráfico] Os nomes de conectores são desativados após a edição do FX-Map
* [Graph] falha ao desfazer
* [Graph] Comportamento estranho com links entre nós
* [Gráfico] dispersão e desanexação de nós recolhidos ao desfazer
* [Graph] As instâncias de função não são atualizadas quando a referência é alterada
* [Controle de Versão] O pacote é recarregado quando uma ação personalizada de Controle de Versão é acionada
* [Controle de versão] Os espaços de trabalho de controle de versão desabilitados ainda estão disponíveis no menu de contexto de um pacote
* [Controle de versão] Remover ação personalizada não a remove do menu contextual de um pacote
* [Propriedades] A visualização do parâmetro não é atualizada ao usar o cursor
* [Iray] Problema de exibição de tempo máximo
* [Iray] Problema na opção de pausa
* [Bakers] falha ao converter UV para SVG usando tradução para coreano/japonês
* [Padarias] mudar o caminho após a primeira cozedura não funciona
* Problema para desfazer [PSD Exporter]
* [PSD] A pasta e as camadas estão bloqueadas no Photoshop CS5
* O cursor de cor [UI] é sempre definido como branco quando um nó de cor uniforme é criado
* [IU] Abrir uma guia existente deve exibi-la em vez de duplicá-la.
* [Predefinições] falha ao alterar o tipo de parâmetro usado em uma predefinição
* [Visualização 3D] os classificadores com o mesmo uso são mesclados
* [2D View] As informações de pixels não funcionam para imagens cuja resolução não é uma potência de 2
* Problema [Library] ao renomear filtros
* [Dados] Corrigir vários erros de digitação em arquivos SBS
* Nó de nível [Parameters] - problema de precisão de nível automático
* [Preferências] Os botões de diretórios de modelos devem ser desativados para “Projeto padrão”

### 7.1.4 (2017.1.4)

*(Lançado em: 2 de outubro de 2017)*

**Adicionado:**

* [Padeiros] Adicione a curvatura da malha de volta
* [Novo verificador de versão] Adicione uma opção de linha de comando para desabilitar a verificação de nova versão (—news hide\_changelog:true)
* [Scripting] Desativar tempo limite do Qprocess

**Corrigido:**

* [Padeiros] não podem alterar a cor do material de UV para SVG
* [UI] não pode fechar a visualização do gráfico usando o clique do botão de rolagem
* [Conteúdo] Alguns ruídos estão em 8 bits em vez de 16 bits
* [Conteúdo] A Suavização da curvatura dá um resultado errado quando a divisão em blocos gráficos está desativada
* [Text] falha ao redimensionar fontes específicas

### 7.1.3 (2017.1.3)

*(Lançado em: 31 de agosto de 2017)*

**Corrigido:**

* [Exibição 3D] falha ao tentar exibir opções de exibição 3D no Mac 10.10.5
* [Visualização 3D] As informações de texto não são exibidas na visualização 3D ao usar a tela Alto dpi
* [3D View] A preferência global por OpenGL/DirectX não é levada em consideração quando o material é redefinido
* [Conteúdo] Height ao normal: normal é invertido ao usar amostragem de Sobel
* [Content] A Oclusão ambiente (hbao\_2) não se comporta corretamente quando definida como não quadrada
* [Conteúdo] As entradas dos geradores de máscara não estão na mesma ordem que o “Combinador de dados de malha”
* [2D View] Histograma: as informações de seleção não são atualizadas na alteração da imagem
* [Visualização 2D] Histograma: as informações de intervalo usadas não são exibidas para imagens em tons de cinza
* [Predefinições] falha ao renomear uma predefinição de um gráfico usado em outro gráfico
* [Gráfico] Os eixos X e Y são invertidos na barra de ferramentas Tamanho principal

### 7.1.2 (2017.1.2)

*(Lançado em: 3 de agosto de 2017)*

**Corrigido:**

* [Conteúdo] Problema de filtragem nos filtros “Bloco automático inteligente” e “Escala de cinza”
* [Conteúdo] Os filtros da biblioteca não levam em consideração a preferência OpenGL/DirectX
* [Content] Não é possível cozinhar SBSAR com non\_square\_transform
* [Content] Forma de panorama: ponto ativo espelhado no canal RGB
* [Content] Tile Sampler: parametrização da cor da posição não normalizada
* [Content] Tile Sampler: os padrões ficam invisíveis se a divisão em blocos gráficos estiver desativada
* [Graph] A opção $normal\_map\_format não funciona quando usamos o menu da barra de espaços/biblioteca
* [Graph] Formato incorreto no nó do bitmap ao arrastar e soltar um recurso RGBxxF
* [Padarias] A cor da malha com cor do material está quebrada
* [Exibição 3D] todas as alterações na exibição 3D geram ações na pilha de desfazer
* [Dependências] falha quando um gráfico tem recursos ausentes na biblioteca personalizada
* [Iray] falha ao iniciar na versão OSX é anterior à 10.11

### 7.1.1 (2017.1.1)

*(Lançado: 18 de julho de 2017)*

**Adicionado:**

* [Padeiros] Adicione uma ação “Redefinir” em campos de recursos
* [Padeiros] Usar preto quando nenhuma cor de vértice for encontrada
* [Predefinições] Oculta o widget predefinido em ocorrências em que nenhuma predefinição está disponível
* [Preferências] Remova a opção “Calcular binormal por fragmento” nas configurações do projeto (agora esta opção é manipulada no plug-in de quadro tangente)
* ajustes de sbsupater.exe

**Corrigido:**

* [Padeiros] O sistema de “erro” não funciona mais
* Serialização de opções [Padeiros]: teclas antigas permanecem
* [Padeiros] falha ao alterar o nome de um padeiro
* [Padeiros] Falhas na interface do usuário
* Filtro de Correspondência de Cores [Conteúdo] - diferença entre CPU/GPU
* [Content] Alguns GrungeMaps geram imagens de 8 bits em vez de 16 bits
* [Graph] Falha ao usar o X “alternar links” no nó fx-map
* [Exibição 3D] Falha aleatória ao abrir a Exibição 3D
* [3D View] Binormal são sempre computados por fragmento, não importa o plugin de espaço tangente
* [Updater] Erro de XML ao usar fonte específica
* [Fogão] módulo em número negativo não retorna o mesmo resultado que o mecanismo
* [UI] problema de interface ao usar o gradiente de seleção na tela de DPI alto
* [MDL] O nó de cor não mantém este valor
* [Packaging] O plug-in de espaço tangente Mikkt Unreal está ausente

### 7.1.0 (2017.1.0)

*(Lançado: 29 de junho de 2017)*

**Adicionado:**

* [Bakers] Nova interface do usuário
* [Padeiros] Mantenha um cache em malha de alta definição até fechar a janela do padeiro
* [Padeiros] Adicione uma opção para corrigir a deformação de inclinação usando uma máscara em tons de cinza
* [Padeiros] Suporte use-high-poly-as-low-poly em padarias de malha
* [Padarias] Tornar a janela Padarias não modal
* [Padeiros] Armazenar estado em arquivo .sbs em formato legível
* [Parâmetros] Copiar/colar parâmetros de um gráfico para outro
* [Parâmetros] Adicione uma opção para copiar um único Parâmetro de entrada (e colá-lo depois)
* [Parâmetros] Remove o botão de função no parâmetro “Modo de cores”
* [Parâmetros] Editar/Salvar/Exibir predefinições de parâmetro incorporadas
* [Parâmetros] Permite que o usuário copie atributos de parâmetros quando um pacote estiver bloqueado
* [Exibição 3D] Não armazena mais as configurações de exibição 3D da última sessão no registro
* [Visualização 3D] Criar novo recurso 3D da cena atual
* [Exibição 3D] Não armazena mais o estado de exibição 3D de uma sessão para outra no registro
* [Exibição 3D] Mesclar os menus “Cena” e “Geometria”
* [3D View] Separe a conversão em sRGB do sombreador de fragmentos (você precisará atualizar seus sombreadores personalizados!)
* [Exibição 3D] Adicione uma opção para criar um novo recurso 3D do estado atual
* [Exibição 3D] Melhorar a mensagem de erro gerada quando #include falha em um código de sombreador
* [Visualização 3D]&#x200B;[Explorer] Criar cena 3D a partir de elementos primitivos
* [3D View] Exibe o número de linha correto quando a compilação do sombreador GLSL falha e o código contém diretivas #include
* [Gráfico] Pode redimensionar um quadro de todos os cantos/bordas
* [Graph] Armazena as informações de Tamanho Pai no recurso de gráfico em vez do registro local
* [Gráfico] otimizar a velocidade de geração de miniaturas de nós
* [Graph] Exponha o orçamento do cache de memória em Preferências
* [Graph] Adicionar uma opção “Redefinir e exibir na visualização 3D” nos nós
* [Content] PBR Converter: adicionar novos Arnold 4/5, Corona 1.6 e Predefinições de renderman
* [Conteúdo] Otimizar o nó AutoLevel e oferecer suporte à entrada HDR
* [Content] Otimizar o filtro HBAO quando a Otimização de GPU estiver desativada, adicione a versão de 16 amostras
* [Cooker] recurso de SVG de saída não suportado para o registro
* [Cooker] Não descartar todos os recursos do SVG se apenas um recurso não for suportado
* [UI] Aumentar o tamanho do bloco da Descrição
* [UI] Adicionar informações de caminho de arquivo em instâncias de gráfico
* [Functions] Adicionar “referência aberta” em instâncias de função
* [Funções] Exibe a lista de gráficos de função ao arrastar e soltar .sbs em um gráfico de função
* [Explorer] Criar novo recurso 3D a partir de fontes
* [Engine] Adicionar variável $tiling
* [Curva] Adicionar opções para inverter horizontalmente/verticalmente a curva
* [Gerenciamento de cores] Ler perfil ICC em bitmaps
* [Export] Adicionar “Rótulo”, “Grupo” e “Dados do usuário” na lista de macros Padrão
* [Preferências] adicione a possibilidade de alterar o caminho para arquivos temporários
* [Doc] Adicionar o formato de gráfico MDL à documentação do formato SBS

**Corrigido:**

* [Graph] Problema de cache: exibir saídas em uma visualização 3D não funciona mais
* [Gráfico] Limpar problema de cache
* [Graph] As solicitações de geração de miniaturas de nós não são canceladas quando o gráfico é invalidado
* [Graph] Problemas de resolução após usar F5
* Exibição de gráfico [Graph] ausente na inicialização
* [Gráfico] A modificação de um parâmetro gera várias chamadas de renderização
* [Graph] falha ao usar o modelo personalizado que contém mapas baked
* [Graph] Falha quando nós vinculados em uma função de gráfico
* [3D View] Bagunça de carregamento paralelo com ProgressManager
* [Exibição 3D] A renderização com iray em uma imagem de resolução personalizada não está completa
* [3D View]&#x200B;[Iray] A definição do material não é mantida
* [2D View] O histograma está vazio em imagens LDR
* [2D View] Problema de exibição quando o modo de divisão em blocos gráficos está ativado
* Parâmetros [MDL] não expostos
* [MDL] falha ao mover um MDL de um pacote para outro durante a renderização
* [MDL] Não perguntar onde atribuir o MDL ao clicar duas vezes no gráfico
* [Bakers] Falha ao assar um arquivo .obj específico
* [Padarias] A textura transferida da malha / normal dá um resultado errado
* [Transformação 2D] Não é possível usar as teclas de seta para alterar o deslocamento no nó de transformação 2D
* Problema de artefato [Transformação 2D] com baixa resolução
* [Atualizador] O relatório de atualização não aparece ao usar quando Ctrl+o/open
* [Propriedades]&#x200B;[Formato] Alguns caracteres têm escape duas vezes em UserTags
* [Nó de bitmap] Ctrl Z não funciona na exibição 2D
* [Preferência] Espaço vazio inútil na guia Aliases
* [Instalador] A instalação de uma versão anterior não funciona na primeira vez
* [Parâmetros] lista suspensa: colocar alguns espaços no último valor rótulo congela SD indefinidamente
* [UI]&#x200B;[MAC] “about Substance” exibe informações de Iray
* [SVG] falha ao importar um SVG específico
* [Content] Filtro HBAO: o parâmetro Radius se comporta de forma diferente em função da resolução (um novo hbao\_2.sbs foi adicionado, o antigo hbao.sbs foi descontinuado)

## Versão 6

### 6.0.4

*(Lançado: 21 de junho de 2017)*

**Corrigido:**

* [Gráfico] falha ao usar o atalho X
* [Gráfico] falha após excluir um link entre nós
* [Gráfico] Excluir um ponto de divisão causa falha no SD
* [Content] Erro de digitação em mg\_surface\_brush
* [Conteúdo] Menor qualidade em HBAO em comparação com 6.0.2
* [Biblioteca] Os ícones do filtro personalizado não são salvos
* [Explorer] Falha ao abrir um recurso 3D referenciando um arquivo ausente
* [Padeiros] Transferir textura da malha é espelhado se a opção “Normal” estiver ativada

### 6.0.3

*(Lançado em: 01 de junho de 2017)*

**Adicionado:**

* [Exportar] Salvar tamanho físico como dpi nas texturas exportadas
* [Exibição 2D] Exibe o rótulo do parâmetro da matriz no menu Transformação

**Corrigido:**

* [Content] Tile Sampler: parametrização da cor da posição não normalizada
* [Conteúdo] Corte: gráfico fantasma em processador de pixels
* [Content] Forma de panorama: ponto ativo espelhado no canal RGB
* [Content] O filtro HBAO pode gerar resolução negativa
* O filtro Correspondência de cores [Conteúdo] é renderizado incorretamente em algumas situações
* [Conteúdo] “Pré-multiplicado para reto” remove o canal alfa
* [Conteúdo] Erros de digitação em vários rótulos
* [Gráfico] As informações de Profundidade de bits são cortadas quando o dimensionamento de DPI é definido como 125.1520 ou 175%
* [Gráfico] Quando uma seleção contendo um quadro é colada, o quadro não é selecionado
* [Gráfico] Quando uma seleção contém um comentário, os elementos colados serão deslocados no gráfico
* [Gráfico] problema com pontos de divisão
* [Gráfico] Alguns conectores de pino não se encaixam quando o mouse é passado
* Exibição de gráfico [Graph] ausente na inicialização
* [Exportar] bitmaps ausentes após a exportação
* [Exportar] Não exporta as dependências na versão a vapor
* [Padarias] falha com malha que tem muitos conjuntos UV
* [Padarias] Falha do padeiro do mapa UV ao assar malhas sem conjuntos UV
* [Engine] Erro do Sampler com Fxmap+HDR
* Falha do [Engine] com imagens jpeg de alta resolução
* [2D View] O widget de transformação fica ausente na exibição 2D quando o modo de visualização lado a lado está ativado
* [Exibição 3D] A instância do gráfico com uso personalizado não é enviada corretamente para a Exibição 3D
* [Preferências] Caminho incorreto para mikktspace.dll
* [Explorer] mover um recurso de bitmap em um pacote faz com que o menu “link/embed” apareça
* [Parameters] falha ao usar &#39;tiling&#39; como nome de parâmetro
* [MDL] nenhum vínculo colorido entre nós
* [Vinculador] Processador de pixels: geração incorreta de sombreadores GLSL
* [Cooker] Problema de Profundidade de bits

### 6.0.2

*(Lançado: 17 de março de 2017)*

**Adicionado:**

* [Engine] Integrar o mecanismo mais recente com otimização de descompactação jpeg

**Corrigido:**

* [Conteúdo] O patch de clone não está mais funcionando
* A saída do Height [Content] não faz parte do grupo de materiais nos modelos
* [MDL] Falha ao excluir uma instância do gráfico
* [MDL] Nenhum aviso entre nós conflitantes
* [MDL] Mensagens de aviso inúteis ao exportar
* [Curva] A exposição do parâmetro de endereçamento não deve ser exposta
* [Engine] Falha ao importar um sbsar que contém um bitmap HDR
* [Nó de texto] A especificação de fonte gera um arquivo XML inválido
* [Editor de gradiente] Os valores não estão fixados corretamente
* [Exibição 3D] Falha ao usar um HDRi personalizado (alta resolução) como ambiente

### 6.0.1

*(Lançado em: 3 de março de 2017)*

**Adicionado:**

* [Padeiros] Melhorar o gerenciamento de tarefas de progresso
* [Padeiros] Alterar a dica de ferramenta de erro quando nenhuma malha estiver selecionada
* [Propriedades] Os parâmetros de pós-efeito 3DView devem ser desativados quando “Pós-processo” estiver desativado em Preferências
* [License] Permitir a especificação de um caminho personalizado para a licença Substance Designer 6
* [Gradiente] Desative o controle deslizante “precisão” se nenhuma separação de gradiente tiver sido feita
* [Fogão] Ignorar recurso ausente na entrada da imagem para evitar falha de cozimento
* [Visualização 3D] Alterar o manuseio de vazamentos de reflexos de specular
* [Graph] Adicionar mais parâmetros para a compatibilidade do mecanismo v6

**Corrigido:**

* [Padeiros] O mapa normal da malha (espaço global) é invertido no eixo Y
* [Padeiros] Cozimento de uma malha sem UV não relata erro
* [Padeiros] A média normal não funciona
* [Bakers] SD falha ao assar AO com uma malha específica
* [Padeiros] O formato de saída não é restaurado corretamente
* A fonte personalizada [Texto] não funciona no player
* [Texto] aviso de fonte inválido ao reabrir um pacote com fonte em recursos
* A entrada de texto [Texto] não funciona no modo de visualização
* O parâmetro de fonte [Text] pode ser exposto
* [Text] congela/falha ao criar uma função no parâmetro text
* [Text] Falha ao expor o tamanho da fonte
* [2D View] A porcentagem de zoom não é exibida corretamente ao usar a tecla “F”
* [2D View] A imagem é deslocada quando o tamanho é alterado
* [Exibição 2D] Descontinuidade ao exibir a divisão em blocos gráficos
* [Exibição 2D] O guizmo de transformação não é visível/editável no modo de visualização
* [Visualização 3D] Tamanho físico não considerado pelo sombreador PBR Parralax
* [Exibição 3D] A configuração da taxa de atualização não é restaurada corretamente de uma sessão para outra
* [Graph] multiangle\_to\_normal prevent publishing
* [Graph] O tamanho de saída do filtro pow está bloqueado
* [Graph]Não é possível criar uma instância de arquivos .sbsar
* [Curva] IU cortada
* [Curva] A exibição de números está ligeiramente cortada
* [Curva] O widget desaparece quando a barra de ferramentas é redimensionada
* O nó do brilho [Content] está danificado
* [Content] Tile Sampler: os padrões ficam invisíveis se a divisão em blocos gráficos estiver desativada
* [Content] MG Mask Builder - Parâmetros de contraste de curvatura invertidos
* [Content] Color Equalizer: parâmetros do grupo personalizado\_color\_variation não conectados
* [Conteúdo] Correção de clone: área da correção não visível quando posicionada em cantos
* [Explorer] Recarregar um pacote enquanto sua dependência é aberta interrompe o pacote de dependência
* [Explorer] Não é possível importar um recurso psd de 32 bits
* [Publish] falha de cozimento (herança ERR:No (absoluta))
* [Gradiente] O gradiente deve ser exibido como linear quando sRGB está desmarcado
* [Transformation2D] Impressão de deslocamento ao mover um guizmo com restrição de eixo
* [Parâmetros] O foco do mouse é roubado pelo menu suspenso
* [Engine] Nenhuma divisão em blocos gráficos não tem efeito no nó de distância no mecanismo da GPU
* [Exportar] Falha ao exportar saídas como TGA
* [MDL] a predefinição de exportação não funciona

### 6.0.0

*(Lançado em: 14 de fevereiro de 2017)*

<b>Adicionado:</b>

* [Engine] Novo nó de curva
* [Engine] Novo nó de texto
* Composição de profundidade de bits do [Engine] 16f/32f
* [Engine] criação de instâncias para mapas FX de GPU
* [Engine] Adicionar função log2
* [Padarias] assar mapa 8k
* [Padarias] Cozido por material / “Conjunto de textura”
* [Bakers] Exibe mensagem de carregamento quando a saída de bitmap está sendo codificada/gravada no disco
* [Padeiros] Adicione uma opção de cancelamento durante a cozedura
* [Nó de gradiente] adiciona ajustes globais para várias chaves selecionadas
* [Nó Gradiente] Simplificar opções do Seletor de gradiente
* [Gráfico] Adicionar uma opção para modificar o tamanho padrão da página principal
* [Graph] Exibir profundidade de pixels da imagem sob o nó
* [Preferências] Preferências globais para DirectX/OpenGL
* [Preferências] Use guias em Preferências/Interface do usuário do projeto
* [Preferências] remova o parâmetro MaxTextureSize localizado nas preferências “3DView”
* [Preferências] Exibe uma ajuda curta sobre o salvamento automático
* [Preferências] Expor opções de formato de imagem
* [Preferências] Adicione uma opção para ocultar o Mapa de ambiente na Visualização 3D por padrão
* [Preferências] Adicione uma opção para a opção alfa padrão de filtro de mapa normal
* [Exibição 2D] Adicione a possibilidade de deslocar para longe dos limites da textura
* [Visualização 2D] Interpretar a proporção X/Y do tamanho físico
* [Visualização 3D] Melhorar o gerenciamento de texturas
* [Exibição 3D] Desativar pós-efeitos por padrão (para evitar falhas na gpu lowend)
* [MDL Graph] Gerenciar o sinalizador oculto no parâmetro IRay
* [MDL Graph] Permite definir o construtor &#39;material()&#39; como Nó Raiz
* [Gráfico MDL] Visualização do nó Criar instância do Gráfico SBS
* [Conteúdo] Adicionar novos filtros de Processamento de Digitalização
* [Conteúdo] Adicionar novos filtros de ajuste (Suporte, Potência, Visualizador de intervalo HDR)
* [Content] Adicionar ruído azul (aproximação rápida)
* [Conteúdo] Adicionar novos efeitos de Forma (Brilho, Sombra, Traçado)
* [Publish] Adicione uma ação “Exportar como anterior” para republicar o último pacote selecionado
* [Publish] Melhorar a geração de SBSAR ao usar bitmaps de alta resolução
* [Publish] Avisa o usuário sobre a configuração de gráfico não “relativa ao pai x1” ao publicar ou carregar em Compartilhar
* [Propriedades] Adicionar atributo “Tamanho físico” em gráficos SBS
* [Parâmetros] Remove ações de função em caminhos de Recurso PKG
* [Parâmetros] Remover pop-up “Valores de visualização alterados”

<b>Corrigido:</b>

* [Gráfico] O uso de memória cresce regularmente sempre que o menu do botão direito do mouse é aberto
* [Graph] [In SSE2] Os nós do polígono não exibem formas quando o parâmetro “Scale” está em negativo
* [Graph] Falha ao alternar de “Inteiro” para “Flutuante” em um parâmetro exposto
* [Gráfico] Mover os nós enquanto um ponto de divisão é selecionado recalculará os nós
* [Graph] Os pontos de divisão não suportam “Desfazer”
* [Gráfico] dica de ferramenta vazia exibida quando a descrição do gráfico contém caracteres não imprimíveis
* [Gráfico MDL] Falha quando o nó atual exibido na exibição de propriedades é excluído
* [Gráfico MDL] O Gráfico MDL que usa a função de construtor material() como raiz não é renderizado corretamente na Visualização 3D
* [MDL] Não é possível exportar o módulo MDL ao usar o operador condicional com o parâmetro de exposição booliano uniforme
* [MDL] Falha ao Carregar um Modelo de Gráfico MDL duas vezes
* [Arquivo MDL] Os materiais que estão usando uma textura não são gerenciados corretamente
* [3D View] O material IRay não é alterado quando o nó raiz do MDLGraph é alterado
* [Exibição 3D] falha aleatória ao fechar a Exibição 3D enquanto uma carga de malha está em andamento
* [Exibição 3D] O Yebis não é reativado após salvar a renderização
* [Visualização 3D] Arquivo PSD inválido gerado ao salvar o resultado de renderização da cena do iray
* [Visualização 3D] o ponto luminoso 1 não se ilumina
* [UI] A área de detecção das Caixas de seleção é muito ampla nos parâmetros “Padarias de malha”
* [UI] Problema estético em “Padarias de malha” Parâmetros
* [Mac] Abrir o SD clicando duas vezes em um sbs não envia a saída para a exibição 3d
* [Mac] [Iray] A renderização do cluster fotoreal não funciona no MacOS
* [Engine] Atan2(0, 0) faz o mecanismo travar
* [Engine] Problema crítico de sincronização
* [Padeiros] Não é possível desativar a normalização automática para o Height
* [Parâmetros] ao converter tons de cinza em rgba, alfa deve ser 255
* [Functions] É possível definir uma função como o nó de saída mesmo se não for compatível
* [Export] Dependências inválidas após exportar um pacote com recursos PSD
* [Console] Limpar o console faz com que o SD falhe

## Versão 5

### 5.6.2

*(Lançado em: 08 de fevereiro de 2017)*

**Corrigido:**

* [Preferências] O sombreador padrão não é levado em consideração
* [Visualização 3D] Falha se o sombreador padrão for alterado no tempo de execução
* Problema ao obter $size no [Engine]

### 5.6.1

*(Lançado: 17 de janeiro de 2017)*

**Adicionado:**

* [Exibição 3D] Definir tamanho de primitivas como 100 cm
* [Content] Adicionar “Filtragem de entrada de imagem” a “Splatter Circular” e “Splatter”
* [Bakers] “Curvatura da malha” Adicione avisos do console no canal “Mesh Sanity Check”

**Corrigido:**

* [Visualização 3D] Desaparece quando desencaixado
* [Gráfico] Os parâmetros “Ruído” e “Precisão” do mapa de degradê não funcionam mais
* [Visualização 3D] ALT+R não funciona após salvar a renderização
* [Bakers] Falha “Curvatura da malha” com algumas malhas ZBrush

### 5.6.0

*(Lançado: 15 de dezembro de 2016)*

**Adicionado:**

* [Content] Adicionado novo filtro “AO (Horizon Base Ambient Oclusão)”
* [Content] Adicionado novo filtro “Mistura de Height”
* [Content] Adicionado novo filtro “Height to Normal (world units)”
* [Content] Adicionado novo filtro “Mistura de Height de material”
* [Content] Adicionado novo filtro “Snow Cover”
* [Content] Adicionado novo filtro “Water Level”
* [Conteúdo] Adicionado novo filtro “Correspondência de cores”
* [Content] Adicionado novo filtro “Varredura de histograma (não uniforme)”
* [Preferências] [IU] Adicione uma opção em Preferências para desativar a detecção de High-DPI
* [Exibição 3d] Adicionar uma opção de “redefinir posição da câmera”
* [Iray] Integrar o IRay SDK 2016.2 para suporte à arquitetura Pascal
* [Graph] Adicionar a opção “Copiar informações do nó para a área de transferência” no menu contextual

**Corrigido:**

* [MDL] raiz do material de alinhamento não é removida na predefinição exportada
* [Gráfico MDL] links para recurso ausente não são excluídos no gráfico MDL
* [Biblioteca] A criação de um novo filtro cria duas condições básicas
* [Biblioteca] As pastas não filtram mais o conteúdo da biblioteca
* [Padeiros] A barra de progresso entra e sai
* [Padeiros] O recurso de gaiola não existente impede assar
* [Content] Vários erros em “Functions.sbs”
* [Exportar] O formato de arquivo é sempre redefinido para png
* [UI] Problema de dimensionamento da interface do Substance Designer
* [Graph] Falha ao mover o pacote original de uma instância do gráfico
* [Preferências] se o plug-in padrão shader/tangent/.. não for encontrado, use os definidos no projeto padrão
* [Parâmetros] Os controles deslizantes têm muita precisão no Mac
* [Explorer] Mover a malha 3D de uma pasta para outra corrompe este recurso
* Fechar a janela não elimina o processo SD
* A caixa de diálogo Abrir arquivo não exibe arquivos com o filtro “Todos os formatos”

### 5.5.3

*(Lançado: 28 de outubro de 2016)*

**Corrigido:**

* [Prateleira] Falha ao criar pasta
* [Padeiros] World\_Space\_Direction não funciona mais

### 5.5.2

*(Lançado: 18 de outubro de 2016)*

**Adicionado:**

* [Gráfico MDL] Propagar valores default do Gráfico SBS para a instância do Nó do Gráfico SBS no Gráfico MDL
* [MDL] Arrastar e soltar suporte do gráfico SBSAR
* [IRay] atualização para SDK 2016.1.6 (261500.16187)
* [sbsrender] Otimizar o gerenciamento de memória do sbsrender para corresponder às performances do reprodutor
* [Visualização 3D] Permite que o tamanho do widget seja menor que a barra de menu superior
* [Console] Permite copiar algumas linhas para a área de transferência

**Corrigido:**

* [Player] Falha ao reproduzir um pacote diretamente no Designer pelo “botão de reprodução”
* [Inicialização] A exibição pop-up não tem o arquivo nvcuvid.dll
* [Inicialização do ambiente] clicar duas vezes em um arquivo .sbs não o carrega no SD
* [Exportar] Falha na exportação com dependências
* [MDL] Problema de sincronização entre um gráfico e sua instância
* [MDL] os nós da instância sbsar estão gerando a textura\_return em vez dos valores
* [Exibição IRay 3D] No Renderizador Iray, o “Canal de Height” não é atualizado corretamente quando você altera o mapa de height
* [Exibição do IRay 3D desencaixada] “Câmera>Salvar renderização” não funciona depois de ocultar o aplicativo na barra de tarefas do Windows
* [Mac IRay] A GPU NVIDIA não é mais detectada pelo IRay
* [Bakers] Textura transferida de malha falha ao assar texturas não POT
* [Falha] Falha ao exportar um gráfico no Substance share
* [Graph] Falha ao selecionar uma instância fantasma
* [Exibição 3D] Não é possível aplicar mais zoom ou menos zoom à câmera ortográfica no modo Iray
* [UI] O Seletor de Cores não gerencia a exibição de Alto DPI
* [Graph] (MacOS 10.11.06) Cálculo infinito com nó de mistura multimaterial
* [Graph] Copiar/colar o conteúdo do gráfico ==> colar no conteúdo e também uma referência a esse gráfico
* [Gráfico] Várias misturas de vários materiais na cena, ele seleciona automaticamente as saídas erradas
* [Graph] Edge Wear de metal trava o PC
* [Library] Os arquivos “SBSAR” exibem o logotipo “S” em vez de miniaturas
* [Biblioteca] As pastas dentro de .sbsar são exibidas na biblioteca

### 5.5.1

*(Lançado em: 08 de setembro de 2016)*

**Adicionado:**

* [Iray] Adicionar modo “IQ” para renderização na nuvem
* [Iray] Atualização para o Iray SDK 2016.1.5

**Corrigido:**

* [MDL] A visualização na visualização 3D não funciona corretamente na primeira vez
* [MDL] gradiente\_interpolation\_linear não é exportado com o caminho completo
* [MDL] O canto inferior direito do quadro recém-criado está exatamente alinhado com o nó relacionado
* [MDL] A miniatura do material raiz não é atualizada em alguns casos
* [MDL] Falha ao excluir todos os nós e refazer
* [MDL] Desempenho lento na exibição do gráfico em comparação com o Gráfico do Substance
* [MDL] Não é possível exportar o módulo MDL devido ao parâmetro IOR
* [MDL] Os parâmetros exibidos não correspondem ao nó selecionado
* [Exibição 3D] O material MDL proveniente de um gráfico MDL não é redefinido quando o nó raiz é excluído
* [3D View] O enquadramento de câmera padrão é perdido após carregar a malha do fbx
* [Exibição 3D] A atribuição de textura não é mantida ao alternar para Iray
* [Iray] Mensagem de aviso do IRay ao mover a câmera
* [Iray] Falha ao alternar para Iray
* [Iray] A senha do VCA não foi salva
* [Graph] Falha ao excluir nós
* [Graph] Pressionar CTRL para copiar o link não funciona com o modo Material
* [Graph] Falha ao excluir nó de saída em um material de nó de instância
* [Padeiros]&#x200B;[Exibição 3D] Não é possível carregar a malha de alta definição
* [Mac]&#x200B;[Exibição 3D] Falha ao tentar restaurar janelas desconectadas em monitor secundário
* [Parâmetros] Não é possível editar um valor em um spinboxedit sem remover o sufixo
* [UI] Usar “Cancelar” ao fechar o SD deve interromper a caixa de mensagem
* Falha ao abrir duas Visualizações 3D
* Falha em Alg::Scripting::Engine ao usar muita condição VisibleIf
* Os arquivos são excluídos pelo salvamento automático se existir um arquivo .algautosave

### 5.5.0

*(Lançado: 25 de agosto de 2016)*

<b>Adicionado:</b>

* O Substance Designer já está disponível no Linux
* Novo Editor de MDL (Linguagem de Definição de Material)
* [Padarias] Nova curvatura do padeiro de malha
* [Biblioteca] Usar ícones de SVG em vez de arquivos de bitmap
* [Library] Adicionar uma opção para filtrar o resultado para MDL, Composição, Função e Fxmap
* [Graph] Estender a opção “Exibir nó recém-criado” para copiar/colar/duplicados
* [Novo documento] Criar um widget de seleção de modelo ao criar um novo gráfico MDL
* [Exibição 3D]&#x200B;[Iray] Exibir modo de renderização + nós VCA ao lado de iterações/tempo
* [Exibição 3D] Aprimorar o desempenho do menu “material” ao abrir
* [3DView]&#x200B;[Bakers] Atualização para o SDK FBX 2017
* [Exibição 3D] Adicione a capacidade de mostrar/ocultar informações de renderização (resolução, iterações etc.) no menu Exibir da Visualização 3D
* [Iray] Expor parâmetros de mosaico de volta à edição de cena
* [Projeto] Adicionar alias gerado automaticamente para o diretório de arquivos de projeto
* [Projeto] Especifique a textura do ambiente padrão nas configurações do projeto
* [Content] Adicionado novo estúdio HDRi
* [Conteúdo] Adicionar um nó de transformação não quadrado à biblioteca
* Inicie o SD com um arquivo .sbscfg específico

<b>Corrigido:</b>

* [Graph] As entradas não se conectam automaticamente a saídas com o mesmo uso.
* [Graph] As entradas de nó inseridas não estão conectadas corretamente
* [Gráfico] Desmarcar também deve selecionar um nó sob o mouse
* [Graph] A inserção de nó não se conecta a todos os links
* [Padeiros] Difusão incorreta em padeiro de curvatura
* [Bakers] “Textura transferida da malha” trava se a malha de alta definição não tiver UVs
* [UI] O ícone de função nos parâmetros não é modificado quando uma função é definida
* [UI] Dicas de ferramentas para parâmetros são cortadas
* [Visualização 3D] mais de 1.000 luzes são exibidas na cena
* [Visualização 3D] O sombreador Lambert da GLSL não gerencia a textura srgb corretamente
* [3D View] Parâmetros de revestimento ausentes ao conectar substâncias em Iray
* [Iray] A exportação predefinida de mdl não funciona quando os espaços no nome
* [Iray] Os parâmetros de subdivisão não são levados em conta
* [Parâmetros] O identificador de parâmetro não é mais exibido
* [Parameters] Falha ao alterar a URL do recurso de “From Resource...” ação
* [Parâmetros] Conversão incorreta de &amp; caracteres
* [Explorer] clicar duas vezes em um gráfico “grande” geralmente não abre na exibição do gráfico
* [Explorer] Os SVG incorporados são mostrados como ausentes no Explorer
* [Explorer] Falha ao renomear um item com o caractere “&amp;”
* [Content] A divisão em blocos gráficos do gradiente 1 está errada ao usar a rotação de 90°/180°
* [Perforce] A integração parece não funcionar se o espaço de trabalho estiver localizado na raiz do disco rígido
* [Dados] A UID gerada para os nós não é exclusiva
* [Preferences] A adição de um alias direcionado à raiz HDD bagunça os caminhos no sbsprj
* [VAZAMENTO DE MEMÓRIA] Alguns diálogos QD não são destruídos quando são fechados

### 5.4.0

*(Lançado: 29 de abril de 2016)*

**Adicionado:**

* Adicionar um link para a Substance Store
* [UI] Suporte para resoluções de alto DPI
* [IU] Permitir a reordenação de tabulações
* [Exibição 3D] Permitir a exportação da renderização para o ArtStation
* [Exibição 3D] Adicionar o sombreador padrão na lista de sombreadores
* [Gráfico] Exibe o nome do recurso sobre o nó de bitmap
* [Gráfico] Aprimorar a ordem de listagem do menu de pesquisa da barra de espaço
* [Padeiros] Novo padeiro “Posição da malha”
* [Bakers] Nova configuração de “mapa normal” para o padeiro Texture Transfert
* [Padeiros] Nova configuração “Tangent” &amp; “Binormal” para o padeiro normal do espaço mundial
* [Script] Permite executar scripts durante ações Salvar, Exportar e Publish
* [Dependências] Adicionar uma opção Recolher/Expandir com base na seleção
* Adicionado um aviso sobre conflitos de extensão do shell

**Corrigido:**

* Falha ao sair
* O processo Substance Designer ainda pode estar em execução após a saída
* [Iray] As saídas não são enviadas para materiais mdl ao alternar o renderizador
* [Conteúdo] Exemplo de mosaico: rotação de padrão aleatória não deve girar a forma

### 5.3.5

*(Lançado: 06 de abril de 2016)*

**Corrigido:**

* [2D View] A opção de menu Transformação 2D do clique com o botão direito está disponível em qualquer nó
* [2D View] gizmo de transformação 2d ainda editável após a exclusão do nó de transformação
* [3D View] O caminho do ambiente não deve ser exibido nos Parâmetros de ambiente
* [Exibição 3D] Os parâmetros de pós-efeitos não são salvos em recursos 3D
* [Visualização 3D] O menu da barra de ferramentas não se comporta como um menu regular
* [Preferências] Não é possível definir o “Limite de cache do mecanismo” superior a 4095
* [Preferências] A configuração de um sombreador padrão não é levada em consideração
* [Iray] Os parâmetros de cor não foram recuperados corretamente
* [Iray] As cores do material MDL são redefinidas
* [Iray] Os bitmaps não são exportados junto com a predefinição de MDL
* [IRay/Mac] Redimensionar a exibição 3D faz com que a estação de trabalho Mac trave
* [Graph] Falha ao exportar o documento PSD
* [Graph] Tamanho de nó exibido incorreto
* [Gráfico de funções] A imagem de entrada do nó de amostra não é editável se apenas uma imagem estiver conectada
* [Engine] Falha ao calcular o gráfico Fxmap
* [Engine OGL] Erro na geração do processador de pixels
* [Gradiente] O seletor de gradiente não funciona no mac
* [PSD] Imagem de 8 bits não convertida corretamente em 16 bits
* [Parâmetros] O widget de histograma de nível não tem o mesmo height em cor e escala de cinza
* [Console] Clicar em uma célula rola a exibição horizontalmente
* [Explorer] Os recursos 3D realocados não são abertos corretamente na exibição 3D

### 5.3.4

*(Lançado: 16 de janeiro de 2016)*

**Corrigido:**

* [Iray] tangente/binormal não foram corretamente levados em consideração
* [Explorer] O pacote está marcado como a ser salvo logo após ser aberto
* [Exibição 3D] O reflexo difuso do IBL é muito forte
* [Exibição 3D] Falha ao arrastar e soltar imagem de 8 bits do explorador para a exibição 3D
* O aplicativo trava desde 1º de janeiro de 2016

### 5.3.3

*(Lançado: 10 de novembro de 2015)*

**Adicionado:**

* [Content] Adicionar “White Noise Fast” (baseado em processador de pixel)
* [Content] Adicionar “Deslocamento global horizontal/vertical” em Amostradores de blocos

**Corrigido:**

* Falha ao criar um novo Substance em algumas situações
* [Padrões] Falha quando os mapas baked estão atualizando o gráfico
* [Bakers] OBJ vindo de zbrush deve usar filename para Corresponder por nome
* [Parâmetros] Falha ao fazer Desfazer/Refazer/Desfazer no gráfico de função
* [Gráfico] Os pontos de divisão não são colados no local correto

### 5.3.2

*(Lançado: 30 de outubro de 2015)*

**Adicionado:**

* [Conteúdo] Adicionar controle de filtragem para entrada de padrão em Tile Generator

**Corrigido:**

* [Exibição 3D] Ponto de foco não inicializado corretamente
* [Exibição 3D] Plano de clipe distante incorreto ao alternar várias vezes de recursos de malha 3D
* [Exibição 3D] Breve artefato de renderização ao carregar uma malha
* [3D View] O mapa de ambiente é preto quando o arquivo não pode ser encontrado -> fallback para mapa de ambiente padrão
* [Exibição 3D] Falha após usar uma imagem personalizada de latitude/longitude
* [Exibição 3D] Falha ao carregar arquivo obj específico
* [3D View] o recarregamento automático da malha não funciona corretamente
* [Iray] Não é possível atribuir textura em mdl externo
* [Iray] Não é possível atribuir texturas ao canal de anisotropia após a redefinição do material
* [UI] O menu pop-up do Windows aparece quando o botão direito do mouse é liberado após mover no 3DView
* [Visualização 2D] A ferramenta Informações não retorna o valor da cor do pixel abaixo do cursor
* [Padeiros] As imagens em tons de cinza são salvas como indexadas com o formato tga
* [Graph] As saídas de visualização na visualização 3D devem redefinir os canais antes de enviar as saídas para a visualização 3D
* [Parâmetros] O nome de entrada do parâmetro fica vazio quando exposto de “Expor parâmetros de nó”
* [Desempenho] Define o retorno de chamada onSubstanceCallbackProfileEvent no mecanismo SOMENTE se os tempos estiverem habilitados

### 5.3.1

*(Lançado: 21 de outubro de 2015)*

**Adicionado:**

* [Exibição 3D] Exibe o nome da malha na cena/edição em vez de “Entidade”
* [Visualização 3D] Redefinir para cor padrão quando uma nova visualização 3D for aberta
* [Exibição 3D] Focalizar a câmera ao alternar de cena para primitiva
* [Exibição 3D] Exibe a resolução da viewport de renderização quando a resolução personalizada é usada
* [Iray] Ajustar a apresentação dos parâmetros da subdivisão
* [Iray] Saída das informações do log IRay para o log SD
* [Padeiros] Ler arquivos OBJ corretamente para tornar a correspondência por nome compatível

**Corrigido:**

* [Exibição 3D] Exibição incorreta de malhas com uma escala diferente de 1.0
* [Exibição 3D] A computação automática perto do plano do clipe não funciona bem para objetos grandes
* [Visualização 3D] O modo Wireframe exibe fios muito grossos
* [Exibição 3D] A janela Salvar renderização não aparece se os pós-efeitos estiverem desativados
* [Exibição 3D] Falha ao alternar a geometria
* [3D View] Mensagem “QOpenGLWidget: Cannot make uninitialized widget current” no registro
* [Visualização 3D] A iluminação não é calculada se o mapa de ambiente for alterado enquanto o Iray estiver em execução
* [Exibição 3D] Falha ao visualizar malha 3D
* [3D View] Desempenho muito ruim do OpenGL depois de ter usado o Iray
* [Exibição 3D] Planos de clipe não calculados corretamente
* [Visualização 3D] Alterar o mapa de ambiente não atualiza a visualização 3D
* [Exibição 3D] As texturas não são atualizadas na alteração do gráfico
* [Exibição 3D] As amostras ocultas GLSLFX ainda são exibidas no menu de seleção
* [3D View] Material não restaurado corretamente ao abrir recursos de malha
* [3D View] Vazamento de memória RAM/VRAM ao abrir várias malhas e atribuir vários gráficos sobre elas
* [Visualização 3D] O foco não leva em consideração a distância focal
* [Iray] nvcuvid.dll está ausente (desinstale a versão anterior para remover a mensagem)
* [Iray] O botão &#39;...&#39; da caixa de diálogo Exportar predefinição não gera a janela de diálogo
* [Iray] A refração/dispersão não funciona corretamente em specular\_difuso\_físico
* [Iray] Não é possível encontrar o modelo padrão (cor magenta)
* [Iray] Não conecte texturas padrão a material mdl para ativar o modo de valor no material de edição
* [Iray] A desescala não é acionada quando uma textura é atualizada
* [Bakers] O padeiro normal do espaço mundial renderiza uma imagem em preto
* [Bakers] Falha ao assar o mapa normal com exibição 3D desencaixada
* [Bakers] Cozinhar com o método “Embedded” enquanto um caminho inválido é definido para “link” impede salvar o recurso
* [Bakers] Cozinhar com o método “Embedded” e alterar o formato de arquivo não altera a extensão no disco
* [Padeiros] Nomes aleatórios para recursos incorporados têm todos um nome XXX..
* [Padeiros] Vários objetos em .obj não são importados corretamente
* [Conteúdo] Mesclagem de materiais: a saída de basecolor não fica oculta quando o canal está desativado
* [Content] Branco\_noise e derivado não são renderizados corretamente a 8k
* [Gráfico] Desempenho lento no gráfico
* [Gráfico] Falha ao arrastar e soltar item de função de Biblioteca para Gráfico de função
* [Graph] “Exibir saídas na visualização 3D” deve enviar apenas a saída visível do nó na visualização 3D
* [Preferences] O usuário padrão\_project tem “Name Suffix” vazio para o recurso “match by name baker”
* [Engine] A conversão de cores -> tons de cinza produz perda de precisão
* [Console] O console/log está poluído por muitas mensagens
* [Share] Falha ao tentar compartilhar um pacote
* [IU] A dica de ferramenta fica bloqueada no menu Arquivos recentes
* Falha ao sair

### 5.3.0

*(Lançado em: 01 de outubro de 2015)*

<b>Adicionado:</b>

* [Exibição 3D] Adicionar renderizador Nvidia Iray
* [Exibição 3D] Girar ambiente usando CTRL+Shift+RMB
* [Exibição 3D] Renderizar a viewport 3D em uma resolução personalizada (Ogl/Iray)
* [Visualização 3D] Tornar o carregamento da cena assíncrono
* [Exibição 3D] Exibir a cena global no Navegador da cena
* [Exibição 3D] Desativar a grade por padrão
* [Exibição 3D] Adicionar atenuação de distância quadrada inversa para luzes de ponto
* [Exibição 3D] Exibir parâmetro de cor em RGB em vez de RGBA
* [Visualização 3D] Luzes separadas/Câmera/Configurações de ambiente
* [Compartilhar] Melhorias para a janela de upload de Substance share

<b>Corrigido:</b>

* [3D View] Erro na normalização de sombreadores PBR
* [Visualização 3D] Falha ao clicar com o botão direito do mouse na raiz no navegador de cena
* [Exibição 3D] Sombreadores PBR: conservação de energia difusa versus específica e luzes de ponto
* [Visualização 3D] Criar “material/redefinição” também redefine os canais para a cor padrão
* [Padeiros] Posição com normalização da esfera não centralizada
* [UI] O estado flutuante do Windows não é salvo ao fechar o aplicativo
* [Fogão] Não é possível publicar quando o sbs está localizado em um caminho que contém caracteres especiais
* [Publicação] Pressionar “enter” no campo de nome após a publicação cancelará a caixa de diálogo
* [Compartilhar] Exportar sbs não mantém o alias sbs://

### 5.2.5

*(Lançado: 15 de setembro de 2015)*

**Adicionado:**

* [Compartilhar] Publish um pacote para o Substance share
* [IU] Link para adicionar Substance share no menu Ajuda

**Corrigido:**

* [Cooker] “Tamanho fora dos limites” é um erro em vez de um aviso
* [Cooker] “Não é possível encontrar a saída do subgrafo” é um erro em vez de um aviso
* [Exibição 3D] PBR difusa/especificação prefere basecolor em vez de difusa
* [Exibição 3D] A divisão em blocos gráficos não funciona corretamente com sombreadores de mosaico
* [Engine] Falha ao instanciar arquivo sbsar específico
* [Engine] As funções Sizelog2 / pow2 não funcionam corretamente
* [Engine] “set” no tamanho de saída não funciona
* O Nível do mipmap [Engine] não está bloqueado para valores negativos
* [Conteúdo] Não é possível publicar um gráfico contendo o filtro tri planar

### 5.2.1

*(Lançado: 27 de agosto de 2015)*

**Corrigido:**

* [Graph] Falha ao calcular sbsar específico
* [Graph] Falha ao instanciar fxmap com várias entradas de imagem
* [Engine] Falha com sizelog2
* [Engine] O valor padrão do parâmetro exposto é ignorado com o Mecanismo DX10
* [Library] O cálculo da miniatura é interrompido quando o projeto contém um alias inválido
* [Cooking] Defina “parâmetro\_desconhecido” e “parâmetro duplicado” como aviso em vez de erros
* [Preferências] O limite de cache do mecanismo está bloqueado em 4095 Mb
* O rótulo do parâmetro de entrada [Function] é interpretado como identificador

### 5.2.0

*(Lançado: 18 de agosto de 2015)*

**Adicionado:**

* [Library] Adicione uma opção nas preferências para ocultar/exibir camadas de PSD
* [Parâmetros] Permitir que os dados do usuário estejam em várias linhas
* [Gráfico] Adicione uma opção de preferência para renderizar comentários em um tamanho constante
* [Graph] Adicione uma opção de preferência para desativar a nova exibição de nó na visualização 2D
* [Desempenho] Aumento de desempenho do processador de pixel no mecanismo DX10
* [Exibição 3D] Adicionar mosaico a sombreadores PBR
* [Exibição 3D] Adicionar opacidade simples a sombreadores PBR (sem classificação de face)
* [Content] Adiciona destinos Vray/Corona/Redshift/Arnold ao filtro do conversor PBR (para converter mapas para esses renderizadores)
* [Content] Adicione a técnica “Detail Oriented” ao filtro Combinação normal

**Corrigido:**

* Falha ao abrir sbs com dependência vazia
* O link para as camadas de PSD são quebradas após o recarregamento do pacote
* [Funções] Funções aninhadas quebram o tipo de segurança
* [Funções] Rótulos, Grupos e Descrições não são exibidos
* [Funções] Falha ao copiar/colar de uma função excluída
* [Gráfico] Link de material quebrado com gráficos sbsar
* [Graph] A criação de vários nós de bitmap a partir de recursos torna o nó empilhado
* [Graph] item de comentário não criado na posição correta quando filho de um nó
* [Graph] Seleção de região do bloco de comentários longos
* [Bakers] O mapa normal do espaço tangente fica preto no Mac
* [Parâmetros] Visível Se não funcionar quando o nome de entrada contém “-”
* [Parâmetros] Valor da etapa em Parâmetros de Entrada ignorado se abaixo de 0,01
* [Library] A tag “Visible in library” não é levada em consideração no sbsar

### 5.1.1

*(Lançado em: 04 de junho de 2015)*

**Adicionado:**

* [Gráfico] Reduzir o espaço entre dois nós ao usar a conexão automática
* [Gráfico] Desabilitar Conexão Automática ao usar arrastar e soltar no gráfico
* [Gráfico] Fazer o quadro aderir à grade
* [Gráfico] Desativar a inserção de nó sobre/no link selecionado para link de material
* [Preferências] Defina o valor máximo para o Tamanho máximo da textura como 8192
* [Conteúdo] Adicionar opções de simetria ao nó “Transformação segura”

**Corrigido:**

* [Graph] O novo nó não é encaixado na grade
* [Gráfico] A troca de links pode gerar loops/falhas
* [Graph] Falha de exibição quando o tamanho/temporização está desabilitado
* [Padeiros] Falha ao transferir para um recurso que usa o mesmo nome da cena
* [Padeiros] O nome do recurso padrão não é retirado do arquivo de projeto correto
* [Engine] Problema com a função Pow2/log
* [Engine] Erro na avaliação da função
* [Fxmaps] Falha ao redefinir o parâmetro como padrão
* [FxMaps] Avaliação de função incorreta
* [Preferências] Clicar na guia Projeto trava no SD
* [Exibição 3D] O uso personalizado é convertido em minúsculas
* [Parâmetros] Não é possível reordenar elementos em listas suspensas
* [Explorer] Falha ao mover um gráfico de função no explorador

### 5.1.0

*(Lançado: 28 de maio de 2015)*

**Adicionado:**

* [Gráfico] Pesquisar/Exibir conteúdo da biblioteca por meio do menu da barra de espaços
* [Graph] Exibir/abrir nó recém-criado
* [Gráfico] redirecionamento de link (alt+shift)
* [Gráfico] selecionar pais do nó
* [Gráfico] Trocar 2 links (X)
* [Graph] Inserir nó sobre um link usando arrastar e soltar
* [Gráfico] Criar gráfico a partir de uma seleção de nó
* [Graph] Excluir link ao usar Alt + LMB em um pino de nó
* [Graph] Não conecta o novo nó ao anterior usando Shift
* [Gráfico] Adicionar uma barra de ferramentas para filtros base
* [Gráfico] Aprimorar grade (ajuste e resolução)
* [Gráfico] Mover o comentário/quadro/pino para o menu do clique com o botão direito
* [Gráfico] Criar nó sobre um link selecionado
* [Gráfico] Adicionar ícones a itens de função
* [Gráfico] Alterar as cores dos pinos no gráfico de função
* [Graph] Use shift para desativar a conexão automática do nó
* [Gráfico] Fazer com que o link selecionado seja desenhado sobre os outros links
* [Gráfico] Adicionar ícones aos nós Fxmap
* [Gráfico] Adicionar uma opção para desenhar links curvos ou retangulares
* [Função] Torna o tipo de vetor diferente mais distinto no gráfico de função (cores de pinos/links)
* [Funções] adicionar ícones em nós e exibir valores para constante / set / get
* [Funções] Adicionar cores ao título do nó
* [Função] Melhorar os desempenhos da avaliação da função (usar código gerado pelo SSE)
* [Função] Exibir aviso se o nó Set/Get estiver vazio
* [Padeiros]&#x200B;[Gráfico] Bitmap de pontilhamento ao converter em 8bpc
* [Padeiros] Média dos normais de vértice no arquivo OBJ se a malha não contiver nenhum
* [Padeiros] Corresponder por nome: usar sufixo como separador
* [Parâmetros] Adicione a opção para alternar entre RGB e HSV no widget de cores
* [Parâmetros] Botão Adicionar conta-gotas no widget de cores
* [Library] Adicionar uma categoria para o conteúdo base (nós de composição, fxmap, função...)
* [Exibição 2D] Informações: adicionar vídeo na faixa [0, 1] e HSV
* [Visualização 3D] Adicionar suporte a mipmap para o ambiente
* [Dependências] Limpar dependências não usadas com o atualizador
* [Atualizador] Não salvar pacotes automaticamente

**Corrigido:**

* [Falha] ao fechar o pacote
* [Falha] ao abrir o gerenciador de dependências em um pacote não salvo
* [Falha] Amostra de erro de cor
* [Engine] Bloqueio da região de divisão FxMap
* Problema de precisão do [Engine] com o mecanismo SSE com nó de desfoque e/ou mesclagem
* [Engine] A computação não para ao dividir por 0
* [Explorer] falha ao exportar pacote com dependência se contiver ciclos de dependência
* [Explorer] Arrastar e soltar recursos geralmente não funciona
* [Pães] O normal cozido fica preto se for maior que 256\*256
* [Padeiros] Salvar um pacote no mesmo local do caminho de exportação quebrará o caminho
* [Bakers] Caminho de destino padrão incorreto quando o pacote ainda não foi salvo
* [Engine] Resultado de tamanho de pixel incorreto quando herdado da função pai
* [Dependências] A dependência não usada não foi removida
* [Dependências] falha ao abrir a janela de dependências do pacote que contém ciclos de pacote
* [Gráfico] a seleção de letreiro é redimensionada em função do zoom
* [Graph] link não “encaixar” na entrada/saída mais próxima
* [Gráfico] Pilha de desfazer incorreta (pode gerar travamentos)
* [Graph] Várias conexões com Ctrl não funcionam se o pino já estiver conectado
* [Exibição 3D] A cor da grade é afetada pela cor do plano de fundo
* [Visualização 3D]&#x200B;[Gráfico] O nó de saída contendo vários usos não é enviado corretamente para a visualização 3D
* [Exibição 3D] Sombreador de mosaico : erro de compilação nas GPUs AMD
* [2D View] Problema no sistema de pinos
* [Funções] Erro de compilação de função (se for o caso)
* [Preferências] sufixo baixo/alto não lido corretamente de sbsprj
* [Biblioteca] Arrastar e soltar uma pasta sobre outra a remove
* [Windows] Várias sessões de SD podem ser executadas
* [Licença] A licença antiga não é mantida
* [Content] Problema no filtro de detecção de borda

### 5.0.3

*(Lançado em: 01 de abril de 2015)*

**Adicionado:**

* [Preferências]&#x200B;[Padeiros] Adicionar uma opção para calcular tbn por vértice ou por pixel para corresponder a UE4
* [Biblioteca] Usar filtragem bilinear para miniaturas
* [Padarias] Permitem que a janela seja reduzida para um height inferior a 800px
* [3DView] Equalizar a exposição do mapa de ambiente / normalizar a rotação para obter um relâmpago consistente
* Nomear atalho de aplicativo com versão principal

**Corrigido:**

* [Graph] Falha ao excluir alguns nós fantasmas
* [Graph] nó encaixado permanece encaixado ao duplicar nó
* [Graph] Falha ao excluir nós
* [Graph] As configurações de saídas de exportação não são armazenadas por gráfico
* [Graph] Estado de encaixe de nó inválido ao excluir o nó
* [Padeiros] Os erros não são mais exibidos em uma caixa de diálogo
* [Padeiros] O recurso ausente não é exibido como ausente na janela de cozimento
* [Publicação] a janela com falha não deve ser editável
* [Publicação] Resultado Incorreto do Sbsar
* [Exibição 3D] Vários materiais de malhas FBX atualizadas não são recarregados corretamente
* [Exibição 3D] O SH difuso pode produzir valores negativos em alguns casos em sombreadores PBR
* [Exibição 2D] A profundidade de bits exibida para imagens de recursos é sempre de 8 bpc
* [Parâmetros] Os parâmetros nem sempre são exibidos nas propriedades do gráfico
* [Menu] “Exportar arquivo de log...” ação não gerenciar para localizar o arquivo log.txt
* [Batchtools] Erro do subsmutador
* [Explorer] Carregar pacotes mantém o realce
* [Properties] Falha ao limpar uma função em um parâmetro enum
* [Preferências] O plug-in Mikkt tangent space não está definido como padrão no user\_project
* [Avaliação/Ativação] Não é possível avaliar/ativar online no Windows
* A barra de status de computação move a interface ao atualizar
* Iniciar vários SD ao mesmo tempo
* Atualizar o URL do Player quando o .exe não for encontrado
* A modificação de arquivo no disco não foi detectada corretamente

### 5.0.2

*(Lançado: 17 de março de 2015)*

**Adicionado:**

* [Library] Adicionar controle normal em material\_adjustment\_blend
* [Library] Adicionar opção de mesclagem para normal em material\_color\_blend
* Atualização para o Qt 5. 4. 1

**Corrigido:**

* [Falha] OSX 10.9 e 10.10 no FreeImage
* [Falha] Ao abrir um arquivo fbx que contém elementos sem nenhum vértice
* [Gráfico] Problemas de arrastar e soltar
* [Gráfico] O atalho para limpar o cache está danificado
* [Gráfico] A TGA aparece em preto/transparente no SD
* [Library] Entrada normal de Tons de Cinza Triplanar incorreta
* [Library] O nó de detecção de borda não funciona corretamente com o mecanismo da cpu
* [Parâmetros] Intervalo do controle deslizante incorreto para float2/3/4
* [Parâmetros] Fazer “Parâmetros de exposição” trava duas vezes o Designer
* [Console] Não foi redimensionado corretamente
* [Console] Duplicação na lista de canais: View3D e 3DView
* [3DView] A ordem de parâmetros definida no glslfx não é preservada na GUI
* [Explorer] Falha ao atualizar texturas ausentes no disco
* [Função] Alterar valor e editar leads para falha
* [Baker] Falha ao abrir a janela de cozimento em um recurso 3D ausente
* [PSD] Falha do Psdparse (ausente MSVCR120.dll)
* [Sobre a janela] Quebra de linha ausente com a versão Steam
* [Sbs] Novos recursos de mecanismo não utilizados no SBS
* [Sbsar] Novos recursos não compatíveis quando usados no SD
* [Ui] A barra de progresso não é limpa depois de concluída após uma exportação com dependências
* vcomp100.dll não encontrado ao iniciar o SD em um Windows 7 recém-instalado

**Problemas Conhecidos:**

* [Windows 8] Arrastar e soltar não funciona na primeira inicialização. Reiniciar o SD deve resolvê-lo.

### 5.0.1

*(Lançado: 05 de março de 2015)*

**Corrigido:**

* Correção de um erro ao exportar bitmaps no Windows.

### 5.0.0

*(Lançado: 04 de março de 2015)*

**Adicionado:**

* [Export] descartar canal de Alpha para TGA e BMP quando estiver totalmente opaco
* [3d View] Definir o sombreador PBR por padrão
* [Exibição 2D] Alternar para exibir imagem como alfa pré-multiplicado
* [Parâmetros] Tamanho: adicionar valores de exibição/bloqueio de largura/Height em listas suspensas
* [Dependências] Novo gerenciador de dependências
* [Dependências] exibir/localizar a instância de nó correspondente a uma dependência
* [Dependência] Abrir um pacote de dependência no explorador de pacotes
* [Engine] Mesclagem: suporte ao parâmetro de opacidade quando uma máscara é usada
* [Engine] Mesclar: adicionar novos modos de mesclagem (sobreposição, tela, luz suave, divisão)
* [Engine] Mesclagem: suporta a mesclagem de alfa simples
* [Engine] Novo nó de Gradiente dinâmico
* [Engine] Novo nó Distância
* [Engine] Novo nó de Processador de Pixel
* [Engine] Fxmap: suporta função dinâmica para imagens de entrada
* [Engine] Função Sampler: suporte a amostragem bilinear
* [Engine] Fxmap: suporta filtro bilinear/mais próximo para imagens de entrada
* [Engine] Fxmap: suporta alfa de imagem de entrada reta/pré-multiplicada
* [Padeiros] Adicione uma opção para corresponder a geometria pelo nome da malha entre malhas de baixa e alta definição
* [Modelos] Crie uma substância de modelo para o Substance Painter
* [Bakers] Novo mapa de textura do mesh baker
* [Graph] Adicionar uma “verificação de compatibilidade” para realçar nós que não são compatíveis com o mecanismo anterior
* [UI] Ajustes do menu Ajuda
* [Preferências] defina o plug-in de espaço tangente Mikkt como o padrão (redefina como padrão nas preferências se SD4 estiver instalado)
* [Biblioteca] Adicionar novos mapas hdr
* Novo Substance a partir do modelo
* Mudar para o Qt5
* Atualizar Sistema de Licença para SD5

**Corrigido:**

* [Somente Mac] Problema do seletor de cores com tela de retina
* [Somente Mac] Arrastar e soltar na exibição 3D no sistema operacional Mac também gira a exibição
* [Padeiros] Cozinhar um mapa sem uma pasta de saída produz uma textura vazia
* [Gráfico] Os nós encaixados no quadro se movem de uma maneira estranha
* [Parâmetros] Os caminhos da biblioteca personalizada não são carregados dos arquivos sbsprj
* [Exibição 3D] CTRL+R para recarregar todos os sombreadores também aciona a redefinição da Exibição 3D
* [Visualização 3D] Env. Alternância uniforme do height do Mipmap para padrão ao carregar o sombreador
* [Exibição 3D] Sombreador PBR : erro de digitação difuso vs baseColor
* [Library] Texturas vinculadas de quebra de caminho de biblioteca não recursiva em pacotes
* [Library] Os mapas de ambiente não exibem .hdr
* [Explorer] “Copiar/Colar” na substância não deveria ser possível
* [Explorer] A opção “Colar” do clique com o botão direito ainda está disponível em um gráfico
* A dica de ferramenta [Função] do classificador está incorreta
* [Gráfico] No modo compacto, as instâncias não mostram todos os nomes de links quando são expandidas automaticamente para adicionar um conversor de tons de cinza
