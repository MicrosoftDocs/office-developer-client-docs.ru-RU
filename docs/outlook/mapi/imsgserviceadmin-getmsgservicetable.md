---
title: IMsgServiceAdminGetMsgServiceTable
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
  
> [in] Всегда NULL.
    
 _lppTable_
  
> [out] Указатель на указатель на таблицу службы сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица службы сообщений успешно возвращена.
    
## <a name="remarks"></a>Примечания

Метод **IMsgServiceAdmin::GetMsgServiceTable** предоставляет доступ к таблице службы сообщений, которая поддерживается MAPI и содержит список служб сообщений, установленных в данный момент в профиле сеанса. Полный список столбцов в таблице службы сообщений см. в [таблице службы сообщений.](message-service-tables.md)
  
Таблица службы сообщений является статической. После того как клиент получит доступ к нему, последующие добавления или удаления службы сообщений не повлияют на него. Если в текущем профиле нет служб сообщений, **GetMsgServiceTable** возвращает таблицу с нулем строк. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnRefreshView  <br/> |MFCMAPI использует метод **IMsgServiceAdmin::GetMsgServiceTable** для загрузки таблицы служб в профиле для отображения в представлении.  <br/> |
   
## <a name="see-also"></a>См. также



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

