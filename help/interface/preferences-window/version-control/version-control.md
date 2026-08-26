---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/interface/preferences-window/version-control.html"
breadcrumb-title: ''
description: Defina as configurações de controle de versão nas preferências do Substance 3D Designer para integração com o Git e outros sistemas.
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences window > Version control
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Controle de versão
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---


# Controle de versão

>[!IMPORTANT]
>
> A versão <b>14.0.0</b> do Substance 3D Designer atualiza o suporte a Perforce para <b>Python 3</b>.
> 
> Verifique se os outros scripts e o ambiente de controle de versão estão ajustados de acordo.

O Designer oferece uma integração Python para o sistema de controle de versão [Perforce](https://www.perforce.com/) (P4).

A integração adiciona um submenu personalizado &#39;Controle de Versão&#39; ao menu contextual de pacotes no [Explorer](../../../interface/the-explorer-window/the-explorer-window.md), bem como ícones personalizados para corresponder ao status de um pacote no P4.

## Preparando P4

No [P4V](https://www.perforce.com/products/helix-core-apps/helix-visual-client-p4v), anote o nome e o caminho do espaço de trabalho, conforme mostrado abaixo:

![Informações do espaço de trabalho P4V](../../../assets/p4v-workspace-strings.jpg "Informações do espaço de trabalho P4V"){zoomable="yes"}

Em qualquer editor de texto ou IDE, abra este script localizado na instalação do Designer: &#39;*tools/version\_control/perforce.py*&#39;.

Na linha 19, edite o caminho para o local do executável <b>&#39;p4&#39;</b> em seu sistema.\
No exemplo abaixo, esse caminho é &#39;*c:/Program Files/Perforce/p4.exe*&#39;.

```
## Editable variables

cPerforceP4AbsPath = os.path.abspath("c:/Program Files/Perforce/p4.exe")

cVerbose = False
```


## Configuração no Designer

O controle de versão está configurado nas [Configurações do projeto](../../../interface/preferences-window/project-settings/project-settings.md), disponíveis nas [Preferências](../../../interface/preferences-window/preferences-window.md) do Designer.

Guia ![&#39;Controle de versão&#39; nas configurações do projeto](../../../assets/p4v-project-settings.jpg " Guia&#39;Controle de versão&#39; nas configurações do projeto"){zoomable="yes"}

1. Acesse “Editar > Preferências”
1. Vá para &#39;Projetos&#39;, selecione o [arquivo de projeto](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) de destino e vá para a guia &#39;Controle de Versão&#39;
1. Verificar &#39;Controle de Versão Habilitado&#39;
1. Preencha estas informações na seção &#39;Espaço de trabalho&#39;:

   * <b>Nome:</b> insira o &#39;Nome do Espaço de Trabalho&#39; recuperado anteriormente do P4V
   * <b>Caminho:</b> insira o &#39;Caminho de Espaço de Trabalho&#39; recuperado anteriormente do P4V

![Configuração P4 no Designer: espaço de trabalho](../../../assets/p4v-project-settings-workspace.jpg "Configuração P4 no Designer: espaço de trabalho"){zoomable="yes"}

### Configurar ações

As ações estarão disponíveis no menu contextual de um pacote no Explorer. Existem ações predefinidas que correspondem à maioria dos conceitos de ferramentas do Controle de versão:

* Todos os rótulos de ação podem ser alterados conforme necessário.
* Todas as ações precisam de um script para serem válidas.

Você pode usar:

* um script *por* ação
* um script para *todas* ações

Um script inicial para todas as ações está disponível na instalação do Designer: &#39;*tools/version\_control/perforce.py*&#39;.

>[!IMPORTANT]
>
> Para estar disponível, o pacote precisa ser salvo no &#39;Caminho do espaço de trabalho&#39; (por exemplo, em &#39;*f:/Dev/perforce*&#39;)

1. No grupo <b>Ações</b>, clique no botão &#39;...&#39; da ação <b>Adicionar</b>
1. Selecione o seguinte script na instalação do Designer: &#39;*tools/version\_control/perforce.py*&#39;
1. O script deve ser configurado automaticamente para todas as outras ações.

![Configuração P4 no Designer: ações](../../../assets/p4v-project-settings-actions.jpg "Configuração P4 no Designer: ações"){zoomable="yes"}

### Configurar ações personalizadas

Como todas as ferramentas de controle de versão são diferentes e incluem muitos recursos, permitimos que o usuário adicione ações personalizadas.

1. Clique em &#39;Adicionar item&#39;
1. Preencha o rótulo da nova ação e defina o caminho do script

### Configurar o interpretador de scripts

1. Na seção “Intérpretes”, clique em “Adicionar item”
1. Definir uma extensão ou sufixo de arquivo de script e o caminho para o executável do intérprete
1. Edite o script perforce.py para atualizar o local do binário &#39;p4&#39;

![Configuração P4 no Designer: intérprete](../../../assets/p4v-project-settings-interpreters.jpg "Configuração P4 no Designer: intérprete"){zoomable="yes"}

## Como usar o controle de versão

1. Criar um novo pacote
1. Salve o pacote no diretório “Caminho do espaço de trabalho”
1. Clique no RMB no pacote: agora você tem acesso ao submenu “Controle de versão”
1. Várias ações estão disponíveis, dependendo do status do arquivo de pacote no espaço de trabalho:

   * <b>Adicionar:</b> Marque os arquivos como &#39;ToAdd&#39;
   * <b>Enviar:</b> envie os pacotes selecionados. Esta ação exibe uma caixa de diálogo para especificar uma mensagem de alteração (veja abaixo)
   * <b>Reverter:</b> reverta as modificações. Esta ação exibe uma caixa de diálogo para selecionar os arquivos a serem revertidos (veja abaixo)
   * <b>Check-out:</b> faça o check-out do arquivo do depósito
   * <b>Obter última versão:</b> recupere a versão mais recente do depósito
   * <b>Status da atualização:</b> Atualize o status do arquivo do pacote

   <table>
   <tr style="border: 0;">
   <td style="border: 0;" valign="top">

   Caixa de diálogo ![&#39;Enviar&#39;](../../../assets/p4v-submit.jpg "&#39;Enviar&#39;"){zoomable="yes"}

   </td>
   <td style="border: 0;" valign="top">

   ![&#39;Reverter&#39; caixa de diálogo](../../../assets/p4v-revert.jpg "&#39;Reverter&#39; caixa de diálogo"){zoomable="yes"}

   </td>
   </tr>
   </table>

>[!NOTE]
>
> Todas as ações são compatíveis com várias seleções
> 
> Para o P4 e outras ferramentas de controle de versão que usam a permissão de arquivo somente leitura para restringir modificações, o usuário precisará primeiro fazer check-out do pacote antes de modificá-lo.
> 
> Arquivos de pacote somente leitura não podem ser modificados no SD.

Dependendo do status do pacote, ele terá os seguintes ícones:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ícone de pacote: atualizado](../../../assets/p4-up-to-date.png "Ícone de pacote: atualizado")

Atualizado

</td>
<td style="border: 0;" valign="top">

![Ícone de pacote: Check-out](../../../assets/p4-checked-out.png "Ícone de pacote: Check-out")

Check-out feito

</td>
<td style="border: 0;" valign="top">

![Ícone de pacote: adicionado](../../../assets/p4-added.png "Ícone de pacote: adicionado")

Marcado para adição

</td>
<td style="border: 0;" valign="top">

![Ícone de pacote: não está no depósito](../../../assets/p4-not-in-depot.png "Ícone de pacote: não está no depósito")

Fora do depósito

</td>
</tr>
</table>

Observe que um pacote que não está atualizado é marcado com um sinal de aviso.

## Scripts de ação

O comando executado por cada ação é compilado desta forma:

meu\_script <b>*NomeEspaçoTrabalhoCaminhoEspaçoTrabalhoNomeAção[ArgosdeAção]*</b>

<b>WorkspaceName:</b> o nome do espaço de trabalho

<b>WorkspacePath:</b> o caminho do diretório raiz do espaço de trabalho

<b>ActionName:</b> o nome da ação:

* *adicionar:* para a ação “Adicionar”
* *check-out:* para a ação “Check-out”
* *enviar:* para a ação “Enviar”
* *reverter:* para a ação “Reverter”
* *get\_last\_version:* para a ação “Obter Última Versão”
* *get\_status:* para a ação “Obter Status”

O rótulo é configurado nas configurações do projeto, com o caractere &#39; &#39; substituído por &#39;\_&#39;. Por exemplo: “Minha ação” => “Minha ação\_ação”.

<b>ActionArgs:</b> argumentos da ação:

* *-desc*: uma cadeia de caracteres de descrição usada pela ação &#39;Enviar&#39;
* *-arquivos:* Uma lista de arquivos
* *-files\_list:* Um arquivo de texto que contém uma lista de arquivos por linha

<b>get\_status</b>: retorna um valor que depende do status do arquivo especificado:

* 0: status indefinido
* 1: não está no depósito
* 2: versão anterior (não atualizada)
* 3: versão mais recente (atualizada)
* 4: retirada
* 5: marcado para adição
* outras ações:
  * 0: sucesso
  * outro: erro
