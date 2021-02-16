---
title: Таблицы поставщиков
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2b81f4aebae692d28ed492df102d59ba34debf63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408973"
---
# <a name="provider-tables"></a>Таблицы поставщиков

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Таблица поставщиков содержит сведения о поставщиках услуг. Существует две разные таблицы поставщиков, которые реализованы с помощью MAPI и используются клиентами. Первая таблица, доступная с помощью вызова метода [IMsgServiceAdmin::GetProviderTable,](imsgserviceadmin-getprovidertable.md) содержит сведения обо всех поставщиках для текущего профиля. Вторая таблица, доступная через [IProviderAdmin::GetProviderTable,](iprovideradmin-getprovidertable.md)создает таблицу, которая хранит сведения обо всех поставщиках служб для службы сообщений.
  
Эти две таблицы отличаются друг от друга. Таблица поставщика, доступная в **IMsgServiceAdmin::GetProviderTable,** содержит только строки, которые представляют поставщиков услуг, а таблица, доступная через **IProviderAdmin::GetProviderTable,** может включать строки, которые представляют дополнительные сведения, связанные с поставщиком услуг. Эти дополнительные сведения добавляются в профиль с ключевым словом "Sections" MAPISVC.INF. Если у поставщика есть дополнительные разделы профиля, он сохраняет значения **MAPIUID** для этих разделов в свойстве **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids).](pidtagserviceextrauids-canonical-property.md) **PR_SERVICE_EXTRA_UIDS** в разделе профиля службы сообщений. 
  
Следующие свойства составляют необходимый набор столбцов в таблицах поставщиков обоих типов:
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal)](pidtagproviderordinal-canonical-property.md)  <br/> |**PR_PROVIDER_UID** ([PidTagProviderUid)](pidtagprovideruid-canonical-property.md)  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType)](pidtagresourcetype-canonical-property.md)  <br/> |
|**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid)](pidtagserviceuid-canonical-property.md)  <br/> |
   
Таблицу поставщика можно использовать для отображения текущего порядка транспорта или ее изменения. Чтобы отобразить текущий порядок, создайте ограничение, чтобы получить только те строки, **для** PR_RESOURCE_TYPE свойству MAPI_TRANSPORT_PROVIDER. Затем используйте **PR_PROVIDER_ORDINAL** в качестве ключа сортировки для сортировки таблицы и получения всех строк с помощью метода [IMAPITable::QueryRows](imapitable-queryrows.md) или [функции HrQueryAllRows.](hrqueryallrows.md) 
  
Чтобы изменить порядок транспорта, применив такое же ограничение и извлекая строки. Затем создайте массив значений из свойства **PR_PROVIDER_UID,** которое представляет уникальные идентификаторы для поставщиков транспорта. Когда идентификаторы находятся в нужном порядке, передайте их методу [IMsgServiceAdmin::MsgServiceTransportOrder.](imsgserviceadmin-msgservicetransportorder.md) 
  
После того как таблица поставщика станет доступной, она не будет отражать последующие изменения, такие как добавление или удаление поставщика.
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

