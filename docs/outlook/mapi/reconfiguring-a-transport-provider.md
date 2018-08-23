---
title: Изменение конфигурации поставщика транспорта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5e7c94b387a5fe9f9682854de4097f6f1bbcd786
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565601"
---
# <a name="reconfiguring-a-transport-provider"></a><span data-ttu-id="8f808-103">Изменение конфигурации поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="8f808-103">Reconfiguring a Transport Provider</span></span>

  
  
<span data-ttu-id="8f808-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f808-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f808-105">Чтобы изменить некоторые свойства поставщика можно использовать объект состояние поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="8f808-105">You can use a transport provider's status object to change some of the properties of the provider.</span></span> <span data-ttu-id="8f808-106">Диапазон свойств, которые могут быть изменены зависит от свойства, которые включены в поставщика свойств и определение этих свойств.</span><span class="sxs-lookup"><span data-stu-id="8f808-106">The range of properties that can be changed depends on the properties that are included with the provider's property sheet and how those properties are defined.</span></span> 
  
 <span data-ttu-id="8f808-107">**Чтобы снова настроить поставщика транспорта активный**</span><span class="sxs-lookup"><span data-stu-id="8f808-107">**To reconfigure an active transport provider**</span></span>
  
1. <span data-ttu-id="8f808-108">Вызов [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для доступа к таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="8f808-108">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="8f808-109">Найдите строку для поставщика транспорта нужно правильно настроить путем создания ограничение свойство, которое соответствует **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) с именем конечного поставщика.</span><span class="sxs-lookup"><span data-stu-id="8f808-109">Locate the row for the transport provider to be reconfigured by creating a property restriction that matches **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the target provider.</span></span> 
    
3. <span data-ttu-id="8f808-110">Вызов [IMAPITable::FindRow](imapitable-findrow.md) для извлечения соответствующих строк.</span><span class="sxs-lookup"><span data-stu-id="8f808-110">Call [IMAPITable::FindRow](imapitable-findrow.md) to retrieve the appropriate row.</span></span> 
    
4. <span data-ttu-id="8f808-111">Проверьте, что в свойстве **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)), поставщика транспорта конечного флаги STATUS_SETTINGS_DIALOG и STATUS_VALIDATE_STATE.</span><span class="sxs-lookup"><span data-stu-id="8f808-111">Check that the STATUS_SETTINGS_DIALOG and STATUS_VALIDATE_STATE flags are set in the target transport provider's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span> <span data-ttu-id="8f808-112">Если STATUS_SETTINGS_DIALOG не задано, поставщика транспорта не отображаются на листе свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8f808-112">If STATUS_SETTINGS_DIALOG is not set, the transport provider does not display a configuration property sheet.</span></span> <span data-ttu-id="8f808-113">Если STATUS_VALIDATE_STATE не задано, не может выполнять динамической перенастройки.</span><span class="sxs-lookup"><span data-stu-id="8f808-113">If STATUS_VALIDATE_STATE is not set, you cannot perform dynamic reconfiguration.</span></span>
    
5. <span data-ttu-id="8f808-114">Если значение STATUS_SETTINGS_DIALOG, вызовите [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) , чтобы открыть окно свойств поставщика транспорта и пользователи могут вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="8f808-114">If STATUS_SETTINGS_DIALOG is set, call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the transport provider's property sheet and allow the user to make changes.</span></span> 
    
6. <span data-ttu-id="8f808-115">По окончании пользователя с перенастроить вызовите [IMAPIStatus::ValidateState](imapistatus-validatestate.md) , если задано STATUS_VALIDATE_STATE, передав CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="8f808-115">After the user has finished with the reconfiguration, call [IMAPIStatus::ValidateState](imapistatus-validatestate.md) if STATUS_VALIDATE_STATE is set, passing CONFIG_CHANGED.</span></span> 
    

