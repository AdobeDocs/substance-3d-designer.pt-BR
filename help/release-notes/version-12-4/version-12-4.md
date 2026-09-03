---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/release-notes/version-12-4.html"
breadcrumb-title: ''
description: Consulte as notas de versão do Substance 3D Designer versão 12.4 para saber mais sobre novos recursos, aprimoramentos e correções de erros.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 12.4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versão 12.4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 1%

---


# Versão 12.4

O **Substance 3D Designer 12.4** traz várias melhorias na qualidade de vida (uma ferramenta para limpar um gráfico, usando fórmulas básicas para definir parâmetros, um botão para gerar semente aleatória, um bloqueio para tamanho etc.) e suporte a gráficos de modelos de Substance na API Python. Veja abaixo para obter mais detalhes sobre todas essas alterações.

Data de lançamento: *31 de janeiro de 2023*

## Melhorias na qualidade de vida

### Ferramenta de limpeza de Grafo

Ao editar o gráfico, às vezes é necessário experimentar várias possibilidades e conectar/desconectar vários nós até o momento em que você obtém o resultado desejado. Então, no final, você tem alguns nós em seu gráfico que não estão conectados a uma saída, portanto, não têm impacto no resultado final. Essa nova ferramenta permitirá que você detecte e exclua automaticamente esses nós para limpar seus gráficos antes de finalizá-los. A ferramenta de limpeza também está opcionalmente procurando em funções de parâmetros e pode ser iniciada no gráfico atual através do botão dedicado na barra de ferramentas Exibição de gráfico ou em uma seleção de gráficos da exibição do Explorer.

![](version-12-4.resources/version-12-4-01.gif){width="640px"}

### Digite fórmulas nos campos de parâmetros

Não é mais necessário usar uma calculadora ou calcular na cabeça quando você deseja inserir valores de parâmetro específicos. Agora, você pode inserir fórmulas básicas diretamente, como adições, divisões, multiplicações ou subtrações, ao definir um valor numérico para um parâmetro nas Propriedades e em outros locais no aplicativo.

![](version-12-4.resources/version-12-4-02.gif){width="640px"}

### Botões de acesso rápido na Visualização 3D

Adicionamos uma barra de ferramentas adicional no [modo de exibição 3D](../../interface/3d-view/3d-view.md) correspondente a todas as opções disponíveis no menu [Exibição](../../interface/3d-view/3d-view.md), para acesso rápido a todas essas opções (por exemplo, Wireframe, Grade, Caixa Delimitadora etc.) à medida que o botão é alternado. Também adicionamos um alternador para mostrar/ocultar o mapa de ambiente.

![](version-12-4.resources/version-12-4-03.gif){width="640px"}

### Botão para gerar uma Distribuição Aleatória

Agora você pode criar variações diferentes rapidamente usando um novo botão para gerar a semente aleatória para o seu gráfico, em vez de mover um controle deslizante.

![](version-12-4.resources/version-12-4-04.gif){width="640px"}

### Bloquear para o widget Tamanho de saída

Agora você pode bloquear a largura e o height do Tamanho de saída para manter um tamanho quadrado e evitar a manipulação dos dois valores sempre que desejar atualizá-los.

![](version-12-4.resources/version-12-4-05.gif){width="640px"}

### Transformar a entrada da imagem em Cor/Escala de cinza

Alterne rapidamente entre uma [Cor de Entrada](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) e uma [Escala de Cinza de Entrada](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) pelo menu contextual do nó.

![](version-12-4.resources/version-12-4-06.gif){width="640px"}

### Selecione o pino clicado ao exibir o Editor de gradiente

No painel de propriedades, ao clicar em um pino para editar um gradiente, agora você selecionará automaticamente o pino correspondente no [Editor de gradiente](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) exibido.

![](version-12-4.resources/version-12-4-07.gif){width="640px"}

### Selecionar nós à frente

Nova entrada no [menu contextual de nó](../../interface/the-graph-view/the-graph-view.md) para selecionar todos os nós conectados à saída do(s) nó(s) selecionado(s), direta ou indiretamente. Assim, você seleciona todos os nós afetados pelo nó. Útil para excluir parte do seu gráfico ou para trabalhar novamente o layout do gráfico.

![](version-12-4.resources/version-12-4-08.gif){width="640px"}

## Atualizações da API Python

Esta versão 12.4 traz também o suporte completo de gráficos de modelos de Substance através da API Python. Isso significa que agora você tem todas as ferramentas necessárias para criar, editar ou avaliar gráficos de modelos de Substance. Para obter detalhes completos, consulte a documentação disponível no menu Ajuda do software.

## Notas de versão

### 12.4.0

*(Lançado Em 24 De Janeiro De 2023)*

<b>Adicionado:</b>

* [Visualização 3D] Adicione botões de acesso rápido para definir opções de exibição (Wireframe, mapa do ambiente, estatísticas da cena etc.)
* [Gerenciamento de cores] Melhorar a qualidade de LUTs 3D cozidos no modo ACE
* [Documentação] Projetos de amostra para gráficos de Substance
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
* [IU] Realçar na Visualização 3D o item atualmente selecionado no Navegador de cena
* [UX] Redefinir intervalos do controle deslizante quando seu valor é redefinido
* [API] Permitir a adição de ações às barras de ferramentas de exibição de gráfico
* [API] Permite criar/editar/avaliar um gráfico de modelo de Substance pela API

<b>Corrigido:</b>

* [3D View] O valor da propriedade “DirectX normal” não é compartilhado entre os renderizadores
* [Exibição 3D] A exibição das estatísticas de cena é ampliada quando a viewport é pequena
* [3D View] A propriedade de exibição do Wireframe não é salva
* [Conteúdo] Os parâmetros de Cor de desfoque radial não têm efeito no canal alfa
* [Localização] Controles deslizantes e botões adicionais são exibidos em Propriedades do OpenGL do ambiente.
* [MDL]&#x200B;[modelo Substance] Falha ao excluir nós expostos
* [Preferências] O arquivo padrão\_config nunca é recriado se excluído
* [Modelo de Substance] Parâmetro de reordenação de falha que não aparece no nível da instância
* [API] SDProperty.getDefaultValue() quase sempre retorna None
