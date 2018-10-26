---
title: IMessageSetReadFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SetReadFlag
api_type:
- COM
ms.assetid: 2d02ebf6-bb8b-42bb-9bd0-870dbae9aeb4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 40815f1df597a8fb1fd8adef3dcc09323e946d30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592964"
---
# <a name="imessagesetreadflag"></a>IMessage::SetReadFlag

**Область применения**: Outlook 2013 | Outlook 2016 
  
Устанавливает или сбрасывает MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщения и управляет Отправка чтения отчеты.
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>���������

_ulFlags_
  
> [in] Битовую маску флагов, который управляет параметром чтение сообщения флаг, то есть отметку MSGFLAG_READ в своем свойстве **PR_MESSAGE_FLAGS** и функции обработки для просмотра отчетов. Можно задать следующие флажки: 
    
  - CLEAR_READ_FLAG: Флаг MSGFLAG_READ должен быть снят в **PR_MESSAGE_FLAGS** и чтения отчет не будут отправляться. 
      
  - CLEAR_NRN_PENDING: Флаг MSGFLAG_NRN_PENDING должен быть снят в **PR_MESSAGE_FLAGS** и не будут отправляться непрочтении отчета. 
      
  - CLEAR_RN_PENDING: Флаг MSGFLAG_RN_PENDING должен быть снят в **PR_MESSAGE_FLAGS** и чтения отчет не будут отправляться. 
      
  - GENERATE_RECEIPT_ONLY: Чтения отчет следует отправить один ожидающий, когда должно быть никаких изменений в состояние флага MSGFLAG_READ.
      
  - MAPI_DEFERRED_ERRORS: Разрешает **SetReadFlag** для возврата успешно, возможно до завершения операции. 
      
  - SUPPRESS_RECEIPT: Ожидающие чтения отчета должна быть отменена Если запрошен чтения отчета, и этот вызов изменяет состояние сообщения из непрочитанные сообщения для чтения. Если этот вызов не изменяет состояние сообщения, поставщик хранения сообщений можно игнорировать этот флаг.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Чтение отметку успешно установить или снять.
    
MAPI_E_NO_SUPPRESS 
  
> Поставщик хранения сообщения не поддерживает подавления чтения отчеты.
    
MAPI_E_INVALID_PARAMETER 
  
> Один из следующих комбинаций флаги задано с помощью параметра _ulFlags_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>Замечания

Метод **IMessage::SetReadFlag** устанавливает или сбрасывает MSGFLAG_READ сообщения в свойство **PR_MESSAGE_FLAGS** и вызовы [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сохранить сообщение. Установка флага MSGFLAG_READ помечает сообщения как читать, которое не обязательно означает, что получателю фактически имеет чтение сообщения. 
  
Кроме того, **SetReadFlags** управляет Отправка просмотра отчетов. Чтение отчета отправляется только в том случае, если отправитель запрашивает один. 
  
Чтение флаг не могут быть изменены для:
  
- Сообщения, не существует.
    
- Сообщения, которые были перемещены в другом месте.
    
- Сообщения, открытые с разрешением на чтение и запись.
    
- Сообщения, которые передаются в настоящее время.
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если ни один из флагов в параметре _ulFlags_ , применяются следующие правила: 
  
- Если MSGFLAG_READ уже задано, ничего не предпринимать.
    
- Если MSGFLAG_READ не установлен, установите его и отправить все ожидающие просмотра отчетов, если свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) имеет значение.
    
Если SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY флаги установлены, бит PR_READ_RECEIPT_REQUESTED, если задано, следует выполнить очистку и просмотра отчетов не будут отправляться.
  
Если задано флаг SUPPRESS_RECEIPT:
  
- Если MSGFLAG_READ уже задано, ничего не предпринимать. 
    
- Если MSGFLAG_READ не установлен, установите его и отменить ожидающие просмотра отчетов.
    
Если флаг CLEAR_READ_FLAG, снимите флаг MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** каждого сообщения и не отправлять чтения отчеты. 
  
Если для флага GENERATE_RECEIPT_ONLY, отправьте все ожидающие чтения отчеты. Выполните MSGFLAG_READ не установлен или clear.
  
Когда SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY флаги, присвойте свойству PR_READ_RECEIPT_REQUESTED значение FALSE, если оно установлено и не отправлять просмотра отчета.
  
Можно оптимизировать поведение отчет с подавлением Создание чтения отчетов в определенных условиях. Тем не менее если не поддерживают подавления отчеты и клиент вызывает **SetReadFlag** с установленным флагом SUPPRESS_RECEIPT, возвратите MAPI_E_NO_SUPPRESS. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |Mfcmapi (en) используется метод **IMessage::SetReadFlag** для задания чтения флаги для выбранного сообщения.  <br/> |
   
## <a name="see-also"></a>См. также

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md) 
- [IMessage: IMAPIProp](imessageimapiprop.md)
- [Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

