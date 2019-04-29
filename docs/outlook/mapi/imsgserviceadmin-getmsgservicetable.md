---
title: Имсгсервицеадминжетмсгсервицетабле
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetMsgServiceTable
api_type:
- COM
ms.assetid: 064dd5ca-0108-4045-b17b-0bb29cb93346
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fcaebb96d4dca4e6bfbee7491dabeafcbd93a2eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410478"
---
# <a name="imsgserviceadmingetmsgservicetable"></a>IMsgServiceAdmin::GetMsgServiceTable

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к таблице службы сообщений, списку служб сообщений в профиле.
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Всегда имеет значение NULL.
    
 _Лпптабле_
  
> вышли Указатель на указатель на таблицу службы сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица службы сообщений успешно возвращена.
    
## <a name="remarks"></a>Примечания

Метод **имсгсервицеадмин:: жетмсгсервицетабле** предоставляет доступ к таблице службы сообщений, таблице, которую поддерживает MAPI, в которой перечислены службы сообщений, установленные в профиле сеанса. Полный список столбцов таблицы служба сообщений приведен в разделе [Таблица службы сообщений](message-service-tables.md).
  
Таблица службы сообщений является статической. После того как клиенту будет предоставлен доступ к нему, последующие добавления и удаления службы сообщений не повлияют на нее. Если в текущем профиле нет служб сообщений, **жетмсгсервицетабле** возвращает таблицу с нулевыми строками. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мсгсервицетабледлг. cpp  <br/> |Кмсгсервицетабледлг:: Онрефрешвиев  <br/> |MFCMAPI использует метод **имсгсервицеадмин:: жетмсгсервицетабле** для загрузки таблицы служб в профиле для отображения в представлении.  <br/> |
   
## <a name="see-also"></a>См. также



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

