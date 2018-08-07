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
ms.openlocfilehash: 4272edef5b1b72944d1d27f0e4dd99ee4956aa57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809352"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**Относится к**: Outlook 
  
Предоставляет доступ к таблице поставщика список поставщиков услуг в профиле.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Всегда имеет значение NULL.
    
 _lppTable_
  
> [out] Указатель на указатель в таблице поставщика.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> В таблице поставщика успешно возвращен.
    
## <a name="remarks"></a>Замечания

Метод **IMsgServiceAdmin::GetProviderTable** предоставляет доступ к таблице поставщика MAPI, таблица, перечисляющая адресной книги, хранилища сообщений и поставщиками транспорта, установленным в профиле. 
  
В отличие от поставщика таблицы, возвращенные с помощью метода [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) в таблице поставщика, возвращаемых при **IMsgServiceAdmin::GetProviderTable** не может содержать дополнительные строки, которые представляют сведения, связанные с помощью одного или нескольких поставщиков услуг в профиле. 
  
Поставщики, которые были удалены, или используется, но помечены для удаления, не включаются в таблице поставщика. Поставщик таблиц являются статическими, что означает, что последующего добавления или удаления из профиля, не отражаются в таблице. 
  
Если профиль не поставщиков, **GetProviderTable** возвращает таблицу с нуля строк и возвращаемое значение S_OK. 
  
Полный список столбцов в таблице поставщика в разделе [Поставщик в таблице](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Для получения строк таблицы поставщика в порядке транспорта, используйте следующую процедуру:
  
1. Вызовите метод [IMAPITable::Restrict](imapitable-restrict.md) , чтобы наложить ограничение свойство, которое соответствует свойства **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) с MAPI_TRANSPORT_PROVIDER.
    
2. Вызовите метод [IMAPITable::SortTable](imapitable-sorttable.md) , используемый для сортировки в таблице в столбце **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
    
3. Вызовите метод [IMAPITable::QueryRows](imapitable-queryrows.md) для получения строки в таблице. 
    
Альтернативой эти вызовы является сделать одного вызова функции [HrQueryAllRows](hrqueryallrows.md) со всеми структуры, передаются в соответствующие данные. 
  
При извлечении **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) столбцов в каждой из строк, чтобы установить порядок транспорта в вызове [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)можно использовать этот массив структур **MAPIUID** .
  
Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ выполняет следующие действия: 
  
- Задает тип string в Юникод для данных, возвращенный методом [IMAPITable::QueryColumns](imapitable-querycolumns.md) для начальной active столбцов в таблице поставщика. Начальное active столбцы для таблицы поставщика — это столбцы, возвращаемый методом **QueryColumns** перед поставщика, который содержит метод [IMAPITable::SetColumns](imapitable-setcolumns.md) вызовов в таблице. 
    
- Задает тип string в Юникод для данных, возвращаемых **QueryRows**для начальной активных строк в таблице поставщика. Начальное active строк для поставщика таблицы, строки, **QueryRows** возвращает перед поставщика, который содержит таблицы вызовы **метода SetColumns**. 
    
- Элементы управления типы свойств порядок сортировки, возвращенный методом [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) перед клиента с таблицей поставщик вызывает метод [IMAPITable::SortTable](imapitable-sorttable.md) . 
    
## <a name="see-also"></a>См. также



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

