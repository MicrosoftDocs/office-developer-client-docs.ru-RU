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
ms.openlocfilehash: 588a32cb2a468c84dfc513af5e4abf6a9a1d0286
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809401"
---
# <a name="imsgserviceadmingetmsgservicetable"></a>IMsgServiceAdmin::GetMsgServiceTable

  
  
**Относится к**: Outlook 
  
Предоставляет доступ к таблице службы сообщений, список служб сообщения в профиле.
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Всегда имеет значение NULL.
    
 _lppTable_
  
> [out] Указатель на указатель в таблице службы сообщений.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> В таблице службы сообщение успешно возвращен.
    
## <a name="remarks"></a>Замечания

Метод **IMsgServiceAdmin::GetMsgServiceTable** предоставляет доступ к таблице службы сообщений, таблица, содержащая MAPI, в котором приведены службы сообщений, установленные в профиле сеанса. Полный список столбцов в таблице служб сообщения в разделе [Таблицы службы сообщений](message-service-tables.md).
  
В таблице службы сообщения является статическим. После клиента предоставлен доступ к нему, появившееся сообщение службы добавления или удаления не повлияет на его. Если в текущий профиль службы не сообщения, **GetMsgServiceTable** возвращает таблицу с нуля строк. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnRefreshView  <br/> |Mfcmapi (en) использует метод **IMsgServiceAdmin::GetMsgServiceTable** для загрузки в таблице службы профиля для отображения в представлении.  <br/> |
   
## <a name="see-also"></a>См. также



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

