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
# <a name="accessing-the-members-of-a-distribution-list"></a>Доступ к участникам списка рассылки

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 **Чтобы получить участников списка рассылки**
  
1. Создайте массив тегов свойств размером с свойствами участников, которые вы хотите получить, например **PR_ENTRYID** [(PidTagEntryId),](pidtagentryid-canonical-property.md) **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)и **PR_DISPLAY_TYPE** [(PidTagDisplayType).](pidtagdisplaytype-canonical-property.md)
    
2. Вызов [IAddrBook::OpenEntry,](iaddrbook-openentry.md) чтобы открыть список рассылки. 
    
3. Чтобы получить доступ к таблице содержимого, позвоните по методу **IABContainer::GetContentsTable.** 
    
4. Позвоните [в HrQueryAllRows,](hrqueryallrows.md) чтобы получить все строки таблицы, представляющие участников списка рассылки. 
    

