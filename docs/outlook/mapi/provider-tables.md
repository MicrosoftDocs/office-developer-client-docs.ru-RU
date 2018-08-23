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
ms.openlocfilehash: ccc51f33ff681021492949c2180fe70940157f4f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566140"
---
# <a name="provider-tables"></a>Таблицы поставщиков

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Таблица Поставщик содержит сведения о поставщиках услуг. Существует две таблицы другого поставщика, как реализуется MAPI и используемого клиентами. Первая таблица, доступного путем вызова метода [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) содержит сведения обо всех поставщиков для текущего профиля. Второй таблицу, доступ через [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)создается таблица, в которой хранятся сведения обо всех поставщиков услуг для службы сообщений.
  
Эти две таблицы иметь другой различие. В таблице поставщика, можно достичь **IMsgServiceAdmin::GetProviderTable** содержит только строки, представляющие поставщиков услуг, хотя можно достичь **IProviderAdmin::GetProviderTable** таблицы может содержать строк, представляющих Дополнительные сведения, связанные с поставщиком услуг. Эти дополнительные данные добавляется к профилю с ключевым словом «Раздела» MAPISVC.INF. Если поставщик разделах дополнительного профиля, его хранятся значения **MAPIUID** для этих разделов в свойстве **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** сохраняется в разделе сообщения службы профилей. 
  
Следующие свойства составляют обязательный столбец, задайте в обоих типов поставщика таблицы:
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
|**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
В таблице поставщика можно использовать для отображения текущего порядка транспорта, или измените его. Для отображения текущего порядка построения ограничения для извлечения только тех строк, свойство **PR_RESOURCE_TYPE** , равным MAPI_TRANSPORT_PROVIDER. Затем используйте **PR_PROVIDER_ORDINAL** как ключ сортировки для сортировки таблицы и извлечь все строки с помощью метода [IMAPITable::QueryRows](imapitable-queryrows.md) или функцию [HrQueryAllRows](hrqueryallrows.md) . 
  
Чтобы изменить порядок транспорта применяются одинаковые ограничения и извлечения строк. Затем создайте массив значений из свойства **PR_PROVIDER_UID** , который представляет уникальных идентификаторов для поставщиков транспорта. Когда идентификаторы в установленном порядке, передачи их в метод [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) . 
  
После таблицы поставщика были сделаны доступными, последующие изменения, такие как добавление или удаление поставщика будет отличаться.
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

