---
title: Доступ к участникам списка рассылки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a32552343fa90dfbbb3571f50846976a5f5f5edd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595365"
---
# <a name="accessing-the-members-of-a-distribution-list"></a><span data-ttu-id="5ae1a-103">Доступ к участникам списка рассылки</span><span class="sxs-lookup"><span data-stu-id="5ae1a-103">Accessing the Members of a Distribution List</span></span>

  
  
<span data-ttu-id="5ae1a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ae1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="5ae1a-105">**Получение членов списка рассылки**</span><span class="sxs-lookup"><span data-stu-id="5ae1a-105">**To get the members of a distribution list**</span></span>
  
1. <span data-ttu-id="5ae1a-106">Создание массива тег размера свойства со свойствами для членов, которые вы хотите получить, такие как **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) и **PR_DISPLAY_TYPE** ([ PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5ae1a-106">Create a sized property tag array with the properties of the members you would like to retrieve, such as **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), and **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="5ae1a-107">Вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md) , чтобы открыть список рассылки.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-107">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the distribution list.</span></span> 
    
3. <span data-ttu-id="5ae1a-108">Вызов метода **IABContainer::GetContentsTable** списка рассылки для доступа к его содержимое в таблице.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-108">Call the distribution list's **IABContainer::GetContentsTable** method to access its contents table.</span></span> 
    
4. <span data-ttu-id="5ae1a-109">Вызовите [HrQueryAllRows](hrqueryallrows.md) , чтобы получить все строки в таблице, представляющее членов списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-109">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all of the table's rows representing the members of the distribution list.</span></span> 
    

