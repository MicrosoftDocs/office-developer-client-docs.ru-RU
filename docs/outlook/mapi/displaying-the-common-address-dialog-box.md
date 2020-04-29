---
title: Отображение диалогового окна "общий адрес"
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
# <a name="displaying-the-common-address-dialog-box"></a>Отображение диалогового окна "общий адрес"

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Диалоговое окно Общий адрес MAPI можно использовать для выполнения различных задач адресации, таких как создание списка получателей. Для отображения этого диалогового окна вызовите **IAddrBook:: Address**. В зависимости от того, какой из множества параметров задается и как вы их устанавливаете, вы можете ограничить отображение записями определенного типа в определенном контейнере.
  
 **Чтобы ограничить диалоговое окно "адрес" Отображение только записей личной адресной книги (PAB)**
  
1. Call [IAddrBook:: жетпаб](iaddrbook-getpab.md) для получения идентификатора записи личной адресной книги. 
    
2. Создайте ограничение свойства, использующее RELOP_EQ для элемента **релоп** структуры [спропертирестриктион](spropertyrestriction.md) и либо **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), либо **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) в качестве члена **улпроптаг** . При использовании **PR_ENTRYID**передайте идентификатор записи, полученный из **жетпаб**. При использовании **PR_AB_PROVIDER_ID**передайте значение, включенное в мспаб. H файл заголовка. **PR_AB_PROVIDER_ID** — это уникальный идентификатор личной адресной книги, разработанной MAPI. 
    
3. Call [IAddrBook:: Address](iaddrbook-address.md) с параметром _лфиеррестриктион_ , указывающий на ограничение свойства. 
    

