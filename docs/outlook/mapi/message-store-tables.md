---
title: Таблицы хранилища сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 735c778cd8e6ccb41de3d3d8cb0fdc163493f712
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572020"
---
# <a name="message-store-tables"></a>Таблицы хранилища сообщений

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
В таблице хранилища сообщений содержит сведения о поставщиках хранилища сообщений текущего профиля. Для каждого сеанса MAPI, реализованный MAPI и используемого клиентами имеется одна таблица хранилища сообщений. Клиенты могут использовать этой таблице, например, для поиска всех экземпляров определенного поставщика или найти конкретное сообщение хранилища. 
  
В таблице хранилища сообщений динамических. Если пользователь клиентское приложение изменяет профиль, изменение хранилища сообщений по умолчанию, например, значения **PR_DEFAULT_STORE** свойства для хранилищ затронутых сообщения сразу же обновляются. 
  
Для доступа клиентов к таблице хранилища сообщений путем вызова метода [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) . 
  
Следующие свойства составляют обязательный столбец, задайте в таблице хранилища сообщений:
  
|||
|:-----|:-----|
|**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

