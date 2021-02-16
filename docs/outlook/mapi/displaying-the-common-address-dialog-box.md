---
title: Отображение диалоговых окна "Общий адрес"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 812c850d1fcb6d3712d76b160b56b839b2e1353d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436905"
---
# <a name="displaying-the-common-address-dialog-box"></a>Отображение диалоговых окна "Общий адрес"

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Диалоговое окно общего адреса MAPI можно использовать для различных задач, таких как создание списка получателей. Чтобы отобразить это диалоговое окно, вызовите **IAddrBook::Address.** В зависимости от того, какой из заданных параметров и как их настроить, можно ограничить отображение записями определенного типа из определенного контейнера.
  
 **Ограничение отображения в диалоговом окне адреса только записей личной адресной книги (PAB)**
  
1. Вызовите [IAddrBook::GetPAB,](iaddrbook-getpab.md) чтобы получить идентификатор записи для PAB. 
    
2. Создайте ограничение свойств, использующее  RELOP_EQ для повторного члена структуры [SPropertyRestriction](spropertyrestriction.md) и либо **PR_ENTRYID** ([PidTagEntryId),](pidtagentryid-canonical-property.md)либо **PR_AB_PROVIDER_ID** ([PidTagAbProviderId)](pidtagabproviderid-canonical-property.md)в качестве члена **ulPropTag.** Если вы используете **PR_ENTRYID,** передав идентификатор записи, полученный из **GetPAB.** Если вы используете **PR_AB_PROVIDER_ID,** передате значение, включенного в MSPAB. Файл h-загона. **PR_AB_PROVIDER_ID** это уникальный идентификатор для PAB, разработанного MAPI. 
    
3. Call [IAddrBook::Address](iaddrbook-address.md) with the  _lpHierRestriction_ parameter pointing to the property restriction. 
    

