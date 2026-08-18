---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/getting-started/activation-and-licenses.html"
breadcrumb-title: ''
description: Saiba como ativar e gerenciar licenças do Substance 3D Designer para acessar todos os recursos e capacidades.
helpx_creative_field: ""
helpx_description: Designer > Getting started > Activation and licenses
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ativação e licenças
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---


# Processo de ativação por tipo de aplicativo

O processo de ativação depende de onde você adquiriu ou tem acesso ao Designer:

| Edição | Processo de ativação |
| --- | --- |
| Creative Cloud para desktop | Consulte a página dedicada na [documentação do HelpX](https://helpx.adobe.com/support/substance-3d-designer.html). Caso haja problemas, a [documentação do Creative Cloud](https://helpx.adobe.com/creative-cloud/user-guide.html) poderá fornecer respostas adicionais. |
| Vapor | Inicie o produto diretamente da biblioteca do Steam. |
| Substance (autônomo) | Consulte o processo de ativação descrito abaixo. |

## Etapas de ativação (edição Substance)

### USANDO O ASSISTENTE DE ATIVAÇÃO

Há três opções disponíveis:

* <b>Avalie este produto</b>: as versões de avaliação herdadas não estão mais disponíveis. Em vez disso, você pode iniciar uma avaliação de 30 dias para cada aplicativo da Substance 3D [aqui](https://www.adobe.com/creativecloud/3d-augmented-reality.html) ou com o Creative Cloud Desktop. Cada versão de avaliação é independente dos outros aplicativos da Substance 3D, portanto você pode experimentá-los um de cada vez ou todos de uma vez.
* <b>Ativar usando um arquivo de licença</b>: ative o produto com um arquivo de licença (<b>\*.key</b>) baixado da página da sua conta no [site da Substance 3D](https://store.substance3d.com/user) antes de 30 de setembro de 2022.
* <b>Ative usando sua conta</b>: contas do substance herdadas não podem mais ser usadas para ativação. [Mais informações sobre contas Substance estão disponíveis aqui](https://helpx.adobe.com/substance-3d/unlisted/faq-end-of-life-accounts.html).

>[!IMPORTANT]
>
> Para instalar o arquivo de licença com o Assistente de ativação, execute o Designer como administrador e desative temporariamente o antivírus.

![Assistente de ativação](../../assets/activation-wizard.png "Assistente de ativação")

### Ativação manual

Você pode ativar manualmente o Designer colocando o arquivo license.key na seguinte pasta:

<table data-preserve-html="true">
<colgroup> <col/> <col/> <col/> <col/> </colgroup><tbody><tr><th style="text-align: left;">Plataforma</th>
<th style="text-align: left;">Versão</th>
<th colspan="2" style="text-align: left;">Caminho</th>
</tr><tr><td rowspan="4" style="text-align: left;"><b>Windows</b></td>
<td rowspan="2" style="text-align: left;"><b>11.2</b> ou posterior</td>
<td style="text-align: left;">AppData &gt; Local</td>
<td style="text-align: left;">C:\Users\[nome do usuário]\AppData\Local\Adobe\Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;">AppData &gt; Roaming</td>
<td style="text-align: left;">C:\Users\[nome do usuário]\AppData\Roaming\Adobe\Adobe Substance 3D Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>11.1</b> ou inferior</td>
<td style="text-align: left;">AppData &gt; Local</td>
<td style="text-align: left;">C:\Users\[nome do usuário]\AppData\Local\Allegorithmic\Substance Designer</td>
</tr><tr><td style="text-align: left;">AppData &gt; Roaming</td>
<td style="text-align: left;">C:\Users\[nome do usuário]\AppData\Roaming\Allegorithmic\Substance Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>Mac</b></td>
<td style="text-align: left;"><b>11.2</b> ou posterior<br/>
</td>
<td colspan="2" style="text-align: left;">/Users/[nome do usuário]/Library/Application Support/Adobe/Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;"><b>11.1</b> ou inferior<br/>
</td>
<td colspan="2" style="text-align: left;">/Users/[nome do usuário]/Library/Application Support/Allegorithmic/Substance Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>Linux</b></td>
<td style="text-align: left;"><b>11.2</b> ou posterior</td>
<td colspan="2" style="text-align: left;">/home/[nome do usuário]/.local/share/Adobe/Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;"><b>11.1</b> ou inferior<br/>
</td>
<td colspan="2" style="text-align: left;">/home/[nome do usuário]/.local/share/Allegorithmic/Substance Designer</td>
</tr></tbody></table>

>[!NOTE]
>
> Alguns dos diretórios nos caminhos mencionados acima podem estar ocultos por padrão. Digite o caminho manualmente no explorador de arquivos ou exiba arquivos ocultos para exibi-los.

>[!IMPORTANT]
>
> Verifique se o arquivo é chamado de **license.key**, caso contrário, o aplicativo não poderá encontrá-lo.

### VARIÁVEL DE AMBIENTE

Você pode substituir o local que o Designer verifica para o arquivo <b>license.key</b> por uma [variável de ambiente](../../pipeline-and-project-con/environment-variables/environment-variables.md).
