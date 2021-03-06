---
title: 'Serviço de terceiros: Conector do Google Analytics'
description: 'Serviço de terceiros: Conector do Google Analytics para Power BI Desktop'
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 12/06/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: b7451f156503d88baf4bdf3f3ae2cb99c04a94c1
ms.sourcegitcommit: 72c9d9ec26e17e94fccb9c5a24301028cebcdeb5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/07/2018
ms.locfileid: "53025593"
---
# <a name="google-analytics-connector-for-power-bi-desktop"></a>Conector do Google Analytics para Power BI Desktop
> [!NOTE]
> O pacote de conteúdo do Google Analytics e o conector no Power BI Desktop dependem da API do Google Analytics Core Reporting. Por isso, os recursos e a disponibilidade podem variar ao longo do tempo.

É possível se conectar aos dados do Google Analytics usando o conector do **Google Analytics**. Para se conectar, siga essas etapas:

1. No **Power BI Desktop**, selecione **Obter Dados** na guia de faixa de opções **Página Inicial**.
2. Na janela **Obter Dados** janela, selecione **Serviços Online** das categorias no painel esquerdo.
3. Selecione **Google Analytics** com as seleções no painel à direita.
4. Na parte inferior da janela, selecione **Conectar**.  
   ![](media/service-google-analytics-connector/tps_googleanalytics_1.png)

Você verá um diálogo que explica que o conector é um Serviço de Terceiro e que avisa sobre como os recursos e a disponibilidade podem ser alterados com o tempo, bem como outros esclarecimentos.  
![](media/service-google-analytics-connector/tps_googleanalytics_2.png)

Ao selecionar **Continuar**, você será solicitado a entrar no Google Analytics.  
![](media/service-google-analytics-connector/tps_googleanalytics_3.png)

Ao digitar suas credenciais, você será notifica que o Power BI gostaria de ter acesso offline. É assim como você usa o **Power BI Desktop** para acessar seus dados do Google Analytics.  

Depois de aceitar, o **Power BI Desktop** mostra que você está conectado no momento.  
![](media/service-google-analytics-connector/tps_googleanalytics_5.png)

Selecione **Conectar** para que os dados do Google Analytics sejam conectados ao **Power BI Desktop** e carregados.  
![](media/service-google-analytics-connector/tps_googleanalytics_6.png)

## <a name="changes-to-the-api"></a>Alterações no API
Podemos tentar lançar atualizações de acordo com as alterações, o API pode ser alterado de forma que afeta os resultados das consultas que gerarmos. Em alguns casos, determinadas consultas podem não ter mais suporte. Devido a essa dependência não podemos garantir os resultados de suas consultas ao usar esse conector.

Mais detalhes sobre as alterações na API do Google Analytics podem ser encontrados em seus [log de alterações](https://developers.google.com/analytics/devguides/changelog).

