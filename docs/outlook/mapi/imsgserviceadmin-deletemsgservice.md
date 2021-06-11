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
ms.openlocfilehash: 6cef03e33abab81a407698b73a007f247ef88194
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407384"
---
# <a name="imsgserviceadmindeletemsgservice"></a>IMsgServiceAdmin::DeleteMsgService

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет службу сообщений из профиля.
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a>Parameters

 _lpuid_
  
> [in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор для удаления службы сообщений. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Служба сообщений была удалена.
    
MAPI_E_NOT_FOUND 
  
> **MapIUID,** на который указывает _lpuid,_ не соответствует существующей службе сообщений. 
    
## <a name="remarks"></a>Примечания

Метод **IMsgServiceAdmin::D eleteMsgService** удаляет службу сообщений из профиля. **DeleteMsgService** удаляет все разделы профилей, связанные со службой сообщений. 
  
 **DeleteMsgService** выполняет следующие действия, чтобы удалить службу сообщений: 
  
1. Вызывает функцию точки входа службы сообщений с параметром  _ulContext_ MSG_SERVICE_DELETE до удаления разделов профилей. Это позволяет службе выполнять любые задачи, определенные для службы. 
    
2. Удаляет службу сообщений.
    
3. Удаляет раздел профилей службы сообщений.
    
Функция точки входа службы сообщений не вызвана после удаления службы.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы получить структуру **MAPIUID** для удаления службы **сообщений, извлеките** столбец свойства [PR_SERVICE_UID (PidTagServiceUid)](pidtagserviceuid-canonical-property.md)из строки службы сообщений в таблице службы сообщений. Дополнительные сведения см. в процедуре, описанной в методе [IMsgServiceAdmin::CreateMsgService.](imsgserviceadmin-createmsgservice.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDeleteSelectedItem  <br/> |MFCMAPI использует **метод IMsgServiceAdmin::D eleteMsgService** для удаления выбранной службы.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

