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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к таблице поставщиков, списку поставщиков услуг в профиле.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Всегда NULL.
    
 _lppTable_
  
> [вышел] Указатель на указатель на таблицу поставщика.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица поставщика успешно возвращена.
    
## <a name="remarks"></a>Примечания

Метод **IMsgServiceAdmin::GetProviderTable** предоставляет доступ к таблице поставщика MAPI, таблице, в которую перечислены все адресная книга, хранилище сообщений и поставщики транспорта, установленные в профиле. 
  
В отличие от таблицы поставщиков, возвращаемой с помощью метода [IProviderAdmin::GetProviderTable,](iprovideradmin-getprovidertable.md) таблица поставщиков, возвращаемая через **IMsgServiceAdmin::GetProviderTable,** не может включать дополнительные строки, которые представляют сведения, связанные с одним или более поставщиками услуг в профиле. 
  
Поставщики, которые были удалены или используются, но помечены для удаления, не включены в таблицу поставщиков. Таблицы поставщиков являются статичными, что означает, что последующие добавления или удаления из профиля не отражаются в таблице. 
  
Если в профиле нет поставщиков, **GetProviderTable** возвращает таблицу с нулевыми строками и S_OK возвращается. 
  
Полный список столбцов в таблице поставщиков см. в [статье Provider Table.](provider-tables.md) 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы получить строки таблицы поставщика в транспортном порядке, используйте следующую процедуру:
  
1. Вызывай метод [IMAPITable::Restrict,](imapitable-restrict.md) чтобы ввести ограничение свойства, которое соответствует свойству **PR_RESOURCE_TYPE** [(PidTagResourceType)](pidtagresourcetype-canonical-property.md)с MAPI_TRANSPORT_PROVIDER.
    
2. Вызов метода [IMAPITable::SortTable](imapitable-sorttable.md) **для** сортировки таблицы столбцом [PR_PROVIDER_ORDINAL (PidTagProviderOrdinal).](pidtagproviderordinal-canonical-property.md) 
    
3. Чтобы получить строки таблицы, позвоните по методу [IMAPITable::QueryRows.](imapitable-queryrows.md) 
    
Альтернативой этим вызовам является один вызов функции [HrQueryAllRows](hrqueryallrows.md) со всеми соответствующими структурами данных. 
  
Если вы извлекаете **столбцы PR_SERVICE_UID** [(PidTagServiceUid)](pidtagserviceuid-canonical-property.md)в каждой строке, вы можете использовать этот массив структур **MAPIUID,** чтобы установить порядок транспорта в вызове [в IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Настройка флага MAPI_UNICODE в  _параметре ulFlags_ делает следующее: 
  
- Задает тип строки в Unicode для данных, возвращаемых для начальных активных столбцов таблицы поставщиков методом [IMAPITable::QueryColumns.](imapitable-querycolumns.md) Начальными активными столбцами для таблицы поставщиков являются те столбцы, которые метод **QueryColumns** возвращает перед поставщиком, который содержит таблицу, вызывает метод [IMAPITable::SetColumns.](imapitable-setcolumns.md) 
    
- Задает тип строки в Unicode для данных, возвращаемой для начальных активных строк таблицы поставщиков **в QueryRows.** Начальные активные строки для таблицы поставщиков — это те строки, которые **возвращаются в QueryRows** перед поставщиком, который содержит таблицу **вызовов SetColumns.** 
    
- Управляет типами свойств порядка сортировки, возвращаемым методом [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) перед клиентом, который содержит таблицу поставщиков, вызывает метод [IMAPITable::SortTable.](imapitable-sorttable.md) 
    
## <a name="see-also"></a>См. также



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

