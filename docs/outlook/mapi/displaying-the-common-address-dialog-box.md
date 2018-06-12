---
title: Отображение стандартным диалоговым окном адрес
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: a7b603504956be9ec3066e5ff5e1d5db7d59852a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808338"
---
# <a name="displaying-the-common-address-dialog-box"></a>Отображение стандартным диалоговым окном адрес

  
  
**Применимо к**: Outlook 
  
Диалоговое окно MAPI распространенных адрес может использоваться для различных адресации задачи, такие как создание списка получателей. Чтобы отобразить это диалоговое окно, вызовите **IAddrBook::Address**. В зависимости от того, какой из много параметров, заданную вами и как задать можно ограничить экрана записи определенного типа из конкретного контейнера.
  
 **Чтобы ограничить поле адрес для отображения только запись адресной книги (адресной книги)**
  
1. Вызовите [IAddrBook::GetPAB](iaddrbook-getpab.md) , чтобы получить идентификатор записи личной адресной книги. 
    
2. Создание ограничение свойство, которое использует RELOP_EQ для элемента **relop** структура [SPropertyRestriction](spropertyrestriction.md) и **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) или **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) в качестве член **ulPropTag** . Если вы используете **PR_ENTRYID**, передайте идентификатор записи, извлекается из **GetPAB**. Если вы используете **PR_AB_PROVIDER_ID**, передайте значение, включенные в MSPAB. Файл заголовка. **PR_AB_PROVIDER_ID** — уникальный идентификатор для адресной книги, разработанная MAPI. 
    
3. Вызов [IAddrBook::Address](iaddrbook-address.md) совместно с параметром _lpHierRestriction_ с указанием ограничении свойства. 
    

