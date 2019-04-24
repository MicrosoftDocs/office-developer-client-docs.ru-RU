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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331243"
---
# <a name="accessing-the-members-of-a-distribution-list"></a><span data-ttu-id="c04dc-103">Доступ к участникам списка рассылки</span><span class="sxs-lookup"><span data-stu-id="c04dc-103">Accessing the Members of a Distribution List</span></span>

  
  
<span data-ttu-id="c04dc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c04dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="c04dc-105">**Получение списка участников списка рассылки**</span><span class="sxs-lookup"><span data-stu-id="c04dc-105">**To get the members of a distribution list**</span></span>
  
1. <span data-ttu-id="c04dc-106">Создайте массив тегов свойств с изменяемыми свойствами элементов, которые требуется извлечь, например **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) и **пр_дисплай_типе** ([ PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c04dc-106">Create a sized property tag array with the properties of the members you would like to retrieve, such as **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), and **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="c04dc-107">Call [IAddrBook:: OpenEntry](iaddrbook-openentry.md) , чтобы открыть список рассылки.</span><span class="sxs-lookup"><span data-stu-id="c04dc-107">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the distribution list.</span></span> 
    
3. <span data-ttu-id="c04dc-108">ВыЗовите метод **иабконтаинер:: жетконтентстабле** списка рассылки для доступа к своей таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="c04dc-108">Call the distribution list's **IABContainer::GetContentsTable** method to access its contents table.</span></span> 
    
4. <span data-ttu-id="c04dc-109">ВыЗовите [хркуеряллровс](hrqueryallrows.md) , чтобы получить все строки таблицы, представляющие участников списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="c04dc-109">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all of the table's rows representing the members of the distribution list.</span></span> 
    

