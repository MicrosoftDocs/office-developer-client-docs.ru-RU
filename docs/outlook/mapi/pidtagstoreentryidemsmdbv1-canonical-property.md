---
title: Каноническое свойство PidTagStoreEntryIdEmsmdbV1
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c8bccbfeb7f04745a66831618deff490bc651b02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415154"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>Каноническое свойство PidTagStoreEntryIdEmsmdbV1

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит старый стиль (Microsoft Outlook 2002 и более ранние версии) идентификатора записи магазина сообщений Microsoft Exchange Server 2010 или Exchange Server 2013 года.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Идентификатор:  <br/> |0x65F60102  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Свойства ID  <br/> |
   
## <a name="remarks"></a>Примечания

Начиная с Microsoft Outlook 2003 г. серверные FQDNs были интегрированы в ID-документы записи, что позволяет избежать дополнительных RPCs для рефералов. Тем не менее, это делает ID записи длиннее и вводит больше сценариев, в которых метод **CompareEntryIDs** должен быть использован, чтобы определить, эквивалентны ли два ID записи. Свойство PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) имеет доступ к более старшему формату ID записи Exchange Server, используемого Microsoft Outlook 2002 (Microsoft Office XP) и более ранних версий. Это позволяет сэкономить пространство, а также уменьшить количество вызовов **CompareEntryIDs,** необходимых для определения эквивалентных ID-данных входа. Обратите внимание, что с помощью более старых ID-адресов записи для открытия почтового ящика могут возникнуть дополнительные RPCs, если требуется направление. 
  
Чтобы получить доступ PR_STORE_ENTRYID_EMSMDB_V1 в кэшировом режиме, необходимо обойти кэш с помощью флага MAPI_NO_CACHE с помощью [метода IMAPIProp::GetProps.](imapiprop-getprops.md) Если **PR_STORE_ENTRYID_EMSMDB_V1** не доступен, код должен вернуться к PR_STORE_ENTRYID. Только Outlook 2003 Microsoft Outlook 2013 поддерживают PR_STORE_ENTRYID_EMSMDB_V1 свойства. 
  
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

