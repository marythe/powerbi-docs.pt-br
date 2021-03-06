---
title: Cmdlets do PowerShell, APIs REST e SDK do .NET para administradores
description: Saiba mais sobre as maneiras de administrar o Power BI por meio de scripts e APIs de programação.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: overview
ms.date: 06/25/2018
ms.author: mblythe
LocalizationGroup: Administration
ms.openlocfilehash: c33d75fa09a4e94e4db6a2b968cd3a3170afd397
ms.sourcegitcommit: f5e39e9ead37445bbeab795890b3d80633383032
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/21/2018
ms.locfileid: "53735536"
---
# <a name="powershell-cmdlets-rest-apis-and-net-sdk-for-power-bi-administration"></a>Cmdlets do PowerShell, APIs REST e SDK do .NET para a administração do Power BI
O Power BI permite aos administradores fazer scripts de tarefas comuns com os cmdlets do PowerShell. Ele também expõe as APIs REST e fornece um SDK do .NET para desenvolver soluções administrativas. Este tópico mostra uma lista de cmdlets e o método do SDK correspondente, bem como o ponto de extremidade da API REST. Para obter mais informações, veja:

- [Download](https://www.powershellgallery.com/packages/MicrosoftPowerBIMgmt/) e [documentação](https://docs.microsoft.com/powershell/power-bi/overview?view=powerbi-ps) do PowerShell
- [Documentação](https://docs.microsoft.com/rest/api/power-bi/admin) da API REST
- [Download](https://www.nuget.org/packages/Microsoft.PowerBI.Api/) do SDK do .NET

> Os cmdlets abaixo devem ser chamados com `-Scope Organization` para operar no locatário para administração.

| **Nome do cmdlet** | **Aliases** | **Método do SDK** | **Ponto de extremidade da API REST** | **Descrição** |
| --- | --- | --- | --- | --- |
| `Get-PowerBIDatasource` | N/A | `Datasets_GetDataSourcesAsAdmin` | /v1.0/myorg/admin/datasets/{datasetkey}/datasources | Obtém as fontes de dados para um determinado conjunto de dados. |
| `Get-PowerBIDataset` | N/A | `Datasets_GetDatasetsAsAdmin` | /v1.0/myorg/admin/datasets | Obtém a lista completa de conjuntos de dados em um locatário do Power BI. |
| `Get-PowerBIWorkspace` | `Get-PowerBIGroup` | `Groups_GetGroupsAsAdmin` | /v1.0/myorg/admin/groups | Obtém a lista completa de workspaces em um locatário do Power BI. |
| `Add-PowerBIWorkspaceUser` | `Add-PowerBIGroupUser` | `Groups_AddUserAsAdmin` | /v1.0/myorg/admin/groups/{groupId}/users | Adiciona um usuário como um membro a um determinado workspace. |
| `Remove-PowerBIWorkspaceUser` | `Remove-PowerBIGroupUser` | `Groups_DeleteUserAsAdmin` | /v1.0/myorg/admin/groups/{groupId}/users/{user} | Remove um usuário da lista de membros de um determinado workspace. |
| `Restore-PowerBIWorkspace` |`Restore-PowerBIGroup` | `Groups_RestoreDeletedGroupAsAdmin` | /v1.0/myorg/admin/groups/{groupId}/restore | Restaura um workspace excluído. |
| `Set-PowerBIWorkspace` |`Set-PowerBIGroup` | `Groups_UpdateGroupAsAdmin` | /v1.0/myorg/admin/groups/{groupId} | Atualiza as propriedades de um determinado workspace. |
| `Get-PowerBIDataset -WorkspaceId` | N/A | `Groups_GetDatasetsAsAdmin` | /v1.0/myorg/admin/groups/{group\_id}/datasets | Obtém os conjuntos de dados dentro de um determinado workspace. |
| `Get-PowerBIReport` | N/A | `Reports_GetReportsAsAdmin` | /v1.0/myorg/admin/reports | Obtém a lista completa de relatórios em um locatário do Power BI. |
| `Get-PowerBIDashboard` | N/A | `Dashboards_GetDashboardsAsAdmin` | /v1.0/myorg/admin/dashboards | Obtém a lista completa de dashboards em um locatário do Power BI. |
| `Get-PowerBIDashboard -WorkspaceId` | N/A | `Groups_GetDashboardsAsAdmin` | /v1.0/myorg/admin/groups/{group\_id}/dashboards | Obtém os dashboards dentro de um determinado workspace. |
| `Get-PowerBITile` | `Get-PowerBIDashboardTile` | `Dashboards_GetTilesAsAdmin` | /v1.0/myorg/admin/dashboards/{dashboard\_id}/tiles | Obtém os blocos de um determinado dashboard. |
| `Get-PowerBIReport` | N/A | `Groups_GetReportsAsAdmin` | /v1.0/myorg/admin/groups/{group\_id}/reports | Obtém os relatórios dentro de um determinado workspace. |
| `Get-PowerBIImport` | N/A | `Imports_GetImportsAsAdmin` | /v1.0/myorg/admin/imports | Obtém a lista completa de importações em um locatário do Power BI. |
| `Connect-PowerBIServiceAccount` | `Login-PowerBI` &  `Login-PowerBIServiceAccount` | N/A | N/A | Faça logon no Power BI e inicie uma sessão. |
| `Disconnect-PowerBIServiceAccount` | `Logout-PowerBI` & `Logout-PowerBIServiceAccount` | N/A | N/A | Faça logoff do Power BI e feche a sessão existente. |
| `Invoke-PowerBIRestMethod`| N/A | Não aplicável | N/A | Envie chamadas arbitrárias da API REST ao Power BI. |
| `Get-PowerBIAccessToken`| N/A | Não aplicável | N/A | Obtenha o token de acesso do Power BI em uma sessão. |
| `Resolve-PowerBIError`| N/A | Não aplicável | N/A | Obtenha informações detalhadas do erro para chamadas de cmdlet sem êxito. |
