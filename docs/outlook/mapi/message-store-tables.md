---
title: Таблицы магазина сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dd28c146f6b05b2dea03f73fab7131f23ca99e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405354"
---
# <a name="message-store-tables"></a>Таблицы магазина сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В таблице хранения сообщений содержатся сведения о поставщиках хранения сообщений в текущем профиле. Существует одна таблица хранения сообщений для каждого сеанса MAPI, реализуемая MAPI и используемая клиентами. Клиенты могут использовать эту таблицу, например, чтобы найти все экземпляры конкретного поставщика или найти определенный магазин сообщений. 
  
Таблица хранения сообщений динамическая. Если пользователь клиентского приложения изменяет профиль, например, изменяя хранилище сообщений  по умолчанию, значения свойств PR_DEFAULT_STORE для затронутых магазинов сообщений немедленно обновляются. 
  
Клиенты получают доступ к таблице хранения сообщений, позвонив по [методу IMAPISession::GetMsgStoresTable.](imapisession-getmsgstorestable.md) 
  
Следующие свойства составляют необходимый столбец, установленный в таблице хранения сообщений:
  
|||
|:-----|:-----|
|**PR_DEFAULT_STORE** [(PidTagDefaultStore)](pidtagdefaultstore-canonical-property.md)  <br/> |**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |
|**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)  <br/> |**PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)  <br/> |
|**PR_MDB_PROVIDER** [(PidTagStoreProvider)](pidtagstoreprovider-canonical-property.md)  <br/> |**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)  <br/> |
|**PR_PROVIDER_DISPLAY** [(PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)  <br/> |**PR_RECORD_KEY** [(PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** [(PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)  <br/> |**PR_RESOURCE_TYPE** [(PidTagResourceType)](pidtagresourcetype-canonical-property.md)  <br/> |
   
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

