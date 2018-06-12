---
title: Доступ к членам списка рассылки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 21975482c458998cbe158a84d535f911156ac392
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808012"
---
# <a name="accessing-the-members-of-a-distribution-list"></a><span data-ttu-id="2aeb9-103">Доступ к членам списка рассылки</span><span class="sxs-lookup"><span data-stu-id="2aeb9-103">Accessing the Members of a Distribution List</span></span>

  
  
<span data-ttu-id="2aeb9-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2aeb9-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="2aeb9-105">**Получение членов списка рассылки**</span><span class="sxs-lookup"><span data-stu-id="2aeb9-105">**To get the members of a distribution list**</span></span>
  
1. <span data-ttu-id="2aeb9-106">Создание массива тег размера свойства со свойствами для членов, которые вы хотите получить, такие как **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) и **PR_DISPLAY_TYPE** ([ PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2aeb9-106">Create a sized property tag array with the properties of the members you would like to retrieve, such as **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), and **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="2aeb9-107">Вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md) , чтобы открыть список рассылки.</span><span class="sxs-lookup"><span data-stu-id="2aeb9-107">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the distribution list.</span></span> 
    
3. <span data-ttu-id="2aeb9-108">Вызов метода **IABContainer::GetContentsTable** списка рассылки для доступа к его содержимое в таблице.</span><span class="sxs-lookup"><span data-stu-id="2aeb9-108">Call the distribution list's **IABContainer::GetContentsTable** method to access its contents table.</span></span> 
    
4. <span data-ttu-id="2aeb9-109">Вызовите [HrQueryAllRows](hrqueryallrows.md) , чтобы получить все строки в таблице, представляющее членов списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="2aeb9-109">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all of the table's rows representing the members of the distribution list.</span></span> 
    

