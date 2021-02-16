---
title: IMsgServiceAdminGetProviderTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetProviderTable
api_type:
- COM
ms.assetid: 7180bff2-91ad-4e11-923e-2a9acefa3215
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1185a35df471fc3f85cbf50fd8ad3baa3927e72b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428769"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к таблице поставщиков, перечислению поставщиков услуг в профиле.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Всегда NULL.
    
 _lppTable_
  
> [out] Указатель на указатель на таблицу поставщика.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица поставщика успешно возвращена.
    
## <a name="remarks"></a>Примечания

Метод **IMsgServiceAdmin::GetProviderTable** предоставляет доступ к таблице поставщиков MAPI, которая содержит список всех поставщиков адресной книги, хранилище сообщений и поставщиков транспорта, установленных в данный момент в профиле. 
  
В отличие от таблицы поставщика, возвращаемой методом [IProviderAdmin::GetProviderTable,](iprovideradmin-getprovidertable.md) таблица поставщиков, возвращаемая с помощью **IMsgServiceAdmin::GetProviderTable,** не может включать дополнительные строки, которые представляют сведения, связанные с одним или более поставщиками служб в профиле. 
  
Поставщики, которые были удалены или используются, но помечены для удаления, не включаются в таблицу поставщиков. Таблицы поставщиков являются статическими, то есть последующие добавления или удаления из профиля не отражаются в таблице. 
  
Если в профиле нет поставщиков, **GetProviderTable** возвращает таблицу с нулевыми строками, а значение S_OK значение. 
  
Полный список столбцов в таблице поставщиков см. в [таблице поставщиков.](provider-tables.md) 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы получить строки таблицы поставщика в порядке транспорта, используйте следующую процедуру:
  
1. Вызовите метод [IMAPITable::Restrict,](imapitable-restrict.md) чтобы наложить ограничение свойства, которое соответствует свойству **PR_RESOURCE_TYPE** ([PidTagResourceType)](pidtagresourcetype-canonical-property.md)с MAPI_TRANSPORT_PROVIDER.
    
2. Вызовите метод [IMAPITable::SortTable](imapitable-sorttable.md) для сортировки таблицы по столбце **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal).](pidtagproviderordinal-canonical-property.md) 
    
3. Вызовите [метод IMAPITable::QueryRows,](imapitable-queryrows.md) чтобы получить строки таблицы. 
    
Альтернативой этим вызовам является один вызов функции [HrQueryAllRows](hrqueryallrows.md) со всеми соответствующими структурами данных. 
  
При извлечении столбцов **PR_SERVICE_UID** ([PidTagServiceUid)](pidtagserviceuid-canonical-property.md)в каждой строке можно использовать этот массив структур **MAPIUID,** чтобы настроить порядок транспорта в вызове [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Установка флага MAPI_UNICODE в  _параметре ulFlags_ делает следующее: 
  
- Задает тип строки Юникод для данных, возвращаемых для начальных активных столбцов таблицы поставщиков методом [IMAPITable::QueryColumns.](imapitable-querycolumns.md) Начальные активные столбцы для таблицы поставщиков — это те столбцы, которые метод **QueryColumns** возвращает перед тем, как поставщик, содержащий таблицу, вызывает метод [IMAPITable::SetColumns.](imapitable-setcolumns.md) 
    
- Задает тип строки Юникод для данных, возвращаемого для начальных активных строк таблицы поставщика **queryRows.** Начальные активные строки для таблицы поставщиков — это строки, которые **QueryRows** возвращает перед тем, как поставщик, содержащий таблицу, вызывает **SetColumns.** 
    
- Управляет типами свойств порядка сортировки, возвращаемого методом [IMAPITable::QuerySortOrder,](imapitable-querysortorder.md) перед тем как клиент, содержащий таблицу поставщика, вызывает метод [IMAPITable::SortTable.](imapitable-sorttable.md) 
    
## <a name="see-also"></a>См. также



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

