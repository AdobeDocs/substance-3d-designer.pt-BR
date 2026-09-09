---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/release-notes/version-12-3.html"
breadcrumb-title: ''
description: Consulte as notas de versão do Substance 3D Designer versão 12.3 para saber mais sobre novos recursos, aprimoramentos e correções de erros.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 12.3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versão 12.3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 0%

---


# Versão 12.3

O <b>Substance 3D Designer 12.3</b> leva os gráficos de modelos do Substance a um novo nível com o <b>suporte de subgrafos</b> (ou instâncias de gráfico), além do<b> &#39;Visible if&#39; </b>controle para parâmetros expostos e alguns<b> novos nós</b> dedicados à edição de curvas. Esta versão também apresenta dois novos painéis (<b>Bem-vindo(a) </b>e <b>Novidades</b>) para aprimorar a integração do usuário e alguns outros recursos secundários ou correções de erros descritos abaixo.

Data de lançamento: *6 de outubro de 2022*

![](../../assets/largef.png){width="1111px"}

## Principais recursos

### Suporte a instâncias do gráfico em gráficos de modelo do Substance

Se você está acostumado a criar gráficos, precisa ser capaz de criar subgrafos (ou ocorrências de gráficos) para reutilizar seu trabalho, tornar os gráficos menos confusos e mais eficientes.\
Isso agora também é possível para gráficos de modelo do Substance: basta arrastar e soltar seu subgrafo do Explorer para o gráfico principal para usá-lo como um nó de instância.

![](../../assets/subgraph.gif){width="600px"}

Também introduzimos o conceito de nós de saída para gráficos de modelo do Substance, como cena de saída. Agora você tem a possibilidade de ter uma ou mais saídas no seu gráfico.\
Cada saída corresponderá a um fixar de saída quando seu gráfico for instanciado em outro gráfico.

![](../../assets/image2022-10-4-15-31-27.png){width="600px"}

Quando você clica com o botão direito do mouse em um nó de instância, é claro que você pode acessar seu subgrafo referenciado para visualizá-lo ou editá-lo.

![](../../assets/image2022-10-4-16-28-36.png){width="600px"}

Graças a subgrafos e parâmetros expostos, você pode criar ativos complexos e aplicar infinitas variações, conforme demonstrado na ilustração abaixo.

![](../../assets/seasons.gif){width="600px"}

### Outras melhorias nos gráficos de modelos do Substance

* <b>Visível para parâmetros expostos</b>\
  Ao expor parâmetros, talvez você queira ocultar ou mostrar parâmetros com base no status de outros parâmetros. Por exemplo, um controle deslizante é exibido somente quando um botão está ativado.\
  Com <b>Se Visível</b>, você pode adicionar condições à visibilidade de parâmetro, mantendo uma interface de usuário limpa e funcional. Esse mecanismo já disponível para gráficos de Substance agora é estendido para gráficos de modelo do Substance, usando, é claro, a mesma sintaxe. <b>\
  </b>

  ![](../../assets/visibleif.gif){width="600px"}

* <b>Novos nós dedicados à edição em curva\
  </b>Esta versão traz alguns novos nós dedicados à edição de curva: a <b>curva reversa</b> troca as duas extremidades de uma curva, a <b>subdivisão de curva</b> adiciona mais vértices em segmentos de acordo com dois métodos, a <b>curva de suavização </b>suaviza todos os ângulos em uma curva 2D e finalmente a <b>curva de deslocamento</b> infla ou esvazia uma curva 2D, conforme mostrado abaixo.<b>

  </b>

  ![](../../assets/curve-offset-4.gif){width="600px"}
* <b>Nova janela de gráfico </b>\
  A janela <b>Novo gráfico de modelo do Substance</b> agora também está disponível para gráficos de modelo do Substance. Você pode adicionar seus próprios modelos ou selecionar um padrão e, em seguida, inserir diretamente o nome do gráfico e selecionar o pacote ao qual o gráfico será adicionado.

  ![](../../assets/image2022-10-5-15-25-42.png){width="600px"}

### Painéis Bem-vindo e Novidades

Apresentamos dois novos painéis para ajudar você a começar a usar o Designer:

Primeiro, o painel <b>Boas-vindas </b> - exibido na primeira vez que você *inicia* o Designer - oferece uma visão geral global do software e sua função no ecossistema Substance 3D. Em seguida, o painel <b>Novidades </b> - exibido na primeira vez que você executa uma *nova versão* do Designer - apresenta rapidamente os principais recursos introduzidos nesta versão.

Esses dois painéis também podem ser acessados no menu Ajuda.

![](../../assets/image2022-10-3-15-47-28.png)

![](../../assets/image2022-10-3-15-47-55.png)

### Diversos

* <b>Widget de dois botões para parâmetros booleanos expostos</b>\
  Agora você tem uma nova maneira de expor parâmetros booleanos em um gráfico de Substance. Além do botão de alternância, você pode usar <b>Botões lado a lado</b> com textos personalizados para tornar mais visíveis os dois modos diferentes acionados pelo parâmetro booleano.
* <b>Resolver problemas de dimensionamento para telas de DPI alto </b>\
  Nas versões anteriores, o Designer não conseguia lidar corretamente com o fator de dimensionamento definido no sistema operacional. Como você pode ver na ilustração abaixo, tudo é perfeitamente gerenciado em uma tela 4K com escala de 125% com todas as fontes e botões exibidos em um tamanho coerente.\
  Observe que a opção &#39;Desativar DPI alto&#39; nas Preferências foi redefinida para *Falso* nesta nova versão, pois essa opção não é mais necessária para ter uma interface utilizável.

  ![](../../assets/highdpi-fix.gif){width="600px"}

* **Suporte nativo ao Apple Silicon (M1 / M2) para a versão Steam**\
  A versão 12.2 do Designer foi a primeira a trazer suporte completo de novas máquinas Apple baseadas em chips M1 ou M2, mas esse suporte estava ausente da edição Steam. De agora em diante, todos os usuários do Designer podem se beneficiar de uma experiência mais rápida e eficiente nessas máquinas.

## Notas de versão

### 12.3.0

*(Lançado Em 06 De outubro De 2022)*

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
