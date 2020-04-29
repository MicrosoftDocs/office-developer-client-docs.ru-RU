---
title: имсгсервицеадминжетпровидертабле
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
  
Предоставляет доступ к таблице поставщика, в которой перечислены поставщики служб в профиле.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Всегда имеет значение NULL.
    
 _лпптабле_
  
> вышли Указатель на указатель на таблицу поставщика.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица поставщика успешно возвращена.
    
## <a name="remarks"></a>Примечания

Метод **имсгсервицеадмин:: жетпровидертабле** предоставляет доступ к таблице поставщика MAPI, таблице, в которой перечислены все адресные книги, хранилища сообщений и поставщики транспорта, установленные в профиле. 
  
В отличие от таблицы поставщика, возвращаемой с помощью метода [ипровидерадмин:: жетпровидертабле](iprovideradmin-getprovidertable.md) , таблица поставщика, возвращенная с помощью **Имсгсервицеадмин:: жетпровидертабле** не может включать дополнительные строки, которые представляют информацию, связанную с одним или несколькими поставщиками услуг в профиле. 
  
Поставщики, которые были удалены или используются, но помечены для удаления, не включаются в таблицу поставщика. Таблицы поставщика являются статическими, что означает, что последующие добавления или удаления из профиля не отражаются в таблице. 
  
Если у профиля нет поставщиков, **жетпровидертабле** возвращает таблицу с нулевыми строками и возвращаемое значение S_OK. 
  
Полный список столбцов таблицы поставщик представлен в разделе [таблица поставщиков](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы получить строки таблицы поставщика в порядке транспорта, используйте следующую процедуру:
  
1. Вызовите метод [IMAPITable:: restrict](imapitable-restrict.md) , чтобы применить ограничение свойства, которое соответствует свойству **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) с MAPI_TRANSPORT_PROVIDER.
    
2. Вызовите метод [IMAPITable:: сорттабле](imapitable-sorttable.md) , чтобы отсортировать таблицу по столбцу **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
    
3. Вызовите метод [IMAPITable:: QueryRows](imapitable-queryrows.md) , чтобы получить строки таблицы. 
    
В качестве альтернативы этим вызовам можно выполнить один вызов функции [хркуеряллровс](hrqueryallrows.md) со всеми соответствующими структурами данных. 
  
При получении столбцов **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) в каждой строке можно использовать этот массив структур **мапиуид** , чтобы установить порядок транспорта в вызове [имсгсервицеадмин:: мсгсервицетранспортордер](imsgserviceadmin-msgservicetransportorder.md).
  
Установка флага MAPI_UNICODE в параметре _ulFlags_ выполняет следующие действия: 
  
- Задает тип строки Юникод для данных, возвращаемых для начальных активных столбцов таблицы поставщика, с помощью метода [IMAPITable:: куериколумнс](imapitable-querycolumns.md) . Исходные активные столбцы для таблицы поставщика — это столбцы, возвращаемые методом **куериколумнс** , прежде чем поставщик, содержащий таблицу, вызывает метод [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) . 
    
- Задает тип строки Юникод для данных, возвращаемых для начальных активных строк таблицы поставщика, с помощью **QueryRows**. Исходные активные строки для таблицы поставщика — это строки, возвращаемые **QueryRows** до того, как поставщик, содержащий таблицу, вызывает **метода SetColumns**. 
    
- Управляет типами свойств порядка сортировки, возвращаемого методом [IMAPITable:: куерисортордер](imapitable-querysortorder.md) перед тем, как клиент, содержащий таблицу поставщика, вызывает метод [IMAPITable:: сорттабле](imapitable-sorttable.md) . 
    
## <a name="see-also"></a>См. также



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

