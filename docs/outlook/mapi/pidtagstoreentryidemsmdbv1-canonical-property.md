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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит старый стиль (Microsoft Outlook 2002 и более ранних версий) идентификатора записи для Microsoft Exchange Server 2010 или Exchange Server 2013.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Идентификатор:  <br/> |0x65F60102  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Свойства ID  <br/> |
   
## <a name="remarks"></a>Примечания

Начиная с Microsoft Outlook 2003, FQDNs сервера были интегрированы в ИД записи, тем самым избегая дополнительных RPCs для ссылок. Однако это делает ИД записей длиннее и представляет дополнительные сценарии, в которых метод **CompareEntryIDs** должен использоваться для определения того, эквивалентны ли два ИД записей. Свойство PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) имеет доступ к старой версии ИД записи Exchange Server, используемой Microsoft Outlook 2002 (Microsoft Office XP) и более ранними версиями. Это позволяет сэкономить место, а также уменьшить количество вызовов **CompareEntryIDs,** необходимых для определения эквивалентных номеров записей. Обратите внимание, что при использовании более старых ИД записей для открытия почтового ящика могут возникнуть дополнительные функции проверки записей, если требуется получить ссылку. 
  
Чтобы получить доступ к PR_STORE_ENTRYID_EMSMDB_V1 в режиме кэширования, необходимо обойти кэш с помощью флага MAPI_NO_CACHE с методом [IMAPIProp::GetProps.](imapiprop-getprops.md) Если **PR_STORE_ENTRYID_EMSMDB_V1** нет, код должен вернуться к PR_STORE_ENTRYID. Свойство PR_STORE_ENTRYID_EMSMDB_V1 поддерживается только с Outlook 2003 по Microsoft Outlook 2013. 
  
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

