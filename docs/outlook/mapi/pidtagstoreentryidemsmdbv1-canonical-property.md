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
ms.openlocfilehash: 74626b735599a5f1485b26fcb65d907b552b3089
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811968"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>Каноническое свойство PidTagStoreEntryIdEmsmdbV1

  
  
**Относится к**: Outlook 
  
Содержит старый стиль (Microsoft Outlook 2002 и более ранних версий) идентификатор записи банка сообщений Microsoft Exchange Server 2010 или Exchange Server 2013.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Идентификатор:  <br/> |0x65F60102  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Идентификатор свойства  <br/> |
   
## <a name="remarks"></a>Замечания

Начиная с Microsoft Outlook 2003, полные доменные имена серверов были интегрированы в идентификаторы, тем самым позволяет избежать дополнительных RPC для ссылок. Тем не менее это делает запись идентификаторы больше времени и приводятся ссылки на дополнительные сценарии использования метода **CompareEntryIDs** для определения ли два запись идентификаторы эквивалентны. PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) свойство обращается к старый формат идентификатор записи Exchange Server, используемый с Microsoft Outlook 2002 (Microsoft Office XP) и более ранних версий. Это можно сохранить пространство и также сократить количество вызовов **CompareEntryIDs** , необходимо определить, когда запись идентификаторы эквивалентны. Обратите внимание, что с помощью более старые записи идентификаторов для открытия почтового ящика, могут вызвать некоторые дополнительные RPC Если ссылка является обязательным. 
  
Для доступа к свойству PR_STORE_ENTRYID_EMSMDB_V1 в режиме кэширования данных, необходимо обойти кэша, используя флаг MAPI_NO_CACHE с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) . Если **PR_STORE_ENTRYID_EMSMDB_V1** недоступен, код должен вернуться к PR_STORE_ENTRYID. Свойство PR_STORE_ENTRYID_EMSMDB_V1 поддерживается только в Outlook 2003 через Microsoft Outlook 2013. 
  
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

