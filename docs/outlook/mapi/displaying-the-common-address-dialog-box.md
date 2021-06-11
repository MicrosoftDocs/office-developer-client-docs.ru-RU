---
title: Отображение диалогового окна общего адреса
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
# <a name="displaying-the-common-address-dialog-box"></a>Отображение диалогового окна общего адреса

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Диалоговое окно общего адреса MAPI можно использовать для решения различных задач, таких как создание списка получателей. Чтобы отобразить диалоговое окно, позвоните **в IAddrBook::Address**. В зависимости от того, какой из множества параметров и как вы их заданы, вы можете ограничить отображение записей определенного типа из определенного контейнера.
  
 **Ограничение диалоговых окне адресов только отображением записей личной адресной книги (PAB)**
  
1. Вызов [IAddrBook::GetPAB](iaddrbook-getpab.md) для получения идентификатора записи PAB. 
    
2. Создайте ограничение свойств, RELOP_EQ для  повторного члена [структуры SPropertyRestriction](spropertyrestriction.md)  и PR_ENTRYID [(PidTagEntryId)](pidtagentryid-canonical-property.md)или **PR_AB_PROVIDER_ID** [(PidTagAbProviderId)](pidtagabproviderid-canonical-property.md)в качестве члена **ulPropTag.** Если вы используете **PR_ENTRYID,** передай идентификатор записи, извлеченный из **GetPAB.** Если вы используете **PR_AB_PROVIDER_ID,** передай значение, включенного в MSPAB. Файл заглавной папки H. **PR_AB_PROVIDER_ID** является уникальным идентификатором для PAB, разработанного MAPI. 
    
3. Вызов [IAddrBook::Address](iaddrbook-address.md) с параметром  _lpHierRestriction,_ указывающий на ограничение свойства. 
    

