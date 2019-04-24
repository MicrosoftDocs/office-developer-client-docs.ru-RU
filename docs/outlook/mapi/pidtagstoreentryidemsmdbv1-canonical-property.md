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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278773"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>Каноническое свойство PidTagStoreEntryIdEmsmdbV1

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит старый стиль (Microsoft Outlook 2002 и более ранние версии) идентификатора записи для хранилища сообщений Microsoft Exchange Server 2010 или Exchange Server 2013.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Идентификатор:  <br/> |0x65F60102  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Свойства идентификатора  <br/> |
   
## <a name="remarks"></a>Замечания

Начиная с Microsoft Outlook 2003, полные доменные имена сервера были интегрированы в идентификаторы записей, что позволяет избежать дополнительных вызовов RPC для ссылок. Тем не менее, это делает идентификаторы записей более длинными и вводит дополнительные сценарии, в которых метод **метод compareentryids** должен использоваться для определения того, эквивалентны ли два идентификатора записи. Свойство PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) получает доступ к старому формату идентификатора записи Exchange Server, используемого Microsoft Outlook 2002 (Microsoft Office XP) и более ранних версий. Это может сэкономить место, а также сократить количество вызовов **метод compareentryids** , необходимых для определения того, когда идентификаторы записей эквивалентны. Обратите внимание на то, что использование старых идентификаторов записей для открытия почтового ящика может привести к дополнительным RPC, если требуется ссылка. 
  
Чтобы получить доступ к свойству PR_STORE_ENTRYID_EMSMDB_V1 в режиме кэширования, необходимо обойти кэш с помощью флага МАПИ_НО_КАЧЕ с методом [IMAPIProp::](imapiprop-getprops.md) GetProperty. Если **PR_STORE_ENTRYID_EMSMDB_V1** недоступен, код должен ВОЗВРАЩАТЬСЯ к пр_сторе_ентрид. Свойство PR_STORE_ENTRYID_EMSMDB_V1 поддерживается только для Outlook 2003 с помощью Microsoft Outlook 2013. 
  
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

