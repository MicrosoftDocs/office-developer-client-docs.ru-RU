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
  
Таблица "поставщик" содержит сведения о поставщиках услуг. Существует две различные таблицы поставщиков, которые реализуются MAPI и используются клиентами. Первая таблица, доступная при вызове метода [имсгсервицеадмин:: жетпровидертабле](imsgserviceadmin-getprovidertable.md) , содержит сведения обо всех поставщиках для текущего профиля. Вторая таблица, доступная с помощью [ипровидерадмин:: жетпровидертабле](iprovideradmin-getprovidertable.md), создает таблицу, в которой хранятся сведения обо всех поставщиках услуг для службы сообщений.
  
Эти две таблицы имеют другое отличие. Таблица поставщика доступна через **имсгсервицеадмин:: жетпровидертабле** содержит только строки, представляющие поставщиков услуг, а таблица, доступная через **Ипровидерадмин:: жетпровидертабле** могут включать строки, представляющие Дополнительные сведения, связанные с поставщиком услуг. Эти дополнительные сведения добавляются в профиль с помощью ключевого слова "sections" MAPISVC. INF. Когда поставщик имеет дополнительные разделы профиля, он сохраняет значения **мапиуид** для этих разделов в свойстве **пр_сервице_екстра_уидс** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **Пр_сервице_екстра_уидс** сохраняется в разделе "профиль службы сообщений". 
  
Следующие свойства составляют обязательный набор столбцов в обоих типах таблиц поставщиков:
  
|||
|:-----|:-----|
|**Пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**Пр_провидер_дисплай** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**Пр_провидер_длл_наме** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**Пр_провидер_ординал** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**Пр_провидер_уид** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))  <br/> |
|**Пр_ресаурце_флагс** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**Пр_ресаурце_типе** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
|**Пр_сервице_наме** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**Пр_сервице_уид** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
Таблица поставщик может использоваться для отображения текущего транспортного заказа или его изменения. Чтобы отобразить текущий заказ, создайте ограничение для извлечения только тех строк, у которых для свойства **пр_ресаурце_типе** задано значение мапи_транспорт_провидер. Затем используйте **пр_провидер_ординал** в качестве ключа сортировки для сортировки таблицы и получения всех строк с помощью метода [IMAPITable:: QueryRows](imapitable-queryrows.md) или [хркуеряллровс](hrqueryallrows.md) . 
  
Чтобы изменить транспортный заказ, примените то же ограничение и извлеките строки. Затем создайте массив значений из свойства **пр_провидер_уид** , представляющего уникальные идентификаторы для поставщиков транспорта. Когда идентификаторы находятся в нужном порядке, передайте их методу [имсгсервицеадмин:: мсгсервицетранспортордер](imsgserviceadmin-msgservicetransportorder.md) . 
  
После того как таблица поставщика станет доступной, она не будет отражать последующие изменения, такие как добавление или удаление поставщика.
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

