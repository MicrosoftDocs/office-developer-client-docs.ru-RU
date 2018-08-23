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
# <a name="accessing-the-members-of-a-distribution-list"></a>Доступ к участникам списка рассылки

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
 **Получение членов списка рассылки**
  
1. Создание массива тег размера свойства со свойствами для членов, которые вы хотите получить, такие как **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) и **PR_DISPLAY_TYPE** ([ PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
    
2. Вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md) , чтобы открыть список рассылки. 
    
3. Вызов метода **IABContainer::GetContentsTable** списка рассылки для доступа к его содержимое в таблице. 
    
4. Вызовите [HrQueryAllRows](hrqueryallrows.md) , чтобы получить все строки в таблице, представляющее членов списка рассылки. 
    

