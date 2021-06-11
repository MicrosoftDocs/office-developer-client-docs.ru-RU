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
ms.openlocfilehash: 2944a53d27bc916ccafcfa649d79e3c00afaf622
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412389"
---
# <a name="accessing-the-members-of-a-distribution-list"></a><span data-ttu-id="4572a-103">Доступ к участникам списка рассылки</span><span class="sxs-lookup"><span data-stu-id="4572a-103">Accessing the Members of a Distribution List</span></span>

  
  
<span data-ttu-id="4572a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4572a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4572a-105">**Чтобы получить участников списка рассылки**</span><span class="sxs-lookup"><span data-stu-id="4572a-105">**To get the members of a distribution list**</span></span>
  
1. <span data-ttu-id="4572a-106">Создайте массив тегов свойств размером с свойствами участников, которые вы хотите получить, например **PR_ENTRYID** [(PidTagEntryId),](pidtagentryid-canonical-property.md) **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)и **PR_DISPLAY_TYPE** [(PidTagDisplayType).](pidtagdisplaytype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="4572a-106">Create a sized property tag array with the properties of the members you would like to retrieve, such as **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), and **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="4572a-107">Вызов [IAddrBook::OpenEntry,](iaddrbook-openentry.md) чтобы открыть список рассылки.</span><span class="sxs-lookup"><span data-stu-id="4572a-107">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the distribution list.</span></span> 
    
3. <span data-ttu-id="4572a-108">Чтобы получить доступ к таблице содержимого, позвоните по методу **IABContainer::GetContentsTable.**</span><span class="sxs-lookup"><span data-stu-id="4572a-108">Call the distribution list's **IABContainer::GetContentsTable** method to access its contents table.</span></span> 
    
4. <span data-ttu-id="4572a-109">Позвоните [в HrQueryAllRows,](hrqueryallrows.md) чтобы получить все строки таблицы, представляющие участников списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="4572a-109">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all of the table's rows representing the members of the distribution list.</span></span> 
    

