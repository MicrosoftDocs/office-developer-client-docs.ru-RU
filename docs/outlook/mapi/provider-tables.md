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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Таблица поставщиков содержит сведения о поставщиках услуг. Существуют две разные таблицы поставщиков, которые реализованы MAPI и используются клиентами. В первой таблице, к которую можно получить доступ с помощью метода [IMsgServiceAdmin::GetProviderTable,](imsgserviceadmin-getprovidertable.md) содержится информация обо всех поставщиках текущего профиля. Вторая таблица, доступная через [IProviderAdmin::GetProviderTable,](iprovideradmin-getprovidertable.md)создает таблицу, которая хранит сведения обо всех поставщиках услуг для службы сообщений.
  
Эти две таблицы имеют другое отличие. Таблица поставщиков, доступная через **IMsgServiceAdmin::GetProviderTable,** содержит только строки, которые представляют поставщиков услуг, в то время как таблица, доступная через **IProviderAdmin::GetProviderTable,** может включать строки, которые представляют дополнительные сведения, связанные с поставщиком услуг. Эта дополнительная информация добавляется в профиль с ключевым словом "Разделы" MAPISVC.INF. Если у поставщика есть дополнительные разделы профилей, он сохраняет значения **MAPIUID** для этих разделов в **свойстве** [PR_SERVICE_EXTRA_UIDS (PidTagServiceExtraUids).](pidtagserviceextrauids-canonical-property.md) **PR_SERVICE_EXTRA_UIDS** сохранена в разделе профиль службы сообщений. 
  
Следующие свойства составляют необходимый столбец, установленный в обоих типах таблиц поставщиков:
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)  <br/> |**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |
|**PR_PROVIDER_DISPLAY** [(PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)  <br/> |**PR_PROVIDER_DLL_NAME** [(PidTagProviderDllName)](pidtagproviderdllname-canonical-property.md)  <br/> |
|**PR_PROVIDER_ORDINAL** [(PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID** [(PidTagProviderUid)](pidtagprovideruid-canonical-property.md)  <br/> |
|**PR_RESOURCE_FLAGS** [(PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)  <br/> |**PR_RESOURCE_TYPE** [(PidTagResourceType)](pidtagresourcetype-canonical-property.md)  <br/> |
|**PR_SERVICE_NAME** [(PidTagServiceName)](pidtagservicename-canonical-property.md)  <br/> |**PR_SERVICE_UID** [(PidTagServiceUid)](pidtagserviceuid-canonical-property.md)  <br/> |
   
Таблица поставщика может использоваться для отображения текущего порядка транспорта или его изменения. Чтобы отобразить текущий порядок, создайте  ограничение, чтобы получить только эти строки с PR_RESOURCE_TYPE для MAPI_TRANSPORT_PROVIDER. Затем используйте **PR_PROVIDER_ORDINAL** в качестве сортировки для сортировки таблицы и получения всех строк с помощью метода [IMAPITable::QueryRows](imapitable-queryrows.md) или [функции HrQueryAllRows.](hrqueryallrows.md) 
  
Чтобы изменить порядок транспорта, применяем те же ограничения и извлекаем строки. Затем создайте массив значений из свойства **PR_PROVIDER_UID,** которое представляет уникальные идентификаторы для поставщиков транспорта. Если идентификаторы находятся в нужном порядке, передайте их методу [IMsgServiceAdmin::MsgServiceTransportOrder.](imsgserviceadmin-msgservicetransportorder.md) 
  
После того как таблица поставщика будет доступна, она не будет отражать последующие изменения, такие как добавление или удаление поставщика.
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

