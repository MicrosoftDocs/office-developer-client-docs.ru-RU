---
title: IMsgServiceAdminDeleteMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.DeleteMsgService
api_type:
- COM
ms.assetid: 3a6b34eb-9d46-488f-8d02-91b27c35de67
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0a3021ed386aa00777694452a755693fc4078093
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809344"
---
# <a name="imsgserviceadmindeletemsgservice"></a>IMsgServiceAdmin::DeleteMsgService

  
  
**Относится к**: Outlook 
  
Удаление службы сообщений из профиля.
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a>Параметры

 _lpuid_
  
> [in] Указатель на структуру [MAPIUID](mapiuid.md) , который содержит уникальный идентификатор для службы сообщений для удаления. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Служба сообщений был удален.
    
MAPI_E_NOT_FOUND 
  
> **MAPIUID** , на который указывает _lpuid_ не соответствует существующую службу сообщений. 
    
## <a name="remarks"></a>Замечания

Метод **IMsgServiceAdmin::DeleteMsgService** удаляет службы сообщений из профиля. **DeleteMsgService** удаляет все разделы профилей, связанные со службой сообщений. 
  
 **DeleteMsgService** выполняет следующие действия, чтобы удалить службы сообщений: 
  
1. Вызывает функцию точки входа службы сообщений вместе с параметром _ulContext_ , равным MSG_SERVICE_DELETE перед удалением раздела профилей. Это позволяет службы для выполнения задач, используемых службой. 
    
2. Удаляет службу сообщений.
    
3. Удаление раздела профиля службы сообщений.
    
После удаления службы функцию точки входа службы сообщений не вызывает еще раз.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Для получения **MAPIUID** структуры для службы сообщений для удаления, получить столбец свойство **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) из службы сообщений строку в таблице службы сообщений. Для получения дополнительных сведений см процедуры, описанные в методе [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDeleteSelectedItem  <br/> |Mfcmapi (en) метод **IMsgServiceAdmin::DeleteMsgService** используется для удаления выбранного службы.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

